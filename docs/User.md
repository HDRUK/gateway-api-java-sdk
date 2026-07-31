

# User

A registered Gateway user

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**name** | **String** |  |  [optional] |
|**firstname** | **String** |  |  [optional] |
|**lastname** | **String** |  |  [optional] |
|**email** | **String** |  |  [optional] |
|**secondaryEmail** | **String** |  |  [optional] |
|**preferredEmail** | [**PreferredEmailEnum**](#PreferredEmailEnum) |  |  [optional] |
|**provider** | **String** |  |  [optional] |
|**sectorId** | **Integer** |  |  [optional] |
|**organisation** | **String** |  |  [optional] |
|**bio** | **String** |  |  [optional] |
|**domain** | **String** |  |  [optional] |
|**link** | **URI** |  |  [optional] |
|**orcid** | **String** |  |  [optional] |
|**contactFeedback** | **Boolean** |  |  [optional] |
|**contactNews** | **Boolean** |  |  [optional] |
|**isAdmin** | **Boolean** |  |  [optional] |
|**terms** | **Boolean** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |



## Enum: PreferredEmailEnum

| Name | Value |
|---- | -----|
| PRIMARY | &quot;primary&quot; |
| SECONDARY | &quot;secondary&quot; |



