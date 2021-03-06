
---
title: "GetCluster"
block_external_search_index: true
---



Use this data source to get the ID of an available OpenStack Magnum cluster.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as openstack from "@pulumi/openstack";

const cluster1 = pulumi.output(openstack.containerinfra.getCluster({
    name: "cluster_1",
}, { async: true }));
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-openstack/blob/master/website/docs/d/containerinfra_cluster_v1.html.markdown.





## Using GetCluster

{{< chooser language "javascript,typescript,python,go,csharp" / >}}


{{% choosable language typescript %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getCluster<span class="p">(</span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/containerinfra/#GetClusterArgs">GetClusterArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/containerinfra/#GetClusterResult">GetClusterResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_cluster(</span>name=None<span class="p">, </span>region=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupCluster<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/containerinfra?tab=doc#LookupClusterArgs">LookupClusterArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/containerinfra?tab=doc#LookupClusterResult">LookupClusterResult</a></span>, error)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetCluster </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.Containerinfra.GetClusterResult.html">GetClusterResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.ContainerInfra.GetClusterArgs.html">GetClusterArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span>? <span class="nx">opts = null<span class="p">)</span><span class="p">
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
    <dd>{{% md %}}The name of the cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V1 Container Infra
client.
If omitted, the `region` argument of the provider is used.
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
    <dd>{{% md %}}The name of the cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V1 Container Infra
client.
If omitted, the `region` argument of the provider is used.
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
    <dd>{{% md %}}The name of the cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V1 Container Infra
client.
If omitted, the `region` argument of the provider is used.
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
    <dd>{{% md %}}The name of the cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V1 Container Infra
client.
If omitted, the `region` argument of the provider is used.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetCluster Result

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Api<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}COE API address.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The UUID of the V1 Container Infra cluster template.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Coe<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}COE software version.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Container<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Create<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The timeout (in minutes) for creating the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Created<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time at which cluster was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Discovery<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL used for cluster node discovery.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Docker<wbr>Volume<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The size (in GB) of the Docker volume.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fixed<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fixed network that is attached to the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fixed<wbr>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fixed subnet that is attached to the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Flavor</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The flavor for the nodes of the cluster.
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
        <span>Keypair</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Compute service SSH keypair.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object></span>
    </dt>
    <dd>{{% md %}}The list of key value pairs representing additional properties of
the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Master<wbr>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}IP addresses of the master node of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Master<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of master nodes for the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Master<wbr>Flavor</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The flavor for the master nodes.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}See Argument Reference above.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Node<wbr>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}IP addresses of the node of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of nodes for the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The project of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}See Argument Reference above.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the Orchestration service stack.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Updated<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time at which cluster was updated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user of the cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Api<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}COE API address.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The UUID of the V1 Container Infra cluster template.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Coe<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}COE software version.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Container<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Create<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The timeout (in minutes) for creating the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Created<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time at which cluster was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Discovery<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL used for cluster node discovery.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Docker<wbr>Volume<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The size (in GB) of the Docker volume.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fixed<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fixed network that is attached to the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fixed<wbr>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fixed subnet that is attached to the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Flavor</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The flavor for the nodes of the cluster.
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
        <span>Keypair</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Compute service SSH keypair.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}The list of key value pairs representing additional properties of
the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Master<wbr>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}IP addresses of the master node of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Master<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of master nodes for the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Master<wbr>Flavor</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The flavor for the master nodes.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}See Argument Reference above.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Node<wbr>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}IP addresses of the node of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of nodes for the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The project of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}See Argument Reference above.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the Orchestration service stack.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Updated<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time at which cluster was updated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user of the cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>api<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}COE API address.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The UUID of the V1 Container Infra cluster template.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>coe<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}COE software version.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>container<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>create<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The timeout (in minutes) for creating the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>created<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time at which cluster was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>discovery<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL used for cluster node discovery.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>docker<wbr>Volume<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The size (in GB) of the Docker volume.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fixed<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fixed network that is attached to the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fixed<wbr>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fixed subnet that is attached to the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>flavor</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The flavor for the nodes of the cluster.
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
        <span>keypair</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Compute service SSH keypair.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}The list of key value pairs representing additional properties of
the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>master<wbr>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}IP addresses of the master node of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>master<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The number of master nodes for the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>master<wbr>Flavor</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The flavor for the master nodes.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}See Argument Reference above.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>node<wbr>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}IP addresses of the node of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The number of nodes for the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The project of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}See Argument Reference above.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>stack<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the Orchestration service stack.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>updated<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time at which cluster was updated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user of the cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>api_<wbr>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}COE API address.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster_<wbr>template_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The UUID of the V1 Container Infra cluster template.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>coe_<wbr>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}COE software version.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>container_<wbr>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>create_<wbr>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The timeout (in minutes) for creating the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>created_<wbr>at</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The time at which cluster was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>discovery_<wbr>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URL used for cluster node discovery.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>docker_<wbr>volume_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The size (in GB) of the Docker volume.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fixed_<wbr>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The fixed network that is attached to the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fixed_<wbr>subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The fixed subnet that is attached to the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>flavor</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The flavor for the nodes of the cluster.
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
        <span>keypair</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Compute service SSH keypair.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The list of key value pairs representing additional properties of
the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>master_<wbr>addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}IP addresses of the master node of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>master_<wbr>count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of master nodes for the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>master_<wbr>flavor</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The flavor for the master nodes.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}See Argument Reference above.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>node_<wbr>addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}IP addresses of the node of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>node_<wbr>count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of nodes for the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The project of the cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}See Argument Reference above.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>stack_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}UUID of the Orchestration service stack.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>updated_<wbr>at</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The time at which cluster was updated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The user of the cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







