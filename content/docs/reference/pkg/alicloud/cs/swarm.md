
---
title: "Swarm"
block_external_search_index: true
---



> **DEPRECATED:** This resource manages swarm cluster, which is being deprecated and will be replaced by Kubernetes cluster.

This resource will help you to manager a Swarm Cluster.

> **NOTE:** Swarm cluster only supports VPC network and you can specify a VPC network by filed `vswitch_id`.

## Example Usage

Basic Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const myCluster = new alicloud.cs.Swarm("my_cluster", {
    cidrBlock: "172.18.0.0/24",
    diskCategory: "cloud_efficiency",
    diskSize: 20,
    imageId: var_image_id,
    instanceType: "ecs.n4.small",
    nodeNumber: 2,
    password: "Yourpassword1234",
    vswitchId: var_vswitch_id,
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-alicloud/blob/master/website/docs/r/cs_swarm.html.markdown.



## Create a Swarm Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/cs/#Swarm">Swarm</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/cs/#SwarmArgs">SwarmArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Swarm</span><span class="p">(resource_name, opts=None, </span>cidr_block=None<span class="p">, </span>disk_category=None<span class="p">, </span>disk_size=None<span class="p">, </span>image_id=None<span class="p">, </span>instance_type=None<span class="p">, </span>is_outdated=None<span class="p">, </span>name=None<span class="p">, </span>name_prefix=None<span class="p">, </span>need_slb=None<span class="p">, </span>node_number=None<span class="p">, </span>password=None<span class="p">, </span>release_eip=None<span class="p">, </span>size=None<span class="p">, </span>vswitch_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewSwarm<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/cs?tab=doc#SwarmArgs">SwarmArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/cs?tab=doc#Swarm">Swarm</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Cs.Swarm.html">Swarm</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.CS.SwarmArgs.html">SwarmArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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

    <dt class="property-required"
            title="Required">
        <span>Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Is<wbr>Outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Need<wbr>Slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Number</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Release<wbr>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-required"
            title="Required">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Is<wbr>Outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Need<wbr>Slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Number</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Release<wbr>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-required"
            title="Required">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk<wbr>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>is<wbr>Outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>need<wbr>Slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Number</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>release<wbr>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-required"
            title="Required">
        <span>vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>cidr_<wbr>block</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk_<wbr>category</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>instance_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>is_<wbr>outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name_<wbr>prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>need_<wbr>slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node_<wbr>number</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>release_<wbr>eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-required"
            title="Required">
        <span>vswitch_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Swarm Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Agent<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The nodes agent version.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Disk<wbr>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Is<wbr>Outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Need<wbr>Slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Node<wbr>Number</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#swarmnode">List&lt;Swarm<wbr>Node&gt;</a></span>
    </dt>
    <dd>{{% md %}}List of cluster nodes. It contains several attributes to `Block Nodes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Release<wbr>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Security<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of security group where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span>Slb<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of load balancer where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vpc<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of VPC where the current cluster is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Agent<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The nodes agent version.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Disk<wbr>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Is<wbr>Outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Need<wbr>Slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Node<wbr>Number</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#swarmnode">[]Swarm<wbr>Node</a></span>
    </dt>
    <dd>{{% md %}}List of cluster nodes. It contains several attributes to `Block Nodes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Release<wbr>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Security<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of security group where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span>Slb<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of load balancer where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vpc<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of VPC where the current cluster is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>agent<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The nodes agent version.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>disk<wbr>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>is<wbr>Outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>need<wbr>Slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>node<wbr>Number</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#swarmnode">Swarm<wbr>Node[]</a></span>
    </dt>
    <dd>{{% md %}}List of cluster nodes. It contains several attributes to `Block Nodes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>release<wbr>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>security<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of security group where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span>slb<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of load balancer where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vpc<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of VPC where the current cluster is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>agent_<wbr>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The nodes agent version.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cidr_<wbr>block</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>disk_<wbr>category</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>disk_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>image_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>is_<wbr>outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name_<wbr>prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>need_<wbr>slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>node_<wbr>number</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#swarmnode">List[Swarm<wbr>Node]</a></span>
    </dt>
    <dd>{{% md %}}List of cluster nodes. It contains several attributes to `Block Nodes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>release_<wbr>eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>security_<wbr>group_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of security group where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span>slb_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of load balancer where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vpc_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of VPC where the current cluster is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vswitch_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Swarm Resource

Get an existing Swarm resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/cs/#SwarmState">SwarmState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/cs/#Swarm">Swarm</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>agent_version=None<span class="p">, </span>cidr_block=None<span class="p">, </span>disk_category=None<span class="p">, </span>disk_size=None<span class="p">, </span>image_id=None<span class="p">, </span>instance_type=None<span class="p">, </span>is_outdated=None<span class="p">, </span>name=None<span class="p">, </span>name_prefix=None<span class="p">, </span>need_slb=None<span class="p">, </span>node_number=None<span class="p">, </span>nodes=None<span class="p">, </span>password=None<span class="p">, </span>release_eip=None<span class="p">, </span>security_group_id=None<span class="p">, </span>size=None<span class="p">, </span>slb_id=None<span class="p">, </span>vpc_id=None<span class="p">, </span>vswitch_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetSwarm<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/cs?tab=doc#SwarmState">SwarmState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/cs?tab=doc#Swarm">Swarm</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Cs.Swarm.html">Swarm</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Cs.SwarmState.html">SwarmState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Agent<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The nodes agent version.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Is<wbr>Outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Need<wbr>Slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Number</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#swarmnode">List&lt;Swarm<wbr>Node<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}List of cluster nodes. It contains several attributes to `Block Nodes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Release<wbr>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of security group where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>Slb<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of load balancer where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpc<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of VPC where the current cluster is located.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Agent<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The nodes agent version.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Is<wbr>Outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Need<wbr>Slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Number</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#swarmnode">[]Swarm<wbr>Node</a></span>
    </dt>
    <dd>{{% md %}}List of cluster nodes. It contains several attributes to `Block Nodes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Release<wbr>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of security group where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>Slb<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of load balancer where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpc<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of VPC where the current cluster is located.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>agent<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The nodes agent version.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk<wbr>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>is<wbr>Outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>need<wbr>Slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Number</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#swarmnode">Swarm<wbr>Node[]?</a></span>
    </dt>
    <dd>{{% md %}}List of cluster nodes. It contains several attributes to `Block Nodes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>release<wbr>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of security group where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>slb<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of load balancer where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpc<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of VPC where the current cluster is located.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vswitch<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>agent_<wbr>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The nodes agent version.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cidr_<wbr>block</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The CIDR block for the Container. It can not be same as the CIDR used by the VPC.
Valid value:
- 192.168.0.0/16
- 172.19-30.0.0/16
- 10.0.0.0/16
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk_<wbr>category</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The data disk category of ECS instance node. Its valid value are `cloud`, `cloud_ssd`, `cloud_essd`, `ephemeral_essd` and `cloud_efficiency`. Default to `cloud_efficiency`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The data disk size of ECS instance node. Its valid value is 20~32768 GB. Default to 20.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The image ID of ECS instance node used. Default to System automate allocated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>is_<wbr>outdated</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to use outdated instance type. Default to false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name_<wbr>prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>need_<wbr>slb</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node_<wbr>number</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The ECS node number of the container cluster. Its value choices are 1~50, and default to 1.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#swarmnode">List[Swarm<wbr>Node]</a></span>
    </dt>
    <dd>{{% md %}}List of cluster nodes. It contains several attributes to `Block Nodes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>release_<wbr>eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to release EIP after creating swarm cluster successfully. Default to false.
* `need_slb`- (ForceNew) Whether to create the default simple routing Server Load Balancer instance for the cluster. The default value is true.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security_<wbr>group_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of security group where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Field 'size' has been deprecated from provider version 1.9.1. New field 'node_number' replaces it.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Field &#39;size&#39; has been deprecated from provider version 1.9.1. New field &#39;node_number&#39; replaces it.{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>slb_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of load balancer where the current cluster worker node is located.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpc_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of VPC where the current cluster is located.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vswitch_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password of ECS instance node. If it is not specified, the container cluster's network mode will be `Classic`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Swarm<wbr>Node</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#SwarmNode">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/cs?tab=doc#SwarmNodeOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Elastic IP address of node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}ID of the node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Private<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The private IP address of node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The node current status. It is different with instance status.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Elastic IP address of node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}ID of the node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Private<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The private IP address of node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The node current status. It is different with instance status.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Elastic IP address of node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}ID of the node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>private<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The private IP address of node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The node current status. It is different with instance status.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>eip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Elastic IP address of node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The container cluster's name. It is the only in one Alicloud account.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>private_<wbr>ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The private IP address of node.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The node current status. It is different with instance status.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

