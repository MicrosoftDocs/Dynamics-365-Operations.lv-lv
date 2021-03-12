---
title: Konfigurēt un palaist darbu, lai grāmatotu pārskatus
description: Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai grāmatotu izrakstus atlasītajam veikalam vai veikalu grupai.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bed4cfb4875231d11ad76e4403c7995519d56e73
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003682"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="a001d-103">Konfigurēt un palaist darbu, lai grāmatotu pārskatus</span><span class="sxs-lookup"><span data-stu-id="a001d-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a001d-104">Šajā procedūrā ir aprakstīts, kā konfigurēt un izpildīt periodisku pakešuzdevumu, lai grāmatotu izrakstus atlasītajam veikalam vai veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="a001d-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="a001d-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="a001d-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="a001d-106">Dodieties uz Visas darbvietas > ..</span><span class="sxs-lookup"><span data-stu-id="a001d-106">Go to All workspaces > ..</span></span> <span data-ttu-id="a001d-107">> Veikala finanses.</span><span class="sxs-lookup"><span data-stu-id="a001d-107">> Store financials.</span></span>
2. <span data-ttu-id="a001d-108">Noklikšķiniet uz Grāmatot pārskatus partijā.</span><span class="sxs-lookup"><span data-stu-id="a001d-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="a001d-109">Atlasiet organizācijas hierarhiju un pēc tam organizācijas zaru kokā atlasiet atsevišķu veikalu vai zaru.</span><span class="sxs-lookup"><span data-stu-id="a001d-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="a001d-110">Atlasiet zaru, lai izveidotu pakešuzdevumu veikalu grupai.</span><span class="sxs-lookup"><span data-stu-id="a001d-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="a001d-111">Noklikšķiniet uz bultiņas, lai pievienotu atlasi.</span><span class="sxs-lookup"><span data-stu-id="a001d-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="a001d-112">Noklikšķiniet uz cilnes Palaist fonā. ![Palaist fonā](../dev-itpro/media/runbackground.png "Palaist fonā")</span><span class="sxs-lookup"><span data-stu-id="a001d-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="a001d-113">Atzīmējiet izvēles rūtiņu Pakešapstrāde vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="a001d-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="a001d-114">![Pakešveida apstrāde](../dev-itpro/media/batchprocessing.png "Pakešveida apstrāde un periodiskums")</span><span class="sxs-lookup"><span data-stu-id="a001d-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="a001d-115">Noklikšķiniet uz Periodiskums.</span><span class="sxs-lookup"><span data-stu-id="a001d-115">Click Recurrence.</span></span>
6. <span data-ttu-id="a001d-116">Laukā Sākuma datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="a001d-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="a001d-117">Laukā Sākuma laiks ievadiet laiku.</span><span class="sxs-lookup"><span data-stu-id="a001d-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="a001d-118">Izvēlieties, vai izbeigt periodiskumu pēc noteikta izpildes ciklu skaita, noteiktā datumā vai nekad.</span><span class="sxs-lookup"><span data-stu-id="a001d-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="a001d-119">Pēc tam izvēlieties dažādas opcijas, lai noteiktu, cik bieži vēlaties uzdevumu izpildīt.</span><span class="sxs-lookup"><span data-stu-id="a001d-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="a001d-120">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="a001d-120">Click OK.</span></span>
9. <span data-ttu-id="a001d-121">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="a001d-121">Click OK.</span></span>

