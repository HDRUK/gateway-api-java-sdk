# DataUseRegistersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDur**](DataUseRegistersApi.md#createDur) | **POST** /api/v1/dur | DurController@store |
| [**createDurByTeamV2**](DataUseRegistersApi.md#createDurByTeamV2) | **POST** /api/v2/teams/{teamId}/dur | TeamDurController@store |
| [**deleteDur**](DataUseRegistersApi.md#deleteDur) | **DELETE** /api/v1/dur/{id} | Delete a dur |
| [**deleteDursV2ByTeamId**](DataUseRegistersApi.md#deleteDursV2ByTeamId) | **DELETE** /api/v2/teams/{teamId}/dur/{id} | TeamDurController@destroy |
| [**editDur**](DataUseRegistersApi.md#editDur) | **PATCH** /api/v1/dur/{id} | Edit a dur |
| [**editDursV2ByTeamId**](DataUseRegistersApi.md#editDursV2ByTeamId) | **PATCH** /api/v2/teams/{teamId}/dur/{id} | TeamDurController@edit |
| [**exportDurTemplate**](DataUseRegistersApi.md#exportDurTemplate) | **GET** /api/v1/dur/template | DurController@exportTemplate |
| [**exportDurTemplateV2**](DataUseRegistersApi.md#exportDurTemplateV2) | **GET** /api/v2/dur/template | DurController@exportTemplate |
| [**exportDurV2**](DataUseRegistersApi.md#exportDurV2) | **GET** /api/v2/dur/export | DurController@export |
| [**fetchAllDur**](DataUseRegistersApi.md#fetchAllDur) | **GET** /api/v1/dur | DurController@index |
| [**fetchAllDurV2**](DataUseRegistersApi.md#fetchAllDurV2) | **GET** /api/v2/dur | DurController@indexActive |
| [**fetchDurById**](DataUseRegistersApi.md#fetchDurById) | **GET** /api/v1/dur/{id} | DurController@show |
| [**fetchDurByIdV2**](DataUseRegistersApi.md#fetchDurByIdV2) | **GET** /api/v2/dur/{id} | DurController@showActive |
| [**updateDur**](DataUseRegistersApi.md#updateDur) | **PUT** /api/v1/dur/{id} | Update a dur by id |
| [**updateDurV2ByTeamId**](DataUseRegistersApi.md#updateDurV2ByTeamId) | **PUT** /api/v2/teams/{teamId}/dur/{id} | TeamDurController@update |
| [**uploadDur**](DataUseRegistersApi.md#uploadDur) | **POST** /api/v1/dur/upload | DurController@upload |


<a id="createDur"></a>
# **createDur**
> CreateDarIntegration201Response createDur(createDurRequest)

DurController@store

Create a new dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    CreateDurRequest createDurRequest = new CreateDurRequest(); // CreateDurRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createDur(createDurRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#createDur");
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
| **createDurRequest** | [**CreateDurRequest**](CreateDurRequest.md)| Pass user credentials | |

### Return type

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="createDurByTeamV2"></a>
# **createDurByTeamV2**
> CreateDarIntegration201Response createDurByTeamV2(teamId, createDurRequest)

TeamDurController@store

Create a new dur by team v2

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    CreateDurRequest createDurRequest = new CreateDurRequest(); // CreateDurRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createDurByTeamV2(teamId, createDurRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#createDurByTeamV2");
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
| **createDurRequest** | [**CreateDurRequest**](CreateDurRequest.md)| Pass user credentials | |

### Return type

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

<a id="deleteDur"></a>
# **deleteDur**
> DeleteApplications200Response deleteDur(id)

Delete a dur

Delete a dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | dur id
    try {
      DeleteApplications200Response result = apiInstance.deleteDur(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#deleteDur");
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
| **id** | **Integer**| dur id | |

### Return type

[**DeleteApplications200Response**](DeleteApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="deleteDursV2ByTeamId"></a>
# **deleteDursV2ByTeamId**
> DeleteApplications200Response deleteDursV2ByTeamId(teamId, id)

TeamDurController@destroy

Delete a dur by team and id v2

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | dur id
    try {
      DeleteApplications200Response result = apiInstance.deleteDursV2ByTeamId(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#deleteDursV2ByTeamId");
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
| **id** | **Integer**| dur id | |

### Return type

[**DeleteApplications200Response**](DeleteApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="editDur"></a>
# **editDur**
> UpdateDur200Response editDur(id, createDurRequest, unarchive)

Edit a dur

Edit a dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | dur id
    CreateDurRequest createDurRequest = new CreateDurRequest(); // CreateDurRequest | Pass user credentials
    String unarchive = "unarchive_example"; // String | Unarchive a dur
    try {
      UpdateDur200Response result = apiInstance.editDur(id, createDurRequest, unarchive);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#editDur");
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
| **id** | **Integer**| dur id | |
| **createDurRequest** | [**CreateDurRequest**](CreateDurRequest.md)| Pass user credentials | |
| **unarchive** | **String**| Unarchive a dur | [optional] |

### Return type

[**UpdateDur200Response**](UpdateDur200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="editDursV2ByTeamId"></a>
# **editDursV2ByTeamId**
> UpdateDur200Response editDursV2ByTeamId(teamId, id, createDurRequest)

TeamDurController@edit

Edit a dur by team v2

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | dur id
    CreateDurRequest createDurRequest = new CreateDurRequest(); // CreateDurRequest | Pass user credentials
    try {
      UpdateDur200Response result = apiInstance.editDursV2ByTeamId(teamId, id, createDurRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#editDursV2ByTeamId");
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
| **id** | **Integer**| dur id | |
| **createDurRequest** | [**CreateDurRequest**](CreateDurRequest.md)| Pass user credentials | |

### Return type

[**UpdateDur200Response**](UpdateDur200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="exportDurTemplate"></a>
# **exportDurTemplate**
> Object exportDurTemplate()

DurController@exportTemplate

Export Dur upload template

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    try {
      Object result = apiInstance.exportDurTemplate();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#exportDurTemplate");
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

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/csv, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | File download |  -  |
| **401** | Unauthorized |  -  |
| **404** | File Not Found |  -  |

<a id="exportDurTemplateV2"></a>
# **exportDurTemplateV2**
> Object exportDurTemplateV2()

DurController@exportTemplate

Export Dur upload template

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    try {
      Object result = apiInstance.exportDurTemplateV2();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#exportDurTemplateV2");
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

**Object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/csv, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | File download |  -  |
| **401** | Unauthorized |  -  |
| **404** | File Not Found |  -  |

<a id="exportDurV2"></a>
# **exportDurV2**
> String exportDurV2(id)

DurController@export

Export CSV of one or more DURs

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | dur id
    try {
      String result = apiInstance.exportDurV2(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#exportDurV2");
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
| **id** | **Integer**| dur id | [optional] |

### Return type

**String**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/csv, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | CSV file |  -  |
| **401** | Unauthorized |  -  |

<a id="fetchAllDur"></a>
# **fetchAllDur**
> FetchAllDur200Response fetchAllDur(sort, projectTitle, perPage)

DurController@index

Returns a list of dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    ProjectTitleAscupdatedAtAsc sort = new ProjectTitleAscupdatedAtAsc(); // ProjectTitleAscupdatedAtAsc | Sort fields in the format field:direction, e.g., project_title:asc,updated_at:asc
    String projectTitle = "projectTitle_example"; // String | Filter tools by project title
    Integer perPage = 1; // Integer | per page
    try {
      FetchAllDur200Response result = apiInstance.fetchAllDur(sort, projectTitle, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#fetchAllDur");
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
| **sort** | [**ProjectTitleAscupdatedAtAsc**](.md)| Sort fields in the format field:direction, e.g., project_title:asc,updated_at:asc | [optional] |
| **projectTitle** | **String**| Filter tools by project title | [optional] |
| **perPage** | **Integer**| per page | [optional] |

### Return type

[**FetchAllDur200Response**](FetchAllDur200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchAllDurV2"></a>
# **fetchAllDurV2**
> FetchAllDurV2200Response fetchAllDurV2(sort, projectTitle, perPage, withRelated)

DurController@indexActive

Returns a list of active dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    ProjectTitleAscupdatedAtAsc sort = new ProjectTitleAscupdatedAtAsc(); // ProjectTitleAscupdatedAtAsc | Sort fields in the format field:direction, e.g., project_title:asc,updated_at:asc
    String projectTitle = "projectTitle_example"; // String | Filter tools by project title
    Integer perPage = 1; // Integer | per page
    Boolean withRelated = true; // Boolean | Show related entities
    try {
      FetchAllDurV2200Response result = apiInstance.fetchAllDurV2(sort, projectTitle, perPage, withRelated);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#fetchAllDurV2");
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
| **sort** | [**ProjectTitleAscupdatedAtAsc**](.md)| Sort fields in the format field:direction, e.g., project_title:asc,updated_at:asc | [optional] |
| **projectTitle** | **String**| Filter tools by project title | [optional] |
| **perPage** | **Integer**| per page | [optional] |
| **withRelated** | **Boolean**| Show related entities | [optional] |

### Return type

[**FetchAllDurV2200Response**](FetchAllDurV2200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchDurById"></a>
# **fetchDurById**
> FetchDurById200Response fetchDurById(id)

DurController@show

Get dur by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | data use register id
    try {
      FetchDurById200Response result = apiInstance.fetchDurById(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#fetchDurById");
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
| **id** | **Integer**| data use register id | |

### Return type

[**FetchDurById200Response**](FetchDurById200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchDurByIdV2"></a>
# **fetchDurByIdV2**
> UpdateDur200Response fetchDurByIdV2(id)

DurController@showActive

Get dur by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | data use register id
    try {
      UpdateDur200Response result = apiInstance.fetchDurByIdV2(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#fetchDurByIdV2");
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
| **id** | **Integer**| data use register id | |

### Return type

[**UpdateDur200Response**](UpdateDur200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="updateDur"></a>
# **updateDur**
> UpdateDur200Response updateDur(id, createDurRequest)

Update a dur by id

Update a dur

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer id = 1; // Integer | dur id
    CreateDurRequest createDurRequest = new CreateDurRequest(); // CreateDurRequest | Pass user credentials
    try {
      UpdateDur200Response result = apiInstance.updateDur(id, createDurRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#updateDur");
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
| **id** | **Integer**| dur id | |
| **createDurRequest** | [**CreateDurRequest**](CreateDurRequest.md)| Pass user credentials | |

### Return type

[**UpdateDur200Response**](UpdateDur200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="updateDurV2ByTeamId"></a>
# **updateDurV2ByTeamId**
> UpdateDur200Response updateDurV2ByTeamId(teamId, id, createDurRequest)

TeamDurController@update

Update a dur by team and id v2

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | dur id
    CreateDurRequest createDurRequest = new CreateDurRequest(); // CreateDurRequest | Pass user credentials
    try {
      UpdateDur200Response result = apiInstance.updateDurV2ByTeamId(teamId, id, createDurRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#updateDurV2ByTeamId");
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
| **id** | **Integer**| dur id | |
| **createDurRequest** | [**CreateDurRequest**](CreateDurRequest.md)| Pass user credentials | |

### Return type

[**UpdateDur200Response**](UpdateDur200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **404** | Not found response |  -  |
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="uploadDur"></a>
# **uploadDur**
> CreateDarIntegration201Response uploadDur(uploadDurRequest)

DurController@upload

Create a new dur with upload data

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataUseRegistersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataUseRegistersApi apiInstance = new DataUseRegistersApi(defaultClient);
    UploadDurRequest uploadDurRequest = new UploadDurRequest(); // UploadDurRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.uploadDur(uploadDurRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataUseRegistersApi#uploadDur");
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
| **uploadDurRequest** | [**UploadDurRequest**](UploadDurRequest.md)| Pass user credentials | |

### Return type

[**CreateDarIntegration201Response**](CreateDarIntegration201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Created |  -  |
| **401** | Unauthorized |  -  |
| **500** | Error |  -  |

