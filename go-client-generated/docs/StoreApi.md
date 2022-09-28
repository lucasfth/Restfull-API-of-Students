# {{classname}}

All URIs are relative to *https://petstore3.swagger.io/api/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DeleteOrder**](StoreApi.md#DeleteOrder) | **Delete** /store/order/{orderId} | Delete purchase order by ID
[**GetInventory**](StoreApi.md#GetInventory) | **Get** /store/inventory | Returns student inventories by status
[**GetOrderById**](StoreApi.md#GetOrderById) | **Get** /store/order/{orderId} | Find purchase order by ID
[**PlaceOrder**](StoreApi.md#PlaceOrder) | **Post** /store/order | Place an order for a student

# **DeleteOrder**
> DeleteOrder(ctx, orderId)
Delete purchase order by ID

For valid response try integer IDs with value < 1000. Anything above 1000 or nonintegers will generate API errors

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **orderId** | **int64**| ID of the order that needs to be deleted | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetInventory**
> map[string]int32 GetInventory(ctx, )
Returns student inventories by status

Returns a map of status codes to quantities

### Required Parameters
This endpoint does not need any parameter.

### Return type

**map[string]int32**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetOrderById**
> Order GetOrderById(ctx, orderId)
Find purchase order by ID

For valid response try integer IDs with value <= 5 or > 10. Other values will generate exceptions.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **orderId** | **int64**| ID of order that needs to be fetched | 

### Return type

[**Order**](Order.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **PlaceOrder**
> Order PlaceOrder(ctx, optional)
Place an order for a student

Place a new order in the store

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***StoreApiPlaceOrderOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a StoreApiPlaceOrderOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**optional.Interface of Order**](Order.md)|  | 
 **id** | **optional.**|  | 
 **studentId** | **optional.**|  | 
 **quantity** | **optional.**|  | 
 **shipDate** | **optional.**|  | 
 **status** | **optional.**|  | 
 **complete** | **optional.**|  | 

### Return type

[**Order**](Order.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/xml, application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

