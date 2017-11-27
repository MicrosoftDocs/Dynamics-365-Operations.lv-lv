---
title: "Viena dokumenta un valūtas pārvērtēšanas jauninājums"
description: "Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem. Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e0cd0c96ad0f30d56eefdc46a0a69160d864175
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="f1487-104">Viena dokumenta un valūtas pārvērtēšanas jauninājums</span><span class="sxs-lookup"><span data-stu-id="f1487-104">Single voucher and currency revaluation upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f1487-105">Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="f1487-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="f1487-106">Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="f1487-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="f1487-107">Veiciet šīs darbības, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="f1487-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="f1487-108">Pirms veicat jaunināšanu uz programmu Dynamics 365 for Operations, izpildiet ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="f1487-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="f1487-109">Laukā **Metode** iestatiet vienumu **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="f1487-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="f1487-110">Tiek izveidota pārvērtēšanas darbība, kas atceļ pēdējo ārvalstu valūtas pārvērtēšanu.</span><span class="sxs-lookup"><span data-stu-id="f1487-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="f1487-111">Tādējādi atvērtās darbības tiek vērtētas pēc to sākotnējās uzskaites valūtas.</span><span class="sxs-lookup"><span data-stu-id="f1487-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="f1487-112">Jauniniet uz Dynamics 365 for Operations versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="f1487-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="f1487-113">Vēlreiz izpildiet ārvalstu valūtas pārvērtēšanu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="f1487-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="f1487-114">Šoreiz laukā **Metode** iestatiet vienumu **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="f1487-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="f1487-115">Tiek izveidota jauna pārvērtēšanas darbība, kas ir balstīta uz pašreizējiem maiņas kursiem.</span><span class="sxs-lookup"><span data-stu-id="f1487-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="f1487-116">Ar šo darbību tiek ierakstīta nerealizētā peļņa/zaudējumi un pareizais Virsgrāmatas kopsavilkuma konts.</span><span class="sxs-lookup"><span data-stu-id="f1487-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





