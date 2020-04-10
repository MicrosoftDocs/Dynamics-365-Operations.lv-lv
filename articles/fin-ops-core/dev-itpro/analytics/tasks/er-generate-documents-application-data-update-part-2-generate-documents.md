---
title: Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem
description: 'Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (1. daļa — importa konfigurācijas).'
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
ms.openlocfilehash: 0ca80a2cc1e58723d1f1b39c1fde003fa990a93c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142436"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="ea8a1-103">Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem</span><span class="sxs-lookup"><span data-stu-id="ea8a1-103">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea8a1-104">Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (1.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="ea8a1-105">daļa: konfigurāciju importēšana)".</span><span class="sxs-lookup"><span data-stu-id="ea8a1-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="ea8a1-106">Šajā procedūrā jūs izpildāt ER importēta formāta konfigurāciju, kas ir izveidota parauga uzņēmumam Litware.Inc., lai ģenerētu elektroniskos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="ea8a1-107">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="ea8a1-108">Šīs darbības var veikt, izmantojot DEMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="ea8a1-109">Pirms sākat, mainiet valsts kontekstu DEMF uzņēmumam no DEU (Vācija) uz BEL (Beļģija).</span><span class="sxs-lookup"><span data-stu-id="ea8a1-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="ea8a1-110">Lai atjauninātu valsts kodu juridiskās personas DEMF primārajā adresē, noklikšķiniet uz Organizācijas administrēšana > Organizācijas > Juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="ea8a1-111">Restartējiet pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="ea8a1-112">Palaidiet importēto ER formātu</span><span class="sxs-lookup"><span data-stu-id="ea8a1-112">Run imported ER format</span></span>
1. <span data-ttu-id="ea8a1-113">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ea8a1-114">Kokā izvērsiet "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="ea8a1-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="ea8a1-115">Kokā atlasiet "Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="ea8a1-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="ea8a1-116">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-116">Click Run.</span></span>
    * <span data-ttu-id="ea8a1-117">Lai ģenerētu Intrastat pārskatu, palaidiet ER formāta konfigurācijas melnraksta versiju.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="ea8a1-118">Laukā Ievadiet faila nosaukumu ierakstiet "intrastat.xml".</span><span class="sxs-lookup"><span data-stu-id="ea8a1-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="ea8a1-119">Norādiet faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="ea8a1-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-120">Click OK.</span></span>
    * <span data-ttu-id="ea8a1-121">Pārskatiet ģenerēto XML failu.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="ea8a1-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-122">Close the page.</span></span>
8. <span data-ttu-id="ea8a1-123">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="ea8a1-124">Atveriet šo formu, lai apskatītu Intrastat darbības, kas iekļautas ģenerētajā elektroniskajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="ea8a1-125">Noklikšķiniet uz Intrastat arhīva.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="ea8a1-126">Detalizēta informācija par pabeigtu Intrastat pārskatu netika arhivēta, jo izpildītais ER formāts neietver iestatījumus pieteikumu datu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="ea8a1-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-127">Close the page.</span></span>
11. <span data-ttu-id="ea8a1-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ea8a1-128">Close the page.</span></span>

