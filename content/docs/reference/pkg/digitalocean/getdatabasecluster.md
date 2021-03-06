
---
title: "GetDatabaseCluster"
block_external_search_index: true
---



Provides information on a DigitalOcean database cluster resource.

> This content is derived from https://github.com/terraform-providers/terraform-provider-digitalocean/blob/master/website/docs/d/database_cluster.html.markdown.





## Using GetDatabaseCluster

{{< chooser language "javascript,typescript,python,go,csharp" / >}}


{{% choosable language typescript %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getDatabaseCluster<span class="p">(</span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/digitalocean/#GetDatabaseClusterArgs">GetDatabaseClusterArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/digitalocean/#GetDatabaseClusterResult">GetDatabaseClusterResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_database_cluster(</span>name=None<span class="p">, </span>tags=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupDatabaseCluster<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-digitalocean/sdk/go/digitalocean/?tab=doc#GetDatabaseClusterArgs">GetDatabaseClusterArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-digitalocean/sdk/go/digitalocean/?tab=doc#LookupDatabaseClusterResult">LookupDatabaseClusterResult</a></span>, error)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetDatabaseCluster </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Digitalocean/Pulumi.Digitalocean.GetDatabaseClusterResult.html">GetDatabaseClusterResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Digitalocean/Pulumi.Digitalocean.GetDatabaseClusterArgs.html">GetDatabaseClusterArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span>? <span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
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
    <dd>{{% md %}}The name of the database cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
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
    <dd>{{% md %}}The name of the database cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
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
    <dd>{{% md %}}The name of the database cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetDatabaseCluster Result

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Database</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the cluster's default database.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Engine</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Database engine used by the cluster (ex. `pg` for PostreSQL).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Database cluster's hostname.
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
        <span>Maintenance<wbr>Windows</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdatabaseclustermaintenancewindow">List&lt;Get<wbr>Database<wbr>Cluster<wbr>Maintenance<wbr>Window&gt;</a></span>
    </dt>
    <dd>{{% md %}}Defines when the automatic maintenance should be performed for the database cluster.
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
        <span>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Number of nodes that will be included in the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Password for the cluster's default user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Network port that the database cluster is listening on.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Private<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Same as `host`, but only accessible from resources within the account and in the same region.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Private<wbr>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Same as `uri`, but only accessible from resources within the account and in the same region.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}DigitalOcean region where the cluster will reside.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Database droplet size associated with the cluster (ex. `db-s-1vcpu-1gb`).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The full URI for connecting to the database cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Urn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The uniform resource name of the database cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Username for the cluster's default user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Engine version used by the cluster (ex. `11` for PostgreSQL 11).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Database</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the cluster's default database.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Engine</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Database engine used by the cluster (ex. `pg` for PostreSQL).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Database cluster's hostname.
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
        <span>Maintenance<wbr>Windows</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdatabaseclustermaintenancewindow">[]Get<wbr>Database<wbr>Cluster<wbr>Maintenance<wbr>Window</a></span>
    </dt>
    <dd>{{% md %}}Defines when the automatic maintenance should be performed for the database cluster.
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
        <span>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Number of nodes that will be included in the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Password for the cluster's default user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Network port that the database cluster is listening on.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Private<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Same as `host`, but only accessible from resources within the account and in the same region.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Private<wbr>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Same as `uri`, but only accessible from resources within the account and in the same region.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}DigitalOcean region where the cluster will reside.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Database droplet size associated with the cluster (ex. `db-s-1vcpu-1gb`).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The full URI for connecting to the database cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Urn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The uniform resource name of the database cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Username for the cluster's default user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Engine version used by the cluster (ex. `11` for PostgreSQL 11).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>database</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the cluster's default database.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>engine</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Database engine used by the cluster (ex. `pg` for PostreSQL).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Database cluster's hostname.
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
        <span>maintenance<wbr>Windows</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdatabaseclustermaintenancewindow">Get<wbr>Database<wbr>Cluster<wbr>Maintenance<wbr>Window[]</a></span>
    </dt>
    <dd>{{% md %}}Defines when the automatic maintenance should be performed for the database cluster.
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
        <span>node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Number of nodes that will be included in the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Password for the cluster's default user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Network port that the database cluster is listening on.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>private<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Same as `host`, but only accessible from resources within the account and in the same region.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>private<wbr>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Same as `uri`, but only accessible from resources within the account and in the same region.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}DigitalOcean region where the cluster will reside.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Database droplet size associated with the cluster (ex. `db-s-1vcpu-1gb`).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The full URI for connecting to the database cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>urn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The uniform resource name of the database cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Username for the cluster's default user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Engine version used by the cluster (ex. `11` for PostgreSQL 11).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>database</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the cluster's default database.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>engine</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Database engine used by the cluster (ex. `pg` for PostreSQL).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Database cluster's hostname.
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
        <span>maintenance_<wbr>windows</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getdatabaseclustermaintenancewindow">List[Get<wbr>Database<wbr>Cluster<wbr>Maintenance<wbr>Window]</a></span>
    </dt>
    <dd>{{% md %}}Defines when the automatic maintenance should be performed for the database cluster.
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
        <span>node_<wbr>count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Number of nodes that will be included in the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Password for the cluster's default user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Network port that the database cluster is listening on.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>private_<wbr>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Same as `host`, but only accessible from resources within the account and in the same region.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>private_<wbr>uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Same as `uri`, but only accessible from resources within the account and in the same region.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}DigitalOcean region where the cluster will reside.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Database droplet size associated with the cluster (ex. `db-s-1vcpu-1gb`).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>uri</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The full URI for connecting to the database cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>urn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The uniform resource name of the database cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Username for the cluster's default user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Engine version used by the cluster (ex. `11` for PostgreSQL 11).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Supporting Types

<h4>Get<wbr>Database<wbr>Cluster<wbr>Maintenance<wbr>Window</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/digitalocean/types/output/#GetDatabaseClusterMaintenanceWindow">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-digitalocean/sdk/go/digitalocean/?tab=doc#GetDatabaseClusterMaintenanceWindow">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Day</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The day of the week on which to apply maintenance updates.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Hour</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The hour in UTC at which maintenance updates will be applied in 24 hour format.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Day</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The day of the week on which to apply maintenance updates.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Hour</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The hour in UTC at which maintenance updates will be applied in 24 hour format.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>day</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The day of the week on which to apply maintenance updates.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>hour</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The hour in UTC at which maintenance updates will be applied in 24 hour format.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>day</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The day of the week on which to apply maintenance updates.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>hour</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The hour in UTC at which maintenance updates will be applied in 24 hour format.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







