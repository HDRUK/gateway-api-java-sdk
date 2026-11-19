

# ExperimentTrigger


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**on** | [**OnEnum**](#OnEnum) |  |  [optional] |
|**delaySeconds** | **Integer** |  |  [optional] |
|**frequency** | [**FrequencyEnum**](#FrequencyEnum) |  |  [optional] |



## Enum: OnEnum

| Name | Value |
|---- | -----|
| LOAD | &quot;load&quot; |
| DELAY | &quot;delay&quot; |
| EXIT_INTENT | &quot;exitIntent&quot; |



## Enum: FrequencyEnum

| Name | Value |
|---- | -----|
| ONCE | &quot;once&quot; |
| UNTIL_ANSWERED | &quot;untilAnswered&quot; |
| ALWAYS | &quot;always&quot; |



