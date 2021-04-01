---
title: Kravas plānošanas rīks
description: Šajā tēmā ir aprakstīts, kā strādāt ar kravas plānošanas rīku.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 480006a6d091acdf5c88fdbf0d9e625088d660d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247242"
---
# <a name="load-building-workbench"></a><span data-ttu-id="beff3-103">Kravas plānošanas rīks</span><span class="sxs-lookup"><span data-stu-id="beff3-103">Load building workbench</span></span>

<span data-ttu-id="beff3-104">Kravas plānošanas rīks ļauj izmantot kravas plānošanas stratēģijas, kad veidojat kravas.</span><span class="sxs-lookup"><span data-stu-id="beff3-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="beff3-105">Kravas plānošanas stratēģijas izveidošana</span><span class="sxs-lookup"><span data-stu-id="beff3-105">Create a load building strategy</span></span>

<span data-ttu-id="beff3-106">Varat izmantot kravas plānošanas stratēģijas, lai automātiski izveidotu kravas.</span><span class="sxs-lookup"><span data-stu-id="beff3-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="beff3-107">Šī iespēja var būt noderīga šādās situācijās:</span><span class="sxs-lookup"><span data-stu-id="beff3-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="beff3-108">Ja regulāri nosūtat noteiktu preču komplektu, kravas stratēģijas palīdz ietaupīt laiku, jo jums nav jāveido tāda pati krava katru reizi.</span><span class="sxs-lookup"><span data-stu-id="beff3-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="beff3-109">Ja vēlaties izvairīties no daļēji pilnas kravas, lai palielinātu efektivitāti, kravas stratēģijas var palīdzēt piepildīt katru kravu, cik vien iespējams.</span><span class="sxs-lookup"><span data-stu-id="beff3-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="beff3-110">Kravas veidošanas stratēģijas klase, ko sauc `TMSLoadBuildingVolumeStrategy`, nodrošina kravas plānošanas stratēģiju, ko sauc *Lielapjoma kravas plānošanas stratēģija*.</span><span class="sxs-lookup"><span data-stu-id="beff3-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="beff3-111">Šī stratēģija ļauj izmantot maksimālās vērtības, kuras ir norādītas garumam un svaram kravas veidnē, vai arī iestatījumus var ignorēt, ievadot jaunas vērtības.</span><span class="sxs-lookup"><span data-stu-id="beff3-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="beff3-112">Šī stratēģija ir vienīgā stratēģija, kas tiek iekļauta ārpus lodziņa.</span><span class="sxs-lookup"><span data-stu-id="beff3-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="beff3-113">(Tomēr, iespējams, ir dažas pielāgotas stratēģijas.)</span><span class="sxs-lookup"><span data-stu-id="beff3-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="beff3-114">Lai izmantotu *Uz apjomu balstītu kravas plānošanas stratēģiju*, atlasiet to laukā **Kravas plānošanas stratēģija** lapā **Kravas plānošanas rīks** (**Transportēšanas pārvaldības &gt; Plānošana &gt; Kravas plānošanas rīks**).</span><span class="sxs-lookup"><span data-stu-id="beff3-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="beff3-115">Lai izveidotu kravas plānošanas stratēģiju, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="beff3-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="beff3-116">Doties uz **Transportēšanas pārvaldība &gt; Uzstādīšana &gt; Kravas plānošana &gt; Kravas plānošanas stratēģija**.</span><span class="sxs-lookup"><span data-stu-id="beff3-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="beff3-117">Darbības rūtī atlasiet **Ģenerēt klašu sarakstu**, lai pārliecinātos, ka jums ir jaunākās visu pieejamo klašu versijas.</span><span class="sxs-lookup"><span data-stu-id="beff3-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="beff3-118">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="beff3-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="beff3-119">Ievadiet unikālu stratēģijas nosaukumu, atlasiet tai kravas plānošanas stratēģijas klasi un ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="beff3-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="beff3-120">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="beff3-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="beff3-121">Darbību rūtī atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="beff3-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="beff3-122">Lapā **Kravas plānošanas stratēģijas parametri** atlasiet **Kravas noslodze** sarakstā un pēc tam laukā **Vērtība** ievadiet procentuālo daļu no kravas kopējā tilpuma kravas, kas jāpiemēro jaunajai kravas plānošanas stratēģijai.</span><span class="sxs-lookup"><span data-stu-id="beff3-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="beff3-123">Atlasiet **Svara noslodze** sarakstā un pēc tam laukā **Vērtība** ievadiet procentuālo daļu no kravas kopējā svara noslodzes, kas jāpiemēro jaunajai kravas plānošanas stratēģijai.</span><span class="sxs-lookup"><span data-stu-id="beff3-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="beff3-124">Aizveriet lapu **Kravas plānošanas stratēģijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="beff3-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="beff3-125">Aizveriet lapu **Kravas plānošanas stratēģijas**.</span><span class="sxs-lookup"><span data-stu-id="beff3-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="beff3-126">Tagad varat piešķirt kravas plānošanas stratēģiju kravas plānošanas veidnei.</span><span class="sxs-lookup"><span data-stu-id="beff3-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="beff3-127">Vai arī to var izmantot tieši kravas plānošanas rīkā.</span><span class="sxs-lookup"><span data-stu-id="beff3-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="beff3-128">Izmantot kravas plānošanas stratēģiju kravas plānošanas rīkā</span><span class="sxs-lookup"><span data-stu-id="beff3-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="beff3-129">Dodieties uz **Transportēšanas pārvaldība &gt; Plānošana &gt; Kravas plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="beff3-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="beff3-130">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="beff3-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="beff3-131">Atlasiet stratēģiju laukā **Kravas plānošanas stratēģija**.</span><span class="sxs-lookup"><span data-stu-id="beff3-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="beff3-132">Ja esat noteicis kravas plānošanas veidni un piešķīris tai kravas plānošanas stratēģiju, darbības rūtī cilnē **Pārvaldīt veidnes** atlasiet **Lietot veidni**.</span><span class="sxs-lookup"><span data-stu-id="beff3-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="beff3-133">Pēc tam nolaižamajā dialoglodziņā **Pielietot kravas plānošanas veidni** atlasiet veidni, kas atrodas laukā **Kravas plānošanas veidnes nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="beff3-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="beff3-134">Kopsavilkuma cilnē **Kravas veidņu secība** atlasiet vienu vai vairākas [kravas veidnes](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="beff3-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="beff3-135">Šis rīks mēģinās ievietot kravu šajos konteineru tipos šeit noteiktajā secībā.</span><span class="sxs-lookup"><span data-stu-id="beff3-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="beff3-136">Parasti mazākie konteineri ir jānovieto saraksta sākumā, lai nodrošinātu, ka vispirms tiek atlasīts vismazākais iespējamais konteiners.</span><span class="sxs-lookup"><span data-stu-id="beff3-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="beff3-137">Darbību rūtī atlasiet **Piedāvāt kravas**.</span><span class="sxs-lookup"><span data-stu-id="beff3-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="beff3-138">Pārskatiet piedāvātās kravas un piedāvātās kravas rindas.</span><span class="sxs-lookup"><span data-stu-id="beff3-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="beff3-139">Darbības rūtī atlasiet **Izveidot kravu**, lai izveidotu kravas, kas pamatotas uz pirmdokumenta rindām kopsavilkuma cilnē **Piedāvātās kravas rindas**.</span><span class="sxs-lookup"><span data-stu-id="beff3-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="beff3-140">Aizveriet lapu **Kravas plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="beff3-140">Close the **Load building workbench** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]