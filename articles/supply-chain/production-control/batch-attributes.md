---
title: Partijas atribūti
description: Šajā tēmā ir sniegta informācija par partijas atribūtiem. Partijas atribūti ir krājumu partijās ietverto izejvielu un saražoto preču raksturlielumi. Tēmā ir arī paskaidrots, kā piešķirt partijas atribūtus un kā tos izmantot meklēšanai, rezervējot partijas.
author: ShylaThompson
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370893e415a79091404f1c4eb0404ba8fd5b9ff2
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433128"
---
# <a name="batch-attributes"></a><span data-ttu-id="3ff10-105">Partijas atribūti</span><span class="sxs-lookup"><span data-stu-id="3ff10-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ff10-106">Šajā tēmā ir sniegta informācija par partijas atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="3ff10-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="3ff10-107">Partijas atribūti ir krājumu partijās ietverto izejvielu un saražoto preču raksturlielumi.</span><span class="sxs-lookup"><span data-stu-id="3ff10-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="3ff10-108">Tēmā ir arī paskaidrots, kā piešķirt partijas atribūtus un kā tos izmantot meklēšanai, rezervējot partijas.</span><span class="sxs-lookup"><span data-stu-id="3ff10-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="3ff10-109">Partijas atribūti ir krājumu partijās ietverto izejvielu un saražoto preču raksturlielumi.</span><span class="sxs-lookup"><span data-stu-id="3ff10-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="3ff10-110">Partijas atribūti var atšķirties atkarībā no tādiem faktoriem kā vides apstākļi, partijas ražošanai izmantoto izejmateriālu kvalitāte vai saražotās preces rezultāta.</span><span class="sxs-lookup"><span data-stu-id="3ff10-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="3ff10-111">Izmantoto partijas atribūtu skaits un veidi var būtiski atšķirties atkarībā no nozares.</span><span class="sxs-lookup"><span data-stu-id="3ff10-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="3ff10-112">Tālāk ir sniegti divi partijas atribūtu izmantošanas piemēri.</span><span class="sxs-lookup"><span data-stu-id="3ff10-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="3ff10-113">Siera ražošanas nozarē pienam, kas ir viens no siera ražošanas izejmateriāliem, var būt tādi atribūti kā tauku saturs un procentuālais svars.</span><span class="sxs-lookup"><span data-stu-id="3ff10-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="3ff10-114">No piena saražotajam sieram var būt citi atribūti, piemēram, mitrums un noturēšanas ilgums.</span><span class="sxs-lookup"><span data-stu-id="3ff10-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="3ff10-115">Tērauda ražošanas nozarē saražotajai dzelzij var būt tādi atribūti kā magnija saturs procentos, sudraba saturs procentos un cinka saturs procentos.</span><span class="sxs-lookup"><span data-stu-id="3ff10-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="3ff10-116">Lai labāk pārvaldītu atribūtu skaitu un veidus, varat izmantot partijas atribūtu grupas.</span><span class="sxs-lookup"><span data-stu-id="3ff10-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="3ff10-117">Tādējādi nav jāpievieno katrs atribūts atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="3ff10-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="3ff10-118">Partijas atribūtu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="3ff10-118">Assign batch attributes</span></span>
<span data-ttu-id="3ff10-119">Varat piešķirt partijas atribūtus atsevišķām precēm, kas ir ietvertas krājumu partijās, vai precēm, kas ir saistītas ar noteiktiem debitoriem.</span><span class="sxs-lookup"><span data-stu-id="3ff10-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="3ff10-120">Pirms partijas atribūta piešķiršanas debitora līmenī, tas ir jāpiešķir preces līmenī.</span><span class="sxs-lookup"><span data-stu-id="3ff10-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="3ff10-121">Precei izsekošanas dimensiju grupā ir jāiestata partijas dimensijas opcija **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="3ff10-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="3ff10-122">Lai piešķirtu partijas atribūtu atsevišķai precei, izmantojiet šīs preces lapu.</span><span class="sxs-lookup"><span data-stu-id="3ff10-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="3ff10-123">Ja atribūts ir raksturīgs noteiktam debitoram paredzētai precei, izmantojiet attiecīgā debitora lapu.</span><span class="sxs-lookup"><span data-stu-id="3ff10-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="3ff10-124">Pievienojot precei atribūtu, jūs definējat arī citus parametrus.</span><span class="sxs-lookup"><span data-stu-id="3ff10-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="3ff10-125">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="3ff10-125">Here are some examples:</span></span>

-   <span data-ttu-id="3ff10-126">Minimālās un maksimālās vērtības diapazons atribūtam, kura tips ir **Vesels skaitlis** vai **Daļskaitlis**.</span><span class="sxs-lookup"><span data-stu-id="3ff10-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="3ff10-127">Pielaides darbības atribūtam, kura tips ir **Vesels skaitlis** vai **Daļskaitlis**.</span><span class="sxs-lookup"><span data-stu-id="3ff10-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="3ff10-128">Ja atribūta vērtība ir ārpus minimālās un maksimālās vērtības diapazona, tad šī darbība var būt brīdinājuma vai kļūdas ziņojuma parādīšana.</span><span class="sxs-lookup"><span data-stu-id="3ff10-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="3ff10-129">Atribūta mērķa vērtība.</span><span class="sxs-lookup"><span data-stu-id="3ff10-129">The target value for the attribute.</span></span> <span data-ttu-id="3ff10-130">Tā ir atribūta optimālā vērtība un attiecas uz visiem atribūtu tipiem.</span><span class="sxs-lookup"><span data-stu-id="3ff10-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="3ff10-131">To preču lapām, kuras atlasāt lapā **Izlaistās preces**, varat piekļūt modulī Preču informācijas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="3ff10-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="3ff10-132">Pēc partijas atribūtu piešķiršanas precei varat pievienot atribūtiem noteiktas vērtības lapā **Krājumu partijas atribūti**.</span><span class="sxs-lookup"><span data-stu-id="3ff10-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="3ff10-133">Partiju rezervēšana</span><span class="sxs-lookup"><span data-stu-id="3ff10-133">Reserve batches</span></span>
<span data-ttu-id="3ff10-134">Rezervējat partijas pārdošanas pasūtījumam, lai izpildītu debitora pasūtījumu, vai kad izdodot un rezervējot partijas ražošanas pasūtījumam, varat meklēt partijas pēc partijas atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="3ff10-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="3ff10-135">Meklēšana palīdz atrast krājumu partiju, kurā ir ietverta prece, kurai ir vajadzīgais partijas atribūts.</span><span class="sxs-lookup"><span data-stu-id="3ff10-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="3ff10-136">Kad esat atradis partiju vai partijas, varat rezervēt preci izcelsmes noliktavas transakcijas rindā.</span><span class="sxs-lookup"><span data-stu-id="3ff10-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>



