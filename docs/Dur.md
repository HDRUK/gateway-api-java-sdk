

# Dur

A Data Use Register (DUR) entry describing an approved use of one or more datasets

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**projectTitle** | **String** |  |  [optional] |
|**projectIdText** | **String** |  |  [optional] |
|**organisationName** | **String** |  |  [optional] |
|**organisationSector** | **String** |  |  [optional] |
|**sectorId** | **Integer** |  |  [optional] |
|**laySummary** | **String** |  |  [optional] |
|**technicalSummary** | **String** |  |  [optional] |
|**latestApprovalDate** | **LocalDate** |  |  [optional] |
|**manualUpload** | **Boolean** |  |  [optional] |
|**rejectionReason** | **String** |  |  [optional] |
|**sublicenceArrangements** | **String** |  |  [optional] |
|**publicBenefitStatement** | **String** |  |  [optional] |
|**dataSensitivityLevel** | **String** |  |  [optional] |
|**projectStartDate** | **LocalDate** |  |  [optional] |
|**projectEndDate** | **LocalDate** |  |  [optional] |
|**accessDate** | **LocalDate** |  |  [optional] |
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
|**nonGatewayDatasets** | **List&lt;String&gt;** |  |  [optional] |
|**nonGatewayApplicants** | **List&lt;String&gt;** |  |  [optional] |
|**fundersAndSponsors** | **List&lt;String&gt;** |  |  [optional] |
|**otherApprovalCommittees** | **List&lt;String&gt;** |  |  [optional] |
|**gatewayOutputsTools** | **List&lt;String&gt;** |  |  [optional] |
|**gatewayOutputsPapers** | **List&lt;String&gt;** |  |  [optional] |
|**nonGatewayOutputs** | **List&lt;String&gt;** |  |  [optional] |
|**enabled** | **Boolean** |  |  [optional] |
|**lastActivity** | **OffsetDateTime** |  |  [optional] |
|**counter** | **Integer** |  |  [optional] |
|**userId** | **Integer** |  |  [optional] |
|**teamId** | **Integer** |  |  [optional] |
|**applicantId** | **Integer** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| DRAFT | &quot;DRAFT&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



