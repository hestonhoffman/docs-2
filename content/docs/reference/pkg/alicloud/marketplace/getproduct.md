
---
title: "GetProduct"
block_external_search_index: true
---



This data source provides the Market product item details of Alibaba Cloud.

> **NOTE:** Available in 1.69.0+

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const defaultProduct = pulumi.output(alicloud.marketplace.getProduct({
    productCode: "cmapi022206",
}, { async: true }));

export const productName = defaultProduct.products[0].name;
export const firstProductSkuCode = defaultProduct.products[0].skuses[0].skuCode;
export const firstProductPackageVersion = defaultProduct.products[0].skuses[0].packageVersions[0].packageVersion;
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-alicloud/blob/master/website/docs/d/market_product.html.markdown.





## Using GetProduct

{{< chooser language "javascript,typescript,python,go,csharp" / >}}


{{% choosable language typescript %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getProduct<span class="p">(</span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/marketplace/#GetProductArgs">GetProductArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/alicloud/marketplace/#GetProductResult">GetProductResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_product(</span>available_region=None<span class="p">, </span>product_code=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupProduct<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/marketplace?tab=doc#LookupProductArgs">LookupProductArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/marketplace?tab=doc#LookupProductResult">LookupProductResult</a></span>, error)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetProduct </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.Marketplace.GetProductResult.html">GetProductResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Alicloud/Pulumi.Alicloud.MarketPlace.GetProductArgs.html">GetProductArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span>? <span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Available<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A available region id used to filter market place Ecs images.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Product<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The product code of the market product.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Available<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A available region id used to filter market place Ecs images.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Product<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The product code of the market product.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>available<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A available region id used to filter market place Ecs images.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>product<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The product code of the market product.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>available_<wbr>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A available region id used to filter market place Ecs images.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>product_<wbr>code</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The product code of the market product.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetProduct Result

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Available<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Product<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Products</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproduct">List&lt;Get<wbr>Product<wbr>Product&gt;</a></span>
    </dt>
    <dd>{{% md %}}A product. It contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Available<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Product<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Products</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproduct">[]Get<wbr>Product<wbr>Product</a></span>
    </dt>
    <dd>{{% md %}}A product. It contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>available<wbr>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>product<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>products</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproduct">Get<wbr>Product<wbr>Product[]</a></span>
    </dt>
    <dd>{{% md %}}A product. It contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>available_<wbr>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}id is the provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>product_<wbr>code</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>products</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproduct">List[Get<wbr>Product<wbr>Product]</a></span>
    </dt>
    <dd>{{% md %}}A product. It contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Supporting Types

<h4>Get<wbr>Product<wbr>Product</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#GetProductProduct">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/marketplace?tab=doc#GetProductProduct">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The code of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Skuses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskus">List&lt;Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of one element containing sku attributes of an object. Each element contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The code of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Skuses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskus">[]Get<wbr>Product<wbr>Product<wbr>Skus</a></span>
    </dt>
    <dd>{{% md %}}A list of one element containing sku attributes of an object. Each element contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The code of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>skuses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskus">Get<wbr>Product<wbr>Product<wbr>Skus[]</a></span>
    </dt>
    <dd>{{% md %}}A list of one element containing sku attributes of an object. Each element contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>code</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The code of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the product.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>skuses</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskus">List[Get<wbr>Product<wbr>Product<wbr>Skus]</a></span>
    </dt>
    <dd>{{% md %}}A list of one element containing sku attributes of an object. Each element contains the following attributes:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Get<wbr>Product<wbr>Product<wbr>Skus</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#GetProductProductSkus">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/marketplace?tab=doc#GetProductProductSkus">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Images</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskusimage">List&lt;Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Image<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}The list of custom ECS images, Each element contains the following attributes:
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Package<wbr>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskuspackageversion">List&lt;Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Package<wbr>Version<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}The list of package version details of this product sku, Each element contains the following attributes:
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Sku<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The sku code of this product sku.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Sku<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The sku name of this product sku.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Images</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskusimage">[]Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Image</a></span>
    </dt>
    <dd>{{% md %}}The list of custom ECS images, Each element contains the following attributes:
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Package<wbr>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskuspackageversion">[]Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Package<wbr>Version</a></span>
    </dt>
    <dd>{{% md %}}The list of package version details of this product sku, Each element contains the following attributes:
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Sku<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The sku code of this product sku.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Sku<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The sku name of this product sku.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>images</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskusimage">Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Image[]</a></span>
    </dt>
    <dd>{{% md %}}The list of custom ECS images, Each element contains the following attributes:
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>package<wbr>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskuspackageversion">Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Package<wbr>Version[]</a></span>
    </dt>
    <dd>{{% md %}}The list of package version details of this product sku, Each element contains the following attributes:
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>sku<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The sku code of this product sku.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>sku<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The sku name of this product sku.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>images</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskusimage">List[Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Image]</a></span>
    </dt>
    <dd>{{% md %}}The list of custom ECS images, Each element contains the following attributes:
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>package<wbr>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getproductproductskuspackageversion">List[Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Package<wbr>Version]</a></span>
    </dt>
    <dd>{{% md %}}The list of package version details of this product sku, Each element contains the following attributes:
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>sku<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The sku code of this product sku.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>sku<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The sku name of this product sku.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Image</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#GetProductProductSkusImage">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/marketplace?tab=doc#GetProductProductSkusImage">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Ecs image id.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Image<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Ecs image display name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Region<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Ecs image region.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Ecs image id.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Image<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Ecs image display name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Region<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Ecs image region.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>image<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Ecs image id.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>image<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Ecs image display name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>region<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Ecs image region.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>image_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Ecs image id.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>image_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Ecs image display name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>region<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Ecs image region.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Get<wbr>Product<wbr>Product<wbr>Skus<wbr>Package<wbr>Version</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#GetProductProductSkusPackageVersion">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-alicloud/sdk/go/alicloud/marketplace?tab=doc#GetProductProductSkusPackageVersion">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Package<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The package name of this product sku package.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Package<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The package version of this product sku package. Currently, the API products can return package_version, but others can not for ensure.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Package<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The package name of this product sku package.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Package<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The package version of this product sku package. Currently, the API products can return package_version, but others can not for ensure.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>package<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The package name of this product sku package.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>package<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The package version of this product sku package. Currently, the API products can return package_version, but others can not for ensure.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>package<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The package name of this product sku package.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>package_<wbr>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The package version of this product sku package. Currently, the API products can return package_version, but others can not for ensure.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







