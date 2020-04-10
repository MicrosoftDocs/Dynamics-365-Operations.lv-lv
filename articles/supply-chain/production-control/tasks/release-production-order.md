---
title: Ražošanas pasūtījuma nodošana izpildei
description: Šajā procedūrā parādīts kā ražošanas pasūtījumu nodot izpildei.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e98adea620d74bdb7a90cedc9b256d9883b27525
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148975"
---
# <a name="release-a-production-order"></a><span data-ttu-id="07551-103">Ražošanas pasūtījuma nodošana izpildei</span><span class="sxs-lookup"><span data-stu-id="07551-103">Release a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07551-104">Šajā procedūrā parādīts kā ražošanas pasūtījumu nodot izpildei.</span><span class="sxs-lookup"><span data-stu-id="07551-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="07551-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="07551-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="07551-106">Šī ir ceturtā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="07551-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="07551-107">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="07551-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="07551-108">Režģī atlasiet ražošanas pasūtījumu, kura statuss ir Ieplānots.</span><span class="sxs-lookup"><span data-stu-id="07551-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="07551-109">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="07551-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="07551-110">Noklikšķiniet uz Nodot izpildei.</span><span class="sxs-lookup"><span data-stu-id="07551-110">Click Release.</span></span>
    * <span data-ttu-id="07551-111">Šajā lapā varat apstiprināt atlasītā ražošanas pasūtījumu kopuma nodošanu izpildei.</span><span class="sxs-lookup"><span data-stu-id="07551-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="07551-112">Ja vēlaties pievienot pasūtījumus, noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="07551-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="07551-113">Solī Nodot izpildei jānorāda, kad ražošanas pasūtījums ir jānodod ražotnei, lai ražotnes operatori varētu ziņot par ražošanas darbu progresu.</span><span class="sxs-lookup"><span data-stu-id="07551-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="07551-114">Var izsniegt ražošanas dokumentāciju, kas satur svarīgu informāciju par ražošanas darbiem.</span><span class="sxs-lookup"><span data-stu-id="07551-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="07551-115">Noliktavas darbs izejmateriālu atlasei tiek veidots krājumiem, kas iestatīti noliktavas procesā.</span><span class="sxs-lookup"><span data-stu-id="07551-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="07551-116">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="07551-116">Click the General tab.</span></span>
    * <span data-ttu-id="07551-117">Atlasiet, kuri ražošanas pārskati ir jādrukā.</span><span class="sxs-lookup"><span data-stu-id="07551-117">Select which production reports should be printed.</span></span> <span data-ttu-id="07551-118">Darbu kartes pārskatā tiek izdrukāta lapa katram ieplānotajam darbam, un ražošanas pasūtījumam jābūt ieplānotam darba līmenī.</span><span class="sxs-lookup"><span data-stu-id="07551-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="07551-119">Pārskats ietver informāciju par plānoto sākuma un beigu laiku, ražojamo daudzumu un informāciju par to, kurš resurss apstrādā darbu.</span><span class="sxs-lookup"><span data-stu-id="07551-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="07551-120">Maršruta darbu pārskatā apkopota tā pati informācija vienā lapā, līdz ar to katram darbam netiek drukāta atsevišķa lapa.</span><span class="sxs-lookup"><span data-stu-id="07551-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="07551-121">Maršruta kartes pārskats attēlo tikai operācijas, bet neattēlo darbus.</span><span class="sxs-lookup"><span data-stu-id="07551-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="07551-122">Tāpēc šim pārskatam nav nepieciešama darbu plānošana, to var izmantot, kad ražošanas uzdevumi ir ieplānoti operāciju līmenī.</span><span class="sxs-lookup"><span data-stu-id="07551-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="07551-123">Noklikšķiniet uz izvēles rūtiņas Drukāt maršruta karti.</span><span class="sxs-lookup"><span data-stu-id="07551-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="07551-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="07551-124">Click OK.</span></span>
7. <span data-ttu-id="07551-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="07551-125">Close the page.</span></span>

