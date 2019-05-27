---
title: Personāla vadības (HR) parametru iestatīšana dažādās juridiskajās personās
description: Jums ir jāiestata koplietotie parametri ierakstiem, kas tiek koplietoti uzņēmumu starpā, piemēram, amatu ierakstiem. Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: a8167545864a1cc2fc22f044f7d16ca590d59b43
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518588"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a><span data-ttu-id="10432-104">Personāla vadības (HR) parametru iestatīšana dažādās juridiskajās personās</span><span class="sxs-lookup"><span data-stu-id="10432-104">Set up Human resources (HR) parameters across legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="10432-105">Jums ir jāiestata koplietotie parametri ierakstiem, kas tiek koplietoti uzņēmumu starpā, piemēram, amatu ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="10432-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="10432-106">Šajā rakstā ir paskaidrots, kā iestatīt personāla vadības parametrus juridiskām personām.</span><span class="sxs-lookup"><span data-stu-id="10432-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="10432-107">Uzņēmumi koplieto dažu veidu ierakstus, piemēram, amatu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="10432-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="10432-108">Šiem ierakstiem ir jāiestata koplietojamie parametri.</span><span class="sxs-lookup"><span data-stu-id="10432-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="10432-109">Piemēram, lapu **Personāla vadības kopīgie parametri** var izmantot, lai iestatītu Personāla vadības parametrus juridiskām personām.</span><span class="sxs-lookup"><span data-stu-id="10432-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="10432-110">Lapā **Personāla vadības kopīgie parametri** parametri tiek grupēti apgabalos, pamatojoties uz to funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="10432-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="10432-111">Iepriekš izlaistā funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="10432-111">Previously released functionality</span></span>
<span data-ttu-id="10432-112">Cilnē **Identifikācija** ir jāatlasa identifikācijas tipi, kas pārstāv šajā lapā uzskaitītos identifikācijas numurus.</span><span class="sxs-lookup"><span data-stu-id="10432-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="10432-113">Identifikācijas tipi ir jāiestata, pirms darbiniekiem varat ievadīt identifikācijas informāciju.</span><span class="sxs-lookup"><span data-stu-id="10432-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="10432-114">Informācija par sociālās apdrošināšanas numuru, nacionālo ID numuru, ārzemnieka ID numuru un personas kodu tiek glabāta lapā **Identifikācijas tips**.</span><span class="sxs-lookup"><span data-stu-id="10432-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="10432-115">Lai definētu jaunu identifikācijas tipu vai pārskatītu esošo tipu sarakstu, noklikšķiniet uz **Personāla vadība** &gt; **cilne Saites** &gt; **Iestatījumi** &gt; **Identifikācijas tipi**.</span><span class="sxs-lookup"><span data-stu-id="10432-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="10432-116">Var ievadīt vienkāršu kodu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="10432-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="10432-117">Ja lietojat programmu Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="10432-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="10432-118">Cilnē **Identifikācija** ir jāatlasa identifikācijas tipi, kas pārstāv šajā lapā uzskaitītos identifikācijas numurus.</span><span class="sxs-lookup"><span data-stu-id="10432-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="10432-119">Identifikācijas tipi ir jāiestata, pirms darbiniekiem varat ievadīt identifikācijas informāciju.</span><span class="sxs-lookup"><span data-stu-id="10432-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="10432-120">Informācija par sociālās apdrošināšanas numuru, nacionālo ID numuru, ārzemnieka ID numuru un personas kodu tiek glabāta lapā **Identifikācijas tips**.</span><span class="sxs-lookup"><span data-stu-id="10432-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="10432-121">Lai definētu jaunu identifikācijas tipu vai pārskatītu esošo tipu sarakstu, noklikšķiniet uz **Personāla vadība** &gt; **Iestatījumi** &gt; **Identifikācijas tipi**.</span><span class="sxs-lookup"><span data-stu-id="10432-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="10432-122">Var ievadīt vienkāršu kodu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="10432-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="10432-123">Cilnē **Numuru sērijas** var atlasīt numuru sērijas, kas tiek izmantotas šiem ierakstiem: Personāla numurs, Amats, Lietotāja pieprasījuma ID, I-9 dokuments, Kandidāts, Diskusija, Atvieglojumu ID un Personāla darbība (ja ir aktivizēts šis ieraksta tips).</span><span class="sxs-lookup"><span data-stu-id="10432-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="10432-124">Lai saglabātu numuru sēriju atsauces un kodus, lietojiet saraksta lapu **Numuru sērijas**.</span><span class="sxs-lookup"><span data-stu-id="10432-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="10432-125">Lai atrastu šo lapu, lietojiet lapu meklēšanas funkciju.</span><span class="sxs-lookup"><span data-stu-id="10432-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="10432-126">Cilnē **Amati** norādiet, vai jauni amati ir pieejami piešķiršanai pēc noklusējuma:</span><span class="sxs-lookup"><span data-stu-id="10432-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="10432-127">**Vienmēr** — darbiniekus jauniem amatiem var piešķirt amatu izveides brīdī.</span><span class="sxs-lookup"><span data-stu-id="10432-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="10432-128">Izveidojot amatus, datums un laiks **Pieejams piešķirei** cilnē **Vispārīgi** lapā **Amati** tiek automātiski iestatīti uz izveides datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="10432-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="10432-129">**Nekad** — darbiniekus jauniem amatiem nevar piešķirt amatu izveides brīdī.</span><span class="sxs-lookup"><span data-stu-id="10432-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="10432-130">Ja šī opcija ir atlasīta, kļūstot pieejamam katram jaunam amatam būs jāatver forma **Amats** un pēc tam cilnē **Vispārīgi** jāievada datums **Pieejams piešķirei**, lai iespējotu darbinieka piešķiri.</span><span class="sxs-lookup"><span data-stu-id="10432-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="10432-131">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="10432-131">Additional resources</span></span>
--------

[<span data-ttu-id="10432-132">Uzņēmumam raksturīgo PV parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="10432-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)



