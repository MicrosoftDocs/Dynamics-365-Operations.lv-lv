--- 
title: " Darba konfigurēšana un palaišana, lai grāmatotu izrakstus"
description: "Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai grāmatotu izrakstus atlasītajam veikalam vai veikalu grupai."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0e2dae54cc9ccfc0a85046c5478e539585c3744d
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="085f5-103"> Darba konfigurēšana un palaišana, lai grāmatotu izrakstus</span><span class="sxs-lookup"><span data-stu-id="085f5-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="085f5-104">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai grāmatotu izrakstus atlasītajam veikalam vai veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="085f5-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="085f5-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="085f5-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="085f5-106">Dodieties uz Visas darbvietas > ..</span><span class="sxs-lookup"><span data-stu-id="085f5-106">Go to All workspaces > ..</span></span> <span data-ttu-id="085f5-107">> Mazumtirdzniecības veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="085f5-107">> Retail store financials.</span></span>
2. <span data-ttu-id="085f5-108">Noklikšķiniet uz Grāmatot izrakstus.</span><span class="sxs-lookup"><span data-stu-id="085f5-108">Click Post statements.</span></span>
    * <span data-ttu-id="085f5-109">Atlasiet organizācijas hierarhiju un pēc tam organizācijas zaru kokā atlasiet atsevišķu veikalu vai zaru.</span><span class="sxs-lookup"><span data-stu-id="085f5-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="085f5-110">Atlasiet zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="085f5-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="085f5-111">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="085f5-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="085f5-112">Noklikšķiniet uz cilnes Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="085f5-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="085f5-113">Atzīmējiet izvēles rūtiņu Pakešapstrāde vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="085f5-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="085f5-114">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="085f5-114">Click Recurrence.</span></span>
6. <span data-ttu-id="085f5-115">Laukā Sākuma datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="085f5-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="085f5-116">Laukā Sākuma laiks ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="085f5-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="085f5-117">Izvēlieties, vai izbeigt periodiskumu pēc noteikta izpildes ciklu skaita, noteiktā datumā vai nekad.</span><span class="sxs-lookup"><span data-stu-id="085f5-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="085f5-118">Pēc tam izvēlieties dažādas opcijas, lai noteiktu, cik bieži vēlaties uzdevumu izpildīt.</span><span class="sxs-lookup"><span data-stu-id="085f5-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="085f5-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="085f5-119">Click OK.</span></span>
9. <span data-ttu-id="085f5-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="085f5-120">Click OK.</span></span>


