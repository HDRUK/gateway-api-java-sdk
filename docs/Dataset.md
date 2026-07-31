

# Dataset

A dataset record managed by the Gateway

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**userId** | **Integer** |  |  [optional] |
|**teamId** | **Integer** |  |  [optional] |
|**pid** | **String** |  |  [optional] |
|**datasetid** | **String** |  |  [optional] |
|**version** | **Integer** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**createOrigin** | [**CreateOriginEnum**](#CreateOriginEnum) |  |  [optional] |
|**isCohortDiscovery** | **Boolean** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| DRAFT | &quot;DRAFT&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



## Enum: CreateOriginEnum

| Name | Value |
|---- | -----|
| MANUAL | &quot;MANUAL&quot; |
| API | &quot;API&quot; |
| GMI | &quot;GMI&quot; |



