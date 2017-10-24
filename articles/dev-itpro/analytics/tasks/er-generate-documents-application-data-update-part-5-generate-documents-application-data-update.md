--- 
title: "Ģenerēt dokumentus, izmantojot pieteikumu datu atjaunināšanu elektronisko pārskatu veidošanai (ER)"
description: "Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra \"ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (4. daļa — modificēt formātu)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b2844621bf50a385ad1a4770c0df2d97623dc77a
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="2e029-103">Ģenerēt dokumentus, izmantojot pieteikumu datu atjaunināšanu elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="2e029-103">Generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e029-104">Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (4. daļa — modificēt formātu)".</span><span class="sxs-lookup"><span data-stu-id="2e029-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="2e029-105">Šajā procedūrā skaidrots, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu un atjauninātu pieteikuma datus.</span><span class="sxs-lookup"><span data-stu-id="2e029-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="2e029-106">Šajā procedūrā jums ir jāizpilda ER formāta konfigurācija, lai ģenerētu Intrastat pārskatu un atjauninātu pieteikumu datus detalizētas informācijas arhivēšanai par pārskatu veidošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="2e029-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="2e029-107">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="2e029-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="2e029-108">Šīs darbības var veikt, izmantojot DEMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="2e029-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="2e029-109">Pirms sākat, pārliecinieties, vai valsts konteksts DEMF uzņēmumam ir BEL (Beļģija).</span><span class="sxs-lookup"><span data-stu-id="2e029-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="2e029-110">Iestatīt starptautiskās tirdzniecības parametrus</span><span class="sxs-lookup"><span data-stu-id="2e029-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="2e029-111">Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="2e029-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="2e029-112">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="2e029-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="2e029-113">Arhivējot detalizētu informāciju par Intrastat pārskatu veidošanas procesu, mums ir nepieciešams noteikt katra izveidotā arhīva ierakstus.</span><span class="sxs-lookup"><span data-stu-id="2e029-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="2e029-114">Šajā nolūkā ir jākonfigurē īpaša numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="2e029-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="2e029-115">Atlasiet atsauci "Intrastat archive ID".</span><span class="sxs-lookup"><span data-stu-id="2e029-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="2e029-116">Laukā Numuru sērijas kods, ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2e029-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="2e029-117">Laukā Numuru sērijas kods ievadiet vai atlasiet vērtību "Fore_2".</span><span class="sxs-lookup"><span data-stu-id="2e029-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="2e029-118">ResolveChanges Numuru sērijas kods.</span><span class="sxs-lookup"><span data-stu-id="2e029-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="2e029-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2e029-119">Click Save.</span></span>
7. <span data-ttu-id="2e029-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2e029-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="2e029-121">Modificētā ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="2e029-121">Run modified ER format</span></span>
1. <span data-ttu-id="2e029-122">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="2e029-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2e029-123">Kokā izvērsiet "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="2e029-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="2e029-124">Kokā atlasiet "Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="2e029-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="2e029-125">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="2e029-125">Click Run.</span></span>
5. <span data-ttu-id="2e029-126">Laukā Ievadiet faila nosaukumu ierakstiet "intrastat2.xml".</span><span class="sxs-lookup"><span data-stu-id="2e029-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="2e029-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="2e029-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="2e029-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2e029-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="2e029-129">ER formāta izpildes rezultātu pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="2e029-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="2e029-130">Pārskatiet ģenerēto XML failu.</span><span class="sxs-lookup"><span data-stu-id="2e029-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="2e029-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2e029-131">Close the page.</span></span>
2. <span data-ttu-id="2e029-132">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2e029-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="2e029-133">Atveriet šo formu, kas satur Intrastat darbības, kuras iekļautas ģenerētajā elektroniskajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="2e029-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="2e029-134">Noklikšķiniet uz Intrastat arhīva.</span><span class="sxs-lookup"><span data-stu-id="2e029-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="2e029-135">Detalizēta informācija par pabeigtu Intrastat pārskatu tika arhivēta, jo izpildītais ER formāts tagad satur iestatījumus pieteikumu datu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="2e029-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="2e029-136">Šajā formā varat redzēt izveidotā arhīva galvenes ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2e029-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="2e029-137">Noklikšķiniet uz Detaļas.</span><span class="sxs-lookup"><span data-stu-id="2e029-137">Click Details.</span></span>
    * <span data-ttu-id="2e029-138">Šajā formā varat redzēt detalizētu informāciju par izveidoto arhīvu.</span><span class="sxs-lookup"><span data-stu-id="2e029-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="2e029-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2e029-139">Close the page.</span></span>
6. <span data-ttu-id="2e029-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2e029-140">Close the page.</span></span>
7. <span data-ttu-id="2e029-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2e029-141">Close the page.</span></span>


