# DatasetsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**countUniqueFields**](DatasetsApi.md#countUniqueFields) | **GET** /api/v1/datasets/count/{field} | DatasetController@count |
| [**createDatasets**](DatasetsApi.md#createDatasets) | **POST** /api/v1/datasets | DatasetController@store |
| [**createDatasetsV2**](DatasetsApi.md#createDatasetsV2) | **POST** /api/v2/datasets | DatasetController@store |
| [**createTeamDatasetsV2**](DatasetsApi.md#createTeamDatasetsV2) | **POST** /api/v2/teams/{teamId}/datasets | TeamDatasetController@store |
| [**deleteDatasets**](DatasetsApi.md#deleteDatasets) | **DELETE** /api/v1/datasets/{id} | DatasetController@destroy |
| [**deleteDatasetsV2**](DatasetsApi.md#deleteDatasetsV2) | **DELETE** /api/v2/datasets/{id} | Delete a dataset |
| [**deleteTeamDatasetsV2**](DatasetsApi.md#deleteTeamDatasetsV2) | **DELETE** /api/v2/teams/{teamId}/datasets/{id} | TeamDatasetController@destroy |
| [**exportDatasetMetadata**](DatasetsApi.md#exportDatasetMetadata) | **GET** /api/v1/datasets/export_metadata/{id} | DatasetController@exportMetadata |
| [**exportDatasets**](DatasetsApi.md#exportDatasets) | **GET** /api/v1/datasets/export | DatasetController@export |
| [**exportDur**](DatasetsApi.md#exportDur) | **GET** /api/v1/dur/export | DurController@export |
| [**exportMockDataset**](DatasetsApi.md#exportMockDataset) | **GET** /api/v1/datasets/export/mock | DatasetController@exportMock |
| [**exportMockDatasetV2**](DatasetsApi.md#exportMockDatasetV2) | **GET** /api/v2/datasets/export/mock | DatasetController@exportMock |
| [**fetchAllDatasets**](DatasetsApi.md#fetchAllDatasets) | **GET** /api/v1/datasets | DatasetController@index |
| [**fetchAllDatasetsV2**](DatasetsApi.md#fetchAllDatasetsV2) | **GET** /api/v2/datasets | DatasetController@index |
| [**fetchDatasets**](DatasetsApi.md#fetchDatasets) | **GET** /api/v1/datasets/{id} | DatasetController@show |
| [**fetchDatasetsV2**](DatasetsApi.md#fetchDatasetsV2) | **GET** /api/v2/datasets/{id} | DatasetController@showActive |
| [**patchDatasets**](DatasetsApi.md#patchDatasets) | **PATCH** /api/v1/datasets/{id} | DatasetController@edit |
| [**patchDatasetsV2**](DatasetsApi.md#patchDatasetsV2) | **PATCH** /api/v2/datasets/{id} | DatasetController@edit |
| [**patchTeamDatasetsV2**](DatasetsApi.md#patchTeamDatasetsV2) | **PATCH** /api/v2/teams/{teamId}/datasets/{id} | TeamDatasetController@edit |
| [**updateDatasets**](DatasetsApi.md#updateDatasets) | **PUT** /api/v1/datasets/{id} | DatasetController@update |
| [**updateDatasetsV2**](DatasetsApi.md#updateDatasetsV2) | **PUT** /api/v2/datasets/{id} | DatasetController@update |
| [**updateTeamDatasetsV2**](DatasetsApi.md#updateTeamDatasetsV2) | **PUT** /api/v2/teams/{teamId}/datasets/{id} | TeamDatasetController@update |


<a id="countUniqueFields"></a>
# **countUniqueFields**
> CountUniqueFieldsCollections200Response countUniqueFields(field, teamId)

DatasetController@count

Get Counts for distinct entries of a field in the model

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    String field = "status"; // String | name of the field to perform a count on
    Integer teamId = 1; // Integer | team id
    try {
      CountUniqueFieldsCollections200Response result = apiInstance.countUniqueFields(field, teamId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#countUniqueFields");
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

<a id="createDatasets"></a>
# **createDatasets**
> CreateDarIntegration201Response createDatasets(createDatasetsRequest)

DatasetController@store

Create a new dataset

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    CreateDatasetsRequest createDatasetsRequest = new CreateDatasetsRequest(); // CreateDatasetsRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createDatasets(createDatasetsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#createDatasets");
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
| **createDatasetsRequest** | [**CreateDatasetsRequest**](CreateDatasetsRequest.md)| Pass user credentials | |

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

<a id="createDatasetsV2"></a>
# **createDatasetsV2**
> CreateDarIntegration201Response createDatasetsV2(createDatasetsV2Request)

DatasetController@store

Create a new dataset

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    CreateDatasetsV2Request createDatasetsV2Request = new CreateDatasetsV2Request(); // CreateDatasetsV2Request | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createDatasetsV2(createDatasetsV2Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#createDatasetsV2");
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
| **createDatasetsV2Request** | [**CreateDatasetsV2Request**](CreateDatasetsV2Request.md)| Pass user credentials | |

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

<a id="createTeamDatasetsV2"></a>
# **createTeamDatasetsV2**
> CreateDarIntegration201Response createTeamDatasetsV2(teamId, createTeamDatasetsV2Request)

TeamDatasetController@store

Create a new dataset for a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    CreateTeamDatasetsV2Request createTeamDatasetsV2Request = new CreateTeamDatasetsV2Request(); // CreateTeamDatasetsV2Request | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.createTeamDatasetsV2(teamId, createTeamDatasetsV2Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#createTeamDatasetsV2");
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
| **createTeamDatasetsV2Request** | [**CreateTeamDatasetsV2Request**](CreateTeamDatasetsV2Request.md)| Pass user credentials | |

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

<a id="deleteDatasets"></a>
# **deleteDatasets**
> DeleteApplications200Response deleteDatasets(id)

DatasetController@destroy

Delete a dataset

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer id = 1; // Integer | dataset id
    try {
      DeleteApplications200Response result = apiInstance.deleteDatasets(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#deleteDatasets");
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
| **id** | **Integer**| dataset id | |

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

<a id="deleteDatasetsV2"></a>
# **deleteDatasetsV2**
> DeleteApplications200Response deleteDatasetsV2(id)

Delete a dataset

Delete a dataset

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer id = 1; // Integer | dataset id
    try {
      DeleteApplications200Response result = apiInstance.deleteDatasetsV2(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#deleteDatasetsV2");
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
| **id** | **Integer**| dataset id | |

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

<a id="deleteTeamDatasetsV2"></a>
# **deleteTeamDatasetsV2**
> DeleteApplications200Response deleteTeamDatasetsV2(teamId, id)

TeamDatasetController@destroy

Delete a team&#39;s dataset

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | dataset id
    try {
      DeleteApplications200Response result = apiInstance.deleteTeamDatasetsV2(teamId, id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#deleteTeamDatasetsV2");
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
| **id** | **Integer**| dataset id | |

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

<a id="exportDatasetMetadata"></a>
# **exportDatasetMetadata**
> String exportDatasetMetadata(id, downloadType)

DatasetController@exportMetadata

Export Structural Metadata CSV of a single dataset

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer id = 1; // Integer | dataset id
    String downloadType = "structural"; // String | download type
    try {
      String result = apiInstance.exportDatasetMetadata(id, downloadType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#exportDatasetMetadata");
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
| **id** | **Integer**| dataset id | |
| **downloadType** | **String**| download type | |

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
| **400** | Bad request |  -  |

<a id="exportDatasets"></a>
# **exportDatasets**
> String exportDatasets(teamId, datasetId)

DatasetController@export

Export CSV Of All Datasets

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer datasetId = 1; // Integer | dataset id
    try {
      String result = apiInstance.exportDatasets(teamId, datasetId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#exportDatasets");
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
| **datasetId** | **Integer**| dataset id | [optional] |

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

<a id="exportDur"></a>
# **exportDur**
> String exportDur(teamId, durId)

DurController@export

Export CSV Of All Dur&#39;s

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer durId = 1; // Integer | dur id
    try {
      String result = apiInstance.exportDur(teamId, durId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#exportDur");
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
| **durId** | **Integer**| dur id | [optional] |

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

<a id="exportMockDataset"></a>
# **exportMockDataset**
> String exportMockDataset(type)

DatasetController@exportMock

Export Mock

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    String type = "template_dataset_structural_metadata"; // String | type export
    try {
      String result = apiInstance.exportMockDataset(type);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#exportMockDataset");
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
| **type** | **String**| type export | [enum: template_dataset_structural_metadata, dataset_metadata] |

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
| **404** | File Not Found |  -  |

<a id="exportMockDatasetV2"></a>
# **exportMockDatasetV2**
> String exportMockDatasetV2(type)

DatasetController@exportMock

Export Mock

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    String type = "template_dataset_structural_metadata"; // String | 
    try {
      String result = apiInstance.exportMockDatasetV2(type);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#exportMockDatasetV2");
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
| **type** | **String**|  | [enum: template_dataset_structural_metadata, dataset_metadata] |

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
| **404** | File Not Found |  -  |

<a id="fetchAllDatasets"></a>
# **fetchAllDatasets**
> FetchAllDatasets200Response fetchAllDatasets(teamId, pid, sort, title, status)

DatasetController@index

Get All Datasets

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    String pid = "aa588d1c-21e7-42d9-9b60-48e3d6b784a9"; // String | get based on a pid
    String sort = "created:desc"; // String | Field and direction (colon separated) to sort by (default: 'created:desc') ... <br/> <br/>         - ?sort=\\<field\\>:\\<direction\\> <br/>         - \\<direction\\> can only be 'asc' or 'desc'  <br/>         - \\<field\\> can only be a valid field for the dataset table that can be ordered on  <br/>         - \\<field\\> can start with the prefix 'metadata.' so that nested values within the field 'metadata'  <br/>             (represented by the GWDM JSON structure) can be used to order on.  <br/>  <br/>
    String title = "hdr"; // String | Three or more characters to filter dataset titles by
    String status = "ACTIVE"; // String | Dataset status to filter by ('ACTIVE', 'DRAFT', 'ARCHIVED')
    try {
      FetchAllDatasets200Response result = apiInstance.fetchAllDatasets(teamId, pid, sort, title, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#fetchAllDatasets");
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
| **pid** | **String**| get based on a pid | [optional] |
| **sort** | **String**| Field and direction (colon separated) to sort by (default: &#39;created:desc&#39;) ... &lt;br/&gt; &lt;br/&gt;         - ?sort&#x3D;\\&lt;field\\&gt;:\\&lt;direction\\&gt; &lt;br/&gt;         - \\&lt;direction\\&gt; can only be &#39;asc&#39; or &#39;desc&#39;  &lt;br/&gt;         - \\&lt;field\\&gt; can only be a valid field for the dataset table that can be ordered on  &lt;br/&gt;         - \\&lt;field\\&gt; can start with the prefix &#39;metadata.&#39; so that nested values within the field &#39;metadata&#39;  &lt;br/&gt;             (represented by the GWDM JSON structure) can be used to order on.  &lt;br/&gt;  &lt;br/&gt; | [optional] |
| **title** | **String**| Three or more characters to filter dataset titles by | [optional] |
| **status** | **String**| Dataset status to filter by (&#39;ACTIVE&#39;, &#39;DRAFT&#39;, &#39;ARCHIVED&#39;) | [optional] |

### Return type

[**FetchAllDatasets200Response**](FetchAllDatasets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchAllDatasetsV2"></a>
# **fetchAllDatasetsV2**
> FetchAllDatasets200Response fetchAllDatasetsV2(sort, title, status, withMetadata)

DatasetController@index

Returns a list of all datasets

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    String sort = "created:desc"; // String | Field and direction (colon separated) to sort by (default: 'created:desc') ... <br/> <br/>         - ?sort=\\<field\\>:\\<direction\\> <br/>         - \\<direction\\> can only be 'asc' or 'desc'  <br/>         - \\<field\\> can only be a valid field for the dataset table that can be ordered on  <br/>         - \\<field\\> can start with the prefix 'metadata.' so that nested values within the field 'metadata'  <br/>             (represented by the GWDM JSON structure) can be used to order on.  <br/>  <br/>
    String title = "hdr"; // String | Three or more characters to filter dataset titles by
    String status = "ACTIVE"; // String | Dataset status to filter by ('ACTIVE', 'DRAFT', 'ARCHIVED')
    String withMetadata = "true"; // String | Boolean whether to return dataset metadata
    try {
      FetchAllDatasets200Response result = apiInstance.fetchAllDatasetsV2(sort, title, status, withMetadata);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#fetchAllDatasetsV2");
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
| **sort** | **String**| Field and direction (colon separated) to sort by (default: &#39;created:desc&#39;) ... &lt;br/&gt; &lt;br/&gt;         - ?sort&#x3D;\\&lt;field\\&gt;:\\&lt;direction\\&gt; &lt;br/&gt;         - \\&lt;direction\\&gt; can only be &#39;asc&#39; or &#39;desc&#39;  &lt;br/&gt;         - \\&lt;field\\&gt; can only be a valid field for the dataset table that can be ordered on  &lt;br/&gt;         - \\&lt;field\\&gt; can start with the prefix &#39;metadata.&#39; so that nested values within the field &#39;metadata&#39;  &lt;br/&gt;             (represented by the GWDM JSON structure) can be used to order on.  &lt;br/&gt;  &lt;br/&gt; | [optional] |
| **title** | **String**| Three or more characters to filter dataset titles by | [optional] |
| **status** | **String**| Dataset status to filter by (&#39;ACTIVE&#39;, &#39;DRAFT&#39;, &#39;ARCHIVED&#39;) | [optional] |
| **withMetadata** | **String**| Boolean whether to return dataset metadata | [optional] |

### Return type

[**FetchAllDatasets200Response**](FetchAllDatasets200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success response |  -  |

<a id="fetchDatasets"></a>
# **fetchDatasets**
> FetchDatasets200Response fetchDatasets(id, export, schemaModel, schemaVersion)

DatasetController@show

Get dataset by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer id = 1; // Integer | dataset id
    String export = "structuralMetadata"; // String | Alternative output schema model.
    String schemaModel = "schemaModel_example"; // String | Alternative output schema model.
    String schemaVersion = "schemaVersion_example"; // String | Alternative output schema version.
    try {
      FetchDatasets200Response result = apiInstance.fetchDatasets(id, export, schemaModel, schemaVersion);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#fetchDatasets");
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
| **id** | **Integer**| dataset id | |
| **export** | **String**| Alternative output schema model. | [optional] |
| **schemaModel** | **String**| Alternative output schema model. | [optional] |
| **schemaVersion** | **String**| Alternative output schema version. | [optional] |

### Return type

[**FetchDatasets200Response**](FetchDatasets200Response.md)

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

<a id="fetchDatasetsV2"></a>
# **fetchDatasetsV2**
> FetchDatasets200Response fetchDatasetsV2(id, export, schemaModel, schemaVersion)

DatasetController@showActive

Get publicly visible dataset by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer id = 1; // Integer | dataset id
    String export = "structuralMetadata"; // String | Set to 'structuralMetadata' to download as CSV.
    String schemaModel = "schemaModel_example"; // String | Alternative output schema model.
    String schemaVersion = "schemaVersion_example"; // String | Alternative output schema version.
    try {
      FetchDatasets200Response result = apiInstance.fetchDatasetsV2(id, export, schemaModel, schemaVersion);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#fetchDatasetsV2");
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
| **id** | **Integer**| dataset id | |
| **export** | **String**| Set to &#39;structuralMetadata&#39; to download as CSV. | [optional] |
| **schemaModel** | **String**| Alternative output schema model. | [optional] |
| **schemaVersion** | **String**| Alternative output schema version. | [optional] |

### Return type

[**FetchDatasets200Response**](FetchDatasets200Response.md)

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

<a id="patchDatasets"></a>
# **patchDatasets**
> DeleteApplications200Response patchDatasets(id, unarchive)

DatasetController@edit

Patch dataset by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer id = 1; // Integer | dataset id
    String unarchive = "unarchive_example"; // String | Unarchive a dataset
    try {
      DeleteApplications200Response result = apiInstance.patchDatasets(id, unarchive);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#patchDatasets");
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
| **id** | **Integer**| dataset id | |
| **unarchive** | **String**| Unarchive a dataset | [optional] |

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
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="patchDatasetsV2"></a>
# **patchDatasetsV2**
> DeleteApplications200Response patchDatasetsV2(id, patchDatasetsV2Request)

DatasetController@edit

Patch dataset by id

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer id = 1; // Integer | dataset id
    PatchDatasetsV2Request patchDatasetsV2Request = new PatchDatasetsV2Request(); // PatchDatasetsV2Request | 
    try {
      DeleteApplications200Response result = apiInstance.patchDatasetsV2(id, patchDatasetsV2Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#patchDatasetsV2");
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
| **id** | **Integer**| dataset id | |
| **patchDatasetsV2Request** | [**PatchDatasetsV2Request**](PatchDatasetsV2Request.md)|  | |

### Return type

[**DeleteApplications200Response**](DeleteApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="patchTeamDatasetsV2"></a>
# **patchTeamDatasetsV2**
> DeleteApplications200Response patchTeamDatasetsV2(teamId, id, patchDatasetsV2Request)

TeamDatasetController@edit

Edit a dataset owned by a team

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | dataset id
    PatchDatasetsV2Request patchDatasetsV2Request = new PatchDatasetsV2Request(); // PatchDatasetsV2Request | Pass user credentials
    try {
      DeleteApplications200Response result = apiInstance.patchTeamDatasetsV2(teamId, id, patchDatasetsV2Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#patchTeamDatasetsV2");
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
| **id** | **Integer**| dataset id | |
| **patchDatasetsV2Request** | [**PatchDatasetsV2Request**](PatchDatasetsV2Request.md)| Pass user credentials | |

### Return type

[**DeleteApplications200Response**](DeleteApplications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="updateDatasets"></a>
# **updateDatasets**
> CreateDarIntegration201Response updateDatasets(id, updateDatasetsRequest)

DatasetController@update

Update a dataset with a new dataset version

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer id = 1; // Integer | dataset id
    UpdateDatasetsRequest updateDatasetsRequest = new UpdateDatasetsRequest(); // UpdateDatasetsRequest | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.updateDatasets(id, updateDatasetsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#updateDatasets");
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
| **id** | **Integer**| dataset id | |
| **updateDatasetsRequest** | [**UpdateDatasetsRequest**](UpdateDatasetsRequest.md)| Pass user credentials | |

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

<a id="updateDatasetsV2"></a>
# **updateDatasetsV2**
> CreateDarIntegration201Response updateDatasetsV2(id, updateDatasetsRequest)

DatasetController@update

Update a dataset with a new dataset version

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer id = 1; // Integer | dataset id
    UpdateDatasetsRequest updateDatasetsRequest = new UpdateDatasetsRequest(); // UpdateDatasetsRequest | 
    try {
      CreateDarIntegration201Response result = apiInstance.updateDatasetsV2(id, updateDatasetsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#updateDatasetsV2");
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
| **id** | **Integer**| dataset id | |
| **updateDatasetsRequest** | [**UpdateDatasetsRequest**](UpdateDatasetsRequest.md)|  | |

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

<a id="updateTeamDatasetsV2"></a>
# **updateTeamDatasetsV2**
> CreateDarIntegration201Response updateTeamDatasetsV2(teamId, id, patchDatasetsV2Request)

TeamDatasetController@update

Update a team dataset with a new dataset version

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DatasetsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DatasetsApi apiInstance = new DatasetsApi(defaultClient);
    Integer teamId = 1; // Integer | team id
    Integer id = 1; // Integer | dataset id
    PatchDatasetsV2Request patchDatasetsV2Request = new PatchDatasetsV2Request(); // PatchDatasetsV2Request | Pass user credentials
    try {
      CreateDarIntegration201Response result = apiInstance.updateTeamDatasetsV2(teamId, id, patchDatasetsV2Request);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DatasetsApi#updateTeamDatasetsV2");
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
| **id** | **Integer**| dataset id | |
| **patchDatasetsV2Request** | [**PatchDatasetsV2Request**](PatchDatasetsV2Request.md)| Pass user credentials | |

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

