
---
title: "SpringCloudService"
block_external_search_index: true
---



Manages an Azure Spring Cloud Service.

> This content is derived from https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/spring_cloud_service.html.markdown.



## Create a SpringCloudService Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/appplatform/#SpringCloudService">SpringCloudService</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/appplatform/#SpringCloudServiceArgs">SpringCloudServiceArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">SpringCloudService</span><span class="p">(resource_name, opts=None, </span>config_server_git_setting=None<span class="p">, </span>location=None<span class="p">, </span>name=None<span class="p">, </span>resource_group_name=None<span class="p">, </span>tags=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewSpringCloudService<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceArgs">SpringCloudServiceArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudService">SpringCloudService</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Appplatform.SpringCloudService.html">SpringCloudService</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.AppPlatform.SpringCloudServiceArgs.html">SpringCloudServiceArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Config<wbr>Server<wbr>Git<wbr>Setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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
        <span>Config<wbr>Server<wbr>Git<wbr>Setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">*Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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
        <span>config<wbr>Server<wbr>Git<wbr>Setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting?</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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
        <span>config_<wbr>server_<wbr>git_<wbr>setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">Dict[Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting]</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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







## SpringCloudService Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Config<wbr>Server<wbr>Git<wbr>Setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting?</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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
        <span>Config<wbr>Server<wbr>Git<wbr>Setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">*Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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
        <span>config<wbr>Server<wbr>Git<wbr>Setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting?</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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
        <span>config_<wbr>server_<wbr>git_<wbr>setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">Dict[Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting]</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>resource_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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








## Look up an Existing SpringCloudService Resource

Get an existing SpringCloudService resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/appplatform/#SpringCloudServiceState">SpringCloudServiceState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/appplatform/#SpringCloudService">SpringCloudService</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>config_server_git_setting=None<span class="p">, </span>location=None<span class="p">, </span>name=None<span class="p">, </span>resource_group_name=None<span class="p">, </span>tags=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetSpringCloudService<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceState">SpringCloudServiceState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudService">SpringCloudService</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Appplatform.SpringCloudService.html">SpringCloudService</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Appplatform.SpringCloudServiceState.html">SpringCloudServiceState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Config<wbr>Server<wbr>Git<wbr>Setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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
        <span>Config<wbr>Server<wbr>Git<wbr>Setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">*Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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
        <span>config<wbr>Server<wbr>Git<wbr>Setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting?</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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
        <span>config_<wbr>server_<wbr>git_<wbr>setting</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsetting">Dict[Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting]</a></span>
    </dt>
    <dd>{{% md %}}A `config_server_git_setting` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Spring Cloud Service resource. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies The name of the resource group in which to create the Spring Cloud Service. Changing this forces a new resource to be created.
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

<h4>Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#SpringCloudServiceConfigServerGitSetting">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#SpringCloudServiceConfigServerGitSetting">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Basic<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettinghttpbasicauth">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Http<wbr>Basic<wbr>Auth<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A `http_basic_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Label</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The default label of the Git repository, should be the branch name, tag name, or commit-id of the repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Repositories</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepository">List&lt;Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more `repository` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Search<wbr>Paths</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}An array of strings used to search subdirectories of the Git repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingsshauth">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Ssh<wbr>Auth<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A `ssh_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URI of the default Git repository used as the Config Server back end, should be started with `http://`, `https://`, `git@`, or `ssh://`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Basic<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettinghttpbasicauth">*Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Http<wbr>Basic<wbr>Auth</a></span>
    </dt>
    <dd>{{% md %}}A `http_basic_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Label</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The default label of the Git repository, should be the branch name, tag name, or commit-id of the repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Repositories</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepository">[]Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository</a></span>
    </dt>
    <dd>{{% md %}}One or more `repository` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Search<wbr>Paths</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An array of strings used to search subdirectories of the Git repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingsshauth">*Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Ssh<wbr>Auth</a></span>
    </dt>
    <dd>{{% md %}}A `ssh_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URI of the default Git repository used as the Config Server back end, should be started with `http://`, `https://`, `git@`, or `ssh://`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>http<wbr>Basic<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettinghttpbasicauth">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Http<wbr>Basic<wbr>Auth?</a></span>
    </dt>
    <dd>{{% md %}}A `http_basic_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>label</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The default label of the Git repository, should be the branch name, tag name, or commit-id of the repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>repositories</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepository">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more `repository` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>search<wbr>Paths</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}An array of strings used to search subdirectories of the Git repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingsshauth">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Ssh<wbr>Auth?</a></span>
    </dt>
    <dd>{{% md %}}A `ssh_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URI of the default Git repository used as the Config Server back end, should be started with `http://`, `https://`, `git@`, or `ssh://`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>http<wbr>Basic<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettinghttpbasicauth">Dict[Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Http<wbr>Basic<wbr>Auth]</a></span>
    </dt>
    <dd>{{% md %}}A `http_basic_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>label</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The default label of the Git repository, should be the branch name, tag name, or commit-id of the repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>repositories</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepository">List[Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository]</a></span>
    </dt>
    <dd>{{% md %}}One or more `repository` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>search<wbr>Paths</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}An array of strings used to search subdirectories of the Git repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingsshauth">Dict[Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Ssh<wbr>Auth]</a></span>
    </dt>
    <dd>{{% md %}}A `ssh_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URI of the default Git repository used as the Config Server back end, should be started with `http://`, `https://`, `git@`, or `ssh://`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Http<wbr>Basic<wbr>Auth</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#SpringCloudServiceConfigServerGitSettingHttpBasicAuth">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#SpringCloudServiceConfigServerGitSettingHttpBasicAuth">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingHttpBasicAuthArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingHttpBasicAuthOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The username that's used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The username that's used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The username that's used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The username that's used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#SpringCloudServiceConfigServerGitSettingRepository">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#SpringCloudServiceConfigServerGitSettingRepository">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingRepositoryArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingRepositoryOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Basic<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepositoryhttpbasicauth">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Http<wbr>Basic<wbr>Auth<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A `http_basic_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Label</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The default label of the Git repository, should be the branch name, tag name, or commit-id of the repository.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A name to identify on the Git repository, required only if repos exists.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Patterns</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}An array of strings used to match an application name. For each pattern, use the `{application}/{profile}` format with wildcards.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Search<wbr>Paths</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}An array of strings used to search subdirectories of the Git repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepositorysshauth">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Ssh<wbr>Auth<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A `ssh_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URI of the Git repository that's used as the Config Server back end should be started with `http://`, `https://`, `git@`, or `ssh://`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Basic<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepositoryhttpbasicauth">*Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Http<wbr>Basic<wbr>Auth</a></span>
    </dt>
    <dd>{{% md %}}A `http_basic_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Label</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The default label of the Git repository, should be the branch name, tag name, or commit-id of the repository.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A name to identify on the Git repository, required only if repos exists.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Patterns</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An array of strings used to match an application name. For each pattern, use the `{application}/{profile}` format with wildcards.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Search<wbr>Paths</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An array of strings used to search subdirectories of the Git repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepositorysshauth">*Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Ssh<wbr>Auth</a></span>
    </dt>
    <dd>{{% md %}}A `ssh_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URI of the Git repository that's used as the Config Server back end should be started with `http://`, `https://`, `git@`, or `ssh://`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>http<wbr>Basic<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepositoryhttpbasicauth">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Http<wbr>Basic<wbr>Auth?</a></span>
    </dt>
    <dd>{{% md %}}A `http_basic_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>label</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The default label of the Git repository, should be the branch name, tag name, or commit-id of the repository.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A name to identify on the Git repository, required only if repos exists.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>patterns</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}An array of strings used to match an application name. For each pattern, use the `{application}/{profile}` format with wildcards.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>search<wbr>Paths</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}An array of strings used to search subdirectories of the Git repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepositorysshauth">Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Ssh<wbr>Auth?</a></span>
    </dt>
    <dd>{{% md %}}A `ssh_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URI of the Git repository that's used as the Config Server back end should be started with `http://`, `https://`, `git@`, or `ssh://`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>http<wbr>Basic<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepositoryhttpbasicauth">Dict[Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Http<wbr>Basic<wbr>Auth]</a></span>
    </dt>
    <dd>{{% md %}}A `http_basic_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>label</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The default label of the Git repository, should be the branch name, tag name, or commit-id of the repository.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A name to identify on the Git repository, required only if repos exists.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>patterns</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}An array of strings used to match an application name. For each pattern, use the `{application}/{profile}` format with wildcards.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>search<wbr>Paths</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}An array of strings used to search subdirectories of the Git repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#springcloudserviceconfigservergitsettingrepositorysshauth">Dict[Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Ssh<wbr>Auth]</a></span>
    </dt>
    <dd>{{% md %}}A `ssh_auth` block as defined below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URI of the Git repository that's used as the Config Server back end should be started with `http://`, `https://`, `git@`, or `ssh://`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Http<wbr>Basic<wbr>Auth</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#SpringCloudServiceConfigServerGitSettingRepositoryHttpBasicAuth">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#SpringCloudServiceConfigServerGitSettingRepositoryHttpBasicAuth">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingRepositoryHttpBasicAuthArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingRepositoryHttpBasicAuthOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The username that's used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The username that's used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The username that's used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The username that's used to access the Git repository server, required when the Git repository server supports Http Basic Authentication.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Repository<wbr>Ssh<wbr>Auth</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#SpringCloudServiceConfigServerGitSettingRepositorySshAuth">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#SpringCloudServiceConfigServerGitSettingRepositorySshAuth">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingRepositorySshAuthArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingRepositorySshAuthOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host key of the Git repository server, should not include the algorithm prefix as covered by `host-key-algorithm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Key<wbr>Algorithm</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host key algorithm, should be `ssh-dss`, `ssh-rsa`, `ecdsa-sha2-nistp256`, `ecdsa-sha2-nistp384`, or `ecdsa-sha2-nistp521`. Required only if `host-key` exists.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Private<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The SSH private key to access the Git repository, required when the URI starts with `git@` or `ssh://`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strict<wbr>Host<wbr>Key<wbr>Checking<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Indicates whether the Config Server instance will fail to start if the host_key does not match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The host key of the Git repository server, should not include the algorithm prefix as covered by `host-key-algorithm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Key<wbr>Algorithm</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The host key algorithm, should be `ssh-dss`, `ssh-rsa`, `ecdsa-sha2-nistp256`, `ecdsa-sha2-nistp384`, or `ecdsa-sha2-nistp521`. Required only if `host-key` exists.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Private<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The SSH private key to access the Git repository, required when the URI starts with `git@` or `ssh://`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strict<wbr>Host<wbr>Key<wbr>Checking<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Indicates whether the Config Server instance will fail to start if the host_key does not match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host key of the Git repository server, should not include the algorithm prefix as covered by `host-key-algorithm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Key<wbr>Algorithm</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host key algorithm, should be `ssh-dss`, `ssh-rsa`, `ecdsa-sha2-nistp256`, `ecdsa-sha2-nistp384`, or `ecdsa-sha2-nistp521`. Required only if `host-key` exists.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>private<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The SSH private key to access the Git repository, required when the URI starts with `git@` or `ssh://`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strict<wbr>Host<wbr>Key<wbr>Checking<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Indicates whether the Config Server instance will fail to start if the host_key does not match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The host key of the Git repository server, should not include the algorithm prefix as covered by `host-key-algorithm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Key<wbr>Algorithm</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The host key algorithm, should be `ssh-dss`, `ssh-rsa`, `ecdsa-sha2-nistp256`, `ecdsa-sha2-nistp384`, or `ecdsa-sha2-nistp521`. Required only if `host-key` exists.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>private<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The SSH private key to access the Git repository, required when the URI starts with `git@` or `ssh://`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strict<wbr>Host<wbr>Key<wbr>Checking<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates whether the Config Server instance will fail to start if the host_key does not match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Spring<wbr>Cloud<wbr>Service<wbr>Config<wbr>Server<wbr>Git<wbr>Setting<wbr>Ssh<wbr>Auth</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#SpringCloudServiceConfigServerGitSettingSshAuth">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#SpringCloudServiceConfigServerGitSettingSshAuth">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingSshAuthArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/appplatform?tab=doc#SpringCloudServiceConfigServerGitSettingSshAuthOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host key of the Git repository server, should not include the algorithm prefix as covered by `host-key-algorithm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Key<wbr>Algorithm</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host key algorithm, should be `ssh-dss`, `ssh-rsa`, `ecdsa-sha2-nistp256`, `ecdsa-sha2-nistp384`, or `ecdsa-sha2-nistp521`. Required only if `host-key` exists.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Private<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The SSH private key to access the Git repository, required when the URI starts with `git@` or `ssh://`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strict<wbr>Host<wbr>Key<wbr>Checking<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Indicates whether the Config Server instance will fail to start if the host_key does not match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The host key of the Git repository server, should not include the algorithm prefix as covered by `host-key-algorithm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Key<wbr>Algorithm</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The host key algorithm, should be `ssh-dss`, `ssh-rsa`, `ecdsa-sha2-nistp256`, `ecdsa-sha2-nistp384`, or `ecdsa-sha2-nistp521`. Required only if `host-key` exists.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Private<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The SSH private key to access the Git repository, required when the URI starts with `git@` or `ssh://`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strict<wbr>Host<wbr>Key<wbr>Checking<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Indicates whether the Config Server instance will fail to start if the host_key does not match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host key of the Git repository server, should not include the algorithm prefix as covered by `host-key-algorithm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Key<wbr>Algorithm</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The host key algorithm, should be `ssh-dss`, `ssh-rsa`, `ecdsa-sha2-nistp256`, `ecdsa-sha2-nistp384`, or `ecdsa-sha2-nistp521`. Required only if `host-key` exists.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>private<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The SSH private key to access the Git repository, required when the URI starts with `git@` or `ssh://`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strict<wbr>Host<wbr>Key<wbr>Checking<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Indicates whether the Config Server instance will fail to start if the host_key does not match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The host key of the Git repository server, should not include the algorithm prefix as covered by `host-key-algorithm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Key<wbr>Algorithm</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The host key algorithm, should be `ssh-dss`, `ssh-rsa`, `ecdsa-sha2-nistp256`, `ecdsa-sha2-nistp384`, or `ecdsa-sha2-nistp521`. Required only if `host-key` exists.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>private<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The SSH private key to access the Git repository, required when the URI starts with `git@` or `ssh://`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strict<wbr>Host<wbr>Key<wbr>Checking<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates whether the Config Server instance will fail to start if the host_key does not match.
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

