---
title: "Budžeta plānošanas datu sadalījums"
description: "Šajā rakstā ir aprakstītas dažādās sadalījuma metodes, kas ir pieejamas programmatūrā Microsoft Dynamics 365 for Operations, kā arī to lietošanas veids."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8bf0bbdf3fec72761f5db0ffd6d60140e52581c1
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="budget-planning-data-allocation"></a>Budžeta plānošanas datu sadalījums

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstītas dažādās sadalījuma metodes, kas ir pieejamas programmatūrā Microsoft Dynamics 365 for Operations, kā arī to lietošanas veids.  

Varat sadalīt budžeta plāna datus vairākos veidos, lai precīzi attēlotu paredzamās summas.

## <a name="allocation-methods"></a>Sadalījuma metodes
Trīs sadalījuma metodes (sadalīt periodos, sadalīt uz dimensijām un izmantot Virsgrāmatas sadalījuma kārtulas) var izveidot budžeta plāna rindas, kas balstās uz rindām vienā budžeta plānā. Trīs citas metodes (apkopot, izplatīt un kopēt no budžeta plāna) var izveidot budžeta plāna rindas citos budžeta plānos. Visām sešām sadalījuma metodēm jānorāda mērķa scenārijs. Mērķa scenārijs var būt vai nu tas pats avota scenārijs vai atšķirīgs no avota scenārija. Papildus varat norādīt, vai jaunas rindas tiek pievienotas budžeta plānam vai aizstās esošās budžeta plāna rindas.

[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Sadalīt pa periodiem** — lai budžeta plāna rindas no avota budžeta plāna scenārija sadalītu pa mērķa scenārija periodiem, tiek izmantota periodu sadalījuma kategorija. Avota summa tiek piešķirta vairākām rindām mērķa scenārijā, pamatojoties uz procentuālo attiecību un datumu, kas ir noteikti perioda sadalījuma kategorijā.         

[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Sadalījums uz dimensijām** — budžeta plāna rindas tiek sadalītas no avota budžeta plānošanas scenārija uz vienu vai vairākām rindām mērķa scenārijā, balstoties uz procentuālo sadalījumu un finanšu dimensijām, kas definētas atlasītajā budžeta sadalījuma noteikumā.           

![](./media/aggregatechart-300x230.png)
**Apkopot** — budžeta plāna rindas tiek apkopotas no avota budžeta plāna scenārija saistītajos (pakārtotajos) budžeta plānos uz mērķa scenāriju pamata budžeta plānā. Šī metode ļauj budžeta summas, kas sagatavotas zemākā organizācijas līmenī, konsolidēt augstākā līmenī.          

[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Izplatīt** — budžeta plāna rindas tiek izplatītas no avota budžeta plānošanas scenārija pamata budžeta plānā uz mērķa scenāriju saistītajos (pakārtotajos) budžeta plānos, pamatojoties uz saistīto plānu organizācijas vienību finanšu dimensijām. Šī metode ļauj budžeta summas, kas sagatavotas augstākā organizācijas līmenī, izplatīt lokālai pārskatīšanai.           

[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Izmantot Virsgrāmatas sadalījuma kārtulas** — budžeta plāna rindas tiek sadalītas no avota budžeta plānošanas scenārija uz mērķa scenāriju saskaņā ar atlasīto Virsgrāmatas sadalījuma kārtulu. 

[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopēt no budžeta plāna** — tāpat kā izplatīšanas sadalījuma metodē, budžeta plāna rindas tiek veidotas mērķa plānā, pamatojoties uz rindām saistītajā budžeta plānā. Tomēr šajā metodē avota budžeta plānam nav jābūt priekštecim, tas var būt jebkurā augstākā līmenī budžeta plānu hierarhijā. Šī sadalījuma metode ir noderīga, ja konsolidētās summas sākotnēji tiek iekļautas budžetā daudz augstākā līmenī un tās jāpārsūta uz zemāku organizācijas līmeni sīkākai pārskatīšanai un pielāgošanai, pirms tās var saņemt augstāka līmeņa apstiprinājumu.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Sadalījuma metožu izmantošana budžeta plānā
Lai veiktu sadalījumu budžeta plāna lapā, atlasiet sadalāmās rindas un pēc tam noklikšķiniet uz **Sadalīt budžetu**.

[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Pēc tam atlasiet sadalījuma metodi. Atlikušie lauki pēc tam tiek iestatīti, pamatojoties uz atlasītās metodes. Šie lauki ietver avota un mērķa budžeta plānu datus un opciju, kas ļauj reizināt avotu ar norādīto koeficientu, izveidojot mērķa summas, lai vienkāršotu lielapjoma korekcijas. Varat arī iestatīt opciju **Pievienot plānam**. Atlasiet **Nē**, lai aizstātu esošās budžeta plāna rindas, vai atlasiet **Jā**, lai saglabātu esošās budžeta plāna rindas un pievienotu jaunas rindas sadalītajām summām.

## <a name="automating-allocations-during-a-workflow"></a>Sadalījumu automatizācija darbplūsmas laikā
Jaudīga funkcija ļauj sadalījumus veikt automātiski kā daļu no budžeta plānošanas darbplūsmas. Budžeta plānam pārvietojoties pa tā darbplūsmu, automatizētie uzdevumi var uzsākt sadalījumu norādītajā budžeta plānošanas stadijā. 

Lai iestatītu automātisko sadalījumu, vispirms jāizveido sadalījuma grafiks lapā **Budžeta plānošanas konfigurācija**. Sadalījuma grafiks nosaka sadalījuma metodi, kas tiks izmantota automatizētā sadalījuma izpildē un dažādu sadalījuma opciju vērtības (skatiet aprakstu iepriekšējā sadaļā). 

Pēc tam izveidojiet stadijas sadalījumu lapā **Budžeta plānošanas konfigurācija**. Stadijas sadalījums piešķir sadalījuma grafiku budžeta plānošanas darbplūsmai un stadijai. 

Visbeidzot, pievienojiet automatizētu uzdevumu budžeta plānošanas stadijas sadalījumam vēlamajā darbplūsmas stadijā. Šajā piemērā darbplūsmā ietverti divi budžeta plānošanas stadiju sadalījumi (apzīmēts ar sarkanu krāsu).

[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)




