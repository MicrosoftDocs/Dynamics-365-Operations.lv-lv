---
title: Iestatīt svītrkodus
description: Šajā rakstā ir aprakstīts, kā izmantot svītrkodus programmā Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 15d12abe32d3f5a47348016c67a4fb02d0a5d8e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "347357"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="b4621-103">Iestatīt svītrkodus</span><span class="sxs-lookup"><span data-stu-id="b4621-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4621-104">Šajā rakstā ir aprakstīts, kā izmantot svītrkodus programmā Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="b4621-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="b4621-105">Preču iepirkšanai un pārdošanai, preces variantu izsekošanai un debitoru un darbinieku datu iestatīšanai vai izmantot svītrkodus.</span><span class="sxs-lookup"><span data-stu-id="b4621-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="b4621-106">Svītrkodus var izmantot arī, lai izsniegtu un apstiprinātu kuponus, dāvanu kartes un kredīta notas.</span><span class="sxs-lookup"><span data-stu-id="b4621-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="b4621-107">Mazumtirdzniecības preces var iestatīt tā, lai uz tām attiektos standarta vai pielāgoti iekšējie svītrkodi.</span><span class="sxs-lookup"><span data-stu-id="b4621-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="b4621-108">Vienai precei var būt vairāki svītrkodi.</span><span class="sxs-lookup"><span data-stu-id="b4621-108">Products can have more than one bar code.</span></span> <span data-ttu-id="b4621-109">Piemēram, precei var būt vairāki svītrkodi tad, ja tā tiek saņemta no dažādiem ražotājiem vai arī tai ir dažādi varianti, kas atkarīgi no izmēra, stila vai krāsas.</span><span class="sxs-lookup"><span data-stu-id="b4621-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="b4621-110">Svītrkodi var ietvert informāciju par preces svaru vai cenu.</span><span class="sxs-lookup"><span data-stu-id="b4621-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="b4621-111">Svītrkodu maskas ir veidnes, ko izmanto svītrkodu izveidei.</span><span class="sxs-lookup"><span data-stu-id="b4621-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="b4621-112">Ja katrai variantu kombinācijai tiek piešķirts unikāls svītrkods, tad, skenējot preces svītrkodu kases sistēmā, programma nosaka, kurš preces variants tiek pārdots.</span><span class="sxs-lookup"><span data-stu-id="b4621-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="b4621-113">Var arī apkopot un skatīt pārdošanas statistiku pēc variantiem.</span><span class="sxs-lookup"><span data-stu-id="b4621-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="b4621-114">Katrai izmēru, krāsu un stilu grupai var piešķirt unikālu numuru, kas svītrkodā tiek izmantots konkrētās grupas identificēšanai.</span><span class="sxs-lookup"><span data-stu-id="b4621-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="b4621-115">Dynamics 365 for Retail izmanto svītrkoda masku, tiek automātiski ģenerētu svītrkodus katrai variantu kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="b4621-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="b4621-116">Šo funkcionalitāti var izmantot, ja ir pieejams daudz dažādu izmēru, krāsu un stilu, jo, pievienojot katru varianta kodu, ievērojami palielinās kombināciju skaits.</span><span class="sxs-lookup"><span data-stu-id="b4621-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="b4621-117">Ja šī funkcionalitāte netiek izmantota, svītrkods jāpiešķir katrai preces variantu raksturojošai kombinācijai manuāli.</span><span class="sxs-lookup"><span data-stu-id="b4621-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="b4621-118">Svītrkodus var arī izveidot manuāli vai automātiski.</span><span class="sxs-lookup"><span data-stu-id="b4621-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="b4621-119">Lai izveidotu svītrkodus, izpildiet tālāk aprakstītos uzdevumus to minētajā secībā.</span><span class="sxs-lookup"><span data-stu-id="b4621-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="b4621-120">[Svītrkoda maskas rakstzīmju iestatīšana](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="b4621-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="b4621-121">[Svītrkodu masku iestatīšana](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="b4621-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="b4621-122">Konfigurējiet svītrkoda iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="b4621-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="b4621-123">Izveidojiet noteiktu preču svītrkodus.</span><span class="sxs-lookup"><span data-stu-id="b4621-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4621-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b4621-124">Additional resources</span></span>

[<span data-ttu-id="b4621-125">Svītrkodu masku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b4621-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)
