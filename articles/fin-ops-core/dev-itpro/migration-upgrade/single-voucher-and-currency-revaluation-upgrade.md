---
title: Vienotu dokumentu žurnālu un valūtas pārvērtēšanu jaunināšana
description: Šajā tēmā aprakstīts, kā jaunināt vienotu dokumentu žurnālu un valūtas pārvērtēšanu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3504c01a4ed1571866fd2a0cd83eef86a57d684a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127307"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="c553e-103">Vienotu dokumentu žurnālu un valūtas pārvērtēšanu jaunināšana</span><span class="sxs-lookup"><span data-stu-id="c553e-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c553e-104">Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="c553e-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="c553e-105">Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="c553e-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="c553e-106">Veiciet šīs darbības, jauninot uz Microsoft Dynamics 365 for Operations versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="c553e-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="c553e-107">Pirms veicat jaunināšanu uz programmu Finance and Operations, izpildiet ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="c553e-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="c553e-108">Laukā **Metode** iestatiet vienumu **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="c553e-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="c553e-109">Tiek izveidota pārvērtēšanas darbība, kas atceļ pēdējo ārvalstu valūtas pārvērtēšanu.</span><span class="sxs-lookup"><span data-stu-id="c553e-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="c553e-110">Tādējādi atvērtās darbības tiek vērtētas pēc to sākotnējās uzskaites valūtas.</span><span class="sxs-lookup"><span data-stu-id="c553e-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="c553e-111">Jauniniet uz versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="c553e-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="c553e-112">Vēlreiz izpildiet ārvalstu valūtas pārvērtēšanu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="c553e-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="c553e-113">Šoreiz laukā **Metode** iestatiet vienumu **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="c553e-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="c553e-114">Tiek izveidota jauna pārvērtēšanas darbība, kas ir balstīta uz pašreizējiem maiņas kursiem.</span><span class="sxs-lookup"><span data-stu-id="c553e-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="c553e-115">Ar šo darbību tiek ierakstīta nerealizētā peļņa/zaudējumi un pareizais Virsgrāmatas kopsavilkuma konts.</span><span class="sxs-lookup"><span data-stu-id="c553e-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>
