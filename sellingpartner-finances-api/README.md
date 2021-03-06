# swagger-java-client

Selling Partner API for Finances
- API version: v0
  - Build date: 2020-12-15T20:01:58.583+08:00

The Selling Partner API for Finances helps you obtain financial information relevant to a seller's business. You can obtain financial events for a given order, financial event group, or date range without having to wait until a statement period closes. You can also obtain financial event groups for a given date range.

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

import com.amazon.spapi.finances.*;
import com.amazon.spapi.finances.auth.*;
import com.amazon.spapi.finances.model.*;
import com.amazon.spapi.finances.api.DefaultApi;

import java.io.File;
import java.util.*;

public class DefaultApiExample {

    public static void main(String[] args) {
        
        DefaultApi apiInstance = new DefaultApi();
        Integer maxResultsPerPage = 100; // Integer | The maximum number of results to return per page.
        OffsetDateTime financialEventGroupStartedBefore = OffsetDateTime.now(); // OffsetDateTime | A date used for selecting financial event groups that opened before (but not at) a specified date and time, in ISO 8601 format. The date-time  must be later than FinancialEventGroupStartedAfter and no later than two minutes before the request was submitted. If FinancialEventGroupStartedAfter and FinancialEventGroupStartedBefore are more than 180 days apart, no financial event groups are returned.
        OffsetDateTime financialEventGroupStartedAfter = OffsetDateTime.now(); // OffsetDateTime | A date used for selecting financial event groups that opened after (or at) a specified date and time, in ISO 8601 format. The date-time must be no later than two minutes before the request was submitted.
        String nextToken = "nextToken_example"; // String | A string token returned in the response of your previous request.
        try {
            ListFinancialEventGroupsResponse result = apiInstance.listFinancialEventGroups(maxResultsPerPage, financialEventGroupStartedBefore, financialEventGroupStartedAfter, nextToken);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling DefaultApi#listFinancialEventGroups");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://sellingpartnerapi-na.amazon.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**listFinancialEventGroups**](docs/DefaultApi.md#listFinancialEventGroups) | **GET** /finances/v0/financialEventGroups | 
*DefaultApi* | [**listFinancialEvents**](docs/DefaultApi.md#listFinancialEvents) | **GET** /finances/v0/financialEvents | 
*DefaultApi* | [**listFinancialEventsByGroupId**](docs/DefaultApi.md#listFinancialEventsByGroupId) | **GET** /finances/v0/financialEventGroups/{eventGroupId}/financialEvents | 
*DefaultApi* | [**listFinancialEventsByOrderId**](docs/DefaultApi.md#listFinancialEventsByOrderId) | **GET** /finances/v0/orders/{orderId}/financialEvents | 


## Documentation for Models

 - [AdjustmentEvent](docs/AdjustmentEvent.md)
 - [AdjustmentEventList](docs/AdjustmentEventList.md)
 - [AdjustmentItem](docs/AdjustmentItem.md)
 - [AdjustmentItemList](docs/AdjustmentItemList.md)
 - [AffordabilityExpenseEvent](docs/AffordabilityExpenseEvent.md)
 - [AffordabilityExpenseEventList](docs/AffordabilityExpenseEventList.md)
 - [ChargeComponent](docs/ChargeComponent.md)
 - [ChargeComponentList](docs/ChargeComponentList.md)
 - [ChargeInstrument](docs/ChargeInstrument.md)
 - [ChargeInstrumentList](docs/ChargeInstrumentList.md)
 - [CouponPaymentEvent](docs/CouponPaymentEvent.md)
 - [CouponPaymentEventList](docs/CouponPaymentEventList.md)
 - [Currency](docs/Currency.md)
 - [DebtRecoveryEvent](docs/DebtRecoveryEvent.md)
 - [DebtRecoveryEventList](docs/DebtRecoveryEventList.md)
 - [DebtRecoveryItem](docs/DebtRecoveryItem.md)
 - [DebtRecoveryItemList](docs/DebtRecoveryItemList.md)
 - [DirectPayment](docs/DirectPayment.md)
 - [DirectPaymentList](docs/DirectPaymentList.md)
 - [Error](docs/Error.md)
 - [ErrorList](docs/ErrorList.md)
 - [FBALiquidationEvent](docs/FBALiquidationEvent.md)
 - [FBALiquidationEventList](docs/FBALiquidationEventList.md)
 - [FeeComponent](docs/FeeComponent.md)
 - [FeeComponentList](docs/FeeComponentList.md)
 - [FinancialEventGroup](docs/FinancialEventGroup.md)
 - [FinancialEventGroupList](docs/FinancialEventGroupList.md)
 - [FinancialEvents](docs/FinancialEvents.md)
 - [ImagingServicesFeeEvent](docs/ImagingServicesFeeEvent.md)
 - [ImagingServicesFeeEventList](docs/ImagingServicesFeeEventList.md)
 - [ListFinancialEventGroupsPayload](docs/ListFinancialEventGroupsPayload.md)
 - [ListFinancialEventGroupsResponse](docs/ListFinancialEventGroupsResponse.md)
 - [ListFinancialEventsPayload](docs/ListFinancialEventsPayload.md)
 - [ListFinancialEventsResponse](docs/ListFinancialEventsResponse.md)
 - [LoanServicingEvent](docs/LoanServicingEvent.md)
 - [LoanServicingEventList](docs/LoanServicingEventList.md)
 - [NetworkComminglingTransactionEvent](docs/NetworkComminglingTransactionEvent.md)
 - [NetworkComminglingTransactionEventList](docs/NetworkComminglingTransactionEventList.md)
 - [PayWithAmazonEvent](docs/PayWithAmazonEvent.md)
 - [PayWithAmazonEventList](docs/PayWithAmazonEventList.md)
 - [ProductAdsPaymentEvent](docs/ProductAdsPaymentEvent.md)
 - [ProductAdsPaymentEventList](docs/ProductAdsPaymentEventList.md)
 - [Promotion](docs/Promotion.md)
 - [PromotionList](docs/PromotionList.md)
 - [RemovalShipmentEvent](docs/RemovalShipmentEvent.md)
 - [RemovalShipmentEventList](docs/RemovalShipmentEventList.md)
 - [RemovalShipmentItem](docs/RemovalShipmentItem.md)
 - [RemovalShipmentItemList](docs/RemovalShipmentItemList.md)
 - [RentalTransactionEvent](docs/RentalTransactionEvent.md)
 - [RentalTransactionEventList](docs/RentalTransactionEventList.md)
 - [RetrochargeEvent](docs/RetrochargeEvent.md)
 - [RetrochargeEventList](docs/RetrochargeEventList.md)
 - [SAFETReimbursementEvent](docs/SAFETReimbursementEvent.md)
 - [SAFETReimbursementEventList](docs/SAFETReimbursementEventList.md)
 - [SAFETReimbursementItem](docs/SAFETReimbursementItem.md)
 - [SAFETReimbursementItemList](docs/SAFETReimbursementItemList.md)
 - [SellerDealPaymentEvent](docs/SellerDealPaymentEvent.md)
 - [SellerDealPaymentEventList](docs/SellerDealPaymentEventList.md)
 - [SellerReviewEnrollmentPaymentEvent](docs/SellerReviewEnrollmentPaymentEvent.md)
 - [SellerReviewEnrollmentPaymentEventList](docs/SellerReviewEnrollmentPaymentEventList.md)
 - [ServiceFeeEvent](docs/ServiceFeeEvent.md)
 - [ServiceFeeEventList](docs/ServiceFeeEventList.md)
 - [ShipmentEvent](docs/ShipmentEvent.md)
 - [ShipmentEventList](docs/ShipmentEventList.md)
 - [ShipmentItem](docs/ShipmentItem.md)
 - [ShipmentItemList](docs/ShipmentItemList.md)
 - [SolutionProviderCreditEvent](docs/SolutionProviderCreditEvent.md)
 - [SolutionProviderCreditEventList](docs/SolutionProviderCreditEventList.md)
 - [TDSReimbursementEvent](docs/TDSReimbursementEvent.md)
 - [TDSReimbursementEventList](docs/TDSReimbursementEventList.md)
 - [TaxWithheldComponent](docs/TaxWithheldComponent.md)
 - [TaxWithheldComponentList](docs/TaxWithheldComponentList.md)
 - [TrialShipmentEvent](docs/TrialShipmentEvent.md)
 - [TrialShipmentEventList](docs/TrialShipmentEventList.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author



