

# ExperimentResponseInput


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**answers** | **Object** | Answers keyed by question block id; unknown ids are dropped |  |
|**path** | **String** |  |  |
|**variant** | **String** |  |  [optional] |
|**contact** | **Boolean** |  |  [optional] |
|**email** | **String** | Required when contact is true and not signed in |  [optional] |
|**recaptcha** | **String** | reCAPTCHA v3 token for the experiment_response action |  |



