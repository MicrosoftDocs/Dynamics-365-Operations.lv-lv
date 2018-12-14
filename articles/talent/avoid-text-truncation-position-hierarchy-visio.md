---
title: "Izvairīšanās no teksta saīs. amatu hierarhijā un eksport. uz Visio"
description: "Šajā tēmā paskaidrots, kā atrisināt problēmu, ja personu vārdi un amatu nosaukumi tiek saīsināti, kad debitori skata amatu hierarhiju programmā Microsoft Dynamics 365 for Talent. Teksta saīsināšana var apgrūtināt ekrānuzņ. veikšanu vai hierarhijas drukāšanu."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: b688a396e3b384aedb06c470b1634150ae7aa038
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="be507-104">Izvairīšanās no teksta saīs. amatu hierarhijā un eksport. uz Visio</span><span class="sxs-lookup"><span data-stu-id="be507-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="be507-105">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="be507-105">**Issue**</span></span>

<span data-ttu-id="be507-106">Kad debitors skata amatu hierarhiju programmā Microsoft Dynamics 365 for Talent, personu vārdi un amatu nosaukumi tiek saīsināti.</span><span class="sxs-lookup"><span data-stu-id="be507-106">When a customer views the position hierarchy in Microsoft Dynamics 365 for Talent, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="be507-107">Tādēļ var būt grūti veikt ekrānuzņēmumu vai izdrukāt un izplatīt hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="be507-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Amatu hierarhija](media/position-h.png)

<span data-ttu-id="be507-109">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="be507-109">**Cause**</span></span>

<span data-ttu-id="be507-110">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="be507-110">This behavior is by design.</span></span>

<span data-ttu-id="be507-111">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="be507-111">**Resolution**</span></span>

<span data-ttu-id="be507-112">Diemžēl lietotāji nevar viegli mainīt teksta lielumu.</span><span class="sxs-lookup"><span data-stu-id="be507-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="be507-113">Tomēr amatu hierarh. var eksportēt no progr. Talent un tad to importēt pakalpojumā Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="be507-113">However, you can export the position hierarchy out of Talent and then import it into Microsoft Visio.</span></span> <span data-ttu-id="be507-114">Lai gan raksts tika izveidots programmai Microsoft Dynamics AX 2012, process attiecas arī uz Talent: [Pozīcijas hierarhijas eksportēšana uz Microsoft Visio](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="be507-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Talent: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="be507-115">Rīkojieties šādi, lai eksp. uz Visio.</span><span class="sxs-lookup"><span data-stu-id="be507-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="be507-116">Progr. Talent atv. saraksta lapu **Amati**.</span><span class="sxs-lookup"><span data-stu-id="be507-116">In Talent, open the **Positions** list page.</span></span>

    <span data-ttu-id="be507-117">Lai iekļautu papildu informāciju organizācijas struktūras diagrammā, pievienojiet laukus sarakstā **Amati**, lai tie būtu pieejami, vēlāk izmantojot vedni šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="be507-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="be507-118">Darbību rūtī atlasiet pogu **Atvērt, izmantojot Microsoft Office** un tad sadaļā **Eksportēt uz Excel** atlasiet **Amati**.</span><span class="sxs-lookup"><span data-stu-id="be507-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="be507-119">Vai arī nospiediet Ctrl+T.</span><span class="sxs-lookup"><span data-stu-id="be507-119">Alternatively, press Ctrl+T.</span></span>

    ![Saraksta lapas Amati eksports uz Excel](media/org-admin.png)

3. <span data-ttu-id="be507-121">Saglabājiet eksportēto Excel failu.</span><span class="sxs-lookup"><span data-stu-id="be507-121">Save the Excel file that is exported.</span></span>

    ![Dialogl. Eksp. uz Excel](media/export-excel.png)

4. <span data-ttu-id="be507-123">Pakalpojumā Visio atl. **Visio — izveidot jaunu** un atl. veidnes kateg. **Uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="be507-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Jauna diagr](media/new.png)

5. <span data-ttu-id="be507-125">Atl. **Organizācijas diagr. vednis** un tad atl. **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="be507-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Organizācijas diagr. vedņa dialogl.](media/orgchart-wizard.png)

6. <span data-ttu-id="be507-127">Atlasiet **Informācija, kas jau ir saglabāta failā vai datu bāzē** un tad atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="be507-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="be507-129">Izv. **Teksta, Org Plus (\*.txt), vai Excel fails** un tad atl. **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="be507-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="be507-131">Pārlūkojiet, lai atlasītu eksportēto Excel failu, kas satur amatu hierarhiju, un tad atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="be507-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="be507-133">Iest. laukā **Nos.** vienumu **Amats**, iest. laukā **Sniedz pārsk.** vien. **Sniedz pārsk. amatam**, tad atl. **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="be507-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="be507-135">Atlasiet laukus, kam jābūt redzamiem katrā zarā, un tad atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="be507-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="be507-137">Pievienojiet kolonnu **Amats** sarakstā **Formas datu lauki** un tad atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="be507-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="be507-139">Attēli pašlaik nav pieejami.</span><span class="sxs-lookup"><span data-stu-id="be507-139">Pictures aren't currently available.</span></span> <span data-ttu-id="be507-140">Tādēļ nākamajā lapā atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="be507-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="be507-141">Atl. **Es vēlos, lai vednis automātiski sadala organizācijas diagrammu pa lappusēm**.</span><span class="sxs-lookup"><span data-stu-id="be507-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Organiz. diagr. vednis 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="be507-143">Atl. **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="be507-143">Select **Finish**.</span></span>

    <span data-ttu-id="be507-144">Ja ir amati, kas nav iekļauti struktūrā, tiek parādīts uzaicinājums iekļaut tos diagrammā.</span><span class="sxs-lookup"><span data-stu-id="be507-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="be507-145">Pakalpojumā Visio ģenerētajā diagrammā katrs vadītājs redzams atsevišķā darblapā.</span><span class="sxs-lookup"><span data-stu-id="be507-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="be507-146">Pamatojoties uz laukiem, kas atlasīti iekļaušanai diagrammā, katrs zars rāda atbilstošu informāciju, kad tiek ģenerēts Visio fails.</span><span class="sxs-lookup"><span data-stu-id="be507-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hierarh. diagr.](media/hierarchy.png)

<span data-ttu-id="be507-148">**Papildu opcija**</span><span class="sxs-lookup"><span data-stu-id="be507-148">**Additional option**</span></span>

<span data-ttu-id="be507-149">Programmā Talent var lietot arī darbvietu **Personas**, lai skatītu ar hierarhiju saistīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="be507-149">In Talent, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
