
---
title: "TaskDefinition"
block_external_search_index: true
---



Manages a revision of an ECS task definition to be used in `aws.ecs.Service`.

{{% examples %}}
{{% /examples %}}



## Create a TaskDefinition Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ecs/#TaskDefinition">TaskDefinition</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ecs/#TaskDefinitionArgs">TaskDefinitionArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">TaskDefinition</span><span class="p">(resource_name, opts=None, </span>container_definitions=None<span class="p">, </span>cpu=None<span class="p">, </span>execution_role_arn=None<span class="p">, </span>family=None<span class="p">, </span>inference_accelerators=None<span class="p">, </span>ipc_mode=None<span class="p">, </span>memory=None<span class="p">, </span>network_mode=None<span class="p">, </span>pid_mode=None<span class="p">, </span>placement_constraints=None<span class="p">, </span>proxy_configuration=None<span class="p">, </span>requires_compatibilities=None<span class="p">, </span>tags=None<span class="p">, </span>task_role_arn=None<span class="p">, </span>volumes=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewTaskDefinition<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionArgs">TaskDefinitionArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinition">TaskDefinition</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ecs.TaskDefinition.html">TaskDefinition</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ecs.TaskDefinitionArgs.html">TaskDefinitionArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Container<wbr>Definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Execution<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Family</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inference<wbr>Accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">List&lt;Task<wbr>Definition<wbr>Inference<wbr>Accelerator<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipc<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pid<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Placement<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">List&lt;Task<wbr>Definition<wbr>Placement<wbr>Constraint<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Proxy<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">Task<wbr>Definition<wbr>Proxy<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Requires<wbr>Compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Task<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">List&lt;Task<wbr>Definition<wbr>Volume<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Container<wbr>Definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Execution<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Family</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inference<wbr>Accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">[]Task<wbr>Definition<wbr>Inference<wbr>Accelerator</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipc<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pid<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Placement<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">[]Task<wbr>Definition<wbr>Placement<wbr>Constraint</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Proxy<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">*Task<wbr>Definition<wbr>Proxy<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Requires<wbr>Compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Task<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">[]Task<wbr>Definition<wbr>Volume</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>container<wbr>Definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>execution<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>family</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inference<wbr>Accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">Task<wbr>Definition<wbr>Inference<wbr>Accelerator[]?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipc<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pid<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>placement<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">Task<wbr>Definition<wbr>Placement<wbr>Constraint[]?</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>proxy<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">Task<wbr>Definition<wbr>Proxy<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>requires<wbr>Compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>task<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">Task<wbr>Definition<wbr>Volume[]?</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>container_<wbr>definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>execution_<wbr>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>family</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inference_<wbr>accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">List[Task<wbr>Definition<wbr>Inference<wbr>Accelerator]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipc_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pid_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>placement_<wbr>constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">List[Task<wbr>Definition<wbr>Placement<wbr>Constraint]</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>proxy_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">Dict[Task<wbr>Definition<wbr>Proxy<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>requires_<wbr>compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>task_<wbr>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">List[Task<wbr>Definition<wbr>Volume]</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## TaskDefinition Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full ARN of the Task Definition (including both `family` and `revision`).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Container<wbr>Definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Execution<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Family</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Inference<wbr>Accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">List&lt;Task<wbr>Definition<wbr>Inference<wbr>Accelerator&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ipc<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Network<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Pid<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Placement<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">List&lt;Task<wbr>Definition<wbr>Placement<wbr>Constraint&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Proxy<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">Task<wbr>Definition<wbr>Proxy<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Requires<wbr>Compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The revision of the task in a particular family.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Task<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">List&lt;Task<wbr>Definition<wbr>Volume&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full ARN of the Task Definition (including both `family` and `revision`).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Container<wbr>Definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Execution<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Family</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Inference<wbr>Accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">[]Task<wbr>Definition<wbr>Inference<wbr>Accelerator</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ipc<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Network<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Pid<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Placement<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">[]Task<wbr>Definition<wbr>Placement<wbr>Constraint</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Proxy<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">*Task<wbr>Definition<wbr>Proxy<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Requires<wbr>Compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The revision of the task in a particular family.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Task<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">[]Task<wbr>Definition<wbr>Volume</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full ARN of the Task Definition (including both `family` and `revision`).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>container<wbr>Definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>execution<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>family</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>inference<wbr>Accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">Task<wbr>Definition<wbr>Inference<wbr>Accelerator[]?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ipc<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>network<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>pid<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>placement<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">Task<wbr>Definition<wbr>Placement<wbr>Constraint[]?</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>proxy<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">Task<wbr>Definition<wbr>Proxy<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>requires<wbr>Compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The revision of the task in a particular family.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>task<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">Task<wbr>Definition<wbr>Volume[]?</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Full ARN of the Task Definition (including both `family` and `revision`).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>container_<wbr>definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>execution_<wbr>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>family</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>inference_<wbr>accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">List[Task<wbr>Definition<wbr>Inference<wbr>Accelerator]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ipc_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>network_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>pid_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>placement_<wbr>constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">List[Task<wbr>Definition<wbr>Placement<wbr>Constraint]</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>proxy_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">Dict[Task<wbr>Definition<wbr>Proxy<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>requires_<wbr>compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The revision of the task in a particular family.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>task_<wbr>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">List[Task<wbr>Definition<wbr>Volume]</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing TaskDefinition Resource

Get an existing TaskDefinition resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ecs/#TaskDefinitionState">TaskDefinitionState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ecs/#TaskDefinition">TaskDefinition</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>arn=None<span class="p">, </span>container_definitions=None<span class="p">, </span>cpu=None<span class="p">, </span>execution_role_arn=None<span class="p">, </span>family=None<span class="p">, </span>inference_accelerators=None<span class="p">, </span>ipc_mode=None<span class="p">, </span>memory=None<span class="p">, </span>network_mode=None<span class="p">, </span>pid_mode=None<span class="p">, </span>placement_constraints=None<span class="p">, </span>proxy_configuration=None<span class="p">, </span>requires_compatibilities=None<span class="p">, </span>revision=None<span class="p">, </span>tags=None<span class="p">, </span>task_role_arn=None<span class="p">, </span>volumes=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetTaskDefinition<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionState">TaskDefinitionState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinition">TaskDefinition</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ecs.TaskDefinition.html">TaskDefinition</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ecs.TaskDefinitionState.html">TaskDefinitionState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Full ARN of the Task Definition (including both `family` and `revision`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Container<wbr>Definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Execution<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Family</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inference<wbr>Accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">List&lt;Task<wbr>Definition<wbr>Inference<wbr>Accelerator<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipc<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pid<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Placement<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">List&lt;Task<wbr>Definition<wbr>Placement<wbr>Constraint<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Proxy<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">Task<wbr>Definition<wbr>Proxy<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Requires<wbr>Compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The revision of the task in a particular family.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Task<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">List&lt;Task<wbr>Definition<wbr>Volume<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Full ARN of the Task Definition (including both `family` and `revision`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Container<wbr>Definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Execution<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Family</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inference<wbr>Accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">[]Task<wbr>Definition<wbr>Inference<wbr>Accelerator</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Ipc<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pid<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Placement<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">[]Task<wbr>Definition<wbr>Placement<wbr>Constraint</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Proxy<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">*Task<wbr>Definition<wbr>Proxy<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Requires<wbr>Compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The revision of the task in a particular family.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Task<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">[]Task<wbr>Definition<wbr>Volume</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Full ARN of the Task Definition (including both `family` and `revision`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>container<wbr>Definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>execution<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>family</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inference<wbr>Accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">Task<wbr>Definition<wbr>Inference<wbr>Accelerator[]?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipc<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pid<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>placement<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">Task<wbr>Definition<wbr>Placement<wbr>Constraint[]?</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>proxy<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">Task<wbr>Definition<wbr>Proxy<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>requires<wbr>Compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The revision of the task in a particular family.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>task<wbr>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">Task<wbr>Definition<wbr>Volume[]?</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Full ARN of the Task Definition (including both `family` and `revision`).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>container_<wbr>definitions</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A list of valid [container definitions]
(http://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_ContainerDefinition.html) provided as a
single valid JSON document. Please note that you should only provide values that are part of the container
definition document. For a detailed description of what parameters are available, see the [Task Definition Parameters]
(https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html) section from the
official [Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>cpu</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The number of cpu units used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>execution_<wbr>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the task execution role that the Amazon ECS container agent and the Docker daemon can assume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>family</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A unique name for your task definition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inference_<wbr>accelerators</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitioninferenceaccelerator">List[Task<wbr>Definition<wbr>Inference<wbr>Accelerator]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block(s) with Inference Accelerators settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>ipc_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The IPC resource namespace to be used for the containers in the task The valid values are `host`, `task`, and `none`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The amount (in MiB) of memory used by the task. If the `requires_compatibilities` is `FARGATE` this field is required.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Docker networking mode to use for the containers in the task. The valid values are `none`, `bridge`, `awsvpc`, and `host`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pid_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The process namespace to use for the containers in the task. The valid values are `host` and `task`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>placement_<wbr>constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionplacementconstraint">List[Task<wbr>Definition<wbr>Placement<wbr>Constraint]</a></span>
    </dt>
    <dd>{{% md %}}A set of placement constraints rules that are taken into consideration during task placement. Maximum number of `placement_constraints` is `10`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>proxy_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionproxyconfiguration">Dict[Task<wbr>Definition<wbr>Proxy<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The proxy configuration details for the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>requires_<wbr>compatibilities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A set of launch types required by the task. The valid values are `EC2` and `FARGATE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The revision of the task in a particular family.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Key-value mapping of resource tags
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>task_<wbr>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of IAM role that allows your Amazon ECS container task to make calls to other AWS services.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolume">List[Task<wbr>Definition<wbr>Volume]</a></span>
    </dt>
    <dd>{{% md %}}A set of volume blocks that containers in your task may use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Task<wbr>Definition<wbr>Inference<wbr>Accelerator</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#TaskDefinitionInferenceAccelerator">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#TaskDefinitionInferenceAccelerator">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionInferenceAcceleratorArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionInferenceAcceleratorOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Device<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elastic Inference accelerator device name. The deviceName must also be referenced in a container definition as a ResourceRequirement.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Device<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elastic Inference accelerator type to use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Device<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elastic Inference accelerator device name. The deviceName must also be referenced in a container definition as a ResourceRequirement.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Device<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elastic Inference accelerator type to use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>device<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elastic Inference accelerator device name. The deviceName must also be referenced in a container definition as a ResourceRequirement.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>device<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Elastic Inference accelerator type to use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>device_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Elastic Inference accelerator device name. The deviceName must also be referenced in a container definition as a ResourceRequirement.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>device<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Elastic Inference accelerator type to use.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Task<wbr>Definition<wbr>Placement<wbr>Constraint</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#TaskDefinitionPlacementConstraint">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#TaskDefinitionPlacementConstraint">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionPlacementConstraintArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionPlacementConstraintOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Expression</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster Query Language expression to apply to the constraint.
For more information, see [Cluster Query Language in the Amazon EC2 Container
Service Developer
Guide](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/cluster-query-language.html).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The proxy type. The default value is `APPMESH`. The only supported value is `APPMESH`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Expression</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Cluster Query Language expression to apply to the constraint.
For more information, see [Cluster Query Language in the Amazon EC2 Container
Service Developer
Guide](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/cluster-query-language.html).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The proxy type. The default value is `APPMESH`. The only supported value is `APPMESH`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>expression</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Cluster Query Language expression to apply to the constraint.
For more information, see [Cluster Query Language in the Amazon EC2 Container
Service Developer
Guide](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/cluster-query-language.html).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The proxy type. The default value is `APPMESH`. The only supported value is `APPMESH`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>expression</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Cluster Query Language expression to apply to the constraint.
For more information, see [Cluster Query Language in the Amazon EC2 Container
Service Developer
Guide](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/cluster-query-language.html).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The proxy type. The default value is `APPMESH`. The only supported value is `APPMESH`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Task<wbr>Definition<wbr>Proxy<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#TaskDefinitionProxyConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#TaskDefinitionProxyConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionProxyConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionProxyConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Container<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the container that will serve as the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string>?</span>
    </dt>
    <dd>{{% md %}}The set of network configuration parameters to provide the Container Network Interface (CNI) plugin, specified a key-value mapping.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The proxy type. The default value is `APPMESH`. The only supported value is `APPMESH`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Container<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the container that will serve as the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Properties</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}The set of network configuration parameters to provide the Container Network Interface (CNI) plugin, specified a key-value mapping.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The proxy type. The default value is `APPMESH`. The only supported value is `APPMESH`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>container<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the container that will serve as the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>properties</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}?</span>
    </dt>
    <dd>{{% md %}}The set of network configuration parameters to provide the Container Network Interface (CNI) plugin, specified a key-value mapping.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The proxy type. The default value is `APPMESH`. The only supported value is `APPMESH`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>container_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the container that will serve as the App Mesh proxy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>properties</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}The set of network configuration parameters to provide the Container Network Interface (CNI) plugin, specified a key-value mapping.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The proxy type. The default value is `APPMESH`. The only supported value is `APPMESH`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Task<wbr>Definition<wbr>Volume</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#TaskDefinitionVolume">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#TaskDefinitionVolume">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionVolumeArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionVolumeOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Volume<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolumedockervolumeconfiguration">Task<wbr>Definition<wbr>Volume<wbr>Docker<wbr>Volume<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Used to configure a docker volume
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Efs<wbr>Volume<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolumeefsvolumeconfiguration">Task<wbr>Definition<wbr>Volume<wbr>Efs<wbr>Volume<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Used to configure a EFS volume. Can be used only with an EC2 type task.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path on the host container instance that is presented to the container. If not set, ECS will create a nonpersistent data volume that starts empty and is deleted after the task has finished.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the volume. This name is referenced in the `sourceVolume`
parameter of container definition in the `mountPoints` section.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Docker<wbr>Volume<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolumedockervolumeconfiguration">*Task<wbr>Definition<wbr>Volume<wbr>Docker<wbr>Volume<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Used to configure a docker volume
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Efs<wbr>Volume<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolumeefsvolumeconfiguration">*Task<wbr>Definition<wbr>Volume<wbr>Efs<wbr>Volume<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Used to configure a EFS volume. Can be used only with an EC2 type task.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The path on the host container instance that is presented to the container. If not set, ECS will create a nonpersistent data volume that starts empty and is deleted after the task has finished.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the volume. This name is referenced in the `sourceVolume`
parameter of container definition in the `mountPoints` section.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>docker<wbr>Volume<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolumedockervolumeconfiguration">Task<wbr>Definition<wbr>Volume<wbr>Docker<wbr>Volume<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}Used to configure a docker volume
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>efs<wbr>Volume<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolumeefsvolumeconfiguration">Task<wbr>Definition<wbr>Volume<wbr>Efs<wbr>Volume<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}Used to configure a EFS volume. Can be used only with an EC2 type task.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path on the host container instance that is presented to the container. If not set, ECS will create a nonpersistent data volume that starts empty and is deleted after the task has finished.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the volume. This name is referenced in the `sourceVolume`
parameter of container definition in the `mountPoints` section.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>docker<wbr>Volume<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolumedockervolumeconfiguration">Dict[Task<wbr>Definition<wbr>Volume<wbr>Docker<wbr>Volume<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}Used to configure a docker volume
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>efs<wbr>Volume<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#taskdefinitionvolumeefsvolumeconfiguration">Dict[Task<wbr>Definition<wbr>Volume<wbr>Efs<wbr>Volume<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}Used to configure a EFS volume. Can be used only with an EC2 type task.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The path on the host container instance that is presented to the container. If not set, ECS will create a nonpersistent data volume that starts empty and is deleted after the task has finished.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the volume. This name is referenced in the `sourceVolume`
parameter of container definition in the `mountPoints` section.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Task<wbr>Definition<wbr>Volume<wbr>Docker<wbr>Volume<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#TaskDefinitionVolumeDockerVolumeConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#TaskDefinitionVolumeDockerVolumeConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionVolumeDockerVolumeConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionVolumeDockerVolumeConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Autoprovision</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If this value is `true`, the Docker volume is created if it does not already exist. *Note*: This field is only used if the scope is `shared`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Docker volume driver to use. The driver value must match the driver name provided by Docker because it is used for task placement.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Driver<wbr>Opts</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string>?</span>
    </dt>
    <dd>{{% md %}}A map of Docker driver specific options.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string>?</span>
    </dt>
    <dd>{{% md %}}A map of custom metadata to add to your Docker volume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The scope for the Docker volume, which determines its lifecycle, either `task` or `shared`.  Docker volumes that are scoped to a `task` are automatically provisioned when the task starts and destroyed when the task stops. Docker volumes that are `scoped` as shared persist after the task stops.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Autoprovision</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If this value is `true`, the Docker volume is created if it does not already exist. *Note*: This field is only used if the scope is `shared`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Docker volume driver to use. The driver value must match the driver name provided by Docker because it is used for task placement.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Driver<wbr>Opts</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A map of Docker driver specific options.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A map of custom metadata to add to your Docker volume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The scope for the Docker volume, which determines its lifecycle, either `task` or `shared`.  Docker volumes that are scoped to a `task` are automatically provisioned when the task starts and destroyed when the task stops. Docker volumes that are `scoped` as shared persist after the task stops.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>autoprovision</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If this value is `true`, the Docker volume is created if it does not already exist. *Note*: This field is only used if the scope is `shared`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Docker volume driver to use. The driver value must match the driver name provided by Docker because it is used for task placement.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>driver<wbr>Opts</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}?</span>
    </dt>
    <dd>{{% md %}}A map of Docker driver specific options.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}?</span>
    </dt>
    <dd>{{% md %}}A map of custom metadata to add to your Docker volume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The scope for the Docker volume, which determines its lifecycle, either `task` or `shared`.  Docker volumes that are scoped to a `task` are automatically provisioned when the task starts and destroyed when the task stops. Docker volumes that are `scoped` as shared persist after the task stops.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>autoprovision</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If this value is `true`, the Docker volume is created if it does not already exist. *Note*: This field is only used if the scope is `shared`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>driver</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Docker volume driver to use. The driver value must match the driver name provided by Docker because it is used for task placement.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>driver<wbr>Opts</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}A map of Docker driver specific options.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>labels</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}A map of custom metadata to add to your Docker volume.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The scope for the Docker volume, which determines its lifecycle, either `task` or `shared`.  Docker volumes that are scoped to a `task` are automatically provisioned when the task starts and destroyed when the task stops. Docker volumes that are `scoped` as shared persist after the task stops.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Task<wbr>Definition<wbr>Volume<wbr>Efs<wbr>Volume<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#TaskDefinitionVolumeEfsVolumeConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#TaskDefinitionVolumeEfsVolumeConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionVolumeEfsVolumeConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ecs?tab=doc#TaskDefinitionVolumeEfsVolumeConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>File<wbr>System<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the EFS File System.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Root<wbr>Directory</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path to mount on the host
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>File<wbr>System<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the EFS File System.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Root<wbr>Directory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The path to mount on the host
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>file<wbr>System<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the EFS File System.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>root<wbr>Directory</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The path to mount on the host
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>file_<wbr>system_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the EFS File System.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>root<wbr>Directory</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The path to mount on the host
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    <dt>Notes</dt>
	<dd>This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).</dd>
</dl>

