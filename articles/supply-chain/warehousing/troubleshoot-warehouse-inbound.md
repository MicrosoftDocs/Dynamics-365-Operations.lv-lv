---
title: Ienākošo noliktavas operāciju problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavas ienākošajām noliktavas operācijām programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645976"
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

Jauna ienākošo kravu apstrādes funkcija *Pārsniedzot kravas daudzumu* izlabo šo problēmu. Lai ieslēgtu šo funkciju, dodieties uz [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet tālāk norādītos līdzekļus (minētajā secībā):

1. Saistīt pirkšanas pasūtījuma krājumu transakcijas ar kravu
1. Noslodzes daudzumu pārmērīga saņemšana

Lai iegūtu papildu informāciju, skatiet [Reģistrēto preču daudzumu grāmatošana uz pirkšanas pasūtījumiem](inbound-load-handling.md#post-registered-quantities).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]