---
title: Pirmdokumentu audita ierobežojuma nosacījumu definēšana
description: Šajā tēmā ir izskaidrots, kā iestatīt un piemērot audita politikas noteikumus.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba720fd1bbbbf8b4f3b936d65d9d7840432f291a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445671"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="4876c-103">Pirmdokumentu audita ierobežojuma nosacījumu definēšana</span><span class="sxs-lookup"><span data-stu-id="4876c-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4876c-104">Šajā tēmā ir izskaidrots, kā iestatīt un piemērot audita politikas noteikumus.</span><span class="sxs-lookup"><span data-stu-id="4876c-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="4876c-105">Piemērā tiek izmantotas izdevumu atskaites ar viesnīcu izdevumu tipu.</span><span class="sxs-lookup"><span data-stu-id="4876c-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="4876c-106">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="4876c-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="4876c-107">Auditora loma ietver šo uzdevumu veikšanai atbilstošās atļaujas.</span><span class="sxs-lookup"><span data-stu-id="4876c-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="4876c-108">Navigācijas rūtī ejiet uz **Moduļi > Audita darbvieta > Iestatīšana > Politikas noteikuma veids**.</span><span class="sxs-lookup"><span data-stu-id="4876c-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="4876c-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4876c-109">Select **New**.</span></span>
3. <span data-ttu-id="4876c-110">Laukā **Noteikuma nosaukums** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4876c-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="4876c-111">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4876c-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="4876c-112">Laukā **Vaicājuma nosaukums** atlasiet **Izdevumu atskaites rinda**</span><span class="sxs-lookup"><span data-stu-id="4876c-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="4876c-113">Laukā **Vaicājuma veids** atlasiet **Apkopot**</span><span class="sxs-lookup"><span data-stu-id="4876c-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="4876c-114">Laukā **Juridiskā persona** atlasiet **Juridiskā persona**</span><span class="sxs-lookup"><span data-stu-id="4876c-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="4876c-115">Laukā **Dokumenta datuma atsauce** atlasiet **Izmaiņu datums un laiks**.</span><span class="sxs-lookup"><span data-stu-id="4876c-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="4876c-116">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="4876c-116">Select **Save**.</span></span>
10. <span data-ttu-id="4876c-117">Navigācijas rūtī ejiet uz **Moduļi > Audita darbvieta > Iestatīšana > Audita politikas**.</span><span class="sxs-lookup"><span data-stu-id="4876c-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="4876c-118">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="4876c-118">Select **New**.</span></span>
12. <span data-ttu-id="4876c-119">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4876c-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="4876c-120">Izvērsiet sadaļu **Politikas organizācijas**.</span><span class="sxs-lookup"><span data-stu-id="4876c-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="4876c-121">Kokā atlasiet **Contoso Entertainment System USA**, tad atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="4876c-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="4876c-122">Kokā atlasiet **Contoso Consulting USA**, tad atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="4876c-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="4876c-123">Kokā atlasiet **Contoso Retail USA**, tad atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="4876c-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="4876c-124">Sakļaujiet sadaļu **Politikas organizācijas**.</span><span class="sxs-lookup"><span data-stu-id="4876c-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="4876c-125">Izvērsiet sadaļu **Politikas noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="4876c-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="4876c-126">Sarakstā atrodiet un atlasiet iepriekš izveidoto ierobežojuma nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="4876c-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="4876c-127">Atlasiet **Izveidot ierobežojuma nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="4876c-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="4876c-128">Laukā **Spēkā stāšanās datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4876c-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="4876c-129">Atlasiet **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="4876c-129">Select **Filter**.</span></span>
23. <span data-ttu-id="4876c-130">Sarakstā atlasiet **Izdevumu kategorijas** rindu un iestatiet detalizēto informāciju kā **Viesnīca**.</span><span class="sxs-lookup"><span data-stu-id="4876c-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="4876c-131">Ievadiet vai atlasiet vērtību laukā **Kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="4876c-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="4876c-132">Atlasiet cilni **Apkopot**.</span><span class="sxs-lookup"><span data-stu-id="4876c-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="4876c-133">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="4876c-133">Select **Add**.</span></span>
27. <span data-ttu-id="4876c-134">Sarakstā atlasiet vērtību laukam **Darījuma summa**.</span><span class="sxs-lookup"><span data-stu-id="4876c-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="4876c-135">Laukā **Lauks** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4876c-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="4876c-136">Laukā **ApkopošanasFunkcija** atlasiet **Summa**.</span><span class="sxs-lookup"><span data-stu-id="4876c-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="4876c-137">Atlasiet cilni **Grupēt pēc**.</span><span class="sxs-lookup"><span data-stu-id="4876c-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="4876c-138">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="4876c-138">Select **Add**.</span></span>
32. <span data-ttu-id="4876c-139">Sarakstā atlasiet vērtību laukam **Darbinieks**.</span><span class="sxs-lookup"><span data-stu-id="4876c-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="4876c-140">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="4876c-140">Select **Add**.</span></span>
34. <span data-ttu-id="4876c-141">Sarakstā atlasiet vērtību laukam **Izdevumu kategorija**.</span><span class="sxs-lookup"><span data-stu-id="4876c-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="4876c-142">Laukā **Lauks** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4876c-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="4876c-143">Atlasiet cilni **Ir rīcībā**.</span><span class="sxs-lookup"><span data-stu-id="4876c-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="4876c-144">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="4876c-144">Select **Add**.</span></span>
38. <span data-ttu-id="4876c-145">Atlasiet **Darījuma summa**.</span><span class="sxs-lookup"><span data-stu-id="4876c-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="4876c-146">Laukā **Lauks** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4876c-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="4876c-147">Laukā **ApkopošanasFunkcija** atlasiet **Summa**.</span><span class="sxs-lookup"><span data-stu-id="4876c-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="4876c-148">Laukā **Kritēriji** ievadiet `>2000`.</span><span class="sxs-lookup"><span data-stu-id="4876c-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="4876c-149">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4876c-149">Select **OK**.</span></span>
43. <span data-ttu-id="4876c-150">Atlasiet **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="4876c-150">Select **Test**.</span></span>
44. <span data-ttu-id="4876c-151">Laukā **Dokumenta atlases sākuma datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4876c-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="4876c-152">Laukā **Dokumenta atlases beigu datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4876c-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="4876c-153">Atlasiet **Veikt pārbaudi**.</span><span class="sxs-lookup"><span data-stu-id="4876c-153">Select **Run test**.</span></span>
47. <span data-ttu-id="4876c-154">Darbību rūtī atlasiet **Audita politika**.</span><span class="sxs-lookup"><span data-stu-id="4876c-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="4876c-155">Atlasiet **Papildu opcijas**.</span><span class="sxs-lookup"><span data-stu-id="4876c-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="4876c-156">Laukā **Sākuma datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4876c-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="4876c-157">Laukā **Beigu datums** ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4876c-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="4876c-158">Atlasiet **Partija**.</span><span class="sxs-lookup"><span data-stu-id="4876c-158">Select **Batch**.</span></span>
52. <span data-ttu-id="4876c-159">Izvērsiet sadaļu **Darbināt fonā**.</span><span class="sxs-lookup"><span data-stu-id="4876c-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="4876c-160">Laukā **Partijas apstrāde** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4876c-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="4876c-161">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4876c-161">Select **OK**.</span></span>
55. <span data-ttu-id="4876c-162">Navigācijas rūtī ejiet uz **Moduļi > Audita darbvieta > Audita lietas**.</span><span class="sxs-lookup"><span data-stu-id="4876c-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="4876c-163">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4876c-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="4876c-164">Izvērsiet sadaļu **Saistības**.</span><span class="sxs-lookup"><span data-stu-id="4876c-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="4876c-165">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4876c-165">In the list, find and select the desired record.</span></span>

