---
title: Pamatlīdzekļa iegādes priekšlikums
description: Šī procedūra parāda, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1891206bb266b126eccfa789b8c8062c9bfa688b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570884"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="0e3d2-103">Pamatlīdzekļa iegādes priekšlikums</span><span class="sxs-lookup"><span data-stu-id="0e3d2-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e3d2-104">Šī procedūra parāda, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="0e3d2-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="0e3d2-106">Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="0e3d2-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-107">Click New.</span></span>
3. <span data-ttu-id="0e3d2-108">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="0e3d2-109">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-109">Click Lines.</span></span>
5. <span data-ttu-id="0e3d2-110">Noklikšķiniet uz Priekšlikumi.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-110">Click Proposals.</span></span>
6. <span data-ttu-id="0e3d2-111">Noklikšķiniet uz Pirkšanas priekšlikums.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="0e3d2-112">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-112">Click Filter.</span></span>
8. <span data-ttu-id="0e3d2-113">Noklikšķiniet uz Atiestatīt un iztīrīt iepriekšējās vērtības.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="0e3d2-114">Atlasiet rindu Pamatlīdzekļa numurs.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="0e3d2-115">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="0e3d2-116">Iestatiet atlikušos kritērijus pamatlīdzekļiem, kurus vēlaties iegūt, izmantojot šo priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="0e3d2-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-117">Click OK.</span></span>
12. <span data-ttu-id="0e3d2-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-118">Click OK.</span></span>
    * <span data-ttu-id="0e3d2-119">Pārbaudiet izveidotās transakcijas rindas.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="0e3d2-120">Tikai pamatlīdzekļi ar iegādes datumu un iegādes cenu, kas ir iestatīta grāmatā, tiks iekļauti iegādes priekšlikumā.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="0e3d2-121">Noklikšķiniet uz cilnes Grāmatas.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-121">Click the Books tab.</span></span>
14. <span data-ttu-id="0e3d2-122">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="0e3d2-122">Click Post.</span></span>

