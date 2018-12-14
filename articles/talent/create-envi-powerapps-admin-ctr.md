---
title: "Nevar izveidot vidi PowerApps administrēšanas centrā"
description: "Šajā tēmā paskaidrots, kā rīkoties, ja administrators nevar izveidot vidi Microsoft PowerApps administr. centrā."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Nevar izveidot vidi PowerApps administrēšanas centrā

[!include [banner](includes/banner.md)]

**Izsniegt**

- Nomnieka/vides administrators nevar izveidot vidi Microsoft PowerApps administrēšanas centrā.
- Licence, kas dod lietotājiem tiesības veikt vides izveides darbību, nav piešķirts tieši lietotājam, kurš veic attiecīgo darbību.

**Risinājums**

Pārliecinieties, ka nomnieka administrators ir piešķīris derīgu PowerApps P2 licenci tieši lietotājam, kurš veiks vides izveides soli. Minētās tiesības nodrošina šādi Microsoft Dynamics pakalpojumu plāni.

| Vispārēja preču noliktavas vienība (SKU)       | PowerApps P2 pak. plāns  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps for Dynamics 365 |
| Microsoft Dynamics 365 pl. Enterprise Edition | PowerApps for Dynamics 365 |

Ņemiet vērā, ka dažādas Microsoft Office SKU arī nodrošina tiesības kopā ar savrupā PowerApps 2. plānu SKU. Ir svarīgi, lai būtu viena šīm SKU.

1. Dodieties uz [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Izveidojiet vides, izpildot instrukcijas sadaļā [Talent nodrošinājums](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

