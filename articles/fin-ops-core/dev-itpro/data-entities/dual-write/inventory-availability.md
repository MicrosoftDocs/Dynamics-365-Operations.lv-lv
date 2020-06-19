---
title: Krājumu pieejamība duālajā ierakstā
description: Šajā tēmā ir sniegta informācija par krājumu pieejamības pārbaudi duālajā ierakstā.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426986"
---
# <a name="inventory-availability"></a><span data-ttu-id="da2b1-103">Krājumu pieejamība</span><span class="sxs-lookup"><span data-stu-id="da2b1-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="da2b1-104">Izmantojot krājumu pieejamību, varat pārbaudīt krājumus pirms preču pievienošanas veidlapās **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** no modeļa atkarīgās programmās Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="da2b1-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="da2b1-105">Piemēram, krājumu pārbaude un izpildes datuma noteikšana ir galvenais uzdevums procesā [no potenciālā klienta līdz skaidrai naudai](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="da2b1-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="da2b1-106">Ja nav pietiekami daudz krājumu, varat aplēst piegādes datumu, pamatojoties uz prognozēto krājumu saņemšanas un izsniegšanas plūsmām.</span><span class="sxs-lookup"><span data-stu-id="da2b1-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="da2b1-107">Varat arī pārbaudīt preces pieejams solīšanai (ATP) informāciju, kur varat atrast ATP daudzumu iepriekš definētā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="da2b1-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="da2b1-108">Rīcībā esošie krājumi</span><span class="sxs-lookup"><span data-stu-id="da2b1-108">On-hand Inventory</span></span> 

<span data-ttu-id="da2b1-109">Dynamics 365 Sales veidlapu **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** galvenē ir pievienota jauna poga **Rīcībā esošie krājumi**.</span><span class="sxs-lookup"><span data-stu-id="da2b1-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="da2b1-110">Noklikšķinot uz pogas, parādās dialoglodziņš, un varat norādīt uzņēmumu un preci, kurai vēlaties pārbaudīt rīcībā esošos krājumus.</span><span class="sxs-lookup"><span data-stu-id="da2b1-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="da2b1-111">Tiek atgriezta informācija par krājumu no Dynamics 365 Supply Chain Management un parādīta tā pati informācija, kas sadaļā [Rīcībā esošie krājumi](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="da2b1-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="da2b1-112">Informācija ietver tālāk minētos daudzumus.</span><span class="sxs-lookup"><span data-stu-id="da2b1-112">The information includes these quantities:</span></span>

- <span data-ttu-id="da2b1-113">**Rīcībā esošais daudzums**</span><span class="sxs-lookup"><span data-stu-id="da2b1-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="da2b1-114">**Rezervētais rīcībā esošais daudzums**</span><span class="sxs-lookup"><span data-stu-id="da2b1-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="da2b1-115">**Pieejamais rīcībā esošais daudzums**</span><span class="sxs-lookup"><span data-stu-id="da2b1-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="da2b1-116">**Pasūtītais daudzums**</span><span class="sxs-lookup"><span data-stu-id="da2b1-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="da2b1-117">**Pasūtījumā iekļautais daudzums**</span><span class="sxs-lookup"><span data-stu-id="da2b1-117">**On-order Quantity**</span></span>
- <span data-ttu-id="da2b1-118">**Rezervētais pasūtītais daudzums**</span><span class="sxs-lookup"><span data-stu-id="da2b1-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="da2b1-119">**Kopējais pieejamais daudzums**</span><span class="sxs-lookup"><span data-stu-id="da2b1-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="da2b1-120">ATP informācija</span><span class="sxs-lookup"><span data-stu-id="da2b1-120">ATP information</span></span>

<span data-ttu-id="da2b1-121">Dynamics 365 Sales veidlapu **Piedāvājumi**, **Pasūtījumi** vai **Rēķini** rindas krājumos ir pievienota jauna poga **ATP informācija**.</span><span class="sxs-lookup"><span data-stu-id="da2b1-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="da2b1-122">Noklikšķinot uz pogas, parādās dialoglodziņš, un varat norādīt uzņēmumu, preci, krājuma atrašanās vietu, krājuma noliktavu un krājumu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="da2b1-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="da2b1-123">Tiek atgriezta **ATP informācija** no Supply Chain Management un tiek parādīti iestatījumi, kas aprakstīti [Pasūtījumu solīšana](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="da2b1-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="da2b1-124">Informācijā ir ietverts **ATP daudzums**, **Ieejas plūsmas daudzums**, **Izejas plūsmas daudzums** un **Rīcībā esošais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="da2b1-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
