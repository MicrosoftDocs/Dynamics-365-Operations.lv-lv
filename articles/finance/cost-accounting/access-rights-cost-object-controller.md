---
title: Izmaksu objekta kontrolieru piekļuves tiesības
description: Šajā tēmā ir sniegta informācija par piekļuves tiesībām izmaksu objektu kontrolieriem.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897628"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="a3054-103">Izmaksu objekta kontrolieru piekļuves tiesības</span><span class="sxs-lookup"><span data-stu-id="a3054-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3054-104">Darbvieta **Izmaksu kontrole** ir centralizēta vieta, kur pārvaldnieki var skatīt savu izmaksu objektu veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="a3054-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="a3054-105">Šī darbvieta sniedz pārvaldniekiem iespēju izmantot izmaksu uzskaites datus, lai gan viņi nav izmaksu grāmatveži.</span><span class="sxs-lookup"><span data-stu-id="a3054-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="a3054-106">Drošības apsvērumu dēļ pārvaldniekiem drīkst nodrošināt piekļuvi tikai tiem izmaksu uzskaites datiem, kas ir saistīti ar konkrēto izmaksu objektu, par kuru viņi ir atbildīgi.</span><span class="sxs-lookup"><span data-stu-id="a3054-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="a3054-107">Darbvietā Izmaksu uzskaite ir pieejamas četras unikālas lomas.</span><span class="sxs-lookup"><span data-stu-id="a3054-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="a3054-108">Lomas nosaukums</span><span class="sxs-lookup"><span data-stu-id="a3054-108">Role name</span></span>               | <span data-ttu-id="a3054-109">Licence</span><span class="sxs-lookup"><span data-stu-id="a3054-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="a3054-110">Izmaksu uzskaites pārvaldnieks</span><span class="sxs-lookup"><span data-stu-id="a3054-110">Cost accounting manager</span></span> | <span data-ttu-id="a3054-111">Aktivitāte</span><span class="sxs-lookup"><span data-stu-id="a3054-111">Activity</span></span>     |
| <span data-ttu-id="a3054-112">Izmaksu grāmatvedis</span><span class="sxs-lookup"><span data-stu-id="a3054-112">Cost accountant</span></span>         | <span data-ttu-id="a3054-113">Operations</span><span class="sxs-lookup"><span data-stu-id="a3054-113">Operations</span></span>   |
| <span data-ttu-id="a3054-114">Izmaksu grāmatvedības darbinieks</span><span class="sxs-lookup"><span data-stu-id="a3054-114">Cost accountant clerk</span></span>   | <span data-ttu-id="a3054-115">Operations</span><span class="sxs-lookup"><span data-stu-id="a3054-115">Operations</span></span>   |
| <span data-ttu-id="a3054-116">Izmaksu objekta kontrolieris</span><span class="sxs-lookup"><span data-stu-id="a3054-116">Cost object controller</span></span>  | <span data-ttu-id="a3054-117">Grupas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="a3054-117">Team members</span></span> |

<span data-ttu-id="a3054-118">Šajā tēmā ir paskaidrots, kā piešķirt pārvaldniekam lomu **Izmaksu objekta kontrolieris**.</span><span class="sxs-lookup"><span data-stu-id="a3054-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="a3054-119">Ja pārvaldniekam ir piešķirta loma **Izmaksu objekta kontrolieris**, viņš var veikt tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a3054-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="a3054-120">Piekļūt darbvietai **Izmaksu kontrole** (klientā).</span><span class="sxs-lookup"><span data-stu-id="a3054-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="a3054-121">Veikt detalizētu apskati un skatīt lapas, kas ir saistītas ar detalizēto apskati.</span><span class="sxs-lookup"><span data-stu-id="a3054-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="a3054-122">Piekļūt darbvietai **Izmaksu kontrole** (mobilajā lietojumprogrammā).</span><span class="sxs-lookup"><span data-stu-id="a3054-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="a3054-123">Loma **Izmaksu objekta kontrolieris** nesniedz iespēju kontrolēt to, kuriem izmaksu objektiem lietotājs var piekļūt un par kuriem izmaksu objektiem lietotājs var skatīt datus.</span><span class="sxs-lookup"><span data-stu-id="a3054-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="a3054-124">Lomas līmeņa drošība tiek nodrošināta, izmantojot dimensiju hierarhijas un piekļuves saraksta hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="a3054-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="a3054-125">Piekļuves tiesību piešķiršana</span><span class="sxs-lookup"><span data-stu-id="a3054-125">Grant access rights</span></span>
<span data-ttu-id="a3054-126">Tālāk ir sniegts dimensiju hierarhijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="a3054-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="a3054-127">**Detalizēta informācija par dimensiju hierarhiju**</span><span class="sxs-lookup"><span data-stu-id="a3054-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="a3054-128">Dimensiju hierarhijas nosaukums</span><span class="sxs-lookup"><span data-stu-id="a3054-128">Dimension hierarchy name</span></span> | <span data-ttu-id="a3054-129">Dimensija</span><span class="sxs-lookup"><span data-stu-id="a3054-129">Dimension</span></span>    | <span data-ttu-id="a3054-130">Dimensiju hierarhijas veida nosaukums</span><span class="sxs-lookup"><span data-stu-id="a3054-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="a3054-131">Piekļuves sarakstu hierarhija</span><span class="sxs-lookup"><span data-stu-id="a3054-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="a3054-132">Organizācija</span><span class="sxs-lookup"><span data-stu-id="a3054-132">Organization</span></span>             | <span data-ttu-id="a3054-133">Izmaksu centri</span><span class="sxs-lookup"><span data-stu-id="a3054-133">Cost centers</span></span> | <span data-ttu-id="a3054-134">Dimensiju klasifikācijas hierarhija</span><span class="sxs-lookup"><span data-stu-id="a3054-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="a3054-135">**Jā**</span><span class="sxs-lookup"><span data-stu-id="a3054-135">**Yes**</span></span>               |

<span data-ttu-id="a3054-136">Varat izmantot hierarhijas veidotāja kopsavilkuma cilni **Lietotāji**, lai katrā mezglā ievietotu vienu vai vairākus lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="a3054-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="a3054-137">Zari</span><span class="sxs-lookup"><span data-stu-id="a3054-137">Nodes</span></span>                 | <span data-ttu-id="a3054-138">Lietotāji</span><span class="sxs-lookup"><span data-stu-id="a3054-138">Users</span></span>            | <span data-ttu-id="a3054-139">Avota dimensijas elements</span><span class="sxs-lookup"><span data-stu-id="a3054-139">From dimension member</span></span>     |   <span data-ttu-id="a3054-140">Mērķa dimensijas elements</span><span class="sxs-lookup"><span data-stu-id="a3054-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="a3054-141">Organizācija</span><span class="sxs-lookup"><span data-stu-id="a3054-141">Organization</span></span>                      | <span data-ttu-id="a3054-142">Bendžamins, Klēra</span><span class="sxs-lookup"><span data-stu-id="a3054-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="a3054-143">&nbsp;&nbsp;Administrators</span><span class="sxs-lookup"><span data-stu-id="a3054-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="a3054-144">Aprīlī</span><span class="sxs-lookup"><span data-stu-id="a3054-144">April</span></span>            |                           |                         |
| <span data-ttu-id="a3054-145">&nbsp;&nbsp;&nbsp;&nbsp;Finansēt</span><span class="sxs-lookup"><span data-stu-id="a3054-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="a3054-146">Alīsija</span><span class="sxs-lookup"><span data-stu-id="a3054-146">Alicia</span></span>           | <span data-ttu-id="a3054-147">CC002</span><span class="sxs-lookup"><span data-stu-id="a3054-147">CC002</span></span>                     | <span data-ttu-id="a3054-148">CC003</span><span class="sxs-lookup"><span data-stu-id="a3054-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="a3054-149">CC007</span><span class="sxs-lookup"><span data-stu-id="a3054-149">CC007</span></span>                     | <span data-ttu-id="a3054-150">CC007</span><span class="sxs-lookup"><span data-stu-id="a3054-150">CC007</span></span>                   |
| <span data-ttu-id="a3054-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="a3054-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="a3054-152">Ārnijs</span><span class="sxs-lookup"><span data-stu-id="a3054-152">Arnie</span></span>            | <span data-ttu-id="a3054-153">CC001</span><span class="sxs-lookup"><span data-stu-id="a3054-153">CC001</span></span>                     | <span data-ttu-id="a3054-154">CC001</span><span class="sxs-lookup"><span data-stu-id="a3054-154">CC001</span></span>                   |
| <span data-ttu-id="a3054-155">&nbsp;&nbsp;Ražošana</span><span class="sxs-lookup"><span data-stu-id="a3054-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="a3054-156">Deivids</span><span class="sxs-lookup"><span data-stu-id="a3054-156">David</span></span>            |                           |                         |
| <span data-ttu-id="a3054-157">&nbsp;&nbsp;&nbsp;&nbsp;Iepakošana</span><span class="sxs-lookup"><span data-stu-id="a3054-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="a3054-158">Elēna</span><span class="sxs-lookup"><span data-stu-id="a3054-158">Ellen</span></span>            | <span data-ttu-id="a3054-159">CC005</span><span class="sxs-lookup"><span data-stu-id="a3054-159">CC005</span></span>                     | <span data-ttu-id="a3054-160">CC005</span><span class="sxs-lookup"><span data-stu-id="a3054-160">CC005</span></span>                   |
| <span data-ttu-id="a3054-161">&nbsp;&nbsp;&nbsp;&nbsp;Montāža</span><span class="sxs-lookup"><span data-stu-id="a3054-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="a3054-162">Kriss</span><span class="sxs-lookup"><span data-stu-id="a3054-162">Chris</span></span>            | <span data-ttu-id="a3054-163">CC006</span><span class="sxs-lookup"><span data-stu-id="a3054-163">CC006</span></span>                     | <span data-ttu-id="a3054-164">CC006</span><span class="sxs-lookup"><span data-stu-id="a3054-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="a3054-165">Izmaksu grāmatveži ir jāpiešķir augstākajam hierarhijas līmenim, lai viņi varētu skatīt visus ierakstus darbvietā Izmaksu uzskaite.</span><span class="sxs-lookup"><span data-stu-id="a3054-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="a3054-166">Pirms piekļuves saraksta hierarhijas un tās drošības iestatījumu lietošanas lapas **Izmaksu uzskaites parametri** cilnē **Vispārīgi** ir jāiestata opcijas **Iespējot skatīšanas piekļuvi izmaksu objekta dimensijas elementiem** vērtība **Jā** (**Izmaksu uzskaite** > **Iestatīšana** > **Parametri**).</span><span class="sxs-lookup"><span data-stu-id="a3054-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="a3054-167">Piekļuves saraksta hierarhijas iestatījumi tiek izmantoti, lai kontrolētu to, kādi dati tiek rādīti tālāk norādītajos apgabalos.</span><span class="sxs-lookup"><span data-stu-id="a3054-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="a3054-168">Darbvietā **Izmaksu kontrole** (klientā)</span><span class="sxs-lookup"><span data-stu-id="a3054-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="a3054-169">Dati lapās, kas tiek izmantotas padziļinātai apskatei</span><span class="sxs-lookup"><span data-stu-id="a3054-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="a3054-170">Darbvietā **Izmaksu kontrole** (mobilajā lietojumprogrammā)</span><span class="sxs-lookup"><span data-stu-id="a3054-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="a3054-171">Kartēs norādītās bilances</span><span class="sxs-lookup"><span data-stu-id="a3054-171">Balances in cards</span></span>

- <span data-ttu-id="a3054-172">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="a3054-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="a3054-173">Power BI vizualizācijās redzamie dati</span><span class="sxs-lookup"><span data-stu-id="a3054-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="a3054-174">Datu Power BI vizualizācijas, kas ir iegultas Dynamics 365 Finance klientā</span><span class="sxs-lookup"><span data-stu-id="a3054-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="a3054-175">Lai piekļuves saraksta hierarhija varētu ietekmēt datus pakalpojumā Power BI, piekļuves saraksta hierarhija ir jāsavieno pārī ar rindas līmeņa drošību pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="a3054-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="a3054-176">Papildinformāciju skatiet rakstā [Drošības iestatīšana satura pakotnei Izmaksu uzskaite](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="a3054-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="a3054-177">Šajā tēmā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darbvietas **Izmaksu kontrole** lietošanas.</span><span class="sxs-lookup"><span data-stu-id="a3054-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="a3054-178">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a3054-178">Additional resources</span></span>

- [<span data-ttu-id="a3054-179">Izmaksu kontroles darbvieta</span><span class="sxs-lookup"><span data-stu-id="a3054-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="a3054-180">Dimensiju hierarhija</span><span class="sxs-lookup"><span data-stu-id="a3054-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="a3054-181">Drošības iestatīšana satura pakotnei Izmaksu uzskaite</span><span class="sxs-lookup"><span data-stu-id="a3054-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
