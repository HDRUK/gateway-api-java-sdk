

# DataAccessApplication

A Data Access Application (DAR) record managed by the Gateway

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Integer** |  |  [optional] |
|**applicantId** | **Integer** |  |  [optional] |
|**projectTitle** | **String** |  |  [optional] |
|**projectId** | **String** |  |  [optional] |
|**applicationType** | **String** |  |  [optional] |
|**submissionStatus** | [**SubmissionStatusEnum**](#SubmissionStatusEnum) |  |  [optional] |
|**approvalStatus** | [**ApprovalStatusEnum**](#ApprovalStatusEnum) |  |  [optional] |
|**isJoint** | **Boolean** |  |  [optional] |
|**statusReviewId** | **Integer** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |
|**deletedAt** | **OffsetDateTime** |  |  [optional] |



## Enum: SubmissionStatusEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;DRAFT&quot; |
| SUBMITTED | &quot;SUBMITTED&quot; |
| FEEDBACK | &quot;FEEDBACK&quot; |



## Enum: ApprovalStatusEnum

| Name | Value |
|---- | -----|
| APPROVED | &quot;APPROVED&quot; |
| APPROVED_COMMENTS | &quot;APPROVED_COMMENTS&quot; |
| REJECTED | &quot;REJECTED&quot; |
| WITHDRAWN | &quot;WITHDRAWN&quot; |



