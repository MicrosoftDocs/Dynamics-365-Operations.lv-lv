---
title: Netiek rādīta opcija Saglabāt manam nākamajam maksājumam
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad e-komercijas vietnes norēķinu lapā zem maksāšanas metodes netiek parādīta izvēles rūtiņa Saglabāt manam nākamajam maksājumam.
author: Reza-Assadi
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
ms.openlocfilehash: 7e3156d1aa9a05dc5d159b6f9b33ae341de640bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801703"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="a7aab-103">Netiek rādīta opcija "Saglabāt manam nākamajam maksājumam"</span><span class="sxs-lookup"><span data-stu-id="a7aab-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7aab-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad e-komercijas vietnes norēķinu lapā zem **Maksāšanas metodes** netiek parādīta izvēles rūtiņa **Saglabāt manam nākamajam maksājumam**.</span><span class="sxs-lookup"><span data-stu-id="a7aab-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="a7aab-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a7aab-105">Description</span></span>

<span data-ttu-id="a7aab-106">E-komercijas vietnes norēķinu lapas sadaļā **Maksājuma metode** netiek parādīta izvēles rūtiņa **Saglabāt manam nākamajam maksājumam**.</span><span class="sxs-lookup"><span data-stu-id="a7aab-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="a7aab-107">Attēlāzemāk parādīts norēķinu lapas piemērs, kurā ir iekļauta izvēles rūtiņa **Saglabāt manam nākamajam maksājumam**.</span><span class="sxs-lookup"><span data-stu-id="a7aab-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Izvēles rūtiņa Saglabāt manam nākamajam maksājumam Maksājumu modulī](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="a7aab-109">Novēršana</span><span class="sxs-lookup"><span data-stu-id="a7aab-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="a7aab-110">Pārbaudīšana, vai programmā Commerce Headquarters ir pareizi konfigurēts Dynamics 365 Payment Connector for Adyen</span><span class="sxs-lookup"><span data-stu-id="a7aab-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="a7aab-111">Lai pārbaudītu, vai programmā Commerce Headquarters ir pareizi konfigurēts Dynamics 365 Payment Connector for Adyen, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a7aab-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a7aab-112">Pārejiet uz sadaļu **Mazumtirdzniecība un tirdzniecība \> Kanāli \> Tiešsaistes veikali**.</span><span class="sxs-lookup"><span data-stu-id="a7aab-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="a7aab-113">Atlasiet tiešsaistes veikalu.</span><span class="sxs-lookup"><span data-stu-id="a7aab-113">Select the online store.</span></span>
1. <span data-ttu-id="a7aab-114">Kopsavilkuma cilnē **Maksājumu konti** pārliecinieties, vai lauka **Atļaut saglabāt maksājuma informāciju e-komercijā** vērtība ir iestatīta uz **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="a7aab-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Atļaut saglabāt maksājuma informāciju e-kommercijas laukā programmā Commerce Headquarters](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="a7aab-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a7aab-116">Additional resources</span></span>

[<span data-ttu-id="a7aab-117">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="a7aab-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="a7aab-118">Tiešsaistes maksājumu instrumentu saglabāšana, izmantojot savienotāju Adyen</span><span class="sxs-lookup"><span data-stu-id="a7aab-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
