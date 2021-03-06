
---
title: "Group"
block_external_search_index: true
---



Provides an AutoScaling Group resource.

> **Note:** You must specify either `launch_configuration`, `launch_template`, or `mixed_instances_policy`.

{{% examples %}}
## Example Usage
{{% example %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const test = new aws.ec2.PlacementGroup("test", {
    strategy: "cluster",
});
const bar = new aws.autoscaling.Group("bar", {
    desiredCapacity: 4,
    forceDelete: true,
    healthCheckGracePeriod: 300,
    healthCheckType: "ELB",
    initialLifecycleHooks: [{
        defaultResult: "CONTINUE",
        heartbeatTimeout: 2000,
        lifecycleTransition: "autoscaling:EC2_INSTANCE_LAUNCHING",
        name: "foobar",
        notificationMetadata: `{
  "foo": "bar"
}
`,
        notificationTargetArn: "arn:aws:sqs:us-east-1:444455556666:queue1*",
        roleArn: "arn:aws:iam::123456789012:role/S3Access",
    }],
    launchConfiguration: aws_launch_configuration_foobar.name,
    maxSize: 5,
    minSize: 2,
    placementGroup: test.id,
    tags: [
        {
            key: "foo",
            propagateAtLaunch: true,
            value: "bar",
        },
        {
            key: "lorem",
            propagateAtLaunch: false,
            value: "ipsum",
        },
    ],
    vpcZoneIdentifiers: [
        aws_subnet_example1.id,
        aws_subnet_example2.id,
    ],
}, { timeouts: {
    delete: "15m",
} });
```

{{% /example %}}
{{% example %}}
### With Latest Version Of Launch Template

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const foobar = new aws.ec2.LaunchTemplate("foobar", {
    imageId: "ami-1a2b3c",
    instanceType: "t2.micro",
    namePrefix: "foobar",
});
const bar = new aws.autoscaling.Group("bar", {
    availabilityZones: ["us-east-1a"],
    desiredCapacity: 1,
    launchTemplate: {
        id: foobar.id,
        version: "$Latest",
    },
    maxSize: 1,
    minSize: 1,
});
```

{{% /example %}}
{{% example %}}
### Mixed Instances Policy

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const exampleLaunchTemplate = new aws.ec2.LaunchTemplate("example", {
    imageId: aws_ami_example.id,
    instanceType: "c5.large",
    namePrefix: "example",
});
const exampleGroup = new aws.autoscaling.Group("example", {
    availabilityZones: ["us-east-1a"],
    desiredCapacity: 1,
    maxSize: 1,
    minSize: 1,
    mixedInstancesPolicy: {
        launchTemplate: {
            launchTemplateSpecification: {
                launchTemplateId: exampleLaunchTemplate.id,
            },
            overrides: [
                {
                    instanceType: "c4.large",
                    weightedCapacity: "3",
                },
                {
                    instanceType: "c3.large",
                    weightedCapacity: "2",
                },
            ],
        },
    },
});
```

{{% /example %}}
{{% /examples %}}
## Interpolated tags

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const config = new pulumi.Config();
const extraTags = config.get("extraTags") || [
    {
        key: "Foo",
        propagateAtLaunch: true,
        value: "Bar",
    },
    {
        key: "Baz",
        propagateAtLaunch: true,
        value: "Bam",
    },
];

const bar = new aws.autoscaling.Group("bar", {
    launchConfiguration: aws_launch_configuration_foobar.name,
    maxSize: 5,
    minSize: 2,
    tagsCollection: [{"key": "interpolation1", "value": "value3", "propagate_at_launch": true}, {"key": "interpolation2", "value": "value4", "propagate_at_launch": true}].concat(extraTags),
    vpcZoneIdentifiers: [
        aws_subnet_example1.id,
        aws_subnet_example2.id,
    ],
});
```

## Waiting for Capacity

A newly-created ASG is initially empty and begins to scale to `min_size` (or
`desired_capacity`, if specified) by launching instances using the provided
Launch Configuration. These instances take time to launch and boot.

On ASG Update, changes to these values also take time to result in the target
number of instances providing service.

This provider provides two mechanisms to help consistently manage ASG scale up
time across dependent resources.

#### Waiting for ASG Capacity

The first is default behavior. This provider waits after ASG creation for
`min_size` (or `desired_capacity`, if specified) healthy instances to show up
in the ASG before continuing.

If `min_size` or `desired_capacity` are changed in a subsequent update,
this provider will also wait for the correct number of healthy instances before
continuing.

This provider considers an instance "healthy" when the ASG reports `HealthStatus:
"Healthy"` and `LifecycleState: "InService"`. See the [AWS AutoScaling
Docs](https://docs.aws.amazon.com/AutoScaling/latest/DeveloperGuide/AutoScalingGroupLifecycle.html)
for more information on an ASG's lifecycle.

This provider will wait for healthy instances for up to
`wait_for_capacity_timeout`. If ASG creation is taking more than a few minutes,
it's worth investigating for scaling activity errors, which can be caused by
problems with the selected Launch Configuration.

Setting `wait_for_capacity_timeout` to `"0"` disables ASG Capacity waiting.

#### Waiting for ELB Capacity

The second mechanism is optional, and affects ASGs with attached ELBs specified
via the `load_balancers` attribute or with ALBs specified with `target_group_arns`.

The `min_elb_capacity` parameter causes this provider to wait for at least the
requested number of instances to show up `"InService"` in all attached ELBs
during ASG creation.  It has no effect on ASG updates.

If `wait_for_elb_capacity` is set, this provider will wait for exactly that number
of Instances to be `"InService"` in all attached ELBs on both creation and
updates.

These parameters can be used to ensure that service is being provided before
this provider moves on. If new instances don't pass the ELB's health checks for any
reason, the deployment will time out, and the ASG will be marked as
tainted (i.e. marked to be destroyed in a follow up run).

As with ASG Capacity, this provider will wait for up to `wait_for_capacity_timeout`
for the proper number of instances to be healthy.

#### Troubleshooting Capacity Waiting Timeouts

If ASG creation takes more than a few minutes, this could indicate one of a
number of configuration problems. See the [AWS Docs on Load Balancer
Troubleshooting](https://docs.aws.amazon.com/ElasticLoadBalancing/latest/DeveloperGuide/elb-troubleshooting.html)
for more information.



## Create a Group Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/autoscaling/#Group">Group</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/autoscaling/#GroupArgs">GroupArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Group</span><span class="p">(resource_name, opts=None, </span>availability_zones=None<span class="p">, </span>default_cooldown=None<span class="p">, </span>desired_capacity=None<span class="p">, </span>enabled_metrics=None<span class="p">, </span>force_delete=None<span class="p">, </span>health_check_grace_period=None<span class="p">, </span>health_check_type=None<span class="p">, </span>initial_lifecycle_hooks=None<span class="p">, </span>launch_configuration=None<span class="p">, </span>launch_template=None<span class="p">, </span>load_balancers=None<span class="p">, </span>max_instance_lifetime=None<span class="p">, </span>max_size=None<span class="p">, </span>metrics_granularity=None<span class="p">, </span>min_elb_capacity=None<span class="p">, </span>min_size=None<span class="p">, </span>mixed_instances_policy=None<span class="p">, </span>name=None<span class="p">, </span>name_prefix=None<span class="p">, </span>placement_group=None<span class="p">, </span>protect_from_scale_in=None<span class="p">, </span>service_linked_role_arn=None<span class="p">, </span>suspended_processes=None<span class="p">, </span>tags=None<span class="p">, </span>tags_collection=None<span class="p">, </span>target_group_arns=None<span class="p">, </span>termination_policies=None<span class="p">, </span>vpc_zone_identifiers=None<span class="p">, </span>wait_for_capacity_timeout=None<span class="p">, </span>wait_for_elb_capacity=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewGroup<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupArgs">GroupArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#Group">Group</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Autoscaling.Group.html">Group</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.AutoScaling.GroupArgs.html">GroupArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

#### Resource Arguments




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Availability<wbr>Zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled<wbr>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Force<wbr>Delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Health<wbr>Check<wbr>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Health<wbr>Check<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Initial<wbr>Lifecycle<wbr>Hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">List&lt;Group<wbr>Initial<wbr>Lifecycle<wbr>Hook<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">Group<wbr>Launch<wbr>Template<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Instance<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metrics<wbr>Granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mixed<wbr>Instances<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Placement<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protect<wbr>From<wbr>Scale<wbr>In</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Linked<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Suspended<wbr>Processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">List&lt;Group<wbr>Tag<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags<wbr>Collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<ImmutableDictionary<string, object>>?</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Group<wbr>Arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Termination<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpc<wbr>Zone<wbr>Identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Capacity<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Availability<wbr>Zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled<wbr>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Force<wbr>Delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Health<wbr>Check<wbr>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Health<wbr>Check<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Initial<wbr>Lifecycle<wbr>Hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">[]Group<wbr>Initial<wbr>Lifecycle<wbr>Hook</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">interface{}</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">*Group<wbr>Launch<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Instance<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metrics<wbr>Granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">interface{}</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mixed<wbr>Instances<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">*Group<wbr>Mixed<wbr>Instances<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Placement<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">interface{}</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protect<wbr>From<wbr>Scale<wbr>In</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Linked<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Suspended<wbr>Processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">[]Group<wbr>Tag</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags<wbr>Collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Group<wbr>Arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Termination<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpc<wbr>Zone<wbr>Identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Capacity<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>availability<wbr>Zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled<wbr>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">Metric[]?</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>force<wbr>Delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>health<wbr>Check<wbr>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>health<wbr>Check<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>initial<wbr>Lifecycle<wbr>Hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">Group<wbr>Initial<wbr>Lifecycle<wbr>Hook[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | LaunchConfiguration</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">Group<wbr>Launch<wbr>Template?</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load<wbr>Balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Instance<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metrics<wbr>Granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | MetricsGranularity</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mixed<wbr>Instances<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">Group<wbr>Mixed<wbr>Instances<wbr>Policy?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>placement<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | PlacementGroup</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protect<wbr>From<wbr>Scale<wbr>In</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Linked<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>suspended<wbr>Processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">Group<wbr>Tag[]?</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags<wbr>Collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}[]?</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Group<wbr>Arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>termination<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpc<wbr>Zone<wbr>Identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait<wbr>For<wbr>Capacity<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait<wbr>For<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>availability_<wbr>zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default_<wbr>cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled_<wbr>metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Metric]</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>force_<wbr>delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>health_<wbr>check_<wbr>grace_<wbr>period</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>health_<wbr>check_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>initial_<wbr>lifecycle_<wbr>hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">List[Group<wbr>Initial<wbr>Lifecycle<wbr>Hook]</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch_<wbr>template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">Dict[Group<wbr>Launch<wbr>Template]</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load_<wbr>balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>instance_<wbr>lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>max_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metrics_<wbr>granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min_<wbr>elb_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>min_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mixed_<wbr>instances_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">Dict[Group<wbr>Mixed<wbr>Instances<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name_<wbr>prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>placement_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protect_<wbr>from_<wbr>scale_<wbr>in</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service_<wbr>linked_<wbr>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>suspended_<wbr>processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">List[Group<wbr>Tag]</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags_<wbr>collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Any>]</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target_<wbr>group_<wbr>arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>termination_<wbr>policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpc_<wbr>zone_<wbr>identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait_<wbr>for_<wbr>capacity_<wbr>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait_<wbr>for_<wbr>elb_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Group Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN for this AutoScaling Group
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Availability<wbr>Zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Default<wbr>Cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enabled<wbr>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Force<wbr>Delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Health<wbr>Check<wbr>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Health<wbr>Check<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Initial<wbr>Lifecycle<wbr>Hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">List&lt;Group<wbr>Initial<wbr>Lifecycle<wbr>Hook&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Launch<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">Group<wbr>Launch<wbr>Template?</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Load<wbr>Balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Max<wbr>Instance<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metrics<wbr>Granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Min<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Mixed<wbr>Instances<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">Group<wbr>Mixed<wbr>Instances<wbr>Policy?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Placement<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Protect<wbr>From<wbr>Scale<wbr>In</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Service<wbr>Linked<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Suspended<wbr>Processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">List&lt;Group<wbr>Tag&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags<wbr>Collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<ImmutableDictionary<string, object>>?</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Target<wbr>Group<wbr>Arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Termination<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vpc<wbr>Zone<wbr>Identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Wait<wbr>For<wbr>Capacity<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Wait<wbr>For<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN for this AutoScaling Group
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Availability<wbr>Zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Default<wbr>Cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enabled<wbr>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Force<wbr>Delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Health<wbr>Check<wbr>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Health<wbr>Check<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Initial<wbr>Lifecycle<wbr>Hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">[]Group<wbr>Initial<wbr>Lifecycle<wbr>Hook</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Launch<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">*Group<wbr>Launch<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Load<wbr>Balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Max<wbr>Instance<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metrics<wbr>Granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Min<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Mixed<wbr>Instances<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">*Group<wbr>Mixed<wbr>Instances<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Placement<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Protect<wbr>From<wbr>Scale<wbr>In</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Service<wbr>Linked<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Suspended<wbr>Processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">[]Group<wbr>Tag</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags<wbr>Collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Target<wbr>Group<wbr>Arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Termination<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vpc<wbr>Zone<wbr>Identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Wait<wbr>For<wbr>Capacity<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Wait<wbr>For<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN for this AutoScaling Group
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>availability<wbr>Zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>default<wbr>Cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enabled<wbr>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">Metric[]?</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>force<wbr>Delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>health<wbr>Check<wbr>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>health<wbr>Check<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>initial<wbr>Lifecycle<wbr>Hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">Group<wbr>Initial<wbr>Lifecycle<wbr>Hook[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>launch<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">Group<wbr>Launch<wbr>Template?</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>load<wbr>Balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>max<wbr>Instance<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metrics<wbr>Granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>min<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>mixed<wbr>Instances<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">Group<wbr>Mixed<wbr>Instances<wbr>Policy?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>placement<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>protect<wbr>From<wbr>Scale<wbr>In</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>service<wbr>Linked<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>suspended<wbr>Processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">Group<wbr>Tag[]?</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags<wbr>Collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}[]?</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>target<wbr>Group<wbr>Arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>termination<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vpc<wbr>Zone<wbr>Identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>wait<wbr>For<wbr>Capacity<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>wait<wbr>For<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN for this AutoScaling Group
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>availability_<wbr>zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>default_<wbr>cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>desired_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enabled_<wbr>metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Metric]</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>force_<wbr>delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>health_<wbr>check_<wbr>grace_<wbr>period</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>health_<wbr>check_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>initial_<wbr>lifecycle_<wbr>hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">List[Group<wbr>Initial<wbr>Lifecycle<wbr>Hook]</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>launch_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>launch_<wbr>template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">Dict[Group<wbr>Launch<wbr>Template]</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>load_<wbr>balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>max_<wbr>instance_<wbr>lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>max_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metrics_<wbr>granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>min_<wbr>elb_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>min_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>mixed_<wbr>instances_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">Dict[Group<wbr>Mixed<wbr>Instances<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name_<wbr>prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>placement_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>protect_<wbr>from_<wbr>scale_<wbr>in</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>service_<wbr>linked_<wbr>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>suspended_<wbr>processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">List[Group<wbr>Tag]</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags_<wbr>collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Any>]</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>target_<wbr>group_<wbr>arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>termination_<wbr>policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vpc_<wbr>zone_<wbr>identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>wait_<wbr>for_<wbr>capacity_<wbr>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>wait_<wbr>for_<wbr>elb_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Group Resource

Get an existing Group resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/autoscaling/#GroupState">GroupState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/autoscaling/#Group">Group</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>arn=None<span class="p">, </span>availability_zones=None<span class="p">, </span>default_cooldown=None<span class="p">, </span>desired_capacity=None<span class="p">, </span>enabled_metrics=None<span class="p">, </span>force_delete=None<span class="p">, </span>health_check_grace_period=None<span class="p">, </span>health_check_type=None<span class="p">, </span>initial_lifecycle_hooks=None<span class="p">, </span>launch_configuration=None<span class="p">, </span>launch_template=None<span class="p">, </span>load_balancers=None<span class="p">, </span>max_instance_lifetime=None<span class="p">, </span>max_size=None<span class="p">, </span>metrics_granularity=None<span class="p">, </span>min_elb_capacity=None<span class="p">, </span>min_size=None<span class="p">, </span>mixed_instances_policy=None<span class="p">, </span>name=None<span class="p">, </span>name_prefix=None<span class="p">, </span>placement_group=None<span class="p">, </span>protect_from_scale_in=None<span class="p">, </span>service_linked_role_arn=None<span class="p">, </span>suspended_processes=None<span class="p">, </span>tags=None<span class="p">, </span>tags_collection=None<span class="p">, </span>target_group_arns=None<span class="p">, </span>termination_policies=None<span class="p">, </span>vpc_zone_identifiers=None<span class="p">, </span>wait_for_capacity_timeout=None<span class="p">, </span>wait_for_elb_capacity=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetGroup<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupState">GroupState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#Group">Group</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Autoscaling.Group.html">Group</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Autoscaling.GroupState.html">GroupState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN for this AutoScaling Group
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Availability<wbr>Zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled<wbr>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Force<wbr>Delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Health<wbr>Check<wbr>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Health<wbr>Check<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Initial<wbr>Lifecycle<wbr>Hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">List&lt;Group<wbr>Initial<wbr>Lifecycle<wbr>Hook<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">Group<wbr>Launch<wbr>Template<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Instance<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metrics<wbr>Granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mixed<wbr>Instances<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Placement<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protect<wbr>From<wbr>Scale<wbr>In</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Linked<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Suspended<wbr>Processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">List&lt;Group<wbr>Tag<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags<wbr>Collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<ImmutableDictionary<string, object>>?</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Group<wbr>Arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Termination<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpc<wbr>Zone<wbr>Identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Capacity<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN for this AutoScaling Group
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Availability<wbr>Zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled<wbr>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Force<wbr>Delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Health<wbr>Check<wbr>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Health<wbr>Check<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Initial<wbr>Lifecycle<wbr>Hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">[]Group<wbr>Initial<wbr>Lifecycle<wbr>Hook</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">interface{}</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">*Group<wbr>Launch<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Instance<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metrics<wbr>Granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">interface{}</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mixed<wbr>Instances<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">*Group<wbr>Mixed<wbr>Instances<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Placement<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">interface{}</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protect<wbr>From<wbr>Scale<wbr>In</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Linked<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Suspended<wbr>Processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">[]Group<wbr>Tag</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags<wbr>Collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Group<wbr>Arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Termination<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpc<wbr>Zone<wbr>Identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Capacity<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN for this AutoScaling Group
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>availability<wbr>Zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled<wbr>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">Metric[]?</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>force<wbr>Delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>health<wbr>Check<wbr>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>health<wbr>Check<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>initial<wbr>Lifecycle<wbr>Hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">Group<wbr>Initial<wbr>Lifecycle<wbr>Hook[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | LaunchConfiguration</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">Group<wbr>Launch<wbr>Template?</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load<wbr>Balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Instance<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metrics<wbr>Granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | MetricsGranularity</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mixed<wbr>Instances<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">Group<wbr>Mixed<wbr>Instances<wbr>Policy?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>placement<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | PlacementGroup</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protect<wbr>From<wbr>Scale<wbr>In</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Linked<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>suspended<wbr>Processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">Group<wbr>Tag[]?</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags<wbr>Collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}[]?</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Group<wbr>Arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>termination<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpc<wbr>Zone<wbr>Identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait<wbr>For<wbr>Capacity<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait<wbr>For<wbr>Elb<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN for this AutoScaling Group
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>availability_<wbr>zones</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of one or more availability zones for the group. This parameter should not be specified when using `vpc_zone_identifier`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default_<wbr>cooldown</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The amount of time, in seconds, after a scaling activity completes before another scaling activity can start.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of Amazon EC2 instances that
should be running in the group. (See also Waiting for
Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled_<wbr>metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Metric]</span>
    </dt>
    <dd>{{% md %}}A list of metrics to collect. The allowed values are `GroupDesiredCapacity`, `GroupInServiceCapacity`, `GroupPendingCapacity`, `GroupMinSize`, `GroupMaxSize`, `GroupInServiceInstances`, `GroupPendingInstances`, `GroupStandbyInstances`, `GroupStandbyCapacity`, `GroupTerminatingCapacity`, `GroupTerminatingInstances`, `GroupTotalCapacity`, `GroupTotalInstances`.
* `wait_for_capacity_timeout` (Default: "10m") A maximum
[duration](https://golang.org/pkg/time/#ParseDuration) that this provider should
wait for ASG instances to be healthy before timing out.  (See also Waiting
for Capacity below.) Setting this to "0" causes
this provider to skip all Capacity Waiting behavior.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>force_<wbr>delete</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allows deleting the autoscaling group without waiting
for all instances in the pool to terminate.  You can force an autoscaling group to delete
even if it's in the process of scaling a resource. Normally, this provider
drains all the instances before deleting the group.  This bypasses that
behavior and potentially leaves resources dangling.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>health_<wbr>check_<wbr>grace_<wbr>period</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Time (in seconds) after instance comes into service before checking health.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>health_<wbr>check_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}"EC2" or "ELB". Controls how health checking is done.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>initial_<wbr>lifecycle_<wbr>hooks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupinitiallifecyclehook">List[Group<wbr>Initial<wbr>Lifecycle<wbr>Hook]</a></span>
    </dt>
    <dd>{{% md %}}One or more
[Lifecycle Hooks](http://docs.aws.amazon.com/autoscaling/latest/userguide/lifecycle-hooks.html)
to attach to the autoscaling group **before** instances are launched. The
syntax is exactly the same as the separate
[`aws.autoscaling.LifecycleHook`](https://www.terraform.io/docs/providers/aws/r/autoscaling_lifecycle_hook.html)
resource, without the `autoscaling_group_name` attribute. Please note that this will only work when creating
a new autoscaling group. For all other use-cases, please use `aws.autoscaling.LifecycleHook` resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The name of the launch configuration to use.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch_<wbr>template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouplaunchtemplate">Dict[Group<wbr>Launch<wbr>Template]</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load_<wbr>balancers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of elastic load balancer names to add to the autoscaling
group names. Only valid for classic load balancers. For ALBs, use `target_group_arns` instead.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>instance_<wbr>lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum amount of time, in seconds, that an instance can be in service, values must be either equal to 0 or between 604800 and 31536000 seconds.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum size of the auto scale group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metrics_<wbr>granularity</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The granularity to associate with the metrics to collect. The only valid value is `1Minute`. Default is `1Minute`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min_<wbr>elb_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Setting this causes this provider to wait for
this number of instances from this autoscaling group to show up healthy in the
ELB only on creation. Updates will not wait on ELB instance number changes.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum size of the auto scale group.
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mixed_<wbr>instances_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicy">Dict[Group<wbr>Mixed<wbr>Instances<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block containing settings to define launch targets for Auto Scaling groups. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name_<wbr>prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Creates a unique name beginning with the specified
prefix. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>placement_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The name of the placement group into which you'll launch your instances, if any.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protect_<wbr>from_<wbr>scale_<wbr>in</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allows setting instance protection. The
autoscaling group will not select instances with this setting for terminination
during scale in events.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service_<wbr>linked_<wbr>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the service-linked role that the ASG will use to call other AWS services
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>suspended_<wbr>processes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of processes to suspend for the AutoScaling Group. The allowed values are `Launch`, `Terminate`, `HealthCheck`, `ReplaceUnhealthy`, `AZRebalance`, `AlarmNotification`, `ScheduledActions`, `AddToLoadBalancer`.
Note that if you suspend either the `Launch` or `Terminate` process types, it can prevent your autoscaling group from functioning properly.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#grouptag">List[Group<wbr>Tag]</a></span>
    </dt>
    <dd>{{% md %}}A list of tag blocks. Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags_<wbr>collection</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Any>]</span>
    </dt>
    <dd>{{% md %}}A list of tag blocks (maps). Tags documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target_<wbr>group_<wbr>arns</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of `aws.alb.TargetGroup` ARNs, for use with Application or Network Load Balancing.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>termination_<wbr>policies</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of policies to decide how the instances in the auto scale group should be terminated. The allowed values are `OldestInstance`, `NewestInstance`, `OldestLaunchConfiguration`, `ClosestToNextInstanceHour`, `OldestLaunchTemplate`, `AllocationStrategy`, `Default`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpc_<wbr>zone_<wbr>identifiers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of subnet IDs to launch resources in.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait_<wbr>for_<wbr>capacity_<wbr>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait_<wbr>for_<wbr>elb_<wbr>capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Setting this will cause this provider to wait
for exactly this number of healthy instances from this autoscaling group in
all attached load balancers on both create and update operations. (Takes
precedence over `min_elb_capacity` behavior.)
(See also Waiting for Capacity below.)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Group<wbr>Initial<wbr>Lifecycle<wbr>Hook</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupInitialLifecycleHook">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GroupInitialLifecycleHook">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupInitialLifecycleHookArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupInitialLifecycleHookOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Result</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Heartbeat<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Lifecycle<wbr>Transition</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Notification<wbr>Metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Notification<wbr>Target<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Result</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Heartbeat<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Lifecycle<wbr>Transition</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Notification<wbr>Metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Notification<wbr>Target<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Result</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>heartbeat<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>lifecycle<wbr>Transition</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>notification<wbr>Metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>notification<wbr>Target<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>default_<wbr>result</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>heartbeat_<wbr>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>lifecycle_<wbr>transition</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>notification_<wbr>metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>notification_<wbr>target_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Group<wbr>Launch<wbr>Template</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupLaunchTemplate">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GroupLaunchTemplate">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupLaunchTemplateArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupLaunchTemplateOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the launch template. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Template version. Can be version number, `$Latest`, or `$Default`. (Default: `$Default`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the launch template. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Template version. Can be version number, `$Latest`, or `$Default`. (Default: `$Default`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the launch template. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Template version. Can be version number, `$Latest`, or `$Default`. (Default: `$Default`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the launch template. Conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the auto scaling group. By default generated by this provider.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Template version. Can be version number, `$Latest`, or `$Default`. (Default: `$Default`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Group<wbr>Mixed<wbr>Instances<wbr>Policy</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupMixedInstancesPolicy">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GroupMixedInstancesPolicy">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Instances<wbr>Distribution</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicyinstancesdistribution">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Instances<wbr>Distribution<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing settings on how to mix on-demand and Spot instances in the Auto Scaling group. Defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplate">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Instances<wbr>Distribution</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicyinstancesdistribution">*Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Instances<wbr>Distribution</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing settings on how to mix on-demand and Spot instances in the Auto Scaling group. Defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplate">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>instances<wbr>Distribution</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicyinstancesdistribution">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Instances<wbr>Distribution?</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing settings on how to mix on-demand and Spot instances in the Auto Scaling group. Defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>launch<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplate">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>instances<wbr>Distribution</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicyinstancesdistribution">Dict[Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Instances<wbr>Distribution]</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing settings on how to mix on-demand and Spot instances in the Auto Scaling group. Defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>launch_<wbr>template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplate">Dict[Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template]</a></span>
    </dt>
    <dd>{{% md %}}Nested argument containing launch template settings along with the overrides to specify multiple instance types and weights. Defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Instances<wbr>Distribution</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupMixedInstancesPolicyInstancesDistribution">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GroupMixedInstancesPolicyInstancesDistribution">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyInstancesDistributionArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyInstancesDistributionOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Demand<wbr>Allocation<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Strategy to use when launching on-demand instances. Valid values: `prioritized`. Default: `prioritized`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Demand<wbr>Base<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Absolute minimum amount of desired capacity that must be fulfilled by on-demand instances. Default: `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Demand<wbr>Percentage<wbr>Above<wbr>Base<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Percentage split between on-demand and Spot instances above the base on-demand capacity. Default: `100`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Spot<wbr>Allocation<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}How to allocate capacity across the Spot pools. Valid values: `lowest-price`, `capacity-optimized`. Default: `lowest-price`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Spot<wbr>Instance<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Number of Spot pools per availability zone to allocate capacity. EC2 Auto Scaling selects the cheapest Spot pools and evenly allocates Spot capacity across the number of Spot pools that you specify. Default: `2`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Spot<wbr>Max<wbr>Price</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Maximum price per unit hour that the user is willing to pay for the Spot instances. Default: an empty string which means the on-demand price.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Demand<wbr>Allocation<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Strategy to use when launching on-demand instances. Valid values: `prioritized`. Default: `prioritized`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Demand<wbr>Base<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Absolute minimum amount of desired capacity that must be fulfilled by on-demand instances. Default: `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Demand<wbr>Percentage<wbr>Above<wbr>Base<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Percentage split between on-demand and Spot instances above the base on-demand capacity. Default: `100`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Spot<wbr>Allocation<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}How to allocate capacity across the Spot pools. Valid values: `lowest-price`, `capacity-optimized`. Default: `lowest-price`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Spot<wbr>Instance<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Number of Spot pools per availability zone to allocate capacity. EC2 Auto Scaling selects the cheapest Spot pools and evenly allocates Spot capacity across the number of Spot pools that you specify. Default: `2`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Spot<wbr>Max<wbr>Price</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Maximum price per unit hour that the user is willing to pay for the Spot instances. Default: an empty string which means the on-demand price.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Demand<wbr>Allocation<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Strategy to use when launching on-demand instances. Valid values: `prioritized`. Default: `prioritized`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Demand<wbr>Base<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Absolute minimum amount of desired capacity that must be fulfilled by on-demand instances. Default: `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Demand<wbr>Percentage<wbr>Above<wbr>Base<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Percentage split between on-demand and Spot instances above the base on-demand capacity. Default: `100`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>spot<wbr>Allocation<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}How to allocate capacity across the Spot pools. Valid values: `lowest-price`, `capacity-optimized`. Default: `lowest-price`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>spot<wbr>Instance<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Number of Spot pools per availability zone to allocate capacity. EC2 Auto Scaling selects the cheapest Spot pools and evenly allocates Spot capacity across the number of Spot pools that you specify. Default: `2`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>spot<wbr>Max<wbr>Price</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Maximum price per unit hour that the user is willing to pay for the Spot instances. Default: an empty string which means the on-demand price.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Demand<wbr>Allocation<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Strategy to use when launching on-demand instances. Valid values: `prioritized`. Default: `prioritized`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Demand<wbr>Base<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Absolute minimum amount of desired capacity that must be fulfilled by on-demand instances. Default: `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Demand<wbr>Percentage<wbr>Above<wbr>Base<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Percentage split between on-demand and Spot instances above the base on-demand capacity. Default: `100`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>spot<wbr>Allocation<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}How to allocate capacity across the Spot pools. Valid values: `lowest-price`, `capacity-optimized`. Default: `lowest-price`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>spot<wbr>Instance<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Number of Spot pools per availability zone to allocate capacity. EC2 Auto Scaling selects the cheapest Spot pools and evenly allocates Spot capacity across the number of Spot pools that you specify. Default: `2`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>spot<wbr>Max<wbr>Price</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Maximum price per unit hour that the user is willing to pay for the Spot instances. Default: an empty string which means the on-demand price.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupMixedInstancesPolicyLaunchTemplate">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GroupMixedInstancesPolicyLaunchTemplate">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyLaunchTemplateArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyLaunchTemplateOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Launch<wbr>Template<wbr>Specification</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplatelaunchtemplatespecification">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Launch<wbr>Template<wbr>Specification<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}Nested argument defines the Launch Template. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Overrides</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplateoverride">List&lt;Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Override<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}List of nested arguments provides the ability to specify multiple instance types. This will override the same parameter in the launch template. For on-demand instances, Auto Scaling considers the order of preference of instance types to launch based on the order specified in the overrides list. Defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Launch<wbr>Template<wbr>Specification</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplatelaunchtemplatespecification">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Launch<wbr>Template<wbr>Specification</a></span>
    </dt>
    <dd>{{% md %}}Nested argument defines the Launch Template. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Overrides</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplateoverride">[]Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Override</a></span>
    </dt>
    <dd>{{% md %}}List of nested arguments provides the ability to specify multiple instance types. This will override the same parameter in the launch template. For on-demand instances, Auto Scaling considers the order of preference of instance types to launch based on the order specified in the overrides list. Defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>launch<wbr>Template<wbr>Specification</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplatelaunchtemplatespecification">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Launch<wbr>Template<wbr>Specification</a></span>
    </dt>
    <dd>{{% md %}}Nested argument defines the Launch Template. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>overrides</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplateoverride">Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Override[]?</a></span>
    </dt>
    <dd>{{% md %}}List of nested arguments provides the ability to specify multiple instance types. This will override the same parameter in the launch template. For on-demand instances, Auto Scaling considers the order of preference of instance types to launch based on the order specified in the overrides list. Defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>launch<wbr>Template<wbr>Specification</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplatelaunchtemplatespecification">Dict[Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Launch<wbr>Template<wbr>Specification]</a></span>
    </dt>
    <dd>{{% md %}}Nested argument defines the Launch Template. Defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>overrides</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#groupmixedinstancespolicylaunchtemplateoverride">List[Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Override]</a></span>
    </dt>
    <dd>{{% md %}}List of nested arguments provides the ability to specify multiple instance types. This will override the same parameter in the launch template. For on-demand instances, Auto Scaling considers the order of preference of instance types to launch based on the order specified in the overrides list. Defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Launch<wbr>Template<wbr>Specification</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupMixedInstancesPolicyLaunchTemplateLaunchTemplateSpecification">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GroupMixedInstancesPolicyLaunchTemplateLaunchTemplateSpecification">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyLaunchTemplateLaunchTemplateSpecificationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyLaunchTemplateLaunchTemplateSpecificationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the launch template. Conflicts with `launch_template_name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Template<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the launch template. Conflicts with `launch_template_id`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Template version. Can be version number, `$Latest`, or `$Default`. (Default: `$Default`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the launch template. Conflicts with `launch_template_name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Launch<wbr>Template<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the launch template. Conflicts with `launch_template_id`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Template version. Can be version number, `$Latest`, or `$Default`. (Default: `$Default`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>launch<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the launch template. Conflicts with `launch_template_name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch<wbr>Template<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the launch template. Conflicts with `launch_template_id`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Template version. Can be version number, `$Latest`, or `$Default`. (Default: `$Default`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>launch<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the launch template. Conflicts with `launch_template_name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>launch<wbr>Template<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the launch template. Conflicts with `launch_template_id`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Template version. Can be version number, `$Latest`, or `$Default`. (Default: `$Default`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Group<wbr>Mixed<wbr>Instances<wbr>Policy<wbr>Launch<wbr>Template<wbr>Override</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupMixedInstancesPolicyLaunchTemplateOverride">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GroupMixedInstancesPolicyLaunchTemplateOverride">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyLaunchTemplateOverrideArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupMixedInstancesPolicyLaunchTemplateOverrideOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Override the instance type in the Launch Template.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Weighted<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of capacity units, which gives the instance type a proportional weight to other instance types.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Override the instance type in the Launch Template.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Weighted<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The number of capacity units, which gives the instance type a proportional weight to other instance types.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Override the instance type in the Launch Template.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>weighted<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of capacity units, which gives the instance type a proportional weight to other instance types.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>instance_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Override the instance type in the Launch Template.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>weighted<wbr>Capacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The number of capacity units, which gives the instance type a proportional weight to other instance types.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Group<wbr>Tag</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GroupTag">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GroupTag">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupTagArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/autoscaling?tab=doc#GroupTagOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Key
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Propagate<wbr>At<wbr>Launch</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enables propagation of the tag to
Amazon EC2 instances launched via this ASG
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Key
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Propagate<wbr>At<wbr>Launch</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enables propagation of the tag to
Amazon EC2 instances launched via this ASG
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Key
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>propagate<wbr>At<wbr>Launch</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Enables propagation of the tag to
Amazon EC2 instances launched via this ASG
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Key
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>propagate<wbr>At<wbr>Launch</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enables propagation of the tag to
Amazon EC2 instances launched via this ASG
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Value
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    <dt>Notes</dt>
	<dd>This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).</dd>
</dl>

