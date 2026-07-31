

# EditCollectionsV2Request


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** |  |  [optional] |
|**description** | **String** |  |  [optional] |
|**imageLink** | **String** |  |  [optional] |
|**enabled** | **Boolean** |  |  [optional] |
|**keywords** | **List&lt;String&gt;** |  |  [optional] |
|**datasets** | [**List&lt;CreateTeamCollectionsRequestDatasetsInner&gt;**](CreateTeamCollectionsRequestDatasetsInner.md) |  |  [optional] |
|**dur** | [**List&lt;CreateTeamCollectionsRequestDatasetsInner&gt;**](CreateTeamCollectionsRequestDatasetsInner.md) |  |  [optional] |
|**publications** | [**List&lt;CreateTeamCollectionsRequestDatasetsInner&gt;**](CreateTeamCollectionsRequestDatasetsInner.md) |  |  [optional] |
|**collaborators** | **List&lt;Integer&gt;** |  |  [optional] |
|**_public** | **Boolean** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| DRAFT | &quot;DRAFT&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



