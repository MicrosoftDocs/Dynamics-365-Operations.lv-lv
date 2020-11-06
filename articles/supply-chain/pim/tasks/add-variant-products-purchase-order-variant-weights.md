---
title: Variantu preču pievienošana pirkšanas pasūtījumiem, izmantojot variantu svaru
description: Šajā procedūrā ir aprakstīts, kā jāizmanto svaru varianti, lai automātiski aizpildītu pirkšanas pasūtījuma rindas katram preces variantam.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27ff3784074a36d073930ba68c8dec8b1121356e
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018288"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="c5066-103">Variantu preču pievienošana pirkšanas pasūtījumiem, izmantojot variantu svaru</span><span class="sxs-lookup"><span data-stu-id="c5066-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5066-104">Šajā procedūrā ir aprakstīts, kā jāizmanto svaru varianti, lai automātiski aizpildītu pirkšanas pasūtījuma rindas katram preces variantam.</span><span class="sxs-lookup"><span data-stu-id="c5066-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="c5066-105">Atlasot preces daudzumu, ko vēlaties iegādāties, pirkšanas pasūtījuma rindas tiek izveidotas visiem preces variantiem, izmantojot ieteicamās daudzuma vērtības, pamatojoties uz svaru, kas konfigurēts preces variantos.</span><span class="sxs-lookup"><span data-stu-id="c5066-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="c5066-106">Šajā procedūrā netiek veiktas svara vērtību konfigurēšanas darbības preču dimensijās un preces variantos.</span><span class="sxs-lookup"><span data-stu-id="c5066-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="c5066-107">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="c5066-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c5066-108">Pārejiet uz sadaļu Kreditori > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="c5066-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="c5066-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c5066-109">Click New.</span></span>
3. <span data-ttu-id="c5066-110">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c5066-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c5066-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c5066-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c5066-112">Pārslēdziet sadaļas Vispārīgi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="c5066-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="c5066-113">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c5066-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c5066-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c5066-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c5066-115">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c5066-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c5066-116">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c5066-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c5066-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c5066-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="c5066-118">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="c5066-118">Click OK.</span></span>
12. <span data-ttu-id="c5066-119">Pārslēdziet sadaļas Detalizēta rindas informācija paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="c5066-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="c5066-120">Noklikšķiniet uz cilnes Varianti.</span><span class="sxs-lookup"><span data-stu-id="c5066-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="c5066-121">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="c5066-121">Click Add line.</span></span>
15. <span data-ttu-id="c5066-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c5066-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="c5066-123">Laukā Krājuma kods ierakstiet 0140.</span><span class="sxs-lookup"><span data-stu-id="c5066-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="c5066-124">Daudzuma laukā iestatiet vērtību 1000.</span><span class="sxs-lookup"><span data-stu-id="c5066-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="c5066-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c5066-125">Click Save.</span></span>

