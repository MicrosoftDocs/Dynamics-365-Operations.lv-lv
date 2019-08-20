---
title: Iestatīt pamatlīdzekļu grupas
description: Šajā procedūrā parādīts, kā izveidot jaunu pamatlīdzekļu grupu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f52b73c07aad1047d6e6e7caf80daecc9c26e7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839789"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="d3d6b-103">Iestatīt pamatlīdzekļu grupas</span><span class="sxs-lookup"><span data-stu-id="d3d6b-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3d6b-104">Šajā procedūrā parādīts, kā izveidot jaunu pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="d3d6b-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="d3d6b-106">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu grupas.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="d3d6b-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-107">Click New.</span></span>
3. <span data-ttu-id="d3d6b-108">Ierakstiet vērtību laukā Pamatlīdzekļu grupa.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="d3d6b-109">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d3d6b-110">Automātiska pamatlīdzekļu numerācija un Numuru sērijas kodu izmantošana pamatlīdzekļu grupai ignorē pamatlīdzekļu parametru iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="d3d6b-111">Ja šīs pamatlīdzekļu grupas līdzekļiem tiks izmantota no citām grupām atšķirīga numerācija, jūs varat to mainīt šeit.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="d3d6b-112">Noklikšķiniet uz Grāmatas.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-112">Click Books.</span></span>
6. <span data-ttu-id="d3d6b-113">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d3d6b-114">Lauka Aprēķināt nolietojumu vērtība ir iestatīta uz Jā, tāpēc līdzekļu grāmata tiek iekļauta nolietojuma piedāvājumos.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="d3d6b-115">Ja vienums Aprēķināt nolietojumu ir iestatīts ar opciju Nē, līdzeklis netiek automātiski norakstīts.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="d3d6b-116">Iestatiet līdzekļa lietošanas ilgumu gados.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="d3d6b-117">Ņemiet vērā, ka lauka Nolietojuma periodi vērtība tiek aprēķināta pēc vērtības Lietošanas ilgums iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="d3d6b-118">Atlasiet opciju laukā Nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="d3d6b-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-119">Close the page.</span></span>

