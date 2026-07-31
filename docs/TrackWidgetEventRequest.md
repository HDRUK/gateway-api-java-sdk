

# TrackWidgetEventRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**eventType** | [**EventTypeEnum**](#EventTypeEnum) |  |  |
|**entityId** | **Integer** |  |  [optional] |
|**entityType** | [**EntityTypeEnum**](#EntityTypeEnum) |  |  [optional] |
|**sourceDomain** | **String** |  |  [optional] |



## Enum: EventTypeEnum

| Name | Value |
|---- | -----|
| PAGE_VIEW | &quot;page_view&quot; |
| CODE_COPIED | &quot;code_copied&quot; |
| GATEWAY_CLICK | &quot;gateway_click&quot; |
| SEARCH | &quot;search&quot; |



## Enum: EntityTypeEnum

| Name | Value |
|---- | -----|
| DATASET | &quot;dataset&quot; |
| TOOL | &quot;tool&quot; |
| COLLECTION | &quot;collection&quot; |
| DUR | &quot;dur&quot; |



