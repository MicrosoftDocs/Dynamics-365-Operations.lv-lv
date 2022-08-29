---
title: Unikāla kontu plāna norobežotāja iestatīšana
description: Šajā rakstā skaidrots, kā kontu plānam un dimensiju vērtībām nevar būt vienāds norobežotājs. Pēc jaunināšanas ir jāmaina norobežotāja vērtības.
author: RyanCCarlson2
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: RCarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.openlocfilehash: 2184d26e104f803ae1bf59155cf18f560652f318
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292502"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Unikāla kontu plāna norobežotāja iestatīšana

[!include [banner](../includes/banner.md)]

Programmā Microsoft Dynamics AX 2012 kontu plānam un dimensijas vērtībām varēja izmantot vienu un to pašu norobežotāju. Pašreizējā finanšu un operāciju versijās kontu plānam un dimensiju nosaukumiem vai vērtībām nevar būt vienāds norobežotājs. Ja norobežotājam ir dublikāts, to var mainīt pēc jaunināšanas. 

## <a name="update-delimiter"></a>Norobežotāja atjaunināšana
Ja ir radies konflikts ar kontu plānu, var mainīt kontu plāna norobežotāju un projekta/apakšprojekta ID formātu. Citus dimensiju norobežotājus nevar mainīt. 
- Kontu plāna norobežotāju var mainīt pēc jaunināšanas sadaļā **Virsgrāmatas parametri** > **Kontu plāns un dimensijas** > **Mainīt norobežotāju**. 
- Ja vienīgais konflikts ir ar projekta/apakšprojekta ID formātu, varat mainīt šo vērtību sadaļā **Projektu vadības un uzskaites parametri** > **Vispārīgi** > **Apakšprojektu formāta modificēšana**. 

### <a name="other-considerations"></a>Citi apsvērumi
Līdzīgi projekta/apakšprojekta ID visiem citiem pamatdatu ierakstiem, kas tiek izmantoti kā finanšu dimensijas, piemēram, kreditoriem vai debitoriem, nedrīkst būt konta ID vērtības, kas izmanto tādu pašu rakstzīmi kā kontu diagrammas norobežotājam. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kā noteikt, vai jūsu vidē ir nepieciešams atjaunināt norobežotājus 
Ja norobežotāji jauninātajā vidē ir konfliktējoši, var veidoties nestabilitāte, ievadot vērtības segmentētas ievades vadīklā vai dimensiju ievades vadīklā. Tas nozīmē, ka būs nepieciešams vienmēr izmantot meklēšanas rezultātus vai uznirstošo izvēlni, ievadot kontu un dimensiju kombinācijas.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

