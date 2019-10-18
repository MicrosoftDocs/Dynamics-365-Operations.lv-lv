---
title: Iestatīt pamatlīdzekļu grupas
description: Šajā tēmā ir paskaidrots, kā izveidot pamatlīdzekļu grupu.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 246502f66c0cfcd4b4ed3c4b9f2ae616e71a1c50
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186881"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="bf6fa-103">Iestatīt pamatlīdzekļu grupas</span><span class="sxs-lookup"><span data-stu-id="bf6fa-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bf6fa-104">Šajā tēmā ir paskaidrots, kā izveidot pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="bf6fa-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="bf6fa-106">Navigācijas rūtī ejiet uz **Moduļi > Pamatlīdzekļi > Iestatīšana> Pamatlīdzekļu grupas**.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="bf6fa-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-107">Select **New**.</span></span>
3. <span data-ttu-id="bf6fa-108">Laukā **Pamatlīdzekļu grupas** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="bf6fa-109">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="bf6fa-110">Pamatlīdzekļu automātiskā numurēšana un numuru secības kods grupā **Pamatlīdzekļi** ignorēs pamatlīdzekļu parametru iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="bf6fa-111">Ja šīs pamatlīdzekļu grupas līdzekļiem tiks izmantota no citām grupām atšķirīga numerācija, jūs varat to mainīt šeit.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="bf6fa-112">Atlasiet **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-112">Select **Books**.</span></span>
6. <span data-ttu-id="bf6fa-113">Laukā **Grāmata** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="bf6fa-114">Lauks **Aprēķināt nolietojumu** ir iestatīts uz **Jā**, tāpēc līdzekļu grāmata tiks iekļauta nolietojuma priekšlikumos.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="bf6fa-115">Ja lauks **Aprēķināt nolietojumu** ir iestatīts uz **Nē**, līdzeklis netiks automātiski nolietots.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="bf6fa-116">Iestatiet līdzekļa lietošanas ilgumu gados.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="bf6fa-117">Ņemiet vērā lauka **Nolietojuma periodi** vērtība tiek aprēķināta pēc servisa dzīves iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="bf6fa-118">Laukā **Nolietojuma vienošanās** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="bf6fa-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bf6fa-119">Close the page.</span></span>

