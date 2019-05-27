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
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550166"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="e0ae2-103">Konfigurēt un palaist darbu, lai aprēķinātu pārskatus</span><span class="sxs-lookup"><span data-stu-id="e0ae2-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e0ae2-104">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai izveidotu un aprēķinātu izrakstus atlasītajam veikalam vai veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="e0ae2-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e0ae2-106">Pārejiet uz sadaļu Visas darbvietas > Mazumtirdzniecības veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="e0ae2-107">Noklikšķiniet uz Aprēķināt izrakstus.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="e0ae2-108">Atlasiet konkrētu veikalu vai zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="e0ae2-109">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="e0ae2-110">Noklikšķiniet uz cilnes Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="e0ae2-111">Sadaļā Pakešveida apstrāde atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="e0ae2-112">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-112">Click Recurrence.</span></span>
6. <span data-ttu-id="e0ae2-113">Laukā Sākuma datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="e0ae2-114">Laukā Sākuma laiks ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="e0ae2-115">Atlasiet opciju Bez beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-115">Select the No end date option.</span></span>
9. <span data-ttu-id="e0ae2-116">Laukā PatternUnit ievadiet Dienas.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="e0ae2-117">Ievadiet skaitli laukā Uz.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="e0ae2-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-118">Click OK.</span></span>
12. <span data-ttu-id="e0ae2-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e0ae2-119">Click OK.</span></span>

