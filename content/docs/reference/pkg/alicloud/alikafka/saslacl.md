
---
title: "SaslAcl"
block_external_search_index: true
---



Provides an ALIKAFKA sasl acl resource.

> **NOTE:** Available in 1.66.0+

> **NOTE:**  Only the following regions support create alikafka sasl user.
[`cn-hangzhou`,`cn-beijing`,`cn-shenzhen`,`cn-shanghai`,`cn-qingdao`,`cn-hongkong`,`cn-huhehaote`,`cn-zhangjiakou`,`ap-southeast-1`,`ap-south-1`,`ap-southeast-5`]

## Example Usage

Basic Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const config = new pulumi.Config();
const username = config.get("username") || "testusername";
const password = config.get("password") || "testpassword";

const defaultZones = pulumi.output(alicloud.getZones({
    availableResourceCreation: "VSwitch",
}, { async: true }));
const defaultNetwork = new alicloud.vpc.Network("default", {
    cidrBlock: "172.16.0.0/12",
});
const defaultSwitch = new alicloud.vpc.Switch("default", {
    availabilityZone: defaultZones.zones[0].id,
    cidrBlock: "172.16.0.0/24",
    vpcId: defaultNetwork.id,
});
const defaultInstance = new alicloud.alikafka.Instance("default", {
    deployType: 5,
    diskSize: 500,
    diskType: 1,
    ioMax: 20,
    topicQuota: 50,
    vswitchId: defaultSwitch.id,
});
const defaultTopic = new alicloud.alikafka.Topic("default", {
    instanceId: defaultInstance.id,
    remark: "topic-remark",
    topic: "test-topic",
});
const defaultSaslUser = new alicloud.alikafka.SaslUser("default", {
    instanceId: defaultInstance.id,
    password: password,
    username: username,
});
const defaultSaslAcl = new alicloud.alikafka.SaslAcl("default", {
    aclOperationType: "Write",
    aclResourceName: defaultTopic.topic,
    aclResourcePatternType: "LITERAL",
    aclResourceType: "Topic",
    instanceId: defaultInstance.id,
    username: defaultSaslUser.username,
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-alicloud/blob/master/website/docs/r/alikafka_sasl_acl.html.markdown.



## Create a SaslAcl Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/alikafka/#SaslAcl">SaslAcl</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/alikafka/#SaslAclArgs">SaslAclArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">SaslAcl</span><span class="p">(resource_name, opts=None, </span>acl_operation_type=None<span class="p">, </span>acl_resource_name=None<span class="p">, </span>acl_resource_pattern_type=None<span class="p">, </span>acl_resource_type=None<span class="p">, </span>instance_id=None<span class="p">, </span>username=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewSaslAcl<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/alikafka?tab=doc#SaslAclArgs">SaslAclArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/alikafka?tab=doc#SaslAcl">SaslAcl</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Alikafka.SaslAcl.html">SaslAcl</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.AliKafka.SaslAclArgs.html">SaslAclArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Acl<wbr>Operation<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Acl<wbr>Resource<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Acl<wbr>Resource<wbr>Pattern<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Acl<wbr>Resource<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Instance<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Acl<wbr>Operation<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Acl<wbr>Resource<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Acl<wbr>Resource<wbr>Pattern<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Acl<wbr>Resource<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Instance<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>acl<wbr>Operation<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>acl<wbr>Resource<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>acl<wbr>Resource<wbr>Pattern<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>acl<wbr>Resource<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>instance<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>acl_<wbr>operation_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>acl_<wbr>resource_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>acl_<wbr>resource_<wbr>pattern_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>acl_<wbr>resource_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>instance_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## SaslAcl Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Acl<wbr>Operation<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Resource<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Resource<wbr>Pattern<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Resource<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The host of the acl.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Acl<wbr>Operation<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Resource<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Resource<wbr>Pattern<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Resource<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The host of the acl.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>acl<wbr>Operation<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl<wbr>Resource<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl<wbr>Resource<wbr>Pattern<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl<wbr>Resource<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The host of the acl.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>acl_<wbr>operation_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl_<wbr>resource_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl_<wbr>resource_<wbr>pattern_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl_<wbr>resource_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The host of the acl.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing SaslAcl Resource

Get an existing SaslAcl resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/alikafka/#SaslAclState">SaslAclState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/alikafka/#SaslAcl">SaslAcl</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>acl_operation_type=None<span class="p">, </span>acl_resource_name=None<span class="p">, </span>acl_resource_pattern_type=None<span class="p">, </span>acl_resource_type=None<span class="p">, </span>host=None<span class="p">, </span>instance_id=None<span class="p">, </span>username=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetSaslAcl<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/alikafka?tab=doc#SaslAclState">SaslAclState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/alikafka?tab=doc#SaslAcl">SaslAcl</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Alikafka.SaslAcl.html">SaslAcl</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Alikafka.SaslAclState.html">SaslAclState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Acl<wbr>Operation<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Acl<wbr>Resource<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Acl<wbr>Resource<wbr>Pattern<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Acl<wbr>Resource<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host of the acl.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Acl<wbr>Operation<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Acl<wbr>Resource<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Acl<wbr>Resource<wbr>Pattern<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Acl<wbr>Resource<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The host of the acl.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>acl<wbr>Operation<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>acl<wbr>Resource<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>acl<wbr>Resource<wbr>Pattern<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>acl<wbr>Resource<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host of the acl.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>acl_<wbr>operation_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Operation type for this acl. The operation type can only be "Write" and "Read".
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>acl_<wbr>resource_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource name for this acl. The resource name should be a topic or consumer group name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>acl_<wbr>resource_<wbr>pattern_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource pattern type for this acl. The resource pattern support two types "LITERAL" and "PREFIXED". "LITERAL": A literal name defines the full name of a resource. The special wildcard character "*" can be used to represent a resource with any name. "PREFIXED": A prefixed name defines a prefix for a resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>acl_<wbr>resource_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource type for this acl. The resource type can only be "Topic" and "Group".
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The host of the acl.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the ALIKAFKA Instance that owns the groups.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Username for the sasl user. The length should between 1 to 64 characters. The user should be an existed sasl user.
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

