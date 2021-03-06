
---
title: "GetSecurityGroupRules"
block_external_search_index: true
---



The `alicloud.ecs.getSecurityGroupRules` data source provides a collection of security permissions of a specific security group.
Each collection item represents a single `ingress` or `egress` permission rule.
The ID of the security group can be provided via a variable or the result from the other data source `alicloud.ecs.getSecurityGroups`.

## Example Usage

The following example shows how to obtain details about a security group rule and how to pass its data to an instance at launch time.

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const config = new pulumi.Config();
// Get the security group id from a variable
const securityGroupId = config.require("securityGroupId");

// Or get it from the alicloud.ecs.getSecurityGroups data source.
// Please note that the data source arguments must be enough to filter results to one security group.
const groupsDs = pulumi.output(alicloud.ecs.getSecurityGroups({
    nameRegex: "api",
}, { async: true }));
// Filter the security group rule by group
const ingressRulesDs = groupsDs.apply(groupsDs => alicloud.ecs.getSecurityGroupRules({
    direction: "ingress",
    groupId: groupsDs.groups[0].id,
    ipProtocol: "TCP",
    nicType: "internet",
}, { async: true }));
// Pass port_range to the backend service
const backend = new alicloud.ecs.Instance("backend", {
    userData: pulumi.interpolate`config_service.sh --portrange=${ingressRulesDs.rules[0].portRange}`,
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-alicloud/blob/master/website/docs/d/security_group_rules.html.markdown.





## Using GetSecurityGroupRules

{{< chooser language "javascript,typescript,python,go,csharp" / >}}


{{% choosable language typescript %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getSecurityGroupRules<span class="p">(</span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/ecs/#GetSecurityGroupRulesArgs">GetSecurityGroupRulesArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/ecs/#GetSecurityGroupRulesResult">GetSecurityGroupRulesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_security_group_rules(</span>direction=None<span class="p">, </span>group_id=None<span class="p">, </span>ip_protocol=None<span class="p">, </span>nic_type=None<span class="p">, </span>output_file=None<span class="p">, </span>policy=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupSecurityGroupRules<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/ecs?tab=doc#LookupSecurityGroupRulesArgs">LookupSecurityGroupRulesArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/ecs?tab=doc#LookupSecurityGroupRulesResult">LookupSecurityGroupRulesResult</a></span>, error)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetSecurityGroupRules </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Ecs.GetSecurityGroupRulesResult.html">GetSecurityGroupRulesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Ecs.GetSecurityGroupRulesArgs.html">GetSecurityGroupRulesArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span>? <span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Authorization direction. Valid values are: `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ip<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The IP protocol. Valid values are: `tcp`, `udp`, `icmp`, `gre` and `all`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Nic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Refers to the network type. Can be either `internet` or `intranet`. The default value is `internet`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Output<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`. The default value is `accept`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Authorization direction. Valid values are: `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ip<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The IP protocol. Valid values are: `tcp`, `udp`, `icmp`, `gre` and `all`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Nic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Refers to the network type. Can be either `internet` or `intranet`. The default value is `internet`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Output<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`. The default value is `accept`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Authorization direction. Valid values are: `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ip<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The IP protocol. Valid values are: `tcp`, `udp`, `icmp`, `gre` and `all`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>nic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Refers to the network type. Can be either `internet` or `intranet`. The default value is `internet`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>output<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`. The default value is `accept`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Authorization direction. Valid values are: `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>group_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ip_<wbr>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP protocol. Valid values are: `tcp`, `udp`, `icmp`, `gre` and `all`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>nic_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Refers to the network type. Can be either `internet` or `intranet`. The default value is `internet`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>output_<wbr>file</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`. The default value is `accept`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetSecurityGroupRules Result

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Authorization direction, `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Group<wbr>Desc</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ip<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The protocol. Can be `tcp`, `udp`, `icmp`, `gre` or `all`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Nic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network type, `internet` or `intranet`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Output<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsecuritygrouprulesrule">List&lt;Get<wbr>Security<wbr>Group<wbr>Rules<wbr>Rule&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of security group rules. Each element contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Authorization direction, `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Group<wbr>Desc</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ip<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The protocol. Can be `tcp`, `udp`, `icmp`, `gre` or `all`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Nic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Network type, `internet` or `intranet`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Output<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsecuritygrouprulesrule">[]Get<wbr>Security<wbr>Group<wbr>Rules<wbr>Rule</a></span>
    </dt>
    <dd>{{% md %}}A list of security group rules. Each element contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Authorization direction, `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>group<wbr>Desc</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ip<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The protocol. Can be `tcp`, `udp`, `icmp`, `gre` or `all`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>nic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network type, `internet` or `intranet`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>output<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsecuritygrouprulesrule">Get<wbr>Security<wbr>Group<wbr>Rules<wbr>Rule[]</a></span>
    </dt>
    <dd>{{% md %}}A list of security group rules. Each element contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Authorization direction, `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>group_<wbr>desc</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>group_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the security group that owns the rules.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ip_<wbr>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The protocol. Can be `tcp`, `udp`, `icmp`, `gre` or `all`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>nic_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Network type, `internet` or `intranet`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>output_<wbr>file</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsecuritygrouprulesrule">List[Get<wbr>Security<wbr>Group<wbr>Rules<wbr>Rule]</a></span>
    </dt>
    <dd>{{% md %}}A list of security group rules. Each element contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Supporting Types

<h4>Get<wbr>Security<wbr>Group<wbr>Rules<wbr>Rule</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#GetSecurityGroupRulesRule">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/ecs?tab=doc#GetSecurityGroupRulesRule">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the rule.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dest<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Target IP address segment for egress authorization.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dest<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dest<wbr>Group<wbr>Owner<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Alibaba Cloud account of the target security group.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Authorization direction. Valid values are: `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP protocol. Valid values are: `tcp`, `udp`, `icmp`, `gre` and `all`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Nic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Refers to the network type. Can be either `internet` or `intranet`. The default value is `internet`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`. The default value is `accept`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Port<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of port numbers.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Rule priority.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Source<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Source IP address segment for ingress authorization.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Source<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Source<wbr>Group<wbr>Owner<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Alibaba Cloud account of the source security group.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the rule.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dest<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Target IP address segment for egress authorization.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dest<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dest<wbr>Group<wbr>Owner<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Alibaba Cloud account of the target security group.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Authorization direction. Valid values are: `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP protocol. Valid values are: `tcp`, `udp`, `icmp`, `gre` and `all`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Nic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Refers to the network type. Can be either `internet` or `intranet`. The default value is `internet`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`. The default value is `accept`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Port<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of port numbers.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Rule priority.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Source<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Source IP address segment for ingress authorization.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Source<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Source<wbr>Group<wbr>Owner<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Alibaba Cloud account of the source security group.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the rule.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dest<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Target IP address segment for egress authorization.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dest<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dest<wbr>Group<wbr>Owner<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Alibaba Cloud account of the target security group.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Authorization direction. Valid values are: `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP protocol. Valid values are: `tcp`, `udp`, `icmp`, `gre` and `all`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>nic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Refers to the network type. Can be either `internet` or `intranet`. The default value is `internet`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`. The default value is `accept`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>port<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of port numbers.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Rule priority.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>source<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Source IP address segment for ingress authorization.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>source<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>source<wbr>Group<wbr>Owner<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Alibaba Cloud account of the source security group.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the rule.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dest<wbr>Cidr<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Target IP address segment for egress authorization.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dest<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dest<wbr>Group<wbr>Owner<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Alibaba Cloud account of the target security group.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>direction</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Authorization direction. Valid values are: `ingress` or `egress`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip_<wbr>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP protocol. Valid values are: `tcp`, `udp`, `icmp`, `gre` and `all`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>nic_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Refers to the network type. Can be either `internet` or `intranet`. The default value is `internet`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Authorization policy. Can be either `accept` or `drop`. The default value is `accept`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>port_<wbr>range</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The range of port numbers.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Rule priority.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>source_<wbr>cidr_<wbr>ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Source IP address segment for ingress authorization.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>source<wbr>Group<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>source_<wbr>group_<wbr>owner_<wbr>account</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Alibaba Cloud account of the source security group.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







