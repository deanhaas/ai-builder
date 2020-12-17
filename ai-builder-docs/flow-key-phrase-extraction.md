---
title: Use the key phrase extraction prebuilt model in Power Automate - AI Builder | Microsoft Docs
description: Provides information about how to set up and use the AI Builder key phrase extraction prebuilt model in Power Automate.
author: alanabrito
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 03/10/2020
ms.author: alanab
ms.reviewer: v-dehaas
---

# Use the key phrase extraction prebuilt model in Power Automate

1. Sign in to [Power Automate](https://flow.microsoft.com/), select the **My flows** tab, and then select **New > +Instant-from blank**.
1. Name your flow, select **Manually trigger a flow** under **Choose how to trigger this flow**, and then select **Create**.
1. Expand **Manually trigger a flow**, select **+Add an input**, select **Text** as the input type, and set as input title **My Text**.
1. Select **+ New step**, search for the term **AI Builder**, and then select **Extract the key phrases from text** in the list of actions.
1. Select the language in the Language input and specify the **My Text** column from the trigger in the Text input:

    > [!div class="mx-imgBorder"]
    > ![Specify my text](media/flow-kpe.png "Specify my text")

1. In the successive actions, you can use any fields extracted by the AI Builder model. For example, you can create a Microsoft Dataverse record for each **Key phrase**:

    > [!div class="mx-imgBorder"]
    > ![Add key phrases screen](media/flow-add-phrase-2.png "Add key phrases in Dataverse")

## Parameters

### Input

|Name |Required |Type |Description |Values |
|---------|---------|---------|---------|---------|
|**Text** |Yes |string |Text to analyze |Text sentences |
|**Language** |Yes |string | Language of the text to analyze | Item in a list of predefined languages or a language code (ex.: "en", "fr", "zh_chs", "ru")

### Output

|Name |Type |Description |
|---------|---------|---------|
|**Key phrase** |string |String denoting a key talking points in the analyzed text. As there could be multiple key phrases, selecting this parameter will create an apply to each loop |

Congratulations! You have created a flow that uses your key phrase extraction AI model. Select **Save** on the top right and then select **Test** to try out your flow.

### See also

[Key phrase extraction overview](prebuilt-key-phrase.md)
