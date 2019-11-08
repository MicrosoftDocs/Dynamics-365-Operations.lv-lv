---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada augusts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
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
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: 14dc4d2a1b69f58d6d9c2466b2bcaf4f9185931e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550278"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-august-2018"></a><span data-ttu-id="03724-103">Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada augusts)</span><span class="sxs-lookup"><span data-stu-id="03724-103">What's new or changed in Dynamics 365 Talent - Core HR (August 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03724-104">**8.1.104 būvējums**</span><span class="sxs-lookup"><span data-stu-id="03724-104">**Build 8.1.104**</span></span>

<span data-ttu-id="03724-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="03724-105">This topic describes features that are either new or changed in Dynamics 365 Talent: Core HR.</span></span>

## <a name="view-expiring-records-in-manager-self-service"></a><span data-ttu-id="03724-106">Skatiet vadītāju patstāvīgi lietojamā pakalpojuma ierakstus, kam beidzas derīgums</span><span class="sxs-lookup"><span data-stu-id="03724-106">View expiring records in Manager self service</span></span>

<span data-ttu-id="03724-107">Tagad varat skatīt vadītāju patstāvīgi lietojamā pakalpojuma ierakstus, kam beidzas derīgums</span><span class="sxs-lookup"><span data-stu-id="03724-107">You can now view expiring records in Manager self-service.</span></span> <span data-ttu-id="03724-108">Jaunas opcijas ļauj jums konfigurēt, kāda informācija būs pieejami vadītājiem skatīšanai.</span><span class="sxs-lookup"><span data-stu-id="03724-108">New options are allow you to configure what information will be available for managers to view.</span></span> <span data-ttu-id="03724-109">Tās iekļauj:</span><span class="sxs-lookup"><span data-stu-id="03724-109">These include:</span></span>

-   <span data-ttu-id="03724-110">Sertifikāti</span><span class="sxs-lookup"><span data-stu-id="03724-110">Certificates</span></span>

-   <span data-ttu-id="03724-111">Identifikācijas numuri</span><span class="sxs-lookup"><span data-stu-id="03724-111">Identification numbers</span></span>

-   <span data-ttu-id="03724-112">Probācijas periodi</span><span class="sxs-lookup"><span data-stu-id="03724-112">Probation periods</span></span>

-   <span data-ttu-id="03724-113">Izvērtēšana</span><span class="sxs-lookup"><span data-stu-id="03724-113">Screenings</span></span>

-   <span data-ttu-id="03724-114">Testi</span><span class="sxs-lookup"><span data-stu-id="03724-114">Tests</span></span>

<span data-ttu-id="03724-115">Šis līdzeklis arī sniedz iespēju norādīt diapazonu dienās, lai meklētu ierakstus, kam beidzas derīgums.</span><span class="sxs-lookup"><span data-stu-id="03724-115">This feature also gives you the ability to specify the range of days in which to look for expiring records.</span></span>

## <a name="configurable-transfer-actions"></a><span data-ttu-id="03724-116">Konfigurējamas pārsūtīšanas darbības</span><span class="sxs-lookup"><span data-stu-id="03724-116">Configurable transfer actions</span></span>

<span data-ttu-id="03724-117">Var konfigurēt pēc lomas opcijas, kas būs pieejama pārsūtīšanas pieprasījuma izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="03724-117">You can configure by role the options that will be available during the entry of a transfer request.</span></span> <span data-ttu-id="03724-118">Šis līdzeklis nodrošina papildu elastību lomām organizācijā.</span><span class="sxs-lookup"><span data-stu-id="03724-118">This feature provides additional flexibility across the roles in an organization.</span></span>

<span data-ttu-id="03724-119">Piemēram, vadītājiem, kuri pieprasa darbinieku pārsūtīšanu, nedrīkst būt piekļuve atlīdzības summas ieteikšanai vai uzdevumu sarakstu atlasīšanai, kas tiks saistīti ar pārsūtīšanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="03724-119">For example, managers requesting employee transfers may not have access to suggest or enter compensation amounts or select the task lists that will be associated with the transfer request.</span></span> <span data-ttu-id="03724-120">Šajā gadījumā, vadītāji var izveidot un iesniegt pārsūtīšanas pieprasījumus, bet tiem nav atļauts ievadīt atlīdzības vai uzdevumu sarakstu piešķires.</span><span class="sxs-lookup"><span data-stu-id="03724-120">In this case, managers can create and submit transfer requests but are not allowed to enter compensation or task list assignments.</span></span> <span data-ttu-id="03724-121">Šajā pašā konfigurācijā HR varēs piešķirt jaunās atlīdzības vērtības, kā arī piešķirt jebkurus papildu kontrolsarakstus, kuri jāaizpilda pārsūtīšanas veikšanas rezultātā.</span><span class="sxs-lookup"><span data-stu-id="03724-121">In this same configuration, HR will be able to assign the new compensation values as well as assign any additional checklists to be completed as a result of the transfer completing.</span></span>

<span data-ttu-id="03724-122">Pēc noklusējuma jaunās konfigurācijas opcijas ir iestatītas, lai iespējas nevarētu mainīt pirms šī atjauninājuma.</span><span class="sxs-lookup"><span data-stu-id="03724-122">By default, the new configuration options are set to not change the capabilities prior to this update.</span></span>

## <a name="leave-and-absence"></a><span data-ttu-id="03724-123">Atvaļinājumi un kavējumi</span><span class="sxs-lookup"><span data-stu-id="03724-123">Leave and absence</span></span>

<span data-ttu-id="03724-124">Tagad ir pieejami papildu datumu lauki atvaļinājumiem un kavējumiem.</span><span class="sxs-lookup"><span data-stu-id="03724-124">There are now additional Date fields available in Leave and Absence.</span></span>

<span data-ttu-id="03724-125">Ar šo līdzekli varat iestatīt uzkrājuma perioda principu plāna līmenī, lai lietotu noteiktus darbinieku datumus.</span><span class="sxs-lookup"><span data-stu-id="03724-125">With this feature you can set the accrual period basis at the plan level to use specific employee dates.</span></span> <span data-ttu-id="03724-126">Tas atvaļinājuma uzkrāšanas procesa laikā ļauj lietot datumus, kuri nav plāna sākuma datums.</span><span class="sxs-lookup"><span data-stu-id="03724-126">This allows for dates other than the plan start date to be used during the leave accrual process.</span></span> <span data-ttu-id="03724-127">Darbiniekam specifisku datumu opcijas ietver tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="03724-127">Options for employee specific dates include the following values:</span></span>

-   <span data-ttu-id="03724-128">Pielāgots (pieejama pirms šī atjauninājuma)</span><span class="sxs-lookup"><span data-stu-id="03724-128">Custom (available prior to this update)</span></span>

-   <span data-ttu-id="03724-129">Gadadienas datums</span><span class="sxs-lookup"><span data-stu-id="03724-129">Anniversary date</span></span>

-   <span data-ttu-id="03724-130">Sākotnējais darbā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="03724-130">Original hire date</span></span>

-   <span data-ttu-id="03724-131">Darba stāža datums</span><span class="sxs-lookup"><span data-stu-id="03724-131">Seniority date</span></span>

-   <span data-ttu-id="03724-132">Nodarbinātā koriģētais pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="03724-132">Worker’s adjusted start date</span></span>

-   <span data-ttu-id="03724-133">Nodarbinātā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="03724-133">Worker’s start date</span></span>

<span data-ttu-id="03724-134">Ja konfigurēts, lai izmantotu vienu no darbiniekam specifiskiem datumiem, reģistrācijas process izmanto norādīto datumu, lai aprēķinātu uzkrāšanas periodus.</span><span class="sxs-lookup"><span data-stu-id="03724-134">When configured to use one of the employee specific dates, the enrollment process will use the specified date to calculate the accrual periods.</span></span> <span data-ttu-id="03724-135">Uzkrāšanas perioda princips tiek parādīts arī darbinieka plāna reģistrācijā, lai palīdzētu jums saprast, kas tiek izmantots uzkrāšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="03724-135">The accrual period basis is also displayed on the employee’s plan enrollment to help you understand what’s being used during the accrual process.</span></span>

## <a name="microsoft-word-integration"></a><span data-ttu-id="03724-136">Microsoft Word integrēšana</span><span class="sxs-lookup"><span data-stu-id="03724-136">Microsoft Word integration</span></span>

<span data-ttu-id="03724-137">Dokumentu veidnes ir iespējotas visā Core HR programmatūrā.</span><span class="sxs-lookup"><span data-stu-id="03724-137">Document templates have been enabled throughout Core HR.</span></span> <span data-ttu-id="03724-138">Šis līdzeklis ļauj izveidot vēstules un pārskatus uz jūsu izveidotās Word veidnes bāzes.</span><span class="sxs-lookup"><span data-stu-id="03724-138">This feature allows you to create letters and reports based on Word templates that you create.</span></span>

<span data-ttu-id="03724-139">Papildinformācija par šo līdzekli ir pieejama vietnē [Office integrāciju apmācība](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span><span class="sxs-lookup"><span data-stu-id="03724-139">Additional information about this feature is available in the [Office integration tutorial](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span></span>


## <a name="other-fixes"></a><span data-ttu-id="03724-140">Citi labojumi</span><span class="sxs-lookup"><span data-stu-id="03724-140">Other fixes</span></span>

<span data-ttu-id="03724-141">Šajā izlaidumā ir ietverti arī vairāki kļūdu labojumi, jaunu vienumu pievienojums, esošo vienumu labojumi un lokalizētas marķējumu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="03724-141">This release also includes a number of bug fixes, the addition of new entities, fixes to existing entities, and localized label changes.</span></span>
