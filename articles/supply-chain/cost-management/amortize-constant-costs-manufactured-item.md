---
title: "Ražotā krājuma konstanto izmaksu amortizācija"
description: "Ražota krājuma konstantas izmaksas atspoguļo operāciju iestatījumu laikus un komponentus ar konstantu daudzumu vai konstantu brāķa apjomu."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8a4e247013c97a72f02209bd460cac82798d3cef
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="9cb78-103">Ražotā krājuma konstanto izmaksu amortizācija</span><span class="sxs-lookup"><span data-stu-id="9cb78-103">Amortize constant costs for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cb78-104">Ražota krājuma konstantas izmaksas atspoguļo operāciju iestatījumu laikus un komponentus ar konstantu daudzumu vai konstantu brāķa apjomu.</span><span class="sxs-lookup"><span data-stu-id="9cb78-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="9cb78-105">Kalkulēšanas laidiena apjoma jēdziens tiek izmantots, lai amortizētu šīs konstantās izmaksas ražota krājuma aprēķinātās izmaksās.</span><span class="sxs-lookup"><span data-stu-id="9cb78-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="9cb78-106">Šim jēdzienam ir vairāki sinonīmi, viens no kuriem ir uzskaites laidiena apjoms.</span><span class="sxs-lookup"><span data-stu-id="9cb78-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="9cb78-107">Amortizācijas konstantu izmaksu jēdzienam arī ir vairāki sinonīmi, viens no kuriem ir proporcionālas konstantas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="9cb78-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="9cb78-108">Ražota krājuma uzskaites laidiena apjoma daudzums tiek izmantots materiālu komplekta (MK) aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="9cb78-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="9cb78-109">Daudzums ir atkarīgs no tā, kā jūs uzsākat un veicat MK aprēķinu, ko paskaidro turpmāk minētais:</span><span class="sxs-lookup"><span data-stu-id="9cb78-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="9cb78-110">Noklusējuma aprēķinu daudzums krājuma MK aprēķinā — Krājuma standarta pasūtījuma daudzums inventarizācijai darbojas kā tā uzskaites laidiena apjoms, bet pēc noklusējuma daudzuma vērtība var būt lielāka, lai atspoguļotu krājuma pasūtījuma daudzuma dalāmo.</span><span class="sxs-lookup"><span data-stu-id="9cb78-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="9cb78-111">Krājuma standarta pasūtījuma daudzums un dalāmais var tikt definēti to noklusējuma pasūtījuma iestatījumos vai vietai noteiktos pasūtījuma iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="9cb78-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="9cb78-112">Noteikts aprēķinu daudzums krājuma MK aprēķinā - Noteikts aprēķina daudzums darbojas kā krājuma kalkulēšanas laidiena apjoms.</span><span class="sxs-lookup"><span data-stu-id="9cb78-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="9cb78-113">Aprēķina daudzums sākotnēji izmanto krājuma standarta pasūtījuma daudzumu, bet noklusējuma vērtību var manuāli pārlabot.</span><span class="sxs-lookup"><span data-stu-id="9cb78-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="9cb78-114">Norādītais aprēķina daudzums atspoguļo uzskaites laidiena apjomu norādītajam krājumam un ražotiem komponentiem, kuriem ir ražošanas MK līnijas veids.</span><span class="sxs-lookup"><span data-stu-id="9cb78-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="9cb78-115">Tas ir tāpēc, ka tiek pieņemts, ka komponenti tiks ražoti līdz noteiktam daudzumam.</span><span class="sxs-lookup"><span data-stu-id="9cb78-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="9cb78-116">Uzskaites laidiena apjoms citiem ražotiem komponentiem, kuriem ir krājuma MK līnijas veids, atspoguļo to standarta pasūtījuma daudzumu.</span><span class="sxs-lookup"><span data-stu-id="9cb78-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="9cb78-117">Noteikts pasūtījuma veikšanas aprēķinu daudzums krājuma MK aprēķinā - Noteikts aprēķinu daudzums darbojas kā krājuma un tā ražoto komponentu kalkulēšanas laidiena apjoms, kad MK aprēķini izmanto pasūtījuma veikšanas izvēršanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="9cb78-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="9cb78-118">Tiek pieņemts, ka ražotie komponenti tiks ražoti līdz noteiktam daudzumam līdzīgi kā ražošanas komponents, kuram ir ražošanas MK līnijas veids.</span><span class="sxs-lookup"><span data-stu-id="9cb78-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="9cb78-119">Noteikts aprēķinu daudzums pasūtījumam noteiktā MK aprēķinā − Pasūtījumam noteiktu MK aprēķinu var veikt līnijas krājumam pārdošanas pasūtījumā, pārdošanas pieprasījumā vai pakalpojuma pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="9cb78-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="9cb78-120">Noteiktais aprēķinu daudzums izmanto sākotnējā rindas elementa daudzumu, bet noklusējuma daudzumu var pārlabot.</span><span class="sxs-lookup"><span data-stu-id="9cb78-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="9cb78-121">Jūs varat atlasīt, vai pasūtījumam noteiktais MK aprēķins izmanto pasūtījuma veikšanas vai daudzlīmeņu izvēršanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="9cb78-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="9cb78-122">Ražoto krājumu amortizēto konstanto izmaksu aprēķinātais apjoms ir nosaukts par maksām.</span><span class="sxs-lookup"><span data-stu-id="9cb78-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>






