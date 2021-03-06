
---
title: "Cluster"
block_external_search_index: true
---



Provides a Rancher v2 Cluster resource. This can be used to create Clusters for Rancher v2 environments and retrieve their information.

> This content is derived from https://github.com/terraform-providers/terraform-provider-rancher2/blob/master/website/docs/r/cluster.html.markdown.



## Create a Cluster Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/rancher2/#Cluster">Cluster</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/rancher2/#ClusterArgs">ClusterArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Cluster</span><span class="p">(resource_name, opts=None, </span>aks_config=None<span class="p">, </span>annotations=None<span class="p">, </span>cluster_auth_endpoint=None<span class="p">, </span>cluster_monitoring_input=None<span class="p">, </span>cluster_template_answers=None<span class="p">, </span>cluster_template_id=None<span class="p">, </span>cluster_template_questions=None<span class="p">, </span>cluster_template_revision_id=None<span class="p">, </span>default_pod_security_policy_template_id=None<span class="p">, </span>description=None<span class="p">, </span>desired_agent_image=None<span class="p">, </span>desired_auth_image=None<span class="p">, </span>docker_root_dir=None<span class="p">, </span>driver=None<span class="p">, </span>eks_config=None<span class="p">, </span>enable_cluster_alerting=None<span class="p">, </span>enable_cluster_istio=None<span class="p">, </span>enable_cluster_monitoring=None<span class="p">, </span>enable_network_policy=None<span class="p">, </span>gke_config=None<span class="p">, </span>k3s_config=None<span class="p">, </span>labels=None<span class="p">, </span>name=None<span class="p">, </span>rke_config=None<span class="p">, </span>scheduled_cluster_scan=None<span class="p">, </span>windows_prefered_cluster=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewCluster<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterArgs">ClusterArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#Cluster">Cluster</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Rancher2/Pulumi.Rancher2..Cluster.html">Cluster</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Rancher2/Pulumi.Rancher2.ClusterArgs.html">ClusterArgs</a></span>? <span class="nx">args = null<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Aks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">Cluster<wbr>Aks<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Auth<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Monitoring<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Cluster<wbr>Cluster<wbr>Template<wbr>Answers<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">List&lt;Cluster<wbr>Cluster<wbr>Template<wbr>Question<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Revision<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Pod<wbr>Security<wbr>Policy<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Agent<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Auth<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Root<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Eks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">Cluster<wbr>Eks<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">Cluster<wbr>Gke<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>K3s<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Cluster<wbr>K3s<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Cluster<wbr>Rke<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduled<wbr>Cluster<wbr>Scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Windows<wbr>Prefered<wbr>Cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">*Cluster<wbr>Aks<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Auth<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">*Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Monitoring<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">*Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">*Cluster<wbr>Cluster<wbr>Template<wbr>Answers</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">[]Cluster<wbr>Cluster<wbr>Template<wbr>Question</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Revision<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Pod<wbr>Security<wbr>Policy<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Agent<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Auth<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Root<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Eks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">*Cluster<wbr>Eks<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">*Cluster<wbr>Gke<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>K3s<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">*Cluster<wbr>K3s<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">*Cluster<wbr>Rke<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduled<wbr>Cluster<wbr>Scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">*Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Windows<wbr>Prefered<wbr>Cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">Cluster<wbr>Aks<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Auth<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint?</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Monitoring<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input?</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Template<wbr>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Cluster<wbr>Cluster<wbr>Template<wbr>Answers?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Template<wbr>Questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">Cluster<wbr>Cluster<wbr>Template<wbr>Question[]?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Template<wbr>Revision<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Pod<wbr>Security<wbr>Policy<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired<wbr>Agent<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired<wbr>Auth<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>docker<wbr>Root<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>eks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">Cluster<wbr>Eks<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Cluster<wbr>Alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Cluster<wbr>Istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Cluster<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">Cluster<wbr>Gke<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>k3s<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Cluster<wbr>K3s<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Cluster<wbr>Rke<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduled<wbr>Cluster<wbr>Scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan?</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>windows<wbr>Prefered<wbr>Cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aks_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">Dict[Cluster<wbr>Aks<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>auth_<wbr>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Dict[Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint]</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>monitoring_<wbr>input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Dict[Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input]</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>template_<wbr>answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Dict[Cluster<wbr>Cluster<wbr>Template<wbr>Answers]</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>template_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>template_<wbr>questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">List[Cluster<wbr>Cluster<wbr>Template<wbr>Question]</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>template_<wbr>revision_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default_<wbr>pod_<wbr>security_<wbr>policy_<wbr>template_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired_<wbr>agent_<wbr>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired_<wbr>auth_<wbr>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>docker_<wbr>root_<wbr>dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>eks_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">Dict[Cluster<wbr>Eks<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable_<wbr>cluster_<wbr>alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable_<wbr>cluster_<wbr>istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable_<wbr>cluster_<wbr>monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable_<wbr>network_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gke_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">Dict[Cluster<wbr>Gke<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>k3s_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Dict[Cluster<wbr>K3s<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rke_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Dict[Cluster<wbr>Rke<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduled_<wbr>cluster_<wbr>scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">Dict[Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan]</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>windows_<wbr>prefered_<wbr>cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Cluster Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Aks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">Cluster<wbr>Aks<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object></span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Auth<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Monitoring<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Registration<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterregistrationtoken">Cluster<wbr>Cluster<wbr>Registration<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}(Computed) Cluster Registration Token generated for the cluster (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Cluster<wbr>Cluster<wbr>Template<wbr>Answers</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">List&lt;Cluster<wbr>Cluster<wbr>Template<wbr>Question&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Revision<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Default<wbr>Pod<wbr>Security<wbr>Policy<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Default<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed) Default project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Desired<wbr>Agent<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Desired<wbr>Auth<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Docker<wbr>Root<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Eks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">Cluster<wbr>Eks<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Cluster<wbr>Alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Cluster<wbr>Istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Cluster<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Gke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">Cluster<wbr>Gke<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>K3s<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Cluster<wbr>K3s<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kube<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed/Sensitive) Kube Config generated for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object></span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Rke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Cluster<wbr>Rke<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Scheduled<wbr>Cluster<wbr>Scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan?</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>System<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed) System project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Windows<wbr>Prefered<wbr>Cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Aks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">*Cluster<wbr>Aks<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Auth<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Monitoring<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Registration<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterregistrationtoken">Cluster<wbr>Cluster<wbr>Registration<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}(Computed) Cluster Registration Token generated for the cluster (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Cluster<wbr>Cluster<wbr>Template<wbr>Answers</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">[]Cluster<wbr>Cluster<wbr>Template<wbr>Question</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cluster<wbr>Template<wbr>Revision<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Default<wbr>Pod<wbr>Security<wbr>Policy<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Default<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed) Default project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Desired<wbr>Agent<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Desired<wbr>Auth<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Docker<wbr>Root<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Eks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">*Cluster<wbr>Eks<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Cluster<wbr>Alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Cluster<wbr>Istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Cluster<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Gke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">*Cluster<wbr>Gke<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>K3s<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Cluster<wbr>K3s<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kube<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed/Sensitive) Kube Config generated for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Rke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Cluster<wbr>Rke<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Scheduled<wbr>Cluster<wbr>Scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">*Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>System<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed) System project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Windows<wbr>Prefered<wbr>Cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>aks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">Cluster<wbr>Aks<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster<wbr>Auth<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster<wbr>Monitoring<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster<wbr>Registration<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterregistrationtoken">Cluster<wbr>Cluster<wbr>Registration<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}(Computed) Cluster Registration Token generated for the cluster (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster<wbr>Template<wbr>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Cluster<wbr>Cluster<wbr>Template<wbr>Answers</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster<wbr>Template<wbr>Questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">Cluster<wbr>Cluster<wbr>Template<wbr>Question[]?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster<wbr>Template<wbr>Revision<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>default<wbr>Pod<wbr>Security<wbr>Policy<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>default<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed) Default project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>desired<wbr>Agent<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>desired<wbr>Auth<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>docker<wbr>Root<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>eks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">Cluster<wbr>Eks<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Cluster<wbr>Alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Cluster<wbr>Istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Cluster<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>gke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">Cluster<wbr>Gke<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>k3s<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Cluster<wbr>K3s<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kube<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed/Sensitive) Kube Config generated for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>rke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Cluster<wbr>Rke<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>scheduled<wbr>Cluster<wbr>Scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan?</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>system<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(Computed) System project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>windows<wbr>Prefered<wbr>Cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>aks_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">Dict[Cluster<wbr>Aks<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster_<wbr>auth_<wbr>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Dict[Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint]</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster_<wbr>monitoring_<wbr>input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Dict[Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input]</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster_<wbr>registration_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterregistrationtoken">Dict[Cluster<wbr>Cluster<wbr>Registration<wbr>Token]</a></span>
    </dt>
    <dd>{{% md %}}(Computed) Cluster Registration Token generated for the cluster (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster_<wbr>template_<wbr>answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Dict[Cluster<wbr>Cluster<wbr>Template<wbr>Answers]</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster_<wbr>template_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster_<wbr>template_<wbr>questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">List[Cluster<wbr>Cluster<wbr>Template<wbr>Question]</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cluster_<wbr>template_<wbr>revision_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>default_<wbr>pod_<wbr>security_<wbr>policy_<wbr>template_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>default_<wbr>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed) Default project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>desired_<wbr>agent_<wbr>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>desired_<wbr>auth_<wbr>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>docker_<wbr>root_<wbr>dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>eks_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">Dict[Cluster<wbr>Eks<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>cluster_<wbr>alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>cluster_<wbr>istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>cluster_<wbr>monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>network_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>gke_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">Dict[Cluster<wbr>Gke<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>k3s_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Dict[Cluster<wbr>K3s<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kube_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed/Sensitive) Kube Config generated for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>rke_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Dict[Cluster<wbr>Rke<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>scheduled_<wbr>cluster_<wbr>scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">Dict[Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan]</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>system_<wbr>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed) System project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>windows_<wbr>prefered_<wbr>cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Cluster Resource

Get an existing Cluster resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/rancher2/#ClusterState">ClusterState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/rancher2/#Cluster">Cluster</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>aks_config=None<span class="p">, </span>annotations=None<span class="p">, </span>cluster_auth_endpoint=None<span class="p">, </span>cluster_monitoring_input=None<span class="p">, </span>cluster_registration_token=None<span class="p">, </span>cluster_template_answers=None<span class="p">, </span>cluster_template_id=None<span class="p">, </span>cluster_template_questions=None<span class="p">, </span>cluster_template_revision_id=None<span class="p">, </span>default_pod_security_policy_template_id=None<span class="p">, </span>default_project_id=None<span class="p">, </span>description=None<span class="p">, </span>desired_agent_image=None<span class="p">, </span>desired_auth_image=None<span class="p">, </span>docker_root_dir=None<span class="p">, </span>driver=None<span class="p">, </span>eks_config=None<span class="p">, </span>enable_cluster_alerting=None<span class="p">, </span>enable_cluster_istio=None<span class="p">, </span>enable_cluster_monitoring=None<span class="p">, </span>enable_network_policy=None<span class="p">, </span>gke_config=None<span class="p">, </span>k3s_config=None<span class="p">, </span>kube_config=None<span class="p">, </span>labels=None<span class="p">, </span>name=None<span class="p">, </span>rke_config=None<span class="p">, </span>scheduled_cluster_scan=None<span class="p">, </span>system_project_id=None<span class="p">, </span>windows_prefered_cluster=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetCluster<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterState">ClusterState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#Cluster">Cluster</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Rancher2/Pulumi.Rancher2..Cluster.html">Cluster</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Rancher2/Pulumi.Rancher2..ClusterState.html">ClusterState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Aks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">Cluster<wbr>Aks<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Auth<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Monitoring<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Registration<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterregistrationtoken">Cluster<wbr>Cluster<wbr>Registration<wbr>Token<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}(Computed) Cluster Registration Token generated for the cluster (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Cluster<wbr>Cluster<wbr>Template<wbr>Answers<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">List&lt;Cluster<wbr>Cluster<wbr>Template<wbr>Question<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Revision<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Pod<wbr>Security<wbr>Policy<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) Default project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Agent<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Auth<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Root<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Eks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">Cluster<wbr>Eks<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">Cluster<wbr>Gke<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>K3s<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Cluster<wbr>K3s<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kube<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed/Sensitive) Kube Config generated for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Cluster<wbr>Rke<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduled<wbr>Cluster<wbr>Scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>System<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) System project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Windows<wbr>Prefered<wbr>Cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">*Cluster<wbr>Aks<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Auth<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">*Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Monitoring<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">*Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Registration<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterregistrationtoken">*Cluster<wbr>Cluster<wbr>Registration<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}(Computed) Cluster Registration Token generated for the cluster (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">*Cluster<wbr>Cluster<wbr>Template<wbr>Answers</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">[]Cluster<wbr>Cluster<wbr>Template<wbr>Question</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Template<wbr>Revision<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Pod<wbr>Security<wbr>Policy<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Computed) Default project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Agent<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Auth<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Root<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Eks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">*Cluster<wbr>Eks<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Cluster<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">*Cluster<wbr>Gke<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>K3s<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">*Cluster<wbr>K3s<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kube<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Computed/Sensitive) Kube Config generated for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">*Cluster<wbr>Rke<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduled<wbr>Cluster<wbr>Scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">*Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>System<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Computed) System project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Windows<wbr>Prefered<wbr>Cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">Cluster<wbr>Aks<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Auth<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint?</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Monitoring<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input?</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Registration<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterregistrationtoken">Cluster<wbr>Cluster<wbr>Registration<wbr>Token?</a></span>
    </dt>
    <dd>{{% md %}}(Computed) Cluster Registration Token generated for the cluster (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Template<wbr>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Cluster<wbr>Cluster<wbr>Template<wbr>Answers?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Template<wbr>Questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">Cluster<wbr>Cluster<wbr>Template<wbr>Question[]?</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Template<wbr>Revision<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Pod<wbr>Security<wbr>Policy<wbr>Template<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) Default project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired<wbr>Agent<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired<wbr>Auth<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>docker<wbr>Root<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>eks<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">Cluster<wbr>Eks<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Cluster<wbr>Alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Cluster<wbr>Istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Cluster<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">Cluster<wbr>Gke<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>k3s<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Cluster<wbr>K3s<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kube<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed/Sensitive) Kube Config generated for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rke<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Cluster<wbr>Rke<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduled<wbr>Cluster<wbr>Scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan?</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>system<wbr>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) System project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>windows<wbr>Prefered<wbr>Cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aks_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusteraksconfig">Dict[Cluster<wbr>Aks<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The Azure AKS configuration for `aks` Clusters. Conflicts with `eks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>auth_<wbr>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterauthendpoint">Dict[Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint]</a></span>
    </dt>
    <dd>{{% md %}}Enabling the [local cluster authorized endpoint](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#local-cluster-auth-endpoint) allows direct communication with the cluster, bypassing the Rancher API proxy. (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>monitoring_<wbr>input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustermonitoringinput">Dict[Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input]</a></span>
    </dt>
    <dd>{{% md %}}Cluster monitoring config. Any parameter defined in [rancher-monitoring charts](https://github.com/rancher/system-charts/tree/dev/charts/rancher-monitoring) could be configured  (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>registration_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclusterregistrationtoken">Dict[Cluster<wbr>Cluster<wbr>Registration<wbr>Token]</a></span>
    </dt>
    <dd>{{% md %}}(Computed) Cluster Registration Token generated for the cluster (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>template_<wbr>answers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplateanswers">Dict[Cluster<wbr>Cluster<wbr>Template<wbr>Answers]</a></span>
    </dt>
    <dd>{{% md %}}Cluster template answers. Just for Rancher v2.3.x and above (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>template_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster template ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>template_<wbr>questions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterclustertemplatequestion">List[Cluster<wbr>Cluster<wbr>Template<wbr>Question]</a></span>
    </dt>
    <dd>{{% md %}}Cluster template questions. Just for Rancher v2.3.x and above (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>template_<wbr>revision_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster template revision ID. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default_<wbr>pod_<wbr>security_<wbr>policy_<wbr>template_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}[Default pod security policy template id](https://rancher.com/docs/rancher/v2.x/en/cluster-provisioning/rke-clusters/options/#pod-security-policy-support) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default_<wbr>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed) Default project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired_<wbr>agent_<wbr>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Desired agent image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired_<wbr>auth_<wbr>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>docker_<wbr>root_<wbr>dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Desired auth image. Just for Rancher v2.3.x and above (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed) The driver used for the Cluster. `imported`, `azurekubernetesservice`, `amazonelasticcontainerservice`, `googlekubernetesengine` and `rancherKubernetesEngine` are supported (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>eks_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustereksconfig">Dict[Cluster<wbr>Eks<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The Amazon EKS configuration for `eks` Clusters. Conflicts with `aks_config`, `gke_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable_<wbr>cluster_<wbr>alerting</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster alerting. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable_<wbr>cluster_<wbr>istio</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster istio. Default `false`. Just for Rancher v2.3.x and above (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable_<wbr>cluster_<wbr>monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable built-in cluster monitoring. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable_<wbr>network_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable project network isolation. Default `false` (bool)
* `scheduled_cluster_scan`- (Optional) Cluster scheduled cis scan. For Rancher v2.4.0 or above (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gke_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clustergkeconfig">Dict[Cluster<wbr>Gke<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The Google GKE configuration for `gke` Clusters. Conflicts with `aks_config`, `eks_config`, `k3s_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>k3s_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfig">Dict[Cluster<wbr>K3s<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The K3S configuration for `k3s` imported Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `rke_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kube_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed/Sensitive) Kube Config generated for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rke_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfig">Dict[Cluster<wbr>Rke<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The RKE configuration for `rke` Clusters. Conflicts with `aks_config`, `eks_config`, `gke_config` and `k3s_config` (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduled_<wbr>cluster_<wbr>scan</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscan">Dict[Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan]</a></span>
    </dt>
    <dd>{{% md %}}Cluster scheduled scan
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>system_<wbr>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed) System project ID for the cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>windows_<wbr>prefered_<wbr>cluster</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Windows preferred cluster. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Cluster<wbr>Aks<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterAksConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterAksConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterAksConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterAksConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aad<wbr>Server<wbr>App<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The secret of an Azure Active Directory server application (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Aad<wbr>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory tenant (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>Client<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory client application of type \"Native\". This application is for user login via kubectl (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>Server<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory server application of type \"Web app/API\". This application represents the managed cluster's apiserver (Server application) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Admin<wbr>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The administrator username to use for Linux hosts. Default `azureuser` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Agent<wbr>Dns<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}DNS prefix to be used to create the FQDN for the agent pool (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Agent<wbr>Os<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}GB size to be used to specify the disk for every machine in the agent pool. If you specify 0, it will apply the default according to the \"agent vm size\" specified. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Agent<wbr>Pool<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name for the agent pool, upto 12 alphanumeric characters. Default `agentpool0` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Agent<wbr>Storage<wbr>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Storage profile specifies what kind of storage used on machine in the agent pool. Chooses from [ManagedDisks StorageAccount]. Default `ManagedDisks` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Agent<wbr>Vm<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Size of machine in the agent pool. Default `Standard_D1_v2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auth<wbr>Base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Different authentication API url to use. Default `https://login.microsoftonline.com/` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Different resource management API url to use. Default `https://management.azure.com/` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure client secret associated with the \"client id\" (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Number of machines (VMs) in the agent pool. Allowed values must be in the range of 1 to 100 (inclusive). Default `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Service<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An IP address assigned to the Kubernetes DNS service. It must be within the Kubernetes Service address range specified in \"service cidr\". Default `10.0.0.10` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Bridge<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range assigned to the Docker bridge network. It must not overlap with any Subnet IP ranges or the Kubernetes Service address range specified in \"service cidr\". Default `172.17.0.1/16` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Http<wbr>Application<wbr>Routing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable the Kubernetes ingress with automatic public DNS name creation. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Turn on Azure Log Analytics monitoring. Uses the Log Analytics \"Default\" workspace if it exists, else creates one. if using an existing workspace, specifies \"log analytics workspace resource id\". Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Azure Kubernetes cluster location. Default `eastus` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Workspace</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of an existing Azure Log Analytics Workspace to use for storing monitoring data. If not specified, uses '{resource group}-{subscription id}-{location code}' (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Workspace<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The resource group of an existing Azure Log Analytics Workspace to use for storing monitoring data. If not specified, uses the 'Cluster' resource group (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Master<wbr>Dns<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}DNS prefix to use the Kubernetes cluster control pane (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Pods</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Maximum number of pods that can run on a node. Default `110` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Plugin</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network plugin used for building Kubernetes network. Chooses from `azure` or `kubenet`. Default `azure` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network policy used for building Kubernetes network. Chooses from `calico` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pod<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range from which to assign Kubernetes Pod IPs when \"network plugin\" is specified in \"kubenet\". Default `172.244.0.0/16` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Cluster resource group (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range from which to assign Kubernetes Service cluster IPs. It must not overlap with any Subnet IP ranges. Default `10.0.0.0/16` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ssh<wbr>Public<wbr>Key<wbr>Contents</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Contents of the SSH public key used to authenticate with Linux hosts (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of an existing Azure Virtual Subnet. Composite of agent virtual network subnet ID (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Subscription<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subscription credentials which uniquely identify Microsoft Azure subscription (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Tags for Kubernetes cluster. For example, foo=bar (map)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Virtual<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the virtual network to use. If it's not specified Rancher will create a new VPC (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Virtual<wbr>Network<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource group of an existing Azure Virtual Network. Composite of agent virtual network subnet ID (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aad<wbr>Server<wbr>App<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The secret of an Azure Active Directory server application (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Aad<wbr>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory tenant (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>Client<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory client application of type \"Native\". This application is for user login via kubectl (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>Server<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory server application of type \"Web app/API\". This application represents the managed cluster's apiserver (Server application) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Admin<wbr>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The administrator username to use for Linux hosts. Default `azureuser` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Agent<wbr>Dns<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}DNS prefix to be used to create the FQDN for the agent pool (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Agent<wbr>Os<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}GB size to be used to specify the disk for every machine in the agent pool. If you specify 0, it will apply the default according to the \"agent vm size\" specified. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Agent<wbr>Pool<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name for the agent pool, upto 12 alphanumeric characters. Default `agentpool0` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Agent<wbr>Storage<wbr>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Storage profile specifies what kind of storage used on machine in the agent pool. Chooses from [ManagedDisks StorageAccount]. Default `ManagedDisks` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Agent<wbr>Vm<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Size of machine in the agent pool. Default `Standard_D1_v2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auth<wbr>Base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Different authentication API url to use. Default `https://login.microsoftonline.com/` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Different resource management API url to use. Default `https://management.azure.com/` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure client secret associated with the \"client id\" (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Number of machines (VMs) in the agent pool. Allowed values must be in the range of 1 to 100 (inclusive). Default `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Service<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}An IP address assigned to the Kubernetes DNS service. It must be within the Kubernetes Service address range specified in \"service cidr\". Default `10.0.0.10` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Bridge<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range assigned to the Docker bridge network. It must not overlap with any Subnet IP ranges or the Kubernetes Service address range specified in \"service cidr\". Default `172.17.0.1/16` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Http<wbr>Application<wbr>Routing</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable the Kubernetes ingress with automatic public DNS name creation. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Turn on Azure Log Analytics monitoring. Uses the Log Analytics \"Default\" workspace if it exists, else creates one. if using an existing workspace, specifies \"log analytics workspace resource id\". Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Azure Kubernetes cluster location. Default `eastus` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Workspace</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of an existing Azure Log Analytics Workspace to use for storing monitoring data. If not specified, uses '{resource group}-{subscription id}-{location code}' (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Workspace<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The resource group of an existing Azure Log Analytics Workspace to use for storing monitoring data. If not specified, uses the 'Cluster' resource group (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Master<wbr>Dns<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}DNS prefix to use the Kubernetes cluster control pane (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Pods</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Maximum number of pods that can run on a node. Default `110` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Plugin</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Network plugin used for building Kubernetes network. Chooses from `azure` or `kubenet`. Default `azure` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Network policy used for building Kubernetes network. Chooses from `calico` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pod<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range from which to assign Kubernetes Pod IPs when \"network plugin\" is specified in \"kubenet\". Default `172.244.0.0/16` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Cluster resource group (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range from which to assign Kubernetes Service cluster IPs. It must not overlap with any Subnet IP ranges. Default `10.0.0.0/16` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ssh<wbr>Public<wbr>Key<wbr>Contents</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Contents of the SSH public key used to authenticate with Linux hosts (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of an existing Azure Virtual Subnet. Composite of agent virtual network subnet ID (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Subscription<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subscription credentials which uniquely identify Microsoft Azure subscription (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Tags for Kubernetes cluster. For example, foo=bar (map)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Virtual<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the virtual network to use. If it's not specified Rancher will create a new VPC (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Virtual<wbr>Network<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource group of an existing Azure Virtual Network. Composite of agent virtual network subnet ID (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aad<wbr>Server<wbr>App<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The secret of an Azure Active Directory server application (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>aad<wbr>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory tenant (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>add<wbr>Client<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory client application of type \"Native\". This application is for user login via kubectl (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>add<wbr>Server<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory server application of type \"Web app/API\". This application represents the managed cluster's apiserver (Server application) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>admin<wbr>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The administrator username to use for Linux hosts. Default `azureuser` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>agent<wbr>Dns<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}DNS prefix to be used to create the FQDN for the agent pool (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>agent<wbr>Os<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}GB size to be used to specify the disk for every machine in the agent pool. If you specify 0, it will apply the default according to the \"agent vm size\" specified. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>agent<wbr>Pool<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name for the agent pool, upto 12 alphanumeric characters. Default `agentpool0` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>agent<wbr>Storage<wbr>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Storage profile specifies what kind of storage used on machine in the agent pool. Chooses from [ManagedDisks StorageAccount]. Default `ManagedDisks` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>agent<wbr>Vm<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Size of machine in the agent pool. Default `Standard_D1_v2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auth<wbr>Base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Different authentication API url to use. Default `https://login.microsoftonline.com/` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Different resource management API url to use. Default `https://management.azure.com/` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure client secret associated with the \"client id\" (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Number of machines (VMs) in the agent pool. Allowed values must be in the range of 1 to 100 (inclusive). Default `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns<wbr>Service<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An IP address assigned to the Kubernetes DNS service. It must be within the Kubernetes Service address range specified in \"service cidr\". Default `10.0.0.10` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>docker<wbr>Bridge<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range assigned to the Docker bridge network. It must not overlap with any Subnet IP ranges or the Kubernetes Service address range specified in \"service cidr\". Default `172.17.0.1/16` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Http<wbr>Application<wbr>Routing</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable the Kubernetes ingress with automatic public DNS name creation. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Turn on Azure Log Analytics monitoring. Uses the Log Analytics \"Default\" workspace if it exists, else creates one. if using an existing workspace, specifies \"log analytics workspace resource id\". Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Azure Kubernetes cluster location. Default `eastus` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log<wbr>Analytics<wbr>Workspace</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of an existing Azure Log Analytics Workspace to use for storing monitoring data. If not specified, uses '{resource group}-{subscription id}-{location code}' (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log<wbr>Analytics<wbr>Workspace<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The resource group of an existing Azure Log Analytics Workspace to use for storing monitoring data. If not specified, uses the 'Cluster' resource group (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>master<wbr>Dns<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}DNS prefix to use the Kubernetes cluster control pane (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Pods</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Maximum number of pods that can run on a node. Default `110` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network<wbr>Plugin</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network plugin used for building Kubernetes network. Chooses from `azure` or `kubenet`. Default `azure` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Network policy used for building Kubernetes network. Chooses from `calico` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pod<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range from which to assign Kubernetes Pod IPs when \"network plugin\" is specified in \"kubenet\". Default `172.244.0.0/16` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Cluster resource group (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range from which to assign Kubernetes Service cluster IPs. It must not overlap with any Subnet IP ranges. Default `10.0.0.0/16` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ssh<wbr>Public<wbr>Key<wbr>Contents</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Contents of the SSH public key used to authenticate with Linux hosts (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of an existing Azure Virtual Subnet. Composite of agent virtual network subnet ID (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>subscription<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subscription credentials which uniquely identify Microsoft Azure subscription (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Tags for Kubernetes cluster. For example, foo=bar (map)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>virtual<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the virtual network to use. If it's not specified Rancher will create a new VPC (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>virtual<wbr>Network<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource group of an existing Azure Virtual Network. Composite of agent virtual network subnet ID (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aad<wbr>Server<wbr>App<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The secret of an Azure Active Directory server application (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>aad<wbr>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory tenant (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>add<wbr>Client<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory client application of type \"Native\". This application is for user login via kubectl (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>add<wbr>Server<wbr>App<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of an Azure Active Directory server application of type \"Web app/API\". This application represents the managed cluster's apiserver (Server application) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>admin<wbr>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The administrator username to use for Linux hosts. Default `azureuser` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>agent<wbr>Dns<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}DNS prefix to be used to create the FQDN for the agent pool (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>agent<wbr>Os<wbr>Disk<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}GB size to be used to specify the disk for every machine in the agent pool. If you specify 0, it will apply the default according to the \"agent vm size\" specified. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>agent<wbr>Pool<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name for the agent pool, upto 12 alphanumeric characters. Default `agentpool0` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>agent<wbr>Storage<wbr>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Storage profile specifies what kind of storage used on machine in the agent pool. Chooses from [ManagedDisks StorageAccount]. Default `ManagedDisks` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>agent<wbr>Vm<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Size of machine in the agent pool. Default `Standard_D1_v2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auth<wbr>Base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Different authentication API url to use. Default `https://login.microsoftonline.com/` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Different resource management API url to use. Default `https://management.azure.com/` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client_<wbr>secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure client secret associated with the \"client id\" (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Number of machines (VMs) in the agent pool. Allowed values must be in the range of 1 to 100 (inclusive). Default `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns<wbr>Service<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An IP address assigned to the Kubernetes DNS service. It must be within the Kubernetes Service address range specified in \"service cidr\". Default `10.0.0.10` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>docker<wbr>Bridge<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range assigned to the Docker bridge network. It must not overlap with any Subnet IP ranges or the Kubernetes Service address range specified in \"service cidr\". Default `172.17.0.1/16` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Http<wbr>Application<wbr>Routing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable the Kubernetes ingress with automatic public DNS name creation. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Turn on Azure Log Analytics monitoring. Uses the Log Analytics \"Default\" workspace if it exists, else creates one. if using an existing workspace, specifies \"log analytics workspace resource id\". Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure Kubernetes cluster location. Default `eastus` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log<wbr>Analytics<wbr>Workspace</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of an existing Azure Log Analytics Workspace to use for storing monitoring data. If not specified, uses '{resource group}-{subscription id}-{location code}' (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log<wbr>Analytics<wbr>Workspace<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource group of an existing Azure Log Analytics Workspace to use for storing monitoring data. If not specified, uses the 'Cluster' resource group (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>master<wbr>Dns<wbr>Prefix</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}DNS prefix to use the Kubernetes cluster control pane (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Pods</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Maximum number of pods that can run on a node. Default `110` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network<wbr>Plugin</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Network plugin used for building Kubernetes network. Chooses from `azure` or `kubenet`. Default `azure` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Network policy used for building Kubernetes network. Chooses from `calico` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pod<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range from which to assign Kubernetes Pod IPs when \"network plugin\" is specified in \"kubenet\". Default `172.244.0.0/16` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Cluster resource group (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A CIDR notation IP range from which to assign Kubernetes Service cluster IPs. It must not overlap with any Subnet IP ranges. Default `10.0.0.0/16` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ssh<wbr>Public<wbr>Key<wbr>Contents</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Contents of the SSH public key used to authenticate with Linux hosts (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>subnet</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of an existing Azure Virtual Subnet. Composite of agent virtual network subnet ID (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>subscription<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Subscription credentials which uniquely identify Microsoft Azure subscription (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Tags for Kubernetes cluster. For example, foo=bar (map)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>tenant_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>virtual<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the virtual network to use. If it's not specified Rancher will create a new VPC (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>virtual<wbr>Network<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource group of an existing Azure Virtual Network. Composite of agent virtual network subnet ID (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Cluster<wbr>Auth<wbr>Endpoint</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterClusterAuthEndpoint">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterClusterAuthEndpoint">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterClusterAuthEndpointArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterClusterAuthEndpointOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ca<wbr>Certs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}CA certs for the authorized cluster endpoint (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}FQDN for the authorized cluster endpoint (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ca<wbr>Certs</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}CA certs for the authorized cluster endpoint (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}FQDN for the authorized cluster endpoint (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ca<wbr>Certs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}CA certs for the authorized cluster endpoint (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}FQDN for the authorized cluster endpoint (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ca_<wbr>certs</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}CA certs for the authorized cluster endpoint (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fqdn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}FQDN for the authorized cluster endpoint (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Cluster<wbr>Monitoring<wbr>Input</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterClusterMonitoringInput">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterClusterMonitoringInput">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterClusterMonitoringInputArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterClusterMonitoringInputOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Key/value answers for monitor input (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Answers</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Key/value answers for monitor input (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>answers</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Key/value answers for monitor input (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>answers</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Key/value answers for monitor input (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Cluster<wbr>Registration<wbr>Token</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterClusterRegistrationToken">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterClusterRegistrationTokenOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Command to execute in a imported k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) The ID of the resource (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Insecure<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Insecure command to execute in a imported k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Manifest<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}K8s manifest url to execute with `kubectl` to import an existing k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node command to execute in linux nodes for custom k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Token for cluster registration token object (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Windows<wbr>Node<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node command to execute in windows nodes for custom k8s cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Command to execute in a imported k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Computed) The ID of the resource (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Insecure<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Insecure command to execute in a imported k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Manifest<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}K8s manifest url to execute with `kubectl` to import an existing k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Node command to execute in linux nodes for custom k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Token for cluster registration token object (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Windows<wbr>Node<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Node command to execute in windows nodes for custom k8s cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>command</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Command to execute in a imported k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Computed) The ID of the resource (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>insecure<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Insecure command to execute in a imported k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>manifest<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}K8s manifest url to execute with `kubectl` to import an existing k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node command to execute in linux nodes for custom k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Token for cluster registration token object (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>windows<wbr>Node<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node command to execute in windows nodes for custom k8s cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>annotations</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Annotations for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>command</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Command to execute in a imported k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Computed) The ID of the resource (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>insecure<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Insecure command to execute in a imported k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>manifest<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}K8s manifest url to execute with `kubectl` to import an existing k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Node command to execute in linux nodes for custom k8s cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Token for cluster registration token object (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>windows<wbr>Node<wbr>Command</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Node command to execute in windows nodes for custom k8s cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Cluster<wbr>Template<wbr>Answers</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterClusterTemplateAnswers">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterClusterTemplateAnswers">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterClusterTemplateAnswersArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterClusterTemplateAnswersOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Project ID to apply answer (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Key/values for answer (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Project ID to apply answer (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Key/values for answer (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Project ID to apply answer (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Key/values for answer (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cluster_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Project ID to apply answer (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Key/values for answer (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Cluster<wbr>Template<wbr>Question</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterClusterTemplateQuestion">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterClusterTemplateQuestion">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterClusterTemplateQuestionArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterClusterTemplateQuestionOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Default</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Default variable value (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Required variable. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Variable type. `boolean`, `int` and `string` are allowed. Default `string` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Variable</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable name (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Default</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Default variable value (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Required variable. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Variable type. `boolean`, `int` and `string` are allowed. Default `string` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Variable</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable name (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>default</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Default variable value (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Required variable. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Variable type. `boolean`, `int` and `string` are allowed. Default `string` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>variable</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Variable name (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>default</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Default variable value (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Required variable. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Variable type. `boolean`, `int` and `string` are allowed. Default `string` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>variable</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Variable name (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Eks<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterEksConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterEksConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterEksConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterEksConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Access<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS Client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ami</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}AMI ID to use for the worker nodes instead of the default (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Associate<wbr>Worker<wbr>Node<wbr>Public<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Associate public ip EKS worker nodes. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The desired number of worker nodes. Just for Rancher v2.3.x and above. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of machine to use for worker nodes. Default `t2.medium` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Key<wbr>Pair<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Allow user to specify key name to use. Just for Rancher v2.2.7 and above (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Maximum<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum number of worker nodes. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Minimum<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The minimum number of worker nodes. Default `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Volume<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The volume size for each node. Default `20` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Secret<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS Client Secret associated with the Client ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}List of security groups to use for the cluster. If it's not specified Rancher will create a new security group (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Role</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The service role to use to perform the cluster operations in AWS. If it's not specified Rancher will create a new service role (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A session token to use with the client key and secret if applicable (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}List of subnets in the virtual network to use. If it's not specified Rancher will create 3 news subnets (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Data</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Pass user-data to the nodes to perform automated configuration tasks (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Virtual<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the virtual network to use. If it's not specified Rancher will create a new VPC (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Access<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS Client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ami</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}AMI ID to use for the worker nodes instead of the default (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Associate<wbr>Worker<wbr>Node<wbr>Public<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Associate public ip EKS worker nodes. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Desired<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The desired number of worker nodes. Just for Rancher v2.3.x and above. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The type of machine to use for worker nodes. Default `t2.medium` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Key<wbr>Pair<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Allow user to specify key name to use. Just for Rancher v2.2.7 and above (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Maximum<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum number of worker nodes. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Minimum<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The minimum number of worker nodes. Default `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Volume<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The volume size for each node. Default `20` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Secret<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS Client Secret associated with the Client ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of security groups to use for the cluster. If it's not specified Rancher will create a new security group (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Role</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The service role to use to perform the cluster operations in AWS. If it's not specified Rancher will create a new service role (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A session token to use with the client key and secret if applicable (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of subnets in the virtual network to use. If it's not specified Rancher will create 3 news subnets (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Data</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Pass user-data to the nodes to perform automated configuration tasks (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Virtual<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the virtual network to use. If it's not specified Rancher will create a new VPC (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>access<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS Client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ami</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}AMI ID to use for the worker nodes instead of the default (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>associate<wbr>Worker<wbr>Node<wbr>Public<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Associate public ip EKS worker nodes. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The desired number of worker nodes. Just for Rancher v2.3.x and above. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of machine to use for worker nodes. Default `t2.medium` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>key<wbr>Pair<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Allow user to specify key name to use. Just for Rancher v2.2.7 and above (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>maximum<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum number of worker nodes. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>minimum<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The minimum number of worker nodes. Default `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Volume<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The volume size for each node. Default `20` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>secret<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS Client Secret associated with the Client ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}List of security groups to use for the cluster. If it's not specified Rancher will create a new security group (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Role</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The service role to use to perform the cluster operations in AWS. If it's not specified Rancher will create a new service role (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A session token to use with the client key and secret if applicable (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}List of subnets in the virtual network to use. If it's not specified Rancher will create 3 news subnets (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Data</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Pass user-data to the nodes to perform automated configuration tasks (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>virtual<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the virtual network to use. If it's not specified Rancher will create a new VPC (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>access_<wbr>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS Client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ami</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}AMI ID to use for the worker nodes instead of the default (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>associate<wbr>Worker<wbr>Node<wbr>Public<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Associate public ip EKS worker nodes. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>desired<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The desired number of worker nodes. Just for Rancher v2.3.x and above. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of machine to use for worker nodes. Default `t2.medium` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>key<wbr>Pair<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Allow user to specify key name to use. Just for Rancher v2.2.7 and above (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>maximum<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum number of worker nodes. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>minimum<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum number of worker nodes. Default `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Volume<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The volume size for each node. Default `20` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>secret_<wbr>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS Client Secret associated with the Client ID (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of security groups to use for the cluster. If it's not specified Rancher will create a new security group (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Role</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The service role to use to perform the cluster operations in AWS. If it's not specified Rancher will create a new service role (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A session token to use with the client key and secret if applicable (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>subnets</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of subnets in the virtual network to use. If it's not specified Rancher will create 3 news subnets (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Data</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Pass user-data to the nodes to perform automated configuration tasks (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>virtual<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the virtual network to use. If it's not specified Rancher will create a new VPC (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Gke<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterGkeConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterGkeConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterGkeConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterGkeConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Cluster<wbr>Ipv4Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range of the container pods (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Credential</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The contents of the GC credential file (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Size<wbr>Gb</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Size of the disk attached to each node. Default `100` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Type of the disk attached to each node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Alpha<wbr>Feature</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}To enable Kubernetes alpha feature. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Auto<wbr>Repair</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Specifies whether the node auto-repair is enabled for the node pool. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Auto<wbr>Upgrade</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Specifies whether node auto-upgrade is enabled for the node pool. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Horizontal<wbr>Pod<wbr>Autoscaling</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable horizontal pod autoscaling for the cluster. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Http<wbr>Load<wbr>Balancing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable HTTP load balancing on GKE cluster. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Kubernetes<wbr>Dashboard</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to enable the Kubernetes dashboard. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Legacy<wbr>Abac</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to enable legacy abac on the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Master<wbr>Authorized<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Network<wbr>Policy<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver logging. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Nodepool<wbr>Autoscaling</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable nodepool autoscaling. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Private<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether the master's internal IP address is used as the cluster endpoint. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Private<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether nodes have internal IP address only. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Stackdriver<wbr>Logging</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver monitoring. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Stackdriver<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver monitoring on GKE cluster (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Image<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The image to use for the worker nodes (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Cluster<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range for the cluster pod IPs (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Cluster<wbr>Secondary<wbr>Range<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the secondary range to be used for the cluster CIDR block (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ip<wbr>Policy<wbr>Create<wbr>Subnetwork</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether a new subnetwork will be created automatically for the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Node<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range of the instance IPs in this cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Services<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range of the services IPs in this cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Services<wbr>Secondary<wbr>Range<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the secondary range to be used for the services CIDR block (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Subnetwork<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A custom subnetwork name to be used if createSubnetwork is true (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Issue<wbr>Client<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Issue a client certificate. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubernetes<wbr>Dashboard</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable the Kubernetes dashboard. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Local<wbr>Ssd<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The number of local SSD disks to be attached to the node. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Locations</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}Locations for GKE cluster (list)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Machine<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Machine type for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Maintenance<wbr>Window</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Maintenance window for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master<wbr>Authorized<wbr>Network<wbr>Cidr<wbr>Blocks</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Define up to 10 external networks that could access Kubernetes master through HTTPS (list)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Master<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP range in CIDR notation to use for the hosted master network (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Master<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Master version for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Maximum number of nodes in the NodePool. Must be >= minNodeCount. There has to enough quota to scale up the cluster. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Minimmum number of nodes in the NodePool. Must be >= 1 and <= maxNodeCount. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Node count for GKE cluster. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Node<wbr>Pool</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the cluster node pool (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Node<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Node version for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Oauth<wbr>Scopes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The set of Google API scopes to be made available on all of the node VMs under the default service account (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Preemptible</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether the nodes are created as preemptible VM instances. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Project ID to apply answer (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}The map of Kubernetes labels to be applied to each cluster (map)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Service<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Google Cloud Platform Service Account to be used by the node VMs (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Sub<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subnetwork for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Taints</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}List of Kubernetes taints to be applied to each node (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Ip<wbr>Aliases</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether alias IPs will be used for pod IPs in the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Zone GKE cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Cluster<wbr>Ipv4Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range of the container pods (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Credential</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The contents of the GC credential file (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disk<wbr>Size<wbr>Gb</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Size of the disk attached to each node. Default `100` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Type of the disk attached to each node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Alpha<wbr>Feature</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}To enable Kubernetes alpha feature. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Auto<wbr>Repair</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the node auto-repair is enabled for the node pool. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Auto<wbr>Upgrade</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether node auto-upgrade is enabled for the node pool. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Horizontal<wbr>Pod<wbr>Autoscaling</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable horizontal pod autoscaling for the cluster. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Http<wbr>Load<wbr>Balancing</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable HTTP load balancing on GKE cluster. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Kubernetes<wbr>Dashboard</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable the Kubernetes dashboard. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Legacy<wbr>Abac</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable legacy abac on the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Master<wbr>Authorized<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Network<wbr>Policy<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver logging. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Nodepool<wbr>Autoscaling</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable nodepool autoscaling. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Private<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether the master's internal IP address is used as the cluster endpoint. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Private<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether nodes have internal IP address only. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Stackdriver<wbr>Logging</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver monitoring. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enable<wbr>Stackdriver<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver monitoring on GKE cluster (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Image<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The image to use for the worker nodes (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Cluster<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range for the cluster pod IPs (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Cluster<wbr>Secondary<wbr>Range<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the secondary range to be used for the cluster CIDR block (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ip<wbr>Policy<wbr>Create<wbr>Subnetwork</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether a new subnetwork will be created automatically for the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Node<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range of the instance IPs in this cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Services<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range of the services IPs in this cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Services<wbr>Secondary<wbr>Range<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the secondary range to be used for the services CIDR block (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Policy<wbr>Subnetwork<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A custom subnetwork name to be used if createSubnetwork is true (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Issue<wbr>Client<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Issue a client certificate. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubernetes<wbr>Dashboard</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable the Kubernetes dashboard. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Local<wbr>Ssd<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The number of local SSD disks to be attached to the node. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Locations</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Locations for GKE cluster (list)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Machine<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Machine type for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Maintenance<wbr>Window</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Maintenance window for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master<wbr>Authorized<wbr>Network<wbr>Cidr<wbr>Blocks</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Define up to 10 external networks that could access Kubernetes master through HTTPS (list)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Master<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP range in CIDR notation to use for the hosted master network (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Master<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Master version for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Maximum number of nodes in the NodePool. Must be >= minNodeCount. There has to enough quota to scale up the cluster. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Minimmum number of nodes in the NodePool. Must be >= 1 and <= maxNodeCount. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Node count for GKE cluster. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Node<wbr>Pool</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the cluster node pool (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Node<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Node version for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Oauth<wbr>Scopes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The set of Google API scopes to be made available on all of the node VMs under the default service account (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Preemptible</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether the nodes are created as preemptible VM instances. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Project ID to apply answer (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}The map of Kubernetes labels to be applied to each cluster (map)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Service<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Google Cloud Platform Service Account to be used by the node VMs (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Sub<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subnetwork for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Taints</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of Kubernetes taints to be applied to each node (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Ip<wbr>Aliases</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether alias IPs will be used for pod IPs in the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Zone GKE cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>cluster<wbr>Ipv4Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range of the container pods (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>credential</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The contents of the GC credential file (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk<wbr>Size<wbr>Gb</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Size of the disk attached to each node. Default `100` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Type of the disk attached to each node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Alpha<wbr>Feature</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}To enable Kubernetes alpha feature. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Auto<wbr>Repair</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Specifies whether the node auto-repair is enabled for the node pool. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Auto<wbr>Upgrade</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Specifies whether node auto-upgrade is enabled for the node pool. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Horizontal<wbr>Pod<wbr>Autoscaling</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable horizontal pod autoscaling for the cluster. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Http<wbr>Load<wbr>Balancing</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable HTTP load balancing on GKE cluster. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Kubernetes<wbr>Dashboard</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to enable the Kubernetes dashboard. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Legacy<wbr>Abac</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to enable legacy abac on the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Master<wbr>Authorized<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Network<wbr>Policy<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver logging. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Nodepool<wbr>Autoscaling</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable nodepool autoscaling. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Private<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether the master's internal IP address is used as the cluster endpoint. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Private<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether nodes have internal IP address only. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Stackdriver<wbr>Logging</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver monitoring. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Stackdriver<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver monitoring on GKE cluster (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>image<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The image to use for the worker nodes (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Cluster<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range for the cluster pod IPs (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Cluster<wbr>Secondary<wbr>Range<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the secondary range to be used for the cluster CIDR block (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ip<wbr>Policy<wbr>Create<wbr>Subnetwork</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether a new subnetwork will be created automatically for the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Node<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range of the instance IPs in this cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Services<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP address range of the services IPs in this cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Services<wbr>Secondary<wbr>Range<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the secondary range to be used for the services CIDR block (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Subnetwork<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A custom subnetwork name to be used if createSubnetwork is true (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>issue<wbr>Client<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Issue a client certificate. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubernetes<wbr>Dashboard</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable the Kubernetes dashboard. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>local<wbr>Ssd<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The number of local SSD disks to be attached to the node. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>locations</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Locations for GKE cluster (list)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>machine<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Machine type for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>maintenance<wbr>Window</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Maintenance window for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master<wbr>Authorized<wbr>Network<wbr>Cidr<wbr>Blocks</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Define up to 10 external networks that could access Kubernetes master through HTTPS (list)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>master<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The IP range in CIDR notation to use for the hosted master network (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>master<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Master version for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Maximum number of nodes in the NodePool. Must be >= minNodeCount. There has to enough quota to scale up the cluster. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Minimmum number of nodes in the NodePool. Must be >= 1 and <= maxNodeCount. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Node count for GKE cluster. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>node<wbr>Pool</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the cluster node pool (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>node<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Node version for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>oauth<wbr>Scopes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The set of Google API scopes to be made available on all of the node VMs under the default service account (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>preemptible</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether the nodes are created as preemptible VM instances. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Project ID to apply answer (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource<wbr>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}The map of Kubernetes labels to be applied to each cluster (map)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>service<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Google Cloud Platform Service Account to be used by the node VMs (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>sub<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subnetwork for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>taints</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}List of Kubernetes taints to be applied to each node (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Ip<wbr>Aliases</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether alias IPs will be used for pod IPs in the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Zone GKE cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>cluster<wbr>Ipv4Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP address range of the container pods (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>credential</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The contents of the GC credential file (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An optional description of this cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disk<wbr>Size<wbr>Gb</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Size of the disk attached to each node. Default `100` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>disk<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Type of the disk attached to each node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Alpha<wbr>Feature</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}To enable Kubernetes alpha feature. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Auto<wbr>Repair</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the node auto-repair is enabled for the node pool. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Auto<wbr>Upgrade</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether node auto-upgrade is enabled for the node pool. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Horizontal<wbr>Pod<wbr>Autoscaling</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable horizontal pod autoscaling for the cluster. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Http<wbr>Load<wbr>Balancing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable HTTP load balancing on GKE cluster. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Kubernetes<wbr>Dashboard</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable the Kubernetes dashboard. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Legacy<wbr>Abac</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to enable legacy abac on the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Master<wbr>Authorized<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Network<wbr>Policy<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver logging. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Nodepool<wbr>Autoscaling</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable nodepool autoscaling. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Private<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the master's internal IP address is used as the cluster endpoint. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Private<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether nodes have internal IP address only. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Stackdriver<wbr>Logging</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver monitoring. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enable<wbr>Stackdriver<wbr>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable stackdriver monitoring on GKE cluster (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>image<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The image to use for the worker nodes (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Cluster<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP address range for the cluster pod IPs (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Cluster<wbr>Secondary<wbr>Range<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the secondary range to be used for the cluster CIDR block (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ip<wbr>Policy<wbr>Create<wbr>Subnetwork</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether a new subnetwork will be created automatically for the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Node<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP address range of the instance IPs in this cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Services<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP address range of the services IPs in this cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Services<wbr>Secondary<wbr>Range<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the secondary range to be used for the services CIDR block (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Policy<wbr>Subnetwork<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A custom subnetwork name to be used if createSubnetwork is true (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>issue<wbr>Client<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Issue a client certificate. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubernetes<wbr>Dashboard</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable the Kubernetes dashboard. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>local<wbr>Ssd<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of local SSD disks to be attached to the node. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>locations</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Locations for GKE cluster (list)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>machine<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Machine type for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>maintenance<wbr>Window</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Maintenance window for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master<wbr>Authorized<wbr>Network<wbr>Cidr<wbr>Blocks</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Define up to 10 external networks that could access Kubernetes master through HTTPS (list)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>master<wbr>Ipv4Cidr<wbr>Block</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IP range in CIDR notation to use for the hosted master network (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>master<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Master version for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Maximum number of nodes in the NodePool. Must be >= minNodeCount. There has to enough quota to scale up the cluster. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Minimmum number of nodes in the NodePool. Must be >= 1 and <= maxNodeCount. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Node count for GKE cluster. Default `3` (int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>node<wbr>Pool</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the cluster node pool (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>node<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Node version for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>oauth<wbr>Scopes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The set of Google API scopes to be made available on all of the node VMs under the default service account (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>preemptible</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the nodes are created as preemptible VM instances. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Project ID to apply answer (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource<wbr>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The map of Kubernetes labels to be applied to each cluster (map)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>service<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Google Cloud Platform Service Account to be used by the node VMs (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>sub<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Subnetwork for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>taints</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of Kubernetes taints to be applied to each node (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Ip<wbr>Aliases</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether alias IPs will be used for pod IPs in the cluster. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Zone GKE cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>K3s<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterK3sConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterK3sConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterK3sConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterK3sConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Upgrade<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfigupgradestrategy">Cluster<wbr>K3s<wbr>Config<wbr>Upgrade<wbr>Strategy<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}K3S upgrade strategy (List maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}K3S kubernetes version (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Upgrade<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfigupgradestrategy">*Cluster<wbr>K3s<wbr>Config<wbr>Upgrade<wbr>Strategy</a></span>
    </dt>
    <dd>{{% md %}}K3S upgrade strategy (List maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}K3S kubernetes version (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>upgrade<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfigupgradestrategy">Cluster<wbr>K3s<wbr>Config<wbr>Upgrade<wbr>Strategy?</a></span>
    </dt>
    <dd>{{% md %}}K3S upgrade strategy (List maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}K3S kubernetes version (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>upgrade_<wbr>strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterk3sconfigupgradestrategy">Dict[Cluster<wbr>K3s<wbr>Config<wbr>Upgrade<wbr>Strategy]</a></span>
    </dt>
    <dd>{{% md %}}K3S upgrade strategy (List maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}K3S kubernetes version (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>K3s<wbr>Config<wbr>Upgrade<wbr>Strategy</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterK3sConfigUpgradeStrategy">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterK3sConfigUpgradeStrategy">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterK3sConfigUpgradeStrategyArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterK3sConfigUpgradeStrategyOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Server<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Drain server nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Worker<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Drain worker nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Server<wbr>Concurrency</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Server concurrency. Default: `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Worker<wbr>Concurrency</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Worker concurrency. Default: `1` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Server<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Drain server nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Worker<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Drain worker nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Server<wbr>Concurrency</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Server concurrency. Default: `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Worker<wbr>Concurrency</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Worker concurrency. Default: `1` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>drain<wbr>Server<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Drain server nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>drain<wbr>Worker<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Drain worker nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>server<wbr>Concurrency</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Server concurrency. Default: `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>worker<wbr>Concurrency</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Worker concurrency. Default: `1` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>drain<wbr>Server<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Drain server nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>drain<wbr>Worker<wbr>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Drain worker nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>server<wbr>Concurrency</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Server concurrency. Default: `1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>worker<wbr>Concurrency</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Worker concurrency. Default: `1` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Addon<wbr>Job<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Duration in seconds of addon job (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Addons</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Addons descripton to deploy on RKE cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Addons<wbr>Includes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Addons yaml manifests to deploy on RKE cluster (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigauthentication">Cluster<wbr>Rke<wbr>Config<wbr>Authentication<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster authentication (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorization</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigauthorization">Cluster<wbr>Rke<wbr>Config<wbr>Authorization<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster authorization (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Bastion<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigbastionhost">Cluster<wbr>Rke<wbr>Config<wbr>Bastion<wbr>Host<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}RKE bastion host (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}RKE options for Calico network provider (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigdns">Cluster<wbr>Rke<wbr>Config<wbr>Dns<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}RKE dns add-on. Just for Rancher v2.2.x (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ignore<wbr>Docker<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Ignore docker version. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ingress</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigingress">Cluster<wbr>Rke<wbr>Config<wbr>Ingress<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes ingress configuration (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigmonitoring">Cluster<wbr>Rke<wbr>Config<wbr>Monitoring<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster monitoring (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetwork">Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignode">List&lt;Cluster<wbr>Rke<wbr>Config<wbr>Node<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}RKE cluster nodes (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Prefix<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Prefix to customize Kubernetes path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Private<wbr>Registries</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigprivateregistry">List&lt;Cluster<wbr>Rke<wbr>Config<wbr>Private<wbr>Registry<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}private registries for docker images (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Services</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservices">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Cert<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster level SSH certificate path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Upgrade<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigupgradestrategy">Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}K3S upgrade strategy (List maxitems: 1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Addon<wbr>Job<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Duration in seconds of addon job (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Addons</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Addons descripton to deploy on RKE cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Addons<wbr>Includes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Addons yaml manifests to deploy on RKE cluster (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigauthentication">*Cluster<wbr>Rke<wbr>Config<wbr>Authentication</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster authentication (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorization</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigauthorization">*Cluster<wbr>Rke<wbr>Config<wbr>Authorization</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster authorization (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Bastion<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigbastionhost">*Cluster<wbr>Rke<wbr>Config<wbr>Bastion<wbr>Host</a></span>
    </dt>
    <dd>{{% md %}}RKE bastion host (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovider">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider</a></span>
    </dt>
    <dd>{{% md %}}RKE options for Calico network provider (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigdns">*Cluster<wbr>Rke<wbr>Config<wbr>Dns</a></span>
    </dt>
    <dd>{{% md %}}RKE dns add-on. Just for Rancher v2.2.x (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ignore<wbr>Docker<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Ignore docker version. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ingress</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigingress">*Cluster<wbr>Rke<wbr>Config<wbr>Ingress</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes ingress configuration (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigmonitoring">*Cluster<wbr>Rke<wbr>Config<wbr>Monitoring</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster monitoring (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetwork">*Cluster<wbr>Rke<wbr>Config<wbr>Network</a></span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignode">[]Cluster<wbr>Rke<wbr>Config<wbr>Node</a></span>
    </dt>
    <dd>{{% md %}}RKE cluster nodes (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Prefix<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Prefix to customize Kubernetes path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Private<wbr>Registries</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigprivateregistry">[]Cluster<wbr>Rke<wbr>Config<wbr>Private<wbr>Registry</a></span>
    </dt>
    <dd>{{% md %}}private registries for docker images (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Services</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservices">*Cluster<wbr>Rke<wbr>Config<wbr>Services</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Cert<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster level SSH certificate path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Upgrade<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigupgradestrategy">*Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy</a></span>
    </dt>
    <dd>{{% md %}}K3S upgrade strategy (List maxitems: 1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>addon<wbr>Job<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Duration in seconds of addon job (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>addons</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Addons descripton to deploy on RKE cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>addons<wbr>Includes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Addons yaml manifests to deploy on RKE cluster (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigauthentication">Cluster<wbr>Rke<wbr>Config<wbr>Authentication?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster authentication (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorization</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigauthorization">Cluster<wbr>Rke<wbr>Config<wbr>Authorization?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster authorization (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>bastion<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigbastionhost">Cluster<wbr>Rke<wbr>Config<wbr>Bastion<wbr>Host?</a></span>
    </dt>
    <dd>{{% md %}}RKE bastion host (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider?</a></span>
    </dt>
    <dd>{{% md %}}RKE options for Calico network provider (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigdns">Cluster<wbr>Rke<wbr>Config<wbr>Dns?</a></span>
    </dt>
    <dd>{{% md %}}RKE dns add-on. Just for Rancher v2.2.x (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ignore<wbr>Docker<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Ignore docker version. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ingress</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigingress">Cluster<wbr>Rke<wbr>Config<wbr>Ingress?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes ingress configuration (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigmonitoring">Cluster<wbr>Rke<wbr>Config<wbr>Monitoring?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster monitoring (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetwork">Cluster<wbr>Rke<wbr>Config<wbr>Network?</a></span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignode">Cluster<wbr>Rke<wbr>Config<wbr>Node[]?</a></span>
    </dt>
    <dd>{{% md %}}RKE cluster nodes (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>prefix<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Prefix to customize Kubernetes path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>private<wbr>Registries</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigprivateregistry">Cluster<wbr>Rke<wbr>Config<wbr>Private<wbr>Registry[]?</a></span>
    </dt>
    <dd>{{% md %}}private registries for docker images (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>services</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservices">Cluster<wbr>Rke<wbr>Config<wbr>Services?</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Cert<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster level SSH certificate path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>upgrade<wbr>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigupgradestrategy">Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy?</a></span>
    </dt>
    <dd>{{% md %}}K3S upgrade strategy (List maxitems: 1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>addon<wbr>Job<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Duration in seconds of addon job (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>addons</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Addons descripton to deploy on RKE cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>addons<wbr>Includes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Addons yaml manifests to deploy on RKE cluster (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigauthentication">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Authentication]</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster authentication (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorization</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigauthorization">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Authorization]</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster authorization (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>bastion<wbr>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigbastionhost">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Bastion<wbr>Host]</a></span>
    </dt>
    <dd>{{% md %}}RKE bastion host (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovider">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider]</a></span>
    </dt>
    <dd>{{% md %}}RKE options for Calico network provider (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigdns">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Dns]</a></span>
    </dt>
    <dd>{{% md %}}RKE dns add-on. Just for Rancher v2.2.x (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ignore<wbr>Docker<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Ignore docker version. Default `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ingress</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigingress">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Ingress]</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes ingress configuration (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubernetes<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Kubernetes master version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitoring</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigmonitoring">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Monitoring]</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster monitoring (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetwork">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Network]</a></span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>nodes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignode">List[Cluster<wbr>Rke<wbr>Config<wbr>Node]</a></span>
    </dt>
    <dd>{{% md %}}RKE cluster nodes (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>prefix<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Prefix to customize Kubernetes path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>private<wbr>Registries</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigprivateregistry">List[Cluster<wbr>Rke<wbr>Config<wbr>Private<wbr>Registry]</a></span>
    </dt>
    <dd>{{% md %}}private registries for docker images (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>services</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservices">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services]</a></span>
    </dt>
    <dd>{{% md %}}Kubernetes cluster services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Cert<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster level SSH certificate path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>upgrade_<wbr>strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigupgradestrategy">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy]</a></span>
    </dt>
    <dd>{{% md %}}K3S upgrade strategy (List maxitems: 1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Authentication</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigAuthentication">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigAuthentication">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigAuthenticationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigAuthenticationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Sans</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}RKE sans for authentication ([]string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE strategy for authentication (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Sans</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}RKE sans for authentication ([]string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}RKE strategy for authentication (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>sans</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}RKE sans for authentication ([]string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE strategy for authentication (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>sans</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}RKE sans for authentication ([]string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strategy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}RKE strategy for authentication (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Authorization</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigAuthorization">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigAuthorization">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigAuthorizationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigAuthorizationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE mode for authorization. `rbac` and `none` modes are available. Default `rbac` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}RKE mode for authorization. `rbac` and `none` modes are available. Default `rbac` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE mode for authorization. `rbac` and `none` modes are available. Default `rbac` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}RKE mode for authorization. `rbac` and `none` modes are available. Default `rbac` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Bastion<wbr>Host</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigBastionHost">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigBastionHost">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigBastionHostArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigBastionHostOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Address ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
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
    <dd>{{% md %}}Address ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Node SSH private key (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
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
    <dd>{{% md %}}Address ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
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
    <dd>{{% md %}}Address ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Node SSH private key (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProvider">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProvider">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aws<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}RKE AWS Cloud Provider config for Cloud Provider [rke-aws-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/aws/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Azure<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderazurecloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Azure<wbr>Cloud<wbr>Provider<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}RKE Azure Cloud Provider config for Cloud Provider [rke-azure-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/azure/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE Custom Cloud Provider config for Cloud Provider (string) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Openstack<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}RKE Openstack Cloud Provider config for Cloud Provider [rke-openstack-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/openstack/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vsphere<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}RKE Vsphere Cloud Provider config for Cloud Provider [rke-vsphere-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/vsphere/) Extra argument `name` is required on `virtual_center` configuration. (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aws<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudprovider">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider</a></span>
    </dt>
    <dd>{{% md %}}RKE AWS Cloud Provider config for Cloud Provider [rke-aws-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/aws/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Azure<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderazurecloudprovider">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Azure<wbr>Cloud<wbr>Provider</a></span>
    </dt>
    <dd>{{% md %}}RKE Azure Cloud Provider config for Cloud Provider [rke-azure-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/azure/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}RKE Custom Cloud Provider config for Cloud Provider (string) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Openstack<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudprovider">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider</a></span>
    </dt>
    <dd>{{% md %}}RKE Openstack Cloud Provider config for Cloud Provider [rke-openstack-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/openstack/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vsphere<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovider">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider</a></span>
    </dt>
    <dd>{{% md %}}RKE Vsphere Cloud Provider config for Cloud Provider [rke-vsphere-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/vsphere/) Extra argument `name` is required on `virtual_center` configuration. (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aws<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider?</a></span>
    </dt>
    <dd>{{% md %}}RKE AWS Cloud Provider config for Cloud Provider [rke-aws-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/aws/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>azure<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderazurecloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Azure<wbr>Cloud<wbr>Provider?</a></span>
    </dt>
    <dd>{{% md %}}RKE Azure Cloud Provider config for Cloud Provider [rke-azure-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/azure/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE Custom Cloud Provider config for Cloud Provider (string) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>openstack<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider?</a></span>
    </dt>
    <dd>{{% md %}}RKE Openstack Cloud Provider config for Cloud Provider [rke-openstack-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/openstack/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vsphere<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovider">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider?</a></span>
    </dt>
    <dd>{{% md %}}RKE Vsphere Cloud Provider config for Cloud Provider [rke-vsphere-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/vsphere/) Extra argument `name` is required on `virtual_center` configuration. (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aws<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudprovider">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider]</a></span>
    </dt>
    <dd>{{% md %}}RKE AWS Cloud Provider config for Cloud Provider [rke-aws-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/aws/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>azure<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderazurecloudprovider">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Azure<wbr>Cloud<wbr>Provider]</a></span>
    </dt>
    <dd>{{% md %}}RKE Azure Cloud Provider config for Cloud Provider [rke-azure-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/azure/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}RKE Custom Cloud Provider config for Cloud Provider (string) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>openstack<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudprovider">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider]</a></span>
    </dt>
    <dd>{{% md %}}RKE Openstack Cloud Provider config for Cloud Provider [rke-openstack-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/openstack/) (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vsphere<wbr>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovider">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider]</a></span>
    </dt>
    <dd>{{% md %}}RKE Vsphere Cloud Provider config for Cloud Provider [rke-vsphere-cloud-provider](https://rancher.com/docs/rke/latest/en/config-options/cloud-providers/vsphere/) Extra argument `name` is required on `virtual_center` configuration. (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderAwsCloudProvider">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderAwsCloudProvider">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderAwsCloudProviderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderAwsCloudProviderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudproviderglobal">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Global<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Overrides</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudproviderserviceoverride">List&lt;Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Service<wbr>Override<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}(list)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudproviderglobal">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Global</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Overrides</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudproviderserviceoverride">[]Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Service<wbr>Override</a></span>
    </dt>
    <dd>{{% md %}}(list)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudproviderglobal">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Global?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Overrides</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudproviderserviceoverride">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Service<wbr>Override[]?</a></span>
    </dt>
    <dd>{{% md %}}(list)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudproviderglobal">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Global]</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Overrides</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudproviderawscloudproviderserviceoverride">List[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Service<wbr>Override]</a></span>
    </dt>
    <dd>{{% md %}}(list)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Global</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderAwsCloudProviderGlobal">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderAwsCloudProviderGlobal">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderAwsCloudProviderGlobalArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderAwsCloudProviderGlobalOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Disable<wbr>Security<wbr>Group<wbr>Ingress</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disable<wbr>Strict<wbr>Zone<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Elb<wbr>Security<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubernetes<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubernetes<wbr>Cluster<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Route<wbr>Table<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpc</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Zone GKE cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Disable<wbr>Security<wbr>Group<wbr>Ingress</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Disable<wbr>Strict<wbr>Zone<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Elb<wbr>Security<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubernetes<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubernetes<wbr>Cluster<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Route<wbr>Table<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vpc</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Zone GKE cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>disable<wbr>Security<wbr>Group<wbr>Ingress</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disable<wbr>Strict<wbr>Zone<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>elb<wbr>Security<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubernetes<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubernetes<wbr>Cluster<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>route<wbr>Table<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpc</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Zone GKE cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>disable<wbr>Security<wbr>Group<wbr>Ingress</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>disable<wbr>Strict<wbr>Zone<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>elb<wbr>Security<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubernetes<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubernetes<wbr>Cluster<wbr>Tag</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>route<wbr>Table<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vpc</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Zone GKE cluster (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Aws<wbr>Cloud<wbr>Provider<wbr>Service<wbr>Override</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderAwsCloudProviderServiceOverride">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderAwsCloudProviderServiceOverride">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderAwsCloudProviderServiceOverrideArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderAwsCloudProviderServiceOverrideOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Service</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Signing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Signing<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Signing<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry URL (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Service</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Signing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Signing<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Signing<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Registry URL (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>service</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>signing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>signing<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>signing<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry URL (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>service</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>signing<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>signing<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>signing<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry URL (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Azure<wbr>Cloud<wbr>Provider</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderAzureCloudProvider">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderAzureCloudProvider">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderAzureCloudProviderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderAzureCloudProviderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aad<wbr>Client<wbr>Cert<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Aad<wbr>Client<wbr>Cert<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Aad<wbr>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Aad<wbr>Client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff<wbr>Duration</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff<wbr>Exponent</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff<wbr>Jitter</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Rate<wbr>Limit</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Rate<wbr>Limit<wbr>Bucket</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Rate<wbr>Limit<wbr>Qps</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Azure Kubernetes cluster location. Default `eastus` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Maximum<wbr>Load<wbr>Balancer<wbr>Rule<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Primary<wbr>Availability<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Primary<wbr>Scale<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the Cluster resource group (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Route<wbr>Table<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Subnet<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Subscription<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subscription credentials which uniquely identify Microsoft Azure subscription (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Instance<wbr>Metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Managed<wbr>Identity<wbr>Extension</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vm<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vnet<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vnet<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aad<wbr>Client<wbr>Cert<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Aad<wbr>Client<wbr>Cert<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Aad<wbr>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Aad<wbr>Client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff<wbr>Duration</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff<wbr>Exponent</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff<wbr>Jitter</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Backoff<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Rate<wbr>Limit</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Rate<wbr>Limit<wbr>Bucket</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider<wbr>Rate<wbr>Limit<wbr>Qps</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Location</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Azure Kubernetes cluster location. Default `eastus` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Maximum<wbr>Load<wbr>Balancer<wbr>Rule<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Primary<wbr>Availability<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Primary<wbr>Scale<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the Cluster resource group (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Route<wbr>Table<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Subnet<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Subscription<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subscription credentials which uniquely identify Microsoft Azure subscription (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Instance<wbr>Metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Managed<wbr>Identity<wbr>Extension</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vm<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vnet<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vnet<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aad<wbr>Client<wbr>Cert<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>aad<wbr>Client<wbr>Cert<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>aad<wbr>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>aad<wbr>Client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff<wbr>Duration</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff<wbr>Exponent</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff<wbr>Jitter</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Rate<wbr>Limit</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Rate<wbr>Limit<wbr>Bucket</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Rate<wbr>Limit<wbr>Qps</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Azure Kubernetes cluster location. Default `eastus` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>maximum<wbr>Load<wbr>Balancer<wbr>Rule<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>primary<wbr>Availability<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>primary<wbr>Scale<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the Cluster resource group (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>route<wbr>Table<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>subnet<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>subscription<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subscription credentials which uniquely identify Microsoft Azure subscription (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Instance<wbr>Metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Managed<wbr>Identity<wbr>Extension</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vm<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vnet<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vnet<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aad<wbr>Client<wbr>Cert<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>aad<wbr>Client<wbr>Cert<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>aad<wbr>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>aad<wbr>Client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff<wbr>Duration</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff<wbr>Exponent</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff<wbr>Jitter</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Backoff<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Rate<wbr>Limit</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Rate<wbr>Limit<wbr>Bucket</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider<wbr>Rate<wbr>Limit<wbr>Qps</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>location</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure Kubernetes cluster location. Default `eastus` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>maximum<wbr>Load<wbr>Balancer<wbr>Rule<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>primary<wbr>Availability<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>primary<wbr>Scale<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Cluster resource group (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>route<wbr>Table<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>subnet<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>subscription<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Subscription credentials which uniquely identify Microsoft Azure subscription (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>tenant_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Instance<wbr>Metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Managed<wbr>Identity<wbr>Extension</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vm<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vnet<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vnet<wbr>Resource<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderOpenstackCloudProvider">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderOpenstackCloudProvider">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Block<wbr>Storage</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderblockstorage">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Block<wbr>Storage<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderglobal">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Global<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderloadbalancer">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Load<wbr>Balancer<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudprovidermetadata">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Metadata<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Route</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderroute">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Route<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Block<wbr>Storage</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderblockstorage">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Block<wbr>Storage</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderglobal">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Global</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderloadbalancer">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Load<wbr>Balancer</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudprovidermetadata">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Metadata</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Route</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderroute">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Route</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>block<wbr>Storage</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderblockstorage">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Block<wbr>Storage?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderglobal">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Global</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderloadbalancer">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Load<wbr>Balancer?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudprovidermetadata">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Metadata?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>route</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderroute">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Route?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>block<wbr>Storage</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderblockstorage">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Block<wbr>Storage]</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderglobal">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Global]</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>load<wbr>Balancer</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderloadbalancer">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Load<wbr>Balancer]</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metadata</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudprovidermetadata">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Metadata]</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>route</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovideropenstackcloudproviderroute">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Route]</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Block<wbr>Storage</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderOpenstackCloudProviderBlockStorage">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderOpenstackCloudProviderBlockStorage">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderBlockStorageArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderBlockStorageOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Bs<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ignore<wbr>Volume<wbr>Az</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Trust<wbr>Device<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Bs<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ignore<wbr>Volume<wbr>Az</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Trust<wbr>Device<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>bs<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ignore<wbr>Volume<wbr>Az</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>trust<wbr>Device<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>bs<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ignore<wbr>Volume<wbr>Az</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>trust<wbr>Device<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Global</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderOpenstackCloudProviderGlobal">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderOpenstackCloudProviderGlobal">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderGlobalArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderGlobalOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Auth<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ca<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Domain<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Required if `domain_name` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Domain<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Required if `domain_id` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tenant<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Required if `tenant_id` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Trust<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Auth<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ca<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Domain<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Required if `domain_name` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Domain<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Required if `domain_id` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tenant<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Required if `tenant_id` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Trust<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>auth<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ca<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>domain<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Required if `domain_name` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>domain<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Required if `domain_id` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tenant<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Required if `tenant_id` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>trust<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>auth<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ca<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>domain<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Required if `domain_name` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>domain<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Required if `domain_id` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tenant_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure tenant ID to use (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tenant<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Required if `tenant_id` not provided. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>trust<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>username</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Load<wbr>Balancer</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderOpenstackCloudProviderLoadBalancer">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderOpenstackCloudProviderLoadBalancer">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderLoadBalancerArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderLoadBalancerOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Create<wbr>Monitor</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Floating<wbr>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lb<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lb<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lb<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Manage<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitor<wbr>Delay</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Default `60s` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitor<wbr>Max<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Default 5 (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitor<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Default `30s` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Octavia</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Create<wbr>Monitor</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Floating<wbr>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lb<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lb<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lb<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Manage<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitor<wbr>Delay</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Default `60s` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitor<wbr>Max<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Default 5 (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Monitor<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Default `30s` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Use<wbr>Octavia</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>create<wbr>Monitor</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>floating<wbr>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lb<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lb<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lb<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>manage<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitor<wbr>Delay</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Default `60s` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitor<wbr>Max<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Default 5 (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitor<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Default `30s` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Octavia</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>create<wbr>Monitor</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>floating<wbr>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lb<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lb<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lb<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>manage<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitor<wbr>Delay</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Default `60s` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitor<wbr>Max<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Default 5 (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>monitor<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Default `30s` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>use<wbr>Octavia</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Metadata</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderOpenstackCloudProviderMetadata">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderOpenstackCloudProviderMetadata">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderMetadataArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderMetadataOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Request<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Search<wbr>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Request<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Search<wbr>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>request<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>search<wbr>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>request<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>search<wbr>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Openstack<wbr>Cloud<wbr>Provider<wbr>Route</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderOpenstackCloudProviderRoute">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderOpenstackCloudProviderRoute">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderRouteArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderOpenstackCloudProviderRouteOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Router<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Router<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>router<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>router<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderVsphereCloudProvider">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderVsphereCloudProvider">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Disk</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderdisk">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Disk<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderglobal">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Global<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovidernetwork">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Network<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Virtual<wbr>Centers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovidervirtualcenter">List&lt;Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Virtual<wbr>Center<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}(List)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Workspace</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderworkspace">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Workspace<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Disk</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderdisk">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Disk</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderglobal">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Global</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovidernetwork">*Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Network</a></span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Virtual<wbr>Centers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovidervirtualcenter">[]Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Virtual<wbr>Center</a></span>
    </dt>
    <dd>{{% md %}}(List)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Workspace</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderworkspace">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Workspace</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>disk</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderdisk">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Disk?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderglobal">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Global?</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovidernetwork">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Network?</a></span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>virtual<wbr>Centers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovidervirtualcenter">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Virtual<wbr>Center[]</a></span>
    </dt>
    <dd>{{% md %}}(List)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>workspace</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderworkspace">Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Workspace</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>disk</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderdisk">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Disk]</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>global</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderglobal">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Global]</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovidernetwork">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Network]</a></span>
    </dt>
    <dd>{{% md %}}Network for GKE cluster (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>virtual<wbr>Centers</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudprovidervirtualcenter">List[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Virtual<wbr>Center]</a></span>
    </dt>
    <dd>{{% md %}}(List)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>workspace</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigcloudprovidervspherecloudproviderworkspace">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Workspace]</a></span>
    </dt>
    <dd>{{% md %}}(list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Disk</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderVsphereCloudProviderDisk">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderVsphereCloudProviderDisk">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderDiskArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderDiskOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Scsi<wbr>Controller<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Scsi<wbr>Controller<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>scsi<wbr>Controller<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>scsi<wbr>Controller<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Global</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderVsphereCloudProviderGlobal">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderVsphereCloudProviderGlobal">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderGlobalArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderGlobalOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Datacenters</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Insecure<wbr>Flag</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Soap<wbr>Roundtrip<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Datacenters</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Insecure<wbr>Flag</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Soap<wbr>Roundtrip<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>datacenters</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>insecure<wbr>Flag</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>soap<wbr>Roundtrip<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>datacenters</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>insecure<wbr>Flag</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}(bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>soap<wbr>Roundtrip<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Network</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderVsphereCloudProviderNetwork">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderVsphereCloudProviderNetwork">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderNetworkArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderNetworkOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Public<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Public<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>public<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>public<wbr>Network</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Virtual<wbr>Center</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderVsphereCloudProviderVirtualCenter">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderVsphereCloudProviderVirtualCenter">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderVirtualCenterArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderVirtualCenterOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Datacenters</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Soap<wbr>Roundtrip<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Datacenters</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Soap<wbr>Roundtrip<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>datacenters</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>soap<wbr>Roundtrip<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>datacenters</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of cluster registration token (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>soap<wbr>Roundtrip<wbr>Count</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}(int)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Cloud<wbr>Provider<wbr>Vsphere<wbr>Cloud<wbr>Provider<wbr>Workspace</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigCloudProviderVsphereCloudProviderWorkspace">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigCloudProviderVsphereCloudProviderWorkspace">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderWorkspaceArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigCloudProviderVsphereCloudProviderWorkspaceOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Datastore</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Folder</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Folder for S3 service. Available from Rancher v2.2.7 (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resourcepool<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Server</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Datastore</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Folder</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Folder for S3 service. Available from Rancher v2.2.7 (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resourcepool<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Server</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Datastore</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>folder</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Folder for S3 service. Available from Rancher v2.2.7 (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resourcepool<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>server</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Datastore</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>folder</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Folder for S3 service. Available from Rancher v2.2.7 (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resourcepool<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>server</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Dns</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigDns">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigDns">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigDnsArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigDnsOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Selector</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Node selector for RKE Ingress (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Reverse<wbr>Cidrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}DNS add-on reverse cidr  (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Upstream<wbr>Nameservers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}DNS add-on upstream nameservers  (list)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Selector</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Node selector for RKE Ingress (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Reverse<wbr>Cidrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}DNS add-on reverse cidr  (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Upstream<wbr>Nameservers</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}DNS add-on upstream nameservers  (list)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Selector</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Node selector for RKE Ingress (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>reverse<wbr>Cidrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}DNS add-on reverse cidr  (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>upstream<wbr>Nameservers</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}DNS add-on upstream nameservers  (list)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Selector</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Node selector for RKE Ingress (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>reverse<wbr>Cidrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}DNS add-on reverse cidr  (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>upstream<wbr>Nameservers</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}DNS add-on upstream nameservers  (list)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Ingress</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigIngress">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigIngress">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigIngressArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigIngressOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Ingress controller DNS policy. `ClusterFirstWithHostNet`, `ClusterFirst`, `Default`, and `None` are supported. [K8S dns Policy](https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/#pod-s-dns-policy) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Selector</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Node selector for RKE Ingress (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Ingress controller DNS policy. `ClusterFirstWithHostNet`, `ClusterFirst`, `Default`, and `None` are supported. [K8S dns Policy](https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/#pod-s-dns-policy) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Selector</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Node selector for RKE Ingress (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>dns<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Ingress controller DNS policy. `ClusterFirstWithHostNet`, `ClusterFirst`, `Default`, and `None` are supported. [K8S dns Policy](https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/#pod-s-dns-policy) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Selector</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Node selector for RKE Ingress (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>dns<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Ingress controller DNS policy. `ClusterFirstWithHostNet`, `ClusterFirst`, `Default`, and `None` are supported. [K8S dns Policy](https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/#pod-s-dns-policy) (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Selector</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Node selector for RKE Ingress (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Monitoring</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigMonitoring">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigMonitoring">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigMonitoringArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigMonitoringOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Provider for RKE monitoring (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Network</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigNetwork">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigNetwork">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Calico<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkcaliconetworkprovider">Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Calico<wbr>Network<wbr>Provider<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Calico provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Canal<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkcanalnetworkprovider">Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Canal<wbr>Network<wbr>Provider<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Canal provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Flannel<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkflannelnetworkprovider">Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Flannel<wbr>Network<wbr>Provider<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Flannel provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mtu</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Network provider MTU. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Plugin</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Plugin for RKE network. `canal` (default), `flannel`, `calico`, `none` and `weave` are supported. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Weave<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkweavenetworkprovider">Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Weave<wbr>Network<wbr>Provider<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Weave provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Calico<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkcaliconetworkprovider">*Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Calico<wbr>Network<wbr>Provider</a></span>
    </dt>
    <dd>{{% md %}}Calico provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Canal<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkcanalnetworkprovider">*Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Canal<wbr>Network<wbr>Provider</a></span>
    </dt>
    <dd>{{% md %}}Canal provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Flannel<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkflannelnetworkprovider">*Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Flannel<wbr>Network<wbr>Provider</a></span>
    </dt>
    <dd>{{% md %}}Flannel provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mtu</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Network provider MTU. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Plugin</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Plugin for RKE network. `canal` (default), `flannel`, `calico`, `none` and `weave` are supported. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Weave<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkweavenetworkprovider">*Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Weave<wbr>Network<wbr>Provider</a></span>
    </dt>
    <dd>{{% md %}}Weave provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>calico<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkcaliconetworkprovider">Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Calico<wbr>Network<wbr>Provider?</a></span>
    </dt>
    <dd>{{% md %}}Calico provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>canal<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkcanalnetworkprovider">Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Canal<wbr>Network<wbr>Provider?</a></span>
    </dt>
    <dd>{{% md %}}Canal provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>flannel<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkflannelnetworkprovider">Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Flannel<wbr>Network<wbr>Provider?</a></span>
    </dt>
    <dd>{{% md %}}Flannel provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mtu</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Network provider MTU. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>plugin</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Plugin for RKE network. `canal` (default), `flannel`, `calico`, `none` and `weave` are supported. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>weave<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkweavenetworkprovider">Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Weave<wbr>Network<wbr>Provider?</a></span>
    </dt>
    <dd>{{% md %}}Weave provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>calico<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkcaliconetworkprovider">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Calico<wbr>Network<wbr>Provider]</a></span>
    </dt>
    <dd>{{% md %}}Calico provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>canal<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkcanalnetworkprovider">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Canal<wbr>Network<wbr>Provider]</a></span>
    </dt>
    <dd>{{% md %}}Canal provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>flannel<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkflannelnetworkprovider">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Flannel<wbr>Network<wbr>Provider]</a></span>
    </dt>
    <dd>{{% md %}}Flannel provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mtu</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Network provider MTU. Default `0` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}RKE options for network (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>plugin</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Plugin for RKE network. `canal` (default), `flannel`, `calico`, `none` and `weave` are supported. (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>weave<wbr>Network<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfignetworkweavenetworkprovider">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Weave<wbr>Network<wbr>Provider]</a></span>
    </dt>
    <dd>{{% md %}}Weave provider config for RKE network (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Calico<wbr>Network<wbr>Provider</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigNetworkCalicoNetworkProvider">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigNetworkCalicoNetworkProvider">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkCalicoNetworkProviderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkCalicoNetworkProviderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE options for Calico network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}RKE options for Calico network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE options for Calico network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cloud<wbr>Provider</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}RKE options for Calico network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Canal<wbr>Network<wbr>Provider</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigNetworkCanalNetworkProvider">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigNetworkCanalNetworkProvider">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkCanalNetworkProviderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkCanalNetworkProviderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Iface</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Iface config Flannel network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Iface</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Iface config Flannel network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>iface</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Iface config Flannel network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>iface</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Iface config Flannel network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Flannel<wbr>Network<wbr>Provider</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigNetworkFlannelNetworkProvider">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigNetworkFlannelNetworkProvider">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkFlannelNetworkProviderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkFlannelNetworkProviderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Iface</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Iface config Flannel network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Iface</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Iface config Flannel network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>iface</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Iface config Flannel network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>iface</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Iface config Flannel network provider (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Network<wbr>Weave<wbr>Network<wbr>Provider</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigNetworkWeaveNetworkProvider">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigNetworkWeaveNetworkProvider">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkWeaveNetworkProviderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNetworkWeaveNetworkProviderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
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
    <dd>{{% md %}}Registry password (string)
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
    <dd>{{% md %}}Registry password (string)
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
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Node</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigNode">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigNode">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNodeArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigNodeOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Address ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Socket</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker socket for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Hostname<wbr>Override</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Hostname override for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Internal<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Internal ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Id for the node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Roles</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}Roles for the node. `controlplane`, `etcd` and `worker` are supported. (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
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
    <dd>{{% md %}}Address ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Socket</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Docker socket for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Hostname<wbr>Override</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Hostname override for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Internal<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Internal ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Node<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Id for the node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Roles</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Roles for the node. `controlplane`, `etcd` and `worker` are supported. (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Node SSH private key (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
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
    <dd>{{% md %}}Address ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>docker<wbr>Socket</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker socket for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>hostname<wbr>Override</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Hostname override for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>internal<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Internal ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Id for the node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>roles</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Roles for the node. `controlplane`, `etcd` and `worker` are supported. (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
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
    <dd>{{% md %}}Address ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>docker<wbr>Socket</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Docker socket for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>hostname<wbr>Override</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Hostname override for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>internal<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Internal ip for node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Labels for cluster registration token object (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>node<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Id for the node (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Port for node. Default `22` (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>roles</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Roles for the node. `controlplane`, `etcd` and `worker` are supported. (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Agent<wbr>Auth</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Use ssh agent auth. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Node SSH private key (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ssh<wbr>Key<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Node SSH private key path (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Private<wbr>Registry</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigPrivateRegistry">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigPrivateRegistry">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigPrivateRegistryArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigPrivateRegistryOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Is<wbr>Default</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Set as default registry. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry URL (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Is<wbr>Default</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Set as default registry. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry URL (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>is<wbr>Default</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Set as default registry. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Registry URL (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>is<wbr>Default</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Set as default registry. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry password (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry URL (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Registry user (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServices">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServices">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Etcd</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcd">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Etcd options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kube<wbr>Api</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapi">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Kube API options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kube<wbr>Controller</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubecontroller">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Controller<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Kube Controller options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubelet</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubelet">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubelet<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Kubelet options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubeproxy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeproxy">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubeproxy<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Kubeproxy options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduler</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesscheduler">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Scheduler<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Scheduler options for RKE services (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Etcd</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcd">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd</a></span>
    </dt>
    <dd>{{% md %}}Etcd options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kube<wbr>Api</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapi">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api</a></span>
    </dt>
    <dd>{{% md %}}Kube API options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kube<wbr>Controller</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubecontroller">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Controller</a></span>
    </dt>
    <dd>{{% md %}}Kube Controller options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubelet</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubelet">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubelet</a></span>
    </dt>
    <dd>{{% md %}}Kubelet options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kubeproxy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeproxy">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubeproxy</a></span>
    </dt>
    <dd>{{% md %}}Kubeproxy options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scheduler</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesscheduler">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Scheduler</a></span>
    </dt>
    <dd>{{% md %}}Scheduler options for RKE services (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>etcd</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcd">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd?</a></span>
    </dt>
    <dd>{{% md %}}Etcd options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kube<wbr>Api</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapi">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api?</a></span>
    </dt>
    <dd>{{% md %}}Kube API options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kube<wbr>Controller</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubecontroller">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Controller?</a></span>
    </dt>
    <dd>{{% md %}}Kube Controller options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubelet</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubelet">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubelet?</a></span>
    </dt>
    <dd>{{% md %}}Kubelet options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubeproxy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeproxy">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubeproxy?</a></span>
    </dt>
    <dd>{{% md %}}Kubeproxy options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduler</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesscheduler">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Scheduler?</a></span>
    </dt>
    <dd>{{% md %}}Scheduler options for RKE services (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>etcd</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcd">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd]</a></span>
    </dt>
    <dd>{{% md %}}Etcd options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kube<wbr>Api</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapi">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api]</a></span>
    </dt>
    <dd>{{% md %}}Kube API options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kube<wbr>Controller</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubecontroller">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Controller]</a></span>
    </dt>
    <dd>{{% md %}}Kube Controller options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubelet</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubelet">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubelet]</a></span>
    </dt>
    <dd>{{% md %}}Kubelet options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kubeproxy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeproxy">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubeproxy]</a></span>
    </dt>
    <dd>{{% md %}}Kubeproxy options for RKE services (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scheduler</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesscheduler">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Scheduler]</a></span>
    </dt>
    <dd>{{% md %}}Scheduler options for RKE services (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesEtcd">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesEtcd">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesEtcdArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesEtcdOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Backup<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcdbackupconfig">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Backup options for etcd service. Just for Rancher v2.2.x (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ca<wbr>Cert</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}TLS CA certificate for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cert</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}TLS certificate for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Creation</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Creation option for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>External<wbr>Urls</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}External urls for etcd service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gid</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Etcd service GID. Default: `0`. For Rancher v2.3.x or above (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}TLS key for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional) Audit log path. Default: `/var/log/kube-audit/audit-log.json` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshot</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Snapshot option for etcd service (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Uid</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Etcd service UID. Default: `0`. For Rancher v2.3.x or above (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Backup<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcdbackupconfig">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}Backup options for etcd service. Just for Rancher v2.2.x (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ca<wbr>Cert</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}TLS CA certificate for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cert</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}TLS certificate for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Creation</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Creation option for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>External<wbr>Urls</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}External urls for etcd service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gid</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Etcd service GID. Default: `0`. For Rancher v2.3.x or above (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}TLS key for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Optional) Audit log path. Default: `/var/log/kube-audit/audit-log.json` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshot</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Snapshot option for etcd service (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Uid</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Etcd service UID. Default: `0`. For Rancher v2.3.x or above (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>backup<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcdbackupconfig">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}Backup options for etcd service. Just for Rancher v2.2.x (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ca<wbr>Cert</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}TLS CA certificate for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cert</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}TLS certificate for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>creation</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Creation option for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>external<wbr>Urls</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}External urls for etcd service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gid</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Etcd service GID. Default: `0`. For Rancher v2.3.x or above (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}TLS key for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional) Audit log path. Default: `/var/log/kube-audit/audit-log.json` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshot</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Snapshot option for etcd service (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>uid</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Etcd service UID. Default: `0`. For Rancher v2.3.x or above (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>backup_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcdbackupconfig">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}Backup options for etcd service. Just for Rancher v2.2.x (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ca<wbr>Cert</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}TLS CA certificate for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cert</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}TLS certificate for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>creation</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Creation option for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>external<wbr>Urls</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}External urls for etcd service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gid</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Etcd service GID. Default: `0`. For Rancher v2.3.x or above (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}TLS key for etcd service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Optional) Audit log path. Default: `/var/log/kube-audit/audit-log.json` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshot</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Snapshot option for etcd service (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>uid</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Etcd service UID. Default: `0`. For Rancher v2.3.x or above (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesEtcdBackupConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesEtcdBackupConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesEtcdBackupConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesEtcdBackupConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Interval<wbr>Hours</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Interval hours for etcd backup. Default `12` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>S3Backup<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcdbackupconfigs3backupconfig">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config<wbr>S3Backup<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}S3 config options for etcd backup (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Safe<wbr>Timestamp</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Safe timestamp for etcd backup. Default: `false` (bool)
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
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Interval<wbr>Hours</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Interval hours for etcd backup. Default `12` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>S3Backup<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcdbackupconfigs3backupconfig">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config<wbr>S3Backup<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}S3 config options for etcd backup (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Safe<wbr>Timestamp</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Safe timestamp for etcd backup. Default: `false` (bool)
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
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>interval<wbr>Hours</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Interval hours for etcd backup. Default `12` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>s3Backup<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcdbackupconfigs3backupconfig">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config<wbr>S3Backup<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}S3 config options for etcd backup (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>safe<wbr>Timestamp</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Safe timestamp for etcd backup. Default: `false` (bool)
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
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>interval<wbr>Hours</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Interval hours for etcd backup. Default `12` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>s3Backup<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigservicesetcdbackupconfigs3backupconfig">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config<wbr>S3Backup<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}S3 config options for etcd backup (list maxitems:1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>safe<wbr>Timestamp</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Safe timestamp for etcd backup. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Etcd<wbr>Backup<wbr>Config<wbr>S3Backup<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesEtcdBackupConfigS3BackupConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesEtcdBackupConfigS3BackupConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesEtcdBackupConfigS3BackupConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesEtcdBackupConfigS3BackupConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Access<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Bucket name for S3 service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Ca</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Base64 encoded custom CA for S3 service. Use filebase64(<FILE>) for encoding file. Available from Rancher v2.2.5 (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Endpoint for S3 service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Folder</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Folder for S3 service. Available from Rancher v2.2.7 (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Secret<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Client Secret associated with the Client ID (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Access<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The AWS Client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Bucket name for S3 service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Ca</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Base64 encoded custom CA for S3 service. Use filebase64(<FILE>) for encoding file. Available from Rancher v2.2.5 (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Endpoint for S3 service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Folder</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Folder for S3 service. Available from Rancher v2.2.7 (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Secret<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The AWS Client Secret associated with the Client ID (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>access<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Bucket name for S3 service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Ca</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Base64 encoded custom CA for S3 service. Use filebase64(<FILE>) for encoding file. Available from Rancher v2.2.5 (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Endpoint for S3 service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>folder</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Folder for S3 service. Available from Rancher v2.2.7 (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>secret<wbr>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The AWS Client Secret associated with the Client ID (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>access_<wbr>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS Client ID to use (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>bucket<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Bucket name for S3 service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Ca</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Base64 encoded custom CA for S3 service. Use filebase64(<FILE>) for encoding file. Available from Rancher v2.2.5 (string)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Endpoint for S3 service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>folder</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Folder for S3 service. Available from Rancher v2.2.7 (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS Region to create the EKS cluster in. Default `us-west-2` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>secret_<wbr>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS Client Secret associated with the Client ID (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesKubeApi">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesKubeApi">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Admission<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Admission configuration (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Always<wbr>Pull<wbr>Images</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable [AlwaysPullImages](https://kubernetes.io/docs/reference/access-authn-authz/admission-controllers/#alwayspullimages) Admission controller plugin. [Rancher docs](https://rancher.com/docs/rke/latest/en/config-options/services/#kubernetes-api-server-options) Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Audit<wbr>Log</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapiauditlog">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}K8s audit log configuration. (list maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Event<wbr>Rate<wbr>Limit</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapieventratelimit">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Event<wbr>Rate<wbr>Limit<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}K8s event rate limit configuration. (list maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pod<wbr>Security<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Pod Security Policy option for kube API service. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Secrets<wbr>Encryption<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapisecretsencryptionconfig">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Secrets<wbr>Encryption<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}[Encrypt k8s secret data configration](https://rancher.com/docs/rke/latest/en/config-options/secrets-encryption/). (list maxitem: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Cluster<wbr>Ip<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Service Cluster ip Range option for kube controller service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Node<wbr>Port<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Service Node Port Range option for kube API service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Admission<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Admission configuration (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Always<wbr>Pull<wbr>Images</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable [AlwaysPullImages](https://kubernetes.io/docs/reference/access-authn-authz/admission-controllers/#alwayspullimages) Admission controller plugin. [Rancher docs](https://rancher.com/docs/rke/latest/en/config-options/services/#kubernetes-api-server-options) Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Audit<wbr>Log</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapiauditlog">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log</a></span>
    </dt>
    <dd>{{% md %}}K8s audit log configuration. (list maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Event<wbr>Rate<wbr>Limit</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapieventratelimit">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Event<wbr>Rate<wbr>Limit</a></span>
    </dt>
    <dd>{{% md %}}K8s event rate limit configuration. (list maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pod<wbr>Security<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Pod Security Policy option for kube API service. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Secrets<wbr>Encryption<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapisecretsencryptionconfig">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Secrets<wbr>Encryption<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}[Encrypt k8s secret data configration](https://rancher.com/docs/rke/latest/en/config-options/secrets-encryption/). (list maxitem: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Cluster<wbr>Ip<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Service Cluster ip Range option for kube controller service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Node<wbr>Port<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Service Node Port Range option for kube API service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admission<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Admission configuration (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>always<wbr>Pull<wbr>Images</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable [AlwaysPullImages](https://kubernetes.io/docs/reference/access-authn-authz/admission-controllers/#alwayspullimages) Admission controller plugin. [Rancher docs](https://rancher.com/docs/rke/latest/en/config-options/services/#kubernetes-api-server-options) Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>audit<wbr>Log</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapiauditlog">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log?</a></span>
    </dt>
    <dd>{{% md %}}K8s audit log configuration. (list maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>event<wbr>Rate<wbr>Limit</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapieventratelimit">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Event<wbr>Rate<wbr>Limit?</a></span>
    </dt>
    <dd>{{% md %}}K8s event rate limit configuration. (list maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pod<wbr>Security<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Pod Security Policy option for kube API service. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>secrets<wbr>Encryption<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapisecretsencryptionconfig">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Secrets<wbr>Encryption<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}[Encrypt k8s secret data configration](https://rancher.com/docs/rke/latest/en/config-options/secrets-encryption/). (list maxitem: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Cluster<wbr>Ip<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Service Cluster ip Range option for kube controller service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Node<wbr>Port<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Service Node Port Range option for kube API service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admission<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Admission configuration (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>always<wbr>Pull<wbr>Images</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable [AlwaysPullImages](https://kubernetes.io/docs/reference/access-authn-authz/admission-controllers/#alwayspullimages) Admission controller plugin. [Rancher docs](https://rancher.com/docs/rke/latest/en/config-options/services/#kubernetes-api-server-options) Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>audit<wbr>Log</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapiauditlog">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log]</a></span>
    </dt>
    <dd>{{% md %}}K8s audit log configuration. (list maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>event<wbr>Rate<wbr>Limit</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapieventratelimit">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Event<wbr>Rate<wbr>Limit]</a></span>
    </dt>
    <dd>{{% md %}}K8s event rate limit configuration. (list maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pod<wbr>Security<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Pod Security Policy option for kube API service. Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>secrets<wbr>Encryption<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapisecretsencryptionconfig">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Secrets<wbr>Encryption<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}[Encrypt k8s secret data configration](https://rancher.com/docs/rke/latest/en/config-options/secrets-encryption/). (list maxitem: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Cluster<wbr>Ip<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Service Cluster ip Range option for kube controller service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Node<wbr>Port<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Service Node Port Range option for kube API service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesKubeApiAuditLog">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesKubeApiAuditLog">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiAuditLogArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiAuditLogOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapiauditlogconfiguration">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Event rate limit configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapiauditlogconfiguration">*Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Event rate limit configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapiauditlogconfiguration">Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}Event rate limit configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigserviceskubeapiauditlogconfiguration">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}Event rate limit configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Audit<wbr>Log<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesKubeApiAuditLogConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesKubeApiAuditLogConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiAuditLogConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiAuditLogConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Format</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Audit log format. Default: 'json' (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Age</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Audit log max age. Default: `30` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Backup</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Audit log max backup. Default: `10` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Audit log max size. Default: `100` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional) Audit log path. Default: `/var/log/kube-audit/audit-log.json` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Audit policy yaml encoded definition. `apiVersion` and `kind: Policy\nrules:"` fields are required in the yaml. Ex. `"apiVersion: audit.k8s.io/v1\nkind: Policy\nrules:\n- level: RequestResponse\n  resources:\n  - resources:\n    - pods\n"` [More info](https://rancher.com/docs/rke/latest/en/config-options/audit-log/) (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Format</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Audit log format. Default: 'json' (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Age</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Audit log max age. Default: `30` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Backup</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Audit log max backup. Default: `10` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Audit log max size. Default: `100` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}(Optional) Audit log path. Default: `/var/log/kube-audit/audit-log.json` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Audit policy yaml encoded definition. `apiVersion` and `kind: Policy\nrules:"` fields are required in the yaml. Ex. `"apiVersion: audit.k8s.io/v1\nkind: Policy\nrules:\n- level: RequestResponse\n  resources:\n  - resources:\n    - pods\n"` [More info](https://rancher.com/docs/rke/latest/en/config-options/audit-log/) (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>format</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Audit log format. Default: 'json' (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Age</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Audit log max age. Default: `30` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Backup</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Audit log max backup. Default: `10` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Audit log max size. Default: `100` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}(Optional) Audit log path. Default: `/var/log/kube-audit/audit-log.json` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Audit policy yaml encoded definition. `apiVersion` and `kind: Policy\nrules:"` fields are required in the yaml. Ex. `"apiVersion: audit.k8s.io/v1\nkind: Policy\nrules:\n- level: RequestResponse\n  resources:\n  - resources:\n    - pods\n"` [More info](https://rancher.com/docs/rke/latest/en/config-options/audit-log/) (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>format</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Audit log format. Default: 'json' (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Age</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Audit log max age. Default: `30` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Backup</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Audit log max backup. Default: `10` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Audit log max size. Default: `100` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}(Optional) Audit log path. Default: `/var/log/kube-audit/audit-log.json` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Audit policy yaml encoded definition. `apiVersion` and `kind: Policy\nrules:"` fields are required in the yaml. Ex. `"apiVersion: audit.k8s.io/v1\nkind: Policy\nrules:\n- level: RequestResponse\n  resources:\n  - resources:\n    - pods\n"` [More info](https://rancher.com/docs/rke/latest/en/config-options/audit-log/) (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Event<wbr>Rate<wbr>Limit</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesKubeApiEventRateLimit">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesKubeApiEventRateLimit">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiEventRateLimitArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiEventRateLimitOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Event rate limit configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Event rate limit configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Event rate limit configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Event rate limit configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Api<wbr>Secrets<wbr>Encryption<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesKubeApiSecretsEncryptionConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesKubeApiSecretsEncryptionConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiSecretsEncryptionConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeApiSecretsEncryptionConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Secrets encryption configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Secrets encryption configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Secrets encryption configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Secrets encryption configuration. (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kube<wbr>Controller</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesKubeController">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesKubeController">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeControllerArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeControllerOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster CIDR option for kube controller service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Cluster<wbr>Ip<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Service Cluster ip Range option for kube controller service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster CIDR option for kube controller service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Service<wbr>Cluster<wbr>Ip<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Service Cluster ip Range option for kube controller service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster CIDR option for kube controller service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Cluster<wbr>Ip<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Service Cluster ip Range option for kube controller service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Cidr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster CIDR option for kube controller service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>service<wbr>Cluster<wbr>Ip<wbr>Range</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Service Cluster ip Range option for kube controller service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubelet</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesKubelet">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesKubelet">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeletArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeletOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Dns<wbr>Server</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster DNS Server option for kubelet service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster Domain option for kubelet service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fail<wbr>Swap<wbr>On</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable or disable failing when swap on is not supported (bool)
* `generate_serving_certificate` [Generate a certificate signed by the kube-ca](https://rancher.com/docs/rke/latest/en/config-options/services/#kubelet-serving-certificate-requirements). Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Generate<wbr>Serving<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Infra<wbr>Container<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Infra container image for kubelet service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Dns<wbr>Server</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster DNS Server option for kubelet service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cluster<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster Domain option for kubelet service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fail<wbr>Swap<wbr>On</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable or disable failing when swap on is not supported (bool)
* `generate_serving_certificate` [Generate a certificate signed by the kube-ca](https://rancher.com/docs/rke/latest/en/config-options/services/#kubelet-serving-certificate-requirements). Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Generate<wbr>Serving<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Infra<wbr>Container<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Infra container image for kubelet service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Dns<wbr>Server</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster DNS Server option for kubelet service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster Domain option for kubelet service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fail<wbr>Swap<wbr>On</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable or disable failing when swap on is not supported (bool)
* `generate_serving_certificate` [Generate a certificate signed by the kube-ca](https://rancher.com/docs/rke/latest/en/config-options/services/#kubelet-serving-certificate-requirements). Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>generate<wbr>Serving<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>infra<wbr>Container<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Infra container image for kubelet service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Dns<wbr>Server</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster DNS Server option for kubelet service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cluster<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster Domain option for kubelet service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fail<wbr>Swap<wbr>On</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable or disable failing when swap on is not supported (bool)
* `generate_serving_certificate` [Generate a certificate signed by the kube-ca](https://rancher.com/docs/rke/latest/en/config-options/services/#kubelet-serving-certificate-requirements). Default `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>generate<wbr>Serving<wbr>Certificate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>infra<wbr>Container<wbr>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Infra container image for kubelet service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Kubeproxy</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesKubeproxy">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesKubeproxy">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeproxyArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesKubeproxyOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Services<wbr>Scheduler</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigServicesScheduler">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigServicesScheduler">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesSchedulerArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigServicesSchedulerOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Image</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Args</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Extra arguments for scheduler service (map)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Binds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra binds for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Envs</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Extra environment for scheduler service (list)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>image</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Docker image for scheduler service (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigUpgradeStrategy">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigUpgradeStrategy">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigUpgradeStrategyArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigUpgradeStrategyOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Drain</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}RKE drain nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigupgradestrategydraininput">Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy<wbr>Drain<wbr>Input<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}RKE drain node input (list Maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Unavailable<wbr>Controlplane</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE max unavailable controlplane nodes. Default: `1` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Unavailable<wbr>Worker</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE max unavailable worker nodes. Default: `10%` (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Drain</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}RKE drain nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Drain<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigupgradestrategydraininput">*Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy<wbr>Drain<wbr>Input</a></span>
    </dt>
    <dd>{{% md %}}RKE drain node input (list Maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Unavailable<wbr>Controlplane</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}RKE max unavailable controlplane nodes. Default: `1` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Unavailable<wbr>Worker</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}RKE max unavailable worker nodes. Default: `10%` (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>drain</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}RKE drain nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>drain<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigupgradestrategydraininput">Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy<wbr>Drain<wbr>Input?</a></span>
    </dt>
    <dd>{{% md %}}RKE drain node input (list Maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Unavailable<wbr>Controlplane</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE max unavailable controlplane nodes. Default: `1` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Unavailable<wbr>Worker</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}RKE max unavailable worker nodes. Default: `10%` (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>drain</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}RKE drain nodes. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>drain<wbr>Input</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterrkeconfigupgradestrategydraininput">Dict[Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy<wbr>Drain<wbr>Input]</a></span>
    </dt>
    <dd>{{% md %}}RKE drain node input (list Maxitems: 1)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Unavailable<wbr>Controlplane</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}RKE max unavailable controlplane nodes. Default: `1` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Unavailable<wbr>Worker</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}RKE max unavailable worker nodes. Default: `10%` (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Rke<wbr>Config<wbr>Upgrade<wbr>Strategy<wbr>Drain<wbr>Input</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterRkeConfigUpgradeStrategyDrainInput">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterRkeConfigUpgradeStrategyDrainInput">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigUpgradeStrategyDrainInputArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterRkeConfigUpgradeStrategyDrainInputOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Delete<wbr>Local<wbr>Data</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Delete RKE node local data. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Force</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Force RKE node drain. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}RKE node drain grace period. Default: `-1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ignore<wbr>Daemon<wbr>Sets</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Ignore RKE daemon sets. Default: `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}RKE node drain timeout. Default: `60` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Delete<wbr>Local<wbr>Data</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Delete RKE node local data. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Force</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Force RKE node drain. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}RKE node drain grace period. Default: `-1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ignore<wbr>Daemon<wbr>Sets</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Ignore RKE daemon sets. Default: `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}RKE node drain timeout. Default: `60` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>delete<wbr>Local<wbr>Data</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Delete RKE node local data. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>force</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Force RKE node drain. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}RKE node drain grace period. Default: `-1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ignore<wbr>Daemon<wbr>Sets</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Ignore RKE daemon sets. Default: `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}RKE node drain timeout. Default: `60` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>delete<wbr>Local<wbr>Data</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Delete RKE node local data. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>force</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Force RKE node drain. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>grace<wbr>Period</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}RKE node drain grace period. Default: `-1` (int)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ignore<wbr>Daemon<wbr>Sets</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Ignore RKE daemon sets. Default: `true` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}RKE node drain timeout. Default: `60` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterScheduledClusterScan">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterScheduledClusterScan">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterScheduledClusterScanArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterScheduledClusterScanOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Scan<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscanconfig">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}Cluster scan config (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Schedule<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscheduleconfig">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Schedule<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}Cluster scan schedule config (list maxitems:1)
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
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Scan<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscanconfig">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}Cluster scan config (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Schedule<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscheduleconfig">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Schedule<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}Cluster scan schedule config (list maxitems:1)
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
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>scan<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscanconfig">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}Cluster scan config (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>schedule<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscheduleconfig">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Schedule<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}Cluster scan schedule config (list maxitems:1)
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
    <dd>{{% md %}}Enable scheduled cluster scan. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>scan<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscanconfig">Dict[Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}Cluster scan config (List maxitems:1)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>schedule<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscheduleconfig">Dict[Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Schedule<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}Cluster scan schedule config (list maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterScheduledClusterScanScanConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterScheduledClusterScanScanConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterScheduledClusterScanScanConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterScheduledClusterScanScanConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cis<wbr>Scan<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscanconfigcisscanconfig">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config<wbr>Cis<wbr>Scan<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Cluster Cis Scan config (List maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cis<wbr>Scan<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscanconfigcisscanconfig">*Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config<wbr>Cis<wbr>Scan<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}Cluster Cis Scan config (List maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cis<wbr>Scan<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscanconfigcisscanconfig">Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config<wbr>Cis<wbr>Scan<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}Cluster Cis Scan config (List maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cis<wbr>Scan<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#clusterscheduledclusterscanscanconfigcisscanconfig">Dict[Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config<wbr>Cis<wbr>Scan<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}Cluster Cis Scan config (List maxitems:1)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Scan<wbr>Config<wbr>Cis<wbr>Scan<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterScheduledClusterScanScanConfigCisScanConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterScheduledClusterScanScanConfigCisScanConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterScheduledClusterScanScanConfigCisScanConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterScheduledClusterScanScanConfigCisScanConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Debug<wbr>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Debug master. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Debug<wbr>Worker</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Debug worker. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Override<wbr>Benchmark<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Override benchmark version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Override<wbr>Skips</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Override skip (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cis scan profile. Allowed values: `"permissive" (default) || "hardened"` (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Debug<wbr>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Debug master. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Debug<wbr>Worker</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Debug worker. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Override<wbr>Benchmark<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Override benchmark version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Override<wbr>Skips</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Override skip (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cis scan profile. Allowed values: `"permissive" (default) || "hardened"` (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>debug<wbr>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Debug master. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>debug<wbr>Worker</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Debug worker. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>override<wbr>Benchmark<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Override benchmark version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>override<wbr>Skips</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Override skip (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cis scan profile. Allowed values: `"permissive" (default) || "hardened"` (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>debug<wbr>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Debug master. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>debug<wbr>Worker</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Debug worker. Default: `false` (bool)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>override<wbr>Benchmark<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Override benchmark version (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>override<wbr>Skips</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Override skip (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cis scan profile. Allowed values: `"permissive" (default) || "hardened"` (string)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Cluster<wbr>Scheduled<wbr>Cluster<wbr>Scan<wbr>Schedule<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/input/#ClusterScheduledClusterScanScheduleConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/rancher2/types/output/#ClusterScheduledClusterScanScheduleConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterScheduledClusterScanScheduleConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-rancher2/sdk/go/rancher2/?tab=doc#ClusterScheduledClusterScanScheduleConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Cron<wbr>Schedule</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Crontab schedule. It should contains 5 fields `"<min> <hour> <month_day> <month> <week_day>"` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Cron<wbr>Schedule</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Crontab schedule. It should contains 5 fields `"<min> <hour> <month_day> <month> <week_day>"` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>cron<wbr>Schedule</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Crontab schedule. It should contains 5 fields `"<min> <hour> <month_day> <month> <week_day>"` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>cron<wbr>Schedule</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Crontab schedule. It should contains 5 fields `"<min> <hour> <month_day> <month> <week_day>"` (string)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>retention</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Retention for etcd backup. Default `6` (int)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-rancher2">https://github.com/pulumi/pulumi-rancher2</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

