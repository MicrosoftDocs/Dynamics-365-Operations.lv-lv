---
title: Masveida finanšu periodu slēgšana
description: Šajā tēmā rādīts, kā apturēt periodu vai pastāvīgi slēgt periodu vairāk nekā vienai juridiskai personai vienlaikus.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4db0f68a22f9129041c7a7c081f397c34c2b07eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254443"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="a0eb2-103">Masveida finanšu periodu slēgšana</span><span class="sxs-lookup"><span data-stu-id="a0eb2-103">Mass financial period close</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0eb2-104">Šajā tēmā rādīts, kā apturēt periodu vai pastāvīgi slēgt periodu vairāk nekā vienai juridiskai personai vienlaikus.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-104">This topic shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="a0eb2-105">Turklāt, šis uzdevums parāda, kā ierobežot lietotāju grupu grāmatošanu noteiktiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="a0eb2-106">Navigācijas rūtī dodieties uz **Moduļi > Virsgrāmata > Perioda slēgšana > Virsgrāmatas kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-106">In the navigation pane, go to **Modules > General ledger > Period close > Ledger calendars**.</span></span> <span data-ttu-id="a0eb2-107">Ievērojiet, ka parādītais juridisko personu saraksts ir atkarīgs no finanšu kalendāra, kas ir atlasīts lapā.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="a0eb2-108">Tiks parādītas tikai juridiskās personas, kas izmanto atlasīto finanšu kalendāru.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-108">Only legal entities using the selected fiscal calendar will display.</span></span>
2. <span data-ttu-id="a0eb2-109">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-109">Select **Edit**.</span></span>
3. <span data-ttu-id="a0eb2-110">Atlasiet periodu, kuram vēlaties mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="a0eb2-111">Atlasiet juridiskās personas, kurām vēlaties atjaunināt statusu.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-111">Select the legal entities for which you want to update the status.</span></span> <span data-ttu-id="a0eb2-112">Jūs varat ātri atlasīt visas juridiskās personas, atlasot atzīmi režģa augšējā kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-112">You can quickly select all legal entities by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="a0eb2-113">Atlasiet **Atjaunināt moduļa piekļuvi**, lai definētu grāmatošanas piekļuvi atlasītajam modulim.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-113">Select **Update module access** to define the posting access to a selected module.</span></span> <span data-ttu-id="a0eb2-114">Moduļa statusi var tikt atjaunināti viens pēc viena, rediģējot ierakstus režģī.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="a0eb2-115">Poga ir noderīgas ja vēlaties ātri atjaunināt vairākus juridisko personu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="a0eb2-116">Modulī **Lietojumprogramma** atlasiet moduli, kuram vēlaties atjaunināt statusu.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-116">In the **Application** module, select the module that you want to update the status.</span></span> <span data-ttu-id="a0eb2-117">Noklikšķiniet uz **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-117">Click **Select**.</span></span>
7. <span data-ttu-id="a0eb2-118">Līmenī **Piekļuve** atlasiet **Visi**, **Neviens** vai konkrētu lietotāju grupu.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-118">In the **Access** level, select **All**, **None**, or a specific user group.</span></span> <span data-ttu-id="a0eb2-119">Noklikšķiniet uz **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-119">Click **Select**.</span></span> <span data-ttu-id="a0eb2-120">Visi nozīmē, ka visi lietotāji ar rediģēšanas piekļuvi moduļiem var veikt grāmatošanu, ja periods ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="a0eb2-121">Neviens nozīmē, ka neviens lietotājs nevar veikt grāmatošanu modulī, ja periods ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="a0eb2-122">Specifiska lietotāju grupa nozīmē, ka tikai grupas lietotāji var veikt grāmatošanu modulī, ja periods ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="a0eb2-123">Atlasiet **Atjaunināt**.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-123">Select **Update**.</span></span>
9. <span data-ttu-id="a0eb2-124">Atlasīt citu periodu, lai atjauninātu statusu.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="a0eb2-125">Atlasiet juridiskās personas, kurām vēlaties atjaunināt perioda statusu.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="a0eb2-126">Atlasiet **Atjaunināt perioda statusu** un iestatiet statusu uz **Apturēts**, **Atvērts** vai **Pastāvīgi slēgts**.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-126">Select **Update period status** and set the status of **On hold**, **Open**, or **Permanently closed**.</span></span> <span data-ttu-id="a0eb2-127">**Atvērts** norāda uz to, ka periodu var grāmatot, ja lietotājam ir piekļuve.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-127">**Open** indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="a0eb2-128">**Apturēts** nozīmē, ka periodu nevar grāmatot, taču periodu var atvērt no jauna.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-128">**On hold** means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="a0eb2-129">**Pastāvīgi slēgts** nozīmē, ka periods ir slēgts un nevar tikt atvērts.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-129">**Permanently closed** means the period is closed and can never be opened.</span></span> <span data-ttu-id="a0eb2-130">Korekcijas nevar grāmatot.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="a0eb2-131">Mēs neiesakām iestatīt periodu uz **Pastāvīgi slēgts**, kamēr nav pabeigti visi pielāgojumi un auditi.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-131">We do not recommend setting a period to **Permanently closed** until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="a0eb2-132">Atlasiet **Atjaunināt**.</span><span class="sxs-lookup"><span data-stu-id="a0eb2-132">Select **Update**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]