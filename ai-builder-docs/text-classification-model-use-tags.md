---
title: Use a model to generate tags - AI Builder | Microsoft Docs
description: Provides information about how to use category classification model–generated tags, and some troubleshooting information
author: raaourik 
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 11/06/2020
ms.author: raaourik 
ms.reviewer: v-dehaas
---


# Use a category classification model to generate tags

[!INCLUDE [cc-data-platform-banner](includes/cc-data-platform-banner.md)]

## Use in Power Automate

If you want to use your trained model in Power Automate, see [Use a category classification custom model in Power Automate](text-classification-model-in-flow.md).

<a name="set-run-schedule-on-common-data-service"></a>

## Set a run schedule on Microsoft Dataverse (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Go to the **Run** view in the **Model settings** panel to set the run schedule. To configure your model to run on your database and generate predictions, select **Generate predictions when new data is added**.

Your model runs whenever a new record is added to its entity.

> [!NOTE]
>You can’t set run schedule for imported category classification models.

## Use in Power Apps

You can integrate your AI Builder category classification models in Power Apps Studio by using the formula bar. More information: [Use formulas for text AI models](use-model.md#use-formulas-for-text-ai-models)

## What if the model isn't writing new tag suggestions?

- Check that you didn't exceed the number of runs for your Power Automate subscription.
- Turn off the Dataverse run setting, and then turn it back on.
