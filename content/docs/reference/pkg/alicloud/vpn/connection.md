
---
title: "Connection"
block_external_search_index: true
---






## Create a Connection Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/vpn/#Connection">Connection</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/vpn/#ConnectionArgs">ConnectionArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Connection</span><span class="p">(resource_name, opts=None, </span>customer_gateway_id=None<span class="p">, </span>effect_immediately=None<span class="p">, </span>ike_configs=None<span class="p">, </span>ipsec_configs=None<span class="p">, </span>local_subnets=None<span class="p">, </span>name=None<span class="p">, </span>remote_subnets=None<span class="p">, </span>vpn_gateway_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewConnection<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpn?tab=doc#ConnectionArgs">ConnectionArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpn?tab=doc#Connection">Connection</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Vpn.Connection.html">Connection</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Vpn.ConnectionArgs.html">ConnectionArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Customer<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Effect<wbr>Immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">List&lt;Connection<wbr>Ike<wbr>Config<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">List&lt;Connection<wbr>Ipsec<wbr>Config<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Local<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Remote<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Vpn<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Customer<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Effect<wbr>Immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">[]Connection<wbr>Ike<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">[]Connection<wbr>Ipsec<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Local<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Remote<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Vpn<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>customer<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>effect<wbr>Immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">Connection<wbr>Ike<wbr>Config[]?</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">Connection<wbr>Ipsec<wbr>Config[]?</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>local<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>remote<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>vpn<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>customer_<wbr>gateway_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>effect_<wbr>immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike_<wbr>configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">List[Connection<wbr>Ike<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec_<wbr>configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">List[Connection<wbr>Ipsec<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>local_<wbr>subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>remote_<wbr>subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>vpn_<wbr>gateway_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Connection Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Customer<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Effect<wbr>Immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ike<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">List&lt;Connection<wbr>Ike<wbr>Config&gt;</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ipsec<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">List&lt;Connection<wbr>Ipsec<wbr>Config&gt;</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Local<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Remote<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The status of VPN connection.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vpn<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Customer<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Effect<wbr>Immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ike<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">[]Connection<wbr>Ike<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ipsec<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">[]Connection<wbr>Ipsec<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Local<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Remote<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The status of VPN connection.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vpn<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>customer<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>effect<wbr>Immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ike<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">Connection<wbr>Ike<wbr>Config[]</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ipsec<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">Connection<wbr>Ipsec<wbr>Config[]</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>local<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>remote<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The status of VPN connection.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vpn<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>customer_<wbr>gateway_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>effect_<wbr>immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ike_<wbr>configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">List[Connection<wbr>Ike<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ipsec_<wbr>configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">List[Connection<wbr>Ipsec<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>local_<wbr>subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>remote_<wbr>subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The status of VPN connection.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vpn_<wbr>gateway_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Connection Resource

Get an existing Connection resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/vpn/#ConnectionState">ConnectionState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/vpn/#Connection">Connection</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>customer_gateway_id=None<span class="p">, </span>effect_immediately=None<span class="p">, </span>ike_configs=None<span class="p">, </span>ipsec_configs=None<span class="p">, </span>local_subnets=None<span class="p">, </span>name=None<span class="p">, </span>remote_subnets=None<span class="p">, </span>status=None<span class="p">, </span>vpn_gateway_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetConnection<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpn?tab=doc#ConnectionState">ConnectionState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpn?tab=doc#Connection">Connection</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Vpn.Connection.html">Connection</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Vpn.ConnectionState.html">ConnectionState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Customer<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Effect<wbr>Immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">List&lt;Connection<wbr>Ike<wbr>Config<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">List&lt;Connection<wbr>Ipsec<wbr>Config<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Local<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Remote<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The status of VPN connection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpn<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Customer<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Effect<wbr>Immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">[]Connection<wbr>Ike<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">[]Connection<wbr>Ipsec<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Local<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Remote<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The status of VPN connection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpn<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>customer<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>effect<wbr>Immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">Connection<wbr>Ike<wbr>Config[]?</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">Connection<wbr>Ipsec<wbr>Config[]?</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>local<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>remote<wbr>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The status of VPN connection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpn<wbr>Gateway<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>customer_<wbr>gateway_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>effect_<wbr>immediately</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to delete a successfully negotiated IPsec tunnel and initiate a negotiation again. Valid value:true,false.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike_<wbr>configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionikeconfig">List[Connection<wbr>Ike<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-one negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec_<wbr>configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionipsecconfig">List[Connection<wbr>Ipsec<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The configurations of phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>local_<wbr>subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the VPC to be connected with the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the IPsec connection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>remote_<wbr>subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The CIDR block of the local data center. This parameter is used for phase-two negotiation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The status of VPN connection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpn_<wbr>gateway_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the VPN gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Connection<wbr>Ike<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/input/#ConnectionIkeConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#ConnectionIkeConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpn?tab=doc#ConnectionIkeConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpn?tab=doc#ConnectionIkeConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Auth<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The authentication algorithm of phase-one negotiation. Valid value: md5 | sha1 | sha256 | sha384 | sha512 |. Default value: sha1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Enc<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The encryption algorithm of phase-one negotiation. Valid value: aes | aes192 | aes256 | des | 3des. Default Valid value: aes
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The SA lifecycle as the result of phase-one negotiation. The valid value of n is [0, 86400], the unit is second and the default value is 86400.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Local<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The identification of the VPN gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The negotiation mode of IKE V1. Valid value: main (main mode) | aggressive (aggressive mode). Default value: main
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Pfs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Diffie-Hellman key exchange algorithm used by phase-one negotiation. Valid value: group1 | group2 | group5 | group14 | group24. Default value: group2
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Remote<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The identification of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The version of the IKE protocol. Valid value: ikev1 | ikev2. Default value: ikev1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Psk</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Used for authentication between the IPsec VPN gateway and the customer gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Auth<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The authentication algorithm of phase-one negotiation. Valid value: md5 | sha1 | sha256 | sha384 | sha512 |. Default value: sha1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Enc<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The encryption algorithm of phase-one negotiation. Valid value: aes | aes192 | aes256 | des | 3des. Default Valid value: aes
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The SA lifecycle as the result of phase-one negotiation. The valid value of n is [0, 86400], the unit is second and the default value is 86400.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Local<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The identification of the VPN gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The negotiation mode of IKE V1. Valid value: main (main mode) | aggressive (aggressive mode). Default value: main
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Pfs</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Diffie-Hellman key exchange algorithm used by phase-one negotiation. Valid value: group1 | group2 | group5 | group14 | group24. Default value: group2
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Remote<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The identification of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ike<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The version of the IKE protocol. Valid value: ikev1 | ikev2. Default value: ikev1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Psk</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Used for authentication between the IPsec VPN gateway and the customer gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Auth<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The authentication algorithm of phase-one negotiation. Valid value: md5 | sha1 | sha256 | sha384 | sha512 |. Default value: sha1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Enc<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The encryption algorithm of phase-one negotiation. Valid value: aes | aes192 | aes256 | des | 3des. Default Valid value: aes
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The SA lifecycle as the result of phase-one negotiation. The valid value of n is [0, 86400], the unit is second and the default value is 86400.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Local<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The identification of the VPN gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The negotiation mode of IKE V1. Valid value: main (main mode) | aggressive (aggressive mode). Default value: main
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Pfs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Diffie-Hellman key exchange algorithm used by phase-one negotiation. Valid value: group1 | group2 | group5 | group14 | group24. Default value: group2
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Remote<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The identification of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The version of the IKE protocol. Valid value: ikev1 | ikev2. Default value: ikev1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>psk</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Used for authentication between the IPsec VPN gateway and the customer gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Auth<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The authentication algorithm of phase-one negotiation. Valid value: md5 | sha1 | sha256 | sha384 | sha512 |. Default value: sha1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Enc<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The encryption algorithm of phase-one negotiation. Valid value: aes | aes192 | aes256 | des | 3des. Default Valid value: aes
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The SA lifecycle as the result of phase-one negotiation. The valid value of n is [0, 86400], the unit is second and the default value is 86400.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Local<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The identification of the VPN gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The negotiation mode of IKE V1. Valid value: main (main mode) | aggressive (aggressive mode). Default value: main
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Pfs</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Diffie-Hellman key exchange algorithm used by phase-one negotiation. Valid value: group1 | group2 | group5 | group14 | group24. Default value: group2
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Remote<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The identification of the customer gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ike<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The version of the IKE protocol. Valid value: ikev1 | ikev2. Default value: ikev1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>psk</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Used for authentication between the IPsec VPN gateway and the customer gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Connection<wbr>Ipsec<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/input/#ConnectionIpsecConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#ConnectionIpsecConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpn?tab=doc#ConnectionIpsecConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/vpn?tab=doc#ConnectionIpsecConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Auth<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The authentication algorithm of phase-two negotiation. Valid value: md5 | sha1 | sha256 | sha384 | sha512 |. Default value: sha1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Enc<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The encryption algorithm of phase-two negotiation. Valid value: aes | aes192 | aes256 | des | 3des. Default value: aes
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The SA lifecycle as the result of phase-two negotiation. The valid value is [0, 86400], the unit is second and the default value is 86400.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Pfs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Diffie-Hellman key exchange algorithm used by phase-two negotiation. Valid value: group1 | group2 | group5 | group14 | group24| disabled. Default value: group2
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Auth<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The authentication algorithm of phase-two negotiation. Valid value: md5 | sha1 | sha256 | sha384 | sha512 |. Default value: sha1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Enc<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The encryption algorithm of phase-two negotiation. Valid value: aes | aes192 | aes256 | des | 3des. Default value: aes
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The SA lifecycle as the result of phase-two negotiation. The valid value is [0, 86400], the unit is second and the default value is 86400.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipsec<wbr>Pfs</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Diffie-Hellman key exchange algorithm used by phase-two negotiation. Valid value: group1 | group2 | group5 | group14 | group24| disabled. Default value: group2
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Auth<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The authentication algorithm of phase-two negotiation. Valid value: md5 | sha1 | sha256 | sha384 | sha512 |. Default value: sha1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Enc<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The encryption algorithm of phase-two negotiation. Valid value: aes | aes192 | aes256 | des | 3des. Default value: aes
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The SA lifecycle as the result of phase-two negotiation. The valid value is [0, 86400], the unit is second and the default value is 86400.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Pfs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Diffie-Hellman key exchange algorithm used by phase-two negotiation. Valid value: group1 | group2 | group5 | group14 | group24| disabled. Default value: group2
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Auth<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The authentication algorithm of phase-two negotiation. Valid value: md5 | sha1 | sha256 | sha384 | sha512 |. Default value: sha1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Enc<wbr>Alg</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The encryption algorithm of phase-two negotiation. Valid value: aes | aes192 | aes256 | des | 3des. Default value: aes
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Lifetime</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The SA lifecycle as the result of phase-two negotiation. The valid value is [0, 86400], the unit is second and the default value is 86400.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipsec<wbr>Pfs</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Diffie-Hellman key exchange algorithm used by phase-two negotiation. Valid value: group1 | group2 | group5 | group14 | group24| disabled. Default value: group2
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

