

# DatasetVersion

A versioned snapshot of dataset metadata in GWDM format

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**datasetId** | **Integer** |  |  [optional] |
|**version** | **Integer** |  |  [optional] |
|**title** | **String** |  |  [optional] |
|**shortTitle** | **String** |  |  [optional] |
|**metadata** | **Object** | Full GWDM-format metadata document for this version |  [optional] |
|**patch** | **List&lt;Object&gt;** | RFC 6902 JSON Patch array used to reconstruct this version from the previous snapshot. Null for full snapshots (v1 and every 10th version). |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |



