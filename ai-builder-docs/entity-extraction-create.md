---
title: Create a custom entity extraction AI model - AI Builder | Microsoft Docs
description: Provides steps to create a custom entity extraction AI model in AI Builder.
author: mfotedar
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 11/06/2020
ms.author: mfotedar
ms.reviewer: v-dehaas
---

# Create an entity extraction custom model

[!INCLUDE [cc-data-platform-banner](includes/cc-data-platform-banner.md)]

## Create your model

To create your custom entity extraction model:

1. Provide at least 10 examples of your text data.
1. Review the results from existing, prebuilt entities.
1. Refine your results by creating your own custom entities or modifying existing, prebuilt entities.
1. Review your model, and train it.
1. Evaluate your model (optional).

## Upload examples of your text data

You need at least 10 data examples to start customizing the model. AI Builder will identify some entities out of the box. You can customize your model by creating new entity types with a small set of examples or by modifying the existing entity types. 

To upload your data:

1. Sign in to [Power Apps](https://make.powerapps.com/) or [Power Automate](https://flow.microsoft.com/).
1. In the left pane, select **AI Builder** > **Build**, and then select **Entity Extraction**.
1. Enter a name for your model, and then select **Create**.
1. Select the **Common Data Service** entity and the field that contains your data.

## Review and refine entities 

AI Builder will automatically extract the prebuilt entity types from your uploaded examples. If the results are satisfactory, you don't need to customize a model and can use the [prebuilt entity extraction](prebuilt-entity-extraction.md) model out of the box.

You can customize your entity extraction model in these ways:

- Create a new entity type.

  You need to provide at least five examples to create a new entity type. For example, to create a new entity type named **size**, you can add an example like "The suitcase was {large}." The braces designate that "large" is of entity type **size**.

- Modify an existing entity type. 

  You need to add least five examples to an existing entity type to modify it.

- Deselect any prebuilt entities that you don't want to include in the model.

  You can select/deselect prebuilt entity types from the settings.

### Next step

[Train and publish your entity extraction custom model](entity-extraction-train.md).
