
---
title: "Route"
block_external_search_index: true
---



Represents a Route resource.

A route is a rule that specifies how certain packets should be handled by
the virtual network. Routes are associated with virtual machines by tag,
and the set of routes for a particular virtual machine is called its
routing table. For each packet leaving a virtual machine, the system
searches that virtual machine's routing table for a single best matching
route.

Routes match packets by destination IP address, preferring smaller or more
specific ranges over larger ones. If there is a tie, the system selects
the route with the smallest priority value. If there is still a tie, it
uses the layer three and four packet headers to select just one of the
remaining matching routes. The packet is then forwarded as specified by
the next_hop field of the winning route -- either to another virtual
machine destination, a virtual machine gateway or a Compute
Engine-operated gateway. Packets that do not match any route in the
sending virtual machine's routing table will be dropped.

A Route resource must have exactly one specification of either
nextHopGateway, nextHopInstance, nextHopIp, nextHopVpnTunnel, or
nextHopIlb.


To get more information about Route, see:

* [API documentation](https://cloud.google.com/compute/docs/reference/rest/v1/routes)
* How-to Guides
    * [Using Routes](https://cloud.google.com/vpc/docs/using-routes)

> This content is derived from https://github.com/terraform-providers/terraform-provider-google/blob/master/website/docs/r/compute_route.html.markdown.



## Create a Route Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gcp/compute/#Route">Route</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gcp/compute/#RouteArgs">RouteArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Route</span><span class="p">(resource_name, opts=None, </span>description=None<span class="p">, </span>dest_range=None<span class="p">, </span>name=None<span class="p">, </span>network=None<span class="p">, </span>next_hop_gateway=None<span class="p">, </span>next_hop_ilb=None<span class="p">, </span>next_hop_instance=None<span class="p">, </span>next_hop_instance_zone=None<span class="p">, </span>next_hop_ip=None<span class="p">, </span>next_hop_vpn_tunnel=None<span class="p">, </span>priority=None<span class="p">, </span>project=None<span class="p">, </span>tags=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewRoute<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#RouteArgs">RouteArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#Route">Route</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Compute.Route.html">Route</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Compute.RouteArgs.html">RouteArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dest<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Instance<wbr>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Vpn<wbr>Tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
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
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dest<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Instance<wbr>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Vpn<wbr>Tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
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
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dest<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Instance<wbr>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Vpn<wbr>Tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
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
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dest_<wbr>range</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>instance_<wbr>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>vpn_<wbr>tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Route Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dest<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Instance<wbr>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL to a Network that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Vpn<wbr>Tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URI of the created resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dest<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Instance<wbr>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL to a Network that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Next<wbr>Hop<wbr>Vpn<wbr>Tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URI of the created resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dest<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next<wbr>Hop<wbr>Gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next<wbr>Hop<wbr>Ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next<wbr>Hop<wbr>Instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next<wbr>Hop<wbr>Instance<wbr>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next<wbr>Hop<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next<wbr>Hop<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL to a Network that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next<wbr>Hop<wbr>Vpn<wbr>Tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URI of the created resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dest_<wbr>range</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next_<wbr>hop_<wbr>gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next_<wbr>hop_<wbr>ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next_<wbr>hop_<wbr>instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next_<wbr>hop_<wbr>instance_<wbr>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next_<wbr>hop_<wbr>ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next_<wbr>hop_<wbr>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to a Network that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>next_<wbr>hop_<wbr>vpn_<wbr>tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>self_<wbr>link</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URI of the created resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Route Resource

Get an existing Route resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gcp/compute/#RouteState">RouteState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gcp/compute/#Route">Route</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>description=None<span class="p">, </span>dest_range=None<span class="p">, </span>name=None<span class="p">, </span>network=None<span class="p">, </span>next_hop_gateway=None<span class="p">, </span>next_hop_ilb=None<span class="p">, </span>next_hop_instance=None<span class="p">, </span>next_hop_instance_zone=None<span class="p">, </span>next_hop_ip=None<span class="p">, </span>next_hop_network=None<span class="p">, </span>next_hop_vpn_tunnel=None<span class="p">, </span>priority=None<span class="p">, </span>project=None<span class="p">, </span>self_link=None<span class="p">, </span>tags=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetRoute<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#RouteState">RouteState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#Route">Route</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Compute.Route.html">Route</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Compute.RouteState.html">RouteState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dest<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Instance<wbr>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a Network that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Vpn<wbr>Tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URI of the created resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
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
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dest<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Instance<wbr>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to a Network that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Next<wbr>Hop<wbr>Vpn<wbr>Tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The URI of the created resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
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
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dest<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Instance<wbr>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a Network that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next<wbr>Hop<wbr>Vpn<wbr>Tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URI of the created resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
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
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dest_<wbr>range</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The destination range of outgoing packets that this route applies to. Only IPv4 is supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and
comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression
'[a-z]([-a-z0-9]*[a-z0-9])?' which means the first character must be a lowercase letter, and all following characters
must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The network that this route applies to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>gateway</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to a gateway that should handle matching packets. Currently, you can only specify the internet gateway, using a full
or partial valid URL: *
'https://www.googleapis.com/compute/v1/projects/project/global/gateways/default-internet-gateway' *
'projects/project/global/gateways/default-internet-gateway' * 'global/gateways/default-internet-gateway' * The string
'default-internet-gateway'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>ilb</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URL to a forwarding rule of type loadBalancingScheme=INTERNAL that should handle matching packets. You can only
specify the forwarding rule as a partial or full URL. For example, the following are all valid URLs:
https://www.googleapis.com/compute/v1/projects/project/regions/region/forwardingRules/forwardingRule
regions/region/forwardingRules/forwardingRule Note that this can only be used when the destinationRange is a public
(non-RFC 1918) IP CIDR range.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>instance</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to an instance that should handle matching packets. You can specify this as a full or partial URL. For example: *
'https://www.googleapis.com/compute/v1/projects/project/zones/zone/instances/instance' *
'projects/project/zones/zone/instances/instance' * 'zones/zone/instances/instance' * Just the instance name, with the
zone in 'next_hop_instance_zone'.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>instance_<wbr>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Optional when `next_hop_instance` is
specified)  The zone of the instance specified in
`next_hop_instance`.  Omit if `next_hop_instance` is specified as
a URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Network IP address of an instance that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to a Network that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>next_<wbr>hop_<wbr>vpn_<wbr>tunnel</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL to a VpnTunnel that should handle matching packets.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The priority of this route. Priority is used to break ties in cases where there is more than one matching route of equal
prefix length. In the case of two routes with equal prefix length, the one with the lowest-numbered priority value wins.
Default value is 1000. Valid range is 0 through 65535.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs.
If it is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>self_<wbr>link</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URI of the created resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of instance tags to which this route applies.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}











<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-gcp">https://github.com/pulumi/pulumi-gcp</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

