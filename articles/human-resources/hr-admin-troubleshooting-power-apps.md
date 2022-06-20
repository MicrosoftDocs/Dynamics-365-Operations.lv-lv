---
title: Nevar izveidot vidi Power Apps administrēšanas centrā
description: Šajā rakstā paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc62d3c8fe560d4f7d2e754a79de6fec3ef6041b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882929"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Nevar izveidot vidi Power Apps administrēšanas centrā


[!INCLUDE [PEAP](../includes/peap-2.md)]

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
