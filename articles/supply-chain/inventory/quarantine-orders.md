---
title: "Karantīnas pasūtījumi"
description: "Šajā tēmā ir aprakstīts, kā karantīnas pasūtījumi tiek izmantoti, lai bloķētu krājumus."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9a05c35d2e4a9e3ad81421eac863d182e8a6b499
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="quarantine-orders"></a>Karantīnas pasūtījumi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā karantīnas pasūtījumi tiek izmantoti, lai bloķētu krājumus.

Karantīnas pasūtījumus var izmantot, lai bloķētu krājumu. Piemēram, varat noteikt krājumu karantīnu kvalitātes kontroles iemeslu dēļ. Krājumi, kam ir noteikta karantīna, tiek pārsūtīti uz karantīnas noliktavu. **Piezīme.** Ja izmantojat papildu noliktavas pārvaldības procesus (modulī Noliktavas pārvaldība), karantīnas pasūtījumu apstrāde tiek izmantota tikai atgriešanas pārdošanas pasūtījumiem.

## <a name="quarantine-on-hand-inventory-items"></a>Rīcībā esošo krājumu karantīna
Kad novietojat krājumus karantīnā, varat izveidot karantīnas pasūtījumus manuāli vai arī iestatīt, lai sistēma ienākošās apstrādes laikā automātiski izveidotu karantīnas pasūtījumus. Lai automātiski izveidotu karantīnas pasūtījumus, atlasiet opciju **Karantīnas pārraudzība** lapas **Krājumu modeļu grupas** cilnē **Krājumu politikas**. Jums jānorāda arī noklusējuma karantīnas noliktava laukā **Karantīnas noliktava** saņemošajām noliktavām. Ja fiziski rīcībā esošie krājumi tiek reģistrēti, izmantojot pirkšanas pasūtījumu vai ražošanas pasūtījumu, karantīnā novietotie krājumi automātiski tiek pārvietoti uz karantīnas noliktavu programmā Microsoft Dynamics 365 for Finance and Operations. Šī kustība notiek tāpēc, ka karantīnas pasūtījuma statuss tiek mainīts uz **Sākts**. Kad jūs izveidojat karantīnas pasūtījumus manuāli, krājumu nav nepieciešams iestatīt karantīnas pārraudzībai saistītajā krājuma modeļa grupā. Šim procesam ir jānorāda rīcībā esošais krājums, kas jānovieto karantīnā, un karantīnas noliktava, kura jāizmanto. Lai palīdzētu plānot procesu, varat izmantot karantīnas pasūtījuma statusus.

## <a name="quarantine-order-statuses"></a>Karantīnas pasūtījumu statusi
Karantīnas pasūtījumiem var būt šāds statuss:

-   Izveidota
-   Uzsākts
-   Ziņots kā pabeigts
-   Pabeigts

### <a name="created"></a>Izveidota

Ja karantīnas pasūtījums ir izveidots manuāli, bet krājums vēl nav novietots karantīnas noliktavā, karantīnas pasūtījumam ir statuss **Izveidots**. Tiek ģenerētas divas krājumu transakcijas. Viena transakcija ir izejas plūsmas transakcija, kurai var būt statuss **Pasūtīts**, **Rezervēts fiziski** vai **Izdots**. Otrā transakcija ir ieejas plūsmas transakcija, kurai karantīnas noliktavā var būt statuss **Pasūtīts** vai **Reģistrēts**. Jūs varat rezervēt, izdot un reģistrēt krājumu atjauninājumus, izmantojot parastos procesus.

### <a name="started"></a>Uzsākts

Kad karantīnas pasūtījumam ir statuss **Sākts**, krājumi tiek pārsūtīti no parastās noliktavas uz karantīnas noliktavu, un tiek ģenerētas divas krājumu transakcijas. Vienai transakcijai ir statuss **Atskaitīts** un otrai transakcijai ir statuss **Saņemts**. Vienlaicīgi tiek arī izveidotas divas krājumu transakcijas, lai izpildītu atgriešanas pārsūtīšanu. Šīm transakcijām nav datuma. Vienai transakcijai ir statuss **Rezervēts fiziski** un otrai transakcijai ir statuss **Pasūtīts**.

### <a name="reported-as-finished"></a>Ziņots kā pabeigts

Noklikšķinot uz **Reģistrēt pabeigšanu**, sāktais karantīnas pasūtījums tiek reģistrēts kā pabeigts. Krājums tiek atbrīvots no karantīnas, bet vēl netiek pārvietots atpakaļ uz parasto noliktavu. Kustību atpakaļ uz parasto noliktavu var apstrādāt, izmantojot krājumu saņemšanas žurnālu, ko var inicializēt pabeigšanas reģistrēšanas laikā.

### <a name="ended"></a>Pabeigts

Kad karantīnas pasūtījums ir pabeigts, krājums tiek pārvietots no karantīnas noliktavas atpakaļ uz parasto noliktavu. Krājuma transakcijas statuss karantīnas noliktavā tiek iestatīts uz **Pārdots** un parastajā noliktavā — uz **Nopirkts**.

## <a name="quarantine-order-scrap"></a>Karantīnas pasūtījuma brāķis
Karantīnas pasūtījuma procesa ietvaros ir iespējams norakstīt krājumu. Apstrādājot brāķi, krājuma statuss tiks iestatīts kā **Pārdots**, izmantojot izdošanas transakciju no karantīnas noliktavas.

<a name="additional-resources"></a>Papildu resursi
--------

[Krājumu bloķēšana](inventory-blocking.md)

