---
title: Karantīnas pasūtījumi
description: Šajā rakstā ir aprakstīts, kā izmantot karantīnas pasūtījumus krājumu bloķēšanai.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e18735117d1f671e0efc0947248bbe266fa0ca6
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065605"
---
# <a name="quarantine-orders"></a>Karantīnas pasūtījumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izmantot karantīnas pasūtījumus krājumu bloķēšanai.

Karantīnas pasūtījumi ļauj bloķēt krājumus. Piemēram, varat noteikt krājumu karantīnu kvalitātes kontroles iemeslu dēļ. Krājumi, kam ir noteikta karantīna, tiek pārsūtīti uz karantīnas noliktavu.

> [!NOTE]
> Ja lietojat noliktavas vadības procesus (noliktavas vadības modulī), karantīnas pasūtījumu apstrāde tiek izmantota tikai atgriešanas pārdošanas pasūtījumiem.

## <a name="quarantine-on-hand-inventory-items"></a>Rīcībā esošo krājumu karantīna

Kad novietojat krājumus karantīnā, varat manuāli izveidot karantīnas pasūtījumus vai arī iestatīt, lai sistēma ienākošās apstrādes laikā tos izveidotu automātiski.

Lai iestatītu sistēmu automātiskai karantīnas pasūtījumu ģenerēšanai, sekojiet šiem darbībam.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Krājumi \> Krājumu modeļu grupas**.
1. Atlasiet atbilstošo modeļu grupu saraksta rūtī vai izveidojiet jaunu modeļu grupu.
1. Kopsavilkuma cilnē **Krājumu politikas** atzīmējiet izvēles rūtiņu **Karantīnas pārvaldība**.
1. Aizvērt lapu.
1. Jums jānorāda noklusējuma karantīnas noliktava laukā **Karantīnas noliktava** saņemošajām noliktavām.

Ja krājums, kas noliktavā reģistrēts kā saņemts, pieder modeļu grupai, kurai atzīmēta izvēles rūtiņa **Karantīnas pārvaldība**, sistēma tai ģenerē karantīnas pasūtījumu. Karantīnas pasūtījums liek darbiniekiem pārvietot krājumu uz karantīnas noliktavu.

Kad jūs manuāli izveidojat karantīnas pasūtījumus lapā **Karantīnas pasūtījumi**, krājumu nav nepieciešams iestatīt karantīnas pārraudzībai saistītajā krājuma modeļa grupā. Šim procesam ir jānorāda rīcībā esošais krājums, kas jānovieto karantīnā, un karantīnas noliktava, kura jāizmanto. Lai palīdzētu plānot procesu, varat izmantot karantīnas pasūtījuma statusus.

## <a name="quarantine-order-statuses"></a>Karantīnas pasūtījumu statusi

Karantīnas pasūtījumiem var būt šāds statuss:

- Izveidota
- Uzsākts
- Ziņots kā pabeigts
- Pabeigts

### <a name="created"></a>Izveidota

Ja karantīnas pasūtījums ir izveidots manuāli, bet krājums vēl nav novietots karantīnas noliktavā, karantīnas pasūtījumam ir statuss **Izveidots**. Tiek ģenerētas divas krājumu transakcijas. Viena transakcija ir izejas plūsmas transakcija, kurai var būt statuss **Pasūtīts**, **Rezervēts fiziski** vai **Izdots**. Otrā transakcija ir ieejas plūsmas transakcija, kurai karantīnas noliktavā var būt statuss **Pasūtīts** vai **Reģistrēts**. Jūs varat rezervēt, izdot un reģistrēt krājumu atjauninājumus, izmantojot parastos procesus.

### <a name="started"></a>Uzsākts

Kad karantīnas pasūtījumam ir statuss **Sākts**, krājumi tiek pārsūtīti no parastās noliktavas uz karantīnas noliktavu, un tiek ģenerētas divas krājumu transakcijas. Vienai transakcijai ir statuss **Atskaitīts** un otrai transakcijai ir statuss **Saņemts**. Vienlaicīgi tiek arī izveidotas divas krājumu transakcijas, lai izpildītu atgriešanas pārsūtīšanu. Šīm transakcijām nav datuma. Vienai transakcijai ir statuss **Rezervēts fiziski** un otrai transakcijai ir statuss **Pasūtīts**.

### <a name="reported-as-finished"></a>Ziņots kā pabeigts

Lai pabeigtu sākto karantīnas pasūtījumu, atveriet pasūtījumu un darbību rūtī atlasiet **Ziņot, ka ir pabeigts**. Krājums tiek atbrīvots no karantīnas, bet vēl netiek pārvietots atpakaļ uz parasto noliktavu. Kustību atpakaļ uz parasto noliktavu var apstrādāt, izmantojot krājumu saņemšanas žurnālu, ko var inicializēt pabeigšanas reģistrēšanas laikā.

### <a name="ended"></a>Beidzās

Kad karantīnas pasūtījums ir pabeigts, krājums tiek pārvietots no karantīnas noliktavas atpakaļ uz parasto noliktavu. Krājuma transakcijas statuss karantīnas noliktavā tiek iestatīts uz *Pārdots* un parastajā noliktavā — uz *Nopirkts*.

## <a name="quarantine-order-scrap"></a>Karantīnas pasūtījuma brāķis

Karantīnas pasūtījuma procesa ietvaros ir iespējams norakstīt krājumu. Apstrādājot brāķi, krājuma statuss ir iestatīts kā *Pārdots*, izmantojot izdošanas transakciju no karantīnas noliktavas.

## <a name="additional-resources"></a>Papildu resursi

- [Krājumu bloķēšana](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
