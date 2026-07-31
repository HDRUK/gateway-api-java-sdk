

# Tool

A software tool or model associated with datasets in the Gateway

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**name** | **String** |  |  [optional] |
|**url** | **URI** |  |  [optional] |
|**description** | **String** |  |  [optional] |
|**resultsInsights** | **String** |  |  [optional] |
|**license** | **Integer** | Foreign key to licenses table |  [optional] |
|**techStack** | **String** |  |  [optional] |
|**categoryId** | **Integer** |  |  [optional] |
|**userId** | **Integer** |  |  [optional] |
|**enabled** | **Boolean** |  |  [optional] |
|**associatedAuthors** | **String** |  |  [optional] |
|**contactAddress** | **String** |  |  [optional] |
|**anyDataset** | **Boolean** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**teamId** | **Integer** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| DRAFT | &quot;DRAFT&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



