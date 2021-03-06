
---
title: "Profile"
block_external_search_index: true
---



Manages a Traffic Manager Profile to which multiple endpoints can be attached.

> This content is derived from https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/traffic_manager_profile.html.markdown.



## Create a Profile Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/trafficmanager/#Profile">Profile</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/trafficmanager/#ProfileArgs">ProfileArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Profile</span><span class="p">(resource_name, opts=None, </span>dns_config=None<span class="p">, </span>monitor_config=None<span class="p">, </span>name=None<span class="p">, </span>profile_status=None<span class="p">, </span>resource_group_name=None<span class="p">, </span>tags=None<span class="p">, </span>traffic_routing_method=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewProfile<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#ProfileArgs">ProfileArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#Profile">Profile</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Trafficmanager.Profile.html">Profile</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.TrafficManager.ProfileArgs.html">ProfileArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Dns<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Profile<wbr>Dns<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Monitor<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Profile<wbr>Monitor<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile<wbr>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Traffic<wbr>Routing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Dns<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Profile<wbr>Dns<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Monitor<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Profile<wbr>Monitor<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile<wbr>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Traffic<wbr>Routing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>dns<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Profile<wbr>Dns<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>monitor<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Profile<wbr>Monitor<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile<wbr>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>traffic<wbr>Routing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>dns_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Dict[Profile<wbr>Dns<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>monitor_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Dict[Profile<wbr>Monitor<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile_<wbr>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>traffic_<wbr>routing_<wbr>method</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Profile Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Dns<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Profile<wbr>Dns<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The FQDN of the created Profile.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Monitor<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Profile<wbr>Monitor<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Profile<wbr>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Traffic<wbr>Routing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Dns<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Profile<wbr>Dns<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The FQDN of the created Profile.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Monitor<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Profile<wbr>Monitor<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Profile<wbr>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Traffic<wbr>Routing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>dns<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Profile<wbr>Dns<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The FQDN of the created Profile.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>monitor<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Profile<wbr>Monitor<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>profile<wbr>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>traffic<wbr>Routing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>dns_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Dict[Profile<wbr>Dns<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The FQDN of the created Profile.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>monitor_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Dict[Profile<wbr>Monitor<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>profile_<wbr>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>resource_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>traffic_<wbr>routing_<wbr>method</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Profile Resource

Get an existing Profile resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/trafficmanager/#ProfileState">ProfileState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/trafficmanager/#Profile">Profile</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>dns_config=None<span class="p">, </span>fqdn=None<span class="p">, </span>monitor_config=None<span class="p">, </span>name=None<span class="p">, </span>profile_status=None<span class="p">, </span>resource_group_name=None<span class="p">, </span>tags=None<span class="p">, </span>traffic_routing_method=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetProfile<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#ProfileState">ProfileState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#Profile">Profile</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Trafficmanager.Profile.html">Profile</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Trafficmanager.ProfileState.html">ProfileState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Dns<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Profile<wbr>Dns<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The FQDN of the created Profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitor<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Profile<wbr>Monitor<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile<wbr>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Traffic<wbr>Routing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">*Profile<wbr>Dns<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The FQDN of the created Profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitor<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">*Profile<wbr>Monitor<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile<wbr>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Traffic<wbr>Routing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>dns<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Profile<wbr>Dns<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The FQDN of the created Profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitor<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Profile<wbr>Monitor<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile<wbr>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>traffic<wbr>Routing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>dns_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilednsconfig">Dict[Profile<wbr>Dns<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the DNS configuration of the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The FQDN of the created Profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitor_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfig">Dict[Profile<wbr>Monitor<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}This block specifies the Endpoint monitoring configuration for the Profile, it supports the fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Traffic Manager profile. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile_<wbr>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The status of the profile, can be set to either `Enabled` or `Disabled`. Defaults to `Enabled`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which to create the Traffic Manager profile.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>traffic_<wbr>routing_<wbr>method</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the algorithm used to route traffic, possible values are:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Profile<wbr>Dns<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#ProfileDnsConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#ProfileDnsConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#ProfileDnsConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#ProfileDnsConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Relative<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The relative domain name, this is combined with the domain name used by Traffic Manager to form the FQDN which is exported as documented below. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The TTL value of the Profile used by Local DNS resolvers and clients.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Relative<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The relative domain name, this is combined with the domain name used by Traffic Manager to form the FQDN which is exported as documented below. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The TTL value of the Profile used by Local DNS resolvers and clients.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>relative<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The relative domain name, this is combined with the domain name used by Traffic Manager to form the FQDN which is exported as documented below. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The TTL value of the Profile used by Local DNS resolvers and clients.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>relative<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The relative domain name, this is combined with the domain name used by Traffic Manager to form the FQDN which is exported as documented below. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The TTL value of the Profile used by Local DNS resolvers and clients.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Profile<wbr>Monitor<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#ProfileMonitorConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#ProfileMonitorConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#ProfileMonitorConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#ProfileMonitorConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Headers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfigcustomheader">List&lt;Profile<wbr>Monitor<wbr>Config<wbr>Custom<wbr>Header<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more `custom_header` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Expected<wbr>Status<wbr>Code<wbr>Ranges</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of status code ranges in the format of `100-101`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Interval<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The interval used to check the endpoint health from a Traffic Manager probing agent. You can specify two values here: `30` (normal probing) and `10` (fast probing). The default value is `30`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path used by the monitoring checks. Required when `protocol` is set to `HTTP` or `HTTPS` - cannot be set when `protocol` is set to `TCP`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The port number used by the monitoring checks.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The protocol used by the monitoring checks, supported values are `HTTP`, `HTTPS` and `TCP`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Timeout<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The amount of time the Traffic Manager probing agent should wait before considering that check a failure when a health check probe is sent to the endpoint. If `interval_in_seconds` is set to `30`, then `timeout_in_seconds` can be between `5` and `10`. The default value is `10`. If `interval_in_seconds` is set to `10`, then valid values are between `5` and `9` and `timeout_in_seconds` is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tolerated<wbr>Number<wbr>Of<wbr>Failures</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The number of failures a Traffic Manager probing agent tolerates before marking that endpoint as unhealthy. Valid values are between `0` and `9`. The default value is `3`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Headers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfigcustomheader">[]Profile<wbr>Monitor<wbr>Config<wbr>Custom<wbr>Header</a></span>
    </dt>
    <dd>{{% md %}}One or more `custom_header` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Expected<wbr>Status<wbr>Code<wbr>Ranges</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of status code ranges in the format of `100-101`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Interval<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The interval used to check the endpoint health from a Traffic Manager probing agent. You can specify two values here: `30` (normal probing) and `10` (fast probing). The default value is `30`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The path used by the monitoring checks. Required when `protocol` is set to `HTTP` or `HTTPS` - cannot be set when `protocol` is set to `TCP`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The port number used by the monitoring checks.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The protocol used by the monitoring checks, supported values are `HTTP`, `HTTPS` and `TCP`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Timeout<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The amount of time the Traffic Manager probing agent should wait before considering that check a failure when a health check probe is sent to the endpoint. If `interval_in_seconds` is set to `30`, then `timeout_in_seconds` can be between `5` and `10`. The default value is `10`. If `interval_in_seconds` is set to `10`, then valid values are between `5` and `9` and `timeout_in_seconds` is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tolerated<wbr>Number<wbr>Of<wbr>Failures</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The number of failures a Traffic Manager probing agent tolerates before marking that endpoint as unhealthy. Valid values are between `0` and `9`. The default value is `3`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Headers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfigcustomheader">Profile<wbr>Monitor<wbr>Config<wbr>Custom<wbr>Header[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more `custom_header` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>expected<wbr>Status<wbr>Code<wbr>Ranges</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of status code ranges in the format of `100-101`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>interval<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The interval used to check the endpoint health from a Traffic Manager probing agent. You can specify two values here: `30` (normal probing) and `10` (fast probing). The default value is `30`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path used by the monitoring checks. Required when `protocol` is set to `HTTP` or `HTTPS` - cannot be set when `protocol` is set to `TCP`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The port number used by the monitoring checks.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The protocol used by the monitoring checks, supported values are `HTTP`, `HTTPS` and `TCP`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>timeout<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The amount of time the Traffic Manager probing agent should wait before considering that check a failure when a health check probe is sent to the endpoint. If `interval_in_seconds` is set to `30`, then `timeout_in_seconds` can be between `5` and `10`. The default value is `10`. If `interval_in_seconds` is set to `10`, then valid values are between `5` and `9` and `timeout_in_seconds` is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tolerated<wbr>Number<wbr>Of<wbr>Failures</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The number of failures a Traffic Manager probing agent tolerates before marking that endpoint as unhealthy. Valid values are between `0` and `9`. The default value is `3`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>custom_<wbr>headers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#profilemonitorconfigcustomheader">List[Profile<wbr>Monitor<wbr>Config<wbr>Custom<wbr>Header]</a></span>
    </dt>
    <dd>{{% md %}}One or more `custom_header` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>expected<wbr>Status<wbr>Code<wbr>Ranges</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of status code ranges in the format of `100-101`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>interval_<wbr>in_<wbr>seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The interval used to check the endpoint health from a Traffic Manager probing agent. You can specify two values here: `30` (normal probing) and `10` (fast probing). The default value is `30`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The path used by the monitoring checks. Required when `protocol` is set to `HTTP` or `HTTPS` - cannot be set when `protocol` is set to `TCP`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The port number used by the monitoring checks.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The protocol used by the monitoring checks, supported values are `HTTP`, `HTTPS` and `TCP`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>timeout<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The amount of time the Traffic Manager probing agent should wait before considering that check a failure when a health check probe is sent to the endpoint. If `interval_in_seconds` is set to `30`, then `timeout_in_seconds` can be between `5` and `10`. The default value is `10`. If `interval_in_seconds` is set to `10`, then valid values are between `5` and `9` and `timeout_in_seconds` is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tolerated<wbr>Number<wbr>Of<wbr>Failures</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of failures a Traffic Manager probing agent tolerates before marking that endpoint as unhealthy. Valid values are between `0` and `9`. The default value is `3`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Profile<wbr>Monitor<wbr>Config<wbr>Custom<wbr>Header</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#ProfileMonitorConfigCustomHeader">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#ProfileMonitorConfigCustomHeader">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#ProfileMonitorConfigCustomHeaderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/trafficmanager?tab=doc#ProfileMonitorConfigCustomHeaderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the custom header.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value of custom header. Applicable for Http and Https protocol.
{{% /md %}}</dd>

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
    <dd>{{% md %}}The name of the custom header.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value of custom header. Applicable for Http and Https protocol.
{{% /md %}}</dd>

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
    <dd>{{% md %}}The name of the custom header.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value of custom header. Applicable for Http and Https protocol.
{{% /md %}}</dd>

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
    <dd>{{% md %}}The name of the custom header.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The value of custom header. Applicable for Http and Https protocol.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure">https://github.com/pulumi/pulumi-azure</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

