# NotificationApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createNotifications**](NotificationApi.md#createNotifications) | **POST** /api/v1/notifications | Notification@store |
| [**deleteNotifications**](NotificationApi.md#deleteNotifications) | **DELETE** /api/v1/notifications/{id} | Notification@destroy |
| [**editNotifications**](NotificationApi.md#editNotifications) | **PATCH** /api/v1/notifications/{id} | Notification@edit |
| [**fetchAllNotifications**](NotificationApi.md#fetchAllNotifications) | **GET** /api/v1/notifications | Notification@index |
| [**fetchNotifications**](NotificationApi.md#fetchNotifications) | **GET** /api/v1/notifications/{id} | Notification@show |
| [**updateNotifications**](NotificationApi.md#updateNotifications) | **PUT** /api/v1/notifications/{id} | Notification@update |


<a id="createNotifications"></a>
# **createNotifications**
> CreateCategories200Response createNotifications(createNotificationsRequest)

Notification@store

Creates a new notification

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.NotificationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    NotificationApi apiInstance = new NotificationApi(defaultClient);
    CreateNotificationsRequest createNotificationsRequest = new CreateNotificationsRequest(); // CreateNotificationsRequest | Notification definition
    try {
      CreateCategories200Response result = apiInstance.createNotifications(createNotificationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationApi#createNotifications");
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
| **createNotificationsRequest** | [**CreateNotificationsRequest**](CreateNotificationsRequest.md)| Notification definition | |

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
| **200** | Success |  -  |
| **500** | Error |  -  |

<a id="deleteNotifications"></a>
# **deleteNotifications**
> DeleteAliases200Response deleteNotifications(id)

Notification@destroy

Delete a notification

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.NotificationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    NotificationApi apiInstance = new NotificationApi(defaultClient);
    Integer id = 1; // Integer | notification id
    try {
      DeleteAliases200Response result = apiInstance.deleteNotifications(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationApi#deleteNotifications");
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
| **id** | **Integer**| notification id | |

### Return type

[**DeleteAliases200Response**](DeleteAliases200Response.md)

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

<a id="editNotifications"></a>
# **editNotifications**
> UpdateNotifications200Response editNotifications(id, editNotificationsRequest)

Notification@edit

Edit a notification

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.NotificationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    NotificationApi apiInstance = new NotificationApi(defaultClient);
    Integer id = 1; // Integer | notification id
    EditNotificationsRequest editNotificationsRequest = new EditNotificationsRequest(); // EditNotificationsRequest | Notification definition
    try {
      UpdateNotifications200Response result = apiInstance.editNotifications(id, editNotificationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationApi#editNotifications");
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
| **id** | **Integer**| notification id | |
| **editNotificationsRequest** | [**EditNotificationsRequest**](EditNotificationsRequest.md)| Notification definition | |

### Return type

[**UpdateNotifications200Response**](UpdateNotifications200Response.md)

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

<a id="fetchAllNotifications"></a>
# **fetchAllNotifications**
> FetchAllNotifications200Response fetchAllNotifications()

Notification@index

Returns a list of notifications enabled on the system

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.NotificationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    NotificationApi apiInstance = new NotificationApi(defaultClient);
    try {
      FetchAllNotifications200Response result = apiInstance.fetchAllNotifications();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationApi#fetchAllNotifications");
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

[**FetchAllNotifications200Response**](FetchAllNotifications200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchNotifications"></a>
# **fetchNotifications**
> FetchNotifications200Response fetchNotifications(id)

Notification@show

Return a single notification

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.NotificationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    NotificationApi apiInstance = new NotificationApi(defaultClient);
    Integer id = 1; // Integer | notification id
    try {
      FetchNotifications200Response result = apiInstance.fetchNotifications(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationApi#fetchNotifications");
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
| **id** | **Integer**| notification id | |

### Return type

[**FetchNotifications200Response**](FetchNotifications200Response.md)

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

<a id="updateNotifications"></a>
# **updateNotifications**
> UpdateNotifications200Response updateNotifications(id, createNotificationsRequest)

Notification@update

Update a notification

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.NotificationApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    NotificationApi apiInstance = new NotificationApi(defaultClient);
    Integer id = 1; // Integer | notification id
    CreateNotificationsRequest createNotificationsRequest = new CreateNotificationsRequest(); // CreateNotificationsRequest | Notification definition
    try {
      UpdateNotifications200Response result = apiInstance.updateNotifications(id, createNotificationsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NotificationApi#updateNotifications");
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
| **id** | **Integer**| notification id | |
| **createNotificationsRequest** | [**CreateNotificationsRequest**](CreateNotificationsRequest.md)| Notification definition | |

### Return type

[**UpdateNotifications200Response**](UpdateNotifications200Response.md)

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

