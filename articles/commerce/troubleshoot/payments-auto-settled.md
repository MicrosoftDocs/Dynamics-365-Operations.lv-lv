---
title: Maksājumi tiek automātiski segti pirms pasūtījumu rēķinu izrakstīšanas vai nosūtīšanas
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad maksājums tiek apmaksāts Adyen portālā nekavējoties pēc pasūtījuma veikšanas pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018264"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="b4fbc-103">Maksājumi tiek automātiski segti pirms pasūtījumu rēķinu izrakstīšanas vai nosūtīšanas</span><span class="sxs-lookup"><span data-stu-id="b4fbc-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4fbc-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad maksājums tiek apmaksāts Adyen portālā nekavējoties pēc pasūtījuma veikšanas pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.</span><span class="sxs-lookup"><span data-stu-id="b4fbc-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="b4fbc-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b4fbc-105">Description</span></span>

<span data-ttu-id="b4fbc-106">Kad pasūtījums tiek veikts, maksājums tiek nekavējoties apmaksāts Adyen portālā pat tad, ja pārdošanas pasūtījums nav iekļauts rēķinā vai nosūtīts.</span><span class="sxs-lookup"><span data-stu-id="b4fbc-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="b4fbc-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="b4fbc-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="b4fbc-108">Manuālas e-komercijas maksājumu tveršanas konfigurēšana Adyen portālā</span><span class="sxs-lookup"><span data-stu-id="b4fbc-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="b4fbc-109">Lai konfigurētu manuālu e-komercijas maksājumu tveršanu Adyen portālā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b4fbc-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="b4fbc-110">Pierakstieties Adyen portālā.</span><span class="sxs-lookup"><span data-stu-id="b4fbc-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="b4fbc-111">Augšējā labajā stūrī atlasiet savu tirgotāja kontu e-komercijas kanālam.</span><span class="sxs-lookup"><span data-stu-id="b4fbc-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="b4fbc-112">Augšējā navigācijā atlasiet **Konts** un pēc tam atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="b4fbc-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="b4fbc-113">Laukā **Tveršanas aizkave** atlasiet **manuāli**.</span><span class="sxs-lookup"><span data-stu-id="b4fbc-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Tveršanas aizkaves iestatīšana Adyen portālā](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="b4fbc-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b4fbc-115">Additional resources</span></span>

[<span data-ttu-id="b4fbc-116">Adyen maksājumu tveršana</span><span class="sxs-lookup"><span data-stu-id="b4fbc-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="b4fbc-117">Dynamics 365 maksājumu savienotājs pakalpojumam Adyen</span><span class="sxs-lookup"><span data-stu-id="b4fbc-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="b4fbc-118">Adyen maksājumu savienotāja iestatīšana risinājumam Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b4fbc-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
