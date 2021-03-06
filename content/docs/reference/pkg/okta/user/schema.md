
---
title: "Schema"
block_external_search_index: true
---



Creates a User Schema property.

This resource allows you to create and configure a custom user schema property.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as okta from "@pulumi/okta";

const example = new okta.user.Schema("example", {
    description: "My custom property name",
    index: "customPropertyName",
    master: "OKTA",
    scope: "SELF",
    title: "customPropertyName",
    type: "string",
});
```

> This content is derived from https://github.com/articulate/terraform-provider-okta/blob/master/website/docs/r/user_schema.html.markdown.



## Create a Schema Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/user/#Schema">Schema</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/user/#SchemaArgs">SchemaArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Schema</span><span class="p">(resource_name, opts=None, </span>array_enums=None<span class="p">, </span>array_one_ofs=None<span class="p">, </span>array_type=None<span class="p">, </span>description=None<span class="p">, </span>enums=None<span class="p">, </span>external_name=None<span class="p">, </span>index=None<span class="p">, </span>master=None<span class="p">, </span>max_length=None<span class="p">, </span>min_length=None<span class="p">, </span>one_ofs=None<span class="p">, </span>permissions=None<span class="p">, </span>required=None<span class="p">, </span>scope=None<span class="p">, </span>title=None<span class="p">, </span>type=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewSchema<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/user?tab=doc#SchemaArgs">SchemaArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/user?tab=doc#Schema">Schema</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.User.Schema.html">Schema</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.User.SchemaArgs.html">SchemaArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Array<wbr>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">List&lt;Schema<wbr>Array<wbr>One<wbr>Of<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>External<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Index</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">List&lt;Schema<wbr>One<wbr>Of<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">[]Schema<wbr>Array<wbr>One<wbr>Of</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>External<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Index</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">[]Schema<wbr>One<wbr>Of</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>array<wbr>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>array<wbr>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">Schema<wbr>Array<wbr>One<wbr>Of[]?</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>array<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>external<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>index</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>one<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">Schema<wbr>One<wbr>Of[]?</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>array_<wbr>enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>array_<wbr>one_<wbr>ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">List[Schema<wbr>Array<wbr>One<wbr>Of]</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>array_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>external_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>index</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>length</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min_<wbr>length</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>one_<wbr>ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">List[Schema<wbr>One<wbr>Of]</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Schema Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Array<wbr>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Array<wbr>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">List&lt;Schema<wbr>Array<wbr>One<wbr>Of&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Array<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>External<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Index</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">List&lt;Schema<wbr>One<wbr>Of&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Array<wbr>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Array<wbr>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">[]Schema<wbr>Array<wbr>One<wbr>Of</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Array<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>External<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Index</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">[]Schema<wbr>One<wbr>Of</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>array<wbr>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>array<wbr>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">Schema<wbr>Array<wbr>One<wbr>Of[]?</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>array<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>external<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>index</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>master</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>one<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">Schema<wbr>One<wbr>Of[]?</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>array_<wbr>enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>array_<wbr>one_<wbr>ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">List[Schema<wbr>Array<wbr>One<wbr>Of]</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>array_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>external_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>index</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>master</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>max_<wbr>length</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>min_<wbr>length</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>one_<wbr>ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">List[Schema<wbr>One<wbr>Of]</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Schema Resource

Get an existing Schema resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/user/#SchemaState">SchemaState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/user/#Schema">Schema</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>array_enums=None<span class="p">, </span>array_one_ofs=None<span class="p">, </span>array_type=None<span class="p">, </span>description=None<span class="p">, </span>enums=None<span class="p">, </span>external_name=None<span class="p">, </span>index=None<span class="p">, </span>master=None<span class="p">, </span>max_length=None<span class="p">, </span>min_length=None<span class="p">, </span>one_ofs=None<span class="p">, </span>permissions=None<span class="p">, </span>required=None<span class="p">, </span>scope=None<span class="p">, </span>title=None<span class="p">, </span>type=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetSchema<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/user?tab=doc#SchemaState">SchemaState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/user?tab=doc#Schema">Schema</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.User.Schema.html">Schema</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.User.SchemaState.html">SchemaState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Array<wbr>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">List&lt;Schema<wbr>Array<wbr>One<wbr>Of<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>External<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Index</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">List&lt;Schema<wbr>One<wbr>Of<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">[]Schema<wbr>Array<wbr>One<wbr>Of</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Array<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>External<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Index</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Master</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">[]Schema<wbr>One<wbr>Of</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>array<wbr>Enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>array<wbr>One<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">Schema<wbr>Array<wbr>One<wbr>Of[]?</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>array<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>external<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>index</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>one<wbr>Ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">Schema<wbr>One<wbr>Of[]?</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>array_<wbr>enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Array of values that an array property's items can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>array_<wbr>one_<wbr>ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaarrayoneof">List[Schema<wbr>Array<wbr>One<wbr>Of]</a></span>
    </dt>
    <dd>{{% md %}}Display name and value an enum array can be set to.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>array_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the array elements if `type` is set to `"array"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enums</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Array of values a primitive property can be set to. See `array_enum` for arrays.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>external_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}External name of the user schema property.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>index</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The property name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>master</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>length</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min_<wbr>length</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum length of the user property value. Only applies to type `"string"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>one_<wbr>ofs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#schemaoneof">List[Schema<wbr>One<wbr>Of]</a></span>
    </dt>
    <dd>{{% md %}}Array of maps containing a mapping for display name to enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>permissions</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Access control permissions for the property. It can be set to `"READ_WRITE"`, `"READ_ONLY"`, `"HIDE"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the property is required for this application's users.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}determines whether an app user attribute can be set at the Individual or Group Level.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the schema property. It can be `"string"`, `"boolean"`, `"number"`, `"integer"`, `"array"`, or `"object"`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Schema<wbr>Array<wbr>One<wbr>Of</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#SchemaArrayOneOf">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#SchemaArrayOneOf">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/user?tab=doc#SchemaArrayOneOfArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/user?tab=doc#SchemaArrayOneOfOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Const</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}value mapping to member of `enum`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Const</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}value mapping to member of `enum`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>const</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}value mapping to member of `enum`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>const</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}value mapping to member of `enum`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Schema<wbr>One<wbr>Of</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#SchemaOneOf">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#SchemaOneOf">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/user?tab=doc#SchemaOneOfArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/user?tab=doc#SchemaOneOfOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Const</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}value mapping to member of `enum`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Const</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}value mapping to member of `enum`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>const</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}value mapping to member of `enum`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>const</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}value mapping to member of `enum`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>title</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}display name for the enum value.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-okta">https://github.com/pulumi/pulumi-okta</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

