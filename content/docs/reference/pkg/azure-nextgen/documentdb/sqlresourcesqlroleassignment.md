
---
title: "SqlResourceSqlRoleAssignment"
title_tag: "Resource SqlResourceSqlRoleAssignment | Module documentdb | Package Azure NextGen"
meta_desc: "Explore the SqlResourceSqlRoleAssignment resource of the documentdb module, including examples, input properties, output properties, lookup functions, and supporting types. An Azure Cosmos DB Role Assignment"
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

An Azure Cosmos DB Role Assignment

{{% examples %}}
## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}
### CosmosDBSqlRoleAssignmentCreateUpdate
{{% example csharp %}}
```csharp
using Pulumi;
using AzureNextGen = Pulumi.AzureNextGen;

class MyStack : Stack
{
    public MyStack()
    {
        var sqlResourceSqlRoleAssignment = new AzureNextGen.DocumentDB.V20200601Preview.SqlResourceSqlRoleAssignment("sqlResourceSqlRoleAssignment", new AzureNextGen.DocumentDB.V20200601Preview.SqlResourceSqlRoleAssignmentArgs
        {
            AccountName = "myAccountName",
            PrincipalId = "myPrincipalId",
            ResourceGroupName = "myResourceGroupName",
            RoleAssignmentId = "myRoleAssignmentId",
            RoleDefinitionId = "/subscriptions/mySubscriptionId/resourceGroups/myResourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlRoleDefinitions/myRoleDefinitionId",
            Scope = "/subscriptions/mySubscriptionId/resourceGroups/myResourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/dbs/purchases/colls/redmond-purchases",
        });
    }

}

```

{{% /example %}}

{{% example go %}}

```go
package main

import (
	documentdb "github.com/pulumi/pulumi-azure-nextgen/sdk/go/azure/documentdb/v20200601preview"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := documentdb.NewSqlResourceSqlRoleAssignment(ctx, "sqlResourceSqlRoleAssignment", &documentdb.SqlResourceSqlRoleAssignmentArgs{
			AccountName:       pulumi.String("myAccountName"),
			PrincipalId:       pulumi.String("myPrincipalId"),
			ResourceGroupName: pulumi.String("myResourceGroupName"),
			RoleAssignmentId:  pulumi.String("myRoleAssignmentId"),
			RoleDefinitionId:  pulumi.String("/subscriptions/mySubscriptionId/resourceGroups/myResourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlRoleDefinitions/myRoleDefinitionId"),
			Scope:             pulumi.String("/subscriptions/mySubscriptionId/resourceGroups/myResourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/dbs/purchases/colls/redmond-purchases"),
		})
		if err != nil {
			return err
		}
		return nil
	})
}

```

{{% /example %}}

{{% example python %}}

```python
import pulumi
import pulumi_azure_nextgen as azure_nextgen

sql_resource_sql_role_assignment = azure_nextgen.documentdb.v20200601preview.SqlResourceSqlRoleAssignment("sqlResourceSqlRoleAssignment",
    account_name="myAccountName",
    principal_id="myPrincipalId",
    resource_group_name="myResourceGroupName",
    role_assignment_id="myRoleAssignmentId",
    role_definition_id="/subscriptions/mySubscriptionId/resourceGroups/myResourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlRoleDefinitions/myRoleDefinitionId",
    scope="/subscriptions/mySubscriptionId/resourceGroups/myResourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/dbs/purchases/colls/redmond-purchases")

```

{{% /example %}}

{{% example typescript %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure_nextgen from "@pulumi/azure-nextgen";

const sqlResourceSqlRoleAssignment = new azure_nextgen.documentdb.v20200601preview.SqlResourceSqlRoleAssignment("sqlResourceSqlRoleAssignment", {
    accountName: "myAccountName",
    principalId: "myPrincipalId",
    resourceGroupName: "myResourceGroupName",
    roleAssignmentId: "myRoleAssignmentId",
    roleDefinitionId: "/subscriptions/mySubscriptionId/resourceGroups/myResourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlRoleDefinitions/myRoleDefinitionId",
    scope: "/subscriptions/mySubscriptionId/resourceGroups/myResourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/dbs/purchases/colls/redmond-purchases",
});

```

{{% /example %}}

{{% /examples %}}


## Create a SqlResourceSqlRoleAssignment Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">SqlResourceSqlRoleAssignment</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span><span class="p">:</span> <span class="nx">SqlResourceSqlRoleAssignmentArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nx">SqlResourceSqlRoleAssignment</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">, </span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">, </span><span class="nx">account_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">principal_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">role_assignment_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">role_definition_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">, </span><span class="nx">scope</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewSqlResourceSqlRoleAssignment</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span><span class="p"> </span><span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> </span><span class="nx">SqlResourceSqlRoleAssignmentArgs</span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">SqlResourceSqlRoleAssignment</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">SqlResourceSqlRoleAssignment</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span><span class="p"> </span><span class="nx">name<span class="p">, </span><span class="nx">SqlResourceSqlRoleAssignmentArgs</span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
  
    <dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>
      The unique name of the resource.
    </dd>
  
    <dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type">SqlResourceSqlRoleAssignmentArgs</span>
    </dt>
    <dd>
      The arguments to resource properties.
    </dd>
  
    <dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span>
    </dt>
    <dd>
      Bag of options to control resource&#39;s behavior.
    </dd>
  

</dl>

{{% /choosable %}}

{{% choosable language python %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type">
            <a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">ResourceOptions</a>
        </span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
  
    <dt
        class="property-optional" title="Optional">
        <span>ctx</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span>
    </dt>
    <dd>
      Context object for the current deployment.
    </dd>
  
    <dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>
      The unique name of the resource.
    </dd>
  
    <dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type">SqlResourceSqlRoleAssignmentArgs</span>
    </dt>
    <dd>
      The arguments to resource properties.
    </dd>
  
    <dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span>
    </dt>
    <dd>
      Bag of options to control resource&#39;s behavior.
    </dd>
  

</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
  
    <dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>
      The unique name of the resource.
    </dd>
  
    <dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type">SqlResourceSqlRoleAssignmentArgs</span>
    </dt>
    <dd>
      The arguments to resource properties.
    </dd>
  
    <dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>
      Bag of options to control resource&#39;s behavior.
    </dd>
  

</dl>

{{% /choosable %}}

## SqlResourceSqlRoleAssignment Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/programming-model#outputs" >}}) in the Programming Model docs.

### Inputs

The SqlResourceSqlRoleAssignment resource accepts the following [input]({{< relref "/docs/intro/concepts/programming-model#outputs" >}}) properties:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="accountname_csharp">
<a href="#accountname_csharp" style="color: inherit; text-decoration: inherit;">Account<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}Cosmos DB database account name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the resource group. The name is case insensitive.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="roleassignmentid_csharp">
<a href="#roleassignmentid_csharp" style="color: inherit; text-decoration: inherit;">Role<wbr>Assignment<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The GUID for the Role Assignment.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="principalid_csharp">
<a href="#principalid_csharp" style="color: inherit; text-decoration: inherit;">Principal<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The unique identifier for the associated AAD principal in the AAD graph to which access is being granted through this Role Assignment. Tenant ID for the principal is inferred using the tenant associated with the subscription.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="roledefinitionid_csharp">
<a href="#roledefinitionid_csharp" style="color: inherit; text-decoration: inherit;">Role<wbr>Definition<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The unique identifier for the associated Role Definition.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="scope_csharp">
<a href="#scope_csharp" style="color: inherit; text-decoration: inherit;">Scope</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The data plane resource path for which access is being granted through this Role Assignment.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="accountname_go">
<a href="#accountname_go" style="color: inherit; text-decoration: inherit;">Account<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}Cosmos DB database account name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the resource group. The name is case insensitive.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="roleassignmentid_go">
<a href="#roleassignmentid_go" style="color: inherit; text-decoration: inherit;">Role<wbr>Assignment<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The GUID for the Role Assignment.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="principalid_go">
<a href="#principalid_go" style="color: inherit; text-decoration: inherit;">Principal<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The unique identifier for the associated AAD principal in the AAD graph to which access is being granted through this Role Assignment. Tenant ID for the principal is inferred using the tenant associated with the subscription.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="roledefinitionid_go">
<a href="#roledefinitionid_go" style="color: inherit; text-decoration: inherit;">Role<wbr>Definition<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The unique identifier for the associated Role Definition.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="scope_go">
<a href="#scope_go" style="color: inherit; text-decoration: inherit;">Scope</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The data plane resource path for which access is being granted through this Role Assignment.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="accountname_nodejs">
<a href="#accountname_nodejs" style="color: inherit; text-decoration: inherit;">account<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}Cosmos DB database account name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the resource group. The name is case insensitive.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="roleassignmentid_nodejs">
<a href="#roleassignmentid_nodejs" style="color: inherit; text-decoration: inherit;">role<wbr>Assignment<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The GUID for the Role Assignment.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="principalid_nodejs">
<a href="#principalid_nodejs" style="color: inherit; text-decoration: inherit;">principal<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The unique identifier for the associated AAD principal in the AAD graph to which access is being granted through this Role Assignment. Tenant ID for the principal is inferred using the tenant associated with the subscription.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="roledefinitionid_nodejs">
<a href="#roledefinitionid_nodejs" style="color: inherit; text-decoration: inherit;">role<wbr>Definition<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The unique identifier for the associated Role Definition.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="scope_nodejs">
<a href="#scope_nodejs" style="color: inherit; text-decoration: inherit;">scope</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The data plane resource path for which access is being granted through this Role Assignment.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="account_name_python">
<a href="#account_name_python" style="color: inherit; text-decoration: inherit;">account_<wbr>name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}Cosmos DB database account name.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The name of the resource group. The name is case insensitive.{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="role_assignment_id_python">
<a href="#role_assignment_id_python" style="color: inherit; text-decoration: inherit;">role_<wbr>assignment_<wbr>id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The GUID for the Role Assignment.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="principal_id_python">
<a href="#principal_id_python" style="color: inherit; text-decoration: inherit;">principal_<wbr>id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The unique identifier for the associated AAD principal in the AAD graph to which access is being granted through this Role Assignment. Tenant ID for the principal is inferred using the tenant associated with the subscription.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="role_definition_id_python">
<a href="#role_definition_id_python" style="color: inherit; text-decoration: inherit;">role_<wbr>definition_<wbr>id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The unique identifier for the associated Role Definition.{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="scope_python">
<a href="#scope_python" style="color: inherit; text-decoration: inherit;">scope</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The data plane resource path for which access is being granted through this Role Assignment.{{% /md %}}</dd>

</dl>
{{% /choosable %}}






### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the SqlResourceSqlRoleAssignment resource produces the following output properties:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the database account.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The type of Azure resource.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the database account.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The type of Azure resource.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the database account.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The type of Azure resource.{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The name of the database account.{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The type of Azure resource.{{% /md %}}</dd>

</dl>
{{% /choosable %}}












<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-nextgen">https://github.com/pulumi/pulumi-azure-nextgen</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
