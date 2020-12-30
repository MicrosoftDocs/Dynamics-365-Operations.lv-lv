---
title: Konsolidācijas kontu grupas un papildu konsolidācijas konti
description: Šajā tēmā ir sniegta informācija par konsolidācijas kontu grupām un papildu konsolidācijas kontiem, kā arī paskaidrota to lietošana programmā Microsoft Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8db7a60656434aafd8114b08c2c0e9493140f27b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445712"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="2c3b9-103">Konsolidācijas kontu grupas un papildu konsolidācijas konti</span><span class="sxs-lookup"><span data-stu-id="2c3b9-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c3b9-104">Šajā tēmā ir sniegta informācija par konsolidācijas kontu grupām un papildu konsolidācijas kontiem, kā arī paskaidrota to lietošana programmā Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 Finance.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="2c3b9-105">Konsolidācijas kontu grupas</span><span class="sxs-lookup"><span data-stu-id="2c3b9-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="2c3b9-106">Konsolidācijas kontu grupas jums ļauj veidot grupas no kontiem, kurus vēlaties izmantot datu konsolidēšanai.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="2c3b9-107">Parasti konsolidācijas kontu grupa pārstāv likumā noteiktu kontu plānu vai kartē kontus uz uzņēmuma vadības definētu grupu.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="2c3b9-108">Konsolidācijas kontu grupas ir atrodamas moduļa **Konsolidācijas** apgabalā **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="2c3b9-109">Kad pievienojat jaunu grupu, šai kontu grupai ir jāievada unikāls identifikators un nosaukums.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="2c3b9-110">Papildu konsolidācijas konti</span><span class="sxs-lookup"><span data-stu-id="2c3b9-110">Additional consolidation accounts</span></span>
<span data-ttu-id="2c3b9-111">Papildu konsolidācijas konti jums ļauj konsolidācijas kontu grupai piešķirt kontu no jau esoša kontu plāna.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="2c3b9-112">Pēc tam varat norādīt konsolidācijas konta vērtību un nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="2c3b9-113">Papildu konsolidācijas konti ir atrodami moduļa **Konsolidācijas** apgabalā **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="2c3b9-114">Kad veidojat jaunu konsolidācijas kontu, ir jānorāda tālāk uzskaitītā informācija.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="2c3b9-115">**Galvenais konts** — šis lauks ir uzmeklēšana, kas rāda visus galvenos kontus, kuri ir balstīti uz lapā atlasīto kontu plānu.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="2c3b9-116">Kad atlasāt kādu kontu, šis nosaukums tiek automātiski ievadīts laukā **Galvenā konta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="2c3b9-117">**Konsolidācijas kontu grupa** — izmantojiet šo lauku, lai norādītu grupu, kurai kontu piešķirt.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="2c3b9-118">Ja konsolidēšanu veicat divos dažādos veidos, tad tas pats konts jums ir jāpievieno visām četrām konsolidācijas kontu grupām.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="2c3b9-119">**Konsolidācijas konts** — ievadiet konsolidācijas konta vērtību.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="2c3b9-120">Šai vērtībai nav jābūt kontam no kontu plāna.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="2c3b9-121">Tā var būt jebkāda jums nepieciešama vērtība.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="2c3b9-122">**Konsolidācijas konta nosaukums** — ievadiet nosaukumu kontam, kuru vēlaties rādīt pieprasījumos un pārskatos.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="2c3b9-123">**SAT līmenis** — šis laiks tiek izmantots, lai iesniegtu kontu izrakstus Meksikas nodokļu iestādēm.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="2c3b9-124">Kad esat beidzis veidot savas konsolidācijas kontu grupas un papildu konsolidācijas kontus, varat atlasīt grupu procesā Konsolidēt tiešsaistē.</span><span class="sxs-lookup"><span data-stu-id="2c3b9-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="2c3b9-125">Plašāku informāciju skatiet šeit: [Izveidot konsolidācijas grupas un papildu konsolidācijas kontus](../general-ledger/tasks/create-consolidation-groups.md)</span><span class="sxs-lookup"><span data-stu-id="2c3b9-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 



