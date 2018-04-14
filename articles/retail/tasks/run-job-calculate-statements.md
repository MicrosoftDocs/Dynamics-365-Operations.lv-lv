--- 
title: " Darba konfigurēšana un palaišana, lai aprēķinātu izrakstus"
description: "Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu un aprēķinātu izrakstus atlasītajam veikalam vai veikalu grupai."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6d98adc919d50957b92a879b69517e0a826ea45f
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="41665-103"> Darba konfigurēšana un palaišana, lai aprēķinātu izrakstus</span><span class="sxs-lookup"><span data-stu-id="41665-103">Configure and run a job to calculate statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="41665-104">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu un aprēķinātu izrakstus atlasītajam veikalam vai veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="41665-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="41665-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="41665-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="41665-106">Pārejiet uz sadaļu Visas darbvietas > Mazumtirdzniecības veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="41665-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="41665-107">Noklikšķiniet uz Aprēķināt izrakstus.</span><span class="sxs-lookup"><span data-stu-id="41665-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="41665-108">Atlasiet konkrētu veikalu vai zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="41665-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="41665-109">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="41665-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="41665-110">Noklikšķiniet uz cilnes Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="41665-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="41665-111">Sadaļā Pakešveida apstrāde atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="41665-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="41665-112">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="41665-112">Click Recurrence.</span></span>
6. <span data-ttu-id="41665-113">Laukā Sākuma datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="41665-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="41665-114">Laukā Sākuma laiks ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="41665-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="41665-115">Atlasiet opciju Bez beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="41665-115">Select the No end date option.</span></span>
9. <span data-ttu-id="41665-116">Laukā PatternUnit ievadiet Dienas.</span><span class="sxs-lookup"><span data-stu-id="41665-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="41665-117">Ievadiet skaitli laukā Uz.</span><span class="sxs-lookup"><span data-stu-id="41665-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="41665-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="41665-118">Click OK.</span></span>
12. <span data-ttu-id="41665-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="41665-119">Click OK.</span></span>


