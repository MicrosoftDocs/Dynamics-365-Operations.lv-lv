---
title: "Iekļaut fizisko vērtību"
description: "Lapas Krājumu modeļu grupas kopsavilkuma cilnes Krājumu modelis izvēles rūtiņu Iekļaut fizisko vērtību izmanto, lai norādītu, vai fiziski atjauninātas transakcijas tiek ņemtas vērā, aprēķinot krājuma faktisko vidējo izmaksu cenu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fa59031ed2144c2e92399933cd5dd40bfca0f2ae
ms.contentlocale: lv-lv
ms.lasthandoff: 07/18/2017

---

# <a name="include-physical-value"></a><span data-ttu-id="ef43a-103">Iekļaut fizisko vērtību</span><span class="sxs-lookup"><span data-stu-id="ef43a-103">Include physical value</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ef43a-104">Lapas Krājumu modeļu grupas kopsavilkuma cilnes Krājumu modelis izvēles rūtiņu Iekļaut fizisko vērtību izmanto, lai norādītu, vai fiziski atjauninātas transakcijas tiek ņemtas vērā, aprēķinot krājuma faktisko vidējo izmaksu cenu.</span><span class="sxs-lookup"><span data-stu-id="ef43a-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="ef43a-105">Izvēles rūtiņā **Iekļaut fizisko vērtību** ir pieejamas tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="ef43a-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="ef43a-106">Vērtība</span><span class="sxs-lookup"><span data-stu-id="ef43a-106">Value</span></span>    | <span data-ttu-id="ef43a-107">Rezultāts</span><span class="sxs-lookup"><span data-stu-id="ef43a-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef43a-108">Atlasīts</span><span class="sxs-lookup"><span data-stu-id="ef43a-108">Selected</span></span> | <span data-ttu-id="ef43a-109">Gan fiziski, gan finansiāli atjauninātās transakcijas izmanto faktisko vidējo izmaksu cenas aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="ef43a-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="ef43a-110">Notīrīts</span><span class="sxs-lookup"><span data-stu-id="ef43a-110">Cleared</span></span>  | <span data-ttu-id="ef43a-111">Lai aprēķinātu faktisko vidējo izmaksu cenu, izmanto tikai finansiāli atjauninātās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="ef43a-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="ef43a-112">Izvēles rūtiņai atkarībā no izmantotā krājumu modeļa ir nedaudz atšķirīga funkcija.</span><span class="sxs-lookup"><span data-stu-id="ef43a-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="ef43a-113">Ja, izmantojot FIFO (pirmais iekšā, pirmais ārā) LIFO (pēdējais iekšā, pirmais ārā) vai LIFO datuma krājumu modeli, ir atlasīta izvēles rūtiņa **Iekļaut fizisko vērtību**, krājumu slēgšana gadījumā tiek veiktas fiziski atjaunināto transakciju korekcijas.</span><span class="sxs-lookup"><span data-stu-id="ef43a-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="ef43a-114">Ja, izmantojot šos krājumu modeļus, izvēles rūtiņa **Iekļaut fizisko vērtību** netiek atlasīta, krājumu slēgšanas gadījumā tiek nosegtas tikai finansiāli atjauninātās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="ef43a-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="ef43a-115">Ja tiek izmantots svērtā vidējā vai svērtā vidējā datuma krājuma modelis, krājumu slēgšana sedz tikai finansiāli atjauninātās transakcijas neatkarīgi no tā, vai izvēles rūtiņa **Iekļaut fizisko vērtību** ir atlasīta vai nē.</span><span class="sxs-lookup"><span data-stu-id="ef43a-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="ef43a-116">**1. piemērs.** Izvēles rūtiņa**Iekļaut fizisko vērtību** ir atlasīta, un ir saņemti tālāk norādītie pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="ef43a-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="ef43a-117">Pirkšanas pasūtījums par 2 vienību daudzumu un izmaksu cenu USD 10,00, kura pavadzīme ir atjaunināta.</span><span class="sxs-lookup"><span data-stu-id="ef43a-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="ef43a-118">Pirkšanas pasūtījums par 3 vienību daudzumu un izmaksu cenu USD 12,00, kura rēķins ir atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="ef43a-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="ef43a-119">Šajā gadījumā faktiskā vidējā izmaksu cena ir USD 11,20, jo gan fiziski, gan finansiāli atjauninātās transakcijas ir izmantotas izmaksu cenas aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="ef43a-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="ef43a-120">**2. piemērs.** Izvēles rūtiņa **Iekļaut fizisko vērtību** nav atlasīta, un izmaksu cena krājumu iestatījumā ir USD 10,00.</span><span class="sxs-lookup"><span data-stu-id="ef43a-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="ef43a-121">Tiek saņemts pirkšanas pasūtījums par 20 vienību daudzumu un izmaksu cenu USD 12,00, kura pavadzīme ir atjaunināta.</span><span class="sxs-lookup"><span data-stu-id="ef43a-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="ef43a-122">Kad pārdošanas pasūtījums ir iegrāmatots, iegrāmatotā izmaksu summa ir USD 10,00, jo faktiskā vidējā izmaksu cena neiekļauj fiziski iegrāmatotās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="ef43a-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="ef43a-123">**Piezīme.** Salīdzinājumam — ja, iegrāmatojot pārdošanas pasūtījumu, izvēles rūtiņa **Iekļaut fizisko vērtību** šim krājumam ir atlasīta, iegrāmatoto izmaksu summa ir USD 12,00.</span><span class="sxs-lookup"><span data-stu-id="ef43a-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>




