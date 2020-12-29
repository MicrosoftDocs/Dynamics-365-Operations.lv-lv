---
title: Krājumu etiķešu inventarizācija
description: Šajā tēmā ir sniegta informācija par etiķešu uzskaiti, kuru izmantojat, lai noliktavas faktisko saturu salīdzinātu ar rīcībā esošajiem krājumiem.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb555cdfbcf3fd0c10ec0e2abcdbe7f4a90d82d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432534"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="00102-103">Krājumu etiķešu inventarizācija</span><span class="sxs-lookup"><span data-stu-id="00102-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00102-104">Šajā tēmā ir sniegta informācija par etiķešu uzskaiti, kuru izmantojat, lai noliktavas faktisko saturu salīdzinātu ar rīcībā esošajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="00102-104">This topic provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="00102-105">Izveidojot rindas lapā **Etiķešu skaitīšana**, katrai krājuma vienībai tiek piešķirts etiķetes numurs, piemēram, skaitlis no 1 līdz 500.</span><span class="sxs-lookup"><span data-stu-id="00102-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="00102-106">Inventarizācijas laikā jūs ievadāt krājuma numuru un daudzumu, kas ir norādīts attiecīgajā etiķetē.</span><span class="sxs-lookup"><span data-stu-id="00102-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="00102-107">Šo etiķeti pēc tam var izmantot par pamatu ievadei etiķešu inventarizācijas žurnālā.</span><span class="sxs-lookup"><span data-stu-id="00102-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="00102-108">Pēc etiķešu inventarizācijas žurnāla grāmatošanas lapā **Inventarizācija** tiek izveidots jauns inventarizācijas žurnāls.</span><span class="sxs-lookup"><span data-stu-id="00102-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="00102-109">Jaunais žurnāls balstās uz etiķešu inventarizācijas žurnāla rindām, kuras izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="00102-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="00102-110">Lai veiktu krājumu etiķešu uzskaiti pēc noteiktas krājumu dimensijas, atlasiet dimensiju lapā **Parādīt dimensijas**, kas tiek parādīta, izveidojot etiķešu inventarizācijas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="00102-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="00102-111">Piemēram, lai saskaitītu krājumus noteiktā noliktavā, atzīmējiet izvēles rūtiņu **Noliktava**.</span><span class="sxs-lookup"><span data-stu-id="00102-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="00102-112">Ja ir atlasīts slīdnis **Bloķēt krājumus inventarizācijas laikā** lapā **Krājumu un noliktavas pārvaldības parametri**, krājumus nevar fiziski atjaunināt inventarizācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="00102-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="00102-113">Tomēr krājumi etiķešu inventarizācijas žurnālos inventarizācijas laikā nav bloķēti.</span><span class="sxs-lookup"><span data-stu-id="00102-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="00102-114">Krājumu darbības netiek veidotas, kamēr etiķešu inventarizācijas žurnāla rindas nav grāmatotas un pārsūtītas uz inventarizācijas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="00102-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="00102-115">Ja etiķetes tiek ievadītas izlases veidā un jūs vēlaties noteikt trūkstošās etiķetes, noklikšķiniet uz kolonnas virsraksta **Etiķete**, lai kārtotu rindas pēc etiķetes.</span><span class="sxs-lookup"><span data-stu-id="00102-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00102-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="00102-116">Additional resources</span></span>

[<span data-ttu-id="00102-117">Cikla inventarizācija</span><span class="sxs-lookup"><span data-stu-id="00102-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
