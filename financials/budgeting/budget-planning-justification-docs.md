---
title: "Budžeta plānošanas pamatojuma dokumenti"
description: "Attaisnojuma dokumenti sniedz stāstījuma tiem lūdz paskaidrot, kāpēc ir nepieciešams noteikts budžets budžets."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Budžeta plānošanas pamatojuma dokumenti

Attaisnojuma dokumenti sniedz stāstījuma tiem lūdz paskaidrot, kāpēc ir nepieciešams noteikts budžets budžets. 

Budžeta plāna veidne ir budžeta manager programmā Microsoft Word izveidojis un piešķirts kārtējā budžeta plānošanas procesā. Budžeta īpašnieki var pēc tam atvērt veidni un ir datus programmā Word aizpildīts automātiski, pamatojoties uz savu budžeta pieprasījumu. Viņi pēc tam var pievienot papildu tekstu vai datus pirms saglabāšanas un savu personalizēto attaisnojuma dokumentu pievienošanu to budžeta plānu.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Iestatīt Microsoft Dynamics Office pievienojumprogramma programmai Microsoft Word

1.  Atveriet jaunu Microsoft Word dokumentu.
2.  Noklikšķiniet uz **ievietot** lentes un noklikšķiniet uz **Store**.
3.  Meklēt Microsoft Dynamics Office pievienojumprogrammu un noklikšķiniet **pievienot**.
4.  Programmā Word, labajā rūtī noklikšķiniet uz **pievienot servera informāciju**.
5.  Ierakstiet vai ielīmējiet servera URL un noklikšķiniet uz **labi**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definēt pamatojumu veidni programmā Microsoft Word

1.  Noklikšķiniet uz **Design** pievienojumprogrammu Microsoft Dynamics Office pēc tam, kad esat pieteicies.
2.  Galvenes informāciju, izmantot **pievienot laukus** pogu.
3.  Atlasiet vienību datu avotu BudgetPlanJustification un uz **nākamo**. **Piezīme:** šai entītijai ir nepieciešama jebkāda pamatojuma dokumentu. Var izmantot citas personas, bet augšupielādēt atpakaļ uz Microsoft Dynamics 365 operācijām cietīs neveiksmi, ja šis uzņēmums nav iekļauts.
4.  BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter un DocumentNumber etiķetes un vērtības pievienošana Word dokumentā. **Piezīme:** var izmantot pielāgotas uzlīmes, nevis uz standarta etiķetēm, ja nepieciešams.
5.  Noklikšķiniet uz **darīts** pabeigt galvenes sekcijas.
6.  Līniju līmeņa daļām no budžeta plāna summas, noklikšķiniet **pievienot tabulu**.
7.  Vēlreiz, atlasiet entītijas datu avotu BudgetPlanJustification un uz **nākamo**.
8.  Pievienojiet laukus, EffectiveDate, ScenarioName, AccountDisplayValue un AccountingCurrencyExpenseAmount. **Piezīme:** ja komentāri ir pieejami, lai pievienotu atsevišķu budžeta plāna rindas ietvaros, tiem var pievienot tabulu šeit.
9.  Pievienot jebkuru papildu norādījumi, kas nodrošina galalietotājam un veiktu nepieciešamo formatējumu vai ieveidošanas dokumentam.
10. Lokālajā datorā, saglabājiet dokumentu un aizveriet failu pirms turpināt.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Iestatīt budžeta plānošanas procesā izmantot pamatojumu template

1.  Microsoft Dynamics 365 operācijām, lai nokļūtu **budžeta līdzekļu**&gt;**Setup**&gt;**budžeta plānošanu**&gt;**attaisnojuma dokumentu veidnes**.
2.  Noklikšķiniet uz **New** un pārlūkot jūsu jaunizveidoto Microsoft Word dokumentam.
3.  Ievadiet veidnes displeja nosaukumu un aprakstu. Click **OK**.
4.  Dodieties uz **budžeta līdzekļu**&gt;**Setup**&gt;**budžeta****plānošanas**&gt;**budžeta plānošanas procesā**.
5.  Procesā, kur pamatojums veidne jāizmanto, un noklikšķiniet uz atlasīt **rediģēt**.
6.  Šajā **attaisnojuma dokumenta veidne** lauku, atlasiet atbilstošo veidni un saglabājiet.

##### <a name="edit-and-save-personalized-justification-documents"></a>Rediģēt un saglabāt dokumentus, personalizētu pamatojums

1.  Dynamics 365 operācijām, izveidot jaunu budžeta plānu vai atvērt esošo budžeta plānu.
2.  Šajā **pamatojums** nolaižamajā izvēlnē atlasiet **izveidot jaunu pamatojumu**.
3.  Pēc piepildīšanas detaļas, izvēlieties augšupielādēt personalizēto dokumentu no **pamatojums** nolaižamo izvēlni.



