---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 1. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97820cd25ece48dc0b8045d9ba509d0971ca5aad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305291"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a><span data-ttu-id="fde69-103">Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 1. oktobris)</span><span class="sxs-lookup"><span data-stu-id="fde69-103">What's new or changed in Dynamics 365 for Talent Core HR (October 1, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fde69-104">**8.1.1035.0 būvējums**</span><span class="sxs-lookup"><span data-stu-id="fde69-104">**Build 8.1.1035.0**</span></span>

<span data-ttu-id="fde69-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="fde69-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="turn-off-electronic-payment-validation"></a><span data-ttu-id="fde69-106">Elektronisko maksājumu apstiprināšanas izslēgšana</span><span class="sxs-lookup"><span data-stu-id="fde69-106">Turn off electronic payment validation</span></span>

<span data-ttu-id="fde69-107">Elektronisko maksājumu informācijas pārbaude tiek veikta tad, ja tiek iestatīti izdevumi par tiešo depozītu, vai nu izmantojot darbvietu **Darbinieku patstāvīgi izmantojams pakalpojums** (ESS) vai tieši darbinieka veidlapu.</span><span class="sxs-lookup"><span data-stu-id="fde69-107">Electronic payment information validation occurs if you set up disbursements for direct deposit either through **Employee self-service** workspace (ESS) or directly on the employee form.</span></span> <span data-ttu-id="fde69-108">Šī opcija nodrošina elastību noņemt šo validāciju, ja nav nepieciešamas summu un atlikušo vērtību apstiprināšanas pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="fde69-108">This option gives you the flexibility to remove that validation if you do not require the validation checks for amounts and remainder values.</span></span> <span data-ttu-id="fde69-109">Šo līdzekli var izmantot, ja notiek ārējas algu sistēmas ar atšķirīgām prasībām integrēšana.</span><span class="sxs-lookup"><span data-stu-id="fde69-109">This feature is helpful if you're integrating with an external payroll system that has different requirements.</span></span>

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a><span data-ttu-id="fde69-110">Vadītāja patstāvīgi izmantojams pakalpojums — komandas dalībnieku mērķu pievienošana, izmantojot grupas veiktspējas mērķu elementu</span><span class="sxs-lookup"><span data-stu-id="fde69-110">Manager self-service - Add goals for team members through the Team performance goals tile</span></span>

<span data-ttu-id="fde69-111">Pirms šī laidiena vadītāji varēja pievienot saviem darbiniekiem mērķus individuāli, izmantojot veiktspējas mērķus, kas saistīti ar katru darbinieku.</span><span class="sxs-lookup"><span data-stu-id="fde69-111">Prior to this release, managers can add goals to their employees individually through the performance goals associated to each employee.</span></span> <span data-ttu-id="fde69-112">Šajā atjauninājumā vadītāji var piekļūt elementam **Grupas veiktspējas mērķi** un izveidot jaunus mērķus, atlasot kādu no viņu tiešajiem ziņojumiem.</span><span class="sxs-lookup"><span data-stu-id="fde69-112">With this update, managers can access the **Team performance goals** tile and create new goals by selecting any of their direct reports.</span></span>

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a><span data-ttu-id="fde69-113">Vadītāja patstāvīgi izmantojams pakalpojums — komandas dalībnieku pārskatu pievienošana, izmantojot grupas veiktspējas pārskatu elementu</span><span class="sxs-lookup"><span data-stu-id="fde69-113">Manager self-service - Add reviews for team members through the Team performance reviews tile</span></span>

<span data-ttu-id="fde69-114">Pirms šī laidiena vadītāji varēja pievienot saviem darbiniekiem pārskatus individuāli, izmantojot pārskatus, kas saistīti ar katru darbinieku.</span><span class="sxs-lookup"><span data-stu-id="fde69-114">Prior to this release, managers can add reviews to their employees individually through the reviews associated to each employee.</span></span> <span data-ttu-id="fde69-115">Šajā atjauninājumā vadītāji var piekļūt elementam **Grupas veiktspējas pārskati** un izveidot jaunus pārskatus, atlasot kādu no viņu tiešajiem ziņojumiem.</span><span class="sxs-lookup"><span data-stu-id="fde69-115">With this update, managers can access the **Team performance reviews** tile and create new reviews by selecting any of their direct reports.</span></span>

## <a name="configure-proration-options-by-leave-plan"></a><span data-ttu-id="fde69-116">Proporcionalitātes opciju konfigurēšana pēc atvaļinājumu plāna</span><span class="sxs-lookup"><span data-stu-id="fde69-116">Configure proration options by leave plan</span></span>

<span data-ttu-id="fde69-117">Organizācijas piešķir prombūtnes laiku dažādi atkarībā no tā, kad darbinieks ir pievienojies uzņēmumam vai atstājis to.</span><span class="sxs-lookup"><span data-stu-id="fde69-117">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="fde69-118">Dažās organizācijās darbiniekiem tiek piešķirts to pilns sadalījums no to pirmās darba dienas, bet citi sadala piemaksas proporcionāli.</span><span class="sxs-lookup"><span data-stu-id="fde69-118">For some organizations, employees are awarded their full allocation on their start date while others prorate the award.</span></span> <span data-ttu-id="fde69-119">Šajā laidienā ir nodrošinātas jaunas opcijas, kas ļauj izvēlēties, kā proporcionāli sadalīt piemaksas un uzkrājumus darbiniekiem, kas pievienojas organizācijai vai atstāj to.</span><span class="sxs-lookup"><span data-stu-id="fde69-119">New options are provided in this release to choose how to prorate the awards and accruals for joiners and leavers in an organization.</span></span> <span data-ttu-id="fde69-120">Opcijas ir šādas: Proporcionāli sadalīts, Pilns uzkrājums un Nav uzkrājuma.</span><span class="sxs-lookup"><span data-stu-id="fde69-120">Options include: Prorated, Full accrual, and No accrual.</span></span>

## <a name="other-changes"></a><span data-ttu-id="fde69-121">Cita izmaiņas</span><span class="sxs-lookup"><span data-stu-id="fde69-121">Other changes</span></span>

-   <span data-ttu-id="fde69-122">Elements Darbinieks atjaunināts — elementu **Darbinieki** tagad var atjaunināt, izmantojot Excel pievienojumprogrammu/datu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="fde69-122">Employee entity updated - The **Personal** title can now be updated using the Excel add-in/data management.</span></span>

-   <span data-ttu-id="fde69-123">Drošības iestatījumu izmaiņas, kas ļauj noņemt pogu **Dzēst** un **Deaktivizēt** maksājuma informācijas darbinieka patstāvīgi izmantojamā pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="fde69-123">Security change to allow removal of the **Delete** and **Deactivate** buttons in employee self-service for payment information.</span></span>

## <a name="known-issue"></a><span data-ttu-id="fde69-124">Zināma problēma</span><span class="sxs-lookup"><span data-stu-id="fde69-124">Known issue</span></span>

-   <span data-ttu-id="fde69-125">**Problēma:** pievienojot nodarbinātajam jaunu pielikumu, tiek deaktivizēta poga **Jauns** un **Rediģēt**. **Risinājums:** pirms pielikuma lapas atvēršanas pārbaudiet, vai lapā **Nodarbinātais** ir aizvērta papildinformācija.</span><span class="sxs-lookup"><span data-stu-id="fde69-125">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="fde69-126">Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, elementa **Pielikumi** pogas tiek iespējotas.</span><span class="sxs-lookup"><span data-stu-id="fde69-126">If the FactBoxes are closed when the **Worker** page is loaded, the **Attachments** buttons will be enabled.</span></span> <span data-ttu-id="fde69-127">(Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)</span><span class="sxs-lookup"><span data-stu-id="fde69-127">(This issue will be fixed in the next platform update.)</span></span>
