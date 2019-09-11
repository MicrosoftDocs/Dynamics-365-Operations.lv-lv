---
title: Līdzekļu skaitītāju manuāla atjaunināšana
description: Šajā tēmā aprakstīta manuāla līdzekļu skaitītāju atjaunināšana programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875779"
---
# <a name="manual-update-of-asset-counters"></a>Līdzekļu skaitītāju manuāla atjaunināšana

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Skaitītāji tiek izmantoti, lai izveidotu līdzekļa reģistrācijas, piemēram, attiecībā uz darbības stundām vai saražoto vienību daudzumu.

Ja skaitītāja tips, kas atlasīts skaitītājam, ir iestatīts uz mantotām skaitītāja vērtībām (**Līdzekļu pārvaldība** > **Uzstādīšana** > **Līdzekļu tipi** > **Skaitītāji** > **Vispārīgi** kopsavilkuma cilne > pārslēgšanas poga **Mantot līdzekļa skaitītāja vērtības** iestatīta uz "Jā"), tad, izveidojot jaunu skaitītāja rindu šim tipam, jebkurš apakšlīdzeklis, kurš izmanto to pašu skaitītāja tipu, tiek automātiski atjaunināts.

Laukā **Visi līdzekļi** jūs izveidojat stundu vai daudzuma skaitītāja reģistrācijas līdzeklim, pamatojoties uz jūsu līdzekļa lasījumiem.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Līdzekļi** > **Visi līdzekļi**.

2. Sarakstā atlasiet līdzekli un noklikšķiniet uz **Skaitītāji**. Veidlapā **Līdzekļu skaitītāji** ir redzams saraksts ar visām iepriekšējām skaitītāju reģistrācijām atlasītajā līdzeklī.

3. Lai izveidotu jaunu reģistrāciju, noklikšķiniet uz **Jauns**. Līdzekļa ID tiek ievietots automātiski.

4. Laukā **Skaitītājs** atlasiet atbilstošo skaitītāju. Ir pieejami vienīgi tie skaitītāji, kas ir saistīti ar līdzekļa tipu, kas atlasīts līdzeklim. Saistītai vienums tiek automātiski ievadīts laukā **Vienums**.

5. Atlasiet skaitītāja reģistrācijas datumu un laiku.

6. Laukā **Vērtība** ievadiet skaitu kopš pēdējās skaitītāja reģistrācijas vai laukā **Apkopotā vērtība** ievadiet kopējo skaitu.

- Ja jūs līdzeklim fiziski instalējat jaunu skaitītāju, jums ir jāreģistrē līdzekļa izmaiņas laukā **Līdzekļa skaitītāji**. Pēc tam jums ir jāizveido divas reģistrācijas rindas ar identiskiem laikspiedoliem un rindā, kas attiecas uz jauno skaitītāju, jūs atlasāt izvēles rūtiņu **Skaitītāja atiestatīšana**. Izveidojot divas reģistrācijas rindas, pirmajai rindai ir jāattiecas uz skaitītāju, kuru aizvietojat. Laukā **Kopsumma** kopējais skaits ir skaitītāja kopsumma no visām šajā skaitītāja tipā reģistrētajām vērtībām.  
- Ja līdzeklī tiek atlasīta izvēles rūtiņa **Skaitītāja atiestatīšana**, izmantojot uzturēšanas plānu ar intervāla tipu "Vienreiz no..." vai "Kad sasniegts...", skaitītājs joprojām ir aktīvs jaunajai skaitītāja rindai, jo jūs izveidojat atsevišķu skaitītāja rindu un sākat no jauna ar jaunu skaitītāju.

![1. attēls](media/11-work-orders.png)


Ja jums ir jāveic skaitītāja reģistrācijas vairākiem līdzekļiem, to var izdarīt **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu skaitītāji**.

>[!NOTE]
>Jūs varat uzstādīt diapazonu, lai definētu nobīdes manuālajās skaitītāja reģistrācijās un ziņojuma veidu, kurš būtu jāuzrāda, ja reģistrācijas ir ārpus definētā diapazona. Skatiet tēmu [Skaitītāji](../setup-for-objects/counters.md) attiecībā uz skaitītāju uzstādīšanu.
