---
title: Kļūda, atkārtoti iesniedzot pirkšanas pasūtījumu darbplūsmai pēc izmaiņu izpildes
description: Kļūda, atkārtoti iesniedzot pirkšanas pasūtījumu darbplūsmai pēc izmaiņu izpildes
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477031"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Kļūda, atkārtoti iesniedzot pirkšanas pasūtījumu darbplūsmai pēc izmaiņu izpildes


## <a name="symptoms"></a>Simptomi

Kad pirkšanas pasūtījums tiek atkārtoti iesniegts pēc izmaiņu veikšanas, darbplūsmā rodas šāda kļūda:

> Apturēts (kļūda): X++ izņēmums: izmaiņas pirkšanas pasūtījumā PO0000569 ir atļautas tikai Melnraksta stāvoklī, ja tiek aktivizēta izmaiņu pārvaldība<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Šī problēma rodas tikai tad, ja pirkšanas pasūtījums bija stāvoklī *Apstiprināts*, pirms jūs pieprasījāt izmaiņas. Ja tiek pieprasītas izmaiņas, kamēr pirkšanas pasūtījums ir stāvoklī *Apstiprināts*, darbplūsma var tikt veiksmīgi apstrādāta.

## <a name="resolution"></a>Novēršana

Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.

Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problēma tiks novērsta, izmantojot [šo Microsoft zināšanu bāzes (KB) rakstu](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).
