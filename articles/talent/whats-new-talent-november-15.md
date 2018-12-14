---
title: "Jaun. un izm. programmā Dynamics 365 for Talent Core HR (2018. g. 15. nov.)"
description: "Šajā tēmā ir aprakstīti līdzekļi, kas ir jauni vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a><span data-ttu-id="04d61-103">Jaun. un izm. programmā Dynamics 365 for Talent Core HR (2018. g. 15. nov.)</span><span class="sxs-lookup"><span data-stu-id="04d61-103">What's new or changed in Dynamics 365 for Talent Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="04d61-104">**8.1.2045 būvējums**</span><span class="sxs-lookup"><span data-stu-id="04d61-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="04d61-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="04d61-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="04d61-106">Citas izmaiņas/labojumi</span><span class="sxs-lookup"><span data-stu-id="04d61-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="04d61-107">Nevar mainīt darbinieka pašreizējo amatu uz turpmāko atvērto amatu</span><span class="sxs-lookup"><span data-stu-id="04d61-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="04d61-108">Ir veiktas izmaiņas, lai iespējotu amatu pārnešanu, ja amats ir pieejams tikai nākotnē.</span><span class="sxs-lookup"><span data-stu-id="04d61-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="04d61-109">Amats netiek rādīts, veidojot jaunu darbinieku</span><span class="sxs-lookup"><span data-stu-id="04d61-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="04d61-110">Ir veiktas izm., lai rādītu visus atvērtos amatus, kas pieejami piešķiršanai, pieņemot darbā jaunu darb. programmā Talent.</span><span class="sxs-lookup"><span data-stu-id="04d61-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="04d61-111">Tas ietver vēsturiskos amatus vai gadījumus, ja amatiem ir nākotnes datums.</span><span class="sxs-lookup"><span data-stu-id="04d61-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="04d61-112">Tagad amati tiks rādīti pareizi, balstoties uz nodarbin. sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="04d61-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="04d61-113">Izbeigš. datumu rāda, balstoties uz lietot. iestat.</span><span class="sxs-lookup"><span data-stu-id="04d61-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="04d61-114">Ir veiktas izm. bijušo darbinieku sarakstā, lai ņemtu vērā laika joslu nobīdes darbiniekiem vēlamajai laika joslai, skatot darba attiec. pārtraukšanas datumu.</span><span class="sxs-lookup"><span data-stu-id="04d61-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="04d61-115">Darba vienumu, kas saistīti ar mani, saites neparāda pareizo inform.</span><span class="sxs-lookup"><span data-stu-id="04d61-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="04d61-116">Ar šīm izmaiņām navigācija uz atsevišķu darba vienumu informāciju sarakstā parādīs pareizu informāciju atlasītajam krājumam.</span><span class="sxs-lookup"><span data-stu-id="04d61-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="04d61-117">Šī problēma rodas tikai ar papildu drošības opcijām.</span><span class="sxs-lookup"><span data-stu-id="04d61-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="04d61-118">Zināma problēma</span><span class="sxs-lookup"><span data-stu-id="04d61-118">Known issue</span></span>

- <span data-ttu-id="04d61-119">**Problēma**: kad nodarbinātajam tiek pievienots jauns pielikums, poga **Jauns** un **Rediģēt** ir pelēkotas.</span><span class="sxs-lookup"><span data-stu-id="04d61-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="04d61-120">**Risinājums:** pirms pielikuma lapas atvēršanas ir jāpārliecinās, vai papildinformācijas lodziņi lapā **Nodarbinātais** ir aizvērti.</span><span class="sxs-lookup"><span data-stu-id="04d61-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="04d61-121">Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas.</span><span class="sxs-lookup"><span data-stu-id="04d61-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="04d61-122">(Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)</span><span class="sxs-lookup"><span data-stu-id="04d61-122">(This issue will be fixed in the next platform update.)</span></span>
