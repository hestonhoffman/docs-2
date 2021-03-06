
---
title: "UserPool"
block_external_search_index: true
---



Provides a Cognito User Pool resource.

{{% examples %}}
## Example Usage

{{% example %}}
### Basic configuration

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const pool = new aws.cognito.UserPool("pool", {});
```

{{% /example %}}
{{% /examples %}}



## Create a UserPool Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/cognito/#UserPool">UserPool</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/cognito/#UserPoolArgs">UserPoolArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">UserPool</span><span class="p">(resource_name, opts=None, </span>admin_create_user_config=None<span class="p">, </span>alias_attributes=None<span class="p">, </span>auto_verified_attributes=None<span class="p">, </span>device_configuration=None<span class="p">, </span>email_configuration=None<span class="p">, </span>email_verification_message=None<span class="p">, </span>email_verification_subject=None<span class="p">, </span>lambda_config=None<span class="p">, </span>mfa_configuration=None<span class="p">, </span>name=None<span class="p">, </span>password_policy=None<span class="p">, </span>schemas=None<span class="p">, </span>sms_authentication_message=None<span class="p">, </span>sms_configuration=None<span class="p">, </span>sms_verification_message=None<span class="p">, </span>software_token_mfa_configuration=None<span class="p">, </span>tags=None<span class="p">, </span>user_pool_add_ons=None<span class="p">, </span>username_attributes=None<span class="p">, </span>username_configuration=None<span class="p">, </span>verification_message_template=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewUserPool<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolArgs">UserPoolArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPool">UserPool</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Cognito.UserPool.html">UserPool</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Cognito.UserPoolArgs.html">UserPoolArgs</a></span>? <span class="nx">args = null<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Admin<wbr>Create<wbr>User<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Alias<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Verified<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">User<wbr>Pool<wbr>Device<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">User<wbr>Pool<wbr>Email<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Verification<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lambda<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">User<wbr>Pool<wbr>Lambda<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">User<wbr>Pool<wbr>Password<wbr>Policy<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">List&lt;User<wbr>Pool<wbr>Schema<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Authentication<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">User<wbr>Pool<wbr>Sms<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Software<wbr>Token<wbr>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Pool<wbr>Add<wbr>Ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">User<wbr>Pool<wbr>Username<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Verification<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Admin<wbr>Create<wbr>User<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">*User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Alias<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Verified<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">*User<wbr>Pool<wbr>Device<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">*User<wbr>Pool<wbr>Email<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Verification<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lambda<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">*User<wbr>Pool<wbr>Lambda<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">*User<wbr>Pool<wbr>Password<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">[]User<wbr>Pool<wbr>Schema</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Authentication<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">*User<wbr>Pool<wbr>Sms<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Software<wbr>Token<wbr>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">*User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Pool<wbr>Add<wbr>Ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">*User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">*User<wbr>Pool<wbr>Username<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Verification<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">*User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admin<wbr>Create<wbr>User<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>alias<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Verified<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">User<wbr>Pool<wbr>Device<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">User<wbr>Pool<wbr>Email<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Verification<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lambda<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">User<wbr>Pool<wbr>Lambda<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">User<wbr>Pool<wbr>Password<wbr>Policy?</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">User<wbr>Pool<wbr>Schema[]?</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Authentication<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">User<wbr>Pool<wbr>Sms<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>software<wbr>Token<wbr>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Pool<wbr>Add<wbr>Ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">User<wbr>Pool<wbr>Username<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>verification<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template?</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admin_<wbr>create_<wbr>user_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">Dict[User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>alias_<wbr>attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>verified_<wbr>attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">Dict[User<wbr>Pool<wbr>Device<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">Dict[User<wbr>Pool<wbr>Email<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email_<wbr>verification_<wbr>message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email_<wbr>verification_<wbr>subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lambda_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">Dict[User<wbr>Pool<wbr>Lambda<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mfa_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">Dict[User<wbr>Pool<wbr>Password<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">List[User<wbr>Pool<wbr>Schema]</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms_<wbr>authentication_<wbr>message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">Dict[User<wbr>Pool<wbr>Sms<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms_<wbr>verification_<wbr>message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>software_<wbr>token_<wbr>mfa_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">Dict[User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user_<wbr>pool_<wbr>add_<wbr>ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">Dict[User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username_<wbr>attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">Dict[User<wbr>Pool<wbr>Username<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>verification_<wbr>message_<wbr>template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">Dict[User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template]</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## UserPool Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Admin<wbr>Create<wbr>User<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Alias<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the user pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Auto<wbr>Verified<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Creation<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date the user pool was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Device<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">User<wbr>Pool<wbr>Device<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Email<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">User<wbr>Pool<wbr>Email<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Email<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Email<wbr>Verification<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The endpoint name of the user pool. Example format: cognito-idp.REGION.amazonaws.com/xxxx_yyyyy
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Lambda<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">User<wbr>Pool<wbr>Lambda<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Last<wbr>Modified<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date the user pool was last modified.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Password<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">User<wbr>Pool<wbr>Password<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">List&lt;User<wbr>Pool<wbr>Schema&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sms<wbr>Authentication<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sms<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">User<wbr>Pool<wbr>Sms<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sms<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Software<wbr>Token<wbr>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User<wbr>Pool<wbr>Add<wbr>Ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Username<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Username<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">User<wbr>Pool<wbr>Username<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Verification<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Admin<wbr>Create<wbr>User<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Alias<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the user pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Auto<wbr>Verified<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Creation<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date the user pool was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Device<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">*User<wbr>Pool<wbr>Device<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Email<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">*User<wbr>Pool<wbr>Email<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Email<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Email<wbr>Verification<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The endpoint name of the user pool. Example format: cognito-idp.REGION.amazonaws.com/xxxx_yyyyy
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Lambda<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">User<wbr>Pool<wbr>Lambda<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Last<wbr>Modified<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date the user pool was last modified.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Password<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">User<wbr>Pool<wbr>Password<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">[]User<wbr>Pool<wbr>Schema</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sms<wbr>Authentication<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sms<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">User<wbr>Pool<wbr>Sms<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sms<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Software<wbr>Token<wbr>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">*User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>User<wbr>Pool<wbr>Add<wbr>Ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">*User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Username<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Username<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">*User<wbr>Pool<wbr>Username<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Verification<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>admin<wbr>Create<wbr>User<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>alias<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the user pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>auto<wbr>Verified<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>creation<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date the user pool was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>device<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">User<wbr>Pool<wbr>Device<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>email<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">User<wbr>Pool<wbr>Email<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>email<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>email<wbr>Verification<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The endpoint name of the user pool. Example format: cognito-idp.REGION.amazonaws.com/xxxx_yyyyy
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>lambda<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">User<wbr>Pool<wbr>Lambda<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>last<wbr>Modified<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The date the user pool was last modified.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>password<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">User<wbr>Pool<wbr>Password<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">User<wbr>Pool<wbr>Schema[]?</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sms<wbr>Authentication<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sms<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">User<wbr>Pool<wbr>Sms<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sms<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>software<wbr>Token<wbr>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user<wbr>Pool<wbr>Add<wbr>Ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>username<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>username<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">User<wbr>Pool<wbr>Username<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>verification<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>admin_<wbr>create_<wbr>user_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">Dict[User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>alias_<wbr>attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the user pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>auto_<wbr>verified_<wbr>attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>creation_<wbr>date</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The date the user pool was created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>device_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">Dict[User<wbr>Pool<wbr>Device<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>email_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">Dict[User<wbr>Pool<wbr>Email<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>email_<wbr>verification_<wbr>message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>email_<wbr>verification_<wbr>subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The endpoint name of the user pool. Example format: cognito-idp.REGION.amazonaws.com/xxxx_yyyyy
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>lambda_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">Dict[User<wbr>Pool<wbr>Lambda<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>last_<wbr>modified_<wbr>date</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The date the user pool was last modified.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>mfa_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>password_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">Dict[User<wbr>Pool<wbr>Password<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">List[User<wbr>Pool<wbr>Schema]</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sms_<wbr>authentication_<wbr>message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sms_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">Dict[User<wbr>Pool<wbr>Sms<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sms_<wbr>verification_<wbr>message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>software_<wbr>token_<wbr>mfa_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">Dict[User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>user_<wbr>pool_<wbr>add_<wbr>ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">Dict[User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>username_<wbr>attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>username_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">Dict[User<wbr>Pool<wbr>Username<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>verification_<wbr>message_<wbr>template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">Dict[User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template]</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing UserPool Resource

Get an existing UserPool resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/cognito/#UserPoolState">UserPoolState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/cognito/#UserPool">UserPool</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>admin_create_user_config=None<span class="p">, </span>alias_attributes=None<span class="p">, </span>arn=None<span class="p">, </span>auto_verified_attributes=None<span class="p">, </span>creation_date=None<span class="p">, </span>device_configuration=None<span class="p">, </span>email_configuration=None<span class="p">, </span>email_verification_message=None<span class="p">, </span>email_verification_subject=None<span class="p">, </span>endpoint=None<span class="p">, </span>lambda_config=None<span class="p">, </span>last_modified_date=None<span class="p">, </span>mfa_configuration=None<span class="p">, </span>name=None<span class="p">, </span>password_policy=None<span class="p">, </span>schemas=None<span class="p">, </span>sms_authentication_message=None<span class="p">, </span>sms_configuration=None<span class="p">, </span>sms_verification_message=None<span class="p">, </span>software_token_mfa_configuration=None<span class="p">, </span>tags=None<span class="p">, </span>user_pool_add_ons=None<span class="p">, </span>username_attributes=None<span class="p">, </span>username_configuration=None<span class="p">, </span>verification_message_template=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetUserPool<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolState">UserPoolState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPool">UserPool</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Cognito.UserPool.html">UserPool</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Cognito.UserPoolState.html">UserPoolState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Admin<wbr>Create<wbr>User<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Alias<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Verified<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Creation<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The date the user pool was created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">User<wbr>Pool<wbr>Device<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">User<wbr>Pool<wbr>Email<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Verification<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The endpoint name of the user pool. Example format: cognito-idp.REGION.amazonaws.com/xxxx_yyyyy
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lambda<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">User<wbr>Pool<wbr>Lambda<wbr>Config<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Last<wbr>Modified<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The date the user pool was last modified.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">User<wbr>Pool<wbr>Password<wbr>Policy<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">List&lt;User<wbr>Pool<wbr>Schema<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Authentication<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">User<wbr>Pool<wbr>Sms<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Software<wbr>Token<wbr>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Pool<wbr>Add<wbr>Ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">User<wbr>Pool<wbr>Username<wbr>Configuration<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Verification<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Admin<wbr>Create<wbr>User<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">*User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Alias<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Verified<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Creation<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The date the user pool was created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">*User<wbr>Pool<wbr>Device<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">*User<wbr>Pool<wbr>Email<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Verification<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The endpoint name of the user pool. Example format: cognito-idp.REGION.amazonaws.com/xxxx_yyyyy
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lambda<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">*User<wbr>Pool<wbr>Lambda<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Last<wbr>Modified<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The date the user pool was last modified.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Password<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">*User<wbr>Pool<wbr>Password<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">[]User<wbr>Pool<wbr>Schema</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Authentication<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">*User<wbr>Pool<wbr>Sms<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Software<wbr>Token<wbr>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">*User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Pool<wbr>Add<wbr>Ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">*User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Username<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">*User<wbr>Pool<wbr>Username<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Verification<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">*User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admin<wbr>Create<wbr>User<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>alias<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Verified<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>creation<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The date the user pool was created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">User<wbr>Pool<wbr>Device<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">User<wbr>Pool<wbr>Email<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Verification<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The endpoint name of the user pool. Example format: cognito-idp.REGION.amazonaws.com/xxxx_yyyyy
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lambda<wbr>Config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">User<wbr>Pool<wbr>Lambda<wbr>Config?</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>last<wbr>Modified<wbr>Date</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The date the user pool was last modified.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">User<wbr>Pool<wbr>Password<wbr>Policy?</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">User<wbr>Pool<wbr>Schema[]?</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Authentication<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">User<wbr>Pool<wbr>Sms<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Verification<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>software<wbr>Token<wbr>Mfa<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Pool<wbr>Add<wbr>Ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons?</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username<wbr>Attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">User<wbr>Pool<wbr>Username<wbr>Configuration?</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>verification<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template?</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admin_<wbr>create_<wbr>user_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfig">Dict[User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}The configuration for AdminCreateUser requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>alias_<wbr>attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Attributes supported as an alias for this user pool. Possible values: phone_number, email, or preferred_username. Conflicts with `username_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>verified_<wbr>attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The attributes to be auto-verified. Possible values: email, phone_number.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>creation_<wbr>date</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The date the user pool was created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooldeviceconfiguration">Dict[User<wbr>Pool<wbr>Device<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The configuration for the user pool's device tracking.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolemailconfiguration">Dict[User<wbr>Pool<wbr>Email<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The Email Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email_<wbr>verification_<wbr>message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification message. Conflicts with `verification_message_template` configuration block `email_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email_<wbr>verification_<wbr>subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the email verification subject. Conflicts with `verification_message_template` configuration block `email_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The endpoint name of the user pool. Example format: cognito-idp.REGION.amazonaws.com/xxxx_yyyyy
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lambda_<wbr>config</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoollambdaconfig">Dict[User<wbr>Pool<wbr>Lambda<wbr>Config]</a></span>
    </dt>
    <dd>{{% md %}}A container for the AWS Lambda triggers associated with the user pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>last_<wbr>modified_<wbr>date</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The date the user pool was last modified.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mfa_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Multi-Factor Authentication (MFA) configuration for the User Pool. Defaults of `OFF`. Valid values:
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>password_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolpasswordpolicy">Dict[User<wbr>Pool<wbr>Password<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}A container for information about the user pool password policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>schemas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschema">List[User<wbr>Pool<wbr>Schema]</a></span>
    </dt>
    <dd>{{% md %}}A container with the schema attributes of a user pool. Schema attributes from the [standard attribute set](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html#cognito-user-pools-standard-attributes) only need to be specified if they are different from the default configuration. Maximum of 50 attributes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms_<wbr>authentication_<wbr>message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS authentication message. The message must contain the `{####}` placeholder, which will be replaced with the code.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsmsconfiguration">Dict[User<wbr>Pool<wbr>Sms<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for Short Message Service (SMS) settings. Detailed below. These settings apply to SMS user verification and SMS Multi-Factor Authentication (MFA). Due to Cognito API restrictions, the SMS configuration cannot be removed without recreating the Cognito User Pool. For user data safety, this resource will ignore the removal of this configuration by disabling drift detection. To force resource recreation after this configuration has been applied, see the [`up` command and use --replace](https://www.pulumi.com/docs/reference/cli/pulumi_up/).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms_<wbr>verification_<wbr>message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string representing the SMS verification message. Conflicts with `verification_message_template` configuration block `sms_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>software_<wbr>token_<wbr>mfa_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolsoftwaretokenmfaconfiguration">Dict[User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for software token Mult-Factor Authentication (MFA) settings. Detailed below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}A mapping of tags to assign to the User Pool.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user_<wbr>pool_<wbr>add_<wbr>ons</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooluserpooladdons">Dict[User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons]</a></span>
    </dt>
    <dd>{{% md %}}Configuration block for user pool add-ons to enable user pool advanced security mode features.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username_<wbr>attributes</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}Specifies whether email addresses or phone numbers can be specified as usernames when a user signs up. Conflicts with `alias_attributes`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>username_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolusernameconfiguration">Dict[User<wbr>Pool<wbr>Username<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The Username Configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>verification_<wbr>message_<wbr>template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolverificationmessagetemplate">Dict[User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template]</a></span>
    </dt>
    <dd>{{% md %}}The verification message templates configuration.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolAdminCreateUserConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolAdminCreateUserConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolAdminCreateUserConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolAdminCreateUserConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Allow<wbr>Admin<wbr>Create<wbr>User<wbr>Only</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Set to True if only the administrator is allowed to create user profiles. Set to False if users can sign themselves up via an app.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Invite<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfiginvitemessagetemplate">User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config<wbr>Invite<wbr>Message<wbr>Template<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The invite message template structure.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Unused<wbr>Account<wbr>Validity<wbr>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}**DEPRECATED** Use password_policy.temporary_password_validity_days instead - The user account expiration limit, in days, after which the account is no longer usable.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use password_policy.temporary_password_validity_days instead{{% /md %}}</p></dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Allow<wbr>Admin<wbr>Create<wbr>User<wbr>Only</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Set to True if only the administrator is allowed to create user profiles. Set to False if users can sign themselves up via an app.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Invite<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfiginvitemessagetemplate">*User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config<wbr>Invite<wbr>Message<wbr>Template</a></span>
    </dt>
    <dd>{{% md %}}The invite message template structure.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Unused<wbr>Account<wbr>Validity<wbr>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}**DEPRECATED** Use password_policy.temporary_password_validity_days instead - The user account expiration limit, in days, after which the account is no longer usable.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use password_policy.temporary_password_validity_days instead{{% /md %}}</p></dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>allow<wbr>Admin<wbr>Create<wbr>User<wbr>Only</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Set to True if only the administrator is allowed to create user profiles. Set to False if users can sign themselves up via an app.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>invite<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfiginvitemessagetemplate">User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config<wbr>Invite<wbr>Message<wbr>Template?</a></span>
    </dt>
    <dd>{{% md %}}The invite message template structure.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>unused<wbr>Account<wbr>Validity<wbr>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}**DEPRECATED** Use password_policy.temporary_password_validity_days instead - The user account expiration limit, in days, after which the account is no longer usable.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use password_policy.temporary_password_validity_days instead{{% /md %}}</p></dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>allow<wbr>Admin<wbr>Create<wbr>User<wbr>Only</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Set to True if only the administrator is allowed to create user profiles. Set to False if users can sign themselves up via an app.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>invite<wbr>Message<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpooladmincreateuserconfiginvitemessagetemplate">Dict[User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config<wbr>Invite<wbr>Message<wbr>Template]</a></span>
    </dt>
    <dd>{{% md %}}The invite message template structure.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>unused<wbr>Account<wbr>Validity<wbr>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}**DEPRECATED** Use password_policy.temporary_password_validity_days instead - The user account expiration limit, in days, after which the account is no longer usable.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use password_policy.temporary_password_validity_days instead{{% /md %}}</p></dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Admin<wbr>Create<wbr>User<wbr>Config<wbr>Invite<wbr>Message<wbr>Template</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolAdminCreateUserConfigInviteMessageTemplate">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolAdminCreateUserConfigInviteMessageTemplate">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolAdminCreateUserConfigInviteMessageTemplateArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolAdminCreateUserConfigInviteMessageTemplateOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The email message template. Must contain the `{####}` placeholder. Conflicts with `email_verification_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template. Conflicts with `email_verification_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The SMS message template. Must contain the `{####}` placeholder. Conflicts with `sms_verification_message` argument.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The email message template. Must contain the `{####}` placeholder. Conflicts with `email_verification_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template. Conflicts with `email_verification_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The SMS message template. Must contain the `{####}` placeholder. Conflicts with `sms_verification_message` argument.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The email message template. Must contain the `{####}` placeholder. Conflicts with `email_verification_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template. Conflicts with `email_verification_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The SMS message template. Must contain the `{####}` placeholder. Conflicts with `sms_verification_message` argument.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The email message template. Must contain the `{####}` placeholder. Conflicts with `email_verification_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template. Conflicts with `email_verification_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The SMS message template. Must contain the `{####}` placeholder. Conflicts with `sms_verification_message` argument.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Device<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolDeviceConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolDeviceConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolDeviceConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolDeviceConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Challenge<wbr>Required<wbr>On<wbr>New<wbr>Device</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Indicates whether a challenge is required on a new device. Only applicable to a new device.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Only<wbr>Remembered<wbr>On<wbr>User<wbr>Prompt</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If true, a device is only remembered on user prompt.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Challenge<wbr>Required<wbr>On<wbr>New<wbr>Device</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Indicates whether a challenge is required on a new device. Only applicable to a new device.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Only<wbr>Remembered<wbr>On<wbr>User<wbr>Prompt</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If true, a device is only remembered on user prompt.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>challenge<wbr>Required<wbr>On<wbr>New<wbr>Device</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Indicates whether a challenge is required on a new device. Only applicable to a new device.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device<wbr>Only<wbr>Remembered<wbr>On<wbr>User<wbr>Prompt</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If true, a device is only remembered on user prompt.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>challenge<wbr>Required<wbr>On<wbr>New<wbr>Device</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Indicates whether a challenge is required on a new device. Only applicable to a new device.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device<wbr>Only<wbr>Remembered<wbr>On<wbr>User<wbr>Prompt</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, a device is only remembered on user prompt.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Email<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolEmailConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolEmailConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolEmailConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolEmailConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Sending<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Instruct Cognito to either use its built-in functional or Amazon SES to send out emails.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>From<wbr>Email<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Sender’s email address or sender’s name with their email address (e.g. "john@smith.com" or "John Smith <john@smith.com>")
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Reply<wbr>To<wbr>Email<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The REPLY-TO email address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Source<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the email source.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Sending<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Instruct Cognito to either use its built-in functional or Amazon SES to send out emails.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>From<wbr>Email<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Sender’s email address or sender’s name with their email address (e.g. "john@smith.com" or "John Smith <john@smith.com>")
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Reply<wbr>To<wbr>Email<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The REPLY-TO email address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Source<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the email source.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Sending<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Instruct Cognito to either use its built-in functional or Amazon SES to send out emails.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>from<wbr>Email<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Sender’s email address or sender’s name with their email address (e.g. "john@smith.com" or "John Smith <john@smith.com>")
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>reply<wbr>To<wbr>Email<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The REPLY-TO email address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>source<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the email source.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Sending<wbr>Account</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Instruct Cognito to either use its built-in functional or Amazon SES to send out emails.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>from<wbr>Email<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Sender’s email address or sender’s name with their email address (e.g. "john@smith.com" or "John Smith <john@smith.com>")
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>reply<wbr>To<wbr>Email<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The REPLY-TO email address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>source_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the email source.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Lambda<wbr>Config</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolLambdaConfig">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolLambdaConfig">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolLambdaConfigArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolLambdaConfigOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Create<wbr>Auth<wbr>Challenge</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the lambda creating an authentication challenge.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom Message AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Define<wbr>Auth<wbr>Challenge</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Defines the authentication challenge.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Post<wbr>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A post-authentication AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Post<wbr>Confirmation</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A post-confirmation AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pre<wbr>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A pre-authentication AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pre<wbr>Sign<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A pre-registration AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pre<wbr>Token<wbr>Generation</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Allow to customize identity token claims before token generation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Migration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The user migration Lambda config type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Verify<wbr>Auth<wbr>Challenge<wbr>Response</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Verifies the authentication challenge response.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Create<wbr>Auth<wbr>Challenge</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the lambda creating an authentication challenge.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Custom<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A custom Message AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Define<wbr>Auth<wbr>Challenge</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Defines the authentication challenge.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Post<wbr>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A post-authentication AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Post<wbr>Confirmation</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A post-confirmation AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pre<wbr>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A pre-authentication AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pre<wbr>Sign<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A pre-registration AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Pre<wbr>Token<wbr>Generation</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Allow to customize identity token claims before token generation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>User<wbr>Migration</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The user migration Lambda config type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Verify<wbr>Auth<wbr>Challenge<wbr>Response</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Verifies the authentication challenge response.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>create<wbr>Auth<wbr>Challenge</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the lambda creating an authentication challenge.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A custom Message AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>define<wbr>Auth<wbr>Challenge</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Defines the authentication challenge.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>post<wbr>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A post-authentication AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>post<wbr>Confirmation</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A post-confirmation AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pre<wbr>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A pre-authentication AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pre<wbr>Sign<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A pre-registration AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pre<wbr>Token<wbr>Generation</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Allow to customize identity token claims before token generation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Migration</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The user migration Lambda config type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>verify<wbr>Auth<wbr>Challenge<wbr>Response</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Verifies the authentication challenge response.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>create<wbr>Auth<wbr>Challenge</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the lambda creating an authentication challenge.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>custom<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A custom Message AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>define<wbr>Auth<wbr>Challenge</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Defines the authentication challenge.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>post<wbr>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A post-authentication AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>post<wbr>Confirmation</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A post-confirmation AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pre<wbr>Authentication</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A pre-authentication AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pre<wbr>Sign<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A pre-registration AWS Lambda trigger.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>pre<wbr>Token<wbr>Generation</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Allow to customize identity token claims before token generation.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>user<wbr>Migration</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The user migration Lambda config type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>verify<wbr>Auth<wbr>Challenge<wbr>Response</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Verifies the authentication challenge response.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Password<wbr>Policy</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolPasswordPolicy">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolPasswordPolicy">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolPasswordPolicyArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolPasswordPolicyOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Minimum<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The minimum length of the password policy that you have set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Require<wbr>Lowercase</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one lowercase letter in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Require<wbr>Numbers</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one number in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Require<wbr>Symbols</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one symbol in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Require<wbr>Uppercase</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one uppercase letter in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Temporary<wbr>Password<wbr>Validity<wbr>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}In the password policy you have set, refers to the number of days a temporary password is valid. If the user does not sign-in during this time, their password will need to be reset by an administrator.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Minimum<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The minimum length of the password policy that you have set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Require<wbr>Lowercase</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one lowercase letter in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Require<wbr>Numbers</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one number in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Require<wbr>Symbols</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one symbol in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Require<wbr>Uppercase</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one uppercase letter in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Temporary<wbr>Password<wbr>Validity<wbr>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}In the password policy you have set, refers to the number of days a temporary password is valid. If the user does not sign-in during this time, their password will need to be reset by an administrator.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>minimum<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The minimum length of the password policy that you have set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>require<wbr>Lowercase</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one lowercase letter in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>require<wbr>Numbers</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one number in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>require<wbr>Symbols</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one symbol in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>require<wbr>Uppercase</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one uppercase letter in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>temporary<wbr>Password<wbr>Validity<wbr>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}In the password policy you have set, refers to the number of days a temporary password is valid. If the user does not sign-in during this time, their password will need to be reset by an administrator.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>minimum<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The minimum length of the password policy that you have set.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>require<wbr>Lowercase</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one lowercase letter in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>require_<wbr>numbers</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one number in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>require_<wbr>symbols</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one symbol in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>require<wbr>Uppercase</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether you have required users to use at least one uppercase letter in their password.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>temporary<wbr>Password<wbr>Validity<wbr>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}In the password policy you have set, refers to the number of days a temporary password is valid. If the user does not sign-in during this time, their password will need to be reset by an administrator.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Schema</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolSchema">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolSchema">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSchemaArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSchemaOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Attribute<wbr>Data<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The attribute data type. Must be one of `Boolean`, `Number`, `String`, `DateTime`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Developer<wbr>Only<wbr>Attribute</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Specifies whether the attribute type is developer only.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mutable</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Specifies whether the attribute can be changed once it has been created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Number<wbr>Attribute<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschemanumberattributeconstraints">User<wbr>Pool<wbr>Schema<wbr>Number<wbr>Attribute<wbr>Constraints<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Specifies the constraints for an attribute of the number type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Specifies whether a user pool attribute is required. If the attribute is required and the user does not provide a value, registration or sign-in will fail.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>String<wbr>Attribute<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschemastringattributeconstraints">User<wbr>Pool<wbr>Schema<wbr>String<wbr>Attribute<wbr>Constraints<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}-Specifies the constraints for an attribute of the string type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Attribute<wbr>Data<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The attribute data type. Must be one of `Boolean`, `Number`, `String`, `DateTime`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Developer<wbr>Only<wbr>Attribute</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the attribute type is developer only.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mutable</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the attribute can be changed once it has been created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Number<wbr>Attribute<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschemanumberattributeconstraints">*User<wbr>Pool<wbr>Schema<wbr>Number<wbr>Attribute<wbr>Constraints</a></span>
    </dt>
    <dd>{{% md %}}Specifies the constraints for an attribute of the number type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Required</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether a user pool attribute is required. If the attribute is required and the user does not provide a value, registration or sign-in will fail.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>String<wbr>Attribute<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschemastringattributeconstraints">*User<wbr>Pool<wbr>Schema<wbr>String<wbr>Attribute<wbr>Constraints</a></span>
    </dt>
    <dd>{{% md %}}-Specifies the constraints for an attribute of the string type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>attribute<wbr>Data<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The attribute data type. Must be one of `Boolean`, `Number`, `String`, `DateTime`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>developer<wbr>Only<wbr>Attribute</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Specifies whether the attribute type is developer only.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mutable</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Specifies whether the attribute can be changed once it has been created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>number<wbr>Attribute<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschemanumberattributeconstraints">User<wbr>Pool<wbr>Schema<wbr>Number<wbr>Attribute<wbr>Constraints?</a></span>
    </dt>
    <dd>{{% md %}}Specifies the constraints for an attribute of the number type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Specifies whether a user pool attribute is required. If the attribute is required and the user does not provide a value, registration or sign-in will fail.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>string<wbr>Attribute<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschemastringattributeconstraints">User<wbr>Pool<wbr>Schema<wbr>String<wbr>Attribute<wbr>Constraints?</a></span>
    </dt>
    <dd>{{% md %}}-Specifies the constraints for an attribute of the string type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>attribute<wbr>Data<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The attribute data type. Must be one of `Boolean`, `Number`, `String`, `DateTime`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>developer<wbr>Only<wbr>Attribute</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the attribute type is developer only.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mutable</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the attribute can be changed once it has been created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the attribute.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>number<wbr>Attribute<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschemanumberattributeconstraints">Dict[User<wbr>Pool<wbr>Schema<wbr>Number<wbr>Attribute<wbr>Constraints]</a></span>
    </dt>
    <dd>{{% md %}}Specifies the constraints for an attribute of the number type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>required</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether a user pool attribute is required. If the attribute is required and the user does not provide a value, registration or sign-in will fail.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>string<wbr>Attribute<wbr>Constraints</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#userpoolschemastringattributeconstraints">Dict[User<wbr>Pool<wbr>Schema<wbr>String<wbr>Attribute<wbr>Constraints]</a></span>
    </dt>
    <dd>{{% md %}}-Specifies the constraints for an attribute of the string type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Schema<wbr>Number<wbr>Attribute<wbr>Constraints</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolSchemaNumberAttributeConstraints">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolSchemaNumberAttributeConstraints">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSchemaNumberAttributeConstraintsArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSchemaNumberAttributeConstraintsOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum value of an attribute that is of the number data type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The minimum value of an attribute that is of the number data type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The maximum value of an attribute that is of the number data type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The minimum value of an attribute that is of the number data type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum value of an attribute that is of the number data type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The minimum value of an attribute that is of the number data type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The maximum value of an attribute that is of the number data type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The minimum value of an attribute that is of the number data type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Schema<wbr>String<wbr>Attribute<wbr>Constraints</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolSchemaStringAttributeConstraints">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolSchemaStringAttributeConstraints">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSchemaStringAttributeConstraintsArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSchemaStringAttributeConstraintsOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum length of an attribute value of the string type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The minimum length of an attribute value of the string type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The maximum length of an attribute value of the string type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The minimum length of an attribute value of the string type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum length of an attribute value of the string type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The minimum length of an attribute value of the string type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The maximum length of an attribute value of the string type.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Length</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The minimum length of an attribute value of the string type.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Sms<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolSmsConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolSmsConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSmsConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSmsConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>External<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The external ID used in IAM role trust relationships. For more information about using external IDs, see [How to Use an External ID When Granting Access to Your AWS Resources to a Third Party](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Sns<wbr>Caller<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Amazon SNS caller. This is usually the IAM role that you've given Cognito permission to assume.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>External<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The external ID used in IAM role trust relationships. For more information about using external IDs, see [How to Use an External ID When Granting Access to Your AWS Resources to a Third Party](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Sns<wbr>Caller<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Amazon SNS caller. This is usually the IAM role that you've given Cognito permission to assume.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>external<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The external ID used in IAM role trust relationships. For more information about using external IDs, see [How to Use an External ID When Granting Access to Your AWS Resources to a Third Party](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>sns<wbr>Caller<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Amazon SNS caller. This is usually the IAM role that you've given Cognito permission to assume.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>external<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The external ID used in IAM role trust relationships. For more information about using external IDs, see [How to Use an External ID When Granting Access to Your AWS Resources to a Third Party](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>sns<wbr>Caller<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the Amazon SNS caller. This is usually the IAM role that you've given Cognito permission to assume.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Software<wbr>Token<wbr>Mfa<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolSoftwareTokenMfaConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolSoftwareTokenMfaConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSoftwareTokenMfaConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolSoftwareTokenMfaConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Boolean whether to enable software token Multi-Factor (MFA) tokens, such as Time-based One-Time Password (TOTP). To disable software token MFA when `sms_configuration` is not present, the `mfa_configuration` argument must be set to `OFF` and the `software_token_mfa_configuration` configuration block must be fully removed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Boolean whether to enable software token Multi-Factor (MFA) tokens, such as Time-based One-Time Password (TOTP). To disable software token MFA when `sms_configuration` is not present, the `mfa_configuration` argument must be set to `OFF` and the `software_token_mfa_configuration` configuration block must be fully removed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Boolean whether to enable software token Multi-Factor (MFA) tokens, such as Time-based One-Time Password (TOTP). To disable software token MFA when `sms_configuration` is not present, the `mfa_configuration` argument must be set to `OFF` and the `software_token_mfa_configuration` configuration block must be fully removed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Boolean whether to enable software token Multi-Factor (MFA) tokens, such as Time-based One-Time Password (TOTP). To disable software token MFA when `sms_configuration` is not present, the `mfa_configuration` argument must be set to `OFF` and the `software_token_mfa_configuration` configuration block must be fully removed.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>User<wbr>Pool<wbr>Add<wbr>Ons</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolUserPoolAddOns">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolUserPoolAddOns">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolUserPoolAddOnsArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolUserPoolAddOnsOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Advanced<wbr>Security<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The mode for advanced security, must be one of `OFF`, `AUDIT` or `ENFORCED`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Advanced<wbr>Security<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The mode for advanced security, must be one of `OFF`, `AUDIT` or `ENFORCED`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>advanced<wbr>Security<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The mode for advanced security, must be one of `OFF`, `AUDIT` or `ENFORCED`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>advanced<wbr>Security<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The mode for advanced security, must be one of `OFF`, `AUDIT` or `ENFORCED`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Username<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolUsernameConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolUsernameConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolUsernameConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolUsernameConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Case<wbr>Sensitive</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether username case sensitivity will be applied for all users in the user pool through Cognito APIs.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Case<wbr>Sensitive</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether username case sensitivity will be applied for all users in the user pool through Cognito APIs.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>case<wbr>Sensitive</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Specifies whether username case sensitivity will be applied for all users in the user pool through Cognito APIs.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>case<wbr>Sensitive</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether username case sensitivity will be applied for all users in the user pool through Cognito APIs.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>User<wbr>Pool<wbr>Verification<wbr>Message<wbr>Template</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#UserPoolVerificationMessageTemplate">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#UserPoolVerificationMessageTemplate">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolVerificationMessageTemplateArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/cognito?tab=doc#UserPoolVerificationMessageTemplateOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Email<wbr>Option</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The default email option. Must be either `CONFIRM_WITH_CODE` or `CONFIRM_WITH_LINK`. Defaults to `CONFIRM_WITH_CODE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The email message template. Must contain the `{####}` placeholder. Conflicts with `email_verification_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Message<wbr>By<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The email message template for sending a confirmation link to the user, it must contain the `{##Click Here##}` placeholder.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template. Conflicts with `email_verification_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Subject<wbr>By<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template for sending a confirmation link to the user.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The SMS message template. Must contain the `{####}` placeholder. Conflicts with `sms_verification_message` argument.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Default<wbr>Email<wbr>Option</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The default email option. Must be either `CONFIRM_WITH_CODE` or `CONFIRM_WITH_LINK`. Defaults to `CONFIRM_WITH_CODE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The email message template. Must contain the `{####}` placeholder. Conflicts with `email_verification_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Message<wbr>By<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The email message template for sending a confirmation link to the user, it must contain the `{##Click Here##}` placeholder.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template. Conflicts with `email_verification_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Email<wbr>Subject<wbr>By<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template for sending a confirmation link to the user.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sms<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The SMS message template. Must contain the `{####}` placeholder. Conflicts with `sms_verification_message` argument.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Email<wbr>Option</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The default email option. Must be either `CONFIRM_WITH_CODE` or `CONFIRM_WITH_LINK`. Defaults to `CONFIRM_WITH_CODE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The email message template. Must contain the `{####}` placeholder. Conflicts with `email_verification_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Message<wbr>By<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The email message template for sending a confirmation link to the user, it must contain the `{##Click Here##}` placeholder.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template. Conflicts with `email_verification_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Subject<wbr>By<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template for sending a confirmation link to the user.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The SMS message template. Must contain the `{####}` placeholder. Conflicts with `sms_verification_message` argument.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>default<wbr>Email<wbr>Option</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The default email option. Must be either `CONFIRM_WITH_CODE` or `CONFIRM_WITH_LINK`. Defaults to `CONFIRM_WITH_CODE`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The email message template. Must contain the `{####}` placeholder. Conflicts with `email_verification_message` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Message<wbr>By<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The email message template for sending a confirmation link to the user, it must contain the `{##Click Here##}` placeholder.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Subject</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template. Conflicts with `email_verification_subject` argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>email<wbr>Subject<wbr>By<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The subject line for the email message template for sending a confirmation link to the user.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sms<wbr>Message</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The SMS message template. Must contain the `{####}` placeholder. Conflicts with `sms_verification_message` argument.
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

