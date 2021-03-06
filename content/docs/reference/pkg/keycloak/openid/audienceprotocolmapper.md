
---
title: "AudienceProtocolMapper"
block_external_search_index: true
---



## # keycloak.openid.AudienceProtocolMapper

Allows for creating and managing audience protocol mappers within
Keycloak. This mapper was added in Keycloak v4.6.0.Final.

Audience protocol mappers allow you add audiences to the `aud` claim
within issued tokens. The audience can be a custom string, or it can be
mapped to the ID of a pre-existing client.

### Example Usage (Client)

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as keycloak from "@pulumi/keycloak";

const realm = new keycloak.Realm("realm", {
    enabled: true,
    realm: "my-realm",
});
const openidClient = new keycloak.openid.Client("openid_client", {
    accessType: "CONFIDENTIAL",
    clientId: "test-client",
    enabled: true,
    realmId: realm.id,
    validRedirectUris: ["http://localhost:8080/openid-callback"],
});
const audienceMapper = new keycloak.openid.AudienceProtocolMapper("audience_mapper", {
    clientId: openidClient.id,
    includedCustomAudience: "foo",
    realmId: realm.id,
});
```

### Example Usage (Client Scope)

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as keycloak from "@pulumi/keycloak";

const realm = new keycloak.Realm("realm", {
    enabled: true,
    realm: "my-realm",
});
const clientScope = new keycloak.openid.ClientScope("client_scope", {
    realmId: realm.id,
});
const audienceMapper = new keycloak.openid.AudienceProtocolMapper("audience_mapper", {
    clientScopeId: clientScope.id,
    includedCustomAudience: "foo",
    realmId: realm.id,
});
```

### Argument Reference

The following arguments are supported:

- `realm_id` - (Required) The realm this protocol mapper exists within.
- `client_id` - (Required if `client_scope_id` is not specified) The client this protocol mapper is attached to.
- `client_scope_id` - (Required if `client_id` is not specified) The client scope this protocol mapper is attached to.
- `name` - (Required) The display name of this protocol mapper in the GUI.
- `included_client_audience` - (Required if `included_custom_audience` is not specified) A client ID to include within the token's `aud` claim.
- `included_custom_audience` - (Required if `included_client_audience` is not specified) A custom audience to include within the token's `aud` claim.
- `add_to_id_token` - (Optional) Indicates if the audience should be included in the `aud` claim for the id token. Defaults to `true`.
- `add_to_access_token` - (Optional) Indicates if the audience should be included in the `aud` claim for the id token. Defaults to `true`.

> This content is derived from https://github.com/mrparkers/terraform-provider-keycloak/blob/master/website/docs/r/keycloak_openid_audience_protocol_mapper.html.markdown.



## Create a AudienceProtocolMapper Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/keycloak/openid/#AudienceProtocolMapper">AudienceProtocolMapper</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/keycloak/openid/#AudienceProtocolMapperArgs">AudienceProtocolMapperArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">AudienceProtocolMapper</span><span class="p">(resource_name, opts=None, </span>add_to_access_token=None<span class="p">, </span>add_to_id_token=None<span class="p">, </span>client_id=None<span class="p">, </span>client_scope_id=None<span class="p">, </span>included_client_audience=None<span class="p">, </span>included_custom_audience=None<span class="p">, </span>name=None<span class="p">, </span>realm_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewAudienceProtocolMapper<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-keycloak/sdk/go/keycloak/openid?tab=doc#AudienceProtocolMapperArgs">AudienceProtocolMapperArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-keycloak/sdk/go/keycloak/openid?tab=doc#AudienceProtocolMapper">AudienceProtocolMapper</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Keycloak/Pulumi.Keycloak.Openid.AudienceProtocolMapper.html">AudienceProtocolMapper</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Keycloak/Pulumi.Keycloak.OpenId.AudienceProtocolMapperArgs.html">AudienceProtocolMapperArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Add<wbr>To<wbr>Access<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>To<wbr>Id<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Client<wbr>Scope<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Included<wbr>Client<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Included<wbr>Custom<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Realm<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>To<wbr>Access<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>To<wbr>Id<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Client<wbr>Scope<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Included<wbr>Client<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Included<wbr>Custom<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Realm<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>add<wbr>To<wbr>Access<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>add<wbr>To<wbr>Id<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>client<wbr>Scope<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>included<wbr>Client<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>included<wbr>Custom<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>realm<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>add_<wbr>to_<wbr>access_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>add_<wbr>to_<wbr>id_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>client_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>client_<wbr>scope_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>included_<wbr>client_<wbr>audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>included_<wbr>custom_<wbr>audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>realm_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## AudienceProtocolMapper Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Add<wbr>To<wbr>Access<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Add<wbr>To<wbr>Id<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Client<wbr>Scope<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Included<wbr>Client<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Included<wbr>Custom<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Realm<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Add<wbr>To<wbr>Access<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Add<wbr>To<wbr>Id<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Client<wbr>Scope<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Included<wbr>Client<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Included<wbr>Custom<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Realm<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>add<wbr>To<wbr>Access<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>add<wbr>To<wbr>Id<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>client<wbr>Scope<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>included<wbr>Client<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>included<wbr>Custom<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>realm<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>add_<wbr>to_<wbr>access_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>add_<wbr>to_<wbr>id_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>client_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>client_<wbr>scope_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>included_<wbr>client_<wbr>audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>included_<wbr>custom_<wbr>audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>realm_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing AudienceProtocolMapper Resource

Get an existing AudienceProtocolMapper resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/keycloak/openid/#AudienceProtocolMapperState">AudienceProtocolMapperState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/keycloak/openid/#AudienceProtocolMapper">AudienceProtocolMapper</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>add_to_access_token=None<span class="p">, </span>add_to_id_token=None<span class="p">, </span>client_id=None<span class="p">, </span>client_scope_id=None<span class="p">, </span>included_client_audience=None<span class="p">, </span>included_custom_audience=None<span class="p">, </span>name=None<span class="p">, </span>realm_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetAudienceProtocolMapper<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-keycloak/sdk/go/keycloak/openid?tab=doc#AudienceProtocolMapperState">AudienceProtocolMapperState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-keycloak/sdk/go/keycloak/openid?tab=doc#AudienceProtocolMapper">AudienceProtocolMapper</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Keycloak/Pulumi.Keycloak.Openid.AudienceProtocolMapper.html">AudienceProtocolMapper</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Keycloak/Pulumi.Keycloak.Openid.AudienceProtocolMapperState.html">AudienceProtocolMapperState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Add<wbr>To<wbr>Access<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>To<wbr>Id<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Client<wbr>Scope<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Included<wbr>Client<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Included<wbr>Custom<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Realm<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>To<wbr>Access<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Add<wbr>To<wbr>Id<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Client<wbr>Scope<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Included<wbr>Client<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Included<wbr>Custom<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Realm<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>add<wbr>To<wbr>Access<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>add<wbr>To<wbr>Id<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>client<wbr>Scope<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>included<wbr>Client<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>included<wbr>Custom<wbr>Audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>realm<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>add_<wbr>to_<wbr>access_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the access token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>add_<wbr>to_<wbr>id_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates if this claim should be added to the id token.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>client_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client. Cannot be used at the same time as client_scope_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>client_<wbr>scope_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The mapper's associated client scope. Cannot be used at the same time as client_id.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>included_<wbr>client_<wbr>audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A client ID to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>included_<wbr>custom_<wbr>audience</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A custom audience to include within the token's `aud` claim. Cannot be used with included_custom_audience
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A human-friendly name that will appear in the Keycloak console.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>realm_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The realm id where the associated client or client scope exists.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}











<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-keycloak">https://github.com/pulumi/pulumi-keycloak</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

