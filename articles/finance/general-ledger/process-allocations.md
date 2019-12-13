---
title: Sadalījumu apstrāde
description: Šajā rakstā ir sniegta informācija par sadalījumiem, to apstrādes iespējām programmā Microsoft Dynamics 365 Finance un to, kā tos var izmantot budžeta plānošanā. Sadalījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām. Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32271e967da2e7f3702b0c6c2dcdba460aa1b382
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770624"
---
# <a name="process-allocations"></a>Sadalījumu apstrādāšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par sadalījumiem, to apstrādes iespējām un to, kā tos var izmantot budžeta plānošanā. Sadalījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām. Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam.

Tālāk norādītās iespējas atbalsta šo procesu.

-   Manuāla transakcijas summu sadale, izmantojot uzskaites sadales sadalīšanas darbību vai lietojot dokumentam finanšu dimensijas noklusējuma veidnes. Papildinformāciju skatiet tēmā [Uzskaites sadales.](../accounts-payable/accounting-distributions.md).
-   Automātiska transakcijas summu sadale, ņemot vērā atsevišķā galvenajā kontā definētos sadalījuma nosacījumus. Sadalījuma konta ieraksti tiek ģenerēti katram žurnālam, pamatojoties uz procentuālajām vērtībām un mērķa virsgrāmatas kontu, ikreiz, kad uzskaites ieraksts atbilst kritērijiem, kas norādīti kā avota virsgrāmatas konts.
-   Automātiska virsgrāmatas bilances vai fiksēto summu sadale, pamatojoties uz virsgrāmatas sadalījuma nosacījumiem. Virsgrāmatas sadalījuma nosacījumi tiek apstrādāti periodiski, izmantojot sadalījuma žurnālus. 

###  <a name="allocations-in-budget-planning"></a>Sadalījumi budžeta plānošanas stadijā

Virsgrāmatas sadalījuma nosacījumus var izmantot budžeta plānos. Budžeta plānošanā izmantojot virsgrāmatas sadalījuma nosacījumus, sadalījuma nosacījumi darbojas tāpat kā virsgrāmatā, taču avota dati un mērķa dati tiek saņemti no budžeta plāna. Varat manuāli atlasīt budžeta plāniem izmantojamos virsgrāmatas sadalījuma nosacījumus. Varat arī izmantot sadalījuma grafiku, kas darbojas kā daļa no darbplūsmas procesa.

> [!NOTE]
> Starpuzņēmuma virsgrāmatas sadalījuma nosacījumus nevar izmantot budžeta plānošanai.





