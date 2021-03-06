
---
title: "GetAgentSelf"
block_external_search_index: true
---



> **Warning:** The `consul..getAgentSelf` resource has been deprecated and will be removed
from a future release of the provider. Read the [upgrade instructions](https://www.terraform.io/docs/providers/consul/guides/upgrading.html#deprecation-of-consul_agent_self) for more information.


The `consul..getAgentSelf` data source returns
[configuration and status data](https://www.consul.io/docs/agent/http/agent.html#agent_self)
from the agent specified in the `provider`.

> This content is derived from https://github.com/terraform-providers/terraform-provider-consul/blob/master/website/docs/d/agent_self.html.markdown.





## Using GetAgentSelf

{{< chooser language "javascript,typescript,python,go,csharp" / >}}


{{% choosable language typescript %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getAgentSelf<span class="p">(</span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/consul/#GetAgentSelfResult">GetAgentSelfResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_agent_self(</span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupAgentSelf<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-consul/sdk/go/consul/?tab=doc#LookupAgentSelfResult">LookupAgentSelfResult</a></span>, error)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetAgentSelf </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Consul/Pulumi.Consul.GetAgentSelfResult.html">GetAgentSelfResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span>? <span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}




## GetAgentSelf Result

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Acl<wbr>Datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Default<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Disabled<wbr>Ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Down<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Enforce08Semantics</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Advertise<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Advertise<wbr>Addr<wbr>Wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Advertise<wbr>Addrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Atlas<wbr>Join</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Bind<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Bootstrap<wbr>Expect</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Bootstrap<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Check<wbr>Deregister<wbr>Interval<wbr>Min</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Check<wbr>Reap<wbr>Interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Check<wbr>Update<wbr>Interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Client<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Data<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dev<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dns</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}A map of DNS configuration attributes.  See below for details on the
contents of the `dns` attribute.
* [`dns_recursors`](https://www.consul.io/docs/agent/options.html#recursors) - A
list of all DNS recursors.
* [`data_dir`](https://www.consul.io/docs/agent/options.html#_data_dir)
* [`datacenter`](https://www.consul.io/docs/agent/options.html#_datacenter)
* [`dev_mode`](https://www.consul.io/docs/agent/options.html#_dev)
* [`domain`](https://www.consul.io/docs/agent/options.html#_domain)
* [`enable_anonymous_signature`](https://www.consul.io/docs/agent/options.html#disable_anonymous_signature)
* `enable_coordinates`
* [`enable_debug`](https://www.consul.io/docs/agent/options.html#enable_debug)
* [`enable_remote_exec`](https://www.consul.io/docs/agent/options.html#disable_remote_exec)
* [`enable_syslog`](https://www.consul.io/docs/agent/options.html#_syslog)
* [`enable_ui`](https://www.consul.io/docs/agent/options.html#_ui)
* [`enable_update_check`](https://www.consul.io/docs/agent/options.html#disable_update_check)
* [`id`](https://www.consul.io/docs/agent/options.html#_node_id)
* [`leave_on_int`](https://www.consul.io/docs/agent/options.html#skip_leave_on_interrupt)
* [`leave_on_term`](https://www.consul.io/docs/agent/options.html#leave_on_terminate)
* [`log_level`](https://www.consul.io/docs/agent/options.html#_log_level)
* [`name`](https://www.consul.io/docs/agent/options.html#_node)
* [`performance`](https://www.consul.io/docs/agent/options.html#performance)
* [`pid_file`](https://www.consul.io/docs/agent/options.html#_pid_file)
* [`ports`](https://www.consul.io/docs/agent/options.html#ports)
* [`protocol_version`](https://www.consul.io/docs/agent/options.html#_protocol)
* [`reconnect_timeout_lan`](https://www.consul.io/docs/agent/options.html#reconnect_timeout)
* [`reconnect_timeout_wan`](https://www.consul.io/docs/agent/options.html#reconnect_timeout_wan)
* [`rejoin_after_leave`](https://www.consul.io/docs/agent/options.html#_rejoin)
* [`retry_join`](https://www.consul.io/docs/agent/options.html#retry_join)
* [`retry_join_ec2`](https://www.consul.io/docs/agent/options.html#retry_join_ec2) -
A map of EC2 retry attributes.  See below for details on the available
information.
* [`retry_join_gce`](https://www.consul.io/docs/agent/options.html#retry_join_gce) -
A map of GCE retry attributes.  See below for details on the available
information.
* [`retry_join_wan`](https://www.consul.io/docs/agent/options.html#_retry_join_wan)
* [`retry_max_attempts`](https://www.consul.io/docs/agent/options.html#_retry_max)
* [`retry_max_attempts_wan`](https://www.consul.io/docs/agent/options.html#_retry_max_wan)
* [`serf_lan_bind_addr`](https://www.consul.io/docs/agent/options.html#_serf_lan_bind)
* [`serf_wan_bind_addr`](https://www.consul.io/docs/agent/options.html#_serf_wan_bind)
* [`server_mode`](https://www.consul.io/docs/agent/options.html#_server)
* [`server_name`](https://www.consul.io/docs/agent/options.html#server_name)
* [`session_ttl_min`](https://www.consul.io/docs/agent/options.html#session_ttl_min)
* [`start_join`](https://www.consul.io/docs/agent/options.html#start_join)
* [`start_join_wan`](https://www.consul.io/docs/agent/options.html#start_join_wan)
* [`syslog_facility`](https://www.consul.io/docs/agent/options.html#syslog_facility)
* [`tls_ca_file`](https://www.consul.io/docs/agent/options.html#ca_file)
* [`tls_cert_file`](https://www.consul.io/docs/agent/options.html#cert_file)
* [`tls_key_file`](https://www.consul.io/docs/agent/options.html#key_file)
* [`tls_min_version`](https://www.consul.io/docs/agent/options.html#tls_min_version)
* [`tls_verify_incoming`](https://www.consul.io/docs/agent/options.html#verify_incoming)
* [`tls_verify_outgoing`](https://www.consul.io/docs/agent/options.html#verify_outgoing)
* [`tls_verify_server_hostname`](https://www.consul.io/docs/agent/options.html#verify_server_hostname)
* [`tagged_addresses`](https://www.consul.io/docs/agent/options.html#translate_wan_addrs)
* [`telemetry`](https://www.consul.io/docs/agent/options.html#telemetry) - A map
of telemetry configuration.
* [`translate_wan_addrs`](https://www.consul.io/docs/agent/options.html#translate_wan_addrs)
* [`ui_dir`](https://www.consul.io/docs/agent/options.html#ui_dir)
* [`unix_sockets`](https://www.consul.io/docs/agent/options.html#unix_sockets)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dns<wbr>Recursors</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Anonymous<wbr>Signature</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Coordinates</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Debug</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Remote<wbr>Exec</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Syslog</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Ui</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Update<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Leave<wbr>On<wbr>Int</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Leave<wbr>On<wbr>Term</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Log<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
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
        <span>Performance</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Pid<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, int></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Protocol<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Reconnect<wbr>Timeout<wbr>Lan</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Reconnect<wbr>Timeout<wbr>Wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Rejoin<wbr>After<wbr>Leave</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Join<wbr>Ec2</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Join<wbr>Gce</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Join<wbr>Wans</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Joins</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Max<wbr>Attempts</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Max<wbr>Attempts<wbr>Wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Serf<wbr>Lan<wbr>Bind<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Serf<wbr>Wan<wbr>Bind<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Server<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Server<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Session<wbr>Ttl<wbr>Min</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Start<wbr>Join<wbr>Wans</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Start<wbr>Joins</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Syslog<wbr>Facility</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tagged<wbr>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Telemetry</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Ca<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Cert<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Key<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Min<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Verify<wbr>Incoming</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Verify<wbr>Outgoing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Verify<wbr>Server<wbr>Hostname</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Translate<wbr>Wan<wbr>Addrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ui<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Unix<wbr>Sockets</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, string></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The version of the Consul agent.
* `version_prerelease`
* `version_revision`
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version<wbr>Prerelease</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version<wbr>Revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Acl<wbr>Datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Default<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Disabled<wbr>Ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Down<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Enforce08Semantics</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Acl<wbr>Ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Advertise<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Advertise<wbr>Addr<wbr>Wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Advertise<wbr>Addrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Atlas<wbr>Join</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Bind<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Bootstrap<wbr>Expect</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Bootstrap<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Check<wbr>Deregister<wbr>Interval<wbr>Min</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Check<wbr>Reap<wbr>Interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Check<wbr>Update<wbr>Interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Client<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Data<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dev<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dns</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A map of DNS configuration attributes.  See below for details on the
contents of the `dns` attribute.
* [`dns_recursors`](https://www.consul.io/docs/agent/options.html#recursors) - A
list of all DNS recursors.
* [`data_dir`](https://www.consul.io/docs/agent/options.html#_data_dir)
* [`datacenter`](https://www.consul.io/docs/agent/options.html#_datacenter)
* [`dev_mode`](https://www.consul.io/docs/agent/options.html#_dev)
* [`domain`](https://www.consul.io/docs/agent/options.html#_domain)
* [`enable_anonymous_signature`](https://www.consul.io/docs/agent/options.html#disable_anonymous_signature)
* `enable_coordinates`
* [`enable_debug`](https://www.consul.io/docs/agent/options.html#enable_debug)
* [`enable_remote_exec`](https://www.consul.io/docs/agent/options.html#disable_remote_exec)
* [`enable_syslog`](https://www.consul.io/docs/agent/options.html#_syslog)
* [`enable_ui`](https://www.consul.io/docs/agent/options.html#_ui)
* [`enable_update_check`](https://www.consul.io/docs/agent/options.html#disable_update_check)
* [`id`](https://www.consul.io/docs/agent/options.html#_node_id)
* [`leave_on_int`](https://www.consul.io/docs/agent/options.html#skip_leave_on_interrupt)
* [`leave_on_term`](https://www.consul.io/docs/agent/options.html#leave_on_terminate)
* [`log_level`](https://www.consul.io/docs/agent/options.html#_log_level)
* [`name`](https://www.consul.io/docs/agent/options.html#_node)
* [`performance`](https://www.consul.io/docs/agent/options.html#performance)
* [`pid_file`](https://www.consul.io/docs/agent/options.html#_pid_file)
* [`ports`](https://www.consul.io/docs/agent/options.html#ports)
* [`protocol_version`](https://www.consul.io/docs/agent/options.html#_protocol)
* [`reconnect_timeout_lan`](https://www.consul.io/docs/agent/options.html#reconnect_timeout)
* [`reconnect_timeout_wan`](https://www.consul.io/docs/agent/options.html#reconnect_timeout_wan)
* [`rejoin_after_leave`](https://www.consul.io/docs/agent/options.html#_rejoin)
* [`retry_join`](https://www.consul.io/docs/agent/options.html#retry_join)
* [`retry_join_ec2`](https://www.consul.io/docs/agent/options.html#retry_join_ec2) -
A map of EC2 retry attributes.  See below for details on the available
information.
* [`retry_join_gce`](https://www.consul.io/docs/agent/options.html#retry_join_gce) -
A map of GCE retry attributes.  See below for details on the available
information.
* [`retry_join_wan`](https://www.consul.io/docs/agent/options.html#_retry_join_wan)
* [`retry_max_attempts`](https://www.consul.io/docs/agent/options.html#_retry_max)
* [`retry_max_attempts_wan`](https://www.consul.io/docs/agent/options.html#_retry_max_wan)
* [`serf_lan_bind_addr`](https://www.consul.io/docs/agent/options.html#_serf_lan_bind)
* [`serf_wan_bind_addr`](https://www.consul.io/docs/agent/options.html#_serf_wan_bind)
* [`server_mode`](https://www.consul.io/docs/agent/options.html#_server)
* [`server_name`](https://www.consul.io/docs/agent/options.html#server_name)
* [`session_ttl_min`](https://www.consul.io/docs/agent/options.html#session_ttl_min)
* [`start_join`](https://www.consul.io/docs/agent/options.html#start_join)
* [`start_join_wan`](https://www.consul.io/docs/agent/options.html#start_join_wan)
* [`syslog_facility`](https://www.consul.io/docs/agent/options.html#syslog_facility)
* [`tls_ca_file`](https://www.consul.io/docs/agent/options.html#ca_file)
* [`tls_cert_file`](https://www.consul.io/docs/agent/options.html#cert_file)
* [`tls_key_file`](https://www.consul.io/docs/agent/options.html#key_file)
* [`tls_min_version`](https://www.consul.io/docs/agent/options.html#tls_min_version)
* [`tls_verify_incoming`](https://www.consul.io/docs/agent/options.html#verify_incoming)
* [`tls_verify_outgoing`](https://www.consul.io/docs/agent/options.html#verify_outgoing)
* [`tls_verify_server_hostname`](https://www.consul.io/docs/agent/options.html#verify_server_hostname)
* [`tagged_addresses`](https://www.consul.io/docs/agent/options.html#translate_wan_addrs)
* [`telemetry`](https://www.consul.io/docs/agent/options.html#telemetry) - A map
of telemetry configuration.
* [`translate_wan_addrs`](https://www.consul.io/docs/agent/options.html#translate_wan_addrs)
* [`ui_dir`](https://www.consul.io/docs/agent/options.html#ui_dir)
* [`unix_sockets`](https://www.consul.io/docs/agent/options.html#unix_sockets)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dns<wbr>Recursors</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Anonymous<wbr>Signature</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Coordinates</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Debug</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Remote<wbr>Exec</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Syslog</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Ui</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enable<wbr>Update<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Leave<wbr>On<wbr>Int</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Leave<wbr>On<wbr>Term</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Log<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
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
        <span>Performance</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Pid<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Protocol<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Reconnect<wbr>Timeout<wbr>Lan</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Reconnect<wbr>Timeout<wbr>Wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Rejoin<wbr>After<wbr>Leave</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Join<wbr>Ec2</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Join<wbr>Gce</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Join<wbr>Wans</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Joins</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Max<wbr>Attempts</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Retry<wbr>Max<wbr>Attempts<wbr>Wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Serf<wbr>Lan<wbr>Bind<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Serf<wbr>Wan<wbr>Bind<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Server<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Server<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Session<wbr>Ttl<wbr>Min</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Start<wbr>Join<wbr>Wans</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Start<wbr>Joins</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Syslog<wbr>Facility</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tagged<wbr>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Telemetry</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Ca<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Cert<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Key<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Min<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Verify<wbr>Incoming</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Verify<wbr>Outgoing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tls<wbr>Verify<wbr>Server<wbr>Hostname</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Translate<wbr>Wan<wbr>Addrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Ui<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Unix<wbr>Sockets</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The version of the Consul agent.
* `version_prerelease`
* `version_revision`
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version<wbr>Prerelease</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Version<wbr>Revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>acl<wbr>Datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl<wbr>Default<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl<wbr>Disabled<wbr>Ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl<wbr>Down<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl<wbr>Enforce08Semantics</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl<wbr>Ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>advertise<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>advertise<wbr>Addr<wbr>Wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>advertise<wbr>Addrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>atlas<wbr>Join</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>bind<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>bootstrap<wbr>Expect</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>bootstrap<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>check<wbr>Deregister<wbr>Interval<wbr>Min</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>check<wbr>Reap<wbr>Interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>check<wbr>Update<wbr>Interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>client<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>data<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dev<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dns</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}A map of DNS configuration attributes.  See below for details on the
contents of the `dns` attribute.
* [`dns_recursors`](https://www.consul.io/docs/agent/options.html#recursors) - A
list of all DNS recursors.
* [`data_dir`](https://www.consul.io/docs/agent/options.html#_data_dir)
* [`datacenter`](https://www.consul.io/docs/agent/options.html#_datacenter)
* [`dev_mode`](https://www.consul.io/docs/agent/options.html#_dev)
* [`domain`](https://www.consul.io/docs/agent/options.html#_domain)
* [`enable_anonymous_signature`](https://www.consul.io/docs/agent/options.html#disable_anonymous_signature)
* `enable_coordinates`
* [`enable_debug`](https://www.consul.io/docs/agent/options.html#enable_debug)
* [`enable_remote_exec`](https://www.consul.io/docs/agent/options.html#disable_remote_exec)
* [`enable_syslog`](https://www.consul.io/docs/agent/options.html#_syslog)
* [`enable_ui`](https://www.consul.io/docs/agent/options.html#_ui)
* [`enable_update_check`](https://www.consul.io/docs/agent/options.html#disable_update_check)
* [`id`](https://www.consul.io/docs/agent/options.html#_node_id)
* [`leave_on_int`](https://www.consul.io/docs/agent/options.html#skip_leave_on_interrupt)
* [`leave_on_term`](https://www.consul.io/docs/agent/options.html#leave_on_terminate)
* [`log_level`](https://www.consul.io/docs/agent/options.html#_log_level)
* [`name`](https://www.consul.io/docs/agent/options.html#_node)
* [`performance`](https://www.consul.io/docs/agent/options.html#performance)
* [`pid_file`](https://www.consul.io/docs/agent/options.html#_pid_file)
* [`ports`](https://www.consul.io/docs/agent/options.html#ports)
* [`protocol_version`](https://www.consul.io/docs/agent/options.html#_protocol)
* [`reconnect_timeout_lan`](https://www.consul.io/docs/agent/options.html#reconnect_timeout)
* [`reconnect_timeout_wan`](https://www.consul.io/docs/agent/options.html#reconnect_timeout_wan)
* [`rejoin_after_leave`](https://www.consul.io/docs/agent/options.html#_rejoin)
* [`retry_join`](https://www.consul.io/docs/agent/options.html#retry_join)
* [`retry_join_ec2`](https://www.consul.io/docs/agent/options.html#retry_join_ec2) -
A map of EC2 retry attributes.  See below for details on the available
information.
* [`retry_join_gce`](https://www.consul.io/docs/agent/options.html#retry_join_gce) -
A map of GCE retry attributes.  See below for details on the available
information.
* [`retry_join_wan`](https://www.consul.io/docs/agent/options.html#_retry_join_wan)
* [`retry_max_attempts`](https://www.consul.io/docs/agent/options.html#_retry_max)
* [`retry_max_attempts_wan`](https://www.consul.io/docs/agent/options.html#_retry_max_wan)
* [`serf_lan_bind_addr`](https://www.consul.io/docs/agent/options.html#_serf_lan_bind)
* [`serf_wan_bind_addr`](https://www.consul.io/docs/agent/options.html#_serf_wan_bind)
* [`server_mode`](https://www.consul.io/docs/agent/options.html#_server)
* [`server_name`](https://www.consul.io/docs/agent/options.html#server_name)
* [`session_ttl_min`](https://www.consul.io/docs/agent/options.html#session_ttl_min)
* [`start_join`](https://www.consul.io/docs/agent/options.html#start_join)
* [`start_join_wan`](https://www.consul.io/docs/agent/options.html#start_join_wan)
* [`syslog_facility`](https://www.consul.io/docs/agent/options.html#syslog_facility)
* [`tls_ca_file`](https://www.consul.io/docs/agent/options.html#ca_file)
* [`tls_cert_file`](https://www.consul.io/docs/agent/options.html#cert_file)
* [`tls_key_file`](https://www.consul.io/docs/agent/options.html#key_file)
* [`tls_min_version`](https://www.consul.io/docs/agent/options.html#tls_min_version)
* [`tls_verify_incoming`](https://www.consul.io/docs/agent/options.html#verify_incoming)
* [`tls_verify_outgoing`](https://www.consul.io/docs/agent/options.html#verify_outgoing)
* [`tls_verify_server_hostname`](https://www.consul.io/docs/agent/options.html#verify_server_hostname)
* [`tagged_addresses`](https://www.consul.io/docs/agent/options.html#translate_wan_addrs)
* [`telemetry`](https://www.consul.io/docs/agent/options.html#telemetry) - A map
of telemetry configuration.
* [`translate_wan_addrs`](https://www.consul.io/docs/agent/options.html#translate_wan_addrs)
* [`ui_dir`](https://www.consul.io/docs/agent/options.html#ui_dir)
* [`unix_sockets`](https://www.consul.io/docs/agent/options.html#unix_sockets)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dns<wbr>Recursors</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Anonymous<wbr>Signature</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Coordinates</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Debug</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Remote<wbr>Exec</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Syslog</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Ui</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable<wbr>Update<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>leave<wbr>On<wbr>Int</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>leave<wbr>On<wbr>Term</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>log<wbr>Level</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
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
        <span>performance</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>pid<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ports</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: number}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>protocol<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>reconnect<wbr>Timeout<wbr>Lan</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>reconnect<wbr>Timeout<wbr>Wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>rejoin<wbr>After<wbr>Leave</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry<wbr>Join<wbr>Ec2</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry<wbr>Join<wbr>Gce</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry<wbr>Join<wbr>Wans</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry<wbr>Joins</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry<wbr>Max<wbr>Attempts</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry<wbr>Max<wbr>Attempts<wbr>Wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>serf<wbr>Lan<wbr>Bind<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>serf<wbr>Wan<wbr>Bind<wbr>Addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>server<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>server<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>session<wbr>Ttl<wbr>Min</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>start<wbr>Join<wbr>Wans</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>start<wbr>Joins</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>syslog<wbr>Facility</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tagged<wbr>Addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>telemetry</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls<wbr>Ca<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls<wbr>Cert<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls<wbr>Key<wbr>File</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls<wbr>Min<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls<wbr>Verify<wbr>Incoming</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls<wbr>Verify<wbr>Outgoing</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls<wbr>Verify<wbr>Server<wbr>Hostname</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>translate<wbr>Wan<wbr>Addrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ui<wbr>Dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>unix<wbr>Sockets</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The version of the Consul agent.
* `version_prerelease`
* `version_revision`
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version<wbr>Prerelease</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version<wbr>Revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>acl_<wbr>datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl_<wbr>default_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl_<wbr>disabled_<wbr>ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl_<wbr>down_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl_<wbr>enforce08_<wbr>semantics</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>acl_<wbr>ttl</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>advertise_<wbr>addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>advertise_<wbr>addr_<wbr>wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>advertise_<wbr>addrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>atlas_<wbr>join</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>bind_<wbr>addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>bootstrap_<wbr>expect</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>bootstrap_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>check_<wbr>deregister_<wbr>interval_<wbr>min</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>check_<wbr>reap_<wbr>interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>check_<wbr>update_<wbr>interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>client_<wbr>addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>data_<wbr>dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>datacenter</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dev_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dns</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}A map of DNS configuration attributes.  See below for details on the
contents of the `dns` attribute.
* [`dns_recursors`](https://www.consul.io/docs/agent/options.html#recursors) - A
list of all DNS recursors.
* [`data_dir`](https://www.consul.io/docs/agent/options.html#_data_dir)
* [`datacenter`](https://www.consul.io/docs/agent/options.html#_datacenter)
* [`dev_mode`](https://www.consul.io/docs/agent/options.html#_dev)
* [`domain`](https://www.consul.io/docs/agent/options.html#_domain)
* [`enable_anonymous_signature`](https://www.consul.io/docs/agent/options.html#disable_anonymous_signature)
* `enable_coordinates`
* [`enable_debug`](https://www.consul.io/docs/agent/options.html#enable_debug)
* [`enable_remote_exec`](https://www.consul.io/docs/agent/options.html#disable_remote_exec)
* [`enable_syslog`](https://www.consul.io/docs/agent/options.html#_syslog)
* [`enable_ui`](https://www.consul.io/docs/agent/options.html#_ui)
* [`enable_update_check`](https://www.consul.io/docs/agent/options.html#disable_update_check)
* [`id`](https://www.consul.io/docs/agent/options.html#_node_id)
* [`leave_on_int`](https://www.consul.io/docs/agent/options.html#skip_leave_on_interrupt)
* [`leave_on_term`](https://www.consul.io/docs/agent/options.html#leave_on_terminate)
* [`log_level`](https://www.consul.io/docs/agent/options.html#_log_level)
* [`name`](https://www.consul.io/docs/agent/options.html#_node)
* [`performance`](https://www.consul.io/docs/agent/options.html#performance)
* [`pid_file`](https://www.consul.io/docs/agent/options.html#_pid_file)
* [`ports`](https://www.consul.io/docs/agent/options.html#ports)
* [`protocol_version`](https://www.consul.io/docs/agent/options.html#_protocol)
* [`reconnect_timeout_lan`](https://www.consul.io/docs/agent/options.html#reconnect_timeout)
* [`reconnect_timeout_wan`](https://www.consul.io/docs/agent/options.html#reconnect_timeout_wan)
* [`rejoin_after_leave`](https://www.consul.io/docs/agent/options.html#_rejoin)
* [`retry_join`](https://www.consul.io/docs/agent/options.html#retry_join)
* [`retry_join_ec2`](https://www.consul.io/docs/agent/options.html#retry_join_ec2) -
A map of EC2 retry attributes.  See below for details on the available
information.
* [`retry_join_gce`](https://www.consul.io/docs/agent/options.html#retry_join_gce) -
A map of GCE retry attributes.  See below for details on the available
information.
* [`retry_join_wan`](https://www.consul.io/docs/agent/options.html#_retry_join_wan)
* [`retry_max_attempts`](https://www.consul.io/docs/agent/options.html#_retry_max)
* [`retry_max_attempts_wan`](https://www.consul.io/docs/agent/options.html#_retry_max_wan)
* [`serf_lan_bind_addr`](https://www.consul.io/docs/agent/options.html#_serf_lan_bind)
* [`serf_wan_bind_addr`](https://www.consul.io/docs/agent/options.html#_serf_wan_bind)
* [`server_mode`](https://www.consul.io/docs/agent/options.html#_server)
* [`server_name`](https://www.consul.io/docs/agent/options.html#server_name)
* [`session_ttl_min`](https://www.consul.io/docs/agent/options.html#session_ttl_min)
* [`start_join`](https://www.consul.io/docs/agent/options.html#start_join)
* [`start_join_wan`](https://www.consul.io/docs/agent/options.html#start_join_wan)
* [`syslog_facility`](https://www.consul.io/docs/agent/options.html#syslog_facility)
* [`tls_ca_file`](https://www.consul.io/docs/agent/options.html#ca_file)
* [`tls_cert_file`](https://www.consul.io/docs/agent/options.html#cert_file)
* [`tls_key_file`](https://www.consul.io/docs/agent/options.html#key_file)
* [`tls_min_version`](https://www.consul.io/docs/agent/options.html#tls_min_version)
* [`tls_verify_incoming`](https://www.consul.io/docs/agent/options.html#verify_incoming)
* [`tls_verify_outgoing`](https://www.consul.io/docs/agent/options.html#verify_outgoing)
* [`tls_verify_server_hostname`](https://www.consul.io/docs/agent/options.html#verify_server_hostname)
* [`tagged_addresses`](https://www.consul.io/docs/agent/options.html#translate_wan_addrs)
* [`telemetry`](https://www.consul.io/docs/agent/options.html#telemetry) - A map
of telemetry configuration.
* [`translate_wan_addrs`](https://www.consul.io/docs/agent/options.html#translate_wan_addrs)
* [`ui_dir`](https://www.consul.io/docs/agent/options.html#ui_dir)
* [`unix_sockets`](https://www.consul.io/docs/agent/options.html#unix_sockets)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dns_<wbr>recursors</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>anonymous_<wbr>signature</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>coordinates</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>debug</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>remote_<wbr>exec</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>syslog</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>ui</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enable_<wbr>update_<wbr>check</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>leave_<wbr>on_<wbr>int</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>leave_<wbr>on_<wbr>term</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>log_<wbr>level</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
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
        <span>performance</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>pid_<wbr>file</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ports</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Integer]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>protocol_<wbr>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>reconnect_<wbr>timeout_<wbr>lan</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>reconnect_<wbr>timeout_<wbr>wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>rejoin_<wbr>after_<wbr>leave</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry_<wbr>join_<wbr>ec2</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry_<wbr>join_<wbr>gce</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry_<wbr>join_<wbr>wans</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry_<wbr>joins</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry_<wbr>max_<wbr>attempts</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>retry_<wbr>max_<wbr>attempts_<wbr>wan</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>serf_<wbr>lan_<wbr>bind_<wbr>addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>serf_<wbr>wan_<wbr>bind_<wbr>addr</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>server_<wbr>mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>server_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>session_<wbr>ttl_<wbr>min</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>start_<wbr>join_<wbr>wans</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>start_<wbr>joins</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>syslog_<wbr>facility</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tagged_<wbr>addresses</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>telemetry</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls_<wbr>ca_<wbr>file</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls_<wbr>cert_<wbr>file</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls_<wbr>key_<wbr>file</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls_<wbr>min_<wbr>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls_<wbr>verify_<wbr>incoming</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls_<wbr>verify_<wbr>outgoing</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tls_<wbr>verify_<wbr>server_<wbr>hostname</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>translate_<wbr>wan_<wbr>addrs</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>ui_<wbr>dir</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>unix_<wbr>sockets</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The version of the Consul agent.
* `version_prerelease`
* `version_revision`
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version_<wbr>prerelease</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>version_<wbr>revision</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}







