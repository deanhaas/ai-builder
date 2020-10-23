---
title: Security in AI Builder - AI Builder | Microsoft Docs
description: Describes security information related to roles, privileges, and access in AI Builder and the services it connects to. 
author: Dean-Haas
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 09/06/2019
ms.author: v-dehaas
ms.reviewer: v-dehaas
---

# Security in AI Builder

AI Builder relies on environment security and Common Data Service security roles and privileges to grant access to AI features in Power Apps. More information: [Security overview](/power-platform/admin/wp-security)

Some privileges are set by default in Common Data Service. This allows built-in security roles to use AI Builder without further actions from system administrators. Specifically:

- Environment makers can use AI Builder to create AI models.
- Common Data Service users can access data by using the models embedded in Power Apps.
- Administrators and system customizers can access all AI models created in the environment.

These security roles have privileges to the AI Builder entities in Common Data Service. Custom security roles can create AI models if they have the same access to the AI Builder entities as the environment maker role.

> [!div class="mx-imgBorder"]
> ![Security roles screen](media/security-roles-screen.png "Security roles screen" )

Scenarios such as object detection, category classification, and prediction require Read access to Common Data Service entities. Make sure environment makers have access to them. They need those entities for objects to detect, tagged text, and input data.

Some features require system customizer privileges to publish your AI models and to allow them to be consumed. These actions can make changes to the Common Data Service schema. Administrators should assign system customizer privileges to users who want to create such AI models.

When you create a prediction AI model, a new field is added to the input entity to store the prediction results. For this reason, you need at least system customizer rights to publish the model for the first time.

For category classification AI models, an entity is created for every new model as soon as the model runs for the first time. Therefore, only system customizers or administrators can run the model. After the model runs, administrators must modify the access rights to the newly created category classification entity in Common Data Service to allow users to use the results.

### See also

[Security concepts in Common Data Service](/power-platform/admin/wp-security-cds)
