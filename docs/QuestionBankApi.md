# QuestionBankApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createQuestionBankQuestion**](QuestionBankApi.md#createQuestionBankQuestion) | **POST** /api/v1/questions | QuestionBank@store |
| [**deleteQuestionBankQuestion**](QuestionBankApi.md#deleteQuestionBankQuestion) | **DELETE** /api/v1/questions/{id} | QuestionBank@destroy |
| [**downloadQuestionBankQuestionFile**](QuestionBankApi.md#downloadQuestionBankQuestionFile) | **GET** /api/v1/questions/{id}/files/{fileId} | QuestionBank@destroyFile |
| [**editQuestionBankQuestion**](QuestionBankApi.md#editQuestionBankQuestion) | **PATCH** /api/v1/questions/{id} | QuestionBank@update |
| [**fetchArchivedQuestionBankQuestions**](QuestionBankApi.md#fetchArchivedQuestionBankQuestions) | **GET** /api/v1/questions/archived | QuestionBank@indexArchived |
| [**fetchCustomQuestionBankQuestions**](QuestionBankApi.md#fetchCustomQuestionBankQuestions) | **GET** /api/v1/questions/custom | QuestionBank@indexCustom |
| [**fetchQuestionBankQuestion**](QuestionBankApi.md#fetchQuestionBankQuestion) | **GET** /api/v1/questions/{id} | QuestionBank@show |
| [**fetchQuestionBankQuestionVersion**](QuestionBankApi.md#fetchQuestionBankQuestionVersion) | **GET** /api/v1/questions/version/{id} | QuestionBank@showVersion |
| [**fetchQuestionBankQuestions**](QuestionBankApi.md#fetchQuestionBankQuestions) | **GET** /api/v1/questions | QuestionBank@index |
| [**fetchStandardQuestionBankQuestions**](QuestionBankApi.md#fetchStandardQuestionBankQuestions) | **GET** /api/v1/questions/standard | QuestionBank@indexStandard |
| [**fetchTeamQuestionBankQuestionsBySection**](QuestionBankApi.md#fetchTeamQuestionBankQuestionsBySection) | **GET** /api/v1/teams/{teamId}/questions/section/{sectionId} | TeamQuestionBank@indexBySection |
| [**updateQuestionBankQuestion**](QuestionBankApi.md#updateQuestionBankQuestion) | **PUT** /api/v1/questions/{id} | QuestionBank@update |
| [**updateQuestionBankQuestionStatus**](QuestionBankApi.md#updateQuestionBankQuestionStatus) | **PATCH** /api/v1/questions/{id}/{status} | QuestionBank@updateStatus |


<a id="createQuestionBankQuestion"></a>
# **createQuestionBankQuestion**
> CreateDarIntegration201Response createQuestionBankQuestion(createQuestionBankQuestionRequest)

QuestionBank@store

Create a new system question bank question with FE-helpful input format

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    CreateQuestionBankQuestionRequest createQuestionBankQuestionRequest = new CreateQuestionBankQuestionRequest(); // CreateQuestionBankQuestionRequest | QuestionBank definition
    try {
      CreateDarIntegration201Response result = apiInstance.createQuestionBankQuestion(createQuestionBankQuestionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#createQuestionBankQuestion");
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
| **createQuestionBankQuestionRequest** | [**CreateQuestionBankQuestionRequest**](CreateQuestionBankQuestionRequest.md)| QuestionBank definition | |

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

<a id="deleteQuestionBankQuestion"></a>
# **deleteQuestionBankQuestion**
> DeleteApplications200Response deleteQuestionBankQuestion(id)

QuestionBank@destroy

Delete a system question bank question

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer id = 1; // Integer | question bank question id
    try {
      DeleteApplications200Response result = apiInstance.deleteQuestionBankQuestion(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#deleteQuestionBankQuestion");
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
| **id** | **Integer**| question bank question id | |

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

<a id="downloadQuestionBankQuestionFile"></a>
# **downloadQuestionBankQuestionFile**
> DeleteApplications200Response downloadQuestionBankQuestionFile(id, fileId)

QuestionBank@destroyFile

Download a system question bank question

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer id = 1; // Integer | question bank question id
    Integer fileId = 1; // Integer | file uuid
    try {
      DeleteApplications200Response result = apiInstance.downloadQuestionBankQuestionFile(id, fileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#downloadQuestionBankQuestionFile");
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
| **id** | **Integer**| question bank question id | |
| **fileId** | **Integer**| file uuid | |

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

<a id="editQuestionBankQuestion"></a>
# **editQuestionBankQuestion**
> UpdateQuestionBankQuestion200Response editQuestionBankQuestion(id, editQuestionBankQuestionRequest)

QuestionBank@update

Edit a system question bank question - use this for parents and children separately

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer id = 1; // Integer | question bank question id
    EditQuestionBankQuestionRequest editQuestionBankQuestionRequest = new EditQuestionBankQuestionRequest(); // EditQuestionBankQuestionRequest | QuestionBank definition
    try {
      UpdateQuestionBankQuestion200Response result = apiInstance.editQuestionBankQuestion(id, editQuestionBankQuestionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#editQuestionBankQuestion");
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
| **id** | **Integer**| question bank question id | |
| **editQuestionBankQuestionRequest** | [**EditQuestionBankQuestionRequest**](EditQuestionBankQuestionRequest.md)| QuestionBank definition | |

### Return type

[**UpdateQuestionBankQuestion200Response**](UpdateQuestionBankQuestion200Response.md)

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

<a id="fetchArchivedQuestionBankQuestions"></a>
# **fetchArchivedQuestionBankQuestions**
> FetchQuestionBankQuestions200Response fetchArchivedQuestionBankQuestions(sectionId, isChild, perPage, page)

QuestionBank@indexArchived

List of archived question bank questions

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer sectionId = 1; // Integer | section id
    Integer isChild = 1; // Integer | filter on is_child field
    Integer perPage = 1; // Integer | per page
    Integer page = 1; // Integer | page
    try {
      FetchQuestionBankQuestions200Response result = apiInstance.fetchArchivedQuestionBankQuestions(sectionId, isChild, perPage, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#fetchArchivedQuestionBankQuestions");
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
| **sectionId** | **Integer**| section id | [optional] |
| **isChild** | **Integer**| filter on is_child field | [optional] |
| **perPage** | **Integer**| per page | [optional] |
| **page** | **Integer**| page | [optional] |

### Return type

[**FetchQuestionBankQuestions200Response**](FetchQuestionBankQuestions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchCustomQuestionBankQuestions"></a>
# **fetchCustomQuestionBankQuestions**
> FetchCustomQuestionBankQuestions200Response fetchCustomQuestionBankQuestions(sectionId, isChild, perPage, page)

QuestionBank@indexCustom

List of custom question bank questions

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer sectionId = 1; // Integer | section id
    Integer isChild = 1; // Integer | filter on is_child field
    Integer perPage = 1; // Integer | per page
    Integer page = 1; // Integer | page
    try {
      FetchCustomQuestionBankQuestions200Response result = apiInstance.fetchCustomQuestionBankQuestions(sectionId, isChild, perPage, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#fetchCustomQuestionBankQuestions");
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
| **sectionId** | **Integer**| section id | [optional] |
| **isChild** | **Integer**| filter on is_child field | [optional] |
| **perPage** | **Integer**| per page | [optional] |
| **page** | **Integer**| page | [optional] |

### Return type

[**FetchCustomQuestionBankQuestions200Response**](FetchCustomQuestionBankQuestions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchQuestionBankQuestion"></a>
# **fetchQuestionBankQuestion**
> FetchQuestionBankQuestion200Response fetchQuestionBankQuestion(id)

QuestionBank@show

Return the latest question bank question version for the supplied question id, in an FE-friendly format

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer id = 1; // Integer | question bank question id
    try {
      FetchQuestionBankQuestion200Response result = apiInstance.fetchQuestionBankQuestion(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#fetchQuestionBankQuestion");
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
| **id** | **Integer**| question bank question id | |

### Return type

[**FetchQuestionBankQuestion200Response**](FetchQuestionBankQuestion200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchQuestionBankQuestionVersion"></a>
# **fetchQuestionBankQuestionVersion**
> FetchQuestionBankQuestionVersion200Response fetchQuestionBankQuestionVersion(id)

QuestionBank@showVersion

Return a single system question bank question version

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer id = 1; // Integer | question bank question version id
    try {
      FetchQuestionBankQuestionVersion200Response result = apiInstance.fetchQuestionBankQuestionVersion(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#fetchQuestionBankQuestionVersion");
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
| **id** | **Integer**| question bank question version id | |

### Return type

[**FetchQuestionBankQuestionVersion200Response**](FetchQuestionBankQuestionVersion200Response.md)

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

<a id="fetchQuestionBankQuestions"></a>
# **fetchQuestionBankQuestions**
> FetchQuestionBankQuestions200Response fetchQuestionBankQuestions(sectionId, isChild, perPage, page)

QuestionBank@index

List of question bank questions

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer sectionId = 1; // Integer | section id
    Integer isChild = 1; // Integer | filter on is_child field
    Integer perPage = 1; // Integer | per page
    Integer page = 1; // Integer | page
    try {
      FetchQuestionBankQuestions200Response result = apiInstance.fetchQuestionBankQuestions(sectionId, isChild, perPage, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#fetchQuestionBankQuestions");
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
| **sectionId** | **Integer**| section id | [optional] |
| **isChild** | **Integer**| filter on is_child field | [optional] |
| **perPage** | **Integer**| per page | [optional] |
| **page** | **Integer**| page | [optional] |

### Return type

[**FetchQuestionBankQuestions200Response**](FetchQuestionBankQuestions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchStandardQuestionBankQuestions"></a>
# **fetchStandardQuestionBankQuestions**
> FetchStandardQuestionBankQuestions200Response fetchStandardQuestionBankQuestions(sectionId, isChild, perPage, page)

QuestionBank@indexStandard

List of standard question bank questions

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer sectionId = 1; // Integer | section id
    Integer isChild = 1; // Integer | filter on is_child field
    Integer perPage = 1; // Integer | per page
    Integer page = 1; // Integer | page
    try {
      FetchStandardQuestionBankQuestions200Response result = apiInstance.fetchStandardQuestionBankQuestions(sectionId, isChild, perPage, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#fetchStandardQuestionBankQuestions");
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
| **sectionId** | **Integer**| section id | [optional] |
| **isChild** | **Integer**| filter on is_child field | [optional] |
| **perPage** | **Integer**| per page | [optional] |
| **page** | **Integer**| page | [optional] |

### Return type

[**FetchStandardQuestionBankQuestions200Response**](FetchStandardQuestionBankQuestions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="fetchTeamQuestionBankQuestionsBySection"></a>
# **fetchTeamQuestionBankQuestionsBySection**
> FetchTeamQuestionBankQuestionsBySection200Response fetchTeamQuestionBankQuestionsBySection(teamId, sectionId, isChild)

TeamQuestionBank@indexBySection

List of question bank questions by section

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer teamId = 1; // Integer | Team ID
    Integer sectionId = 1; // Integer | section id
    Integer isChild = 1; // Integer | filter on is_child field
    try {
      FetchTeamQuestionBankQuestionsBySection200Response result = apiInstance.fetchTeamQuestionBankQuestionsBySection(teamId, sectionId, isChild);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#fetchTeamQuestionBankQuestionsBySection");
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
| **teamId** | **Integer**| Team ID | |
| **sectionId** | **Integer**| section id | |
| **isChild** | **Integer**| filter on is_child field | [optional] |

### Return type

[**FetchTeamQuestionBankQuestionsBySection200Response**](FetchTeamQuestionBankQuestionsBySection200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

<a id="updateQuestionBankQuestion"></a>
# **updateQuestionBankQuestion**
> UpdateQuestionBankQuestion200Response updateQuestionBankQuestion(id, updateQuestionBankQuestionRequest)

QuestionBank@update

Update a system question bank question - children and their versions are updated through parents

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer id = 1; // Integer | question bank question id
    UpdateQuestionBankQuestionRequest updateQuestionBankQuestionRequest = new UpdateQuestionBankQuestionRequest(); // UpdateQuestionBankQuestionRequest | QuestionBank definition
    try {
      UpdateQuestionBankQuestion200Response result = apiInstance.updateQuestionBankQuestion(id, updateQuestionBankQuestionRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#updateQuestionBankQuestion");
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
| **id** | **Integer**| question bank question id | |
| **updateQuestionBankQuestionRequest** | [**UpdateQuestionBankQuestionRequest**](UpdateQuestionBankQuestionRequest.md)| QuestionBank definition | |

### Return type

[**UpdateQuestionBankQuestion200Response**](UpdateQuestionBankQuestion200Response.md)

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

<a id="updateQuestionBankQuestionStatus"></a>
# **updateQuestionBankQuestionStatus**
> UpdateQuestionBankQuestionStatus200Response updateQuestionBankQuestionStatus(id, status)

QuestionBank@updateStatus

Lock, unlock, archive or unarchive a question bank question

### Example
```java
// Import classes:
import uk.ac.hdruk.gatewayapi.ApiClient;
import uk.ac.hdruk.gatewayapi.ApiException;
import uk.ac.hdruk.gatewayapi.Configuration;
import uk.ac.hdruk.gatewayapi.auth.*;
import uk.ac.hdruk.gatewayapi.models.*;
import uk.ac.hdruk.gatewayapi.api.QuestionBankApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    QuestionBankApi apiInstance = new QuestionBankApi(defaultClient);
    Integer id = 1; // Integer | question bank question id
    String status = "lock"; // String | lock or unlock
    try {
      UpdateQuestionBankQuestionStatus200Response result = apiInstance.updateQuestionBankQuestionStatus(id, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuestionBankApi#updateQuestionBankQuestionStatus");
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
| **id** | **Integer**| question bank question id | |
| **status** | **String**| lock or unlock | |

### Return type

[**UpdateQuestionBankQuestionStatus200Response**](UpdateQuestionBankQuestionStatus200Response.md)

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

