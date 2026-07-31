# FormHydrationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getFormSchema**](FormHydrationApi.md#getFormSchema) | **GET** /api/v1/form_hydration/schema | Retrieve form schema data |
| [**onboardingFormHydration**](FormHydrationApi.md#onboardingFormHydration) | **GET** /api/v1/form_hydration | Retrieve form schema data |


<a id="getFormSchema"></a>
# **getFormSchema**
> Object getFormSchema(model, version)

Retrieve form schema data

Retrieves form schema data based on the provided model and version.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.FormHydrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    FormHydrationApi apiInstance = new FormHydrationApi(defaultClient);
    String model = "model_example"; // String | The model for which form schema is requested.
    String version = "version_example"; // String | The version of the model for which form schema is requested.
    try {
      Object result = apiInstance.getFormSchema(model, version);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FormHydrationApi#getFormSchema");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **model** | **String**| The model for which form schema is requested. | [optional] |
| **version** | **String**| The version of the model for which form schema is requested. | [optional] |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Bad request. Missing required parameters or invalid parameters. |  -  |
| **500** | Internal server error. Failed to retrieve form schema data. |  -  |

<a id="onboardingFormHydration"></a>
# **onboardingFormHydration**
> Object onboardingFormHydration(name, version, dataTypes)

Retrieve form schema data

Retrieves form schema data based on the provided model and version.

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.FormHydrationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    FormHydrationApi apiInstance = new FormHydrationApi(defaultClient);
    String name = "name_example"; // String | The model name for which form schema is requested.
    String version = "version_example"; // String | The version of the model for which form schema is requested.
    String dataTypes = "dataTypes_example"; // String | The data types of the dataset about to be onboarded.
    try {
      Object result = apiInstance.onboardingFormHydration(name, version, dataTypes);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FormHydrationApi#onboardingFormHydration");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **name** | **String**| The model name for which form schema is requested. | [optional] |
| **version** | **String**| The version of the model for which form schema is requested. | [optional] |
| **dataTypes** | **String**| The data types of the dataset about to be onboarded. | [optional] |

### Return type

**Object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Bad request. Missing required parameters or invalid parameters. |  -  |
| **500** | Internal server error. Failed to retrieve form schema data. |  -  |

