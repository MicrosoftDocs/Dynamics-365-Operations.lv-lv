---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 16. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 13e89faa3f8470125010ccdb40a6f01c0a9c4fe7
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008781"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-19-2018"></a><span data-ttu-id="3ea32-103">Jaunumi un izmaiņas programmā Dynamics 365 Talent: Core HR (2018. gada 19. oktobris)</span><span class="sxs-lookup"><span data-stu-id="3ea32-103">What's new or changed in Dynamics 365 Talent: Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="3ea32-104">**8.1.1067 būvējums**</span><span class="sxs-lookup"><span data-stu-id="3ea32-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="3ea32-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="3ea32-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="3ea32-106">Ļaušana vadītājiem atjaunināt brīvā laika pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="3ea32-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="3ea32-107">Darbinieku brīvā laika pieprasījumus var būt nepieciešams atjaunināt pēc tam, kad tie ir apstiprināti, izmantojot darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="3ea32-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="3ea32-108">Daudzos gadījumos vadītājs šos atjauninājumus veic darbinieka vārdā.</span><span class="sxs-lookup"><span data-stu-id="3ea32-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="3ea32-109">Šis jaunais līdzeklis nodrošina iespēju vadītājiem atjaunināt brīvo laiku vai atcelt brīvā laika pieprasījumus savu darbinieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="3ea32-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="3ea32-110">Šo iespēju kontrolē parametrs **Darbs kāda vārdā**, un šo parametru var iestatīt lapā **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="3ea32-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="3ea32-111">Ļaušana personāla vadībai (HR) atjaunināt brīvā laika pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="3ea32-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="3ea32-112">Līdzīgi iepriekš aprakstītajam līdzeklim, arī personāla vadībai (HR) var būt nepieciešams atjaunināt darbinieku brīvā laika pieprasījumus pēc tam, kad tie ir apstiprināti, izmantojot darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="3ea32-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="3ea32-113">Šis līdzeklis nodrošina HR lietotājiem iespēju atjaunināt brīvā laika pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="3ea32-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="3ea32-114">Šī iespēja tiek aktivizēta darbvietā **Personas** un lapā **Nodarbinātais**, izmantojot jaunu opciju ar nosaukumu **Skatīt brīvo laiku**.</span><span class="sxs-lookup"><span data-stu-id="3ea32-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="3ea32-115">Šajās lapās HR lietotāji var skatīt pieprasījumus un atjaunināt brīvā laika transakcijas, līdzīgi kā šīs darbības var veikt vadītāji.</span><span class="sxs-lookup"><span data-stu-id="3ea32-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="3ea32-116">Drošības pienākums, kas kontrolē piekļuvi šai funkcionalitātei, ir šāds:</span><span class="sxs-lookup"><span data-stu-id="3ea32-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="3ea32-117">Pienākums: Uzturēt nodarbinātajam raksturīgus atvaļinājumu un prombūtnes procesus.</span><span class="sxs-lookup"><span data-stu-id="3ea32-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="3ea32-118">Privilēģija: Uzturēt visu nodarbināto atvaļinājuma un prombūtnes pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="3ea32-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="3ea32-119">Cita izmaiņas</span><span class="sxs-lookup"><span data-stu-id="3ea32-119">Other changes</span></span>
<span data-ttu-id="3ea32-120">Šajā laidienā ir ieviesti tālāk aprakstītie atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="3ea32-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="3ea32-121">Izmaiņas nodarbināto darbā pieņemšanas darbībās, lai nodarbinātie vairs “neiestrēgtu” stāvoklī **Darbplūsma izpildīta**.</span><span class="sxs-lookup"><span data-stu-id="3ea32-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="3ea32-122">Nodarbinātības ierakstu tagad var izveidot bez nodarbinātības sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="3ea32-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="3ea32-123">Dynamics 365 Talent reģistrācijas datums kursam, kas tiek rādīts darbinieku pašapkalpošanās sadaļā, tagad datumam lieto laika joslas nobīdi.</span><span class="sxs-lookup"><span data-stu-id="3ea32-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="3ea32-124">Excel failus var importēt vairākas reizes bez kļūdām, izmantojot **elementu Darbinieks**.</span><span class="sxs-lookup"><span data-stu-id="3ea32-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="3ea32-125">Zināma problēma</span><span class="sxs-lookup"><span data-stu-id="3ea32-125">Known issue</span></span>

- <span data-ttu-id="3ea32-126">**Problēma**: kad nodarbinātajam tiek pievienots jauns pielikums, poga **Jauns** un **Rediģēt** ir pelēkotas.</span><span class="sxs-lookup"><span data-stu-id="3ea32-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="3ea32-127">**Risinājums:** pirms pielikuma lapas atvēršanas ir jāpārliecinās, vai papildinformācijas lodziņi lapā **Nodarbinātais** ir aizvērti.</span><span class="sxs-lookup"><span data-stu-id="3ea32-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="3ea32-128">Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas.</span><span class="sxs-lookup"><span data-stu-id="3ea32-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="3ea32-129">(Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)</span><span class="sxs-lookup"><span data-stu-id="3ea32-129">(This issue will be fixed in the next platform update.)</span></span>
