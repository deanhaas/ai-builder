---
title: Use the business card reader prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to use the AI Builder business card reader prebuilt model in Power Automate
author: alanabrito
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 12/12/2019
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the business card reader prebuilt model in Power Automate

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **File** as the input type, and set as input title **My Image**.
1. Select **+ New step**, search for **AI Builder** in the Search for filters and actions box, and then select **Read business card information** in the list of actions.
1. Leave **auto** in the **Image type** column as the type can be detected automatically.
1. Specify the **My Image** column from the trigger in the **Image** input for your flow:

    > [!div class="mx-imgBorder"]
    > ![Specify my image](media/flow-bcr.png "Specify my image")

1. Specify the **My Image** column from the trigger in the image input for your flow.

Congratulations! You've created a flow that uses the business card reader AI model. Select **Save** in the upper-right corner, and then select **Test** to try out your flow.

## Example business card reader flow
The following example shows a new contact being created in Microsoft Dataverse using the business card data.

   > [!div class="mx-imgBorder"]
   > !['Create new record' screen](media/flow-business-card-overview-2.png "'Create new record' screen")

## Parameters

### Input

|Name |Required |Type |Description |Values |
|---------|---------|---------|---------|---------|
|**Image type** |Yes |string |Mime type of the image|"auto" as default value. This column being obsolete, any value will be accepted. |
|**Image** |Yes |file |Image file to analyze| |


### Output

|Name |Type |Description |
|---------|---------|---------|
|**City** |string |The city address|
|**Country** |string |The country address|
|**Postal Code** |string |The postal code address|
|**PO Box** |string |The post office box address|
|**State** |string |The state address|
|**Street** |string |The street address|
|**Work phone or other phone** |string |The first phone or fax number|
|**Cleaned image** |file |The image after processing where the business card appears cropped and enhanced from the original image|
|**Cleaned image type** |string |Type of the cleaned image|
|**Company name** |string |The company name|
|**Department** |string |The organization department found|
|**Email** |string |The contact email found in the business card, if any|
|**Fax** |string |The third phone or fax number|
|**First name** |string |The contact first name|
|**Full address** |string |The contact full address|
|**Full name** |string |The contact full name|
|**Title** |string |The contact job title|
|**Last name** |string |The contact last name|
|**Mobile phone** |string |The second phone or fax number|
|**Website** |string |The website|

## See also

[Business card reader overview](prebuilt-business-card.md)
