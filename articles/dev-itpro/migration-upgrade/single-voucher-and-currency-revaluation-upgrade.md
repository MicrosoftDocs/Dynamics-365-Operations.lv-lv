---
title: Viena dokumenta žurnālu un valūtas pārvērtēšanas jaunināšana
description: Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem. Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554524"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="a1d11-104">Vienotu dokumentu žurnālu un valūtas pārvērtēšanu jaunināšana</span><span class="sxs-lookup"><span data-stu-id="a1d11-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1d11-105">Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="a1d11-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="a1d11-106">Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="a1d11-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="a1d11-107">Veiciet šīs darbības, jauninot uz Microsoft Dynamics 365 for Operations versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="a1d11-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="a1d11-108">Pirms veicat jaunināšanu uz programmu Dynamics 365 for Operations, izpildiet ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="a1d11-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="a1d11-109">Laukā **Metode** iestatiet vienumu **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="a1d11-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="a1d11-110">Tiek izveidota pārvērtēšanas darbība, kas atceļ pēdējo ārvalstu valūtas pārvērtēšanu.</span><span class="sxs-lookup"><span data-stu-id="a1d11-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="a1d11-111">Tādējādi atvērtās darbības tiek vērtētas pēc to sākotnējās uzskaites valūtas.</span><span class="sxs-lookup"><span data-stu-id="a1d11-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="a1d11-112">Jauniniet uz Dynamics 365 for Operations versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="a1d11-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="a1d11-113">Vēlreiz izpildiet ārvalstu valūtas pārvērtēšanu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="a1d11-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="a1d11-114">Šoreiz laukā **Metode** iestatiet vienumu **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="a1d11-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="a1d11-115">Tiek izveidota jauna pārvērtēšanas darbība, kas ir balstīta uz pašreizējiem maiņas kursiem.</span><span class="sxs-lookup"><span data-stu-id="a1d11-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="a1d11-116">Ar šo darbību tiek ierakstīta nerealizētā peļņa/zaudējumi un pareizais Virsgrāmatas kopsavilkuma konts.</span><span class="sxs-lookup"><span data-stu-id="a1d11-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>




