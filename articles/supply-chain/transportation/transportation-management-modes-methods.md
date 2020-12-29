---
title: Transportēšanas pārvaldības veidi un metodes
description: Šajā tēmā parādīts, kā iestatīt Transportēšanas pārvaldības režīmus un metodes.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: ceb3930cdb7764f846e88edfff6906b902a7f5fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2020
ms.locfileid: "4433243"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="ee42b-103">Transportēšanas pārvaldības veidi un metodes</span><span class="sxs-lookup"><span data-stu-id="ee42b-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee42b-104">Transportēšanas pārvaldības režīms atspoguļo transporta veidu, ko pārvadātājs izmanto kravas piegādēm, piemēram, mazākām par slodzi (LTL) kravas slodzes lielumā (TL) vai pasta sūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="ee42b-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="ee42b-105">Transportēšanas metode atspoguļo transporta formu, ko pārvadātājs izmanto kravas piegādēm, piemēram, piegāde pa gaisu, zemi, ūdeni vai dzelzceļu.</span><span class="sxs-lookup"><span data-stu-id="ee42b-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="ee42b-106">Režīmi un transportēšanas metodes tiek izmantotas vairākos kontekstos.</span><span class="sxs-lookup"><span data-stu-id="ee42b-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="ee42b-107">Maršruta plānos tiek izmantoti tikai režīmi, bet, iestatot nosūtīšanas pārvadātājus un pārvadātāju pakalpojumus, tiek izmantoti abi režīmi un transportēšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="ee42b-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="ee42b-108">Nav nevienas tiešas attiecības vai hierarhijas starp režīmiem un transportēšanas metodēm.</span><span class="sxs-lookup"><span data-stu-id="ee42b-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="ee42b-109">Režīma izveide</span><span class="sxs-lookup"><span data-stu-id="ee42b-109">Create a mode</span></span>

<span data-ttu-id="ee42b-110">Lai izveidotu režīmu, veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="ee42b-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="ee42b-111">Pārejiet uz sadaļu **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Režīms**.</span><span class="sxs-lookup"><span data-stu-id="ee42b-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="ee42b-112">Atlasiet **Jauns**, lai izveidotu jaunu režīmu.</span><span class="sxs-lookup"><span data-stu-id="ee42b-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="ee42b-113">Ievadiet režīmam unikālu ID un aprakstošu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ee42b-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="ee42b-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ee42b-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="ee42b-115">Transportēšanas metodes izveide</span><span class="sxs-lookup"><span data-stu-id="ee42b-115">Create a transportation method</span></span>

<span data-ttu-id="ee42b-116">Lai izveidotu transportēšanas metodi, veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="ee42b-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="ee42b-117">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Transportēšanas metodes**.</span><span class="sxs-lookup"><span data-stu-id="ee42b-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="ee42b-118">Atlasiet **Jauns**, lai izveidotu jaunus transportēšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="ee42b-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="ee42b-119">Ievadiet transportēšanas metodei unikālu ID un aprakstošu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ee42b-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="ee42b-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ee42b-120">Close the page.</span></span>
