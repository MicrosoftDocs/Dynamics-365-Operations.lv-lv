---
title: Nevar izveidot vidi Power Apps administrēšanas centrā
description: Šajā tēmā ir paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50a5aac71ec8ed850cfad32bdb1b8d589eb2885a
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413565"
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
