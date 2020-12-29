---
title: Transportēšanas kravas daļēja nosūtīšana
description: Šajā tēmā ir paskaidrots, kā var daļēji nosūtīt kravu un atlikt kravas noslodzes plānošanu.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e92a15cf4e2694eba1804184a02a7fd13159799e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432660"
---
# <a name="partial-shipment-of-a-transport-load"></a>Transportēšanas kravas daļēja nosūtīšana

[!include[banner](../includes/banner.md)]

Iestatot daļēju kravu nosūtīšanu, varat apstrādāt kravas gadījumos, kad noslodzi nevar noteikt, kamēr visas pārdošanas rindas nav pievienotas kravai. Procesu var pabeigt, kad ir zināms precīzs palešu skaits. Tādēļ nav jāizlemj, kuras paletes tiks piešķirtas kuram transportam, līdz brīdim, kad transportā fiziski tiek iekrauti izveidotie krājumi.

Šis līdzeklis piedāvā alternatīvu stingrākas struktūras ieviešanai, kurā jums jānosaka, kuras paletes tiks piešķirtas kuram transportam, pirms var izveidot izdošanas darbu vai iekraušanas darbu. Tā vietā lietotāji var konfigurēt atsevišķas kravas daļējas nosūtīšanas apstiprināšanai. Pēc tam var veikt transporta iekraušanas procesu attiecīgajām kravām. Tādēļ transportēšanas plānošanas nodaļa var plānot kravas, neņemot vērā atsevišķa transporta noslodzi.

Iekraušanas laikā darbinieki var definēt jaunu transportēšanas kravu, kurā var iekraut paleti. Vai arī tie var identificēt esošu transportēšanas kravu. Šos datus var ierakstīt, izmantojot mobilo ierīci. Tādēļ vairāki noliktavas darbinieki var iekraut krājumus no tās pašas kravas vai dažādām kravām tajā pašā kravas automašīnas. Pēc tam kravas var nosūtīt pilnībā vai daļēji.

> [!NOTE] 
> Lai iekrautu krājumus no kravas noteiktā transportēšanas kravā un daļēji nosūtītu kravu, ir jāģenerē darbs, izmantojot iekraušanas klasi darba veidnē. Parastu izdošanas darbu, kura tips ir **Izdošana**, nevar iekraut transportēšanas kravā, piemēram, kravas automašīnā.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Transportēšanas kravu iestatīšana daļējai nosūtīšanai

Kravu daļējas nosūtīšanas iestatīšana sastāv no divām procedūrām.

### <a name="set-the-loading-strategy"></a>Iekraušanas stratēģijas iestatīšana

Ir jāiespējo daļēja iekraušana, iestatot iekraušanas stratēģiju. Varat iestatīt iekraušanas stratēģiju pēc tam, kad esat izveidojis kravu.

1. Atlasiet **Noliktavas pārvaldība** \> **Kravas** \> **Visas kravas**.
2. Atlasiet kravu un pēc tam noklikšķiniet uz **Galvene**.
3. Laukā **Iekraušanas stratēģija** atlasiet **Atļauta daļējas kravas sūtīšana**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Izvēlnes elementa izveide transportēšanas kravu iekraušanai

Ir jāizveido jauns izvēlnes elements, kas ļauj veikt transportēšanas kravu iekraušanu. Transportēšanas kravas ļauj grupēt darba rindas no vienas vai vairākām kravām. Visu, kas tiek pievienots transportēšanas kravai, pēc tam var nosūtīt, izmantojot mobilo skeneri.

1. Atlasiet **Noliktavas pārvaldība** \> **Iestatīšana** \> **Mobilā ierīce** \> **Mobilās ierīces izvēlnes elementi**.
2. Atlasiet **Jauns** un pēc tam laukā **Režīms** atlasiet **Darbs**.
3. Iestatiet opciju **Izmantot esošo darbu** uz **Jā**.
4. Cilnes **Vispārīgi** laukā **Novirzītājs** atlasiet **Transporta iekraušana**.
5. Lai iespējotu sūtījuma apstiprinājumu, izmantojot mobilo skeneri, laukā **Atļautais nosūtīšanas apstiprināšanas tips** atlasiet vienumu **Transportēšanas krava**.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Transportēšanas kravas nosūtīšanas apstiprināšana no klienta

Šis iestatījums ļauj apstiprināt nosūtīšanai tādas transportēšanas kravas, kurās ir pilna vai daļēja krava.

1. Atlasiet **Noliktavas pārvaldība** \> **Kravas** \> **Transportēšanas kravas**.
2. Darbību rūtī, cilnē **Nosūtīt un saņemt**, grupā **Apstiprināt** atlasiet **Transportēšana**.
