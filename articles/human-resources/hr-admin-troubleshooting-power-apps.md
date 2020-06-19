---
title: Nevar izveidot vidi Power Apps administrēšanas centrā
description: Šajā rakstā paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431065"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Nevar izveidot vidi Power Apps administrēšanas centrā

**Izejas plūsma**

- Nomnieka/vides administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
- Licence, kas dod lietotājiem tiesības veikt vides izveides darbību, nav piešķirts tieši lietotājam, kurš veic attiecīgo darbību.

**Risinājums**

Pārliecinieties, ka nomnieka administrators ir piešķīris derīgu Power Apps P2 licenci tieši lietotājam, kurš veiks vides izveides soli. Tālāk ir norādīti Microsoft Dynamics pakalpojumu plāni, kas nodrošina šīs tiesības.

| Vispārēja preču noliktavas vienība (SKU)       | Power Apps P2 pakalpojumu plāns  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 plāns Enterprise Edition | Power Apps for Dynamics 365 |

Ņemiet vērā, ka šīs tiesības nodrošina arī dažādas Microsoft Office SKU, kā arī savrupas Power Apps 2. plāna SKU. Ir svarīgi, lai būtu viena šīm SKU.

1. Dodieties uz [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Izveidojiet vides, izpildot instrukcijas [Human Resources nodrošināšana](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
