---
title: Noliktavas programmas notikumi
description: Šajā rakstā ir aprakstīta noliktavas programmas notikumu apstrāde, kas tiek izmantota noliktavas programmas notikumu ziņojumu apstrādei kā daļa no pakešuzdevuma.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 41b9538d3064bad24c4c5c60d401605e47e9c655
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905459"
---
# <a name="warehouse-app-event-processing"></a>Noliktavas lietojumprogrammas notikumu apstrāde

[!include [banner](../includes/banner.md)]

Pakešuzdevumi, kas tiek izpildīti Supply Chain Management, var izmantot datus no noliktavas programmas izsniegtās notikumu apstrādes rindas, lai atbilstoši reaģētu uz signalizētajiem notikumiem. Šis līdzeklis rindai pievieno svarīgus notikumus, atbildot uz noteiktiem darbību veidiem, ko veikuši darbinieki, izmantojot programmu. Piemēram, izmantojot līdzekli *Izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas*, pārsūtīšanas pasūtījuma virsraksts un rindas tiek izveidotas un atjauninātas aizmugursistēmā, kad sistēma palaiž pakešuzdevumu **Apstrādāt noliktavas programmas notikumus**.

## <a name="turn-the-process-warehouse-app-events-feature-on-or-off"></a>Ieslēgt vai izslēgt līdzekli Apstrādāt noliktavas programmas notikumus

No Piegādes ķēdes pārvaldības versijas 10.0.25 šī funkcija ir ieslēgta pēc noklusējuma. Administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot *apstrādes noliktavas programmas notikumu* līdzekli līdzekļu [pārvaldības darbvietā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

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

Varat skatīt notikumu rindu un notikumu ziņojumus, ko ģenerējusi Warehouse Management mobile programma, dodoties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Mobilās ierīces žurnāli \> Noliktavas programmas notikumi**.

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