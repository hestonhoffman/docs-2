
---
title: "AlertCondition"
block_external_search_index: true
---



Use this resource to create and manage plugins alert conditions in New Relic.

## Terms

The `term` mapping supports the following arguments:

  * `duration` - (Required) In minutes, must be in the range of `5` to `120`, inclusive.
  * `operator` - (Optional) `above`, `below`, or `equal`.  Defaults to `equal`.
  * `priority` - (Optional) `critical` or `warning`.  Defaults to `critical`.
  * `threshold` - (Required) Must be 0 or greater.
  * `time_function` - (Required) `all` or `any`.

> This content is derived from https://github.com/terraform-providers/terraform-provider-newrelic/blob/master/website/docs/r/plugins_alert_condition.html.markdown.



## Create a AlertCondition Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/newrelic/plugins/#AlertCondition">AlertCondition</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/newrelic/plugins/#AlertConditionArgs">AlertConditionArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">AlertCondition</span><span class="p">(resource_name, opts=None, </span>enabled=None<span class="p">, </span>entities=None<span class="p">, </span>metric=None<span class="p">, </span>metric_description=None<span class="p">, </span>name=None<span class="p">, </span>plugin_guid=None<span class="p">, </span>plugin_id=None<span class="p">, </span>policy_id=None<span class="p">, </span>runbook_url=None<span class="p">, </span>terms=None<span class="p">, </span>value_function=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewAlertCondition<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/plugins?tab=doc#AlertConditionArgs">AlertConditionArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/plugins?tab=doc#AlertCondition">AlertCondition</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Newrelic/Pulumi.Newrelic.Plugins.AlertCondition.html">AlertCondition</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Newrelic/Pulumi.Newrelic.Plugins.AlertConditionArgs.html">AlertConditionArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<int></span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Metric<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Plugin<wbr>Guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Plugin<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Runbook<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">List&lt;Alert<wbr>Condition<wbr>Term<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
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
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]int</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Metric<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Plugin<wbr>Guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Plugin<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Runbook<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">[]Alert<wbr>Condition<wbr>Term</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
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
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">number[]</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>metric<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>plugin<wbr>Guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>plugin<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>runbook<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">Alert<wbr>Condition<wbr>Term[]</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
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
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Integer]</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>metric_<wbr>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>plugin_<wbr>guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>plugin_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>policy_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>runbook_<wbr>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">List[Alert<wbr>Condition<wbr>Term]</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value_<wbr>function</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## AlertCondition Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<int></span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metric<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Plugin<wbr>Guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Plugin<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Runbook<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">List&lt;Alert<wbr>Condition<wbr>Term&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]int</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metric<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Plugin<wbr>Guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Plugin<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Runbook<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">[]Alert<wbr>Condition<wbr>Term</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">number[]</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metric<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>plugin<wbr>Guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>plugin<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>runbook<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">Alert<wbr>Condition<wbr>Term[]</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Integer]</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metric_<wbr>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>plugin_<wbr>guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>plugin_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>policy_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>runbook_<wbr>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">List[Alert<wbr>Condition<wbr>Term]</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>value_<wbr>function</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing AlertCondition Resource

Get an existing AlertCondition resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/newrelic/plugins/#AlertConditionState">AlertConditionState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/newrelic/plugins/#AlertCondition">AlertCondition</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>enabled=None<span class="p">, </span>entities=None<span class="p">, </span>metric=None<span class="p">, </span>metric_description=None<span class="p">, </span>name=None<span class="p">, </span>plugin_guid=None<span class="p">, </span>plugin_id=None<span class="p">, </span>policy_id=None<span class="p">, </span>runbook_url=None<span class="p">, </span>terms=None<span class="p">, </span>value_function=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetAlertCondition<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/plugins?tab=doc#AlertConditionState">AlertConditionState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/plugins?tab=doc#AlertCondition">AlertCondition</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Newrelic/Pulumi.Newrelic.Plugins.AlertCondition.html">AlertCondition</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Newrelic/Pulumi.Newrelic.Plugins.AlertConditionState.html">AlertConditionState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<int>?</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metric<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Plugin<wbr>Guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Plugin<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Runbook<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">List&lt;Alert<wbr>Condition<wbr>Term<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
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
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]int</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metric<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Plugin<wbr>Guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Plugin<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Runbook<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">[]Alert<wbr>Condition<wbr>Term</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
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
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">number[]?</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metric<wbr>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>plugin<wbr>Guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>plugin<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>runbook<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">Alert<wbr>Condition<wbr>Term[]?</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
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
    <dd>{{% md %}}Whether or not this condition is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Integer]</span>
    </dt>
    <dd>{{% md %}}The plugin component IDs to target.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The plugin metric to evaluate.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metric_<wbr>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The metric description.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The title of the condition. Must be between 1 and 64 characters, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>plugin_<wbr>guid</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The GUID of the plugin which produces the metric.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>plugin_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the installed plugin instance which produces the metric.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>policy_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The ID of the policy where this condition should be used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>runbook_<wbr>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Runbook URL to display in notifications.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>terms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#alertconditionterm">List[Alert<wbr>Condition<wbr>Term]</a></span>
    </dt>
    <dd>{{% md %}}A list of terms for this condition. See Terms below for details.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value_<wbr>function</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The value function to apply to the metric data.  One of `min`, `max`, `average`, `sample_size`, `total`, or `percent`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Alert<wbr>Condition<wbr>Term</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/newrelic/types/input/#AlertConditionTerm">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/newrelic/types/output/#AlertConditionTerm">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/plugins?tab=doc#AlertConditionTermArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/plugins?tab=doc#AlertConditionTermOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Duration</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Operator</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Threshold</span>
        <span class="property-indicator"></span>
        <span class="property-type">double</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Time<wbr>Function</span>
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
        <span>Duration</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Operator</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Threshold</span>
        <span class="property-indicator"></span>
        <span class="property-type">float64</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Time<wbr>Function</span>
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
        <span>duration</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>operator</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>threshold</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>time<wbr>Function</span>
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
        <span>duration</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>operator</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>threshold</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>time<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-newrelic">https://github.com/pulumi/pulumi-newrelic</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

