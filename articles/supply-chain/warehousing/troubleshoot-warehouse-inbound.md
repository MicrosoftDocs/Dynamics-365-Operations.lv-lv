---
title: Ienākošo noliktavas operāciju problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas ienākošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920991"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Ienākošo noliktavas operāciju problēmu novēršana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas ienākošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Tiek parādīts šāds kļūdas ziņojums: "Kvalitātes pasūtījums %1 ir ģenerēts. Klastera profilu nevarēja atrast, lūdzu, pārbaudiet savu konfigurāciju."

### <a name="issue-description"></a>Problēmas apraksts

Šis kļūdas ziņojums ir saistīts ar saņemšanas procesu, kurā ir ieslēgta kvalitātes pārvaldība (QMS). Atkarībā no konfigurācijas jūsu vidē papildu detaļas par transakciju, kas ģenerē kļūdas ziņojumu, var palīdzēt novērst šo problēmu.

### <a name="issue-resolution"></a>Problēmas risinājums

Vispirms pārskatiet [klastera izdošanas](set-up-cluster-picking.md) iestatījumu un pārliecinieties, ka klasteru profili ir pareizi iestatīti. Klastera izdošanai nevar izmantot mobilās ierīces izvēlnes vienumu, ja vien nav iestatīti klasteru profili. Atkarībā no jūsu vides, iespējams, būs jāpārskata arī citas saistītās konfigurācijas.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Jauktā numura zīmes saņemšana nestrādā nevienam izvietojuma kodam, izņemot Kredītu.

### <a name="issue-description"></a>Problēmas apraksts

Kad **Darbības** lauks izvietojuma kodam ir iestatīts kā *Kredīts* vai *Brāķis*, varat izmantot tikai [Jaukto numura zīmes saņemšanas](mixed-license-plate-receiving.md) izvēlnes elementu, lai apstrādātu atgrieztos krājumus.

### <a name="issue-resolution"></a>Problēmas risinājums

Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums. Pašlaik tikai [izvietojuma kodi](../service-management/set-up-disposition-codes.md), kuros **Darbības** lauks ir iestatīts kā *Kredīts* vai *Brāķis*, tiek atbalstīts jauktai numura zīmes saņemšanai.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Palaižot atjaunināt produktu ieejas plūsmas periodisko uzdevumu, neapstiprinātie pirkšanas pasūtījumi tiek apstiprināti.

### <a name="issue-description"></a>Problēmas apraksts

Pēc tam, kad esat palaidis *Atjaunināt preču ieejas plūsmu* periodisko uzdevumu, sistēma automātiski apstiprina neapstiprinātos pirkšanas pasūtījumus, kuriem ir krājuma darbības statuss *Reģistrēts*.

### <a name="issue-resolution"></a>Problēmas risinājums

Jauna ienākošo kravu apstrādes funkcija *Pārsniedzot kravas daudzumu* izlabo šo problēmu. Lai ieslēgtu šo funkciju, dodieties uz darbvietu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet tālāk norādītos līdzekļus (minētajā secībā):

1. Saistīt pirkšanas pasūtījuma krājumu transakcijas ar kravu
1. Noslodzes daudzumu pārmērīga saņemšana

Lai iegūtu papildu informāciju, skatiet [Reģistrēto preču daudzumu grāmatošana uz pirkšanas pasūtījumiem](inbound-load-handling.md#post-registered-quantities).

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Kad reģistrēju ienākošos pasūtījumus, es saņemu šādu kļūdas ziņojumu: "Daudzums nav derīgs."

### <a name="issue-description"></a>Problēmas apraksts

Ja **Numura zīmes grupēšanas politikas** lauks ir iestatīts uz *Lietotājs, kas ir definēts* mobilās ierīces izvēlnes elementam, kas tiek izmantots ienākošo pasūtījumu reģistrēšanai, saņemat kļūdas ziņojumu ("Daudzums nav derīgs"), un reģistrāciju nevar pabeigt.

### <a name="issue-cause"></a>Izsniegšanas iemesls

Ja *Lietotājs, kas ir definēts* tiek izmantots kā numura zīmi grupēšanas politika, sistēma ienākošos krājumus sadala atsevišķās numura vienībai, kā norādīts vienību secību grupā. Ja partijas vai sērijas numuri tiek izmantoti saņemtā krājuma izsekošanai, katras partijas vai sērijas daudzumi ir jānorāda uz reģistrēto numura zīmi. Ja numura zīmei norādītais daudzums pārsniedz daudzumu, kas joprojām ir jāsaņem saskaņā ar pašreizējām dimensijām, saņemat kļūdas ziņojumu.

### <a name="issue-resolution"></a>Problēmas risinājums

Kad reģistrējiet krājumu, izmantojot mobilās ierīces izvēlnes vienumu, kura **Numura zīmi grupēšanas politikas** lauks ir iestatīts uz *Lietotājs, kas ir definēts*, sistēmai var būt nepieciešams apstiprināt vai ievadīt numura zīmi numurus, partijas numurus vai sērijas numurus.

Numura zīmes apstiprināšanas lapā sistēma parādīs daudzumu, kas ir piešķirts pašreizējai numura zīmei. Partijas vai sērijas apstiprinājuma lapās sistēma rādīs daudzumu, kas ir jāsaņem pašreizējā numura zīmi. Šeit tiks iekļauts arī lauks, kur varat ievadīt daudzumu, ko reģistrēt numura zīmes un paketes vai sērijas numura kombinācijai. Šajā gadījumā pārliecinieties, ka numura zīmei reģistrētais daudzums nepārsniedz daudzumu, kas joprojām ir jāsaņem.

Ja saņemšanas pasūtījuma reģistrācijā tiek ģenerēts pārāk daudz numura zīmju, **Numura zīmes grupēšanas politikas** lauka vērtību var mainīt uz *Numura zīmes grupēšanu*, krājumam var piešķirt jaunu vienību secību grupu vai vienību secību grupas opciju **Numura zīmju grupai** var deaktivizēt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
