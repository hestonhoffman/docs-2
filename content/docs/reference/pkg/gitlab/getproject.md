
---
title: "GetProject"
block_external_search_index: true
---



Provides details about a specific project in the gitlab provider. The results include the name of the project, path, description, default branch, etc.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as gitlab from "@pulumi/gitlab";

const example = pulumi.output(gitlab.getProject({
    id: 30,
}, { async: true }));
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-gitlab/blob/master/website/docs/d/project.html.markdown.





## Using GetProject

{{< chooser language "javascript,typescript,python,go,csharp" / >}}


{{% choosable language typescript %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getProject<span class="p">(</span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gitlab/#GetProjectArgs">GetProjectArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gitlab/#GetProjectResult">GetProjectResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_project(</span>archived=None<span class="p">, </span>default_branch=None<span class="p">, </span>description=None<span class="p">, </span>http_url_to_repo=None<span class="p">, </span>id=None<span class="p">, </span>issues_enabled=None<span class="p">, </span>lfs_enabled=None<span class="p">, </span>merge_requests_enabled=None<span class="p">, </span>name=None<span class="p">, </span>namespace_id=None<span class="p">, </span>path=None<span class="p">, </span>pipelines_enabled=None<span class="p">, </span>request_access_enabled=None<span class="p">, </span>runners_token=None<span class="p">, </span>snippets_enabled=None<span class="p">, </span>ssh_url_to_repo=None<span class="p">, </span>visibility_level=None<span class="p">, </span>web_url=None<span class="p">, </span>wiki_enabled=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupProject<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gitlab/sdk/go/gitlab/?tab=doc#GetProjectArgs">GetProjectArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gitlab/sdk/go/gitlab/?tab=doc#LookupProjectResult">LookupProjectResult</a></span>, error)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetProject </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gitlab/Pulumi.Gitlab.GetProjectResult.html">GetProjectResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gitlab/Pulumi.Gitlab.GetProjectArgs.html">GetProjectArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span>? <span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Archived</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether the project is in read-only mode (archived).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Branch</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The default branch for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description of the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via HTTP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The integer that uniquely identifies the project within the gitlab install.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Issues<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable issue tracking for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lfs<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable LFS for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Merge<wbr>Requests<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable merge requests for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Namespace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The namespace (group or user) of the project. Defaults to your user.
See `gitlab..Group` for an example.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path of the repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pipelines<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable pipelines for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Request<wbr>Access<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Allow users to request member access.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Runners<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registration token to use during runner setup.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snippets<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable snippets for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via SSH.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Visibility<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Repositories are created as private by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Web<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL that can be used to find the project in a browser.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wiki<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable wiki for the project.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Archived</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether the project is in read-only mode (archived).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Branch</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The default branch for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A description of the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via HTTP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The integer that uniquely identifies the project within the gitlab install.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Issues<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable issue tracking for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lfs<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable LFS for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Merge<wbr>Requests<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable merge requests for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Namespace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The namespace (group or user) of the project. Defaults to your user.
See `gitlab..Group` for an example.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The path of the repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pipelines<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable pipelines for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Request<wbr>Access<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Allow users to request member access.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Runners<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Registration token to use during runner setup.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snippets<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable snippets for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via SSH.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Visibility<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Repositories are created as private by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Web<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}URL that can be used to find the project in a browser.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wiki<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable wiki for the project.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>archived</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether the project is in read-only mode (archived).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Branch</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The default branch for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description of the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>http<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via HTTP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The integer that uniquely identifies the project within the gitlab install.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>issues<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable issue tracking for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lfs<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable LFS for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>merge<wbr>Requests<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable merge requests for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>namespace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The namespace (group or user) of the project. Defaults to your user.
See `gitlab..Group` for an example.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path of the repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pipelines<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable pipelines for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>request<wbr>Access<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Allow users to request member access.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>runners<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registration token to use during runner setup.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snippets<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable snippets for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via SSH.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>visibility<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Repositories are created as private by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>web<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}URL that can be used to find the project in a browser.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wiki<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable wiki for the project.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>archived</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the project is in read-only mode (archived).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default_<wbr>branch</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The default branch for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description of the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>http_<wbr>url_<wbr>to_<wbr>repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via HTTP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The integer that uniquely identifies the project within the gitlab install.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>issues_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable issue tracking for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lfs_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable LFS for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>merge_<wbr>requests_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable merge requests for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>namespace_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The namespace (group or user) of the project. Defaults to your user.
See `gitlab..Group` for an example.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The path of the repository.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pipelines_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable pipelines for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>request_<wbr>access_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allow users to request member access.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>runners_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registration token to use during runner setup.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snippets_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable snippets for the project.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh_<wbr>url_<wbr>to_<wbr>repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via SSH.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>visibility_<wbr>level</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Repositories are created as private by default.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>web_<wbr>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL that can be used to find the project in a browser.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wiki_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable wiki for the project.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetProject Result

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Archived</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the project is in read-only mode (archived).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Default<wbr>Branch</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default branch for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description of the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Http<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via HTTP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Integer that uniquely identifies the project within the gitlab install.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Issues<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable issue tracking for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Lfs<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable LFS for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Merge<wbr>Requests<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable merge requests for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Namespace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The namespace (group or user) of the project. Defaults to your user.
See `gitlab..Group` for an example.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The path of the repository.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Pipelines<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable pipelines for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Request<wbr>Access<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allow users to request member access.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Runners<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registration token to use during runner setup.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Snippets<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable snippets for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ssh<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via SSH.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Visibility<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Repositories are created as private by default.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Web<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL that can be used to find the project in a browser.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Wiki<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable wiki for the project.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Archived</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the project is in read-only mode (archived).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Default<wbr>Branch</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default branch for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description of the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Http<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via HTTP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Integer that uniquely identifies the project within the gitlab install.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Issues<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable issue tracking for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Lfs<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable LFS for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Merge<wbr>Requests<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable merge requests for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Namespace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The namespace (group or user) of the project. Defaults to your user.
See `gitlab..Group` for an example.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The path of the repository.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Pipelines<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable pipelines for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Request<wbr>Access<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allow users to request member access.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Runners<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registration token to use during runner setup.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Snippets<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable snippets for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ssh<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via SSH.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Visibility<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Repositories are created as private by default.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Web<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL that can be used to find the project in a browser.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Wiki<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable wiki for the project.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>archived</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether the project is in read-only mode (archived).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>default<wbr>Branch</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default branch for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description of the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>http<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via HTTP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Integer that uniquely identifies the project within the gitlab install.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>issues<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Enable issue tracking for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>lfs<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Enable LFS for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>merge<wbr>Requests<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Enable merge requests for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>namespace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The namespace (group or user) of the project. Defaults to your user.
See `gitlab..Group` for an example.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The path of the repository.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>pipelines<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Enable pipelines for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>request<wbr>Access<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Allow users to request member access.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>runners<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registration token to use during runner setup.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>snippets<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Enable snippets for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ssh<wbr>Url<wbr>To<wbr>Repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via SSH.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>visibility<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Repositories are created as private by default.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>web<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}URL that can be used to find the project in a browser.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>wiki<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Enable wiki for the project.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>archived</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the project is in read-only mode (archived).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>default_<wbr>branch</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The default branch for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description of the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>http_<wbr>url_<wbr>to_<wbr>repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via HTTP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Integer that uniquely identifies the project within the gitlab install.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>issues_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable issue tracking for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>lfs_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable LFS for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>merge_<wbr>requests_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable merge requests for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>namespace_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The namespace (group or user) of the project. Defaults to your user.
See `gitlab..Group` for an example.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The path of the repository.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>pipelines_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable pipelines for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>request_<wbr>access_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Allow users to request member access.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>runners_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registration token to use during runner setup.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>snippets_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable snippets for the project.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ssh_<wbr>url_<wbr>to_<wbr>repo</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL that can be provided to `git clone` to clone the
repository via SSH.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>visibility_<wbr>level</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Repositories are created as private by default.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>web_<wbr>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}URL that can be used to find the project in a browser.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>wiki_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable wiki for the project.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







