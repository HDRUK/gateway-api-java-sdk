

# UpdatePublicationsRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**paperTitle** | **String** |  |  [optional] |
|**authors** | **String** |  |  [optional] |
|**yearOfPublication** | **String** |  |  [optional] |
|**paperDoi** | **String** |  |  [optional] |
|**publicationType** | **String** |  |  [optional] |
|**journalName** | **String** |  |  [optional] |
|**_abstract** | **String** |  |  [optional] |
|**url** | **String** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**datasets** | [**List&lt;CreatePublicationsRequestDatasetsInner&gt;**](CreatePublicationsRequestDatasetsInner.md) |  |  [optional] |
|**tools** | [**List&lt;CreatePublicationsRequestToolsInner&gt;**](CreatePublicationsRequestToolsInner.md) |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| DRAFT | &quot;DRAFT&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



