--- 
title: "Konfigurācijas nodrošinātāja izveidei un kā aktīva atzīmēšana elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot konfigurācijas nodrošinātāju Elektroniskajos pārskatos (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 018aee917c13f576759ebd812d31cbc9d83e2d1a
ms.contentlocale: lv-lv
ms.lasthandoff: 02/23/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="26f47-103">Konfigurācijas nodrošinātāja izveidei un kā aktīva atzīmēšana elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="26f47-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26f47-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot konfigurācijas nodrošinātāju Elektroniskajos pārskatos (ER).</span><span class="sxs-lookup"><span data-stu-id="26f47-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="26f47-105">Katra ER konfigurācija atsauksies uz nodrošinātāju kā konfigurācijas autoru.</span><span class="sxs-lookup"><span data-stu-id="26f47-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="26f47-106">Šajā piemērā tiek izveidots konfigurēšanas pakalpojuma sniedzējs parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurēšanas pakalpojuma sniedzēji ir kopīgi visiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="26f47-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="26f47-107">Nodrošinātāja izveide</span><span class="sxs-lookup"><span data-stu-id="26f47-107">Create a provider</span></span>
1. <span data-ttu-id="26f47-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="26f47-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="26f47-109">Noklikšķiniet uz Konfigurācijas nodrošinātāji.</span><span class="sxs-lookup"><span data-stu-id="26f47-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="26f47-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="26f47-110">Click New.</span></span>
    * <span data-ttu-id="26f47-111">Nodrošinātāja ierakstam ir unikāls nosaukums un URL.</span><span class="sxs-lookup"><span data-stu-id="26f47-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="26f47-112">Pārskatiet šīs lapas saturu un izlaidiet šo procedūru, ja “Litware, Inc.” (`http://www.litware.com`) ieraksts jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="26f47-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="26f47-113">Laukā Nosaukums ierakstiet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="26f47-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="26f47-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="26f47-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="26f47-115">Laukā Interneta adrese ierakstiet `http://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="26f47-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="26f47-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="26f47-116">Click Save.</span></span>
7. <span data-ttu-id="26f47-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="26f47-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="26f47-118">Atlasiet kā aktīvu nodrošinātāju</span><span class="sxs-lookup"><span data-stu-id="26f47-118">Select as an active provider</span></span>
1. <span data-ttu-id="26f47-119">Atlasiet pakalpojumu sniedzēju Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="26f47-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="26f47-120">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="26f47-120">Click Set active.</span></span>


