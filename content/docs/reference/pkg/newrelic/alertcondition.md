
---
title: "AlertCondition"
block_external_search_index: true
---



Use this resource to create and manage alert conditions for APM, Browser, and Mobile in New Relic.

## Terms

The `term` mapping supports the following arguments:

  * `duration` - (Required) In minutes, must be in the range of `5` to `120`, inclusive.
  * `operator` - (Optional) `above`, `below`, or `equal`.  Defaults to `equal`.
  * `priority` - (Optional) `critical` or `warning`.  Defaults to `critical`. Terms must include at least one `critical` priority term
  * `threshold` - (Required) Must be 0 or greater.
  * `time_function` - (Required) `all` or `any`.

> This content is derived from https://github.com/terraform-providers/terraform-provider-newrelic/blob/master/website/docs/r/alert_condition.html.markdown.



## Create a AlertCondition Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/newrelic/#AlertCondition">AlertCondition</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/newrelic/#AlertConditionArgs">AlertConditionArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">AlertCondition</span><span class="p">(resource_name, opts=None, </span>condition_scope=None<span class="p">, </span>enabled=None<span class="p">, </span>entities=None<span class="p">, </span>gc_metric=None<span class="p">, </span>metric=None<span class="p">, </span>name=None<span class="p">, </span>policy_id=None<span class="p">, </span>runbook_url=None<span class="p">, </span>terms=None<span class="p">, </span>type=None<span class="p">, </span>user_defined_metric=None<span class="p">, </span>user_defined_value_function=None<span class="p">, </span>violation_close_timer=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewAlertCondition<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/?tab=doc#AlertConditionArgs">AlertConditionArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/?tab=doc#AlertCondition">AlertCondition</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Newrelic/Pulumi.Newrelic..AlertCondition.html">AlertCondition</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Newrelic/Pulumi.Newrelic.AlertConditionArgs.html">AlertConditionArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Condition<wbr>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<int></span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gc<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Defined<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Defined<wbr>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Violation<wbr>Close<wbr>Timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Condition<wbr>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]int</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gc<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Defined<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Defined<wbr>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Violation<wbr>Close<wbr>Timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>condition<wbr>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">number[]</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gc<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Defined<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Defined<wbr>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>violation<wbr>Close<wbr>Timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>condition_<wbr>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Integer]</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gc_<wbr>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user_<wbr>defined_<wbr>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user_<wbr>defined_<wbr>value_<wbr>function</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>violation_<wbr>close_<wbr>timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## AlertCondition Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Condition<wbr>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<int></span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Gc<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User<wbr>Defined<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User<wbr>Defined<wbr>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Violation<wbr>Close<wbr>Timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Condition<wbr>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]int</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Gc<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User<wbr>Defined<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User<wbr>Defined<wbr>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Violation<wbr>Close<wbr>Timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>condition<wbr>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">number[]</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>gc<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user<wbr>Defined<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user<wbr>Defined<wbr>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>violation<wbr>Close<wbr>Timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>condition_<wbr>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Integer]</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>gc_<wbr>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user_<wbr>defined_<wbr>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user_<wbr>defined_<wbr>value_<wbr>function</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>violation_<wbr>close_<wbr>timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing AlertCondition Resource

Get an existing AlertCondition resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/newrelic/#AlertConditionState">AlertConditionState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/newrelic/#AlertCondition">AlertCondition</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>condition_scope=None<span class="p">, </span>enabled=None<span class="p">, </span>entities=None<span class="p">, </span>gc_metric=None<span class="p">, </span>metric=None<span class="p">, </span>name=None<span class="p">, </span>policy_id=None<span class="p">, </span>runbook_url=None<span class="p">, </span>terms=None<span class="p">, </span>type=None<span class="p">, </span>user_defined_metric=None<span class="p">, </span>user_defined_value_function=None<span class="p">, </span>violation_close_timer=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetAlertCondition<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/?tab=doc#AlertConditionState">AlertConditionState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/?tab=doc#AlertCondition">AlertCondition</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Newrelic/Pulumi.Newrelic..AlertCondition.html">AlertCondition</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Newrelic/Pulumi.Newrelic..AlertConditionState.html">AlertConditionState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Condition<wbr>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<int>?</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gc<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Defined<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Defined<wbr>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Violation<wbr>Close<wbr>Timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Condition<wbr>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]int</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gc<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Defined<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Defined<wbr>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Violation<wbr>Close<wbr>Timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>condition<wbr>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">number[]?</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gc<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Defined<wbr>Metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Defined<wbr>Value<wbr>Function</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>violation<wbr>Close<wbr>Timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>condition_<wbr>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}`application` or `instance`.  Choose `application` for most scenarios.  If you are using the JVM plugin in New Relic, the `instance` setting allows your condition to trigger [for specific app instances](https://docs.newrelic.com/docs/alerts/new-relic-alerts/defining-conditions/scope-alert-thresholds-specific-instances).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the condition is enabled or not. Defaults to true.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>entities</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Integer]</span>
    </dt>
    <dd>{{% md %}}The instance IDs associated with this condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gc_<wbr>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A valid Garbage Collection metric e.g. `GC/G1 Young Generation`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The metric field accepts parameters based on the `type` set. One of these metrics based on `type`:
* `apm_app_metric`
* `apdex`
* `error_percentage`
* `response_time_background`
* `response_time_web`
* `throughput_background`
* `throughput_web`
* `user_defined`
* `apm_kt_metric`
* `apdex`
* `error_count`
* `error_percentage`
* `response_time`
* `throughput`
* `browser_metric`
* `ajax_response_time`
* `ajax_throughput`
* `dom_processing`
* `end_user_apdex`
* `network`
* `page_rendering`
* `page_view_throughput`
* `page_views_with_js_errors`
* `request_queuing`
* `total_page_load`
* `user_defined`
* `web_application`
* `mobile_metric`
* `database`
* `images`
* `json`
* `mobile_crash_rate`
* `network_error_percentage`
* `network`
* `status_error_percentage`
* `user_defined`
* `view_loading`
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
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of condition. One of: `apm_app_metric`, `apm_kt_metric`, `browser_metric`, `mobile_metric`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user_<wbr>defined_<wbr>metric</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A custom metric to be evaluated.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user_<wbr>defined_<wbr>value_<wbr>function</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}One of: `average`, `min`, `max`, `total`, or `sample_size`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>violation_<wbr>close_<wbr>timer</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Automatically close instance-based violations, including JVM health metric violations, after the number of hours specified. Must be: `1`, `2`, `4`, `8`, `12` or `24`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Alert<wbr>Condition<wbr>Term</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/newrelic/types/input/#AlertConditionTerm">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/newrelic/types/output/#AlertConditionTerm">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/?tab=doc#AlertConditionTermArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-newrelic/sdk/go/newrelic/?tab=doc#AlertConditionTermOutput">output</a> API doc for this type.
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

