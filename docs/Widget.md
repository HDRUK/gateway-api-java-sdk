

# Widget

A widget record managed by the Gateway

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**teamId** | **Integer** |  |  [optional] |
|**dataCustodianEntitiesIds** | **String** |  |  [optional] |
|**includedDatasets** | **String** |  |  [optional] |
|**includedDataUses** | **String** |  |  [optional] |
|**includedScripts** | **String** |  |  [optional] |
|**includedCollections** | **String** |  |  [optional] |
|**includeSearchBar** | **Boolean** |  |  [optional] |
|**includeCohortLink** | **Boolean** |  |  [optional] |
|**sizeWidth** | **Integer** |  |  [optional] |
|**sizeHeight** | **Integer** |  |  [optional] |
|**unit** | [**UnitEnum**](#UnitEnum) |  |  [optional] |
|**keepProportions** | **Boolean** |  |  [optional] |
|**widgetName** | **String** |  |  [optional] |
|**permittedDomains** | **String** |  |  [optional] |
|**brandingPrimary** | **String** |  |  [optional] |
|**brandingSecondary** | **String** |  |  [optional] |
|**brandingNeutral** | **String** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |



## Enum: UnitEnum

| Name | Value |
|---- | -----|
| PX | &quot;px&quot; |
| PERCENT | &quot;%&quot; |
| REM | &quot;rem&quot; |



