---
title: Uzlabota pēc partijas izsekoto krājumu apstrāde
description: Šajā tēmā ir aprakstīti uzlabojumi, kas ieviesti pēc partijas izsekoto krājumu apstrādē, kura tiek veikta pārskata grāmatošanas procesa laikā.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: ecff18f0a34d22ef359f473fa6aaaff16c811bb6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004209"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="91ac4-103">Uzlabota pēc partijas izsekoto krājumu apstrāde</span><span class="sxs-lookup"><span data-stu-id="91ac4-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="91ac4-104">Pārdošanas punktā (POS) nevar tvert partijas numurus pēc partijas izsekotajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="91ac4-104">In Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="91ac4-105">Tomēr attiecībā uz noteiktām konfigurācijām, ja galvenajā birojā pārdošana tiek grāmatota, izmantojot debitoru pasūtījumus vai grāmatojot pārskatu, sistēma Microsoft Dynamics sagaida, ka pastāv derīgi pēc partijas izsekoto krājumu partijas numuri un ka tie tiks izmantoti rēķinu izrakstīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="91ac4-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="91ac4-106">Ja precēm ir pieejami derīgi partijas numuri, tiek izmantots pārskatu grāmatošanas laikā veiktais debitora pasūtījumu rēķinu un pārdošanas pasūtījumu rēķinu izrakstīšanas process.</span><span class="sxs-lookup"><span data-stu-id="91ac4-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="91ac4-107">Citādi debitora pasūtījumu rēķinu izrakstīšanas procesu nevar grāmatot, un POS lietotājs saņem kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="91ac4-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="91ac4-108">Pēc tam pārskatu grāmatošanas procesam tiek aktivizēts kļūdas stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="91ac4-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="91ac4-109">Šis kļūdas stāvoklis rodas pat tad, ja precēm ir iespējoti negatīvi krājumi.</span><span class="sxs-lookup"><span data-stu-id="91ac4-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="91ac4-110">Ieviešot uzlabojumus programmā Retail 10.0.4 un jaunākās versijās, tika nodrošināts: ja pēc partijas izsekotiem krājumiem ir iespējoti negatīvie krājumi un krājuma daudzums ir 0 (nulle) vai nav pieejams partijas numurs, šiem krājumiem netiek bloķēta debitora pasūtījuma rēķinu un pārdošanas pasūtījuma rēķinu izrakstīšana pārskata grāmatošanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="91ac4-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="91ac4-111">Ja partijas numuri nav pieejami, jaunā funkcionalitāte pārdošanas rindām izmanto noklusējuma partijas ID.</span><span class="sxs-lookup"><span data-stu-id="91ac4-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="91ac4-112">Lai definētu debitora pasūtījumiem izmantojamo noklusējuma partijas ID, kopsavilkuma cilnes **Pasūtījums** lapas **Tirdzniecības parametri** cilnē **Debitoru pasūtījumi** iestatiet vērtību laukā **Noklusējuma partijas ID**.</span><span class="sxs-lookup"><span data-stu-id="91ac4-112">To define the default batch ID that is used for customer orders, on the **Commerce parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="91ac4-113">Lai definētu pārskatu grāmatošanas laikā pārdošanas pasūtījumu rēķinos izmantojamo noklusējuma partijas ID, kopsavilkuma cilnes **Krājumu atjaunināšana** lapas **Tirdzniecības parametri** cilnē **Grāmatošana** iestatiet vērtību laukā **Noklusējuma partijas ID**.</span><span class="sxs-lookup"><span data-stu-id="91ac4-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Commerce parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="91ac4-114">Šī funkcionalitāte ir pieejama tikai tad, ja attiecīgajai veikala noliktavai un krājumiem ir iespējoti papildu noliktavas procesi.</span><span class="sxs-lookup"><span data-stu-id="91ac4-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="91ac4-115">Turpmākajos laidienos šī funkcionalitāte tiks atbalstīta arī tad, ja netiks izmantots papildu noliktavas pārvaldības process.</span><span class="sxs-lookup"><span data-stu-id="91ac4-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="91ac4-116">Retail versijā 10.0.5. tika ieviests atbalsts uzlabotai pēc partijas izsekoto krājumu apstrādei izrakstu grāmatošanas laikā neuzlabotiem noliktavas pārvaldības scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="91ac4-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>
