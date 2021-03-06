
---
title: "Frontdoor"
block_external_search_index: true
---



Manages an Azure Front Door instance.

Azure Front Door Service is Microsoft's highly available and scalable web application acceleration platform and global HTTP(s) load balancer. It provides built-in DDoS protection and application layer security and caching. Front Door enables you to build applications that maximize and automate high-availability and performance for your end-users. Use Front Door with Azure services including Web/Mobile Apps, Cloud Services and Virtual Machines – or combine it with on-premises services for hybrid deployments and smooth cloud migration.

Below are some of the key scenarios that Azure Front Door Service addresses:
* Use Front Door to improve application scale and availability with instant multi-region failover
* Use Front Door to improve application performance with SSL offload and routing requests to the fastest available application backend.
* Use Front Door for application layer security and DDoS protection for your application.

> This content is derived from https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/frontdoor.html.markdown.



## Create a Frontdoor Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/frontdoor/#Frontdoor">Frontdoor</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/frontdoor/#FrontdoorArgs">FrontdoorArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Frontdoor</span><span class="p">(resource_name, opts=None, </span>backend_pool_health_probes=None<span class="p">, </span>backend_pool_load_balancings=None<span class="p">, </span>backend_pools=None<span class="p">, </span>enforce_backend_pools_certificate_name_check=None<span class="p">, </span>friendly_name=None<span class="p">, </span>frontend_endpoints=None<span class="p">, </span>load_balancer_enabled=None<span class="p">, </span>location=None<span class="p">, </span>name=None<span class="p">, </span>resource_group_name=None<span class="p">, </span>routing_rules=None<span class="p">, </span>tags=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewFrontdoor<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorArgs">FrontdoorArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#Frontdoor">Frontdoor</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Frontdoor.Frontdoor.html">Frontdoor</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.FrontDoor.FrontdoorArgs.html">FrontdoorArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Backend<wbr>Pool<wbr>Health<wbr>Probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">List&lt;Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Backend<wbr>Pool<wbr>Load<wbr>Balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">List&lt;Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Backend<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">List&lt;Frontdoor<wbr>Backend<wbr>Pool<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Enforce<wbr>Backend<wbr>Pools<wbr>Certificate<wbr>Name<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Friendly<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">List&lt;Frontdoor<wbr>Frontend<wbr>Endpoint<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancer<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Routing<wbr>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">List&lt;Frontdoor<wbr>Routing<wbr>Rule<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Backend<wbr>Pool<wbr>Health<wbr>Probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">[]Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Backend<wbr>Pool<wbr>Load<wbr>Balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">[]Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Backend<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">[]Frontdoor<wbr>Backend<wbr>Pool</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Enforce<wbr>Backend<wbr>Pools<wbr>Certificate<wbr>Name<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Friendly<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">[]Frontdoor<wbr>Frontend<wbr>Endpoint</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancer<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Routing<wbr>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">[]Frontdoor<wbr>Routing<wbr>Rule</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>backend<wbr>Pool<wbr>Health<wbr>Probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe[]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>backend<wbr>Pool<wbr>Load<wbr>Balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing[]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>backend<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">Frontdoor<wbr>Backend<wbr>Pool[]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>enforce<wbr>Backend<wbr>Pools<wbr>Certificate<wbr>Name<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>friendly<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">Frontdoor<wbr>Frontend<wbr>Endpoint[]</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load<wbr>Balancer<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>routing<wbr>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">Frontdoor<wbr>Routing<wbr>Rule[]</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>backend_<wbr>pool_<wbr>health_<wbr>probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">List[Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>backend_<wbr>pool_<wbr>load_<wbr>balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">List[Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>backend_<wbr>pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">List[Frontdoor<wbr>Backend<wbr>Pool]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>enforce_<wbr>backend_<wbr>pools_<wbr>certificate_<wbr>name_<wbr>check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>friendly_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>frontend_<wbr>endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">List[Frontdoor<wbr>Frontend<wbr>Endpoint]</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load_<wbr>balancer_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>routing_<wbr>rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">List[Frontdoor<wbr>Routing<wbr>Rule]</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Frontdoor Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Backend<wbr>Pool<wbr>Health<wbr>Probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">List&lt;Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Backend<wbr>Pool<wbr>Load<wbr>Balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">List&lt;Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Backend<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">List&lt;Frontdoor<wbr>Backend<wbr>Pool&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cname</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The host that each frontendEndpoint must CNAME to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enforce<wbr>Backend<wbr>Pools<wbr>Certificate<wbr>Name<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Friendly<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">List&lt;Frontdoor<wbr>Frontend<wbr>Endpoint&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Load<wbr>Balancer<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Routing<wbr>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">List&lt;Frontdoor<wbr>Routing<wbr>Rule&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Backend<wbr>Pool<wbr>Health<wbr>Probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">[]Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Backend<wbr>Pool<wbr>Load<wbr>Balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">[]Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Backend<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">[]Frontdoor<wbr>Backend<wbr>Pool</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cname</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The host that each frontendEndpoint must CNAME to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enforce<wbr>Backend<wbr>Pools<wbr>Certificate<wbr>Name<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Friendly<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">[]Frontdoor<wbr>Frontend<wbr>Endpoint</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Load<wbr>Balancer<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Routing<wbr>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">[]Frontdoor<wbr>Routing<wbr>Rule</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>backend<wbr>Pool<wbr>Health<wbr>Probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe[]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>backend<wbr>Pool<wbr>Load<wbr>Balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing[]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>backend<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">Frontdoor<wbr>Backend<wbr>Pool[]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cname</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The host that each frontendEndpoint must CNAME to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enforce<wbr>Backend<wbr>Pools<wbr>Certificate<wbr>Name<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>friendly<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">Frontdoor<wbr>Frontend<wbr>Endpoint[]</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>load<wbr>Balancer<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>routing<wbr>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">Frontdoor<wbr>Routing<wbr>Rule[]</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>backend_<wbr>pool_<wbr>health_<wbr>probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">List[Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>backend_<wbr>pool_<wbr>load_<wbr>balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">List[Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>backend_<wbr>pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">List[Frontdoor<wbr>Backend<wbr>Pool]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cname</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The host that each frontendEndpoint must CNAME to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enforce_<wbr>backend_<wbr>pools_<wbr>certificate_<wbr>name_<wbr>check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>friendly_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>frontend_<wbr>endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">List[Frontdoor<wbr>Frontend<wbr>Endpoint]</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>load_<wbr>balancer_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>resource_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>routing_<wbr>rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">List[Frontdoor<wbr>Routing<wbr>Rule]</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Frontdoor Resource

Get an existing Frontdoor resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/frontdoor/#FrontdoorState">FrontdoorState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/frontdoor/#Frontdoor">Frontdoor</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>backend_pool_health_probes=None<span class="p">, </span>backend_pool_load_balancings=None<span class="p">, </span>backend_pools=None<span class="p">, </span>cname=None<span class="p">, </span>enforce_backend_pools_certificate_name_check=None<span class="p">, </span>friendly_name=None<span class="p">, </span>frontend_endpoints=None<span class="p">, </span>load_balancer_enabled=None<span class="p">, </span>location=None<span class="p">, </span>name=None<span class="p">, </span>resource_group_name=None<span class="p">, </span>routing_rules=None<span class="p">, </span>tags=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetFrontdoor<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorState">FrontdoorState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#Frontdoor">Frontdoor</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Frontdoor.Frontdoor.html">Frontdoor</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Frontdoor.FrontdoorState.html">FrontdoorState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Backend<wbr>Pool<wbr>Health<wbr>Probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">List&lt;Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backend<wbr>Pool<wbr>Load<wbr>Balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">List&lt;Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backend<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">List&lt;Frontdoor<wbr>Backend<wbr>Pool<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cname</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host that each frontendEndpoint must CNAME to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enforce<wbr>Backend<wbr>Pools<wbr>Certificate<wbr>Name<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Friendly<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">List&lt;Frontdoor<wbr>Frontend<wbr>Endpoint<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancer<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Routing<wbr>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">List&lt;Frontdoor<wbr>Routing<wbr>Rule<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Backend<wbr>Pool<wbr>Health<wbr>Probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">[]Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backend<wbr>Pool<wbr>Load<wbr>Balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">[]Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backend<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">[]Frontdoor<wbr>Backend<wbr>Pool</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cname</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The host that each frontendEndpoint must CNAME to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enforce<wbr>Backend<wbr>Pools<wbr>Certificate<wbr>Name<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Friendly<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">[]Frontdoor<wbr>Frontend<wbr>Endpoint</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancer<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Routing<wbr>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">[]Frontdoor<wbr>Routing<wbr>Rule</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>backend<wbr>Pool<wbr>Health<wbr>Probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe[]?</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backend<wbr>Pool<wbr>Load<wbr>Balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing[]?</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backend<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">Frontdoor<wbr>Backend<wbr>Pool[]?</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cname</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host that each frontendEndpoint must CNAME to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enforce<wbr>Backend<wbr>Pools<wbr>Certificate<wbr>Name<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>friendly<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">Frontdoor<wbr>Frontend<wbr>Endpoint[]?</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load<wbr>Balancer<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>routing<wbr>Rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">Frontdoor<wbr>Routing<wbr>Rule[]?</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>backend_<wbr>pool_<wbr>health_<wbr>probes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolhealthprobe">List[Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_health_probe` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backend_<wbr>pool_<wbr>load_<wbr>balancings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolloadbalancing">List[Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool_load_balancing` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backend_<wbr>pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpool">List[Frontdoor<wbr>Backend<wbr>Pool]</a></span>
    </dt>
    <dd>{{% md %}}A `backend_pool` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cname</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The host that each frontendEndpoint must CNAME to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enforce_<wbr>backend_<wbr>pools_<wbr>certificate_<wbr>name_<wbr>check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enforce certificate name check on `HTTPS` requests to all backend pools, this setting will have no effect on `HTTP` requests. Permitted values are `true` or `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>friendly_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A friendly name for the Front Door service.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>frontend_<wbr>endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpoint">List[Frontdoor<wbr>Frontend<wbr>Endpoint]</a></span>
    </dt>
    <dd>{{% md %}}A `frontend_endpoint` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load_<wbr>balancer_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Should the Front Door Load Balancer be Enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Due to the service&#39;s API changing &#39;location&#39; must now always be set to &#39;Global&#39; for new resources, however if the Front Door service was created prior 2020/03/10 it may continue to exist in a specific current location{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Front Door service. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Resource Group in which the Front Door service should exist. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>routing_<wbr>rules</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingrule">List[Frontdoor<wbr>Routing<wbr>Rule]</a></span>
    </dt>
    <dd>{{% md %}}A `routing_rule` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Frontdoor<wbr>Backend<wbr>Pool</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#FrontdoorBackendPool">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#FrontdoorBackendPool">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorBackendPoolArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorBackendPoolOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Backends</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolbackend">List&lt;Frontdoor<wbr>Backend<wbr>Pool<wbr>Backend<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A `backend` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Health<wbr>Probe<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `backend_pool_health_probe` block whithin this resource to use for this `Backend Pool`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Load<wbr>Balancing<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `backend_pool_load_balancing` block within this resource to use for this `Backend Pool`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Backend Pool.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Backends</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolbackend">[]Frontdoor<wbr>Backend<wbr>Pool<wbr>Backend</a></span>
    </dt>
    <dd>{{% md %}}A `backend` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Health<wbr>Probe<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `backend_pool_health_probe` block whithin this resource to use for this `Backend Pool`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Load<wbr>Balancing<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `backend_pool_load_balancing` block within this resource to use for this `Backend Pool`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Backend Pool.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>backends</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolbackend">Frontdoor<wbr>Backend<wbr>Pool<wbr>Backend[]</a></span>
    </dt>
    <dd>{{% md %}}A `backend` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>health<wbr>Probe<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `backend_pool_health_probe` block whithin this resource to use for this `Backend Pool`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>load<wbr>Balancing<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `backend_pool_load_balancing` block within this resource to use for this `Backend Pool`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Backend Pool.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>backends</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorbackendpoolbackend">List[Frontdoor<wbr>Backend<wbr>Pool<wbr>Backend]</a></span>
    </dt>
    <dd>{{% md %}}A `backend` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>health<wbr>Probe<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `backend_pool_health_probe` block whithin this resource to use for this `Backend Pool`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>load<wbr>Balancing<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `backend_pool_load_balancing` block within this resource to use for this `Backend Pool`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Backend Pool.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Frontdoor<wbr>Backend<wbr>Pool<wbr>Backend</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#FrontdoorBackendPoolBackend">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#FrontdoorBackendPoolBackend">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorBackendPoolBackendArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorBackendPoolBackendOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Location of the backend (IP address or FQDN)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Specifies if the backend is enabled or not. Valid options are `true` or `false`. Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Host<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value to use as the host header sent to the backend.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Http<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The HTTP TCP port number. Possible values are between `1` - `65535`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Https<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The HTTPS TCP port number. Possible values are between `1` - `65535`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Priority to use for load balancing. Higher priorities will not be used for load balancing if any lower priority backend is healthy. Defaults to `1`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Weight</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Weight of this endpoint for load balancing purposes. Defaults to `50`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Location of the backend (IP address or FQDN)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Specifies if the backend is enabled or not. Valid options are `true` or `false`. Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Host<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value to use as the host header sent to the backend.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Http<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The HTTP TCP port number. Possible values are between `1` - `65535`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Https<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The HTTPS TCP port number. Possible values are between `1` - `65535`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Priority to use for load balancing. Higher priorities will not be used for load balancing if any lower priority backend is healthy. Defaults to `1`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Weight</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Weight of this endpoint for load balancing purposes. Defaults to `50`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Location of the backend (IP address or FQDN)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Specifies if the backend is enabled or not. Valid options are `true` or `false`. Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>host<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value to use as the host header sent to the backend.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>http<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The HTTP TCP port number. Possible values are between `1` - `65535`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>https<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The HTTPS TCP port number. Possible values are between `1` - `65535`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Priority to use for load balancing. Higher priorities will not be used for load balancing if any lower priority backend is healthy. Defaults to `1`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>weight</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Weight of this endpoint for load balancing purposes. Defaults to `50`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Location of the backend (IP address or FQDN)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies if the backend is enabled or not. Valid options are `true` or `false`. Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>host<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The value to use as the host header sent to the backend.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>http<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The HTTP TCP port number. Possible values are between `1` - `65535`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>https<wbr>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The HTTPS TCP port number. Possible values are between `1` - `65535`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Priority to use for load balancing. Higher priorities will not be used for load balancing if any lower priority backend is healthy. Defaults to `1`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>weight</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Weight of this endpoint for load balancing purposes. Defaults to `50`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Frontdoor<wbr>Backend<wbr>Pool<wbr>Health<wbr>Probe</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#FrontdoorBackendPoolHealthProbe">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#FrontdoorBackendPoolHealthProbe">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorBackendPoolHealthProbeArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorBackendPoolHealthProbeOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Is this health probe enabled? Dafaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Interval<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The number of seconds between each Health Probe. Defaults to `120`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Health Probe.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path to use for the Health Probe. Default is `/`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Probe<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies HTTP method the health probe uses when querying the backend pool instances. Possible values include: `Get` and `Head`. Defaults to `Get`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Protocol scheme to use for the Health Probe. Defaults to `Http`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Is this health probe enabled? Dafaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Interval<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The number of seconds between each Health Probe. Defaults to `120`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Health Probe.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The path to use for the Health Probe. Default is `/`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Probe<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies HTTP method the health probe uses when querying the backend pool instances. Possible values include: `Get` and `Head`. Defaults to `Get`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Protocol scheme to use for the Health Probe. Defaults to `Http`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Is this health probe enabled? Dafaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>interval<wbr>In<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The number of seconds between each Health Probe. Defaults to `120`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Health Probe.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path to use for the Health Probe. Default is `/`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>probe<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies HTTP method the health probe uses when querying the backend pool instances. Possible values include: `Get` and `Head`. Defaults to `Get`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Protocol scheme to use for the Health Probe. Defaults to `Http`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this health probe enabled? Dafaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>interval_<wbr>in_<wbr>seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of seconds between each Health Probe. Defaults to `120`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Health Probe.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The path to use for the Health Probe. Default is `/`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>probe<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies HTTP method the health probe uses when querying the backend pool instances. Possible values include: `Get` and `Head`. Defaults to `Get`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Protocol scheme to use for the Health Probe. Defaults to `Http`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Frontdoor<wbr>Backend<wbr>Pool<wbr>Load<wbr>Balancing</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#FrontdoorBackendPoolLoadBalancing">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#FrontdoorBackendPoolLoadBalancing">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorBackendPoolLoadBalancingArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorBackendPoolLoadBalancingOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Additional<wbr>Latency<wbr>Milliseconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The additional latency in milliseconds for probes to fall into the lowest latency bucket. Defaults to `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Load Balancer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sample<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The number of samples to consider for load balancing decisions. Defaults to `4`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Successful<wbr>Samples<wbr>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The number of samples within the sample period that must succeed. Defaults to `2`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Additional<wbr>Latency<wbr>Milliseconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The additional latency in milliseconds for probes to fall into the lowest latency bucket. Defaults to `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Load Balancer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sample<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The number of samples to consider for load balancing decisions. Defaults to `4`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Successful<wbr>Samples<wbr>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The number of samples within the sample period that must succeed. Defaults to `2`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>additional<wbr>Latency<wbr>Milliseconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The additional latency in milliseconds for probes to fall into the lowest latency bucket. Defaults to `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Load Balancer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sample<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The number of samples to consider for load balancing decisions. Defaults to `4`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>successful<wbr>Samples<wbr>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The number of samples within the sample period that must succeed. Defaults to `2`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>additional<wbr>Latency<wbr>Milliseconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The additional latency in milliseconds for probes to fall into the lowest latency bucket. Defaults to `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Load Balancer.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sample<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of samples to consider for load balancing decisions. Defaults to `4`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>successful<wbr>Samples<wbr>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of samples within the sample period that must succeed. Defaults to `2`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Frontdoor<wbr>Frontend<wbr>Endpoint</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#FrontdoorFrontendEndpoint">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#FrontdoorFrontendEndpoint">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorFrontendEndpointArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorFrontendEndpointOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Https<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpointcustomhttpsconfiguration">Frontdoor<wbr>Frontend<wbr>Endpoint<wbr>Custom<wbr>Https<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A `custom_https_configuration` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Custom<wbr>Https<wbr>Provisioning<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Should the HTTPS protocol be enabled for a custom domain associated with the Front Door?
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Host<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the host name of the `frontend_endpoint`. Must be a domain name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `frontend_endpoint`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Affinity<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to allow session affinity on this host. Valid options are `true` or `false` Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Affinity<wbr>Ttl<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The TTL to use in seconds for session affinity, if applicable. Defaults to `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Web<wbr>Application<wbr>Firewall<wbr>Policy<wbr>Link<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Defines the Web Application Firewall policy `ID` for each host.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Https<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpointcustomhttpsconfiguration">*Frontdoor<wbr>Frontend<wbr>Endpoint<wbr>Custom<wbr>Https<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}A `custom_https_configuration` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Custom<wbr>Https<wbr>Provisioning<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Should the HTTPS protocol be enabled for a custom domain associated with the Front Door?
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Host<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the host name of the `frontend_endpoint`. Must be a domain name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `frontend_endpoint`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Affinity<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to allow session affinity on this host. Valid options are `true` or `false` Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Affinity<wbr>Ttl<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The TTL to use in seconds for session affinity, if applicable. Defaults to `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Web<wbr>Application<wbr>Firewall<wbr>Policy<wbr>Link<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Defines the Web Application Firewall policy `ID` for each host.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Https<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpointcustomhttpsconfiguration">Frontdoor<wbr>Frontend<wbr>Endpoint<wbr>Custom<wbr>Https<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}A `custom_https_configuration` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>custom<wbr>Https<wbr>Provisioning<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Should the HTTPS protocol be enabled for a custom domain associated with the Front Door?
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>host<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the host name of the `frontend_endpoint`. Must be a domain name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `frontend_endpoint`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Affinity<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to allow session affinity on this host. Valid options are `true` or `false` Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Affinity<wbr>Ttl<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The TTL to use in seconds for session affinity, if applicable. Defaults to `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>web<wbr>Application<wbr>Firewall<wbr>Policy<wbr>Link<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Defines the Web Application Firewall policy `ID` for each host.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Https<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorfrontendendpointcustomhttpsconfiguration">Dict[Frontdoor<wbr>Frontend<wbr>Endpoint<wbr>Custom<wbr>Https<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}A `custom_https_configuration` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>custom<wbr>Https<wbr>Provisioning<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Should the HTTPS protocol be enabled for a custom domain associated with the Front Door?
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>host_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the host name of the `frontend_endpoint`. Must be a domain name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the `frontend_endpoint`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Affinity<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to allow session affinity on this host. Valid options are `true` or `false` Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Affinity<wbr>Ttl<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The TTL to use in seconds for session affinity, if applicable. Defaults to `0`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>web<wbr>Application<wbr>Firewall<wbr>Policy<wbr>Link<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Defines the Web Application Firewall policy `ID` for each host.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Frontdoor<wbr>Frontend<wbr>Endpoint<wbr>Custom<wbr>Https<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#FrontdoorFrontendEndpointCustomHttpsConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#FrontdoorFrontendEndpointCustomHttpsConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorFrontendEndpointCustomHttpsConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorFrontendEndpointCustomHttpsConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Secret<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the Key Vault secret representing the full certificate PFX.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Secret<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The version of the Key Vault secret representing the full certificate PFX.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Vault<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the Key Vault containing the SSL certificate.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Certificate<wbr>Source</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Certificate source to encrypted `HTTPS` traffic with. Allowed values are `FrontDoor` or `AzureKeyVault`. Defaults to `FrontDoor`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Minimum<wbr>Tls<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Minimum client TLS version supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provisioning<wbr>State</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provisioning state of the Front Door.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provisioning<wbr>Substate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provisioning substate of the Front Door
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Secret<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the Key Vault secret representing the full certificate PFX.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Secret<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The version of the Key Vault secret representing the full certificate PFX.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Vault<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the Key Vault containing the SSL certificate.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Certificate<wbr>Source</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Certificate source to encrypted `HTTPS` traffic with. Allowed values are `FrontDoor` or `AzureKeyVault`. Defaults to `FrontDoor`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Minimum<wbr>Tls<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Minimum client TLS version supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provisioning<wbr>State</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Provisioning state of the Front Door.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provisioning<wbr>Substate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Provisioning substate of the Front Door
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Secret<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the Key Vault secret representing the full certificate PFX.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Secret<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The version of the Key Vault secret representing the full certificate PFX.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Vault<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the Key Vault containing the SSL certificate.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>certificate<wbr>Source</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Certificate source to encrypted `HTTPS` traffic with. Allowed values are `FrontDoor` or `AzureKeyVault`. Defaults to `FrontDoor`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>minimum<wbr>Tls<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Minimum client TLS version supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provisioning<wbr>State</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provisioning state of the Front Door.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provisioning<wbr>Substate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provisioning substate of the Front Door
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Secret<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Key Vault secret representing the full certificate PFX.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Secret<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The version of the Key Vault secret representing the full certificate PFX.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>azure<wbr>Key<wbr>Vault<wbr>Certificate<wbr>Vault<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the Key Vault containing the SSL certificate.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>certificate<wbr>Source</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Certificate source to encrypted `HTTPS` traffic with. Allowed values are `FrontDoor` or `AzureKeyVault`. Defaults to `FrontDoor`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>minimum_<wbr>tls_<wbr>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Minimum client TLS version supported.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provisioning<wbr>State</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Provisioning state of the Front Door.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provisioning<wbr>Substate</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Provisioning substate of the Front Door
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Frontdoor<wbr>Routing<wbr>Rule</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#FrontdoorRoutingRule">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#FrontdoorRoutingRule">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorRoutingRuleArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorRoutingRuleOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Accepted<wbr>Protocols</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}Protocol schemes to match for the Backend Routing Rule. Defaults to `Http`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}`Enable` or `Disable` use of this Backend Routing Rule. Permitted values are `true` or `false`. Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Forwarding<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingruleforwardingconfiguration">Frontdoor<wbr>Routing<wbr>Rule<wbr>Forwarding<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A `forwarding_configuration` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The names of the `frontend_endpoint` blocks whithin this resource to associate with this `routing_rule`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Routing Rule.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Patterns<wbr>To<wbr>Matches</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The route patterns for the Backend Routing Rule. Defaults to `/*`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Redirect<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingruleredirectconfiguration">Frontdoor<wbr>Routing<wbr>Rule<wbr>Redirect<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A `redirect_configuration` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Accepted<wbr>Protocols</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Protocol schemes to match for the Backend Routing Rule. Defaults to `Http`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}`Enable` or `Disable` use of this Backend Routing Rule. Permitted values are `true` or `false`. Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Forwarding<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingruleforwardingconfiguration">*Frontdoor<wbr>Routing<wbr>Rule<wbr>Forwarding<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}A `forwarding_configuration` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The names of the `frontend_endpoint` blocks whithin this resource to associate with this `routing_rule`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Routing Rule.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Patterns<wbr>To<wbr>Matches</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The route patterns for the Backend Routing Rule. Defaults to `/*`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Redirect<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingruleredirectconfiguration">*Frontdoor<wbr>Routing<wbr>Rule<wbr>Redirect<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}A `redirect_configuration` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>accepted<wbr>Protocols</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Protocol schemes to match for the Backend Routing Rule. Defaults to `Http`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}`Enable` or `Disable` use of this Backend Routing Rule. Permitted values are `true` or `false`. Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>forwarding<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingruleforwardingconfiguration">Frontdoor<wbr>Routing<wbr>Rule<wbr>Forwarding<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}A `forwarding_configuration` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>frontend<wbr>Endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The names of the `frontend_endpoint` blocks whithin this resource to associate with this `routing_rule`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Routing Rule.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>patterns<wbr>To<wbr>Matches</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The route patterns for the Backend Routing Rule. Defaults to `/*`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>redirect<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingruleredirectconfiguration">Frontdoor<wbr>Routing<wbr>Rule<wbr>Redirect<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}A `redirect_configuration` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>accepted<wbr>Protocols</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Protocol schemes to match for the Backend Routing Rule. Defaults to `Http`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}`Enable` or `Disable` use of this Backend Routing Rule. Permitted values are `true` or `false`. Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>forwarding<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingruleforwardingconfiguration">Dict[Frontdoor<wbr>Routing<wbr>Rule<wbr>Forwarding<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}A `forwarding_configuration` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>frontend_<wbr>endpoints</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The names of the `frontend_endpoint` blocks whithin this resource to associate with this `routing_rule`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the FrontDoor.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Routing Rule.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>patterns<wbr>To<wbr>Matches</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The route patterns for the Backend Routing Rule. Defaults to `/*`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>redirect<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#frontdoorroutingruleredirectconfiguration">Dict[Frontdoor<wbr>Routing<wbr>Rule<wbr>Redirect<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}A `redirect_configuration` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Frontdoor<wbr>Routing<wbr>Rule<wbr>Forwarding<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#FrontdoorRoutingRuleForwardingConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#FrontdoorRoutingRuleForwardingConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorRoutingRuleForwardingConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorRoutingRuleForwardingConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Backend<wbr>Pool<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Backend Pool to forward the incoming traffic to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cache<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Specifies whether to Enable caching or not. Valid options are `true` or `false`. Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cache<wbr>Query<wbr>Parameter<wbr>Strip<wbr>Directive</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Defines cache behavior in releation to query string parameters. Valid options are `StripAll` or `StripNone`. Defaults to `StripAll`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cache<wbr>Use<wbr>Dynamic<wbr>Compression</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to use dynamic compression when caching. Valid options are `true` or `false`. Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Forwarding<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Path to use when constructing the request to forward to the backend. This functions as a URL Rewrite. Default behavior preserves the URL path.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Forwarding<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Protocol to use when redirecting. Valid options are `HttpOnly`, `HttpsOnly`, or `MatchRequest`. Defaults to `HttpsOnly`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Backend<wbr>Pool<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Backend Pool to forward the incoming traffic to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cache<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether to Enable caching or not. Valid options are `true` or `false`. Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cache<wbr>Query<wbr>Parameter<wbr>Strip<wbr>Directive</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Defines cache behavior in releation to query string parameters. Valid options are `StripAll` or `StripNone`. Defaults to `StripAll`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cache<wbr>Use<wbr>Dynamic<wbr>Compression</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to use dynamic compression when caching. Valid options are `true` or `false`. Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Forwarding<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Path to use when constructing the request to forward to the backend. This functions as a URL Rewrite. Default behavior preserves the URL path.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Forwarding<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Protocol to use when redirecting. Valid options are `HttpOnly`, `HttpsOnly`, or `MatchRequest`. Defaults to `HttpsOnly`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>backend<wbr>Pool<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Backend Pool to forward the incoming traffic to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cache<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Specifies whether to Enable caching or not. Valid options are `true` or `false`. Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cache<wbr>Query<wbr>Parameter<wbr>Strip<wbr>Directive</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Defines cache behavior in releation to query string parameters. Valid options are `StripAll` or `StripNone`. Defaults to `StripAll`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cache<wbr>Use<wbr>Dynamic<wbr>Compression</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to use dynamic compression when caching. Valid options are `true` or `false`. Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Forwarding<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Path to use when constructing the request to forward to the backend. This functions as a URL Rewrite. Default behavior preserves the URL path.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>forwarding<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Protocol to use when redirecting. Valid options are `HttpOnly`, `HttpsOnly`, or `MatchRequest`. Defaults to `HttpsOnly`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>backend<wbr>Pool<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Backend Pool to forward the incoming traffic to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cache<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether to Enable caching or not. Valid options are `true` or `false`. Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cache<wbr>Query<wbr>Parameter<wbr>Strip<wbr>Directive</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Defines cache behavior in releation to query string parameters. Valid options are `StripAll` or `StripNone`. Defaults to `StripAll`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cache<wbr>Use<wbr>Dynamic<wbr>Compression</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to use dynamic compression when caching. Valid options are `true` or `false`. Defaults to `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Forwarding<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Path to use when constructing the request to forward to the backend. This functions as a URL Rewrite. Default behavior preserves the URL path.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>forwarding<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Protocol to use when redirecting. Valid options are `HttpOnly`, `HttpsOnly`, or `MatchRequest`. Defaults to `HttpsOnly`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Frontdoor<wbr>Routing<wbr>Rule<wbr>Redirect<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#FrontdoorRoutingRuleRedirectConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#FrontdoorRoutingRuleRedirectConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorRoutingRuleRedirectConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/frontdoor?tab=doc#FrontdoorRoutingRuleRedirectConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Fragment</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The destination fragment in the portion of URL after '#'. Set this to add a fragment to the redirect URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Set this to change the URL for the redirection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path to retain as per the incoming request, or update in the URL for the redirection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Query<wbr>String</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Replace any existing query string from the incoming request URL.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Redirect<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Protocol to use when redirecting. Valid options are `HttpOnly`, `HttpsOnly`, or `MatchRequest`. Defaults to `MatchRequest`
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Redirect<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status code for the redirect. Valida options are `Moved`, `Found`, `TemporaryRedirect`, `PermanentRedirect`. Defaults to `Found`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Fragment</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The destination fragment in the portion of URL after '#'. Set this to add a fragment to the redirect URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Set this to change the URL for the redirection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The path to retain as per the incoming request, or update in the URL for the redirection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Query<wbr>String</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Replace any existing query string from the incoming request URL.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Redirect<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Protocol to use when redirecting. Valid options are `HttpOnly`, `HttpsOnly`, or `MatchRequest`. Defaults to `MatchRequest`
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Redirect<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status code for the redirect. Valida options are `Moved`, `Found`, `TemporaryRedirect`, `PermanentRedirect`. Defaults to `Found`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Fragment</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The destination fragment in the portion of URL after '#'. Set this to add a fragment to the redirect URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Set this to change the URL for the redirection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path to retain as per the incoming request, or update in the URL for the redirection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Query<wbr>String</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Replace any existing query string from the incoming request URL.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>redirect<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Protocol to use when redirecting. Valid options are `HttpOnly`, `HttpsOnly`, or `MatchRequest`. Defaults to `MatchRequest`
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>redirect<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status code for the redirect. Valida options are `Moved`, `Found`, `TemporaryRedirect`, `PermanentRedirect`. Defaults to `Found`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Fragment</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The destination fragment in the portion of URL after '#'. Set this to add a fragment to the redirect URL.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Set this to change the URL for the redirection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The path to retain as per the incoming request, or update in the URL for the redirection.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Query<wbr>String</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Replace any existing query string from the incoming request URL.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>redirect<wbr>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Protocol to use when redirecting. Valid options are `HttpOnly`, `HttpsOnly`, or `MatchRequest`. Defaults to `MatchRequest`
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>redirect<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Status code for the redirect. Valida options are `Moved`, `Found`, `TemporaryRedirect`, `PermanentRedirect`. Defaults to `Found`
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

