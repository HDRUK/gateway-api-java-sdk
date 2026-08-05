# DataCustodianNetworksApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDataCustodianNetwork**](DataCustodianNetworksApi.md#createDataCustodianNetwork) | **POST** /api/v2/data_custodian_networks | DataCustodianNetworks@store |
| [**deleteDataCustodianNetwork**](DataCustodianNetworksApi.md#deleteDataCustodianNetwork) | **DELETE** /api/v2/data_custodian_networks/{id} | DataCustodianNetworks@destroy |
| [**editDataCustodianNetwork**](DataCustodianNetworksApi.md#editDataCustodianNetwork) | **PATCH** /api/v2/data_custodian_networks/{id} | DataCustodianNetworks@edit |
| [**fetchDataCustodianNetwork**](DataCustodianNetworksApi.md#fetchDataCustodianNetwork) | **GET** /api/v2/data_custodian_networks/{id} | DataCustodianNetworks@show |
| [**fetchDataCustodianNetworkCustodiansSummary**](DataCustodianNetworksApi.md#fetchDataCustodianNetworkCustodiansSummary) | **GET** /api/v2/data_custodian_networks/{id}/custodians_summary | DataCustodianNetworks@showCustodiansSummary |
| [**fetchDataCustodianNetworkDatasetsSummary**](DataCustodianNetworksApi.md#fetchDataCustodianNetworkDatasetsSummary) | **GET** /api/v2/data_custodian_networks/{id}/datasets_summary | DataCustodianNetworks@showDatasetsSummary |
| [**fetchDataCustodianNetworkEntitiesSummary**](DataCustodianNetworksApi.md#fetchDataCustodianNetworkEntitiesSummary) | **GET** /api/v2/data_custodian_networks/{id}/entities_summary | DataCustodianNetworks@showSummary |
| [**fetchDataCustodianNetworkInfo**](DataCustodianNetworksApi.md#fetchDataCustodianNetworkInfo) | **GET** /api/v2/data_custodian_networks/{id}/info | DataCustodianNetworks@showInfoSummary |
| [**fetchDataCustodianNetworks**](DataCustodianNetworksApi.md#fetchDataCustodianNetworks) | **GET** /api/v2/data_custodian_networks | DataCustodianNetworks@index |
| [**updateDataCustodianNetwork**](DataCustodianNetworksApi.md#updateDataCustodianNetwork) | **PUT** /api/v2/data_custodian_networks/{id} | DataCustodianNetworks@update |


<a id="createDataCustodianNetwork"></a>
# **createDataCustodianNetwork**
> CreateDarIntegration201Response createDataCustodianNetwork(createDataProviderCollRequest)

DataCustodianNetworks@store

Creates a new DataCustodianNetwork

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    CreateDataProviderCollRequest createDataProviderCollRequest = new CreateDataProviderCollRequest(); // CreateDataProviderCollRequest | DataCustodianNetwork definition
    try {
      CreateDarIntegration201Response result = apiInstance.createDataCustodianNetwork(createDataProviderCollRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#createDataCustodianNetwork");
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
| **createDataProviderCollRequest** | [**CreateDataProviderCollRequest**](CreateDataProviderCollRequest.md)| DataCustodianNetwork definition | |

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
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="deleteDataCustodianNetwork"></a>
# **deleteDataCustodianNetwork**
> DeleteApplications200Response deleteDataCustodianNetwork(id)

DataCustodianNetworks@destroy

Delete a DataCustodianNetwork

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    Integer id = 1; // Integer | DataCustodianNetwork ID
    try {
      DeleteApplications200Response result = apiInstance.deleteDataCustodianNetwork(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#deleteDataCustodianNetwork");
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
| **id** | **Integer**| DataCustodianNetwork ID | |

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

<a id="editDataCustodianNetwork"></a>
# **editDataCustodianNetwork**
> UpdateDataCustodianNetwork200Response editDataCustodianNetwork(id, editDataProviderCollRequest)

DataCustodianNetworks@edit

Edit a DataCustodianNetwork

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    Integer id = 1; // Integer | DataCustodianNetwork ID
    EditDataProviderCollRequest editDataProviderCollRequest = new EditDataProviderCollRequest(); // EditDataProviderCollRequest | DataCustodianNetwork definition
    try {
      UpdateDataCustodianNetwork200Response result = apiInstance.editDataCustodianNetwork(id, editDataProviderCollRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#editDataCustodianNetwork");
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
| **id** | **Integer**| DataCustodianNetwork ID | |
| **editDataProviderCollRequest** | [**EditDataProviderCollRequest**](EditDataProviderCollRequest.md)| DataCustodianNetwork definition | |

### Return type

[**UpdateDataCustodianNetwork200Response**](UpdateDataCustodianNetwork200Response.md)

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

<a id="fetchDataCustodianNetwork"></a>
# **fetchDataCustodianNetwork**
> FetchDataCustodianNetwork200Response fetchDataCustodianNetwork(id)

DataCustodianNetworks@show

Return a single DataCustodianNetwork

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    Integer id = 1; // Integer | DataCustodianNetwork ID
    try {
      FetchDataCustodianNetwork200Response result = apiInstance.fetchDataCustodianNetwork(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#fetchDataCustodianNetwork");
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
| **id** | **Integer**| DataCustodianNetwork ID | |

### Return type

[**FetchDataCustodianNetwork200Response**](FetchDataCustodianNetwork200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchDataCustodianNetworkCustodiansSummary"></a>
# **fetchDataCustodianNetworkCustodiansSummary**
> FetchDataCustodianNetworkCustodiansSummary200Response fetchDataCustodianNetworkCustodiansSummary(id)

DataCustodianNetworks@showCustodiansSummary

Return a single DataCustodianNetwork - custodians summary

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    Integer id = 1; // Integer | DataCustodianNetwork ID - summary
    try {
      FetchDataCustodianNetworkCustodiansSummary200Response result = apiInstance.fetchDataCustodianNetworkCustodiansSummary(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#fetchDataCustodianNetworkCustodiansSummary");
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
| **id** | **Integer**| DataCustodianNetwork ID - summary | |

### Return type

[**FetchDataCustodianNetworkCustodiansSummary200Response**](FetchDataCustodianNetworkCustodiansSummary200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchDataCustodianNetworkDatasetsSummary"></a>
# **fetchDataCustodianNetworkDatasetsSummary**
> FetchDataCustodianNetworkDatasetsSummary200Response fetchDataCustodianNetworkDatasetsSummary(id)

DataCustodianNetworks@showDatasetsSummary

Return a single DataCustodianNetwork - summary of datasets

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    Integer id = 1; // Integer | DataCustodianNetwork ID - summary
    try {
      FetchDataCustodianNetworkDatasetsSummary200Response result = apiInstance.fetchDataCustodianNetworkDatasetsSummary(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#fetchDataCustodianNetworkDatasetsSummary");
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
| **id** | **Integer**| DataCustodianNetwork ID - summary | |

### Return type

[**FetchDataCustodianNetworkDatasetsSummary200Response**](FetchDataCustodianNetworkDatasetsSummary200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchDataCustodianNetworkEntitiesSummary"></a>
# **fetchDataCustodianNetworkEntitiesSummary**
> FetchDataCustodianNetworkEntitiesSummary200Response fetchDataCustodianNetworkEntitiesSummary(id)

DataCustodianNetworks@showSummary

Return a single DataCustodianNetwork - summary of entities

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    Integer id = 1; // Integer | DataCustodianNetwork ID - summary
    try {
      FetchDataCustodianNetworkEntitiesSummary200Response result = apiInstance.fetchDataCustodianNetworkEntitiesSummary(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#fetchDataCustodianNetworkEntitiesSummary");
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
| **id** | **Integer**| DataCustodianNetwork ID - summary | |

### Return type

[**FetchDataCustodianNetworkEntitiesSummary200Response**](FetchDataCustodianNetworkEntitiesSummary200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchDataCustodianNetworkInfo"></a>
# **fetchDataCustodianNetworkInfo**
> FetchDataCustodianNetworkInfo200Response fetchDataCustodianNetworkInfo(id)

DataCustodianNetworks@showInfoSummary

Return a single DataCustodianNetwork - basic information

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    Integer id = 1; // Integer | DataCustodianNetwork ID - summary
    try {
      FetchDataCustodianNetworkInfo200Response result = apiInstance.fetchDataCustodianNetworkInfo(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#fetchDataCustodianNetworkInfo");
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
| **id** | **Integer**| DataCustodianNetwork ID - summary | |

### Return type

[**FetchDataCustodianNetworkInfo200Response**](FetchDataCustodianNetworkInfo200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **404** | Not found response |  -  |

<a id="fetchDataCustodianNetworks"></a>
# **fetchDataCustodianNetworks**
> FetchDataCustodianNetworks200Response fetchDataCustodianNetworks(perPage)

DataCustodianNetworks@index

Returns a list of DataCustodianNetworks enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    Integer perPage = 1; // Integer | per page
    try {
      FetchDataCustodianNetworks200Response result = apiInstance.fetchDataCustodianNetworks(perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#fetchDataCustodianNetworks");
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
| **perPage** | **Integer**| per page | [optional] |

### Return type

[**FetchDataCustodianNetworks200Response**](FetchDataCustodianNetworks200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="updateDataCustodianNetwork"></a>
# **updateDataCustodianNetwork**
> UpdateDataCustodianNetwork200Response updateDataCustodianNetwork(id, updateDataProviderCollRequest)

DataCustodianNetworks@update

Update a DataCustodianNetwork

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.DataCustodianNetworksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    DataCustodianNetworksApi apiInstance = new DataCustodianNetworksApi(defaultClient);
    Integer id = 1; // Integer | DataCustodianNetworks ID
    UpdateDataProviderCollRequest updateDataProviderCollRequest = new UpdateDataProviderCollRequest(); // UpdateDataProviderCollRequest | DataCustodianNetwork definition
    try {
      UpdateDataCustodianNetwork200Response result = apiInstance.updateDataCustodianNetwork(id, updateDataProviderCollRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DataCustodianNetworksApi#updateDataCustodianNetwork");
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
| **id** | **Integer**| DataCustodianNetworks ID | |
| **updateDataProviderCollRequest** | [**UpdateDataProviderCollRequest**](UpdateDataProviderCollRequest.md)| DataCustodianNetwork definition | |

### Return type

[**UpdateDataCustodianNetwork200Response**](UpdateDataCustodianNetwork200Response.md)

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

