---
title: Konfigurēt un palaist darbu, lai aprēķinātu pārskatus
description: Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu un aprēķinātu izrakstus atlasītajam veikalam vai veikalu grupai.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52798303ef5d96a44270f971703928d0c6c4c2c1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023266"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="db1be-103">Konfigurēt un palaist darbu, lai aprēķinātu pārskatus</span><span class="sxs-lookup"><span data-stu-id="db1be-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="db1be-104">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu un aprēķinātu izrakstus atlasītajam veikalam vai veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="db1be-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="db1be-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="db1be-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="db1be-106">Pārejiet uz sadaļu Visas darbvietas > Veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="db1be-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="db1be-107">Noklikšķiniet uz Aprēķināt izrakstus.</span><span class="sxs-lookup"><span data-stu-id="db1be-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="db1be-108">Atlasiet konkrētu veikalu vai zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="db1be-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="db1be-109">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="db1be-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="db1be-110">Noklikšķiniet uz cilnes Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="db1be-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="db1be-111">Sadaļā Pakešveida apstrāde atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="db1be-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="db1be-112">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="db1be-112">Click Recurrence.</span></span>
6. <span data-ttu-id="db1be-113">Laukā Sākuma datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="db1be-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="db1be-114">Laukā Sākuma laiks ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="db1be-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="db1be-115">Atlasiet opciju Bez beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="db1be-115">Select the No end date option.</span></span>
9. <span data-ttu-id="db1be-116">Laukā PatternUnit ievadiet Dienas.</span><span class="sxs-lookup"><span data-stu-id="db1be-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="db1be-117">Ievadiet skaitli laukā Uz.</span><span class="sxs-lookup"><span data-stu-id="db1be-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="db1be-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="db1be-118">Click OK.</span></span>
12. <span data-ttu-id="db1be-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="db1be-119">Click OK.</span></span>
