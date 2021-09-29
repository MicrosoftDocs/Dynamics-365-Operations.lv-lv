---
title: Unikāla kontu plāna norobežotāja iestatīšana
description: Šajā tēmā ir paskaidrots, kā kontu plānam un dimensijas vērtībām nevar izmantot vienu un to pašu norobežotāju. Pēc jaunināšanas ir jāmaina norobežotāja vērtības.
author: panolte
ms.date: 09/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: a19dc8926df0efeac242e2e42ac37fdad91df9f8
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500507"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Unikāla kontu plāna norobežotāja iestatīšana

[!include [banner](../includes/banner.md)]

Programmā Microsoft Dynamics AX 2012 kontu plānam un dimensijas vērtībām varēja izmantot vienu un to pašu norobežotāju. Pašreizējās Finance and Operations versijās nevar būt tāds pats norobežotājs kontu plānam un dimensijas vērtībām. Ja norobežotājam ir dublikāts, to var mainīt pēc jaunināšanas. 

## <a name="update-delimiter"></a>Norobežotāja atjaunināšana
Ja ir radies konflikts ar kontu plānu, var mainīt kontu plāna norobežotāju un projekta/apakšprojekta ID formātu. Citus dimensiju norobežotājus nevar mainīt. 
- Kontu plāna norobežotāju var mainīt pēc jaunināšanas sadaļā **Virsgrāmatas parametri** > **Kontu plāns un dimensijas** > **Mainīt norobežotāju**. 
- Ja vienīgais konflikts ir ar projekta/apakšprojekta ID formātu, varat mainīt šo vērtību sadaļā **Projektu vadības un uzskaites parametri** > **Vispārīgi** > **Apakšprojektu formāta modificēšana**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kā noteikt, vai jūsu vidē ir nepieciešams atjaunināt norobežotājus 
Ja norobežotāji jauninātajā vidē ir konfliktējoši, var veidoties nestabilitāte, ievadot vērtības segmentētas ievades vadīklā vai dimensiju ievades vadīklā. Tas nozīmē, ka būs nepieciešams vienmēr izmantot meklēšanas rezultātus vai uznirstošo izvēlni, ievadot kontu un dimensiju kombinācijas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
