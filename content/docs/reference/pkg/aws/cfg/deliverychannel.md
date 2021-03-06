
---
title: "DeliveryChannel"
block_external_search_index: true
---



Provides an AWS Config Delivery Channel.

> **Note:** Delivery Channel requires a [Configuration Recorder](https://www.terraform.io/docs/providers/aws/r/config_configuration_recorder.html) to be present. Use of `depends_on` (as shown below) is recommended to avoid race conditions.

{{% examples %}}
## Example Usage
{{% example %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const bucket = new aws.s3.Bucket("b", {
    forceDestroy: true,
});
const role = new aws.iam.Role("r", {
    assumeRolePolicy: `{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Action": "sts:AssumeRole",
      "Principal": {
        "Service": "config.amazonaws.com"
      },
      "Effect": "Allow",
      "Sid": ""
    }
  ]
}
`,
});
const fooRecorder = new aws.cfg.Recorder("foo", {
    roleArn: role.arn,
});
const fooDeliveryChannel = new aws.cfg.DeliveryChannel("foo", {
    s3BucketName: bucket.bucket,
}, { dependsOn: [fooRecorder] });
const rolePolicy = new aws.iam.RolePolicy("p", {
    policy: pulumi.interpolate`{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Action": [
        "s3:*"
      ],
      "Effect": "Allow",
      "Resource": [
        "${bucket.arn}",
        "${bucket.arn}/*"
      ]
    }
  ]
}
`,
    role: role.id,
});
```

{{% /example %}}
{{% /examples %}}



## Create a DeliveryChannel Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/cfg/#DeliveryChannel">DeliveryChannel</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/cfg/#DeliveryChannelArgs">DeliveryChannelArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">DeliveryChannel</span><span class="p">(resource_name, opts=None, </span>name=None<span class="p">, </span>s3_bucket_name=None<span class="p">, </span>s3_key_prefix=None<span class="p">, </span>snapshot_delivery_properties=None<span class="p">, </span>sns_topic_arn=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewDeliveryChannel<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cfg?tab=doc#DeliveryChannelArgs">DeliveryChannelArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cfg?tab=doc#DeliveryChannel">DeliveryChannel</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Cfg.DeliveryChannel.html">DeliveryChannel</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Cfg.DeliveryChannelArgs.html">DeliveryChannelArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>S3Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>S3Key<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshot<wbr>Delivery<wbr>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sns<wbr>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>S3Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>S3Key<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshot<wbr>Delivery<wbr>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">*Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sns<wbr>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>s3Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>s3Key<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshot<wbr>Delivery<wbr>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties?</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sns<wbr>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>s3_<wbr>bucket_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>s3_<wbr>key_<wbr>prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshot_<wbr>delivery_<wbr>properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">Dict[Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties]</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sns_<wbr>topic_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## DeliveryChannel Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>S3Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>S3Key<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Snapshot<wbr>Delivery<wbr>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties?</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sns<wbr>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>S3Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>S3Key<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Snapshot<wbr>Delivery<wbr>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">*Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sns<wbr>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>s3Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>s3Key<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>snapshot<wbr>Delivery<wbr>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties?</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sns<wbr>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>s3_<wbr>bucket_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>s3_<wbr>key_<wbr>prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>snapshot_<wbr>delivery_<wbr>properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">Dict[Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties]</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sns_<wbr>topic_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing DeliveryChannel Resource

Get an existing DeliveryChannel resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/cfg/#DeliveryChannelState">DeliveryChannelState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/cfg/#DeliveryChannel">DeliveryChannel</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>name=None<span class="p">, </span>s3_bucket_name=None<span class="p">, </span>s3_key_prefix=None<span class="p">, </span>snapshot_delivery_properties=None<span class="p">, </span>sns_topic_arn=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetDeliveryChannel<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cfg?tab=doc#DeliveryChannelState">DeliveryChannelState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cfg?tab=doc#DeliveryChannel">DeliveryChannel</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Cfg.DeliveryChannel.html">DeliveryChannel</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Cfg.DeliveryChannelState.html">DeliveryChannelState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>S3Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>S3Key<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshot<wbr>Delivery<wbr>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sns<wbr>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>S3Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>S3Key<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshot<wbr>Delivery<wbr>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">*Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sns<wbr>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>s3Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>s3Key<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshot<wbr>Delivery<wbr>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties?</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sns<wbr>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the delivery channel. Defaults to `default`. Changing it recreates the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>s3_<wbr>bucket_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the S3 bucket used to store the configuration history.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>s3_<wbr>key_<wbr>prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The prefix for the specified S3 bucket.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshot_<wbr>delivery_<wbr>properties</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#deliverychannelsnapshotdeliveryproperties">Dict[Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties]</a></span>
    </dt>
    <dd>{{% md %}}Options for how AWS Config delivers configuration snapshots. See below
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sns_<wbr>topic_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic that AWS Config delivers notifications to.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Delivery<wbr>Channel<wbr>Snapshot<wbr>Delivery<wbr>Properties</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#DeliveryChannelSnapshotDeliveryProperties">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#DeliveryChannelSnapshotDeliveryProperties">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cfg?tab=doc#DeliveryChannelSnapshotDeliveryPropertiesArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cfg?tab=doc#DeliveryChannelSnapshotDeliveryPropertiesOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Delivery<wbr>Frequency</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- The frequency with which AWS Config recurringly delivers configuration snapshots.
e.g. `One_Hour` or `Three_Hours`.
Valid values are listed [here](https://docs.aws.amazon.com/config/latest/APIReference/API_ConfigSnapshotDeliveryProperties.html#API_ConfigSnapshotDeliveryProperties_Contents).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Delivery<wbr>Frequency</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}- The frequency with which AWS Config recurringly delivers configuration snapshots.
e.g. `One_Hour` or `Three_Hours`.
Valid values are listed [here](https://docs.aws.amazon.com/config/latest/APIReference/API_ConfigSnapshotDeliveryProperties.html#API_ConfigSnapshotDeliveryProperties_Contents).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>delivery<wbr>Frequency</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- The frequency with which AWS Config recurringly delivers configuration snapshots.
e.g. `One_Hour` or `Three_Hours`.
Valid values are listed [here](https://docs.aws.amazon.com/config/latest/APIReference/API_ConfigSnapshotDeliveryProperties.html#API_ConfigSnapshotDeliveryProperties_Contents).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>delivery<wbr>Frequency</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- The frequency with which AWS Config recurringly delivers configuration snapshots.
e.g. `One_Hour` or `Three_Hours`.
Valid values are listed [here](https://docs.aws.amazon.com/config/latest/APIReference/API_ConfigSnapshotDeliveryProperties.html#API_ConfigSnapshotDeliveryProperties_Contents).
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

