# IntegrationsDatasetsTestApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**integrationsDatasetsTest**](IntegrationsDatasetsTestApi.md#integrationsDatasetsTest) | **POST** /api/v1/integrations/datasets/test | IntegrationDatasetController@datasetTest |


<a id="integrationsDatasetsTest"></a>
# **integrationsDatasetsTest**
> CreateCategories200Response integrationsDatasetsTest(datasetsTestRequest)

IntegrationDatasetController@datasetTest

Integrations datasets test

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.IntegrationsDatasetsTestApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    IntegrationsDatasetsTestApi apiInstance = new IntegrationsDatasetsTestApi(defaultClient);
    DatasetsTestRequest datasetsTestRequest = new DatasetsTestRequest(); // DatasetsTestRequest | Pass datasets payload
    try {
      CreateCategories200Response result = apiInstance.integrationsDatasetsTest(datasetsTestRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IntegrationsDatasetsTestApi#integrationsDatasetsTest");
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
| **datasetsTestRequest** | [**DatasetsTestRequest**](DatasetsTestRequest.md)| Pass datasets payload | |

### Return type

[**CreateCategories200Response**](CreateCategories200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

