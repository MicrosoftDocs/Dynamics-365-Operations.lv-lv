---
title: Vispārējās plānošanas krājumus nevar filtrēt pēc to saistītajām vajadzību grupu vērtībām
description: Vispārējās plānošanas krājumus nevar filtrēt pēc to saistītajām vajadzību grupu vērtībām.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049479"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="ecbcb-103">Vispārējās plānošanas krājumus nevar filtrēt pēc to saistītajām vajadzību grupu vērtībām</span><span class="sxs-lookup"><span data-stu-id="ecbcb-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="ecbcb-104">KB numurs: 4612572</span><span class="sxs-lookup"><span data-stu-id="ecbcb-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="ecbcb-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="ecbcb-105">Symptoms</span></span>

<span data-ttu-id="ecbcb-106">Ir jāfiltrē krājumi, kas tiks iekļauti vispārējā plānošanas pakešuzdevumā, pamatojoties uz saistīto ierakstu vērtībām no krājumu vajadzības tabulas.</span><span class="sxs-lookup"><span data-stu-id="ecbcb-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="ecbcb-107">(Piemēram, jūs vēlaties filtrēt krājumus pēc to **Kreditora** un/vai **Vajadzības grupas** vērtības).</span><span class="sxs-lookup"><span data-stu-id="ecbcb-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="ecbcb-108">Pakešuzdevuma filtra iestatījumi ļauj izveidot savienojumu no tabulas **Krājumi** uz tabulu **Krājumu vajadzības**, un pēc tam vaicājumā norādīt lauku vērtības no krājumu vajadzību tabulas.</span><span class="sxs-lookup"><span data-stu-id="ecbcb-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="ecbcb-109">Tomēr pēc šī iestatījuma pabeigšanas sistēma vēl joprojām izveido plānotos pasūtījumus visam krājumu nodrošinājumam ne tikai krājumiem, kas atbilst norādītajām lauku vērtībām krājumu vajadzību tabulā.</span><span class="sxs-lookup"><span data-stu-id="ecbcb-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="ecbcb-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="ecbcb-110">Resolution</span></span>

<span data-ttu-id="ecbcb-111">Pakešuzdevumu filtrs var filtrēt tikai krājumiem.</span><span class="sxs-lookup"><span data-stu-id="ecbcb-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="ecbcb-112">Lai arī varat pievienot savienojumu **Krājumu vajadzību** tabulai, filtrēšanas iestatījumi, kurus šajā tabulā izveidojat, neietekmē vaicājuma izvadi.</span><span class="sxs-lookup"><span data-stu-id="ecbcb-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="ecbcb-113">Izpildlaikā sistēma palaiž plānošanu visām vajadzības grupām un visām variācijām, kas ir filtrētiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="ecbcb-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="ecbcb-114">Kad krājums jau ir iekļauts izpildē, visas vajadzības grupas, kas ir iekļautas krājumu filtrā, neietekmē plānošanas izvadi.</span><span class="sxs-lookup"><span data-stu-id="ecbcb-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
