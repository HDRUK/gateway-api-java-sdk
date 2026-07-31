

# GetFederationHistory200ResponseDataInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**jobUuid** | **String** |  |  [optional] |
|**startedAt** | **OffsetDateTime** |  |  [optional] |
|**finishedAt** | **OffsetDateTime** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**message** | **String** |  |  [optional] |
|**failedDatasets** | [**List&lt;GetFederationHistory200ResponseDataInnerFailedDatasetsInner&gt;**](GetFederationHistory200ResponseDataInnerFailedDatasetsInner.md) |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| SUCCESS | &quot;success&quot; |
| FAILED | &quot;failed&quot; |
| IN_PROGRESS | &quot;in_progress&quot; |



