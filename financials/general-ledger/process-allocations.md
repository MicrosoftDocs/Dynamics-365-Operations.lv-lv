---
title: "Sadalījumu apstrāde"
description: "Šajā rakstā ir sniegta informācija par sadalījumiem, to apstrādes iespējām programmatūrā Microsoft Dynamics 365 for Operations un veidiem, kā tos var izmantot budžeta plānošanā. Sadalījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām. Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1cfaeab1562716aa4c91806b228f17625e25dfff
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="process-allocations"></a>Sadalījumu apstrāde

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par sadalījumiem, to apstrādes iespējām programmatūrā Microsoft Dynamics 365 for Operations un veidiem, kā tos var izmantot budžeta plānošanā. Sadalījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām. Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam.

Programmatūra Microsoft Dynamics 365 for Operations nodrošina tālāk norādītās iespējas šī procesa atbalstam.

-   Manuāla transakcijas summu sadale, izmantojot uzskaites sadales sadalīšanas darbību vai lietojot dokumentam finanšu dimensijas noklusējuma veidnes. Papildinformāciju skatiet tēmā [Uzskaites sadales.](../accounts-payable/accounting-distributions.md)
-   Automātiska transakcijas summu sadale, ņemot vērā atsevišķā galvenajā kontā definētos sadalījuma nosacījumus. Sadalījuma konta ieraksti tiek ģenerēti katram žurnālam, pamatojoties uz procentuālajām vērtībām un mērķa virsgrāmatas kontu, ikreiz, kad uzskaites ieraksts atbilst kritērijiem, kas norādīti kā avota virsgrāmatas konts.
-   Automātiska virsgrāmatas bilances vai fiksēto summu sadale, pamatojoties uz virsgrāmatas sadalījuma nosacījumiem. Virsgrāmatas sadalījuma nosacījumi tiek apstrādāti periodiski, izmantojot sadalījuma žurnālus. 

###  <a name="allocations-in-budget-planning"></a>Sadalījumi budžeta plānošanas stadijā

Virsgrāmatas sadalījuma nosacījumus var izmantot budžeta plānos. Budžeta plānošanā izmantojot virsgrāmatas sadalījuma nosacījumus, sadalījuma nosacījumi darbojas tāpat kā virsgrāmatā, taču avota dati un mērķa dati tiek saņemti no budžeta plāna. Varat manuāli atlasīt budžeta plāniem izmantojamos virsgrāmatas sadalījuma nosacījumus. Varat arī izmantot sadalījuma grafiku, kas darbojas kā daļa no darbplūsmas procesa.

> [!NOTE]
> Starpuzņēmuma virsgrāmatas sadalījuma nosacījumus nevar izmantot budžeta plānošanai.






