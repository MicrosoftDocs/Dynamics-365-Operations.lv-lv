---
title: Līdzekļu skaitītāju manuāla atjaunināšana
description: Šajā tēmā aprakstīta manuāla līdzekļu skaitītāju atjaunināšana programmā Līdzekļu pārvaldība.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 74d840cbb064018560a6abc2823f520c2f3179ac42b149c0507c9421a4e73391
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776438"
---
# <a name="manual-update-of-asset-counters"></a>Pamatlīdzekļu skaitītāju manuāla atjaunināšana

[!include [banner](../../includes/banner.md)]



Skaitītāji tiek izmantoti, lai veidotu reģistrācijas uz līdzekļa, piemēram, reģistrācijas par līdzekļa darbības stundu skaitu, vai par saražoto daudzumu.

Atlasītais skaitītāja veids var būt iestatīts tā, lai tas pārmantotu skaitītāja vērtības. Citiem vārdiem, opcija **Pārmantot līdzekļa skaitītāja vērtības** ir iestatīta uz **Jā**, kas atrodas kopsavilkuma cilnē **Vispārīgi** lapā **Skaitītāji** (**Līdzekļa pārvaldība** > **Iestatīšana** > **Līdzekļu veidi** > **Skaitītāji**). Šādā gadījumā, veidojot jaunu šī vaida skaitītāja rindu, katrs pakārtotais līdzeklis, kas izmanto tādu pašu skaitītāja veidu, tiek automātiski atjaunināts.

Lapā **Visi līdzekļi** jūs izveidojat stundu vai daudzuma skaitītāja reģistrācijas līdzeklim, pamatojoties uz jūsu līdzekļa lasījumiem.

1. Atlasiet **Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Visi līdzekļi**

2. Atlasiet līdzekli un pēc tam darbības rūtī, cilnē **Līdzeklis** grupā **Profilaktiska** atlasiet **Skaitītāji**. Lapā **Līdzekļu skaitītāji** ir redzams saraksts ar visām iepriekšējām skaitītāju reģistrācijām, kas tika veiktas atlasītajā līdzeklī.

3. Atlasiet **Jauns**, lai izveidotu reģistrāciju. Līdzekļa ID tiek automātiski ievadīts laukā **Līdzeklis**.

4. Laukā **Skaitītājs** atlasiet atbilstošo skaitītāju. Atlasei ir pieejami vienīgi tie skaitītāji, kas ir saistīti ar līdzekļa tipu, kas atlasīts līdzeklim. Saistītais vienums tiek automātiski ievadīts laukā **Vienums**.

5. Laukā **Reģistrētajā** atlasiet skaitītāja reģistrācijas datumu un laiku.

6. Laukā **Vērtība** ievadiet numuru kopš pēdējās skaitītāja reģistrācijas. Vai arī laukā **Uzkrātā vērtība** ievadiet kopējo skaitu.

Ņemiet vērā šādus punktus:

- Ja jūs līdzeklim fiziski instalējat jaunu skaitītāju, jums ir jāreģistrē līdzekļa izmaiņas lapā **Līdzekļa skaitītāji**. Pēc tam jāizveido divas reģistrācijas rindas ar identiskiem laikspiedoliem. Pirmajai rindai jābūt aizvietotajam skaitītājam. Rindā, kas saistīta ar jauno skaitītāju, atzīmējiet izvēles rūtiņu **Skaitītāja atiestatīšana**. Laukā **Kopsumma** kopējais skaits ir skaitītāja kopsummas no visām šajā skaitītāja tipā reģistrētajām vērtībām.

- Ja līdzeklī tiek atlasīta izvēles rūtiņa **Skaitītāja atiestatīšana**, izmantojot uzturēšanas plānu ar intervāla veidu "Vienreiz no..." vai "Kad sasniegts...", skaitītājs joprojām ir aktīvs jaunajai skaitītāja rindai, jo jūs izveidojat atsevišķu skaitītāja rindu un sākat no jauna ar jaunu skaitītāju.

Attēlā zemāk ir parādīta lapa **Līdzekļu skaitītāji**.

![1. attēls.](media/11-work-orders.png)

Lapā **Līdzekļu skaitītāji** (**Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu skaitītāji**) var veikt skaitītāja reģistrācijas vairākiem līdzekļiem vienlaicīgi, ja nepieciešams.

>[!NOTE]
>Varat iestatīt diapazonu, lai definētu novirzes manuālā skaitītāja reģistrācijās. Varat arī norādīt ziņojuma veidu, kas tiek parādīts, ja reģistrācijas ir ārpus definētā diapazona. Papildinformāciju par to, kā iestatīt saistītos skaitītājus, skatiet [Skaitītāji](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]