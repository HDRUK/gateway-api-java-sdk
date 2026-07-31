

# SavedSearch

A user's saved search definition

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**userId** | **Integer** |  |  [optional] |
|**name** | **String** |  |  [optional] |
|**searchTerm** | **String** |  |  [optional] |
|**searchEndpoint** | **String** |  |  [optional] |
|**sortOrder** | [**SortOrderEnum**](#SortOrderEnum) |  |  [optional] |
|**enabled** | **Boolean** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |
|**deletedAt** | **OffsetDateTime** |  |  [optional] |



## Enum: SortOrderEnum

| Name | Value |
|---- | -----|
| SCORE_DESC | &quot;score:desc&quot; |
| NAME_ASC | &quot;name:asc&quot; |
| NAME_DESC | &quot;name:desc&quot; |
| CREATED_AT_ASC | &quot;created_at:asc&quot; |
| CREATED_AT_DESC | &quot;created_at:desc&quot; |



