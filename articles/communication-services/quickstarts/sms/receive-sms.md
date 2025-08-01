---
title: Receive an SMS message
titleSuffix: Azure Communication Services
description: This article describes how to receive an SMS message by using Azure Communication Services.
author: tophpalmer
manager: shahen
services: azure-communication-services
ms.author: chpalm
ms.date: 02/09/2023
ms.topic: quickstart
ms.service: azure-communication-services
ms.subservice: sms
ms.custom: devx-track-extended-java, devx-track-js
zone_pivot_groups: acs-js-power
---

# Receive an SMS message

Azure Communication Services SMS capabilities provide developers options to consume SMS received events. The events are posted to Azure Event Grid, which provides out of the box integrations to process those using webhooks, Azure Functions, Power Automate / Logic App connectors, and more.

Once received, SMS messages can be processed to respond to them or log them to a database for future access.

This article describes how to process SMS received events through Azure Functions using Event Grid triggers and no-code connectors for Power Automate / Logic Apps.

The `SMSReceived` event generated when an SMS is sent to an Azure Communication Services phone number is formatted in the following way:

```json
[{
  "id": "d29ebbea-3341-4466-9690-0a03af35228e",
  "topic": "/subscriptions/aaaa0a0a-bb1b-cc2c-dd3d-eeeeee4e4e4e/resourcegroups/acse2e/providers/microsoft.communication/communicationservices/{communication-services-resource-name}",
  "subject": "/phonenumber/15555555555",
  "data": {
    "MessageId": "d29ebbea-3341-4466-9690-0a03af35228e",
    "From": "15555555555",
    "To": "15555555555",
    "Message": "Great to connect with Azure Communication Services events",
    "ReceivedTimestamp": "2020-09-18T00:27:45.32Z"
  },
  "eventType": "Microsoft.Communication.SMSReceived",
  "dataVersion": "1.0",
  "metadataVersion": "1",
  "eventTime": "2020-09-18T00:27:47Z"
}]
```
> [!NOTE] 
> The format of `MessageId` returned by this API is considered an internal implementation detail and is subject to change without notice. Clients must treat message IDs as opaque identifiers and must not parse, infer structure, or build logic based on their format or content.

To start generating events, configure Azure Event Grid to use your Azure Communication Services resource.

> [!NOTE] 
> Using Azure Event Grid incurs more costs. For more information, see [Azure Event Grid pricing](https://azure.microsoft.com/pricing/details/event-grid/).

## Prerequisites

- An Azure account with an active subscription. [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
- An active Communication Services resource and connection string. [Create a Communication Services resource](../create-communication-resource.md).
- An SMS-enabled telephone number. [Get a phone number](../telephony/get-phone-number.md).
- Enable Event Grid resource provide on your subscription. See [instructions](../sms/handle-sms-events.md#register-an-event-grid-resource-provider).

::: zone pivot="programming-language-javascript"
[!INCLUDE [Receive SMS with Azure Function (JS)](./includes/receive-sms-js.md)]
::: zone-end

::: zone pivot="platform-power"
[!INCLUDE [Receive SMS with Power Automate and Logic Apps](./includes/receive-sms-no-code.md)]
::: zone-end

## Clean up resources

If you want to clean up and remove a Communication Services subscription, you can delete the resource or resource group. Deleting the resource group also deletes any other resources associated with it. Learn more about [cleaning up resources](../create-communication-resource.md#clean-up-resources).

## Toll-free verification

If you have a new toll-free number and want to send a [high volume of SMS messages](../../concepts/sms/sms-faq.md#what-happens-if-i-dont-verify-my-toll-free-numbers) or send SMS messages to Canadian phone numbers, see [SMS FAQ > Submit toll free verification](../../concepts/sms/sms-faq.md#how-do-i-submit-a-toll-free-verification) to learn how to verify your toll-free number.

## Next steps

> [!div class="nextstepaction"]
> [Send SMS](./send.md)

> [!div class="nextstepaction"]
> [Phone number types](../../concepts/telephony/plan-solution.md)

> [!div class="nextstepaction"]
> [Learn more about SMS](../../concepts/sms/concepts.md)