# ToolsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**countTeamUniqueFieldsToolsV2**](ToolsApi.md#countTeamUniqueFieldsToolsV2) | **GET** /api/v2/teams/{teamId}/tools/count/{field} | TeamToolController@count |
| [**countUniqueFieldsTools**](ToolsApi.md#countUniqueFieldsTools) | **GET** /api/v1/tools/count/{field} | ToolController@count |
| [**countUserUniqueFieldsToolsV2**](ToolsApi.md#countUserUniqueFieldsToolsV2) | **GET** /api/v2/users/{userId}/tools/count/{field} | UserToolController@count |
| [**createTools**](ToolsApi.md#createTools) | **POST** /api/v1/tools | ToolController@store |
| [**createToolsByTeamV2**](ToolsApi.md#createToolsByTeamV2) | **POST** /api/v2/teams/{teamId}/tools | ToolController@store |
| [**createToolsByUserV2**](ToolsApi.md#createToolsByUserV2) | **POST** /api/v2/users/{userId}/tools | UserToolController@store |
| [**createToolsIntegrations**](ToolsApi.md#createToolsIntegrations) | **POST** /api/v1/integrations/tools | IntegrationToolController@store |
| [**deleteTools**](ToolsApi.md#deleteTools) | **DELETE** /api/v1/tools/{id} | ToolController@destroy |
| [**deleteToolsByTeamidV2**](ToolsApi.md#deleteToolsByTeamidV2) | **DELETE** /api/v2/teams/{teamId}/tools/{id} | TeamToolController@destroy |
| [**deleteToolsByUserV2**](ToolsApi.md#deleteToolsByUserV2) | **DELETE** /api/v2/users/{userId}/tools/{id} | UserToolController@destroy |
| [**deleteToolsIntegrations**](ToolsApi.md#deleteToolsIntegrations) | **DELETE** /api/v1/integrations/tools/{id} | IntegrationToolController@destroy |
| [**editTools**](ToolsApi.md#editTools) | **PATCH** /api/v1/tools/{id} | ToolController@edit |
| [**editToolsByTeamidV2**](ToolsApi.md#editToolsByTeamidV2) | **PATCH** /api/v2/teams/{teamId}/tools/{id} | TeamToolController@edit |
| [**editToolsByUserV2**](ToolsApi.md#editToolsByUserV2) | **PATCH** /api/v2/users/{userId}/tools/{id} | UserToolController@edit |
| [**editToolsIntegrations**](ToolsApi.md#editToolsIntegrations) | **PATCH** /api/v1/integrations/tools/{id} | IntegrationToolController@edit |
| [**fetchAllToolByTeamAndStatusV2**](ToolsApi.md#fetchAllToolByTeamAndStatusV2) | **GET** /api/v2/teams/{teamId}/tools/status/{status} | TeamToolController@indexStatus |
| [**fetchAllToolByUserAndStatusV2**](ToolsApi.md#fetchAllToolByUserAndStatusV2) | **GET** /api/v2/users/{userId}/tools/status/{status} | UserToolController@indexStatus |
| [**fetchAllTools**](ToolsApi.md#fetchAllTools) | **GET** /api/v1/tools | Fetch all tools |
| [**fetchAllToolsIntegrations**](ToolsApi.md#fetchAllToolsIntegrations) | **GET** /api/v1/integrations/tools | IntegrationToolController@index |
| [**fetchAllToolsV2**](ToolsApi.md#fetchAllToolsV2) | **GET** /api/v2/tools | ToolController@indexActive |
| [**fetchTools**](ToolsApi.md#fetchTools) | **GET** /api/v1/tools/{id} | ToolController@show |
| [**fetchToolsByTeamAndByIdV2**](ToolsApi.md#fetchToolsByTeamAndByIdV2) | **GET** /api/v2/teams/{teamId}/tools/{id} | TeamToolController@show |
| [**fetchToolsByUserAndByIdV2**](ToolsApi.md#fetchToolsByUserAndByIdV2) | **GET** /api/v2/users/{userId}/tools/{id} | UserToolController@show |
| [**fetchToolsIntegrations**](ToolsApi.md#fetchToolsIntegrations) | **GET** /api/v1/integrations/tools/{id} | IntegrationToolController@show |
| [**fetchToolsV2**](ToolsApi.md#fetchToolsV2) | **GET** /api/v2/tools/{id} | ToolController@showActive |
| [**updateTools**](ToolsApi.md#updateTools) | **PUT** /api/v1/tools/{id} | ToolController@update |
| [**updateToolsByTeamidV2**](ToolsApi.md#updateToolsByTeamidV2) | **PUT** /api/v2/teams/{teamId}/tools/{id} | TeamToolController@update |
| [**updateToolsByUserV2**](ToolsApi.md#updateToolsByUserV2) | **PUT** /api/v2/users/{userId}/tools/{id} | UserToolController@update |
| [**updateToolsIntegrations**](ToolsApi.md#updateToolsIntegrations) | **PUT** /api/v1/integrations/tools/{id} | IntegrationToolController@update |


<a id="countTeamUniqueFieldsToolsV2"></a>
# **countTeamUniqueFieldsToolsV2**
> CountUniqueFieldsCollections200Response countTeamUniqueFieldsToolsV2(teamId, field)

TeamToolController@count

Get team counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    String field = "status"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countTeamUniqueFieldsToolsV2(teamId, field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#countTeamUniqueFieldsToolsV2");
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
| **teamId** | **Integer**| team id | |
| **field** | **String**| name of the field to perform a count on | |

### Return type

[**CountUniqueFieldsCollections200Response**](CountUniqueFieldsCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="countUniqueFieldsTools"></a>
# **countUniqueFieldsTools**
> CountUniqueFieldsCollections200Response countUniqueFieldsTools(field, teamId)

ToolController@count

Get Counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    String field = "status"; // String | name of the field to perform a count on
    Integer teamId = 1; // Integer | team id
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUniqueFieldsTools(field, teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#countUniqueFieldsTools");
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
| **field** | **String**| name of the field to perform a count on | |
| **teamId** | **Integer**| team id | |

### Return type

[**CountUniqueFieldsCollections200Response**](CountUniqueFieldsCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="countUserUniqueFieldsToolsV2"></a>
# **countUserUniqueFieldsToolsV2**
> CountUniqueFieldsCollections200Response countUserUniqueFieldsToolsV2(userId, field)

UserToolController@count

Get user counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer userId = 1; // Integer | user id
    String field = "status"; // String | name of the field to perform a count on
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUserUniqueFieldsToolsV2(userId, field);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#countUserUniqueFieldsToolsV2");
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
| **userId** | **Integer**| user id | |
| **field** | **String**| name of the field to perform a count on | |

### Return type

[**CountUniqueFieldsCollections200Response**](CountUniqueFieldsCollections200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="createTools"></a>
# **createTools**
> CreateCategories200Response createTools(createToolsRequest)

ToolController@store

Create a new tool

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    CreateToolsRequest createToolsRequest = new CreateToolsRequest(); // CreateToolsRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createTools(createToolsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#createTools");
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
| **createToolsRequest** | [**CreateToolsRequest**](CreateToolsRequest.md)| Pass user credentials | |

### Return type

[**CreateCategories200Response**](CreateCategories200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="createToolsByTeamV2"></a>
# **createToolsByTeamV2**
> CreateCategories200Response createToolsByTeamV2(teamId, createToolsRequest)

ToolController@store

Create a new tool by team v2

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    CreateToolsRequest createToolsRequest = new CreateToolsRequest(); // CreateToolsRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createToolsByTeamV2(teamId, createToolsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#createToolsByTeamV2");
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
| **teamId** | **Integer**| team id | |
| **createToolsRequest** | [**CreateToolsRequest**](CreateToolsRequest.md)| Pass user credentials | |

### Return type

[**CreateCategories200Response**](CreateCategories200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="createToolsByUserV2"></a>
# **createToolsByUserV2**
> CreateCategories200Response createToolsByUserV2(userId, createToolsRequest)

UserToolController@store

Create a new tool by user v2

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer userId = 1; // Integer | user id
    CreateToolsRequest createToolsRequest = new CreateToolsRequest(); // CreateToolsRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createToolsByUserV2(userId, createToolsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#createToolsByUserV2");
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
| **userId** | **Integer**| user id | |
| **createToolsRequest** | [**CreateToolsRequest**](CreateToolsRequest.md)| Pass user credentials | |

### Return type

[**CreateCategories200Response**](CreateCategories200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="createToolsIntegrations"></a>
# **createToolsIntegrations**
> CreateCategories200Response createToolsIntegrations(createToolsIntegrationsRequest)

IntegrationToolController@store

Create a new tool

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    CreateToolsIntegrationsRequest createToolsIntegrationsRequest = new CreateToolsIntegrationsRequest(); // CreateToolsIntegrationsRequest | Pass user credentials
    try {
      CreateCategories200Response result = apiInstance.createToolsIntegrations(createToolsIntegrationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#createToolsIntegrations");
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
| **createToolsIntegrationsRequest** | [**CreateToolsIntegrationsRequest**](CreateToolsIntegrationsRequest.md)| Pass user credentials | |

### Return type

[**CreateCategories200Response**](CreateCategories200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="deleteTools"></a>
# **deleteTools**
> DeleteFederation200Response deleteTools(id)

ToolController@destroy

Delete tool by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer id = 1; // Integer | tool id
    try {
      DeleteFederation200Response result = apiInstance.deleteTools(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#deleteTools");
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
| **id** | **Integer**| tool id | |

### Return type

[**DeleteFederation200Response**](DeleteFederation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Error response |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="deleteToolsByTeamidV2"></a>
# **deleteToolsByTeamidV2**
> DeleteFederation200Response deleteToolsByTeamidV2(teamId, id)

TeamToolController@destroy

Delete tool by id and by team_id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | tool id
    try {
      DeleteFederation200Response result = apiInstance.deleteToolsByTeamidV2(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#deleteToolsByTeamidV2");
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
| **teamId** | **Integer**| team id | |
| **id** | **Integer**| tool id | |

### Return type

[**DeleteFederation200Response**](DeleteFederation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Error response |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="deleteToolsByUserV2"></a>
# **deleteToolsByUserV2**
> DeleteFederation200Response deleteToolsByUserV2(userId, id)

UserToolController@destroy

Delete tool by id and by user

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer userId = 1; // Integer | user id
    Integer id = 1; // Integer | tool id
    try {
      DeleteFederation200Response result = apiInstance.deleteToolsByUserV2(userId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#deleteToolsByUserV2");
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
| **userId** | **Integer**| user id | |
| **id** | **Integer**| tool id | |

### Return type

[**DeleteFederation200Response**](DeleteFederation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Error response |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="deleteToolsIntegrations"></a>
# **deleteToolsIntegrations**
> DeleteFederation200Response deleteToolsIntegrations(id)

IntegrationToolController@destroy

Delete tool by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer id = 1; // Integer | tool id
    try {
      DeleteFederation200Response result = apiInstance.deleteToolsIntegrations(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#deleteToolsIntegrations");
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
| **id** | **Integer**| tool id | |

### Return type

[**DeleteFederation200Response**](DeleteFederation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Error response |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="editTools"></a>
# **editTools**
> FetchToolsIntegrations200Response editTools(id, updateToolsRequest, unarchive)

ToolController@edit

Edit tool by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer id = 1; // Integer | tool id
    UpdateToolsRequest updateToolsRequest = new UpdateToolsRequest(); // UpdateToolsRequest | Pass user credentials
    String unarchive = "unarchive_example"; // String | Unarchive a tool
    try {
      FetchToolsIntegrations200Response result = apiInstance.editTools(id, updateToolsRequest, unarchive);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#editTools");
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
| **id** | **Integer**| tool id | |
| **updateToolsRequest** | [**UpdateToolsRequest**](UpdateToolsRequest.md)| Pass user credentials | |
| **unarchive** | **String**| Unarchive a tool | [optional] |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="editToolsByTeamidV2"></a>
# **editToolsByTeamidV2**
> FetchToolsIntegrations200Response editToolsByTeamidV2(teamId, id, updateToolsRequest)

TeamToolController@edit

Edit tool by id and by teamid

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | tool id
    UpdateToolsRequest updateToolsRequest = new UpdateToolsRequest(); // UpdateToolsRequest | Pass user credentials
    try {
      FetchToolsIntegrations200Response result = apiInstance.editToolsByTeamidV2(teamId, id, updateToolsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#editToolsByTeamidV2");
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
| **teamId** | **Integer**| team id | |
| **id** | **Integer**| tool id | |
| **updateToolsRequest** | [**UpdateToolsRequest**](UpdateToolsRequest.md)| Pass user credentials | |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="editToolsByUserV2"></a>
# **editToolsByUserV2**
> FetchToolsIntegrations200Response editToolsByUserV2(userId, id, updateToolsRequest)

UserToolController@edit

Edit tool by id and by user

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer userId = 1; // Integer | user id
    Integer id = 1; // Integer | tool id
    UpdateToolsRequest updateToolsRequest = new UpdateToolsRequest(); // UpdateToolsRequest | Pass user credentials
    try {
      FetchToolsIntegrations200Response result = apiInstance.editToolsByUserV2(userId, id, updateToolsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#editToolsByUserV2");
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
| **userId** | **Integer**| user id | |
| **id** | **Integer**| tool id | |
| **updateToolsRequest** | [**UpdateToolsRequest**](UpdateToolsRequest.md)| Pass user credentials | |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="editToolsIntegrations"></a>
# **editToolsIntegrations**
> FetchToolsIntegrations200Response editToolsIntegrations(id, updateToolsIntegrationsRequest)

IntegrationToolController@edit

Edit tool by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer id = 1; // Integer | tool id
    UpdateToolsIntegrationsRequest updateToolsIntegrationsRequest = new UpdateToolsIntegrationsRequest(); // UpdateToolsIntegrationsRequest | Pass user credentials
    try {
      FetchToolsIntegrations200Response result = apiInstance.editToolsIntegrations(id, updateToolsIntegrationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#editToolsIntegrations");
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
| **id** | **Integer**| tool id | |
| **updateToolsIntegrationsRequest** | [**UpdateToolsIntegrationsRequest**](UpdateToolsIntegrationsRequest.md)| Pass user credentials | |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="fetchAllToolByTeamAndStatusV2"></a>
# **fetchAllToolByTeamAndStatusV2**
> FetchAllToolsIntegrations200Response fetchAllToolByTeamAndStatusV2(teamId, status)

TeamToolController@indexStatus

Returns a list of a teams tools with given status

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Long teamId = 56L; // Long | ID of the team
    String status = "active"; // String | Status of the tool (active, draft, or archived). Defaults to active if not provided.
    try {
      FetchAllToolsIntegrations200Response result = apiInstance.fetchAllToolByTeamAndStatusV2(teamId, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchAllToolByTeamAndStatusV2");
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
| **teamId** | **Long**| ID of the team | |
| **status** | **String**| Status of the tool (active, draft, or archived). Defaults to active if not provided. | [default to active] [enum: active, draft, archived] |

### Return type

[**FetchAllToolsIntegrations200Response**](FetchAllToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Not Found |  -  |

<a id="fetchAllToolByUserAndStatusV2"></a>
# **fetchAllToolByUserAndStatusV2**
> FetchAllToolsIntegrations200Response fetchAllToolByUserAndStatusV2(userId, status)

UserToolController@indexStatus

Returns a list of a user tools

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Long userId = 56L; // Long | ID of the user
    String status = "active"; // String | Status of the tool (active, draft, or archived). Defaults to active if not provided.
    try {
      FetchAllToolsIntegrations200Response result = apiInstance.fetchAllToolByUserAndStatusV2(userId, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchAllToolByUserAndStatusV2");
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
| **userId** | **Long**| ID of the user | |
| **status** | **String**| Status of the tool (active, draft, or archived). Defaults to active if not provided. | [default to active] [enum: active, draft, archived] |

### Return type

[**FetchAllToolsIntegrations200Response**](FetchAllToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **404** | Not Found |  -  |

<a id="fetchAllTools"></a>
# **fetchAllTools**
> FetchAllTools200Response fetchAllTools(mongoId, teamId, userId, title, sort)

Fetch all tools

Get all tools with optional filters and sorting

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    String mongoId = "mongoId_example"; // String | Filter tools by mongo ID
    Integer teamId = 56; // Integer | Filter tools by team ID
    Integer userId = 56; // Integer | Filter tools by user ID
    String title = "title_example"; // String | Filter tools by title
    String sort = "name:asc"; // String | Sort tools by a specific field and direction, e.g., 'name:asc' or 'created_at:desc'
    try {
      FetchAllTools200Response result = apiInstance.fetchAllTools(mongoId, teamId, userId, title, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchAllTools");
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
| **mongoId** | **String**| Filter tools by mongo ID | [optional] |
| **teamId** | **Integer**| Filter tools by team ID | [optional] |
| **userId** | **Integer**| Filter tools by user ID | [optional] |
| **title** | **String**| Filter tools by title | [optional] |
| **sort** | **String**| Sort tools by a specific field and direction, e.g., &#39;name:asc&#39; or &#39;created_at:desc&#39; | [optional] |

### Return type

[**FetchAllTools200Response**](FetchAllTools200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **400** | Bad request response |  -  |
| **500** | Internal server error |  -  |

<a id="fetchAllToolsIntegrations"></a>
# **fetchAllToolsIntegrations**
> FetchAllToolsIntegrations200Response fetchAllToolsIntegrations()

IntegrationToolController@index

Get All Tools

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    try {
      FetchAllToolsIntegrations200Response result = apiInstance.fetchAllToolsIntegrations();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchAllToolsIntegrations");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**FetchAllToolsIntegrations200Response**](FetchAllToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchAllToolsV2"></a>
# **fetchAllToolsV2**
> FetchAllTools200Response fetchAllToolsV2(name, sort)

ToolController@indexActive

Get all tools with optional filters and sorting

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    String name = "name_example"; // String | Filter tools by name
    String sort = "name:asc"; // String | Sort tools by a specific field and direction, e.g., 'name:asc' or 'created_at:desc'
    try {
      FetchAllTools200Response result = apiInstance.fetchAllToolsV2(name, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchAllToolsV2");
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
| **name** | **String**| Filter tools by name | [optional] |
| **sort** | **String**| Sort tools by a specific field and direction, e.g., &#39;name:asc&#39; or &#39;created_at:desc&#39; | [optional] |

### Return type

[**FetchAllTools200Response**](FetchAllTools200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **400** | Bad request response |  -  |
| **500** | Internal server error |  -  |

<a id="fetchTools"></a>
# **fetchTools**
> FetchToolsIntegrations200Response fetchTools(id, viewType)

ToolController@show

Get tool by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer id = 1; // Integer | tool id
    String viewType = "full"; // String | Query flag to show full tool data or a trimmed version (defaults to full).
    try {
      FetchToolsIntegrations200Response result = apiInstance.fetchTools(id, viewType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchTools");
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
| **id** | **Integer**| tool id | |
| **viewType** | **String**| Query flag to show full tool data or a trimmed version (defaults to full). | [optional] [default to full] |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |
| **404** | Not found response |  -  |

<a id="fetchToolsByTeamAndByIdV2"></a>
# **fetchToolsByTeamAndByIdV2**
> FetchToolsIntegrations200Response fetchToolsByTeamAndByIdV2(teamId, id, viewType)

TeamToolController@show

Get tool by team id and by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | tool id
    String viewType = "full"; // String | Query flag to show full tool data or a trimmed version (defaults to full).
    try {
      FetchToolsIntegrations200Response result = apiInstance.fetchToolsByTeamAndByIdV2(teamId, id, viewType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchToolsByTeamAndByIdV2");
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
| **teamId** | **Integer**| team id | |
| **id** | **Integer**| tool id | |
| **viewType** | **String**| Query flag to show full tool data or a trimmed version (defaults to full). | [optional] [default to full] |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |
| **404** | Not found response |  -  |

<a id="fetchToolsByUserAndByIdV2"></a>
# **fetchToolsByUserAndByIdV2**
> FetchToolsIntegrations200Response fetchToolsByUserAndByIdV2(userId, id, viewType)

UserToolController@show

Get tool by user id and by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer userId = 1; // Integer | user id
    Integer id = 1; // Integer | tool id
    String viewType = "full"; // String | Query flag to show full tool data or a trimmed version (defaults to full).
    try {
      FetchToolsIntegrations200Response result = apiInstance.fetchToolsByUserAndByIdV2(userId, id, viewType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchToolsByUserAndByIdV2");
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
| **userId** | **Integer**| user id | |
| **id** | **Integer**| tool id | |
| **viewType** | **String**| Query flag to show full tool data or a trimmed version (defaults to full). | [optional] [default to full] |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |
| **404** | Not found response |  -  |

<a id="fetchToolsIntegrations"></a>
# **fetchToolsIntegrations**
> FetchToolsIntegrations200Response fetchToolsIntegrations(id)

IntegrationToolController@show

Get tool by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer id = 1; // Integer | tool id
    try {
      FetchToolsIntegrations200Response result = apiInstance.fetchToolsIntegrations(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchToolsIntegrations");
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
| **id** | **Integer**| tool id | |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |
| **404** | Not found response |  -  |

<a id="fetchToolsV2"></a>
# **fetchToolsV2**
> FetchToolsIntegrations200Response fetchToolsV2(id)

ToolController@showActive

Get tool by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer id = 1; // Integer | tool id
    try {
      FetchToolsIntegrations200Response result = apiInstance.fetchToolsV2(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#fetchToolsV2");
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
| **id** | **Integer**| tool id | |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |
| **401** | Unauthorized |  -  |
| **404** | Not found response |  -  |

<a id="updateTools"></a>
# **updateTools**
> FetchToolsIntegrations200Response updateTools(id, updateToolsRequest)

ToolController@update

Update tool by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer id = 1; // Integer | tool id
    UpdateToolsRequest updateToolsRequest = new UpdateToolsRequest(); // UpdateToolsRequest | Pass user credentials
    try {
      FetchToolsIntegrations200Response result = apiInstance.updateTools(id, updateToolsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#updateTools");
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
| **id** | **Integer**| tool id | |
| **updateToolsRequest** | [**UpdateToolsRequest**](UpdateToolsRequest.md)| Pass user credentials | |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="updateToolsByTeamidV2"></a>
# **updateToolsByTeamidV2**
> FetchToolsIntegrations200Response updateToolsByTeamidV2(teamId, id, updateToolsRequest)

TeamToolController@update

Update tools by team id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | tool id
    UpdateToolsRequest updateToolsRequest = new UpdateToolsRequest(); // UpdateToolsRequest | Pass user credentials
    try {
      FetchToolsIntegrations200Response result = apiInstance.updateToolsByTeamidV2(teamId, id, updateToolsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#updateToolsByTeamidV2");
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
| **teamId** | **Integer**| team id | |
| **id** | **Integer**| tool id | |
| **updateToolsRequest** | [**UpdateToolsRequest**](UpdateToolsRequest.md)| Pass user credentials | |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="updateToolsByUserV2"></a>
# **updateToolsByUserV2**
> FetchToolsIntegrations200Response updateToolsByUserV2(userId, id, updateToolsRequest)

UserToolController@update

Update tools by user id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer userId = 1; // Integer | user id
    Integer id = 1; // Integer | tool id
    UpdateToolsRequest updateToolsRequest = new UpdateToolsRequest(); // UpdateToolsRequest | Pass user credentials
    try {
      FetchToolsIntegrations200Response result = apiInstance.updateToolsByUserV2(userId, id, updateToolsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#updateToolsByUserV2");
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
| **userId** | **Integer**| user id | |
| **id** | **Integer**| tool id | |
| **updateToolsRequest** | [**UpdateToolsRequest**](UpdateToolsRequest.md)| Pass user credentials | |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="updateToolsIntegrations"></a>
# **updateToolsIntegrations**
> FetchToolsIntegrations200Response updateToolsIntegrations(id, updateToolsIntegrationsRequest)

IntegrationToolController@update

Update tool by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.ToolsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    ToolsApi apiInstance = new ToolsApi(defaultClient);
    Integer id = 1; // Integer | tool id
    UpdateToolsIntegrationsRequest updateToolsIntegrationsRequest = new UpdateToolsIntegrationsRequest(); // UpdateToolsIntegrationsRequest | Pass user credentials
    try {
      FetchToolsIntegrations200Response result = apiInstance.updateToolsIntegrations(id, updateToolsIntegrationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ToolsApi#updateToolsIntegrations");
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
| **id** | **Integer**| tool id | |
| **updateToolsIntegrationsRequest** | [**UpdateToolsIntegrationsRequest**](UpdateToolsIntegrationsRequest.md)| Pass user credentials | |

### Return type

[**FetchToolsIntegrations200Response**](FetchToolsIntegrations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **400** | bad request |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

