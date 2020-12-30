---
title: Budžeta plānošanas attaisnojuma dokumenti
description: Attaisnojuma dokumenti sniedz skaidrojumu tiem, kas budžetam pieprasa paskaidrot, kādēļ ir nepieciešams kāds noteikts budžets.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 321da6643b421070ddd9f32bddd3e8d72f0adb86
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445713"
---
# <a name="budget-planning-justification-documents"></a>Budžeta plānošanas attaisnojuma dokumenti

[!include [banner](../includes/banner.md)]

Attaisnojuma dokumenti sniedz skaidrojumu tiem, kas budžetam pieprasa paskaidrot, kādēļ ir nepieciešams kāds noteikts budžets. 

Budžeta pārvaldnieks izveido budžeta plāna veidni programmā Microsoft Word, un tā tiek piešķirta pašreizējam budžeta plānošanas procesam. Pēc tam budžeta īpašnieki šo veidni var atvērt un likt datus automātiski aizpildīt programmā Word, pamatojoties uz to budžeta pieprasījumu. Pēc tam viņi var pievienot papildu tekstu vai datus, pirms savu personalizēto attaisnojuma dokumentu saglabā un pievieno budžeta plānam.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Dynamics Office pievienojumprogrammas iestatīšana programmai Microsoft Word

1.  Atveriet jaunu Microsoft Word dokumentu.
2.  Lentē noklikšķiniet uz **Ievietot** un noklikšķiniet uz **Veikals**.
3.  Meklējiet Microsoft Dynamics Office pievienojumprogrammu un noklikšķiniet uz **Pievienot**.
4.  Programmā Word, labajā rūtī noklikšķiniet uz **Pievienot servera informāciju**.
5.  Ierakstiet vai ielīmējiet servera vietrādi URL un noklikšķiniet uz **Labi**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Līdzināšanas veidnes definēšana programmā Microsoft Word

1.  Pēc pierakstīšanās Microsoft Dynamics Office pievienojumprogrammā noklikšķiniet uz **Dizains**.
2.  Galvenes informācijai izmantojiet pogu **Pievienot laukus**.
3.  Atlasiet BudgetPlanJustification elementa datu avotu un noklikšķiniet uz **Tālāk**. **Piezīme.** Šis elements ir nepieciešams visiem attaisnojuma dokumentiem. Var izmantot citus elementus, taču, ja nav ietverts šis elements, neizdodas augšupielāde atpakaļ programmā Microsoft Dynamics 365 Finance.
4.  Word dokumentā pievienojiet etiķetes un vērtības BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter un DocumentNumber. **Piezīme.** Ja nepieciešams, varat izmantot pats savas pielāgotās etiķetes, nevis standarta etiķetes.
5.  Lai pabeigtu galvenes atlasi, noklikšķiniet uz **Gatavs**.
6.  Rindas līmeņa informācijai par budžeta plāna summām noklikšķiniet uz **Pievienot tabulu**.
7.  Atkal atlasiet BudgetPlanJustification elementa datu avotu un noklikšķiniet uz **Tālāk**.
8.  Pievienojiet laukus vērtībām EffectiveDate, ScenarioName, AccountDisplayValue un AccountingCurrencyExpenseAmount. **Piezīme.** Ja atsevišķās budžeta plāna rindās pievienošanai ir pieejami komentāri, šeit tos varat pievienot tabulai.
9.  Pievienojiet visus papildu norādījumus, ko sniegt lietotājam, un veiciet dokumentam visu nepieciešamo formatēšanu vai stila mainīšanu.
10. Saglabājiet dokumentu lokālajā datorā un aizveriet failu, pirms turpināt.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Iestatīt budžeta plānošanas procesu attaisnojuma veidnes lietošanai

1.  Pārejiet uz sadaļu **Budžeta veidošana** &gt; **Iestatīšana** &gt; **Budžeta plānošana** &gt; **Attaisnojuma dokumenta veidnes**.
2.  Noklikšķiniet uz **Jauns** un pārlūkojiet līdz jaunizveidotajam Microsoft Word dokumentam.
3.  Ievadiet veidnes parādāmo nosaukumu un aprakstu. Noklikšķiniet uz **Labi**.
4.  Dodieties uz **Budžeta veidošana** &gt; **Iestatīšana** &gt; **Budžeta** **plānošana** &gt; **Budžeta plānošanas process**.
5.  Atlasiet procesu, kurā ir jālieto attaisnojuma veidne, un noklikšķiniet uz **Rediģēt**.
6.  Laukā **Attaisnojuma dokumenta veidne** atlasiet atbilstošo veidni un saglabājiet.

##### <a name="edit-and-save-personalized-justification-documents"></a>Rediģēt un saglabāt personalizētus attaisnojuma dokumentus

1.  Izveidot jaunu budžeta plānu vai atveriet esošu budžeta plānu.
2.  Nolaižamajā izvēlnē **Attaisnojums** atlasiet vienumu **Izveidot jaunu attaisnojumu**.
3.  Pēc informācijas aizpildīšanas izvēlieties augšupielādēt personalizēto dokumentu no nolaižamās izvēlnes **Attaisnojums**.




