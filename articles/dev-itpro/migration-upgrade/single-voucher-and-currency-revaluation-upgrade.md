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
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b76354d0b8bb89e09e861e013a0c680c36b6537d
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851685"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="71795-104">Vienotu dokumentu žurnālu un valūtas pārvērtēšanu jaunināšana</span><span class="sxs-lookup"><span data-stu-id="71795-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71795-105">Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="71795-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="71795-106">Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="71795-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="71795-107">Veiciet šīs darbības, jauninot uz Microsoft Dynamics 365 for Operations versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="71795-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="71795-108">Pirms veicat jaunināšanu uz programmu Dynamics 365 for Operations, izpildiet ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="71795-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="71795-109">Laukā **Metode** iestatiet vienumu **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="71795-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="71795-110">Tiek izveidota pārvērtēšanas darbība, kas atceļ pēdējo ārvalstu valūtas pārvērtēšanu.</span><span class="sxs-lookup"><span data-stu-id="71795-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="71795-111">Tādējādi atvērtās darbības tiek vērtētas pēc to sākotnējās uzskaites valūtas.</span><span class="sxs-lookup"><span data-stu-id="71795-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="71795-112">Jauniniet uz Dynamics 365 for Operations versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="71795-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="71795-113">Vēlreiz izpildiet ārvalstu valūtas pārvērtēšanu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="71795-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="71795-114">Šoreiz laukā **Metode** iestatiet vienumu **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="71795-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="71795-115">Tiek izveidota jauna pārvērtēšanas darbība, kas ir balstīta uz pašreizējiem maiņas kursiem.</span><span class="sxs-lookup"><span data-stu-id="71795-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="71795-116">Ar šo darbību tiek ierakstīta nerealizētā peļņa/zaudējumi un pareizais Virsgrāmatas kopsavilkuma konts.</span><span class="sxs-lookup"><span data-stu-id="71795-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>




