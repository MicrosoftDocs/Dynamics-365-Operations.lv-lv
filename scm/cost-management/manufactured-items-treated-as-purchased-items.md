---
title: "Iestatīs izstrādājumus, kas ražoti vai iepirkti"
description: "Produkti ir iespējami dažādi – var ražo (ražo) vai sagādātas (nopirkto). Šajā rakstā ir aprakstīti daži raksturīgākie jautājumi, kas jāņem vērā, konfigurējot preces vairāku ieguves veidu atbalstam."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5360c7b1475763b8e33205bff560393e9ee51882
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-products-that-can-be-produced-or-procured"></a>Iestatīs izstrādājumus, kas ražoti vai iepirkti

Produkti ir iespējami dažādi – var ražo (ražo) vai sagādātas (nopirkto). Šajā rakstā ir aprakstīti daži raksturīgākie jautājumi, kas jāņem vērā, konfigurējot preces vairāku ieguves veidu atbalstam. 

Vairāku resursu plānošanu parasti izmanto iegādātam krājumam, kas laiku pa laikam tiek saražots, vai krājumam, kas galvenokārt bija saražotais krājums, bet mainīts tā, lai tas tagad galvenokārt būtu iegādājams krājums. Vispirms krājums tiks veidots, kā saražotais krājums, lai definētu materiālu komplektu (MK), maršruta informāciju, kā arī lai atbalstītu krājuma ražojuma pasūtījumus. Ražošanas tipam jābūt iestatītam uz **MK** (vai ražošanas procesam uz **Formula** vai **Līdzprodukts**).

Izmantojot standarta izmaksas, ražotajam krājumam var aprēķināt krājuma izmaksu ierakstu. Tomēr krājumu izmaksu ieraksts var neatbilst tām standarta izmaksām, kas paredzētas iegādes nolūkiem. Šādā gadījumā standarta izmaksas manuāli jāievada un jāaktivizē krājumu izmaksu ierakstam. Izmaksu aprēķināšanai izmantojiet īpašu MK un maršrutu, kas attiecas uz preču piegādes komplekta finanšu periodu, lai samazinātu novirzes laika gaitā. Turklāt vienā vietā saražoto krājumu var pārsūtīt uz citu vietu. Tāpēc krājuma izmaksas manuāli jāievada un jāaktivizē tai vietai, uz kuru pārsūtīts krājums. Izmantojot saražoto krājumu kā sastāvdaļu augstāka līmeņa produktos, sastāvdaļas izmaksas ir jāuzskata par iepirkto krājumu. Šīs vadlīnijas stājas spēkā neatkarīgi no tā, vai sastāvdaļas izmaksas tika aprēķinātas vai manuāli ievadītas. Citiem vārdiem sakot, MK aprēķinam jāapstrādā krājuma izmaksas kā iegādājamā sastāvdaļa, nevis izmantot krājuma MK un maršrutēšanas informāciju izmaksu aprēķināšanai. Lai izvairītos no šī aprēķina, atlasiet karodziņu **Pārtraukt izvēršanu**, kas iegults MK aprēķinu grupā, kas piešķirta krājumam. Lai novērstu vispārējās plānošanas aprēķinus no izvēršanas prasībām, izmantojot krājumu, iestatiet izvēršanas periodu uz 0 (nulle) dienām krājuma vajadzībām vai seguma grupai. Vispārējās plānošanas aprēķins pēc tam apstrādās krājumu kā iegādāto krājumu, un neveiks papildu aprēķinus krājuma MK un maršruta informācijai.




