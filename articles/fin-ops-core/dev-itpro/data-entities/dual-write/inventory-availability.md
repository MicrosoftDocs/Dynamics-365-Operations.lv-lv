---
title: Krājumu pieejamība duālajā ierakstā
description: Šajā tēmā ir sniegta informācija par to, kā pārbaudīt krājumu pieejamību duālajā ierakstā.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997896"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="b7017-103">Krājumu pieejamība duālajā ierakstā</span><span class="sxs-lookup"><span data-stu-id="b7017-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b7017-104">Izmantojot krājumu pieejamību, varat pārbaudīt krājumus pirms preču pievienošanas lapā **Piedāvājumi** , **Pasūtījumi** vai **Rēķini** programmā Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b7017-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations** , **Orders** , or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="b7017-105">Piemēram, krājumu pārbaude un izpildes datuma noteikšana ir galvenais uzdevums procesā [no potenciālā klienta līdz skaidrai naudai](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="b7017-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="b7017-106">Ja nav pietiekami daudz krājumu, varat aplēst piegādes datumu, pamatojoties uz prognozēto krājumu saņemšanas un izsniegšanas plūsmām.</span><span class="sxs-lookup"><span data-stu-id="b7017-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="b7017-107">Varat arī pārbaudīt preces pieejams solīšanai (ATP) informāciju, kur varat atrast ATP daudzumu iepriekš definētā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="b7017-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="b7017-108">Rīcībā esošie krājumi</span><span class="sxs-lookup"><span data-stu-id="b7017-108">On-hand inventory</span></span>

<span data-ttu-id="b7017-109">Dynamics 365 Sales **Piedāvājumi** , **Pasūtījumi** vai **Rēķini** lapu galvenē ir pievienota jauna poga **Rīcībā esošie krājumi**.</span><span class="sxs-lookup"><span data-stu-id="b7017-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="b7017-110">Atlasot šo pogu, parādās dialoglodziņš, kur varat norādīt uzņēmumu un preci, kurai vēlaties pārbaudīt rīcībā esošos krājumus.</span><span class="sxs-lookup"><span data-stu-id="b7017-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="b7017-111">Šis dialoglodziņš parāda to pašu informāciju, ko [rīcībā esošie krājumi](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="b7017-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="b7017-112">Dialoglodziņā tiek atgriezta informācija par krājumiem no Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b7017-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b7017-113">Šajā informācijā ir iekļauti tālāk norādītie daudzumi:</span><span class="sxs-lookup"><span data-stu-id="b7017-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="b7017-114">Rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-114">On-hand quantity</span></span>
- <span data-ttu-id="b7017-115">Rezervētais rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="b7017-116">Pieejamais rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-116">Available on-hand quantity</span></span>
- <span data-ttu-id="b7017-117">Pasūtītais daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-117">Ordered quantity</span></span>
- <span data-ttu-id="b7017-118">Pasūtījumā iekļautais daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-118">On-order quantity</span></span>
- <span data-ttu-id="b7017-119">Rezervētais pasūtītais daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="b7017-120">Kopējais pieejamais daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="b7017-121">ATP informācija</span><span class="sxs-lookup"><span data-stu-id="b7017-121">ATP information</span></span>

<span data-ttu-id="b7017-122">Programmā Sales ir pievienota jauna **ATP informācija** , kas ir pievienota rindas precēm **Piedāvājumu** , **Pasūtījumu** un **Rēķinu** lapās.</span><span class="sxs-lookup"><span data-stu-id="b7017-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="b7017-123">Atlasot šo pogu, parādās dialoglodziņš, kur varat norādīt uzņēmumu, preci, krājuma atrašanās vietu, krājuma noliktavu un krājumu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="b7017-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="b7017-124">Šim dialoglodziņam ir tie paši iestatījumi, kas aprakstīti [Pasūtījumu solīšanā](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="b7017-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="b7017-125">Dialoglodziņā tiek atgriezta ATP informācija no Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b7017-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="b7017-126">Šajā informācijā ir iekļauti tālāk norādītie daudzumi:</span><span class="sxs-lookup"><span data-stu-id="b7017-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="b7017-127">ATP daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-127">ATP quantity</span></span>
- <span data-ttu-id="b7017-128">Ieejas plūsmas daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-128">Receipt quantity</span></span>
- <span data-ttu-id="b7017-129">Izejas plūsmas daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-129">Issue quantity</span></span>
- <span data-ttu-id="b7017-130">Rīcībā esošais daudzums</span><span class="sxs-lookup"><span data-stu-id="b7017-130">On-hand quantity</span></span>
