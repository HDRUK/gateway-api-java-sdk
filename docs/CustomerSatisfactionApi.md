# CustomerSatisfactionApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCsat**](CustomerSatisfactionApi.md#createCsat) | **POST** /api/v1/csat | Create Customer Satisfaction Score |
| [**editCsat**](CustomerSatisfactionApi.md#editCsat) | **PATCH** /api/v1/csat/{id} | Update Customer Satisfaction Description |


<a id="createCsat"></a>
# **createCsat**
> DeleteAliases200Response createCsat(createCsatRequest)

Create Customer Satisfaction Score

Creates a customer satisfaction score between 0 and 5

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CustomerSatisfactionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CustomerSatisfactionApi apiInstance = new CustomerSatisfactionApi(defaultClient);
    CreateCsatRequest createCsatRequest = new CreateCsatRequest(); // CreateCsatRequest | Customer Satisfaction score
    try {
      DeleteAliases200Response result = apiInstance.createCsat(createCsatRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomerSatisfactionApi#createCsat");
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
| **createCsatRequest** | [**CreateCsatRequest**](CreateCsatRequest.md)| Customer Satisfaction score | |

### Return type

[**DeleteAliases200Response**](DeleteAliases200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Resource Created |  -  |
| **422** | Validation Error |  -  |
| **500** | Internal Server Error |  -  |

<a id="editCsat"></a>
# **editCsat**
> EditCsat200Response editCsat(id, editCsatRequest)

Update Customer Satisfaction Description

Update a description for a satisfaction score entry

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.CustomerSatisfactionApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CustomerSatisfactionApi apiInstance = new CustomerSatisfactionApi(defaultClient);
    Integer id = 56; // Integer | ID of the CSAT entry
    EditCsatRequest editCsatRequest = new EditCsatRequest(); // EditCsatRequest | Reason to update
    try {
      EditCsat200Response result = apiInstance.editCsat(id, editCsatRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CustomerSatisfactionApi#editCsat");
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
| **id** | **Integer**| ID of the CSAT entry | |
| **editCsatRequest** | [**EditCsatRequest**](EditCsatRequest.md)| Reason to update | |

### Return type

[**EditCsat200Response**](EditCsat200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Update successful |  -  |

