---
title: Pirmdokumentu audita ierobežojuma nosacījumu definēšana
description: Šajā tēmā ir izskaidrots, kā iestatīt un piemērot audita politikas noteikumus.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62ebe3d6ba1208bd5f9a2082969b1960c413c152
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836965"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="412b3-103">Pirmdokumentu audita ierobežojuma nosacījumu definēšana</span><span class="sxs-lookup"><span data-stu-id="412b3-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="412b3-104">Šajā tēmā ir izskaidrots, kā iestatīt un piemērot audita politikas noteikumus.</span><span class="sxs-lookup"><span data-stu-id="412b3-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="412b3-105">Piemērā tiek izmantotas izdevumu atskaites ar viesnīcu izdevumu tipu.</span><span class="sxs-lookup"><span data-stu-id="412b3-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="412b3-106">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="412b3-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="412b3-107">Auditora loma ietver šo uzdevumu veikšanai atbilstošās atļaujas.</span><span class="sxs-lookup"><span data-stu-id="412b3-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="412b3-108">Navigācijas rūtī ejiet uz **Moduļi > Audita darbvieta > Iestatīšana > Politikas noteikuma veids**.</span><span class="sxs-lookup"><span data-stu-id="412b3-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="412b3-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="412b3-109">Select **New**.</span></span>
3. <span data-ttu-id="412b3-110">Laukā **Noteikuma nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="412b3-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="412b3-111">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="412b3-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="412b3-112">Laukā **Vaicājuma nosaukums** atlasiet **Izdevumu atskaites rinda**</span><span class="sxs-lookup"><span data-stu-id="412b3-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="412b3-113">Laukā **Vaicājuma veids** atlasiet **Apkopot**</span><span class="sxs-lookup"><span data-stu-id="412b3-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="412b3-114">Laukā **Juridiskā persona** atlasiet **Juridiskā persona**</span><span class="sxs-lookup"><span data-stu-id="412b3-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="412b3-115">Laukā **Dokumenta datuma atsauce** atlasiet **Izmaiņu datums un laiks**.</span><span class="sxs-lookup"><span data-stu-id="412b3-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="412b3-116">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="412b3-116">Select **Save**.</span></span>
10. <span data-ttu-id="412b3-117">Navigācijas rūtī ejiet uz **Moduļi > Audita darbvieta > Iestatīšana > Audita politikas**.</span><span class="sxs-lookup"><span data-stu-id="412b3-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="412b3-118">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="412b3-118">Select **New**.</span></span>
12. <span data-ttu-id="412b3-119">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="412b3-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="412b3-120">Izvērsiet sadaļu **Politikas organizācijas**.</span><span class="sxs-lookup"><span data-stu-id="412b3-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="412b3-121">Kokā atlasiet **Contoso Entertainment System USA**, tad atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="412b3-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="412b3-122">Kokā atlasiet **Contoso Consulting USA**, tad atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="412b3-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="412b3-123">Kokā atlasiet **Contoso Retail USA**, tad atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="412b3-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="412b3-124">Sakļaujiet sadaļu **Politikas organizācijas**.</span><span class="sxs-lookup"><span data-stu-id="412b3-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="412b3-125">Izvērsiet sadaļu **Politikas noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="412b3-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="412b3-126">Sarakstā atrodiet un atlasiet iepriekš izveidoto ierobežojuma nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="412b3-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="412b3-127">Atlasiet **Izveidot ierobežojuma nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="412b3-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="412b3-128">Laukā **Spēkā stāšanās datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="412b3-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="412b3-129">Atlasiet **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="412b3-129">Select **Filter**.</span></span>
23. <span data-ttu-id="412b3-130">Sarakstā atlasiet **Izdevumu kategorijas** rindu un iestatiet detalizēto informāciju kā **Viesnīca**.</span><span class="sxs-lookup"><span data-stu-id="412b3-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="412b3-131">Ievadiet vai atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="412b3-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="412b3-132">Atlasiet cilni **Apkopot**.</span><span class="sxs-lookup"><span data-stu-id="412b3-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="412b3-133">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="412b3-133">Select **Add**.</span></span>
27. <span data-ttu-id="412b3-134">Sarakstā atlasiet vērtību laukam **Darījuma summa**.</span><span class="sxs-lookup"><span data-stu-id="412b3-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="412b3-135">Laukā **Lauks** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="412b3-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="412b3-136">Laukā **ApkopošanasFunkcija** atlasiet **Summa**.</span><span class="sxs-lookup"><span data-stu-id="412b3-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="412b3-137">Atlasiet cilni **Grupēt pēc**.</span><span class="sxs-lookup"><span data-stu-id="412b3-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="412b3-138">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="412b3-138">Select **Add**.</span></span>
32. <span data-ttu-id="412b3-139">Sarakstā atlasiet vērtību laukam **Darbinieks**.</span><span class="sxs-lookup"><span data-stu-id="412b3-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="412b3-140">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="412b3-140">Select **Add**.</span></span>
34. <span data-ttu-id="412b3-141">Sarakstā atlasiet vērtību laukam **Izdevumu kategorija**.</span><span class="sxs-lookup"><span data-stu-id="412b3-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="412b3-142">Laukā **Lauks** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="412b3-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="412b3-143">Atlasiet cilni **Ir rīcībā**.</span><span class="sxs-lookup"><span data-stu-id="412b3-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="412b3-144">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="412b3-144">Select **Add**.</span></span>
38. <span data-ttu-id="412b3-145">Atlasiet **Darījuma summa**.</span><span class="sxs-lookup"><span data-stu-id="412b3-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="412b3-146">Laukā **Lauks** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="412b3-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="412b3-147">Laukā **ApkopošanasFunkcija** atlasiet **Summa**.</span><span class="sxs-lookup"><span data-stu-id="412b3-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="412b3-148">Laukā **Kritēriji** ievadiet `>2000`.</span><span class="sxs-lookup"><span data-stu-id="412b3-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="412b3-149">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="412b3-149">Select **OK**.</span></span>
43. <span data-ttu-id="412b3-150">Atlasiet **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="412b3-150">Select **Test**.</span></span>
44. <span data-ttu-id="412b3-151">Laukā **Dokumenta atlases sākuma datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="412b3-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="412b3-152">Laukā **Dokumenta atlases beigu datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="412b3-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="412b3-153">Atlasiet **Veikt pārbaudi**.</span><span class="sxs-lookup"><span data-stu-id="412b3-153">Select **Run test**.</span></span>
47. <span data-ttu-id="412b3-154">Darbību rūtī atlasiet **Audita politika**.</span><span class="sxs-lookup"><span data-stu-id="412b3-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="412b3-155">Atlasiet **Papildu opcijas**.</span><span class="sxs-lookup"><span data-stu-id="412b3-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="412b3-156">Laukā **Sākuma datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="412b3-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="412b3-157">Laukā **Beigu datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="412b3-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="412b3-158">Atlasiet **Partija**.</span><span class="sxs-lookup"><span data-stu-id="412b3-158">Select **Batch**.</span></span>
52. <span data-ttu-id="412b3-159">Izvērsiet sadaļu **Darbināt fonā**.</span><span class="sxs-lookup"><span data-stu-id="412b3-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="412b3-160">Laukā **Partijas apstrāde** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="412b3-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="412b3-161">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="412b3-161">Select **OK**.</span></span>
55. <span data-ttu-id="412b3-162">Navigācijas rūtī ejiet uz **Moduļi > Audita darbvieta > Audita lietas**.</span><span class="sxs-lookup"><span data-stu-id="412b3-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="412b3-163">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="412b3-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="412b3-164">Izvērsiet sadaļu **Saistības**.</span><span class="sxs-lookup"><span data-stu-id="412b3-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="412b3-165">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="412b3-165">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]