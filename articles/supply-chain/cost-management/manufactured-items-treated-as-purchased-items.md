---
title: "Saražojamo vai sagādājamo preču iestatīšana"
description: "Preces var iegūt dažādos veidos — tās var saražot (izgatavot) vai sagādāt (nopirkt). Šajā rakstā ir aprakstīti daži raksturīgākie jautājumi, kas jāņem vērā, konfigurējot preces vairāku ieguves veidu atbalstam."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6a11167e2ae2597356ca0e8c0fc8ac8417f3a5bf
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="5d878-104">Saražojamo vai sagādājamo preču iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5d878-104">Set up products that can be produced or procured</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5d878-105">Preces var iegūt dažādos veidos — tās var saražot (izgatavot) vai sagādāt (nopirkt).</span><span class="sxs-lookup"><span data-stu-id="5d878-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="5d878-106">Šajā rakstā ir aprakstīti daži raksturīgākie jautājumi, kas jāņem vērā, konfigurējot preces vairāku ieguves veidu atbalstam.</span><span class="sxs-lookup"><span data-stu-id="5d878-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="5d878-107">Vairāku resursu plānošanu parasti izmanto iegādātam krājumam, kas laiku pa laikam tiek saražots, vai krājumam, kas galvenokārt bija saražotais krājums, bet mainīts tā, lai tas tagad galvenokārt būtu iegādājams krājums.</span><span class="sxs-lookup"><span data-stu-id="5d878-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="5d878-108">Vispirms krājums tiks veidots, kā saražotais krājums, lai definētu materiālu komplektu (MK), maršruta informāciju, kā arī lai atbalstītu krājuma ražojuma pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="5d878-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="5d878-109">Ražošanas tipam jābūt iestatītam uz **MK** (vai ražošanas procesam uz **Formula** vai **Līdzprodukts**).</span><span class="sxs-lookup"><span data-stu-id="5d878-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="5d878-110">Izmantojot standarta izmaksas, ražotajam krājumam var aprēķināt krājuma izmaksu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5d878-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="5d878-111">Tomēr krājumu izmaksu ieraksts var neatbilst tām standarta izmaksām, kas paredzētas iegādes nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="5d878-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="5d878-112">Šādā gadījumā standarta izmaksas manuāli jāievada un jāaktivizē krājumu izmaksu ierakstam.</span><span class="sxs-lookup"><span data-stu-id="5d878-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="5d878-113">Izmaksu aprēķināšanai izmantojiet īpašu MK un maršrutu, kas attiecas uz preču piegādes komplekta finanšu periodu, lai samazinātu novirzes laika gaitā.</span><span class="sxs-lookup"><span data-stu-id="5d878-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="5d878-114">Turklāt vienā vietā saražoto krājumu var pārsūtīt uz citu vietu.</span><span class="sxs-lookup"><span data-stu-id="5d878-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="5d878-115">Tāpēc krājuma izmaksas manuāli jāievada un jāaktivizē tai vietai, uz kuru pārsūtīts krājums.</span><span class="sxs-lookup"><span data-stu-id="5d878-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="5d878-116">Izmantojot saražoto krājumu kā sastāvdaļu augstāka līmeņa produktos, sastāvdaļas izmaksas ir jāuzskata par iepirkto krājumu.</span><span class="sxs-lookup"><span data-stu-id="5d878-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="5d878-117">Šīs vadlīnijas stājas spēkā neatkarīgi no tā, vai sastāvdaļas izmaksas tika aprēķinātas vai manuāli ievadītas.</span><span class="sxs-lookup"><span data-stu-id="5d878-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="5d878-118">Citiem vārdiem sakot, MK aprēķinam jāapstrādā krājuma izmaksas kā iegādājamā sastāvdaļa, nevis izmantot krājuma MK un maršrutēšanas informāciju izmaksu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="5d878-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> <span data-ttu-id="5d878-119">Lai izvairītos no šī aprēķina, atlasiet karodziņu **Pārtraukt izvēršanu**, kas iegults MK aprēķinu grupā, kas piešķirta krājumam.</span><span class="sxs-lookup"><span data-stu-id="5d878-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="5d878-120">Lai novērstu vispārējās plānošanas aprēķinus no izvēršanas prasībām, izmantojot krājumu, iestatiet izvēršanas periodu uz 0 (nulle) dienām krājuma vajadzībām vai seguma grupai.</span><span class="sxs-lookup"><span data-stu-id="5d878-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="5d878-121">Vispārējās plānošanas aprēķins pēc tam apstrādās krājumu kā iegādāto krājumu, un neveiks papildu aprēķinus krājuma MK un maršruta informācijai.</span><span class="sxs-lookup"><span data-stu-id="5d878-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






