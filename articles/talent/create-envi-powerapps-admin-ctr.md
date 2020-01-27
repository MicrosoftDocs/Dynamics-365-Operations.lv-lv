---
title: Nevar izveidot vidi Power Apps administrēšanas centrā
description: Šajā tēmā ir paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft Power Apps administrēšanas centrā.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7a66b7624655aaf976aaa63b2626f65c54d0ea38
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898822"
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
2. Izveidojiet vides, izpildot instrukcijas sadaļā [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
