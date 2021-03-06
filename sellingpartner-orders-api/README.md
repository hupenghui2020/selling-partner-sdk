# swagger-java-client

Selling Partner API for Orders
- API version: v0
  - Build date: 2020-12-15T20:03:19.199+08:00

The Selling Partner API for Orders helps you programmatically retrieve order information. These APIs let you develop fast, flexible, custom applications in areas like order synchronization, order research, and demand-based decision support tools.

  For more information, please visit [https://sellercentral.amazon.com/gp/mws/contactus.html](https://sellercentral.amazon.com/gp/mws/contactus.html)

*Automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen)*


## Requirements

Building the API client library requires:
1. Java 1.7+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>io.swagger</groupId>
  <artifactId>swagger-java-client</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "io.swagger:swagger-java-client:1.0.0"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/swagger-java-client-1.0.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import com.amazon.spapi.orders.*;
import com.amazon.spapi.orders.auth.*;
import com.amazon.spapi.orders.model.*;
import com.amazon.spapi.orders.api.OrdersV0Api;

import java.io.File;
import java.util.*;

public class OrdersV0ApiExample {

    public static void main(String[] args) {
        
        OrdersV0Api apiInstance = new OrdersV0Api();
        String orderId = "orderId_example"; // String | An Amazon-defined order identifier, in 3-7-7 format.
        try {
            GetOrderResponse result = apiInstance.getOrder(orderId);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersV0Api#getOrder");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://sellingpartnerapi-na.amazon.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*OrdersV0Api* | [**getOrder**](docs/OrdersV0Api.md#getOrder) | **GET** /orders/v0/orders/{orderId} | 
*OrdersV0Api* | [**getOrderAddress**](docs/OrdersV0Api.md#getOrderAddress) | **GET** /orders/v0/orders/{orderId}/address | 
*OrdersV0Api* | [**getOrderBuyerInfo**](docs/OrdersV0Api.md#getOrderBuyerInfo) | **GET** /orders/v0/orders/{orderId}/buyerInfo | 
*OrdersV0Api* | [**getOrderItems**](docs/OrdersV0Api.md#getOrderItems) | **GET** /orders/v0/orders/{orderId}/orderItems | 
*OrdersV0Api* | [**getOrderItemsBuyerInfo**](docs/OrdersV0Api.md#getOrderItemsBuyerInfo) | **GET** /orders/v0/orders/{orderId}/orderItems/buyerInfo | 
*OrdersV0Api* | [**getOrders**](docs/OrdersV0Api.md#getOrders) | **GET** /orders/v0/orders | 


## Documentation for Models

 - [Address](docs/Address.md)
 - [BuyerCustomizedInfoDetail](docs/BuyerCustomizedInfoDetail.md)
 - [BuyerTaxInfo](docs/BuyerTaxInfo.md)
 - [Error](docs/Error.md)
 - [ErrorList](docs/ErrorList.md)
 - [FulfillmentInstruction](docs/FulfillmentInstruction.md)
 - [GetOrderAddressResponse](docs/GetOrderAddressResponse.md)
 - [GetOrderBuyerInfoResponse](docs/GetOrderBuyerInfoResponse.md)
 - [GetOrderItemsBuyerInfoResponse](docs/GetOrderItemsBuyerInfoResponse.md)
 - [GetOrderItemsResponse](docs/GetOrderItemsResponse.md)
 - [GetOrderResponse](docs/GetOrderResponse.md)
 - [GetOrdersResponse](docs/GetOrdersResponse.md)
 - [Money](docs/Money.md)
 - [Order](docs/Order.md)
 - [OrderAddress](docs/OrderAddress.md)
 - [OrderBuyerInfo](docs/OrderBuyerInfo.md)
 - [OrderItem](docs/OrderItem.md)
 - [OrderItemBuyerInfo](docs/OrderItemBuyerInfo.md)
 - [OrderItemBuyerInfoList](docs/OrderItemBuyerInfoList.md)
 - [OrderItemList](docs/OrderItemList.md)
 - [OrderItemsBuyerInfoList](docs/OrderItemsBuyerInfoList.md)
 - [OrderItemsList](docs/OrderItemsList.md)
 - [OrderList](docs/OrderList.md)
 - [OrdersList](docs/OrdersList.md)
 - [PaymentExecutionDetailItem](docs/PaymentExecutionDetailItem.md)
 - [PaymentExecutionDetailItemList](docs/PaymentExecutionDetailItemList.md)
 - [PaymentMethodDetailItemList](docs/PaymentMethodDetailItemList.md)
 - [PointsGrantedDetail](docs/PointsGrantedDetail.md)
 - [ProductInfoDetail](docs/ProductInfoDetail.md)
 - [PromotionIdList](docs/PromotionIdList.md)
 - [TaxClassification](docs/TaxClassification.md)
 - [TaxCollection](docs/TaxCollection.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author



