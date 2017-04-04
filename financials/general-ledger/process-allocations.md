---
title: "Sadalījumu apstrāde"
description: "Šajā rakstā ir sniegta informācija par piešķiršanas iespējas pārstrādei, tos Microsoft Dynamics 365 operācijām, un kā tos var izmantot budžeta plānošanā. Sadalījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām. Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 37f4df5d0b79208a8c565bc9101ddde193a6ef5b
ms.lasthandoff: 03/31/2017


---

# <a name="process-allocations"></a>Sadalījumu apstrāde

Šajā rakstā ir sniegta informācija par piešķiršanas iespējas pārstrādei, tos Microsoft Dynamics 365 operācijām, un kā tos var izmantot budžeta plānošanā. Sadalījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām. Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam.

Microsoft Dynamics 365 operāciju sniedz šādas iespējas atbalstīt šo procesu:

-   Manuāli piešķirt darījumu summas, izmantojot sadalīto darbību uzskaites sadali, vai, piemērojot finanšu dimensijai noklusējuma veidnes dokumentu. Lai iegūtu papildinformāciju, skatiet [uzskaites sadali.](\accounts-payable\accounting-distributions.md)
-   Automātiska transakcijas summu sadale, ņemot vērā atsevišķā galvenajā kontā definētos sadalījuma nosacījumus. Sadalījuma konta ieraksti tiek ģenerēti katram žurnālam, pamatojoties uz procentuālajām vērtībām un mērķa virsgrāmatas kontu, ikreiz, kad uzskaites ieraksts atbilst kritērijiem, kas norādīti kā avota virsgrāmatas konts.
-   Automātiska virsgrāmatas bilances vai fiksēto summu sadale, pamatojoties uz virsgrāmatas sadalījuma nosacījumiem. Virsgrāmatas sadalījuma nosacījumi tiek apstrādāti periodiski, izmantojot sadalījuma žurnālus. 

###  <a name="allocations-in-budget-planning"></a>Sadalījumi budžeta plānošanas stadijā

Virsgrāmatas sadalījuma nosacījumus var izmantot budžeta plānos. Budžeta plānošanā izmantojot virsgrāmatas sadalījuma nosacījumus, sadalījuma nosacījumi darbojas tāpat kā virsgrāmatā, taču avota dati un mērķa dati tiek saņemti no budžeta plāna. Varat manuāli atlasīt budžeta plāniem izmantojamos virsgrāmatas sadalījuma nosacījumus. Varat arī izmantot sadalījuma grafiku, kas darbojas kā daļa no darbplūsmas procesa.

> [!NOTE]
> Starpuzņēmuma virsgrāmatas sadalījuma nosacījumus nevar izmantot budžeta plānošanai.




