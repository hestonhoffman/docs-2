
---
title: "MemcachedLayer"
block_external_search_index: true
---



Provides an OpsWorks memcached layer resource.

{{% examples %}}
## Example Usage
{{% example %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const cache = new aws.opsworks.MemcachedLayer("cache", {
    stackId: aws_opsworks_stack_main.id,
});
```

{{% /example %}}
{{% /examples %}}



## Create a MemcachedLayer Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/opsworks/#MemcachedLayer">MemcachedLayer</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/opsworks/#MemcachedLayerArgs">MemcachedLayerArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">MemcachedLayer</span><span class="p">(resource_name, opts=None, </span>allocated_memory=None<span class="p">, </span>auto_assign_elastic_ips=None<span class="p">, </span>auto_assign_public_ips=None<span class="p">, </span>auto_healing=None<span class="p">, </span>custom_configure_recipes=None<span class="p">, </span>custom_deploy_recipes=None<span class="p">, </span>custom_instance_profile_arn=None<span class="p">, </span>custom_json=None<span class="p">, </span>custom_security_group_ids=None<span class="p">, </span>custom_setup_recipes=None<span class="p">, </span>custom_shutdown_recipes=None<span class="p">, </span>custom_undeploy_recipes=None<span class="p">, </span>drain_elb_on_shutdown=None<span class="p">, </span>ebs_volumes=None<span class="p">, </span>elastic_load_balancer=None<span class="p">, </span>install_updates_on_boot=None<span class="p">, </span>instance_shutdown_timeout=None<span class="p">, </span>name=None<span class="p">, </span>stack_id=None<span class="p">, </span>system_packages=None<span class="p">, </span>tags=None<span class="p">, </span>use_ebs_optimized_instances=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewMemcachedLayer<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/opsworks?tab=doc#MemcachedLayerArgs">MemcachedLayerArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/opsworks?tab=doc#MemcachedLayer">MemcachedLayer</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Opsworks.MemcachedLayer.html">MemcachedLayer</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.OpsWorks.MemcachedLayerArgs.html">MemcachedLayerArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Allocated<wbr>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Assign<wbr>Elastic<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Assign<wbr>Public<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Configure<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Deploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Instance<wbr>Profile<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Json</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Setup<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Shutdown<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Undeploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Elb<wbr>On<wbr>Shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ebs<wbr>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">List&lt;Memcached<wbr>Layer<wbr>Ebs<wbr>Volume<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Elastic<wbr>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Install<wbr>Updates<wbr>On<wbr>Boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Shutdown<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>System<wbr>Packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Ebs<wbr>Optimized<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Allocated<wbr>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Assign<wbr>Elastic<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Assign<wbr>Public<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Configure<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Deploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Instance<wbr>Profile<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Json</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Setup<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Shutdown<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Undeploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Elb<wbr>On<wbr>Shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ebs<wbr>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">[]Memcached<wbr>Layer<wbr>Ebs<wbr>Volume</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Elastic<wbr>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Install<wbr>Updates<wbr>On<wbr>Boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Shutdown<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>System<wbr>Packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Ebs<wbr>Optimized<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>allocated<wbr>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Assign<wbr>Elastic<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Assign<wbr>Public<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Configure<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Deploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Instance<wbr>Profile<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Json</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Setup<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Shutdown<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Undeploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>drain<wbr>Elb<wbr>On<wbr>Shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ebs<wbr>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">Memcached<wbr>Layer<wbr>Ebs<wbr>Volume[]?</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>elastic<wbr>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>install<wbr>Updates<wbr>On<wbr>Boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Shutdown<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>system<wbr>Packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Ebs<wbr>Optimized<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>allocated_<wbr>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>assign_<wbr>elastic_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>assign_<wbr>public_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>configure_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>deploy_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>instance_<wbr>profile_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>json</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>security_<wbr>group_<wbr>ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>setup_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>shutdown_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>undeploy_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>drain_<wbr>elb_<wbr>on_<wbr>shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ebs_<wbr>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">List[Memcached<wbr>Layer<wbr>Ebs<wbr>Volume]</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>elastic_<wbr>load_<wbr>balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>install_<wbr>updates_<wbr>on_<wbr>boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance_<wbr>shutdown_<wbr>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>stack_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>system_<wbr>packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use_<wbr>ebs_<wbr>optimized_<wbr>instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## MemcachedLayer Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Allocated<wbr>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name(ARN) of the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Auto<wbr>Assign<wbr>Elastic<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Auto<wbr>Assign<wbr>Public<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Auto<wbr>Healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Configure<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Deploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Instance<wbr>Profile<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Json</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Setup<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Shutdown<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Undeploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Drain<wbr>Elb<wbr>On<wbr>Shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ebs<wbr>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">List&lt;Memcached<wbr>Layer<wbr>Ebs<wbr>Volume&gt;?</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Elastic<wbr>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Install<wbr>Updates<wbr>On<wbr>Boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Shutdown<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>System<wbr>Packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Use<wbr>Ebs<wbr>Optimized<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Allocated<wbr>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name(ARN) of the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Auto<wbr>Assign<wbr>Elastic<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Auto<wbr>Assign<wbr>Public<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Auto<wbr>Healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Configure<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Deploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Instance<wbr>Profile<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Json</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Setup<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Shutdown<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Custom<wbr>Undeploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Drain<wbr>Elb<wbr>On<wbr>Shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ebs<wbr>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">[]Memcached<wbr>Layer<wbr>Ebs<wbr>Volume</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Elastic<wbr>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Install<wbr>Updates<wbr>On<wbr>Boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Shutdown<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>System<wbr>Packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Use<wbr>Ebs<wbr>Optimized<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>allocated<wbr>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name(ARN) of the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>auto<wbr>Assign<wbr>Elastic<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>auto<wbr>Assign<wbr>Public<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>auto<wbr>Healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom<wbr>Configure<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom<wbr>Deploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom<wbr>Instance<wbr>Profile<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom<wbr>Json</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom<wbr>Setup<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom<wbr>Shutdown<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom<wbr>Undeploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>drain<wbr>Elb<wbr>On<wbr>Shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ebs<wbr>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">Memcached<wbr>Layer<wbr>Ebs<wbr>Volume[]?</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>elastic<wbr>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>install<wbr>Updates<wbr>On<wbr>Boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance<wbr>Shutdown<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>system<wbr>Packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>use<wbr>Ebs<wbr>Optimized<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>allocated_<wbr>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name(ARN) of the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>auto_<wbr>assign_<wbr>elastic_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>auto_<wbr>assign_<wbr>public_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>auto_<wbr>healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom_<wbr>configure_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom_<wbr>deploy_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom_<wbr>instance_<wbr>profile_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom_<wbr>json</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom_<wbr>security_<wbr>group_<wbr>ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom_<wbr>setup_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom_<wbr>shutdown_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>custom_<wbr>undeploy_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>drain_<wbr>elb_<wbr>on_<wbr>shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ebs_<wbr>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">List[Memcached<wbr>Layer<wbr>Ebs<wbr>Volume]</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>elastic_<wbr>load_<wbr>balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>install_<wbr>updates_<wbr>on_<wbr>boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance_<wbr>shutdown_<wbr>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>stack_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>system_<wbr>packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>use_<wbr>ebs_<wbr>optimized_<wbr>instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing MemcachedLayer Resource

Get an existing MemcachedLayer resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/opsworks/#MemcachedLayerState">MemcachedLayerState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/opsworks/#MemcachedLayer">MemcachedLayer</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>allocated_memory=None<span class="p">, </span>arn=None<span class="p">, </span>auto_assign_elastic_ips=None<span class="p">, </span>auto_assign_public_ips=None<span class="p">, </span>auto_healing=None<span class="p">, </span>custom_configure_recipes=None<span class="p">, </span>custom_deploy_recipes=None<span class="p">, </span>custom_instance_profile_arn=None<span class="p">, </span>custom_json=None<span class="p">, </span>custom_security_group_ids=None<span class="p">, </span>custom_setup_recipes=None<span class="p">, </span>custom_shutdown_recipes=None<span class="p">, </span>custom_undeploy_recipes=None<span class="p">, </span>drain_elb_on_shutdown=None<span class="p">, </span>ebs_volumes=None<span class="p">, </span>elastic_load_balancer=None<span class="p">, </span>install_updates_on_boot=None<span class="p">, </span>instance_shutdown_timeout=None<span class="p">, </span>name=None<span class="p">, </span>stack_id=None<span class="p">, </span>system_packages=None<span class="p">, </span>tags=None<span class="p">, </span>use_ebs_optimized_instances=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetMemcachedLayer<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/opsworks?tab=doc#MemcachedLayerState">MemcachedLayerState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/opsworks?tab=doc#MemcachedLayer">MemcachedLayer</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Opsworks.MemcachedLayer.html">MemcachedLayer</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Opsworks.MemcachedLayerState.html">MemcachedLayerState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Allocated<wbr>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name(ARN) of the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Assign<wbr>Elastic<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Assign<wbr>Public<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Configure<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Deploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Instance<wbr>Profile<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Json</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Setup<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Shutdown<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Undeploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Elb<wbr>On<wbr>Shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ebs<wbr>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">List&lt;Memcached<wbr>Layer<wbr>Ebs<wbr>Volume<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Elastic<wbr>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Install<wbr>Updates<wbr>On<wbr>Boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Shutdown<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>System<wbr>Packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Ebs<wbr>Optimized<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Allocated<wbr>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name(ARN) of the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Assign<wbr>Elastic<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Assign<wbr>Public<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Configure<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Deploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Instance<wbr>Profile<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Json</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Setup<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Shutdown<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Undeploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Elb<wbr>On<wbr>Shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ebs<wbr>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">[]Memcached<wbr>Layer<wbr>Ebs<wbr>Volume</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Elastic<wbr>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Install<wbr>Updates<wbr>On<wbr>Boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Shutdown<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>System<wbr>Packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Ebs<wbr>Optimized<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>allocated<wbr>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name(ARN) of the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Assign<wbr>Elastic<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Assign<wbr>Public<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Configure<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Deploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Instance<wbr>Profile<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Json</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Setup<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Shutdown<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Undeploy<wbr>Recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>drain<wbr>Elb<wbr>On<wbr>Shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ebs<wbr>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">Memcached<wbr>Layer<wbr>Ebs<wbr>Volume[]?</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>elastic<wbr>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>install<wbr>Updates<wbr>On<wbr>Boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Shutdown<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>system<wbr>Packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Ebs<wbr>Optimized<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>allocated_<wbr>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Amount of memory to allocate for the cache on each instance, in megabytes. Defaults to 512MB.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name(ARN) of the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>assign_<wbr>elastic_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to automatically assign an elastic IP address to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>assign_<wbr>public_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}For stacks belonging to a VPC, whether to automatically assign a public IP address to each of the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>healing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable auto-healing for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>configure_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>deploy_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>instance_<wbr>profile_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of an IAM profile that will be used for the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>json</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Custom JSON attributes to apply to the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>security_<wbr>group_<wbr>ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Ids for a set of security groups to apply to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>setup_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>shutdown_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>undeploy_<wbr>recipes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>drain_<wbr>elb_<wbr>on_<wbr>shutdown</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable Elastic Load Balancing connection draining.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ebs_<wbr>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#memcachedlayerebsvolume">List[Memcached<wbr>Layer<wbr>Ebs<wbr>Volume]</a></span>
    </dt>
    <dd>{{% md %}}`ebs_volume` blocks, as described below, will each create an EBS volume and connect it to the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>elastic_<wbr>load_<wbr>balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of an Elastic Load Balancer to attach to this layer
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>install_<wbr>updates_<wbr>on_<wbr>boot</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to install OS and package updates on each instance when it boots.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance_<wbr>shutdown_<wbr>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The time, in seconds, that OpsWorks will wait for Chef to complete after triggering the Shutdown event.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A human-readable name for the layer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>stack_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of the stack the layer will belong to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>system_<wbr>packages</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Names of a set of system packages to install on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use_<wbr>ebs_<wbr>optimized_<wbr>instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to use EBS-optimized instances.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Memcached<wbr>Layer<wbr>Ebs<wbr>Volume</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#MemcachedLayerEbsVolume">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#MemcachedLayerEbsVolume">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/opsworks?tab=doc#MemcachedLayerEbsVolumeArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/opsworks?tab=doc#MemcachedLayerEbsVolumeOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Iops</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}For PIOPS volumes, the IOPS per disk.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Mount<wbr>Point</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The path to mount the EBS volume on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Number<wbr>Of<wbr>Disks</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of disks to use for the EBS volume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Raid<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The RAID level to use for the volume.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The size of the volume in gigabytes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of volume to create. This may be `standard` (the default), `io1` or `gp2`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Iops</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}For PIOPS volumes, the IOPS per disk.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Mount<wbr>Point</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The path to mount the EBS volume on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Number<wbr>Of<wbr>Disks</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of disks to use for the EBS volume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Raid<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The RAID level to use for the volume.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The size of the volume in gigabytes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The type of volume to create. This may be `standard` (the default), `io1` or `gp2`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>iops</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}For PIOPS volumes, the IOPS per disk.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>mount<wbr>Point</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The path to mount the EBS volume on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>number<wbr>Of<wbr>Disks</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The number of disks to use for the EBS volume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>raid<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The RAID level to use for the volume.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The size of the volume in gigabytes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of volume to create. This may be `standard` (the default), `io1` or `gp2`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>iops</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}For PIOPS volumes, the IOPS per disk.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>mount<wbr>Point</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The path to mount the EBS volume on the layer's instances.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>number<wbr>Of<wbr>Disks</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of disks to use for the EBS volume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>raid<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The RAID level to use for the volume.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The size of the volume in gigabytes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of volume to create. This may be `standard` (the default), `io1` or `gp2`.
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

