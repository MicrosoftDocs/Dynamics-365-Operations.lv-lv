---
title: Piekļuves tiesību definēšana izmaksu objektu kontrolieriem
description: Šajā tēmā ir sniegta informācija par piekļuves tiesībām izmaksu objektu kontrolieriem.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a9ef770d1e2d74d5cc9ed57375431cf2846966d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841709"
---
# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="bf228-103">Piekļuves tiesības izmaksu objekta kontrolierim</span><span class="sxs-lookup"><span data-stu-id="bf228-103">Access rights of a cost object controller</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf228-104">Darbvieta **Izmaksu kontrole** ir centralizēta vieta, kur pārvaldnieki var skatīt savu izmaksu objektu veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="bf228-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="bf228-105">Šī darbvieta sniedz pārvaldniekiem iespēju izmantot izmaksu uzskaites datus, lai gan viņi nav izmaksu grāmatveži.</span><span class="sxs-lookup"><span data-stu-id="bf228-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="bf228-106">Drošības apsvērumu dēļ pārvaldniekiem drīkst nodrošināt piekļuvi tikai tiem izmaksu uzskaites datiem, kas ir saistīti ar konkrēto izmaksu objektu, par kuru viņi ir atbildīgi.</span><span class="sxs-lookup"><span data-stu-id="bf228-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="bf228-107">Darbvietā Izmaksu uzskaite ir pieejamas četras unikālas lomas.</span><span class="sxs-lookup"><span data-stu-id="bf228-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="bf228-108">Lomas nosaukums</span><span class="sxs-lookup"><span data-stu-id="bf228-108">Role name</span></span>               | <span data-ttu-id="bf228-109">Licence</span><span class="sxs-lookup"><span data-stu-id="bf228-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="bf228-110">Izmaksu uzskaites pārvaldnieks</span><span class="sxs-lookup"><span data-stu-id="bf228-110">Cost accounting manager</span></span> | <span data-ttu-id="bf228-111">Aktivitāte</span><span class="sxs-lookup"><span data-stu-id="bf228-111">Activity</span></span>     |
| <span data-ttu-id="bf228-112">Izmaksu grāmatvedis</span><span class="sxs-lookup"><span data-stu-id="bf228-112">Cost accountant</span></span>         | <span data-ttu-id="bf228-113">Operations</span><span class="sxs-lookup"><span data-stu-id="bf228-113">Operations</span></span>   |
| <span data-ttu-id="bf228-114">Izmaksu grāmatvedības darbinieks</span><span class="sxs-lookup"><span data-stu-id="bf228-114">Cost accountant clerk</span></span>   | <span data-ttu-id="bf228-115">Operations</span><span class="sxs-lookup"><span data-stu-id="bf228-115">Operations</span></span>   |
| <span data-ttu-id="bf228-116">Izmaksu objekta kontrolieris</span><span class="sxs-lookup"><span data-stu-id="bf228-116">Cost object controller</span></span>  | <span data-ttu-id="bf228-117">Grupas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="bf228-117">Team members</span></span> |

<span data-ttu-id="bf228-118">Šajā tēmā ir paskaidrots, kā piešķirt pārvaldniekam lomu **Izmaksu objekta kontrolieris**.</span><span class="sxs-lookup"><span data-stu-id="bf228-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="bf228-119">Ja pārvaldniekam ir piešķirta loma **Izmaksu objekta kontrolieris**, viņš var veikt tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="bf228-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="bf228-120">Piekļūt darbvietai **Izmaksu kontrole** (klientā).</span><span class="sxs-lookup"><span data-stu-id="bf228-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="bf228-121">Veikt detalizētu apskati un skatīt lapas, kas ir saistītas ar detalizēto apskati.</span><span class="sxs-lookup"><span data-stu-id="bf228-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="bf228-122">Piekļūt darbvietai **Izmaksu kontrole** (mobilajā lietojumprogrammā).</span><span class="sxs-lookup"><span data-stu-id="bf228-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="bf228-123">Loma **Izmaksu objekta kontrolieris** nesniedz iespēju kontrolēt to, kuriem izmaksu objektiem lietotājs var piekļūt un par kuriem izmaksu objektiem lietotājs var skatīt datus.</span><span class="sxs-lookup"><span data-stu-id="bf228-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="bf228-124">Lomas līmeņa drošība tiek nodrošināta, izmantojot dimensiju hierarhijas un piekļuves saraksta hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="bf228-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="bf228-125">Piekļuves tiesību piešķiršana</span><span class="sxs-lookup"><span data-stu-id="bf228-125">Grant access rights</span></span>
<span data-ttu-id="bf228-126">Tālāk ir sniegts dimensiju hierarhijas piemērs.</span><span class="sxs-lookup"><span data-stu-id="bf228-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="bf228-127">**Detalizēta informācija par dimensiju hierarhiju**</span><span class="sxs-lookup"><span data-stu-id="bf228-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="bf228-128">Dimensiju hierarhijas nosaukums</span><span class="sxs-lookup"><span data-stu-id="bf228-128">Dimension hierarchy name</span></span> | <span data-ttu-id="bf228-129">Dimensija</span><span class="sxs-lookup"><span data-stu-id="bf228-129">Dimension</span></span>    | <span data-ttu-id="bf228-130">Dimensiju hierarhijas veida nosaukums</span><span class="sxs-lookup"><span data-stu-id="bf228-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="bf228-131">Piekļuves sarakstu hierarhija</span><span class="sxs-lookup"><span data-stu-id="bf228-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="bf228-132">Organizācija</span><span class="sxs-lookup"><span data-stu-id="bf228-132">Organization</span></span>             | <span data-ttu-id="bf228-133">Izmaksu centri</span><span class="sxs-lookup"><span data-stu-id="bf228-133">Cost centers</span></span> | <span data-ttu-id="bf228-134">Dimensiju klasifikācijas hierarhija</span><span class="sxs-lookup"><span data-stu-id="bf228-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="bf228-135">**Jā**</span><span class="sxs-lookup"><span data-stu-id="bf228-135">**Yes**</span></span>               |

<span data-ttu-id="bf228-136">Varat izmantot hierarhijas veidotāja kopsavilkuma cilni **Lietotāji**, lai katrā mezglā ievietotu vienu vai vairākus lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="bf228-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="bf228-137">Lietotāji</span><span class="sxs-lookup"><span data-stu-id="bf228-137">Users</span></span>            | <span data-ttu-id="bf228-138">Dimensijas elementu diapazons</span><span class="sxs-lookup"><span data-stu-id="bf228-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="bf228-139">**Mezgli**</span><span class="sxs-lookup"><span data-stu-id="bf228-139">**Nodes**</span></span>                         | <span data-ttu-id="bf228-140">**Lietotāja ID**</span><span class="sxs-lookup"><span data-stu-id="bf228-140">**User ID**</span></span>      | <span data-ttu-id="bf228-141">**Avota dimensijas elements**</span><span class="sxs-lookup"><span data-stu-id="bf228-141">**From dimension member**</span></span> | <span data-ttu-id="bf228-142">**Mērķa dimensijas elements**</span><span class="sxs-lookup"><span data-stu-id="bf228-142">**To dimension member**</span></span> |
| <span data-ttu-id="bf228-143">Organizācija</span><span class="sxs-lookup"><span data-stu-id="bf228-143">Organization</span></span>                      | <span data-ttu-id="bf228-144">Bendžamins, Klēra</span><span class="sxs-lookup"><span data-stu-id="bf228-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="bf228-145">&nbsp;&nbsp;Administrators</span><span class="sxs-lookup"><span data-stu-id="bf228-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="bf228-146">Aprīlī</span><span class="sxs-lookup"><span data-stu-id="bf228-146">April</span></span>            |                           |                         |
| <span data-ttu-id="bf228-147">&nbsp;&nbsp;&nbsp;&nbsp;Finansēt</span><span class="sxs-lookup"><span data-stu-id="bf228-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="bf228-148">Alīsija</span><span class="sxs-lookup"><span data-stu-id="bf228-148">Alicia</span></span>           | <span data-ttu-id="bf228-149">CC002</span><span class="sxs-lookup"><span data-stu-id="bf228-149">CC002</span></span>                     | <span data-ttu-id="bf228-150">CC003</span><span class="sxs-lookup"><span data-stu-id="bf228-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="bf228-151">CC007</span><span class="sxs-lookup"><span data-stu-id="bf228-151">CC007</span></span>                     | <span data-ttu-id="bf228-152">CC007</span><span class="sxs-lookup"><span data-stu-id="bf228-152">CC007</span></span>                   |
| <span data-ttu-id="bf228-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="bf228-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="bf228-154">Ārnijs</span><span class="sxs-lookup"><span data-stu-id="bf228-154">Arnie</span></span>            | <span data-ttu-id="bf228-155">CC001</span><span class="sxs-lookup"><span data-stu-id="bf228-155">CC001</span></span>                     | <span data-ttu-id="bf228-156">CC001</span><span class="sxs-lookup"><span data-stu-id="bf228-156">CC001</span></span>                   |
| <span data-ttu-id="bf228-157">&nbsp;&nbsp;Ražošana</span><span class="sxs-lookup"><span data-stu-id="bf228-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="bf228-158">Deivids</span><span class="sxs-lookup"><span data-stu-id="bf228-158">David</span></span>            |                           |                         |
| <span data-ttu-id="bf228-159">&nbsp;&nbsp;&nbsp;&nbsp;Iepakošana</span><span class="sxs-lookup"><span data-stu-id="bf228-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="bf228-160">Elēna</span><span class="sxs-lookup"><span data-stu-id="bf228-160">Ellen</span></span>            | <span data-ttu-id="bf228-161">CC005</span><span class="sxs-lookup"><span data-stu-id="bf228-161">CC005</span></span>                     | <span data-ttu-id="bf228-162">CC005</span><span class="sxs-lookup"><span data-stu-id="bf228-162">CC005</span></span>                   |
| <span data-ttu-id="bf228-163">&nbsp;&nbsp;&nbsp;&nbsp;Montāža</span><span class="sxs-lookup"><span data-stu-id="bf228-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="bf228-164">Kriss</span><span class="sxs-lookup"><span data-stu-id="bf228-164">Chris</span></span>            | <span data-ttu-id="bf228-165">CC006</span><span class="sxs-lookup"><span data-stu-id="bf228-165">CC006</span></span>                     | <span data-ttu-id="bf228-166">CC006</span><span class="sxs-lookup"><span data-stu-id="bf228-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="bf228-167">Izmaksu grāmatveži ir jāpiešķir augstākajam hierarhijas līmenim, lai viņi varētu skatīt visus ierakstus darbvietā Izmaksu uzskaite.</span><span class="sxs-lookup"><span data-stu-id="bf228-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="bf228-168">Pirms piekļuves saraksta hierarhijas un tās drošības iestatījumu lietošanas lapas **Izmaksu uzskaites parametri** cilnē **Vispārīgi** ir jāiestata opcijas **Iespējot skatīšanas piekļuvi izmaksu objekta dimensijas elementiem** vērtība **Jā** (**Izmaksu uzskaite** > **Iestatīšana** > **Parametri**).</span><span class="sxs-lookup"><span data-stu-id="bf228-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="bf228-169">Piekļuves saraksta hierarhijas iestatījumi tiek izmantoti, lai kontrolētu to, kādi dati tiek rādīti tālāk norādītajos apgabalos.</span><span class="sxs-lookup"><span data-stu-id="bf228-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="bf228-170">Darbvietā **Izmaksu kontrole** (klientā)</span><span class="sxs-lookup"><span data-stu-id="bf228-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="bf228-171">Dati lapās, kas tiek izmantotas padziļinātai apskatei</span><span class="sxs-lookup"><span data-stu-id="bf228-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="bf228-172">Darbvietā **Izmaksu kontrole** (mobilajā lietojumprogrammā)</span><span class="sxs-lookup"><span data-stu-id="bf228-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="bf228-173">Kartēs norādītās bilances</span><span class="sxs-lookup"><span data-stu-id="bf228-173">Balances in cards</span></span>

- <span data-ttu-id="bf228-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="bf228-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="bf228-175">Power BI vizualizācijās redzamie dati</span><span class="sxs-lookup"><span data-stu-id="bf228-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="bf228-176">Datu Power BIvizualizācijas, kas ir iegultas Microsoft Dynamics 365 for Finance and Operations klientā</span><span class="sxs-lookup"><span data-stu-id="bf228-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="bf228-177">Lai piekļuves saraksta hierarhija varētu ietekmēt datus pakalpojumā Power BI, piekļuves saraksta hierarhija ir jāsavieno pārī ar rindas līmeņa drošību pakalpojumā Power BI.</span><span class="sxs-lookup"><span data-stu-id="bf228-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="bf228-178">Papildinformāciju skatiet rakstā [Drošības iestatīšana satura pakotnei Izmaksu uzskaite](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="bf228-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="bf228-179">Šajā tēmā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darbvietas **Izmaksu kontrole** lietošanas.</span><span class="sxs-lookup"><span data-stu-id="bf228-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="bf228-180">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bf228-180">Additional resources</span></span>

- [<span data-ttu-id="bf228-181">Izmaksu kontroles darbvieta</span><span class="sxs-lookup"><span data-stu-id="bf228-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="bf228-182">Dimensiju hierarhija</span><span class="sxs-lookup"><span data-stu-id="bf228-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="bf228-183">Drošības iestatīšana satura pakotnei Izmaksu uzskaite</span><span class="sxs-lookup"><span data-stu-id="bf228-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
