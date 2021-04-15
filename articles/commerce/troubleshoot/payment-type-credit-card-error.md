---
title: Pārdošanas pasūtījuma lapā maksājuma veidam jābūt kredītkartes kļūdai
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad pēc pasūtījuma sinhronizācijas pārdošanas pasūtījuma lapā tiek parādīts kļūdas paziņojums.
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
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801679"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="31b48-103">Pārdošanas pasūtījuma lapā "maksājuma veidam jābūt kredītkartes kļūdai"</span><span class="sxs-lookup"><span data-stu-id="31b48-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31b48-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad pēc pasūtījuma sinhronizācijas pārdošanas pasūtījuma lapā tiek parādīts kļūdas paziņojums.</span><span class="sxs-lookup"><span data-stu-id="31b48-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="31b48-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="31b48-105">Description</span></span>

<span data-ttu-id="31b48-106">Kad pēc pasūtījuma sinhronizēšanas atverat pārdošanas pasūtījuma lapu, tiek saņemts šāds kļūdas ziņojums: "Maksājuma veidam jābūt kredītkartei, jo ir norādīts kredītkartes numurs."</span><span class="sxs-lookup"><span data-stu-id="31b48-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Maksājuma veidam jābūt kredītkartes kļūdai](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="31b48-108">Novēršana</span><span class="sxs-lookup"><span data-stu-id="31b48-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="31b48-109">Iestatīt maksājuma veidu programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="31b48-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="31b48-110">Pārejiet uz sadaļu **Debitori \> Maksājumu iestatījumi \> Apmaksas nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="31b48-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="31b48-111">Navigācijas kreisajā pusē atlasiet apmaksas nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="31b48-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="31b48-112">Laukā **Maksājuma veids** pārliecinieties, ka ir atlasīta **Kredītkarte**.</span><span class="sxs-lookup"><span data-stu-id="31b48-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31b48-113">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="31b48-113">Additional resources</span></span>

[<span data-ttu-id="31b48-114">Tiešsaistes pārdošanas un maksājumu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="31b48-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)
