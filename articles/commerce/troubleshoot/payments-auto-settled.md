---
title: Maksājumi tiek automātiski segti pirms pasūtījumu rēķinu izrakstīšanas vai nosūtīšanas
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad maksājums tiek apmaksāts Adyen portālā nekavējoties pēc pasūtījuma veikšanas pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585429"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="bff4a-103">Maksājumi tiek automātiski segti pirms pasūtījumu rēķinu izrakstīšanas vai nosūtīšanas</span><span class="sxs-lookup"><span data-stu-id="bff4a-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bff4a-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad maksājums tiek apmaksāts Adyen portālā nekavējoties pēc pasūtījuma veikšanas pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.</span><span class="sxs-lookup"><span data-stu-id="bff4a-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="bff4a-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="bff4a-105">Description</span></span>

<span data-ttu-id="bff4a-106">Kad pasūtījums tiek veikts, maksājums tiek nekavējoties apmaksāts Adyen portālā pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.</span><span class="sxs-lookup"><span data-stu-id="bff4a-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="bff4a-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="bff4a-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="bff4a-108">Manuālas e-komercijas maksājumu tveršanas konfigurēšana Adyen portālā</span><span class="sxs-lookup"><span data-stu-id="bff4a-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="bff4a-109">Lai konfigurētu manuālu e-komercijas maksājumu tveršanu Adyen portālā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="bff4a-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="bff4a-110">Pierakstieties Adyen portālā.</span><span class="sxs-lookup"><span data-stu-id="bff4a-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="bff4a-111">Augšējā labajā stūrī atlasiet savu tirgotāja kontu e-komercijas kanālam.</span><span class="sxs-lookup"><span data-stu-id="bff4a-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="bff4a-112">Augšējā navigācijā atlasiet **Konts** un pēc tam atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="bff4a-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="bff4a-113">Laukā **Tveršanas aizkave** atlasiet **manuāli**.</span><span class="sxs-lookup"><span data-stu-id="bff4a-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Tveršanas aizkaves iestatīšana Adyen portālā](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="bff4a-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bff4a-115">Additional resources</span></span>

[<span data-ttu-id="bff4a-116">Adyen maksājumu tveršana</span><span class="sxs-lookup"><span data-stu-id="bff4a-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="bff4a-117">Dynamics 365 maksājumu savienotājs pakalpojumam Adyen</span><span class="sxs-lookup"><span data-stu-id="bff4a-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="bff4a-118">Adyen maksājumu savienotāja iestatīšana risinājumam Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bff4a-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
