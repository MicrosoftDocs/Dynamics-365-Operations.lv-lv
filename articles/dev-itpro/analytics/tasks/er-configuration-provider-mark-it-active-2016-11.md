--- 
title: "Konfigurāciju nodrošinātāju izveide un atzīmēšana aktīvā statusā"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot konfigurācijas nodrošinātāju Elektroniskajos pārskatos (ER)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13a27c2fec2a2b226e9ae8d5b8f9a61e8b79ceb0
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="f3a2e-103">Konfigurāciju nodrošinātāju izveide un atzīmēšana aktīvā statusā</span><span class="sxs-lookup"><span data-stu-id="f3a2e-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3a2e-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot konfigurācijas nodrošinātāju Elektroniskajos pārskatos (ER).</span><span class="sxs-lookup"><span data-stu-id="f3a2e-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="f3a2e-105">Katra ER konfigurācija atsauksies uz nodrošinātāju kā konfigurācijas autoru.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="f3a2e-106">Šajā piemērā tiek izveidots konfigurēšanas pakalpojuma sniedzējs parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurēšanas pakalpojuma sniedzēji ir kopīgi visiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="f3a2e-107">Nodrošinātāja izveide</span><span class="sxs-lookup"><span data-stu-id="f3a2e-107">Create a provider</span></span>
1. <span data-ttu-id="f3a2e-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f3a2e-109">Noklikšķiniet uz Konfigurācijas nodrošinātāji.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="f3a2e-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-110">Click New.</span></span>
    * <span data-ttu-id="f3a2e-111">Nodrošinātāja ierakstam ir unikāls nosaukums un URL.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="f3a2e-112">Pārskatiet šīs lapas saturu un izlaidiet šo procedūru, ja “Litware, Inc.” (http://www.litware.com) ieraksts jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="f3a2e-113">Laukā Nosaukums ierakstiet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="f3a2e-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="f3a2e-115">Laukā Interneta adrese ierakstiet “http://www.litware.com”.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * http://www.litware.com  
6. <span data-ttu-id="f3a2e-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-116">Click Save.</span></span>
7. <span data-ttu-id="f3a2e-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="f3a2e-118">Atlasiet kā aktīvu nodrošinātāju</span><span class="sxs-lookup"><span data-stu-id="f3a2e-118">Select as an active provider</span></span>
1. <span data-ttu-id="f3a2e-119">Atlasiet pakalpojumu sniedzēju Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="f3a2e-120">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="f3a2e-120">Click Set active.</span></span>


