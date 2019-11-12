---
title: Unikāla kontu plāna norobežotāja iestatīšana
description: Šajā tēmā ir paskaidrots, kā kontu plānam un dimensijas vērtībām nevar izmantot vienu un to pašu norobežotāju. Pēc jaunināšanas ir jāmaina norobežotāja vērtības.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 5861bcaa42f7bc5ec20916fe1a44418bdd9c2ffe
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550912"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Unikāla kontu plāna norobežotāja iestatīšana

[!include [banner](../includes/banner.md)]

Programmā Microsoft Dynamics AX 2012 kontu plānam un dimensijas vērtībām varēja izmantot vienu un to pašu norobežotāju. Finance and Operations pašreizējās versijās nevar būt tāds pats norobežotājs kontu plānam un dimensijas vērtībām. Ja norobežotājam ir dublikāts, to var mainīt pēc jaunināšanas. 

Šī funkcija ir pieejama tālāk minētajās versijās.
- Finance and Operations versija 8.0
- Finance and Operations versija 7.1, KB 4094701. Nevar ievadīt finanšu dimensijas, ja dimensijas vērtības satur kontu plāna norobežotāju
- Finance and Operations versija 7.2, KB 4092967. Nevar izvēlēties apakšprojektu kā dimensiju, ja apakšprojekta formāts satur dimensijas norobežotāju

## <a name="update-delimiter"></a>Norobežotāja atjaunināšana
Ja ir radies konflikts ar kontu plānu, var mainīt kontu plāna norobežotāju un projekta/apakšprojekta ID formātu. Citus dimensiju norobežotājus nevar mainīt. 
- Kontu plāna norobežotāju var mainīt pēc jaunināšanas sadaļā **Virsgrāmatas parametri** > **Kontu plāns un dimensijas** > **Mainīt norobežotāju**. 
- Ja vienīgais konflikts ir ar projekta/apakšprojekta ID formātu, varat mainīt šo vērtību sadaļā **Projektu vadības un uzskaites parametri** > **Vispārīgi** > **Apakšprojektu formāta modificēšana**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kā noteikt, vai jūsu vidē ir nepieciešams atjaunināt norobežotājus 
Ja norobežotāji jauninātajā vidē ir konfliktējoši, var veidoties nestabilitāte, ievadot vērtības segmentētas ievades vadīklā vai dimensiju ievades vadīklā. Tas nozīmē, ka būs nepieciešams vienmēr izmantot meklēšanas rezultātus vai uznirstošo izvēlni, ievadot kontu un dimensiju kombinācijas.
