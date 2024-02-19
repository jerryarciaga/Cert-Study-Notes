# Introduction to ARM Templates
## What is Infrastructure as Code?
The process of **managing and provisioning** computer data centers (eg, Azure) through machine-readable **definition files** (eg. JSON files) rather than physical hardware configuration or interactive configuration tools.
You write a script that will setup cloud services for you.
IaC's can either be:
* **Declarative** - You defined exactly what you want, and you get exactly that
* **Imperative** - You define what you generally want, and the service will guess what you want
**ARM templates** are **JSON files that define Azure Resources** you want to provision and Azure Services you want to configure.
* With ARM Templates you can:
	* **ARM Templates** are declarative.
	* stand up, tear down or share entire architectures in minutes
	* Reduce configuration mistakes
	* Know exactly what you have defined for a stack to establish an architecture baseline for compliance
# ARM Templates
* With ARM templates you can:
	* **ARM Templates** are declarative (you get exactly what you define)
	* stand up, tear down or share entire architectures in minutes
	* Reduce configuration mistakes
	* Establish an architecture baseline for compliance
	* **Modularity** Break up your architecture in multiple files and reuse them
	* **Extensibility** Add PowerShell and Bash scripts to your templates
	* **Testing** YOu can use the ARM template tool kit (`arm-ttk`)
	* **Preview Changes** Before you create infrastructure via template, see what it will create
	* **Built-In Validation** Will only deploy your template if it passes
	* **Tracked Deployments** Keep track of changes to architecture over time
	* **Policy as Code** Apply Azure policies to ensure you remain compliant
	* **Microsoft Blueprints** establishes relationship between resource and the template
	* **CI/CD integration**
	* **Exportable Code** (exporting the current state of a resource groups and resources)
	* **Authoring Tools** Visual Studio Code has advanced features for authoring ARM Templates
# ARM Template Skeleton
**Skeleton** The general structure of an ARM template
```
{
	"$schema":"https://something.json",
	"contentVersion": "1.0.0.",
	"apiProfile": "",
	"parameters": { },
	"variables": { },
	"functions": [ ],
	"resources": [ ],
	"outputs": { }
}
```

* `$schema` describes the properties that are available within a template
* `contentVersion` the version of the template. You can provide any value for this element
* `apiProfile` Use this value to avoid having to specify API versions for each resource in the template
* `parameters` values you can pass along to your template
* `variables` you transform parameters or resource properties using function expressions
* `functions` User-defined functions available within the template
* `resources` the Azure resources you'll want to deploy or update
* `outputs` values that are returned after deployment
# ARM Template Resources
**Resource** An Azure Resource you want to provision
* `type` Type of the resources. Follows the format of `{ResourceProvider}/ResourceType`
* `apiVersion` Version of the REST API to use for the resource. Each resource provider published its own API versions
* `name` Name of the resource
* `location` Most resources have a location property. The region where the resource will be deployed
* `Other Properties` Varies per resource types
# ARM Template Parameters
**Parameters** Allow you to pass variables to your ARM template
* `type` the expected data type of the inputted value
	* `string`, `securestring`, `int`, `bool`, `object`, `secureObject`, and `array`
* `defaultValue` if no value is provided it will be set to this value
* `allowedValues` an array of allowed values
* `minValue` the minimal possible value
* `maxValue` the maximum possible value
* `minLength` minimum length of characters or array
* `maxLength` maximum length of characters or array
* `description` the description that will be displayed in the Azure Portal
# ARM Template Functions
**Functions** Allow you to apply transformation to your ARM variables
* Template Functions - built-in functions
* User-Defined Functions - custom functions you create
* Functions are called using **parentheses**
	* Example: `{"condition": "[equals(parameters('newOrExisting'),'new')]"}
* **Template Functions**
* **Array**: array, concat, contains, createArray, empty, first, intersection, last, length, min, max, range, skip, take, union
* **Comparison**: coalesce, equals, less, lessOrEquals, greater, greaterOrEquals
* **Date**: dateTimeAdd, utcNow
* **Deployment**: deployment, environment, **parameters**, **variables**
* **Logical**: and, or, if, not
* **Numeric**: add, copyIndex, div, float, int, min, max, mod, mul, sub
* **Object**
* **Resource**
* **String**
# ARM Template Variables
**Variables** Template variables are used to simplify your arm templates. You transform parameters and resource properties using functions and then assign them into a reusable variable.
**Nested Variables** You can use json object to have nested variables to scope your variables for multiple use cases
# ARM Template Output
**Outputs** Return values from deployed resources, so you can use them programmatically.
You can specify **the type and value** under outputs