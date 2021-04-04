---
title: Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu
description: Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kura var rasties, sinhronizējot tiešsaistes pasūtījumu.
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585423"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="a5279-103">Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu</span><span class="sxs-lookup"><span data-stu-id="a5279-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5279-104">Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kura var rasties, sinhronizējot tiešsaistes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a5279-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="a5279-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a5279-105">Description</span></span>

<span data-ttu-id="a5279-106">Kad sinhronizējat tiešsaistes pasūtījumu, tiek saņemts šāds kļūdas ziņojums: "Lai apstrādātu kredītkartes darījumu, ir nepieciešams noklusējuma maksājumu pakalpojums."</span><span class="sxs-lookup"><span data-stu-id="a5279-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Neesoša noklusējuma maksājumu pakalpojuma kļūda](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="a5279-108">Novēršana</span><span class="sxs-lookup"><span data-stu-id="a5279-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="a5279-109">Noklusējuma maksājumu pakalpojuma apstiprināšana vai iestatīšana programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="a5279-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="a5279-110">Lai apstiprinātu vai iestatītu noklusējuma maksājumu pakalpojumu programmā Commerce Headquarters, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="a5279-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a5279-111">Pārejiet uz sadaļu **Debitoru parādi \> Maksājumu iestatīšana \> Maksājumu pakalpojumi**.</span><span class="sxs-lookup"><span data-stu-id="a5279-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="a5279-112">Pārliecinieties, ka opcija **Noklusējuma apstrādātājs jaunām kredītkartēm** ir iestatīts uz **Jā** vienam maksājumu pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="a5279-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5279-113">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a5279-113">Additional resources</span></span>

[<span data-ttu-id="a5279-114">Kredītkartes iestatīšana, autorizēšana un nolasīšana</span><span class="sxs-lookup"><span data-stu-id="a5279-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
