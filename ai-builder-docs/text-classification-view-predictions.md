---
title: View generated results - AI Builder | Microsoft Docs
description: Provides steps to view category classification predictions after you publish your model in AI Builder.
author: raaourik 
ms.service: aibuilder
ms.topic: conceptual
ms.custom: 
ms.date: 11/06/2020
ms.author: raaourik
ms.reviewer: v-dehaas
---

# View results

[!INCLUDE [cc-data-platform-banner](includes/cc-data-platform-banner.md)]

This topic shows you how to see the output of your prediction model.

1. After you select **Use Model** and configure it to run on Microsoft Dataverse, the output location appears in the **Settings** pane under the **Run** pivot.

    The name shown in **Tags output** is the name of the entity and attribute that's created after publishing. It's a link that takes you to the entity viewer section where the new fields added by AI Builder appear.

2. In the **Views** section, see values of the output fields for the different records. Use the **Filter by** function in the lower-right side pane to filter for only the records that don't have a label.

3. Next, you can build a basic model-driven app to use the output. For information about how to build a model-driven app in Power Apps, see [model-driven app overview](/powerapps/maker/model-driven-apps/model-driven-app-overview).

### Next step

[Use a category classification model to generate tags](text-classification-model-use-tags.md)
