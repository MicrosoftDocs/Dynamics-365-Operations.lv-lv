---
title: Nevar izveidot vidi Power Apps administrēšanas centrā
description: Šajā rakstā paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73c8910900ba6486a8e60a547b07ea0c82a6cb10
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053351"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Nevar izveidot vidi Power Apps administrēšanas centrā

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Izejas plūsma**

- Nomnieka/vides administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
- Lietotājam nav licences, kas dod tiesības izveidot vides.

**Risinājums**

Pārliecinieties, vai nomnieka administrators ir piešķīris derīgu Power Apps P2 licenci lietotājam, kas veido vidi. Šādi Microsoft Dynamics pakalpojumu plāni sniedz atļaujas vides izveidošanai:

| Vispārēja preču noliktavas vienība (SKU)       | Power Apps P2 pakalpojumu plāns  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 plāns Enterprise Edition | Power Apps for Dynamics 365 |

Ņemiet vērā, ka šīs tiesības nodrošina arī dažādas Microsoft Office SKU, kā arī savrupas Power Apps 2. plāna SKU. Ir svarīgi, lai būtu viena šīm SKU.

1. Dodieties uz [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Izveidojiet vides, izpildot instrukcijas [Human Resources nodrošināšana](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]