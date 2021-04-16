---
title: Iekļaut fizisko vērtību
description: Lapas Krājumu modeļu grupas kopsavilkuma cilnes Krājumu modelis izvēles rūtiņu Iekļaut fizisko vērtību izmanto, lai norādītu, vai fiziski atjauninātas transakcijas tiek ņemtas vērā, aprēķinot krājuma faktisko vidējo izmaksu cenu.
author: AndersGirke
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ab5ecc74d41610098bf927fc4768bc216e42f4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816680"
---
# <a name="include-physical-value"></a><span data-ttu-id="5ddf4-103">Iekļaut fizisko vērtību</span><span class="sxs-lookup"><span data-stu-id="5ddf4-103">Include physical value</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ddf4-104">Lapas Krājumu modeļu grupas kopsavilkuma cilnes Krājumu modelis izvēles rūtiņu Iekļaut fizisko vērtību izmanto, lai norādītu, vai fiziski atjauninātas transakcijas tiek ņemtas vērā, aprēķinot krājuma faktisko vidējo izmaksu cenu.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="5ddf4-105">Izvēles rūtiņā **Iekļaut fizisko vērtību** ir pieejamas tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="5ddf4-106">Vērtība</span><span class="sxs-lookup"><span data-stu-id="5ddf4-106">Value</span></span>    | <span data-ttu-id="5ddf4-107">Rezultāts</span><span class="sxs-lookup"><span data-stu-id="5ddf4-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ddf4-108">Atlasīts</span><span class="sxs-lookup"><span data-stu-id="5ddf4-108">Selected</span></span> | <span data-ttu-id="5ddf4-109">Gan fiziski, gan finansiāli atjauninātās transakcijas izmanto faktisko vidējo izmaksu cenas aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="5ddf4-110">Notīrīts</span><span class="sxs-lookup"><span data-stu-id="5ddf4-110">Cleared</span></span>  | <span data-ttu-id="5ddf4-111">Lai aprēķinātu faktisko vidējo izmaksu cenu, izmanto tikai finansiāli atjauninātās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="5ddf4-112">Izvēles rūtiņai atkarībā no izmantotā krājumu modeļa ir nedaudz atšķirīga funkcija.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="5ddf4-113">Ja, izmantojot FIFO (pirmais iekšā, pirmais ārā) LIFO (pēdējais iekšā, pirmais ārā) vai LIFO datuma krājumu modeli, ir atlasīta izvēles rūtiņa **Iekļaut fizisko vērtību**, krājumu slēgšana gadījumā tiek veiktas fiziski atjaunināto transakciju korekcijas.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="5ddf4-114">Ja, izmantojot šos krājumu modeļus, izvēles rūtiņa **Iekļaut fizisko vērtību** netiek atlasīta, krājumu slēgšanas gadījumā tiek nosegtas tikai finansiāli atjauninātās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="5ddf4-115">Ja tiek izmantots svērtā vidējā vai svērtā vidējā datuma krājuma modelis, krājumu slēgšana sedz tikai finansiāli atjauninātās transakcijas neatkarīgi no tā, vai izvēles rūtiņa **Iekļaut fizisko vērtību** ir atlasīta vai nē.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="5ddf4-116">**1. piemērs.** Izvēles rūtiņa **Iekļaut fizisko vērtību** ir atlasīta, un ir saņemti tālāk norādītie pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="5ddf4-117">Pirkšanas pasūtījums par 2 vienību daudzumu un izmaksu cenu USD 10,00, kura pavadzīme ir atjaunināta.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated.</span></span>
-   <span data-ttu-id="5ddf4-118">Pirkšanas pasūtījums par 3 vienību daudzumu un izmaksu cenu USD 12,00, kura rēķins ir atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated.</span></span>

<span data-ttu-id="5ddf4-119">Šajā gadījumā faktiskā vidējā izmaksu cena ir USD 11,20 = (2x10+3x12)/(2+3), jo gan fiziski, gan finansiāli atjauninātās transakcijas ir izmantotas izmaksu cenas aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-119">In this case, the running average cost price will be USD 11.20 = (2x10+3x12)/(2+3), because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> 

<span data-ttu-id="5ddf4-120">**2. piemērs.** Izvēles rūtiņa **Iekļaut fizisko vērtību** nav atlasīta, un izmaksu cena krājumu iestatījumā ir USD 10,00.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> 

-   <span data-ttu-id="5ddf4-121">Tiek saņemts pirkšanas pasūtījums par 20 vienību daudzumu un izmaksu cenu USD 12,00, kura pavadzīme ir atjaunināta.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span>

<span data-ttu-id="5ddf4-122">Kad pārdošanas pasūtījums ir iegrāmatots, iegrāmatotā izmaksu summa ir USD 10,00, jo faktiskā vidējā izmaksu cena neiekļauj fiziski iegrāmatotās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ddf4-123">Salīdzinājumam — ja, iegrāmatojot pārdošanas pasūtījumu, izvēles rūtiņa **Iekļaut fizisko vērtību** šim krājumam ir atlasīta, iegrāmatoto izmaksu summa ir USD 12,00.</span><span class="sxs-lookup"><span data-stu-id="5ddf4-123">For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]