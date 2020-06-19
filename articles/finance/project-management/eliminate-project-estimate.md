---
title: Projekta novērtējuma likvidēšana
description: Šajā tēmā sniegta informācija par projekta budžeta likvidēšanu pēc tam, kad tas ir izpildīts.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410242"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="ddbf9-103">Projekta novērtējuma likvidēšana</span><span class="sxs-lookup"><span data-stu-id="ddbf9-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddbf9-104">Projekta aplēses sniedz finanšu skatījumu darbam, kas ir aplēsts un plānots projektam.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="ddbf9-105">Lai strādātu ar projekta budžetiem, projekts ir jāpievieno budžeta projektam.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="ddbf9-106">Budžeta projekts ir balstīts uz esošu projektu, taču vairāki projekti var attiekties uz vienu budžeta projektu.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="ddbf9-107">Budžeta projektiem var pievienot tikai fiksētas cenas un investīciju projektus, un šiem projektiem ir jāietilpst tajā pašā projektu grupā, kurā ietilpst budžeta projekts.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="ddbf9-108">Lai likvidētu budžeta projektu, tam jābūt pabeigtam.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="ddbf9-109">Tālāk minētajās darbībās ir paskaidrots, kā likvidēt budžetu.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="ddbf9-110">Dodieties uz **Projektu vadība un uzskaite** > **Visi projekti** un atveriet projektu.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="ddbf9-111">Cilnē **Pārvaldīt** atlasiet **Budžeti** un lapā **Budžets** atlasiet **Likvidēt**.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="ddbf9-112">Cilnes **Vispārīgi** lapā **Likvidēt budžetu** iestatiet tālāk norādītās opcijas.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="ddbf9-113">**Perioda kods**: atlasiet perioda kodu, lai izvēlētos atbilstīgos projektu budžetus.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="ddbf9-114">**Budžeta datums**: atlasiet likvidēšanai atbilstošu budžeta datumu.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="ddbf9-115">**Likvidēt ar NP brīdinājumiem**: iespējojiet šo opciju, lai sniegtu paziņojumu, kad tiks likvidēts budžets, kas saistīts ar nepabeigtu darbu (NP).</span><span class="sxs-lookup"><span data-stu-id="ddbf9-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="ddbf9-116">Ja šī opcija nav iespējota, likvidēšanu nevar turpināt, ja pastāv kādas ar budžetu nesaistītas darbības.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="ddbf9-117">Šī opcija ir pieejama tikai tad, ja likvidēšana tiek lietota budžeta projektam.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="ddbf9-118">Tā nav pieejama, ja izmantojat periodiskos grāmatojumus.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="ddbf9-119">Šis iestatījums darbojas ar iestatījumiem lapas **Projekta parametri** cilnes **Likvidēt** lauku grupā **Atļaut likvidēšanu arī tad, ja pastāv ar budžetu nesaistītas transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="ddbf9-120">**Iestatīt stadiju uz Pabeigts** : iespējojiet šo opciju, lai iestatītu budžeta projekta stadiju uz **Pabeigts** pēc tam, kad esat palaidis likvidēšanu.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="ddbf9-121">**Drukāt budžeta sarakstu**: atlasiet informāciju, kura jāiekļauj, drukājot brudžeta sarakstu.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="ddbf9-122">**Rādīt informācijas žurnālu**: iespējojiet šo opciju, lai rādītu informācijas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="ddbf9-123">**Grāmatošanas datums**: izvēlieties budžeta grāmatošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="ddbf9-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-124">Select **OK**.</span></span>
5. <span data-ttu-id="ddbf9-125">Kad likvidēšanas process ir pabeigts, likvidētais budžeta projekts tiek parādīts ar negatīvu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="ddbf9-126">Ja neesat paredzējis likvidēt budžetu, varat atlasīt likvidēt budžetu un atlasīt **Atsaukt likvidēšanu**.</span><span class="sxs-lookup"><span data-stu-id="ddbf9-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
