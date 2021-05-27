---
title: Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu
description: Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kura var rasties, sinhronizējot tiešsaistes pasūtījumu.
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021131"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="d1af8-103">Pasūtījumu sinhronizācijas kļūda saistībā ar noklusējuma maksājumu pakalpojumu</span><span class="sxs-lookup"><span data-stu-id="d1af8-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1af8-104">Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt novērst kļūdu, kura var rasties, sinhronizējot tiešsaistes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="d1af8-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="d1af8-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d1af8-105">Description</span></span>

<span data-ttu-id="d1af8-106">Kad sinhronizējat tiešsaistes pasūtījumu, tiek saņemts šāds kļūdas ziņojums: "Lai apstrādātu kredītkartes darījumu, ir nepieciešams noklusējuma maksājumu pakalpojums."</span><span class="sxs-lookup"><span data-stu-id="d1af8-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Neesoša noklusējuma maksājumu pakalpojuma kļūda](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="d1af8-108">Novēršana</span><span class="sxs-lookup"><span data-stu-id="d1af8-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="d1af8-109">Noklusējuma maksājumu pakalpojuma apstiprināšana vai iestatīšana programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="d1af8-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="d1af8-110">Lai apstiprinātu vai iestatītu noklusējuma maksājumu pakalpojumu programmā Commerce Headquarters, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="d1af8-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d1af8-111">Pārejiet uz sadaļu **Debitoru parādi \> Maksājumu iestatīšana \> Maksājumu pakalpojumi**.</span><span class="sxs-lookup"><span data-stu-id="d1af8-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="d1af8-112">Pārliecinieties, ka opcija **Noklusējuma apstrādātājs jaunām kredītkartēm** ir iestatīts uz **Jā** vienam maksājumu pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="d1af8-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1af8-113">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d1af8-113">Additional resources</span></span>

[<span data-ttu-id="d1af8-114">Kredītkartes iestatīšana, autorizēšana un nolasīšana</span><span class="sxs-lookup"><span data-stu-id="d1af8-114">Credit card setup, authorization, and capture</span></span>](../../finance/accounts-receivable/credit-card-authorizations.md)