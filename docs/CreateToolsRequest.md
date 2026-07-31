

# CreateToolsRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** |  |  [optional] |
|**url** | **String** |  |  [optional] |
|**description** | **String** |  |  [optional] |
|**resultsInsights** | **String** |  |  [optional] |
|**license** | **Integer** |  |  [optional] |
|**techStack** | **String** |  |  [optional] |
|**categoryId** | **Integer** |  |  [optional] |
|**userId** | **Integer** |  |  [optional] |
|**teamId** | **Integer** |  |  [optional] |
|**tags** | **List&lt;Long&gt;** |  |  [optional] |
|**dataset** | [**List&lt;CreateToolsIntegrationsRequestDatasetInner&gt;**](CreateToolsIntegrationsRequestDatasetInner.md) |  |  [optional] |
|**enabled** | **Integer** |  |  [optional] |
|**programmingLanguage** | **List&lt;Long&gt;** |  |  [optional] |
|**programmingPackage** | **List&lt;Long&gt;** |  |  [optional] |
|**typeCategory** | **List&lt;Long&gt;** |  |  [optional] |
|**associatedAuthors** | **String** |  |  [optional] |
|**contactAddress** | **String** |  |  [optional] |
|**publications** | [**List&lt;CreateToolsIntegrationsRequestPublicationsInner&gt;**](CreateToolsIntegrationsRequestPublicationsInner.md) |  |  [optional] |
|**durs** | **List&lt;Long&gt;** |  |  [optional] |
|**collections** | [**List&lt;CreateToolsRequestCollectionsInner&gt;**](CreateToolsRequestCollectionsInner.md) |  |  [optional] |
|**anyDataset** | **Boolean** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| DRAFT | &quot;DRAFT&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



