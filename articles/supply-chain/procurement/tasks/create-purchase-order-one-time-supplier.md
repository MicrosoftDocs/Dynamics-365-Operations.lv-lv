---
title: Pirkšanas pasūtījuma izveide vienreizējam piegādātājam
description: Šajā procedūrā ir parādīts, kā izveidot pirkšanas pasūtījumu vienreizējam piegādātājam.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: beaf6bcbc870e11e74289375611c631306545633
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "312880"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="18330-103">Pirkšanas pasūtījuma izveide vienreizējam piegādātājam</span><span class="sxs-lookup"><span data-stu-id="18330-103">Create a purchase order for a one-time supplier</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18330-104">Šajā procedūrā ir parādīts, kā izveidot pirkšanas pasūtījumu vienreizējam piegādātājam.</span><span class="sxs-lookup"><span data-stu-id="18330-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="18330-105">Piegādātājs tiek automātiski izveidots ar pirkšanas pasūtījumu, nevis kreditora konts ir jāizveido manuāli.</span><span class="sxs-lookup"><span data-stu-id="18330-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="18330-106">Pirkuma pasūtījumu parasti veic iepirkuma aģenti.</span><span class="sxs-lookup"><span data-stu-id="18330-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="18330-107">Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="18330-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="18330-108">Pastāv priekšnosacījums, kas vienreizējā kreditora kontam ir jābūt iestatītam lapā Kreditoru parametri.</span><span class="sxs-lookup"><span data-stu-id="18330-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="18330-109">Pirkšanas pasūtījuma izveide vienreizējam piegādātājam</span><span class="sxs-lookup"><span data-stu-id="18330-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="18330-110">Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="18330-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="18330-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="18330-111">Click New.</span></span>
3. <span data-ttu-id="18330-112">Atlasiet Jā laukā Vienreizējs piegādātājs.</span><span class="sxs-lookup"><span data-stu-id="18330-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="18330-113">Kreditora konts tiek automātiski izveidots un piešķirts pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="18330-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="18330-114">Kreditora konts tiek izveidots, pamatojoties uz veidni, kas ir norādīta kreditoru parametru lapas cilnē Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="18330-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="18330-115">Laukā Nosaukums ierakstiet nosaukumu šim piegādātājam.</span><span class="sxs-lookup"><span data-stu-id="18330-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="18330-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18330-116">Click OK.</span></span>
    * <span data-ttu-id="18330-117">Pirkšanas pasūtījumu tagad var pabeigt un apstrādāt tāpat kā jebkuru citu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="18330-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="18330-118">Ar veidu, kā tas tiek darīts, nav saistīta neviena izteikta īpašība.</span><span class="sxs-lookup"><span data-stu-id="18330-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="18330-119">Rēķins ņems vērā veicamu transakciju uz kreditora kontu, kas tika izveidota ar šo pasūtījumu, un pēc tam tiks apstrādāts maksājums.</span><span class="sxs-lookup"><span data-stu-id="18330-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="18330-120">Kad tas ir pabeigts, kreditora kontu var dzēst.</span><span class="sxs-lookup"><span data-stu-id="18330-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="18330-121">Parasti to dara kreditoru departaments.</span><span class="sxs-lookup"><span data-stu-id="18330-121">This is typically done by the accounts payable department.</span></span>  

