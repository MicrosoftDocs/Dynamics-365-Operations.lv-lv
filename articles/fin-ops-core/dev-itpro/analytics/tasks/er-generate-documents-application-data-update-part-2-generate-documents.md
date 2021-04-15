---
title: Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem
description: Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu. (1. daļa - konfigurāciju importēšana).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d3f528d48f345ec4b5cc2a46d7740cb6d0a36cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751086"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="d6f7d-104">Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem</span><span class="sxs-lookup"><span data-stu-id="d6f7d-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6f7d-105">Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (1.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="d6f7d-106">daļa: konfigurāciju importēšana)".</span><span class="sxs-lookup"><span data-stu-id="d6f7d-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="d6f7d-107">Šajā procedūrā jūs izpildāt ER importēta formāta konfigurāciju, kas ir izveidota parauga uzņēmumam Litware.Inc., lai ģenerētu elektroniskos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="d6f7d-108">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="d6f7d-109">Šīs darbības var veikt, izmantojot DEMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="d6f7d-110">Pirms sākat, mainiet valsts kontekstu DEMF uzņēmumam no DEU (Vācija) uz BEL (Beļģija).</span><span class="sxs-lookup"><span data-stu-id="d6f7d-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="d6f7d-111">Lai atjauninātu valsts kodu juridiskās personas DEMF primārajā adresē, noklikšķiniet uz Organizācijas administrēšana > Organizācijas > Juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="d6f7d-112">Restartējiet pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="d6f7d-113">Palaidiet importēto ER formātu</span><span class="sxs-lookup"><span data-stu-id="d6f7d-113">Run imported ER format</span></span>
1. <span data-ttu-id="d6f7d-114">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d6f7d-115">Kokā izvērsiet "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="d6f7d-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="d6f7d-116">Kokā atlasiet "Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="d6f7d-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="d6f7d-117">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-117">Click Run.</span></span>
    * <span data-ttu-id="d6f7d-118">Lai ģenerētu Intrastat pārskatu, palaidiet ER formāta konfigurācijas melnraksta versiju.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="d6f7d-119">Laukā Ievadiet faila nosaukumu ierakstiet "intrastat.xml".</span><span class="sxs-lookup"><span data-stu-id="d6f7d-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="d6f7d-120">Norādiet faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="d6f7d-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-121">Click OK.</span></span>
    * <span data-ttu-id="d6f7d-122">Pārskatiet ģenerēto XML failu.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="d6f7d-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-123">Close the page.</span></span>
8. <span data-ttu-id="d6f7d-124">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="d6f7d-125">Atveriet šo formu, lai apskatītu Intrastat darbības, kas iekļautas ģenerētajā elektroniskajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="d6f7d-126">Noklikšķiniet uz Intrastat arhīva.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="d6f7d-127">Detalizēta informācija par pabeigtu Intrastat pārskatu netika arhivēta, jo izpildītais ER formāts neietver iestatījumus pieteikumu datu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="d6f7d-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-128">Close the page.</span></span>
11. <span data-ttu-id="d6f7d-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d6f7d-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]