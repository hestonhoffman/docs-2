
---
title: "GetKubernetesCluster"
block_external_search_index: true
---








## Using GetKubernetesCluster

{{< chooser language "javascript,typescript,python,go,csharp" / >}}


{{% choosable language typescript %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getKubernetesCluster<span class="p">(</span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/digitalocean/#GetKubernetesClusterArgs">GetKubernetesClusterArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/digitalocean/#GetKubernetesClusterResult">GetKubernetesClusterResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_kubernetes_cluster(</span>name=None<span class="p">, </span>tags=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupKubernetesCluster<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-digitalocean/sdk/go/digitalocean/?tab=doc#GetKubernetesClusterArgs">GetKubernetesClusterArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-digitalocean/sdk/go/digitalocean/?tab=doc#LookupKubernetesClusterResult">LookupKubernetesClusterResult</a></span>, error)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetKubernetesCluster </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Digitalocean/Pulumi.Digitalocean.GetKubernetesClusterResult.html">GetKubernetesClusterResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Digitalocean/Pulumi.Digitalocean.GetKubernetesClusterArgs.html">GetKubernetesClusterArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span>? <span class="nx">opts = null<span class="p">)</span><span class="p">
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
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
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
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
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
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
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
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetKubernetesCluster Result

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses in the overlay network of the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Created<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The base URL of the API server on the Kubernetes master node.
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
        <span>Ipv4Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The public IPv4 address of the Kubernetes master node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kube<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusterkubeconfig">List&lt;Get<wbr>Kubernetes<wbr>Cluster<wbr>Kube<wbr>Config&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Node<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusternodepool">List&lt;Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of node pools associated with the cluster. Each node pool exports the following attributes:
- `id` -  The unique ID that can be used to identify and reference the node pool.
- `name` - The name of the node pool.
- `size` - The slug identifier for the type of Droplet used as workers in the node pool.
- `node_count` - The number of Droplet instances in the node pool.
- `actual_node_count` - The actual number of nodes in the node pool, which is especially useful when auto-scaling is enabled.
- `auto_scale` - A boolean indicating whether auto-scaling is enabled on the node pool.
- `min_nodes` - If auto-scaling is enabled, this represents the minimum number of nodes that the node pool can be scaled down to.
- `max_nodes` - If auto-scaling is enabled, this represents the maximum number of nodes that the node pool can be scaled up to.
- `tags` - A list of tag names applied to the node pool.
- `labels` - A map of key/value pairs applied to nodes in the pool. The labels are exposed in the Kubernetes API as labels in the metadata of the corresponding [Node resources](https://kubernetes.io/docs/concepts/architecture/nodes/).
- `nodes` - A list of nodes in the pool. Each node exports the following attributes:
+ `id` -  A unique ID that can be used to identify and reference the node.
+ `name` - The auto-generated name for the node.
+ `status` -  A string indicating the current status of the individual node.
+ `created_at` - The date and time when the node was created.
+ `updated_at` - The date and time when the node was last updated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The slug identifier for the region where the Kubernetes cluster is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Service<wbr>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of assignable IP addresses for services running in the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string indicating the current status of the cluster. Potential values include running, provisioning, and errored.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Updated<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was last updated.
* `kube_config.0` - A representation of the Kubernetes cluster's kubeconfig with the following attributes:
- `raw_config` - The full contents of the Kubernetes cluster's kubeconfig file.
- `host` - The URL of the API server on the Kubernetes master node.
- `cluster_ca_certificate` - The base64 encoded public certificate for the cluster's certificate authority.
- `token` - The DigitalOcean API access token used by clients to access the cluster.
- `client_key` - The base64 encoded private key used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `client_certificate` - The base64 encoded public certificate used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `expires_at` - The date and time when the credentials will expire and need to be regenerated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The slug identifier for the version of Kubernetes used for the cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses in the overlay network of the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Created<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The base URL of the API server on the Kubernetes master node.
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
        <span>Ipv4Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The public IPv4 address of the Kubernetes master node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kube<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusterkubeconfig">[]Get<wbr>Kubernetes<wbr>Cluster<wbr>Kube<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Node<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusternodepool">[]Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool</a></span>
    </dt>
    <dd>{{% md %}}A list of node pools associated with the cluster. Each node pool exports the following attributes:
- `id` -  The unique ID that can be used to identify and reference the node pool.
- `name` - The name of the node pool.
- `size` - The slug identifier for the type of Droplet used as workers in the node pool.
- `node_count` - The number of Droplet instances in the node pool.
- `actual_node_count` - The actual number of nodes in the node pool, which is especially useful when auto-scaling is enabled.
- `auto_scale` - A boolean indicating whether auto-scaling is enabled on the node pool.
- `min_nodes` - If auto-scaling is enabled, this represents the minimum number of nodes that the node pool can be scaled down to.
- `max_nodes` - If auto-scaling is enabled, this represents the maximum number of nodes that the node pool can be scaled up to.
- `tags` - A list of tag names applied to the node pool.
- `labels` - A map of key/value pairs applied to nodes in the pool. The labels are exposed in the Kubernetes API as labels in the metadata of the corresponding [Node resources](https://kubernetes.io/docs/concepts/architecture/nodes/).
- `nodes` - A list of nodes in the pool. Each node exports the following attributes:
+ `id` -  A unique ID that can be used to identify and reference the node.
+ `name` - The auto-generated name for the node.
+ `status` -  A string indicating the current status of the individual node.
+ `created_at` - The date and time when the node was created.
+ `updated_at` - The date and time when the node was last updated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The slug identifier for the region where the Kubernetes cluster is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Service<wbr>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of assignable IP addresses for services running in the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string indicating the current status of the cluster. Potential values include running, provisioning, and errored.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Updated<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was last updated.
* `kube_config.0` - A representation of the Kubernetes cluster's kubeconfig with the following attributes:
- `raw_config` - The full contents of the Kubernetes cluster's kubeconfig file.
- `host` - The URL of the API server on the Kubernetes master node.
- `cluster_ca_certificate` - The base64 encoded public certificate for the cluster's certificate authority.
- `token` - The DigitalOcean API access token used by clients to access the cluster.
- `client_key` - The base64 encoded private key used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `client_certificate` - The base64 encoded public certificate used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `expires_at` - The date and time when the credentials will expire and need to be regenerated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The slug identifier for the version of Kubernetes used for the cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>cluster<wbr>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses in the overlay network of the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>created<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The base URL of the API server on the Kubernetes master node.
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
        <span>ipv4Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The public IPv4 address of the Kubernetes master node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kube<wbr>Configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusterkubeconfig">Get<wbr>Kubernetes<wbr>Cluster<wbr>Kube<wbr>Config[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>node<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusternodepool">Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool[]</a></span>
    </dt>
    <dd>{{% md %}}A list of node pools associated with the cluster. Each node pool exports the following attributes:
- `id` -  The unique ID that can be used to identify and reference the node pool.
- `name` - The name of the node pool.
- `size` - The slug identifier for the type of Droplet used as workers in the node pool.
- `node_count` - The number of Droplet instances in the node pool.
- `actual_node_count` - The actual number of nodes in the node pool, which is especially useful when auto-scaling is enabled.
- `auto_scale` - A boolean indicating whether auto-scaling is enabled on the node pool.
- `min_nodes` - If auto-scaling is enabled, this represents the minimum number of nodes that the node pool can be scaled down to.
- `max_nodes` - If auto-scaling is enabled, this represents the maximum number of nodes that the node pool can be scaled up to.
- `tags` - A list of tag names applied to the node pool.
- `labels` - A map of key/value pairs applied to nodes in the pool. The labels are exposed in the Kubernetes API as labels in the metadata of the corresponding [Node resources](https://kubernetes.io/docs/concepts/architecture/nodes/).
- `nodes` - A list of nodes in the pool. Each node exports the following attributes:
+ `id` -  A unique ID that can be used to identify and reference the node.
+ `name` - The auto-generated name for the node.
+ `status` -  A string indicating the current status of the individual node.
+ `created_at` - The date and time when the node was created.
+ `updated_at` - The date and time when the node was last updated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The slug identifier for the region where the Kubernetes cluster is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>service<wbr>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The range of assignable IP addresses for services running in the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string indicating the current status of the cluster. Potential values include running, provisioning, and errored.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>updated<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was last updated.
* `kube_config.0` - A representation of the Kubernetes cluster's kubeconfig with the following attributes:
- `raw_config` - The full contents of the Kubernetes cluster's kubeconfig file.
- `host` - The URL of the API server on the Kubernetes master node.
- `cluster_ca_certificate` - The base64 encoded public certificate for the cluster's certificate authority.
- `token` - The DigitalOcean API access token used by clients to access the cluster.
- `client_key` - The base64 encoded private key used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `client_certificate` - The base64 encoded public certificate used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `expires_at` - The date and time when the credentials will expire and need to be regenerated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The slug identifier for the version of Kubernetes used for the cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>cluster_<wbr>subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The range of IP addresses in the overlay network of the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>created_<wbr>at</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The base URL of the API server on the Kubernetes master node.
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
        <span>ipv4_<wbr>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The public IPv4 address of the Kubernetes master node.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kube_<wbr>configs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusterkubeconfig">List[Get<wbr>Kubernetes<wbr>Cluster<wbr>Kube<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>node_<wbr>pools</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusternodepool">List[Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool]</a></span>
    </dt>
    <dd>{{% md %}}A list of node pools associated with the cluster. Each node pool exports the following attributes:
- `id` -  The unique ID that can be used to identify and reference the node pool.
- `name` - The name of the node pool.
- `size` - The slug identifier for the type of Droplet used as workers in the node pool.
- `node_count` - The number of Droplet instances in the node pool.
- `actual_node_count` - The actual number of nodes in the node pool, which is especially useful when auto-scaling is enabled.
- `auto_scale` - A boolean indicating whether auto-scaling is enabled on the node pool.
- `min_nodes` - If auto-scaling is enabled, this represents the minimum number of nodes that the node pool can be scaled down to.
- `max_nodes` - If auto-scaling is enabled, this represents the maximum number of nodes that the node pool can be scaled up to.
- `tags` - A list of tag names applied to the node pool.
- `labels` - A map of key/value pairs applied to nodes in the pool. The labels are exposed in the Kubernetes API as labels in the metadata of the corresponding [Node resources](https://kubernetes.io/docs/concepts/architecture/nodes/).
- `nodes` - A list of nodes in the pool. Each node exports the following attributes:
+ `id` -  A unique ID that can be used to identify and reference the node.
+ `name` - The auto-generated name for the node.
+ `status` -  A string indicating the current status of the individual node.
+ `created_at` - The date and time when the node was created.
+ `updated_at` - The date and time when the node was last updated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The slug identifier for the region where the Kubernetes cluster is located.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>service_<wbr>subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The range of assignable IP addresses for services running in the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string indicating the current status of the cluster. Potential values include running, provisioning, and errored.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>updated_<wbr>at</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was last updated.
* `kube_config.0` - A representation of the Kubernetes cluster's kubeconfig with the following attributes:
- `raw_config` - The full contents of the Kubernetes cluster's kubeconfig file.
- `host` - The URL of the API server on the Kubernetes master node.
- `cluster_ca_certificate` - The base64 encoded public certificate for the cluster's certificate authority.
- `token` - The DigitalOcean API access token used by clients to access the cluster.
- `client_key` - The base64 encoded private key used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `client_certificate` - The base64 encoded public certificate used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `expires_at` - The date and time when the credentials will expire and need to be regenerated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The slug identifier for the version of Kubernetes used for the cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Supporting Types

<h4>Get<wbr>Kubernetes<wbr>Cluster<wbr>Kube<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/digitalocean/types/output/#GetKubernetesClusterKubeConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-digitalocean/sdk/go/digitalocean/?tab=doc#GetKubernetesClusterKubeConfig">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Cluster<wbr>Ca<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Expires<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Raw<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Cluster<wbr>Ca<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Expires<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Raw<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>client<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>cluster<wbr>Ca<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>expires<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>raw<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>client<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>cluster<wbr>Ca<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>expires<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>raw<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/digitalocean/types/output/#GetKubernetesClusterNodePool">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-digitalocean/sdk/go/digitalocean/?tab=doc#GetKubernetesClusterNodePool">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Actual<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Auto<wbr>Scale</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique ID that can be used to identify and reference a Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Max<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Min<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusternodepoolnode">List&lt;Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool<wbr>Node<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Actual<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Auto<wbr>Scale</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique ID that can be used to identify and reference a Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Max<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Min<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusternodepoolnode">[]Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool<wbr>Node</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>actual<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>auto<wbr>Scale</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique ID that can be used to identify and reference a Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>max<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>min<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusternodepoolnode">Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool<wbr>Node[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>actual_<wbr>node_<wbr>count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>auto_<wbr>scale</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique ID that can be used to identify and reference a Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>max_<wbr>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>min_<wbr>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>node_<wbr>count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getkubernetesclusternodepoolnode">List[Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool<wbr>Node]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of tag names to be applied to the Kubernetes cluster.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Get<wbr>Kubernetes<wbr>Cluster<wbr>Node<wbr>Pool<wbr>Node</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/digitalocean/types/output/#GetKubernetesClusterNodePoolNode">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-digitalocean/sdk/go/digitalocean/?tab=doc#GetKubernetesClusterNodePoolNode">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Created<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Droplet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique ID that can be used to identify and reference a Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string indicating the current status of the cluster. Potential values include running, provisioning, and errored.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Updated<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was last updated.
* `kube_config.0` - A representation of the Kubernetes cluster's kubeconfig with the following attributes:
- `raw_config` - The full contents of the Kubernetes cluster's kubeconfig file.
- `host` - The URL of the API server on the Kubernetes master node.
- `cluster_ca_certificate` - The base64 encoded public certificate for the cluster's certificate authority.
- `token` - The DigitalOcean API access token used by clients to access the cluster.
- `client_key` - The base64 encoded private key used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `client_certificate` - The base64 encoded public certificate used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `expires_at` - The date and time when the credentials will expire and need to be regenerated.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Created<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Droplet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique ID that can be used to identify and reference a Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string indicating the current status of the cluster. Potential values include running, provisioning, and errored.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Updated<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was last updated.
* `kube_config.0` - A representation of the Kubernetes cluster's kubeconfig with the following attributes:
- `raw_config` - The full contents of the Kubernetes cluster's kubeconfig file.
- `host` - The URL of the API server on the Kubernetes master node.
- `cluster_ca_certificate` - The base64 encoded public certificate for the cluster's certificate authority.
- `token` - The DigitalOcean API access token used by clients to access the cluster.
- `client_key` - The base64 encoded private key used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `client_certificate` - The base64 encoded public certificate used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `expires_at` - The date and time when the credentials will expire and need to be regenerated.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>created<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>droplet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique ID that can be used to identify and reference a Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string indicating the current status of the cluster. Potential values include running, provisioning, and errored.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>updated<wbr>At</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was last updated.
* `kube_config.0` - A representation of the Kubernetes cluster's kubeconfig with the following attributes:
- `raw_config` - The full contents of the Kubernetes cluster's kubeconfig file.
- `host` - The URL of the API server on the Kubernetes master node.
- `cluster_ca_certificate` - The base64 encoded public certificate for the cluster's certificate authority.
- `token` - The DigitalOcean API access token used by clients to access the cluster.
- `client_key` - The base64 encoded private key used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `client_certificate` - The base64 encoded public certificate used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `expires_at` - The date and time when the credentials will expire and need to be regenerated.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>created_<wbr>at</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>droplet_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique ID that can be used to identify and reference a Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of Kubernetes cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string indicating the current status of the cluster. Potential values include running, provisioning, and errored.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>updated_<wbr>at</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The date and time when the Kubernetes cluster was last updated.
* `kube_config.0` - A representation of the Kubernetes cluster's kubeconfig with the following attributes:
- `raw_config` - The full contents of the Kubernetes cluster's kubeconfig file.
- `host` - The URL of the API server on the Kubernetes master node.
- `cluster_ca_certificate` - The base64 encoded public certificate for the cluster's certificate authority.
- `token` - The DigitalOcean API access token used by clients to access the cluster.
- `client_key` - The base64 encoded private key used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `client_certificate` - The base64 encoded public certificate used by clients to access the cluster. Only available if token authentication is not supported on your cluster.
- `expires_at` - The date and time when the credentials will expire and need to be regenerated.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







