
---
title: "NetworkAclEntries"
block_external_search_index: true
---



Provides a network acl entries resource to create ingress and egress entries.

> **NOTE:** Available in 1.45.0+. Currently, the resource are only available in Hongkong(cn-hongkong), India(ap-south-1), and Indonesia(ap-southeast-1) regions.

> **NOTE:** It doesn't support concurrency and the order of the ingress and egress entries determines the priority.

> **NOTE:** Using this resource need to open a whitelist.

## Example Usage

Basic Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const config = new pulumi.Config();
const name = config.get("name") || "NetworkAclEntries";

const defaultZones = pulumi.output(alicloud.getZones({
    availableResourceCreation: "VSwitch",
}, { async: true }));
const defaultNetwork = new alicloud.vpc.Network("default", {
    cidrBlock: "172.16.0.0/12",
});
const defaultNetworkAcl = new alicloud.vpc.NetworkAcl("default", {
    vpcId: defaultNetwork.id,
});
const defaultSwitch = new alicloud.vpc.Switch("default", {
    availabilityZone: defaultZones.zones[0].id,
    cidrBlock: "172.16.0.0/21",
    vpcId: defaultNetwork.id,
});
const defaultNetworkAclAttachment = new alicloud.vpc.NetworkAclAttachment("default", {
    networkAclId: defaultNetworkAcl.id,
    resources: [{
        resourceId: defaultSwitch.id,
        resourceType: "VSwitch",
    }],
});
const defaultNetworkAclEntries = new alicloud.vpc.NetworkAclEntries("default", {
    egresses: [{
        description: name,
        destinationCidrIp: "0.0.0.0/32",
        entryType: "custom",
        name: name,
        policy: "accept",
        port: "-1/-1",
        protocol: "all",
    }],
    ingresses: [{
        description: name,
        entryType: "custom",
        name: name,
        policy: "accept",
        port: "-1/-1",
        protocol: "all",
        sourceCidrIp: "0.0.0.0/32",
    }],
    networkAclId: defaultNetworkAcl.id,
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-alicloud/blob/master/website/docs/r/network_acl_entries.html.markdown.



## Create a NetworkAclEntries Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/vpc/#NetworkAclEntries">NetworkAclEntries</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/vpc/#NetworkAclEntriesArgs">NetworkAclEntriesArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">NetworkAclEntries</span><span class="p">(resource_name, opts=None, </span>egresses=None<span class="p">, </span>ingresses=None<span class="p">, </span>network_acl_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewNetworkAclEntries<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpc?tab=doc#NetworkAclEntriesArgs">NetworkAclEntriesArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpc?tab=doc#NetworkAclEntries">NetworkAclEntries</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Vpc.NetworkAclEntries.html">NetworkAclEntries</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Vpc.NetworkAclEntriesArgs.html">NetworkAclEntriesArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">List&lt;Network<wbr>Acl<wbr>Entries<wbr>Egress<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">List&lt;Network<wbr>Acl<wbr>Entries<wbr>Ingress<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Network<wbr>Acl<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">[]Network<wbr>Acl<wbr>Entries<wbr>Egress</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">[]Network<wbr>Acl<wbr>Entries<wbr>Ingress</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Network<wbr>Acl<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">Network<wbr>Acl<wbr>Entries<wbr>Egress[]?</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">Network<wbr>Acl<wbr>Entries<wbr>Ingress[]?</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>network<wbr>Acl<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">List[Network<wbr>Acl<wbr>Entries<wbr>Egress]</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">List[Network<wbr>Acl<wbr>Entries<wbr>Ingress]</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>network_<wbr>acl_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## NetworkAclEntries Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">List&lt;Network<wbr>Acl<wbr>Entries<wbr>Egress&gt;?</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">List&lt;Network<wbr>Acl<wbr>Entries<wbr>Ingress&gt;?</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Network<wbr>Acl<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">[]Network<wbr>Acl<wbr>Entries<wbr>Egress</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">[]Network<wbr>Acl<wbr>Entries<wbr>Ingress</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Network<wbr>Acl<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">Network<wbr>Acl<wbr>Entries<wbr>Egress[]?</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">Network<wbr>Acl<wbr>Entries<wbr>Ingress[]?</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>network<wbr>Acl<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">List[Network<wbr>Acl<wbr>Entries<wbr>Egress]</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">List[Network<wbr>Acl<wbr>Entries<wbr>Ingress]</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>network_<wbr>acl_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing NetworkAclEntries Resource

Get an existing NetworkAclEntries resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/vpc/#NetworkAclEntriesState">NetworkAclEntriesState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/vpc/#NetworkAclEntries">NetworkAclEntries</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>egresses=None<span class="p">, </span>ingresses=None<span class="p">, </span>network_acl_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetNetworkAclEntries<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpc?tab=doc#NetworkAclEntriesState">NetworkAclEntriesState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpc?tab=doc#NetworkAclEntries">NetworkAclEntries</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Vpc.NetworkAclEntries.html">NetworkAclEntries</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Vpc.NetworkAclEntriesState.html">NetworkAclEntriesState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">List&lt;Network<wbr>Acl<wbr>Entries<wbr>Egress<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">List&lt;Network<wbr>Acl<wbr>Entries<wbr>Ingress<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Acl<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">[]Network<wbr>Acl<wbr>Entries<wbr>Egress</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">[]Network<wbr>Acl<wbr>Entries<wbr>Ingress</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Acl<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">Network<wbr>Acl<wbr>Entries<wbr>Egress[]?</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">Network<wbr>Acl<wbr>Entries<wbr>Ingress[]?</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network<wbr>Acl<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>egresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesegress">List[Network<wbr>Acl<wbr>Entries<wbr>Egress]</a></span>
    </dt>
    <dd>{{% md %}}List of the egress entries of the network acl. The order of the egress entries determines the priority. The details see Block Egress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ingresses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#networkaclentriesingress">List[Network<wbr>Acl<wbr>Entries<wbr>Ingress]</a></span>
    </dt>
    <dd>{{% md %}}List of the ingress entries of the network acl. The order of the ingress entries determines the priority. The details see Block Ingress.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network_<wbr>acl_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of the network acl, the field can't be changed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Network<wbr>Acl<wbr>Entries<wbr>Egress</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/input/#NetworkAclEntriesEgress">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#NetworkAclEntriesEgress">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpc?tab=doc#NetworkAclEntriesEgressArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpc?tab=doc#NetworkAclEntriesEgressOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Destination<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The destination ip of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Entry<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The entry type of the egress entry. It must be `custom` or `system`. Default value is `custom`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The policy of the egress entry. It must be `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The protocol of the egress entry.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The description of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Destination<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The destination ip of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Entry<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The entry type of the egress entry. It must be `custom` or `system`. Default value is `custom`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The policy of the egress entry. It must be `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The port of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The protocol of the egress entry.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>destination<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The destination ip of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>entry<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The entry type of the egress entry. It must be `custom` or `system`. Default value is `custom`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The policy of the egress entry. It must be `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The protocol of the egress entry.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>destination<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The destination ip of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>entry<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The entry type of the egress entry. It must be `custom` or `system`. Default value is `custom`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The policy of the egress entry. It must be `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The port of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The protocol of the egress entry.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Network<wbr>Acl<wbr>Entries<wbr>Ingress</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/input/#NetworkAclEntriesIngress">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#NetworkAclEntriesIngress">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpc?tab=doc#NetworkAclEntriesIngressArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpc?tab=doc#NetworkAclEntriesIngressOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Entry<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The entry type of the egress entry. It must be `custom` or `system`. Default value is `custom`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The policy of the egress entry. It must be `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The protocol of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Source<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The source ip of the ingress entry.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The description of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Entry<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The entry type of the egress entry. It must be `custom` or `system`. Default value is `custom`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The policy of the egress entry. It must be `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The port of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The protocol of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Source<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The source ip of the ingress entry.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>entry<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The entry type of the egress entry. It must be `custom` or `system`. Default value is `custom`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The policy of the egress entry. It must be `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The protocol of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>source<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The source ip of the ingress entry.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>entry<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The entry type of the egress entry. It must be `custom` or `system`. Default value is `custom`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The policy of the egress entry. It must be `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The port of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The protocol of the egress entry.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>source_<wbr>cidr_<wbr>ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The source ip of the ingress entry.
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

