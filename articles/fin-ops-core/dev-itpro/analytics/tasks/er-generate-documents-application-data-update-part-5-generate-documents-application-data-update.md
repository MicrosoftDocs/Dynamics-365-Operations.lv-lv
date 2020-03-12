---
title: Dokumentu ar programmas datiem ģenerēšana
description: 'Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (4. daļa — modificēt formātu)".'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 759869577ef30cd3f81eb74103a93cc5d1a3d608
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042854"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="35eeb-103">Dokumentu ar programmas datiem ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="35eeb-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35eeb-104">Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (4. daļa — modificēt formātu)".</span><span class="sxs-lookup"><span data-stu-id="35eeb-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="35eeb-105">Šajā procedūrā skaidrots, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu un atjauninātu pieteikuma datus.</span><span class="sxs-lookup"><span data-stu-id="35eeb-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="35eeb-106">Šajā procedūrā jums ir jāizpilda ER formāta konfigurācija, lai ģenerētu Intrastat pārskatu un atjauninātu pieteikumu datus detalizētas informācijas arhivēšanai par pārskatu veidošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="35eeb-107">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="35eeb-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="35eeb-108">Šīs darbības var veikt, izmantojot DEMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="35eeb-109">Pirms sākat, pārliecinieties, vai valsts konteksts DEMF uzņēmumam ir BEL (Beļģija).</span><span class="sxs-lookup"><span data-stu-id="35eeb-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="35eeb-110">Iestatīt starptautiskās tirdzniecības parametrus</span><span class="sxs-lookup"><span data-stu-id="35eeb-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="35eeb-111">Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="35eeb-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="35eeb-112">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="35eeb-112">Click the Number sequences tab.</span></span>

    <span data-ttu-id="35eeb-113">Arhivējot detalizētu informāciju par Intrastat pārskatu veidošanas procesu, mums ir nepieciešams noteikt katra izveidotā arhīva ierakstus.</span><span class="sxs-lookup"><span data-stu-id="35eeb-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="35eeb-114">Šajā nolūkā ir jākonfigurē īpaša numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="35eeb-114">A special number sequence must be configured for that.</span></span>  

3. <span data-ttu-id="35eeb-115">Atlasiet atsauci "Intrastat archive ID".</span><span class="sxs-lookup"><span data-stu-id="35eeb-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="35eeb-116">Laukā Numuru sērijas kods, ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="35eeb-116">In the Number sequence code field, type a value.</span></span>

    <span data-ttu-id="35eeb-117">Laukā Numuru sērijas kods ievadiet vai atlasiet vērtību "Fore_2".</span><span class="sxs-lookup"><span data-stu-id="35eeb-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  

5. <span data-ttu-id="35eeb-118">ResolveChanges Numuru sērijas kods.</span><span class="sxs-lookup"><span data-stu-id="35eeb-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="35eeb-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="35eeb-119">Click Save.</span></span>
7. <span data-ttu-id="35eeb-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="35eeb-121">Modificētā ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="35eeb-121">Run modified ER format</span></span>
1. <span data-ttu-id="35eeb-122">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="35eeb-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="35eeb-123">Kokā izvērsiet "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="35eeb-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="35eeb-124">Kokā atlasiet "Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="35eeb-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="35eeb-125">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="35eeb-125">Click Run.</span></span>
5. <span data-ttu-id="35eeb-126">Laukā Ievadiet faila nosaukumu ierakstiet "intrastat2.xml".</span><span class="sxs-lookup"><span data-stu-id="35eeb-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
6. <span data-ttu-id="35eeb-127">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="35eeb-127">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="35eeb-128">ER formāta izpildes rezultātu pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="35eeb-128">Review ER format execution’s results</span></span>
<span data-ttu-id="35eeb-129">Pārskatiet ģenerēto XML failu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-129">Review the generated XML file.</span></span>  
1. <span data-ttu-id="35eeb-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-130">Close the page.</span></span>
2. <span data-ttu-id="35eeb-131">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="35eeb-131">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>

    <span data-ttu-id="35eeb-132">Atveriet šo formu, kas satur Intrastat darbības, kuras iekļautas ģenerētajā elektroniskajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="35eeb-132">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  

3. <span data-ttu-id="35eeb-133">Noklikšķiniet uz Intrastat arhīva.</span><span class="sxs-lookup"><span data-stu-id="35eeb-133">Click Intrastat archive.</span></span>

    <span data-ttu-id="35eeb-134">Detalizēta informācija par pabeigtu Intrastat pārskatu tika arhivēta, jo izpildītais ER formāts tagad satur iestatījumus pieteikumu datu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="35eeb-134">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="35eeb-135">Šajā formā varat redzēt izveidotā arhīva galvenes ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-135">In this form, you can see the header record of the created archive.</span></span>  

4. <span data-ttu-id="35eeb-136">Noklikšķiniet uz Detaļas.</span><span class="sxs-lookup"><span data-stu-id="35eeb-136">Click Details.</span></span>

    <span data-ttu-id="35eeb-137">Šajā formā varat redzēt detalizētu informāciju par izveidoto arhīvu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-137">In this form, you can see the details for the created archive.</span></span>  

5. <span data-ttu-id="35eeb-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-138">Close the page.</span></span>
6. <span data-ttu-id="35eeb-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-139">Close the page.</span></span>
7. <span data-ttu-id="35eeb-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35eeb-140">Close the page.</span></span>

