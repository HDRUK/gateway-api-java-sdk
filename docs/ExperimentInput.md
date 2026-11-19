

# ExperimentInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**definition** | **Object** | See Experiment.definition |  |
|**targeting** | **Object** | See Experiment.targeting |  |
|**trigger** | **Object** | See Experiment.trigger |  |
|**startsAt** | **LocalDate** |  |  [optional] |
|**endsAt** | **LocalDate** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;draft&quot; |
| ACTIVE | &quot;active&quot; |
| PAUSED | &quot;paused&quot; |
| ARCHIVED | &quot;archived&quot; |



