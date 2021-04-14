---
title: Vienotu dokumentu žurnālu un valūtas pārvērtēšanu jaunināšana
description: Šajā tēmā aprakstīts, kā jaunināt vienotu dokumentu žurnālu un valūtas pārvērtēšanu.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6b66b969d13cff7f1f39fb644f459aa92bea198f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743925"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="52187-103">Vienotu dokumentu žurnālu un valūtas pārvērtēšanu jaunināšana</span><span class="sxs-lookup"><span data-stu-id="52187-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52187-104">Dažas organizācijas ievada žurnālus, kuros ir viens dokuments, kurā ir vairāk nekā viens debitors vai kreditors, un tās arī izpilda ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="52187-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="52187-105">Šajā tēmā ir aprakstītas darbības, kuras šīm organizācijām jāveic, jauninot uz Microsoft Dynamics 365 for Operations programmas versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="52187-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="52187-106">Veiciet šīs darbības, jauninot uz Microsoft Dynamics 365 for Operations versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="52187-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="52187-107">Pirms veicat jaunināšanu uz programmu Finance and Operations, izpildiet ārvalstu valūtas pārvērtēšanas procesu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="52187-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="52187-108">Laukā **Metode** iestatiet vienumu **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="52187-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="52187-109">Tiek izveidota pārvērtēšanas darbība, kas atceļ pēdējo ārvalstu valūtas pārvērtēšanu.</span><span class="sxs-lookup"><span data-stu-id="52187-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="52187-110">Tādējādi atvērtās darbības tiek vērtētas pēc to sākotnējās uzskaites valūtas.</span><span class="sxs-lookup"><span data-stu-id="52187-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="52187-111">Jauniniet uz versiju 1611.</span><span class="sxs-lookup"><span data-stu-id="52187-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="52187-112">Vēlreiz izpildiet ārvalstu valūtas pārvērtēšanu debitoru un kreditoru parādiem.</span><span class="sxs-lookup"><span data-stu-id="52187-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="52187-113">Šoreiz laukā **Metode** iestatiet vienumu **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="52187-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="52187-114">Tiek izveidota jauna pārvērtēšanas darbība, kas ir balstīta uz pašreizējiem maiņas kursiem.</span><span class="sxs-lookup"><span data-stu-id="52187-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="52187-115">Ar šo darbību tiek ierakstīta nerealizētā peļņa/zaudējumi un pareizais Virsgrāmatas kopsavilkuma konts.</span><span class="sxs-lookup"><span data-stu-id="52187-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]