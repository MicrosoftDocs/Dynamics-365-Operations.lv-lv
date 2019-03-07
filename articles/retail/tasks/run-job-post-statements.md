---
title: Konfigurēt un palaist darbu, lai grāmatotu pārskatus
description: Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai grāmatotu izrakstus atlasītajam veikalam vai veikalu grupai.
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
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "346299"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="15fb4-103">Konfigurēt un palaist darbu, lai grāmatotu pārskatus</span><span class="sxs-lookup"><span data-stu-id="15fb4-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="15fb4-104">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai grāmatotu izrakstus atlasītajam veikalam vai veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="15fb4-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="15fb4-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="15fb4-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="15fb4-106">Dodieties uz Visas darbvietas > ..</span><span class="sxs-lookup"><span data-stu-id="15fb4-106">Go to All workspaces > ..</span></span> <span data-ttu-id="15fb4-107">> Mazumtirdzniecības veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="15fb4-107">> Retail store financials.</span></span>
2. <span data-ttu-id="15fb4-108">Noklikšķiniet uz Grāmatot izrakstus.</span><span class="sxs-lookup"><span data-stu-id="15fb4-108">Click Post statements.</span></span>
    * <span data-ttu-id="15fb4-109">Atlasiet organizācijas hierarhiju un pēc tam organizācijas zaru kokā atlasiet atsevišķu veikalu vai zaru.</span><span class="sxs-lookup"><span data-stu-id="15fb4-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="15fb4-110">Atlasiet zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="15fb4-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="15fb4-111">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="15fb4-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="15fb4-112">Noklikšķiniet uz cilnes Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="15fb4-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="15fb4-113">Atzīmējiet izvēles rūtiņu Pakešapstrāde vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="15fb4-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="15fb4-114">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="15fb4-114">Click Recurrence.</span></span>
6. <span data-ttu-id="15fb4-115">Laukā Sākuma datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="15fb4-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="15fb4-116">Laukā Sākuma laiks ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="15fb4-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="15fb4-117">Izvēlieties, vai izbeigt periodiskumu pēc noteikta izpildes ciklu skaita, noteiktā datumā vai nekad.</span><span class="sxs-lookup"><span data-stu-id="15fb4-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="15fb4-118">Pēc tam izvēlieties dažādas opcijas, lai noteiktu, cik bieži vēlaties uzdevumu izpildīt.</span><span class="sxs-lookup"><span data-stu-id="15fb4-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="15fb4-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="15fb4-119">Click OK.</span></span>
9. <span data-ttu-id="15fb4-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="15fb4-120">Click OK.</span></span>

