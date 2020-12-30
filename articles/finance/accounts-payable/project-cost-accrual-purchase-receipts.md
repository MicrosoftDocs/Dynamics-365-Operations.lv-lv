---
title: Uzkrātās projekta izmaksas pirkšanas pavadzīmēs
description: Šajā tēmā ir aprakstīts, kā var izsekot uzkrātajām projekta izmaksām pirkšanas pavadzīmēs programmā Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0a930b4921a29d5ce561ce0e958733f0c3261b81
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445546"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Uzkrātās projekta izmaksas pirkšanas pavadzīmēs

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā var izsekot uzkrātajām projekta izmaksām pirkšanas pavadzīmēs programmā Microsoft Dynamics 365 Finance. 

Bieži vien projekta rēķini tiek saņemti vēlāk par preču un pakalpojumu piegādi, un tas var būtiski ietekmēt projekta izpildes pamatrādītājus (KPI). Ir svarīgi, lai jūs varētu izsekot šīs transakcijas gan finanšu, gan projekta pārskatos.

Tas ir atainots tālāk sniegtajā scenārija piemērā. 

Uzņēmums Contoso Consulting ir sācis jaunu mākoņa izvietošanas projektu. Ir izveidots pirkšanas pasūtījums, lai nopirktu datoru šī projekta vajadzībām. Datora izmaksas ir $ 1500 un uzstādīšanas pakalpojumu izmaksas ir $ 150. Kreditors ir piegādājis un uzstādījis datoru, taču uzņēmums Contoso Consulting vēl nav saņēmis rēķinu. Projekta vadītājs vēlas redzēt uzkrātās projekta izmaksas $ 1650, pirms tiek piegādāts rēķins. Šīs izmaksas ir arī jāietver uzņēmuma mēneša beigu finanšu pārskatos. 

Uzkrātās izmaksas ir jāreģistrē gan finanšu līmenī, gan projekta līmenī pārskatu izveides nolūkā. Var izsekot krājumu un sagādes kategoriju preces ieejas plūsmas finanšu atjauninājumu. 

Krājumiem lapā **Kreditoru parādu parametri** atlasiet opciju **Grāmatot produktu ieejas plūsmas Virsgrāmatā**.
[![Kreditoru parādu parametru lapa](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Sagādes kategorijām lapā **Kategorijas ierobežojuma nosacījums** atlasiet nosacījumus **Pirkšana** un pēc tam katrai sagādes kategorijai atlasiet vienumu **rāt ieejas plūsmas pirkšanas izdevumus**.
[![Kategorijas ierobežojuma nosacījumu lapa](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Grāmatojot ar preces ieejas plūsmu saistītos dokumentus, tiek izmantoti konti **Pirkšanas izdevumi, kas nav iekļauti rēķinos** un **Pirkumu uzkrājums**, kas ir ietverti sadaļā **Grāmatošanas iestatīšana**.

Izmantojot to pašu scenāriju, apskatīsim, kā preces ieejas plūsmas grāmatošana ietekmē Virsgrāmatas un preces informāciju. 

**1. darbība.** Izveidojiet un apstipriniet jaunu projekta pirkšanas pasūtījumu, lai reģistrētu datora pirkšanu par $ 1500 un uzstādīšanas pakalpojumus par $ 150.
[![Jauna pirkšanas pasūtījuma izveide](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Pēc pirkšanas pasūtījuma apstiprināšanas tiek izveidotas projekta fiksēto izmaksu transakcijas. 
[![Izveidotās darbības](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Tiek iestatīta fiksēto izmaksu transakciju lauka **Darbības izcelsme** vērtība **Pirkšanas pasūtījums**. Izveidojot un apstiprinot pirkšanas pasūtījumu, netiek izveidotas projekta transakcijas. 

**2. darbība.** Tiek piegādātas preces un pakalpojumu, un tiek reģistrēta preces ieejas plūsma. 

Grāmatojot preces ieejas plūsmu, tiek ģenerēts dokuments, kas tiek grāmatots Virsgrāmatā. Šis dokuments izraisa pirkšanas izdevumu rēķinos neiekļautu izdevumu konta debitēšanu un pirkumu uzkrājuma konta kreditēšanu. 
[![Dokumentu transakcijas](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Grāmatojot preces ieejas plūsmu, tiek izmantoti sagādes kategoriju un preču grāmatošanas iestatījumi, nevis projektu kategoriju grāmatošanas iestatījumi. Lai pareizi atainotu pirkumu uzkrājumu finanšu ietekmi, ir jāsaskaņo šie iestatījumi. 

Sagādes kategorijas var kartēt ar preču kategorijām lapā **Sagādes kategorija**.
[![Sagādes kategorijas lapa](./media/accruals7-1024x390.png)](./media/accruals7.png)

**3. darbība.** Izveidojiet kreditora rēķina melnrakstu. 

Preces ieejas plūsmas grāmatošana neietekmē projekta informāciju. Lai to atrisinātu, varat ģenerēt kreditora rēķina melnrakstu uzreiz pēc pirkšanas ieejas plūsmas grāmatošanas. Pārejiet uz lapu **Pirkšanas pasūtījums** &gt; **cilni Rēķins** &gt; **Ģenerēt** &gt; **Rēķins**. Tādējādi tiek izveidots nenokārtota rēķina dokuments, kas nodrošina projekta informācijas atjaunināšanu. 

Izveidojot kreditora rēķina melnrakstu, tiek ģenerētas nepabeigtas projekta transakcijas. 
[![Nepabeigtie projektu darījumi](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Lapā **Fiksētās izmaksas** tiek slēgti 1. darbības ietvaros izveidotie ieraksti un tiek izveidoti jauni ieraksti, kas atbilst fiksētajām izmaksām nenokārtotajā kreditora rēķinā. Tiek iestatīta fiksēto izmaksu lauka **Darbības izcelsme** vērtība **Kreditora rēķins**.
[![Fiksēto izmaksu lapa](./media/accruals9-1024x200.png)](./media/accruals9.png)

Kreditora rēķina stāvoklis ir Nenokārtots, līdz tiek saņemts faktiskais kreditora rēķins.



