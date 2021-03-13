---
title: Izvairīšanās no teksta saīsināšanas amatu hierarhijā un eksportēšana uz Visio
description: Šajā rakstā ir paskaidrots, kā atrisināt problēmu, kas izraisa personu vārdu un amatu nosaukumu saīsināšanu, kad debitori skata amatu hierarhiju programmā Microsoft Dynamics 365 Human Resources. Teksta saīsināšana var apgrūtināt ekrānuzņ. veikšanu vai hierarhijas drukāšanu.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0dc91d3165f14c165f75756dc63a3dc8f63149aa
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113398"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="bfc86-104">Izvairīšanās no teksta saīs. amatu hierarhijā un eksport. uz Visio</span><span class="sxs-lookup"><span data-stu-id="bfc86-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

<span data-ttu-id="bfc86-105">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="bfc86-105">**Issue**</span></span>

<span data-ttu-id="bfc86-106">Kad debitors skata amatu hierarhiju programmā Microsoft Dynamics 365 Human Resources, tiek saīsināti personu vārdi un amatu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="bfc86-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="bfc86-107">Tādēļ var būt grūti veikt ekrānuzņēmumu vai izdrukāt un izplatīt hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="bfc86-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Amatu hierarhija](media/position-h.png)

<span data-ttu-id="bfc86-109">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="bfc86-109">**Cause**</span></span>

<span data-ttu-id="bfc86-110">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="bfc86-110">This behavior is by design.</span></span>

<span data-ttu-id="bfc86-111">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="bfc86-111">**Resolution**</span></span>

<span data-ttu-id="bfc86-112">Diemžēl lietotāji nevar viegli mainīt teksta lielumu.</span><span class="sxs-lookup"><span data-stu-id="bfc86-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="bfc86-113">Tomēr amatu hierarhiju var eksportēt no Human Resources un tad to importēt Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="bfc86-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="bfc86-114">Lai gan šis raksts sarakstīts par Microsoft Dynamics AX 2012, process attiecas arī uz Human Resources: [Amatu hierarhijas eksportēšana uz Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="bfc86-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="bfc86-115">Rīkojieties šādi, lai eksp. uz Visio.</span><span class="sxs-lookup"><span data-stu-id="bfc86-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="bfc86-116">Human Resources atveriet saraksta lapu **Pozīcijas**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="bfc86-117">Lai iekļautu papildu informāciju organizācijas struktūras diagrammā, pievienojiet laukus sarakstā **Amati**, lai tie būtu pieejami, vēlāk izmantojot vedni šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="bfc86-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="bfc86-118">Darbību rūtī atlasiet pogu **Atvērt, izmantojot Microsoft Office** un pēc tam sadaļā **Eksportēt uz Excel** atlasiet vienumu **Amati**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="bfc86-119">Vai arī nospiediet Ctrl+T.</span><span class="sxs-lookup"><span data-stu-id="bfc86-119">Alternatively, press Ctrl+T.</span></span>

    ![Saraksta lapas Amati eksports uz Excel](media/org-admin.png)

3. <span data-ttu-id="bfc86-121">Saglabājiet eksportēto Excel failu.</span><span class="sxs-lookup"><span data-stu-id="bfc86-121">Save the Excel file that is exported.</span></span>

    ![Dialogl. Eksp. uz Excel](media/export-excel.png)

4. <span data-ttu-id="bfc86-123">Pakalpojumā Visio atl. **Visio — izveidot jaunu** un atl. veidnes kateg. **Uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Jauna diagr](media/new.png)

5. <span data-ttu-id="bfc86-125">Atl. **Organizācijas diagr. vednis** un tad atl. **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Organizācijas diagr. vedņa dialogl.](media/orgchart-wizard.png)

6. <span data-ttu-id="bfc86-127">Atlasiet **Informācija, kas jau ir saglabāta failā vai datu bāzē** un tad atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="bfc86-129">Izv. **Teksta, Org Plus (\*.txt), vai Excel fails** un tad atl. **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="bfc86-131">Pārlūkojiet, lai atlasītu eksportēto Excel failu, kas satur amatu hierarhiju, un tad atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="bfc86-133">Iest. laukā **Nos.** vienumu **Amats**, iest. laukā **Sniedz pārsk.** vien. **Sniedz pārsk. amatam**, tad atl. **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="bfc86-135">Atlasiet laukus, kam jābūt redzamiem katrā zarā, un tad atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="bfc86-137">Pievienojiet kolonnu **Amats** sarakstā **Formas datu lauki** un tad atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Organiz. diagr. vednis 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="bfc86-139">Attēli pašlaik nav pieejami.</span><span class="sxs-lookup"><span data-stu-id="bfc86-139">Pictures aren't currently available.</span></span> <span data-ttu-id="bfc86-140">Tādēļ nākamajā lapā atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="bfc86-141">Atl. **Es vēlos, lai vednis automātiski sadala organizācijas diagrammu pa lappusēm**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Organiz. diagr. vednis 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="bfc86-143">Atl. **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="bfc86-143">Select **Finish**.</span></span>

    <span data-ttu-id="bfc86-144">Ja ir amati, kas nav iekļauti struktūrā, tiek parādīts uzaicinājums iekļaut tos diagrammā.</span><span class="sxs-lookup"><span data-stu-id="bfc86-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="bfc86-145">Pakalpojumā Visio ģenerētajā diagrammā katrs vadītājs redzams atsevišķā darblapā.</span><span class="sxs-lookup"><span data-stu-id="bfc86-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="bfc86-146">Pamatojoties uz laukiem, kas atlasīti iekļaušanai diagrammā, katrs zars rāda atbilstošu informāciju, kad tiek ģenerēts Visio fails.</span><span class="sxs-lookup"><span data-stu-id="bfc86-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hierarh. diagr.](media/hierarchy.png)

<span data-ttu-id="bfc86-148">**Papildu opcija**</span><span class="sxs-lookup"><span data-stu-id="bfc86-148">**Additional option**</span></span>

<span data-ttu-id="bfc86-149">Human Resources var lietot arī darbvietu **Personas**, lai skatītu ar hierarhiju saistīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="bfc86-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
