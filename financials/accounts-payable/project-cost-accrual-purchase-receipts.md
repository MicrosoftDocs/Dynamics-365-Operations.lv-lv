---
title: "Projekta izmaksu uzkrāšanas uz iepirkuma p/z"
description: "Šajā tēmā ir aprakstīts, kā uzkrātos projekta izmaksām no pirkšanas kvītis var izsekot Microsoft Dynamics 365 operācijām."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Projekta izmaksu uzkrāšanas uz iepirkuma p/z

Šajā tēmā ir aprakstīts, kā uzkrātos projekta izmaksām no pirkšanas kvītis var izsekot Microsoft Dynamics 365 operācijām. 

Rēķinu projektam bieži pienāk vēlāk nekā preces un pakalpojumi tiek sniegti, kas varētu būt nozīmīga ietekme uz projekta veiktspējas pamatrādītāji (KPI). Tas ir svarīgi, lai būtu iespējams izsekot šos darījumus, gan finanšu un projektu atskaites.

Tas ilustrē piemērs scenārijā. 

Contoso Consulting ir sākusi jaunu mākonis izvietošanas projektu. Iegādāties datoru projektam tiek izveidots pirkšanas pasūtījums. Dators maksās $1500 un instalācijas pakalpojumi maksās $150. Piegādātājam ir piegādāts un instalēta datorā, bet rēķins vēl nav sasniegusi Contoso Consulting. Projekta vadītājs gribētu redzēt projekta izmaksu uzkrāšanas $1650 pirms rēķins tiek piegādāts. Šīs izmaksas būtu jāatspoguļo arī uzņēmuma mēneša beigu finanšu pārskatus. 

Uzkrātās izmaksas ir jāreģistrē finanšu līmeni, gan projektu līmenī ziņošanas nolūkiem. Dynamics 365 operācijām, finansiāli atjauninot produkta saņemšanas var izsekot, krājumu un iepirkumu kategorijām. 

Krājumiem, par **debitoru kreditoru parametrus** lapu, atlasiet **pēc produkta saņemšanas Virsgrāmatas** variants.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Iepirkuma kategorijām, par **kategorijas politikas kārtula** lapu, atlasiet **pirktspēju** politiku, un pēc tam atlasiet **uzkrāšanas iepirkuma rēķina saņemšanas** katrai iepirkuma kategorijai.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

**Pirkšanas izdevumi ANO rēķinos** un **pirkšanas uzkrāšanas** kontiem, **kontējumu uzstādījumi** tiek izmantots, grāmatojot dokumentus, kas saistīti ar preču saņemšanu.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Izmantojot šo pašu scenāriju, let's redzēt, kā grāmatošanas produkta saņemšanas ietekmēs Virsgrāmatu un projekta informāciju. 

**1. solis:** izveidot un apstiprināt jaunu pirkšanas pasūtījumu projekta ierakstīt $150 $1500 un uzstādīšanas pakalpojumus datoru iegādei.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Kad pirkšanas pasūtījums ir apstiprināts, projekta darbības fiksētās izmaksas tiek veidotas. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Fiksēto izmaksu darbības būs **darbības izcelsme** lauku iestatīt **pirkšanas pasūtījuma**. Veidojot un apstiprinot pirkšanas pasūtījums netiek izveidots projekta darbības. 

**2. solis:** saņemt piegādāto preču un pakalpojumu un produktu saņemšanas ir reģistrēts. 

Grāmatošanas produkta saņemšanu radīs un grāmatotu Virsgrāmatas dokumenta. Dokumentu pirkuma izdevumi, rēķinos un konta debeta un kredīta pirkšanu uzkrāšanas konts. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Grāmatošanas produkta saņemšanas izmantos grāmatošanas iestatījumā iepirkumu kategorijas un produkti, kas nav projekta kategorijas grāmatošanas iestatījumā. Lai pareizi atspoguļotu finansiālo ietekmi pirkšanas uzkrājumus, šai uzstādīšanas programmai nepieciešams jāsaskaņo. 

Var kartēt uz iepirkumu kategorijas projektu kategorijām **iepirkuma kategorija** lapā.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**3. solis:** izveidot projektu kreditora rēķinu. 

Programmā Dynamics 365 operācijām, grāmatojot preču saņemšanu neietekmē projekta informāciju. Tieši pēc tam, kad iepirkuma p/z grāmatošanas, kā profilakse, varētu radīt projektu kreditora rēķinu. Dodieties uz **pirkšanas pasūtījuma** lapas &gt;**rēķinu cilnē**&gt;**Generate**&gt;**rēķina**. Tas rada gaida rēķina dokumenta, kas atjaunina informāciju par projektiem. 

Kreditora rēķina projektu izveide radīs līdz projekta darbības. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Šajā **izdarīts izmaksu** lapu, tiks slēgts 1. solī izveidoto ierakstu un jauniem ierakstiem tiks izveidota, lai atspoguļotu izmaksu saistību sūtījis gaidāmo kreditora rēķinu. **Darbības izcelsme** lauku fiksētās izmaksas tiks iestatīts **kreditora rēķina**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Kreditora rēķins tiks paliek gaidošā stāvoklī, līdz faktiskās kreditora rēķinu ierodas.


