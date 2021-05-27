---
title: Kredītkartes ievades lapa izrakstīšanās laikā rāda kļūdu
description: Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja maksājuma metodes sadaļa netiek ielādēta un rāda kļūdas ziņojumu.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018510"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="8c16d-103">Kredītkartes ievades lapa izrakstīšanās laikā rāda kļūdu</span><span class="sxs-lookup"><span data-stu-id="8c16d-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c16d-104">Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja **Maksājuma metodes** sadaļa netiek ielādēta un rāda kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="8c16d-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="8c16d-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="8c16d-105">Description</span></span>

<span data-ttu-id="8c16d-106">Atverot tiešsaistes veikala izrakstīšanās lapu, netiek ielādēta sadaļa **Maksājuma metode** un tiek rādīts kļūdas ziņojums: "Kaut kas neizdevās.</span><span class="sxs-lookup"><span data-stu-id="8c16d-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="8c16d-107">Lūdzu, vēlāk mēģiniet vēlreiz.”</span><span class="sxs-lookup"><span data-stu-id="8c16d-107">Please try again later."</span></span>

![Maksājumu moduļa kļūda](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="8c16d-109">Novēršana</span><span class="sxs-lookup"><span data-stu-id="8c16d-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="8c16d-110">Pagaidiet, kamēr beidzas Commerce Scale Unit kešdarbes termiņš</span><span class="sxs-lookup"><span data-stu-id="8c16d-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="8c16d-111">Maksājumu pakalpojumu iestatījumi tiešsaistes veikala izrakstīšanās lapā tiek glabāti Commerce Scale Unit un var paiet līdz 15 minūtēm, iekams tie parādās e-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="8c16d-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="8c16d-112">Šie maksājumu pakalpojuma iestatījumi ietver izmaiņas pārdevēja konta ID, mākoņu API atslēgā un dažādos konfigurācijas iestatījumos, kas ir saistīti ar maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="8c16d-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c16d-113">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8c16d-113">Additional resources</span></span>

[<span data-ttu-id="8c16d-114">Tiešsaistes kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8c16d-114">Set up an online channel</span></span>](../channel-setup-online.md)
