
---
title: "ComputeClusterVmDependencyRule"
block_external_search_index: true
---



The `vsphere..ComputeClusterVmDependencyRule` resource can be used to manage
VM dependency rules in a cluster, either created by the
[`vsphere..ComputeCluster`][tf-vsphere-cluster-resource] resource or looked up
by the [`vsphere..ComputeCluster`][tf-vsphere-cluster-data-source] data source.

[tf-vsphere-cluster-resource]: /docs/providers/vsphere/r/compute_cluster.html
[tf-vsphere-cluster-data-source]: /docs/providers/vsphere/d/compute_cluster.html

A virtual machine dependency rule applies to vSphere HA, and allows
user-defined startup orders for virtual machines in the case of host failure.
Virtual machines are supplied via groups, which can be managed via the
[`vsphere..ComputeClusterVmGroup`][tf-vsphere-cluster-vm-group-resource]
resource.

[tf-vsphere-cluster-vm-group-resource]: /docs/providers/vsphere/r/compute_cluster_vm_group.html

> **NOTE:** This resource requires vCenter and is not available on direct ESXi
connections.

## Example Usage

The example below creates two virtual machine in a cluster using the
[`vsphere..VirtualMachine`][tf-vsphere-vm-resource] resource in a cluster
looked up by the [`vsphere..ComputeCluster`][tf-vsphere-cluster-data-source]
data source. It then creates a group with this virtual machine. Two groups are created, each with one of the created VMs. Finally, a rule is created to ensure that `vm1` starts before `vm2`.

[tf-vsphere-vm-resource]: /docs/providers/vsphere/r/virtual_machine.html

> Note how `dependency_vm_group_name` and
`vm_group_name` are sourced off of the `name` attributes from
the [`vsphere..ComputeClusterVmGroup`][tf-vsphere-cluster-vm-group-resource]
resource. This is to ensure that the rule is not created before the groups
exist, which may not possibly happen in the event that the names came from a
"static" source such as a variable.

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as vsphere from "@pulumi/vsphere";

const dc = pulumi.output(vsphere.getDatacenter({
    name: "dc1",
}, { async: true }));
const datastore = dc.apply(dc => vsphere.getDatastore({
    datacenterId: dc.id,
    name: "datastore1",
}, { async: true }));
const cluster = dc.apply(dc => vsphere.getComputeCluster({
    datacenterId: dc.id,
    name: "cluster1",
}, { async: true }));
const network = dc.apply(dc => vsphere.getNetwork({
    datacenterId: dc.id,
    name: "network1",
}, { async: true }));
const vm1 = new vsphere.VirtualMachine("vm1", {
    datastoreId: datastore.id,
    disks: [{
        label: "disk0",
        size: 20,
    }],
    guestId: "other3xLinux64Guest",
    memory: 2048,
    networkInterfaces: [{
        networkId: network.id,
    }],
    numCpus: 2,
    resourcePoolId: cluster.resourcePoolId,
});
const vm2 = new vsphere.VirtualMachine("vm2", {
    datastoreId: datastore.id,
    disks: [{
        label: "disk0",
        size: 20,
    }],
    guestId: "other3xLinux64Guest",
    memory: 2048,
    networkInterfaces: [{
        networkId: network.id,
    }],
    numCpus: 2,
    resourcePoolId: cluster.resourcePoolId,
});
const clusterVmGroup1 = new vsphere.ComputeClusterVmGroup("cluster_vm_group1", {
    computeClusterId: cluster.id,
    virtualMachineIds: [vm1.id],
});
const clusterVmGroup2 = new vsphere.ComputeClusterVmGroup("cluster_vm_group2", {
    computeClusterId: cluster.id,
    virtualMachineIds: [vm2.id],
});
const clusterVmDependencyRule = new vsphere.ComputeClusterVmDependencyRule("cluster_vm_dependency_rule", {
    computeClusterId: cluster.id,
    dependencyVmGroupName: clusterVmGroup1.name,
    vmGroupName: clusterVmGroup2.name,
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-vsphere/blob/master/website/docs/r/compute_cluster_vm_dependency_rule.html.markdown.



## Create a ComputeClusterVmDependencyRule Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/vsphere/#ComputeClusterVmDependencyRule">ComputeClusterVmDependencyRule</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/vsphere/#ComputeClusterVmDependencyRuleArgs">ComputeClusterVmDependencyRuleArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">ComputeClusterVmDependencyRule</span><span class="p">(resource_name, opts=None, </span>compute_cluster_id=None<span class="p">, </span>dependency_vm_group_name=None<span class="p">, </span>enabled=None<span class="p">, </span>mandatory=None<span class="p">, </span>name=None<span class="p">, </span>vm_group_name=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewComputeClusterVmDependencyRule<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-vsphere/sdk/go/vsphere/?tab=doc#ComputeClusterVmDependencyRuleArgs">ComputeClusterVmDependencyRuleArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-vsphere/sdk/go/vsphere/?tab=doc#ComputeClusterVmDependencyRule">ComputeClusterVmDependencyRule</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Vsphere/Pulumi.Vsphere..ComputeClusterVmDependencyRule.html">ComputeClusterVmDependencyRule</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Vsphere/Pulumi.Vsphere.ComputeClusterVmDependencyRuleArgs.html">ComputeClusterVmDependencyRuleArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Compute<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dependency<wbr>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Compute<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dependency<wbr>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>compute<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dependency<wbr>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>compute_<wbr>cluster_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dependency_<wbr>vm_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>vm_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## ComputeClusterVmDependencyRule Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Compute<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dependency<wbr>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Compute<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dependency<wbr>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>compute<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dependency<wbr>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>compute_<wbr>cluster_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dependency_<wbr>vm_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>vm_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing ComputeClusterVmDependencyRule Resource

Get an existing ComputeClusterVmDependencyRule resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/vsphere/#ComputeClusterVmDependencyRuleState">ComputeClusterVmDependencyRuleState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/vsphere/#ComputeClusterVmDependencyRule">ComputeClusterVmDependencyRule</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>compute_cluster_id=None<span class="p">, </span>dependency_vm_group_name=None<span class="p">, </span>enabled=None<span class="p">, </span>mandatory=None<span class="p">, </span>name=None<span class="p">, </span>vm_group_name=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetComputeClusterVmDependencyRule<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-vsphere/sdk/go/vsphere/?tab=doc#ComputeClusterVmDependencyRuleState">ComputeClusterVmDependencyRuleState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-vsphere/sdk/go/vsphere/?tab=doc#ComputeClusterVmDependencyRule">ComputeClusterVmDependencyRule</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Vsphere/Pulumi.Vsphere..ComputeClusterVmDependencyRule.html">ComputeClusterVmDependencyRule</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Vsphere/Pulumi.Vsphere..ComputeClusterVmDependencyRuleState.html">ComputeClusterVmDependencyRuleState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Compute<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dependency<wbr>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Compute<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dependency<wbr>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>compute<wbr>Cluster<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dependency<wbr>Vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vm<wbr>Group<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>compute_<wbr>cluster_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The [managed object reference
ID][docs-about-morefs] of the cluster to put the group in.  Forces a new
resource if changed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dependency_<wbr>vm_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that this
rule depends on. The VMs defined in the group specified by
`vm_group_name` will not be started until the VMs in this
group are started.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Enable this rule in the cluster. Default: `true`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mandatory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}When this value is `true`, prevents any virtual
machine operations that may violate this rule. Default: `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the rule. This must be unique in the
cluster.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vm_<wbr>group_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the VM group that is the subject of
this rule. The VMs defined in this group will not be started until the VMs in
the group specified by
`dependency_vm_group_name` are started.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}











<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-vsphere">https://github.com/pulumi/pulumi-vsphere</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

