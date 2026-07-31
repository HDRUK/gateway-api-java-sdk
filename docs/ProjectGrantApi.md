# ProjectGrantApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**fetchAllProjectGrants**](ProjectGrantApi.md#fetchAllProjectGrants) | **GET** /api/v1/project_grants | ProjectGrantController@index |
| [**fetchProjectGrant**](ProjectGrantApi.md#fetchProjectGrant) | **GET** /api/v1/project_grants/{id} | ProjectGrantController@show |


<a id="fetchAllProjectGrants"></a>
# **fetchAllProjectGrants**
> FetchAllProjectGrants200Response fetchAllProjectGrants(pid, version, projectGrantName, userId, teamId, withRelated)

ProjectGrantController@index

Get all project grants

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProjectGrantApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectGrantApi apiInstance = new ProjectGrantApi(defaultClient);
    String pid = "pid_example"; // String | Filter by dataset pid
    Integer version = 56; // Integer | Filter by dataset version number
    String projectGrantName = "projectGrantName_example"; // String | Filter by project grant name
    Integer userId = 56; // Integer | Filter by owning user id
    Integer teamId = 56; // Integer | Filter by owning team id
    Boolean withRelated = true; // Boolean | 
    try {
      FetchAllProjectGrants200Response result = apiInstance.fetchAllProjectGrants(pid, version, projectGrantName, userId, teamId, withRelated);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectGrantApi#fetchAllProjectGrants");
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
| **pid** | **String**| Filter by dataset pid | [optional] |
| **version** | **Integer**| Filter by dataset version number | [optional] |
| **projectGrantName** | **String**| Filter by project grant name | [optional] |
| **userId** | **Integer**| Filter by owning user id | [optional] |
| **teamId** | **Integer**| Filter by owning team id | [optional] |
| **withRelated** | **Boolean**|  | [optional] |

### Return type

[**FetchAllProjectGrants200Response**](FetchAllProjectGrants200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchProjectGrant"></a>
# **fetchProjectGrant**
> CountUniqueFieldsCollections200Response fetchProjectGrant(id, withRelated)

ProjectGrantController@show

Get a single project grant

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ProjectGrantApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ProjectGrantApi apiInstance = new ProjectGrantApi(defaultClient);
    Integer id = 56; // Integer | 
    Boolean withRelated = true; // Boolean | 
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.fetchProjectGrant(id, withRelated);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProjectGrantApi#fetchProjectGrant");
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
| **id** | **Integer**|  | |
| **withRelated** | **Boolean**|  | [optional] |

### Return type

[**CountUniqueFieldsCollections200Response**](CountUniqueFieldsCollections200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

