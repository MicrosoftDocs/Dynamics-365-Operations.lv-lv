---
title: Sagādes un avotu darbplūsmu problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar sagādes un avotu darbplūsmām.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: e8274890c581fffc7330538430c9b2ba060041bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999107"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Sagādes un avotu darbplūsmu problēmu novēršana

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar sagādes un avotu darbplūsmām.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Kļūda, atkārtoti iesniedzot pirkšanas pasūtījumu darbplūsmai pēc izmaiņu veikšanas: “Izmaiņas pirkšanas pasūtījumā X ir atļautas tikai Melnraksta stāvoklī, kad ir aktivizēta izmaiņu pārvaldība”

Šī problēma rodas tikai tad, ja pirkšanas pasūtījums bija stāvoklī *Apstiprināts*, pirms jūs pieprasījāt izmaiņas. Ja tiek pieprasītas izmaiņas, kamēr pirkšanas pasūtījums ir stāvoklī *Apstiprināts*, darbplūsma var tikt veiksmīgi apstrādāta.

### <a name="error-description"></a>Kļūdas apraksts

Kad pirkšanas pasūtījums tiek atkārtoti iesniegts pēc izmaiņu veikšanas, darbplūsmā rodas šāda kļūda:

> Apturēts (kļūda): X++ izņēmums: izmaiņas pirkšanas pasūtījumā PO0000569 ir atļautas tikai Melnraksta stāvoklī, ja tiek aktivizēta izmaiņu pārvaldība<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Problēmas risinājums

Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.

Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problēma tiks novērsta, izmantojot [šo Microsoft zināšanu bāzes (KB) rakstu](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Viena vai vairākas uzskaites sadales ir vai nu pārdalītas, vai nepilnīgi sadalītas.

Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.

Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Ja pirkšanas pasūtījumā, kurā ir ieslēgta izmaiņu pārvaldība, tiek atcelts nosūtīšanas atlikums, tad pirkšanas pasūtījums tiek nosūtīts uz statusu Apstiprināts.

### <a name="issue-description"></a>Problēmas apraksts

Pirkšanas pasūtījums, kas pakļauts izmaiņu pārvaldībai, ja vienīgā pieprasītā izmaiņa ir nosūtīšanas atlikuma atcelšana vienai vai vairākām rindām, tiks tieši pārsūtīts uz statusu *Apstiprināts*, kad tas tiks apstiprināts un žurnāls netiks izveidots.

### <a name="issue-resolution"></a>Problēmas risinājums

Nosūtīšanas atlikuma atcelšana neietekmē apstiprinājumu žurnāla saturu. Šī funkcionalitāte jāizmanto, kad rinda ir daļēji saņemta un atlikusī kvalitāte ir jāatceļ procesa posmā pēc tam, kad ar kreditoru ir apstiprināts pirkšanas pasūtījums.

Ja tas jāatspoguļo pirkšanas pasūtījuma apstiprinājumā, daudzums ir jākoriģē pirkšanas pasūtījuma rindā, lai apstiprinājums tiktu pieprasīts. Pretējā gadījumā, ja rindā nekas nav saņemts, daudzumu var noņemt. Šādā gadījumā būs nepieciešams atkārtots apstiprinājums.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Atceltie pirkšanas pasūtījumi tiek parādīti Pirkšanas pasūtījumu sagatavošanas darbvietas melnrakstu sarakstā.

### <a name="issue-description"></a>Problēmas apraksts

Atceļot pirkšanas pasūtījumus, ar statusu *Apstiprināts*, atceltie pirkšanas pasūtījumi joprojām parādās **Pirkšanas pasūtījumu sagatavošanas** darbvietas pirkšanas pasūtījumu melnrakstu sarakstā.

### <a name="issue-resolution"></a>Problēmas risinājums

Šī problēma rodas tikai tiem pirkšanas pasūtījumiem, kas ir pakļauti izmaiņu pārvaldībai. Tas notiek tāpēc, ka atcelšana tiek uzskatīta par izmaiņu, kas ir jāapstiprina. Apstiprinājumu sistēma var veikt automātiski. Atceltais pirkšanas pasūtījums ir jāiesniedz apstiprināšanas darbplūsmai, lai to varētu nosūtīt uz statusu *Apstiprināts*. Pēc tam pirkšanas pasūtījums vairs netiks rādīts **Pirkšanas pasūtījumu sagatavošanas** darbvietas pirkšanas pasūtījumu melnrakstu sarakstā.

