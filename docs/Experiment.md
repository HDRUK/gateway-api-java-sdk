

# Experiment

A feedback prompt or design review shown to targeted visitors

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**name** | **String** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**definition** | [**ExperimentDefinition**](ExperimentDefinition.md) |  |  [optional] |
|**targeting** | [**ExperimentTargeting**](ExperimentTargeting.md) |  |  [optional] |
|**trigger** | [**ExperimentTrigger**](ExperimentTrigger.md) |  |  [optional] |
|**startsAt** | **LocalDate** |  |  [optional] |
|**endsAt** | **LocalDate** |  |  [optional] |
|**createdBy** | **Integer** |  |  [optional] |
|**responsesCount** | **Integer** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |
|**deletedAt** | **OffsetDateTime** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;draft&quot; |
| ACTIVE | &quot;active&quot; |
| PAUSED | &quot;paused&quot; |
| ARCHIVED | &quot;archived&quot; |



