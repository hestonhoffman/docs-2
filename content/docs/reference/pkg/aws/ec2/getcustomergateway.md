
---
title: "GetCustomerGateway"
block_external_search_index: true
---



Get an existing AWS Customer Gateway.

{{% examples %}}
## Example Usage
{{% example %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const foo = pulumi.output(aws.ec2.getCustomerGateway({
    filters: [{
        name: "tag:Name",
        values: ["foo-prod"],
    }],
}, { async: true }));
const main = new aws.ec2.VpnGateway("main", {
    amazonSideAsn: "7224",
    vpcId: aws_vpc_main.id,
});
const transit = new aws.ec2.VpnConnection("transit", {
    customerGatewayId: foo.id!,
    staticRoutesOnly: false,
    type: foo.type,
    vpnGatewayId: main.id,
});
```

{{% /example %}}
{{% /examples %}}





## Using GetCustomerGateway

{{< chooser language "javascript,typescript,python,go,csharp" / >}}


{{% choosable language typescript %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getCustomerGateway<span class="p">(</span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ec2/#GetCustomerGatewayArgs">GetCustomerGatewayArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ec2/#GetCustomerGatewayResult">GetCustomerGatewayResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_customer_gateway(</span>filters=None<span class="p">, </span>id=None<span class="p">, </span>tags=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupCustomerGateway<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ec2?tab=doc#LookupCustomerGatewayArgs">LookupCustomerGatewayArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ec2?tab=doc#LookupCustomerGatewayResult">LookupCustomerGatewayResult</a></span>, error)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetCustomerGateway </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ec2.GetCustomerGatewayResult.html">GetCustomerGatewayResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ec2.GetCustomerGatewayArgs.html">GetCustomerGatewayArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span>? <span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getcustomergatewayfilter">List&lt;Get<wbr>Customer<wbr>Gateway<wbr>Filter<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more [name-value pairs][dcg-filters] to filter by.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Map of key-value pairs assigned to the gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getcustomergatewayfilter">[]Get<wbr>Customer<wbr>Gateway<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}One or more [name-value pairs][dcg-filters] to filter by.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Map of key-value pairs assigned to the gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getcustomergatewayfilter">Get<wbr>Customer<wbr>Gateway<wbr>Filter[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more [name-value pairs][dcg-filters] to filter by.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Map of key-value pairs assigned to the gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getcustomergatewayfilter">List[Get<wbr>Customer<wbr>Gateway<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}One or more [name-value pairs][dcg-filters] to filter by.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the gateway.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Map of key-value pairs assigned to the gateway.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetCustomerGateway Result

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Bgp<wbr>Asn</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}(Optional) The gateway's Border Gateway Protocol (BGP) Autonomous System Number (ASN).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getcustomergatewayfilter">List&lt;Get<wbr>Customer<wbr>Gateway<wbr>Filter&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ip<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Optional) The IP address of the gateway's Internet-routable external interface.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object></span>
    </dt>
    <dd>{{% md %}}Map of key-value pairs assigned to the gateway.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Optional) The type of customer gateway. The only type AWS supports at this time is "ipsec.1".
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Bgp<wbr>Asn</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}(Optional) The gateway's Border Gateway Protocol (BGP) Autonomous System Number (ASN).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getcustomergatewayfilter">[]Get<wbr>Customer<wbr>Gateway<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ip<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Optional) The IP address of the gateway's Internet-routable external interface.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Map of key-value pairs assigned to the gateway.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Optional) The type of customer gateway. The only type AWS supports at this time is "ipsec.1".
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>bgp<wbr>Asn</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}(Optional) The gateway's Border Gateway Protocol (BGP) Autonomous System Number (ASN).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getcustomergatewayfilter">Get<wbr>Customer<wbr>Gateway<wbr>Filter[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ip<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Optional) The IP address of the gateway's Internet-routable external interface.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}Map of key-value pairs assigned to the gateway.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Optional) The type of customer gateway. The only type AWS supports at this time is "ipsec.1".
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>bgp_<wbr>asn</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(Optional) The gateway's Border Gateway Protocol (BGP) Autonomous System Number (ASN).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>filters</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getcustomergatewayfilter">List[Get<wbr>Customer<wbr>Gateway<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ip_<wbr>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Optional) The IP address of the gateway's Internet-routable external interface.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Map of key-value pairs assigned to the gateway.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Optional) The type of customer gateway. The only type AWS supports at this time is "ipsec.1".
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Supporting Types

<h4>Get<wbr>Customer<wbr>Gateway<wbr>Filter</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#GetCustomerGatewayFilter">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GetCustomerGatewayFilter">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ec2?tab=doc#GetCustomerGatewayFilterArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ec2?tab=doc#GetCustomerGatewayFilter">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}







