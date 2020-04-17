
---
title: "Authorizer"
block_external_search_index: true
---



Manages an Amazon API Gateway Version 2 authorizer.
More information can be found in the [Amazon API Gateway Developer Guide](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api.html).

{{% examples %}}
## Example Usage

{{% example %}}
### Basic WebSocket API

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = new aws.apigatewayv2.Authorizer("example", {
    apiId: aws_apigatewayv2_api_example.id,
    authorizerType: "REQUEST",
    authorizerUri: aws_lambda_function_example.invokeArn,
    identitySources: ["route.request.header.Auth"],
});
```

{{% /example %}}
{{% example %}}
### Basic HTTP API

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const example = new aws.apigatewayv2.Authorizer("example", {
    apiId: aws_apigatewayv2_api_example.id,
    authorizerType: "JWT",
    identitySources: ["$request.header.Authorization"],
    jwtConfiguration: {
        audiences: ["example"],
        issuer: pulumi.interpolate`https://${aws_cognito_user_pool_example.endpoint}`,
    },
});
```

{{% /example %}}
{{% /examples %}}



## Create a Authorizer Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/apigatewayv2/#Authorizer">Authorizer</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/apigatewayv2/#AuthorizerArgs">AuthorizerArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Authorizer</span><span class="p">(resource_name, opts=None, </span>api_id=None<span class="p">, </span>authorizer_credentials_arn=None<span class="p">, </span>authorizer_type=None<span class="p">, </span>authorizer_uri=None<span class="p">, </span>identity_sources=None<span class="p">, </span>jwt_configuration=None<span class="p">, </span>name=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewAuthorizer<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/v2/go/aws/apigatewayv2?tab=doc#AuthorizerArgs">AuthorizerArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/v2/go/aws/apigatewayv2?tab=doc#Authorizer">Authorizer</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.ApiGatewayV2.Authorizer.html">Authorizer</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.ApiGatewayV2.AuthorizerArgs.html">AuthorizerArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Api<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The API identifier.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Authorizer<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer type. Valid values: `JWT`, `REQUEST`.
For WebSocket APIs, specify `REQUEST` for a Lambda function using incoming request parameters.
For HTTP APIs, specify `JWT` to use JSON Web Tokens.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Identity<wbr>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}The identity sources for which authorization is requested.
For `REQUEST` authorizers the value is a list of one or more mapping expressions of the specified request parameters.
For `JWT` authorizers the single entry specifies where to extract the JSON Web Token (JWT) from inbound requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Credentials<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The required credentials as an IAM role for API Gateway to invoke the authorizer.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer's Uniform Resource Identifier (URI).
For `REQUEST` authorizers this must be a well-formed Lambda function URI, such as the `invoke_arn` attribute of the [`aws.lambda.Function`](https://www.terraform.io/docs/providers/aws/r/lambda_function.html) resource.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Jwt<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#authorizerjwtconfiguration">Authorizer<wbr>Jwt<wbr>Configuration<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The configuration of a JWT authorizer. Required for the `JWT` authorizer type.
Supported only for HTTP APIs.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the authorizer.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Api<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The API identifier.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Authorizer<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer type. Valid values: `JWT`, `REQUEST`.
For WebSocket APIs, specify `REQUEST` for a Lambda function using incoming request parameters.
For HTTP APIs, specify `JWT` to use JSON Web Tokens.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Identity<wbr>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}The identity sources for which authorization is requested.
For `REQUEST` authorizers the value is a list of one or more mapping expressions of the specified request parameters.
For `JWT` authorizers the single entry specifies where to extract the JSON Web Token (JWT) from inbound requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Credentials<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The required credentials as an IAM role for API Gateway to invoke the authorizer.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer's Uniform Resource Identifier (URI).
For `REQUEST` authorizers this must be a well-formed Lambda function URI, such as the `invoke_arn` attribute of the [`aws.lambda.Function`](https://www.terraform.io/docs/providers/aws/r/lambda_function.html) resource.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Jwt<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#authorizerjwtconfiguration">Authorizer<wbr>Jwt<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The configuration of a JWT authorizer. Required for the `JWT` authorizer type.
Supported only for HTTP APIs.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the authorizer.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>api<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The API identifier.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>authorizer<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer type. Valid values: `JWT`, `REQUEST`.
For WebSocket APIs, specify `REQUEST` for a Lambda function using incoming request parameters.
For HTTP APIs, specify `JWT` to use JSON Web Tokens.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>identity<wbr>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}The identity sources for which authorization is requested.
For `REQUEST` authorizers the value is a list of one or more mapping expressions of the specified request parameters.
For `JWT` authorizers the single entry specifies where to extract the JSON Web Token (JWT) from inbound requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer<wbr>Credentials<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The required credentials as an IAM role for API Gateway to invoke the authorizer.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer<wbr>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer's Uniform Resource Identifier (URI).
For `REQUEST` authorizers this must be a well-formed Lambda function URI, such as the `invoke_arn` attribute of the [`aws.lambda.Function`](https://www.terraform.io/docs/providers/aws/r/lambda_function.html) resource.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>jwt<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#authorizerjwtconfiguration">Authorizer<wbr>Jwt<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The configuration of a JWT authorizer. Required for the `JWT` authorizer type.
Supported only for HTTP APIs.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the authorizer.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>api_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The API identifier.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>authorizer_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The authorizer type. Valid values: `JWT`, `REQUEST`.
For WebSocket APIs, specify `REQUEST` for a Lambda function using incoming request parameters.
For HTTP APIs, specify `JWT` to use JSON Web Tokens.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>identity_<wbr>sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}The identity sources for which authorization is requested.
For `REQUEST` authorizers the value is a list of one or more mapping expressions of the specified request parameters.
For `JWT` authorizers the single entry specifies where to extract the JSON Web Token (JWT) from inbound requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer_<wbr>credentials_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The required credentials as an IAM role for API Gateway to invoke the authorizer.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer_<wbr>uri</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The authorizer's Uniform Resource Identifier (URI).
For `REQUEST` authorizers this must be a well-formed Lambda function URI, such as the `invoke_arn` attribute of the [`aws.lambda.Function`](https://www.terraform.io/docs/providers/aws/r/lambda_function.html) resource.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>jwt_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#authorizerjwtconfiguration">Dict[Authorizer<wbr>Jwt<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The configuration of a JWT authorizer. Required for the `JWT` authorizer type.
Supported only for HTTP APIs.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The name of the authorizer.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Look up an Existing Authorizer Resource

Get an existing Authorizer resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/apigatewayv2/#AuthorizerState">AuthorizerState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/apigatewayv2/#Authorizer">Authorizer</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>api_id=None<span class="p">, </span>authorizer_credentials_arn=None<span class="p">, </span>authorizer_type=None<span class="p">, </span>authorizer_uri=None<span class="p">, </span>identity_sources=None<span class="p">, </span>jwt_configuration=None<span class="p">, </span>name=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetAuthorizer<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/v2/go/aws/apigatewayv2?tab=doc#AuthorizerState">AuthorizerState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/v2/go/aws/apigatewayv2?tab=doc#Authorizer">Authorizer</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.ApiGatewayV2.Authorizer.html">Authorizer</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.ApiGatewayV2.AuthorizerState.html">AuthorizerState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Api<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The API identifier.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Credentials<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The required credentials as an IAM role for API Gateway to invoke the authorizer.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer type. Valid values: `JWT`, `REQUEST`.
For WebSocket APIs, specify `REQUEST` for a Lambda function using incoming request parameters.
For HTTP APIs, specify `JWT` to use JSON Web Tokens.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer's Uniform Resource Identifier (URI).
For `REQUEST` authorizers this must be a well-formed Lambda function URI, such as the `invoke_arn` attribute of the [`aws.lambda.Function`](https://www.terraform.io/docs/providers/aws/r/lambda_function.html) resource.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Identity<wbr>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}The identity sources for which authorization is requested.
For `REQUEST` authorizers the value is a list of one or more mapping expressions of the specified request parameters.
For `JWT` authorizers the single entry specifies where to extract the JSON Web Token (JWT) from inbound requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Jwt<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#authorizerjwtconfiguration">Authorizer<wbr>Jwt<wbr>Configuration<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}The configuration of a JWT authorizer. Required for the `JWT` authorizer type.
Supported only for HTTP APIs.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the authorizer.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Api<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The API identifier.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Credentials<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The required credentials as an IAM role for API Gateway to invoke the authorizer.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer type. Valid values: `JWT`, `REQUEST`.
For WebSocket APIs, specify `REQUEST` for a Lambda function using incoming request parameters.
For HTTP APIs, specify `JWT` to use JSON Web Tokens.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authorizer<wbr>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer's Uniform Resource Identifier (URI).
For `REQUEST` authorizers this must be a well-formed Lambda function URI, such as the `invoke_arn` attribute of the [`aws.lambda.Function`](https://www.terraform.io/docs/providers/aws/r/lambda_function.html) resource.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Identity<wbr>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}The identity sources for which authorization is requested.
For `REQUEST` authorizers the value is a list of one or more mapping expressions of the specified request parameters.
For `JWT` authorizers the single entry specifies where to extract the JSON Web Token (JWT) from inbound requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Jwt<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#authorizerjwtconfiguration">Authorizer<wbr>Jwt<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The configuration of a JWT authorizer. Required for the `JWT` authorizer type.
Supported only for HTTP APIs.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the authorizer.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>api<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The API identifier.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer<wbr>Credentials<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The required credentials as an IAM role for API Gateway to invoke the authorizer.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer type. Valid values: `JWT`, `REQUEST`.
For WebSocket APIs, specify `REQUEST` for a Lambda function using incoming request parameters.
For HTTP APIs, specify `JWT` to use JSON Web Tokens.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer<wbr>Uri</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The authorizer's Uniform Resource Identifier (URI).
For `REQUEST` authorizers this must be a well-formed Lambda function URI, such as the `invoke_arn` attribute of the [`aws.lambda.Function`](https://www.terraform.io/docs/providers/aws/r/lambda_function.html) resource.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>identity<wbr>Sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}The identity sources for which authorization is requested.
For `REQUEST` authorizers the value is a list of one or more mapping expressions of the specified request parameters.
For `JWT` authorizers the single entry specifies where to extract the JSON Web Token (JWT) from inbound requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>jwt<wbr>Configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#authorizerjwtconfiguration">Authorizer<wbr>Jwt<wbr>Configuration</a></span>
    </dt>
    <dd>{{% md %}}The configuration of a JWT authorizer. Required for the `JWT` authorizer type.
Supported only for HTTP APIs.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the authorizer.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>api_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The API identifier.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer_<wbr>credentials_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The required credentials as an IAM role for API Gateway to invoke the authorizer.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The authorizer type. Valid values: `JWT`, `REQUEST`.
For WebSocket APIs, specify `REQUEST` for a Lambda function using incoming request parameters.
For HTTP APIs, specify `JWT` to use JSON Web Tokens.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authorizer_<wbr>uri</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The authorizer's Uniform Resource Identifier (URI).
For `REQUEST` authorizers this must be a well-formed Lambda function URI, such as the `invoke_arn` attribute of the [`aws.lambda.Function`](https://www.terraform.io/docs/providers/aws/r/lambda_function.html) resource.
Supported only for `REQUEST` authorizers.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>identity_<wbr>sources</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}The identity sources for which authorization is requested.
For `REQUEST` authorizers the value is a list of one or more mapping expressions of the specified request parameters.
For `JWT` authorizers the single entry specifies where to extract the JSON Web Token (JWT) from inbound requests.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>jwt_<wbr>configuration</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#authorizerjwtconfiguration">Dict[Authorizer<wbr>Jwt<wbr>Configuration]</a></span>
    </dt>
    <dd>{{% md %}}The configuration of a JWT authorizer. Required for the `JWT` authorizer type.
Supported only for HTTP APIs.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The name of the authorizer.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Authorizer<wbr>Jwt<wbr>Configuration</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#AuthorizerJwtConfiguration">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#AuthorizerJwtConfiguration">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/v2/go/aws/apigatewayv2?tab=doc#AuthorizerJwtConfigurationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/v2/go/aws/apigatewayv2?tab=doc#AuthorizerJwtConfigurationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Audiences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of the intended recipients of the JWT. A valid JWT must provide an aud that matches at least one entry in this list.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Issuer</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The base domain of the identity provider that issues JSON Web Tokens, such as the `endpoint` attribute of the [`aws.cognito.UserPool`](https://www.terraform.io/docs/providers/aws/r/cognito_user_pool.html) resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Audiences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}A list of the intended recipients of the JWT. A valid JWT must provide an aud that matches at least one entry in this list.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Issuer</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The base domain of the identity provider that issues JSON Web Tokens, such as the `endpoint` attribute of the [`aws.cognito.UserPool`](https://www.terraform.io/docs/providers/aws/r/cognito_user_pool.html) resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>audiences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}A list of the intended recipients of the JWT. A valid JWT must provide an aud that matches at least one entry in this list.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>issuer</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The base domain of the identity provider that issues JSON Web Tokens, such as the `endpoint` attribute of the [`aws.cognito.UserPool`](https://www.terraform.io/docs/providers/aws/r/cognito_user_pool.html) resource.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>audiences</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}A list of the intended recipients of the JWT. A valid JWT must provide an aud that matches at least one entry in this list.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>issuer</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The base domain of the identity provider that issues JSON Web Tokens, such as the `endpoint` attribute of the [`aws.cognito.UserPool`](https://www.terraform.io/docs/providers/aws/r/cognito_user_pool.html) resource.
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
