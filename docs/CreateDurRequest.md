

# CreateDurRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**nonGatewayDatasets** | **List&lt;String&gt;** |  |  [optional] |
|**nonGatewayApplicants** | **List&lt;String&gt;** |  |  [optional] |
|**fundersAndSponsors** | **List&lt;String&gt;** |  |  [optional] |
|**otherApprovalCommittees** | **List&lt;String&gt;** |  |  [optional] |
|**gatewayOutputsTools** | **List&lt;String&gt;** |  |  [optional] |
|**gatewayOutputsPapers** | **List&lt;String&gt;** |  |  [optional] |
|**nonGatewayOutputs** | **List&lt;String&gt;** |  |  [optional] |
|**projectTitle** | **String** |  |  [optional] |
|**projectIdText** | **String** |  |  [optional] |
|**organisationName** | **String** |  |  [optional] |
|**organisationSector** | **String** |  |  [optional] |
|**laySummary** | **String** |  |  [optional] |
|**technicalSummary** | **String** |  |  [optional] |
|**latestApprovalDate** | **OffsetDateTime** |  |  [optional] |
|**manualUpload** | **Boolean** |  |  [optional] |
|**rejectionReason** | **String** |  |  [optional] |
|**sublicenceArrangements** | **String** |  |  [optional] |
|**publicBenefitStatement** | **String** |  |  [optional] |
|**dataSensitivityLevel** | **String** |  |  [optional] |
|**projectStartDate** | **OffsetDateTime** |  |  [optional] |
|**projectEndDate** | **OffsetDateTime** |  |  [optional] |
|**accessDate** | **OffsetDateTime** |  |  [optional] |
|**accreditedResearcherStatus** | **String** |  |  [optional] |
|**confidentialDataDescription** | **String** |  |  [optional] |
|**datasetLinkageDescription** | **String** |  |  [optional] |
|**dutyOfConfidentiality** | **String** |  |  [optional] |
|**legalBasisForDataArticle6** | **String** |  |  [optional] |
|**legalBasisForDataArticle9** | **String** |  |  [optional] |
|**nationalDataOptout** | **String** |  |  [optional] |
|**organisationId** | **String** |  |  [optional] |
|**privacyEnhancements** | **String** |  |  [optional] |
|**requestCategoryType** | **String** |  |  [optional] |
|**requestFrequency** | **String** |  |  [optional] |
|**accessType** | **String** |  |  [optional] |
|**mongoObjectDarId** | **String** |  |  [optional] |
|**enabled** | **Boolean** |  |  [optional] |
|**lastActivity** | **OffsetDateTime** |  |  [optional] |
|**counter** | **Integer** |  |  [optional] |
|**mongoObjectId** | **String** |  |  [optional] |
|**mongoId** | **String** |  |  [optional] |
|**datasets** | [**List&lt;CreateDurRequestDatasetsInner&gt;**](CreateDurRequestDatasetsInner.md) |  |  [optional] |
|**publications** | [**List&lt;CreateDurRequestPublicationsInner&gt;**](CreateDurRequestPublicationsInner.md) |  |  [optional] |
|**keywords** | **List&lt;String&gt;** |  |  [optional] |
|**users** | [**List&lt;CreateDurRequestUsersInner&gt;**](CreateDurRequestUsersInner.md) |  |  [optional] |
|**user** | [**List&lt;CreateDurRequestUsersInner&gt;**](CreateDurRequestUsersInner.md) |  |  [optional] |
|**team** | [**List&lt;CreateDurRequestTeamInner&gt;**](CreateDurRequestTeamInner.md) |  |  [optional] |
|**applicantId** | **String** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| DRAFT | &quot;DRAFT&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



