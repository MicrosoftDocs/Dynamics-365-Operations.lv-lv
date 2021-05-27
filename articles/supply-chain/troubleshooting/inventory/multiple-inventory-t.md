---
title: Vairāki krājumu darījumi partiju numuriem, kad tiek atspējots fiziskais labojums
description: Vairāki krājumu darījumi tiek izveidoti pēc pirkšanas pasūtījuma rindas pielāgošanas krājumiem, kuru partijas numura grupas fiziskās atjaunināšanas opcija ir iestatīta uz Nē.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026725"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="211ae-103">Vairāki krājumu darījumi partiju numuriem, kad tiek atspējots fiziskais labojums</span><span class="sxs-lookup"><span data-stu-id="211ae-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="211ae-104">KB numurs: 4613390</span><span class="sxs-lookup"><span data-stu-id="211ae-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="211ae-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="211ae-105">Symptoms</span></span>

<span data-ttu-id="211ae-106">Vairāki krājumu darījumi tiek izveidoti pēc pirkšanas pasūtījuma rindas pielāgošanas krājumiem, kuru partijas numura grupas **Fiziskās atjaunināšanas** opcija ir iestatīta uz *Nē*.</span><span class="sxs-lookup"><span data-stu-id="211ae-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="211ae-107">Izveidojot krājumu, kura partijas numuru grupas **fiziskās atjaunināšanas** opcija ir iestatīta uz *Nē*, sistēma automātiski izveido jaunu partijas numuru, ja modificējat pirkšanas rindas daudzumu un saglabājat pirkšanas pasūtījuma lapu.</span><span class="sxs-lookup"><span data-stu-id="211ae-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="211ae-108">Novēršana</span><span class="sxs-lookup"><span data-stu-id="211ae-108">Resolution</span></span>

<span data-ttu-id="211ae-109">**Fiziskās atjaunināšanas** iestatījums numuru grupām darbojas šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="211ae-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="211ae-110">Kad opcija ir iestatīta uz *Jā*, jauni partijas numuri tiek izveidoti tikai pēc fiziskās atjaunināšanas (piemēram, kad preces tiek sūtītas vai saņemtas).</span><span class="sxs-lookup"><span data-stu-id="211ae-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="211ae-111">Kad opcija ir iestatīta uz *Nē*, jauns partijas numurs tiek izveidots katru reizi, kad notiek piemērojama atjaunināšana (piemēram, kad pirkšanas pasūtījumam tiek pievienots jauns daudzums).</span><span class="sxs-lookup"><span data-stu-id="211ae-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
