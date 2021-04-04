---
title: Noliktavas programmas notikumi
description: Šajā tēmā aprakstīta noliktavas programmas notikumu apstrāde, ko izmanto, lai apstrādātu noliktavas programmas notikumu ziņojumus kā daļu no pakešuzdevuma.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0bafcbd5306860cb80d6e813aabf83853a9011c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248647"
---
# <a name="warehouse-app-event-processing"></a>Noliktavas lietojumprogrammas notikumu apstrāde

[!include [banner](../includes/banner.md)]

Pakešuzdevumi, kas tiek izpildīti Supply Chain Management, var izmantot datus no noliktavas programmas izsniegtās notikumu apstrādes rindas, lai atbilstoši reaģētu uz signalizētajiem notikumiem. Šis līdzeklis rindai pievieno svarīgus notikumus, atbildot uz noteiktiem darbību veidiem, ko veikuši darbinieki, izmantojot programmu. Piemēram, izmantojot līdzekli **Izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas**, pārsūtīšanas pasūtījuma virsraksts un rindas tiek izveidotas un atjauninātas aizmugursistēmā, kad sistēma palaiž pakešuzdevumu **Apstrādāt noliktavas programmas notikumus**.

## <a name="enable-the-process-warehouse-app-events-feature"></a>Iespējot līdzekli Apstrādāt noliktavas programmas notikumus

Lai varētu izmantot šo līdzekli, tam vispirms jābūt iespējotam sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lapu, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības. Līdzeklis Apstrādāt noliktavas programmas notikumus ir norādīts kā:

- **Modulis** — Noliktavas vadība
- **Līdzekļa nosaukums** — Apstrādāt noliktavas programmas notikumus

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Iestatiet pakešuzdevumu, lai apstrādātu noliktavas programmas notikumus

### <a name="process-warehouse-app-events"></a>Apstrādāt noliktavas programmas notikumus

Iestatiet ieplānotu pakešuzdevumu, lai apstrādātu noliktavas programmas notikumus pārsūtīšanas pasūtījumu izveidošanai un rindu atjauninājumiem.

1. Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Apstrādāt noliktavas programmas notikumus**.
1. Tiek atvērts dialoglodziņš Apstrādāt noliktavas programmas notikumus. Izvērsiet kopsavilkuma cilni **Palaist fonā** un iestatiet **Pakešapstrāde** uz **Jā**.
1. Kopsavilkuma cilnē **Palaist fonā** atlasiet **Periodiskums**.
1. Atveras dialoglodziņš **Definēt periodiskumu**. Iestatiet izpildes grafiku, kas nepieciešams jūsu biznesam.
1. Atlasiet **Labi** lai atgrieztos pie dialoglodziņa **Apstrādāt noliktavas programmas notikumus**.
1. Lai pievienotu pakešuzdevumu pakešuzdevumu rindai, atlasiet **Labi** dialoglodziņā **Apstrādāt noliktavas programmas notikumus**.

## <a name="query-warehouse-app-events"></a>Vaicājumu noliktavas programmas notikumi

Varat skatīt notikumu rindu un notikumu ziņojumus, ko ģenerējusi noliktavas programma, dodoties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Mobilās ierīces žurnāli \> Noliktavas programmas notikumi**.

## <a name="the-standard-event-queue-process"></a>Standarta notikumu rindas process

Noliktavas programmas notikumu rinda parasti tiek izmantota ar sekojošo aprakstīto plūsmu:

1. Notikums tiek pievienots rindai ar notikuma ziņojumu. Jaunajam ziņojumam sākotnēji ir notikuma stāvoklis **Gaidīšana**, kas nozīmē, ka pakešuzdevums **Apstrādāt noliktavas programmas notikumus** neturpināsies un neapstrādās ziņojumu.
1. Tiklīdz ziņojuma stāvoklis tiek atjaunināts uz **Ievietots rindā**, pakešuzdevums **Apstrādāt noliktavas programmas** notikumus turpināsies un apstrādās notikumu.
1. Pakešuzdevums atjaunina notikuma stāvokļus uz vai nu **Pabeigts** vai **Nesekmīgs**, atkarībā no tā, vai pieprasītais process bija iespējams.
1. Kad visu saistīto notikuma ziņojumu statuss ir **Pabeigts**, notikums tiek dzēsts no rindas.

 Detalizētu piemēru skatiet šeit: [Pārsūtīšanas pasūtījuma izveide no noliktavas programmas procesa](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Notikumu kļūdu apstrāde

Kā daļu no noliktavas notikumu apstrādes, pieprasītā ziņojuma aktivitāte nevar saņemt procesus no pakešuzdevuma. Šādā gadījumā notikuma ziņojums mainīsies uz **Nesekmīgs**. Varat izmantot informāciju no **Pakešuzdevumu žurnāla**, lai uzzinātu iemeslu un veiktu nepieciešamās darbības, lai labotu problēmas.

Detalizētu piemēru skatiet šeit: [Pārsūtīšanas pasūtījuma izveide no noliktavas programmas](create-transfer-order-from-warehouse-app.md).

Lai atiestatītu nesekmīgu noliktavas programmas notikuma ziņojumu:

1. Doties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Mobilās ierīces žurnāli \> Noliktavas programmas notikumi**.
1. Kopsavilkuma cilnē **Noliktavas programmas notikumu ziņojumi** atrodiet un atlasiet atbilstošu notikumu, kam parādīts statuss **Nesekmīgs** kolonnā **Notikuma stāvoklis**.
1. Atlasiet **Atiestatīt** rīkjoslā **Noliktavas programmas notikumu ziņojumi**.
1. Turpiniet darbu, līdz visi atbilstošie ziņojumi ir atiestatīti.

Varat arī noņemt notikuma ziņojumu **Nesekmīgs**, izmantojot opciju **Dzēst** rīkjoslā **Noliktavas programmas notikumu ziņojumi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]