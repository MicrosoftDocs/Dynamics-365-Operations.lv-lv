---
title: Debitoru kredītu grupas
description: Šajā tēmā ir sniegta informācija par debitora kredītu grupu.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7121b78f3318bae9f82b2f0f951bc7bfe6c4358
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015311"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="3b99f-103">Debitoru kredītu grupas</span><span class="sxs-lookup"><span data-stu-id="3b99f-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3b99f-104">Varat definēt debitoru grupas, kurām ir vienāds kredīta limits.</span><span class="sxs-lookup"><span data-stu-id="3b99f-104">You can define groups of customers who have the same credit limit.</span></span> <span data-ttu-id="3b99f-105">Tiek apsvērts arī individuālais kredīta limits, kas noteikts debitora rēķina kontā.</span><span class="sxs-lookup"><span data-stu-id="3b99f-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="3b99f-106">Debitoru kredīta grupas dalībniekus var atlasīt no dažādām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="3b99f-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="3b99f-107">Kad jūs pievienojat debitoru debitoru kredīta grupas klientu sarakstam, katra debitora kredīta limita beigu datums tiek mainīts uz grupas piešķirto beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="3b99f-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="3b99f-108">Varat izveidot debitoru kredīta grupas lapā **Debitoru kredīta grupas** (**Kredīta pārvaldība \> Iestatījumi> Debitoru kredīta grupas \> Debitoru kredīta grupas**).</span><span class="sxs-lookup"><span data-stu-id="3b99f-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="3b99f-109">Laukos **Grupas numurs** un **Apraksts** ievadiet grupas identifikatoru un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="3b99f-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="3b99f-110">Laukos **Kredīta limits** un **Valūta** ievadiet kredīta limitu un valūtu, kas jālieto, kad sistēma pārbauda katra grupas locekļa kredīta limitu.</span><span class="sxs-lookup"><span data-stu-id="3b99f-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="3b99f-111">Laukā **Kredīta limita beigu datums** ievadiet datumu, kad kredīta limita termiņš beidzas.</span><span class="sxs-lookup"><span data-stu-id="3b99f-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="3b99f-112">Debitora kredīta grupām ir jābūt beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="3b99f-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="3b99f-113">Pēc debitora kredīta grupas iestatīšanas varat pievienot tai debitorus, norādot to juridisko personu un debitora konta ID.</span><span class="sxs-lookup"><span data-stu-id="3b99f-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="3b99f-114">Kad pievienojat debitora kredīta grupai jaunu debitoru, sistēma meklē vienu un to pašu debitora kontu visās juridiskajās personās un piedāvā to pievienot debitora kredīta grupai.</span><span class="sxs-lookup"><span data-stu-id="3b99f-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="3b99f-115">Izmantojiet izvēlni **Vecuma bilances**, lai skatītu detalizētu vecumstruktūru bilanču informāciju par visiem debitoru kredītu grupas rēķinu debitoriem.</span><span class="sxs-lookup"><span data-stu-id="3b99f-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="3b99f-116">Lapā **Vecumstruktūras bilance** tiek rādīts rēķina debitora kontu vecuma bilanču kopsavilkums.</span><span class="sxs-lookup"><span data-stu-id="3b99f-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
