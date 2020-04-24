---
title: Pirkšanas pasūtījuma izveide vienreizējam piegādātājam
description: Šajā procedūrā ir parādīts, kā izveidot pirkšanas pasūtījumu vienreizējam piegādātājam.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76915772809d736cac9e8a9439d9e693a4490eec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204911"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="be13e-103">Pirkšanas pasūtījuma izveide vienreizējam piegādātājam</span><span class="sxs-lookup"><span data-stu-id="be13e-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be13e-104">Šajā procedūrā ir parādīts, kā izveidot pirkšanas pasūtījumu vienreizējam piegādātājam.</span><span class="sxs-lookup"><span data-stu-id="be13e-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="be13e-105">Piegādātājs tiek automātiski izveidots ar pirkšanas pasūtījumu, nevis kreditora konts ir jāizveido manuāli.</span><span class="sxs-lookup"><span data-stu-id="be13e-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="be13e-106">Pirkuma pasūtījumu parasti veic iepirkuma aģenti.</span><span class="sxs-lookup"><span data-stu-id="be13e-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="be13e-107">Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="be13e-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="be13e-108">Pastāv priekšnosacījums, kas vienreizējā kreditora kontam ir jābūt iestatītam lapā Kreditoru parametri.</span><span class="sxs-lookup"><span data-stu-id="be13e-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="be13e-109">Pirkšanas pasūtījuma izveide vienreizējam piegādātājam</span><span class="sxs-lookup"><span data-stu-id="be13e-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="be13e-110">Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="be13e-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="be13e-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="be13e-111">Click New.</span></span>
3. <span data-ttu-id="be13e-112">Atlasiet Jā laukā Vienreizējs piegādātājs.</span><span class="sxs-lookup"><span data-stu-id="be13e-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="be13e-113">Kreditora konts tiek automātiski izveidots un piešķirts pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="be13e-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="be13e-114">Kreditora konts tiek izveidots, pamatojoties uz veidni, kas ir norādīta kreditoru parametru lapas cilnē Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="be13e-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="be13e-115">Laukā Nosaukums ierakstiet nosaukumu šim piegādātājam.</span><span class="sxs-lookup"><span data-stu-id="be13e-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="be13e-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="be13e-116">Click OK.</span></span>
    * <span data-ttu-id="be13e-117">Pirkšanas pasūtījumu tagad var pabeigt un apstrādāt tāpat kā jebkuru citu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="be13e-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="be13e-118">Ar veidu, kā tas tiek darīts, nav saistīta neviena izteikta īpašība.</span><span class="sxs-lookup"><span data-stu-id="be13e-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="be13e-119">Rēķins ņems vērā veicamu transakciju uz kreditora kontu, kas tika izveidota ar šo pasūtījumu, un pēc tam tiks apstrādāts maksājums.</span><span class="sxs-lookup"><span data-stu-id="be13e-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

