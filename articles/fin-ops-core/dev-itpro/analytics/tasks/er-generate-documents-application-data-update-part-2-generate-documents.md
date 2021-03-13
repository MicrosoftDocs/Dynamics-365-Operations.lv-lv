---
title: Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem
description: Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu. (1. daļa - konfigurāciju importēšana).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 417c419dc6925bac337fe74a2f057395316ec75d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092926"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="046a6-104">Konfigurāciju noformēšana, lai ģenerētu dokumentus ar programmas datiem</span><span class="sxs-lookup"><span data-stu-id="046a6-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="046a6-105">Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (1.</span><span class="sxs-lookup"><span data-stu-id="046a6-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="046a6-106">daļa: konfigurāciju importēšana)".</span><span class="sxs-lookup"><span data-stu-id="046a6-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="046a6-107">Šajā procedūrā jūs izpildāt ER importēta formāta konfigurāciju, kas ir izveidota parauga uzņēmumam Litware.Inc., lai ģenerētu elektroniskos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="046a6-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="046a6-108">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="046a6-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="046a6-109">Šīs darbības var veikt, izmantojot DEMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="046a6-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="046a6-110">Pirms sākat, mainiet valsts kontekstu DEMF uzņēmumam no DEU (Vācija) uz BEL (Beļģija).</span><span class="sxs-lookup"><span data-stu-id="046a6-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="046a6-111">Lai atjauninātu valsts kodu juridiskās personas DEMF primārajā adresē, noklikšķiniet uz Organizācijas administrēšana > Organizācijas > Juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="046a6-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="046a6-112">Restartējiet pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="046a6-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="046a6-113">Palaidiet importēto ER formātu</span><span class="sxs-lookup"><span data-stu-id="046a6-113">Run imported ER format</span></span>
1. <span data-ttu-id="046a6-114">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="046a6-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="046a6-115">Kokā izvērsiet "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="046a6-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="046a6-116">Kokā atlasiet "Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="046a6-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="046a6-117">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="046a6-117">Click Run.</span></span>
    * <span data-ttu-id="046a6-118">Lai ģenerētu Intrastat pārskatu, palaidiet ER formāta konfigurācijas melnraksta versiju.</span><span class="sxs-lookup"><span data-stu-id="046a6-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="046a6-119">Laukā Ievadiet faila nosaukumu ierakstiet "intrastat.xml".</span><span class="sxs-lookup"><span data-stu-id="046a6-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="046a6-120">Norādiet faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="046a6-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="046a6-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="046a6-121">Click OK.</span></span>
    * <span data-ttu-id="046a6-122">Pārskatiet ģenerēto XML failu.</span><span class="sxs-lookup"><span data-stu-id="046a6-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="046a6-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="046a6-123">Close the page.</span></span>
8. <span data-ttu-id="046a6-124">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="046a6-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="046a6-125">Atveriet šo formu, lai apskatītu Intrastat darbības, kas iekļautas ģenerētajā elektroniskajā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="046a6-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="046a6-126">Noklikšķiniet uz Intrastat arhīva.</span><span class="sxs-lookup"><span data-stu-id="046a6-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="046a6-127">Detalizēta informācija par pabeigtu Intrastat pārskatu netika arhivēta, jo izpildītais ER formāts neietver iestatījumus pieteikumu datu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="046a6-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="046a6-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="046a6-128">Close the page.</span></span>
11. <span data-ttu-id="046a6-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="046a6-129">Close the page.</span></span>

