---
title: "Konteinera svara un tilpuma ietveršana kravā"
description: "Šajā tēmā ir aprakstīts, kā iestatīt un lietot funkcionalitāti konteinera svara un tilpuma ietveršanai kravās."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b137db6f67da30d6ac3a973940c1df1fd7268a1a
ms.openlocfilehash: ac1df9b430feb025e4a544a7ecd7baa0c919cbe4
ms.contentlocale: lv-lv
ms.lasthandoff: 10/02/2017

---

# <a name="include-container-weight-and-volume-on-load"></a>Konteinera svara un tilpuma ietveršana kravā

[!include[banner](../includes/banner.md)]

Funkcionalitāte konteinera svara un tilpuma ietveršanai kravā skaidri parāda kravu veidojošo konteineru un krājumu kopējo svaru un tilpumu.

Krava ietver atsevišķu sūtījumu vai vairākus sūtījumus, un šie sūtījumi ietver atsevišķus krājumus, kas pieder vienam pārdošanas pasūtījumam vai vairākiem pārdošanas pasūtījumiem. Šie krājumi tiek ievietoti konteinerā, un konteineri tiek ievietoti kravā. Arī krājumi, kas atrodas ārpus konteinera, var veidot daļu no kravas. Pamatojoties uz šiem nosacījumiem, sistēma aprēķina vērtības attiecībā uz kravas svaru un tilpumu, ņemot vērā gan konteineru, gan krājumu svaru un tilpumu.

Ja aprēķinātās vērtības nav precīzs, varat tās pielāgot, ievadot faktiskās vērtības attiecībā uz kravas svaru un tilpumu. Svara un tilpuma vērtības tiek izmantotas transportēšanas pārvaldības procesos. Šis vērtības tiek izmantotas, piemēram, likmju un maršrutu rīkā, kur tās palīdz definēt kravu likmi un maršrutu, un tās tiek izmantotas arī transportēšanas norēķinos un transportlīdzekļu vadītāju reģistrēšanai norīkojuma izpildei.

## <a name="where-it-applies"></a>Darbības tvērums

Funkcionalitāte konteinera svara un tilpuma ietveršanai kravā attiecas uz transportēšanas pārvaldības procesiem, piemēram, uz likmju un maršrutu rīku, transportēšanas norēķiniem un transportlīdzekļu vadītāju reģistrēšanu norīkojuma izpildei.

## <a name="how-it-is-set-up"></a>Kā to iestatīt

Par kravu uzskatāmo konteineru skaits tiek aprēķināts, pamatojoties uz konteinera svaru un tilpumu, kā arī uz konteinera izmantojuma procentuālo daudzumu.

-   Lai konteineram iestatītu svaru un tilpumu, noklikšķiniet uz **Noliktavas vadība** \> **Iestatījumi** \> **Konteineri** \> **Konteineru tipi**.

-   Lai iestatītu konteinera izmantojuma procentuālo vērtību, noklikšķiniet uz **Noliktavas vadība** \> **Iestatījumi** \> **Konteineri** \> **Konteineru grupas** un ievadiet vērtību laukā **Konteinera izmantojuma procentuālā vērtība**.

