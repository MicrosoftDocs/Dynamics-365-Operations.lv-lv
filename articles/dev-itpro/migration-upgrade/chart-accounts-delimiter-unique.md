---
title: "Unikāla kontu plāna norobežotāja nodrošināšana"
description: "Risinājumā Dynamics 365 for Finance and Operations nevar būt tāds pats norobežotājs kontu plānam un dimensijas vērtībām. Pēc jaunināšanas ir jāmaina norobežotāja vērtības."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Unikāla kontu plāna norobežotāja nodrošināšana

[!include [banner](../includes/banner.md)]

Programmā Microsoft Dynamics AX 2012 varēja izmantot tādu pašu norobežotāju kontu plānam un dimensijas vērtībām. Risinājumā Dynamics 365 for Finance and Operations nevar būt tāds pats norobežotājs kontu plānam un dimensijas vērtībām. Ja norobežotājam ir dublikāts, to var mainīt pēc jaunināšanas. 

Šī funkcija ir pieejama:
- Dynamics 365 for Finance and Operations versijā 8.0
- Dynamics 365 for Finance and Operations versijā 7.1, KB 4094701 Nevar ievadīt finanšu dimensijas, ja dimensijas vērtības satur kontu plāna norobežotāju
- Dynamics 365 for Finance and Operations versijā 7.2, KB 4092967 Nevar izvēlēties apakšprojektu kā dimensiju, ja apakšprojekta formātā ir dimensiju norobežotājs

## <a name="update-delimiter"></a>Norobežotāja atjaunināšana
Ja ir radies konflikts ar kontu plānu, var mainīt kontu plāna norobežotāju un projekta/apakšprojekta ID formātu. Citus dimensiju norobežotājus nevar mainīt. 
- Kontu plāna norobežotāju var mainīt pēc jaunināšanas uz Finance and Operations sadaļā **Virsgrāmatas parametri** > **Kontu plāns un dimensijas** > **Mainīt norobežotāju**. 
- Ja vienīgais konflikts ir ar projekta/apakšprojekta ID formātu, varat mainīt šo vērtību sadaļā **Projektu vadības un uzskaites parametri** > **Vispārīgi** > **Apakšprojektu formāta modificēšana**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kā noteikt, vai jūsu vidē ir nepieciešams atjaunināt norobežotājus 
Ja norobežotāji jauninātajā vidē ir konfliktējoši, var veidoties nestabilitāte, ievadot vērtības segmentētas ievades vadīklā vai dimensiju ievades vadīklā. Tas nozīmē, ka būs nepieciešams vienmēr izmantot meklēšanas rezultātus vai uznirstošo izvēlni, ievadot kontu un dimensiju kombinācijas.

