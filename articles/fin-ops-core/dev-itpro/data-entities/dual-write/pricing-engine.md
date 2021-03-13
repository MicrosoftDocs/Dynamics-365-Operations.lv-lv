---
title: Sinhronizēt ar Supply Chain Management cenu noteikšanas programmu pēc pieprasījuma
description: Šajā tēmā aprakstīts, kā izmantot cenu noteikšanas programmu programmā Microsoft Dynamics 365 Supply Chain Management no pakalpojuma Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 45a9de18a3ff9c50eba8b316171b492605d683d4
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130657"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="976cd-103">Sinhronizēt ar Supply Chain Management cenu noteikšanas programmu pēc pieprasījuma</span><span class="sxs-lookup"><span data-stu-id="976cd-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="976cd-104">Microsoft Dynamics 365 Supply Chain Management iekļauj cenu noteikšanas programmu, kas apstrādā tirdzniecības līgumus, cenu lapas, klientu lojalitātes programmas, veicināšanas pasākumus un atlaides.</span><span class="sxs-lookup"><span data-stu-id="976cd-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="976cd-105">Cenu noteikšanas programma izmanto kompleksas kārtulas, lai noteiktu labāko cenu dotajam piedāvājumam vai pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="976cd-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="976cd-106">Izmantojot duālo ierakstu, jūs izmantojat vai nu statisko cenu noteikšanu vai cenu noteikšanas programmu no Dynamics 365 Supply Chain Management piedāvājumu un pasūtījumu lapās pakalpojumā Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="976cd-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="976cd-107">Izmantot cenu noteikšanas programmu no Supply Chain Management pakalpojumā Sales</span><span class="sxs-lookup"><span data-stu-id="976cd-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="976cd-108">Pakalpojumā Sales dodieties uz **Pārdošana \>Pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="976cd-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="976cd-109">Atlasiet **Jauns**, lai izveidotu jaunu pasūtījumu vai atlasītu esošu pasūtījumu sarakstā **Mani pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="976cd-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="976cd-110">Pievienojiet jaunu pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="976cd-110">Add a new order line.</span></span>
4. <span data-ttu-id="976cd-111">Ja veidojat jaunu pasūtījumu, darbību rūtī atlasiet **Cenas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="976cd-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="976cd-112">Ja atjaunināt esošu pasūtījumu, darbību rūtī atlasiet **Pārrēķināt**.</span><span class="sxs-lookup"><span data-stu-id="976cd-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="976cd-113">Šādas kolonnas tiek automātiski aizpildītas:</span><span class="sxs-lookup"><span data-stu-id="976cd-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="976cd-114">Detalizēta summa</span><span class="sxs-lookup"><span data-stu-id="976cd-114">Detail Amount</span></span>
    + <span data-ttu-id="976cd-115">Atlaide %</span><span class="sxs-lookup"><span data-stu-id="976cd-115">Discount %</span></span>
    + <span data-ttu-id="976cd-116">Atlaide</span><span class="sxs-lookup"><span data-stu-id="976cd-116">Discount</span></span>
    + <span data-ttu-id="976cd-117">Summa bez vedmaksas</span><span class="sxs-lookup"><span data-stu-id="976cd-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="976cd-118">Piegādes summa</span><span class="sxs-lookup"><span data-stu-id="976cd-118">Freight Amount</span></span>
    + <span data-ttu-id="976cd-119">Nodokļu kopsumma</span><span class="sxs-lookup"><span data-stu-id="976cd-119">Total Tax</span></span>
    + <span data-ttu-id="976cd-120">Kopsumma</span><span class="sxs-lookup"><span data-stu-id="976cd-120">Total Amount</span></span>
    
5. <span data-ttu-id="976cd-121">Lai nodrošinātu, ka sistēma ņem vērā tirdzniecības un pārdošanas līgumus, lai aprēķinātu cenu:</span><span class="sxs-lookup"><span data-stu-id="976cd-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="976cd-122">Dodieties uz Supply Chain Management vidi.</span><span class="sxs-lookup"><span data-stu-id="976cd-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="976cd-123">Navigējiet uz **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="976cd-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="976cd-124">Atlasiet cilni **Cenas** sānu navigācijas joslā.</span><span class="sxs-lookup"><span data-stu-id="976cd-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="976cd-125">Saskaņā ar **Tirdzniecības līguma vērtēšanas** kopsavilkuma cilni, noņemiet atzīmi no **Manuālas ievades** opcijas.</span><span class="sxs-lookup"><span data-stu-id="976cd-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="976cd-126">Kā tas darbojas</span><span class="sxs-lookup"><span data-stu-id="976cd-126">How it works</span></span>

<span data-ttu-id="976cd-127">Pakalpojumā Sales atlasot **Cenas pasūtījums** saistītajam pārdošanas pasūtījumam tiek izsaukta funkcija **Kopsumma** programmas Supply Chain Management cilnē **Pārdošanas pasūtījums\> Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="976cd-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="976cd-128">Vērtības pasūtījuma kopsummā pakalpojumā Sales tiek izmantotas, lai aizpildītu atbilstošās kolonnas programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="976cd-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="976cd-129">Kad pārdošanas pasūtījuma kopsumma tiek aprēķināta programmā Supply Chain Management, aprēķinā novērtē esošos tirdzniecības līgumus un pārdošanas līgumus klientam un preces, kas norādītas pārdošanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="976cd-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="976cd-130">Šī informācija tiek izmantota kopsummu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="976cd-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="976cd-131">Kad ir atlasīts **Cenas pasūtījums**, programma Sales automātiski ataino visus iestatījumus, kas veikti programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="976cd-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="976cd-132">Ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="976cd-132">Limitations</span></span>

<span data-ttu-id="976cd-133">Kad programmā Sales ir aizpildītas kolonnas, tiek piemēroti šādi ierobežojumi:</span><span class="sxs-lookup"><span data-stu-id="976cd-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="976cd-134">Pakalpojumā Sales netiek replicēti maksu un maksu sadalījumu iestatījumi no programmas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="976cd-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="976cd-135">Cenu noteikšanā netiek ņemtas vērā īpašas mazumtirdzniecības cenas, kas konkretizētas pārdošanas pasūtījuma rindas lapas kolonnā **Mazumtirdzniecības kanāls** programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="976cd-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="976cd-136">Atlaides, kas definētas programmas Supply Chain Management sadaļā **Mazumtirdzniecības atlaižu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="976cd-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
