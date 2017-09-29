--- 
title: "Masveida finanšu periodu slēgšana"
description: "Šī procedūra parāda, kā aizturēt vai neatgriezeniski slēgt periodu, vai vienlaicīgi vairāk nekā vienu juridisku personu."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8d7151cbcd02f9312ca6b0de5e27231a0b0dc9d6
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="mass-financial-period-close"></a><span data-ttu-id="818f7-103">Masveida finanšu periodu slēgšana</span><span class="sxs-lookup"><span data-stu-id="818f7-103">Mass financial period close</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="818f7-104">Šī procedūra parāda, kā aizturēt vai neatgriezeniski slēgt periodu, vai vienlaicīgi vairāk nekā vienu juridisku personu.</span><span class="sxs-lookup"><span data-stu-id="818f7-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="818f7-105">Turklāt, šis uzdevums parāda, kā ierobežot lietotāju grupu grāmatošanu noteiktiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="818f7-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="818f7-106">Dodieties uz Virsgrāmata > Perioda noslēgšana > Virsgrāmatas kalendāri.</span><span class="sxs-lookup"><span data-stu-id="818f7-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="818f7-107">Ievērojiet, ka parādītais juridisko personu saraksts ir atkarīgs no finanšu kalendāra, kas ir atlasīts lapā.</span><span class="sxs-lookup"><span data-stu-id="818f7-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="818f7-108">Tiks parādītas tikai juridiskās personas, kas izmanto atlasīto finanšu kalendāru.</span><span class="sxs-lookup"><span data-stu-id="818f7-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="818f7-109">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="818f7-109">Click Edit.</span></span>
3. <span data-ttu-id="818f7-110">Atlasiet periodu, kuram vēlaties mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="818f7-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="818f7-111">Atlasiet juridiskās personas, kurām vēlaties atjaunināt statusu.</span><span class="sxs-lookup"><span data-stu-id="818f7-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="818f7-112">Jūs varat ātri atlasīt visas juridiskās personas, atzīmējot izvēles rūtiņu, kas atrodas režģa augšējā kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="818f7-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="818f7-113">Atlasiet Atjaunināt moduļa piekļuvi, lai definētu grāmatošanas piekļuvi atlasītajam modulim.</span><span class="sxs-lookup"><span data-stu-id="818f7-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="818f7-114">Moduļa statusi var tikt atjaunināti viens pēc viena, rediģējot ierakstus režģī.</span><span class="sxs-lookup"><span data-stu-id="818f7-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="818f7-115">Poga ir noderīgas ja vēlaties ātri atjaunināt vairākus juridisko personu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="818f7-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="818f7-116">Laukā Programmas modulis, atlasiet moduli, kura statusu vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="818f7-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="818f7-117">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="818f7-117">Click Select.</span></span>
7. <span data-ttu-id="818f7-118">Piekļuves līmenī, atlasiet Visi, Neviens vai ir konkrēta lietotāju grupa.</span><span class="sxs-lookup"><span data-stu-id="818f7-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="818f7-119">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="818f7-119">Click Select.</span></span>
    * <span data-ttu-id="818f7-120">Visi nozīmē, ka visi lietotāji ar rediģēšanas piekļuvi moduļiem var veikt grāmatošanu, ja periods ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="818f7-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="818f7-121">Neviens nozīmē, ka neviens lietotājs nevar veikt grāmatošanu modulī, ja periods ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="818f7-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="818f7-122">Specifiska lietotāju grupa nozīmē, ka tikai grupas lietotāji var veikt grāmatošanu modulī, ja periods ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="818f7-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="818f7-123">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="818f7-123">Click Update.</span></span>
9. <span data-ttu-id="818f7-124">Atlasīt citu periodu, lai atjauninātu statusu.</span><span class="sxs-lookup"><span data-stu-id="818f7-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="818f7-125">Atlasiet juridiskās personas, kurām vēlaties atjaunināt perioda statusu.</span><span class="sxs-lookup"><span data-stu-id="818f7-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="818f7-126">Atlasiet Perioda statusu, un iestatiet statusu Aizturēts, Atvērts vai Neatgriezeniski slēgts.</span><span class="sxs-lookup"><span data-stu-id="818f7-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="818f7-127">Atvērts norāda uz periodu, kurā var grāmatot, pie nosacījuma, ka lietotājam ir piekļuve.</span><span class="sxs-lookup"><span data-stu-id="818f7-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="818f7-128">Aizturēts nozīmē, ka periods nevar būt grāmatots, bet periodu var atvērt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="818f7-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="818f7-129">Neatgriezeniski slēgts nozīmē, ka periods ir slēgts un to nevar atvērt.</span><span class="sxs-lookup"><span data-stu-id="818f7-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="818f7-130">Korekcijas nevar grāmatot.</span><span class="sxs-lookup"><span data-stu-id="818f7-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="818f7-131">Nav ieteicams iestatīt periodu uz Neatgriezeniski slēgts, kamēr visas korekcijas un auditi nav pabeigti.</span><span class="sxs-lookup"><span data-stu-id="818f7-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="818f7-132">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="818f7-132">Click Update.</span></span>


