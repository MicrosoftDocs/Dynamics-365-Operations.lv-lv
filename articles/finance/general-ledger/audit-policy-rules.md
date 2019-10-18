---
title: Audita ierobežojuma nosacījumi
description: Audita politiku var izmantot, lai novērtētu izdevumu pārskatus, kreditoru rēķinus un pirkšanas pasūtījumus, lai pārliecinātos, ka tie atbilst izveidotajiem politikas nosacījumiem. Visi ar audita politiku saistītie nosacījumi tiek izpildīti pakešuzdevuma režīmā saskaņā ar norādīto grafiku.  Katras politikas nosacījums ir politikas nosacījumu veida instance. Katram politikas nosacījumu veidam vienlaikus var būt aktīvs tikai viens politikas nosacījums.
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de6406029aa88424863dd9a47505f5b3ad27f237
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178810"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="11887-106">Audita ierobežojuma nosacījumi</span><span class="sxs-lookup"><span data-stu-id="11887-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11887-107">Audita politiku var izmantot, lai novērtētu izdevumu pārskatus, kreditoru rēķinus un pirkšanas pasūtījumus, lai pārliecinātos, ka tie atbilst izveidotajiem politikas nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="11887-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="11887-108">Visi ar audita politiku saistītie nosacījumi tiek izpildīti pakešuzdevuma režīmā saskaņā ar norādīto grafiku.</span><span class="sxs-lookup"><span data-stu-id="11887-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="11887-109">Katras politikas nosacījums ir politikas nosacījumu veida instance.</span><span class="sxs-lookup"><span data-stu-id="11887-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="11887-110">Katram politikas nosacījumu veidam vienlaikus var būt aktīvs tikai viens politikas nosacījums.</span><span class="sxs-lookup"><span data-stu-id="11887-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="11887-111">Vaicājumi un vaicājumu veidi</span><span class="sxs-lookup"><span data-stu-id="11887-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="11887-112">Veidojot audita politikas nosacījumu, vispirms ir jāatlasa politikas nosacījuma veids.</span><span class="sxs-lookup"><span data-stu-id="11887-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="11887-113">Politikas nosacījuma veids nosaka lietojumprogrammas objektu koka (AOT) vaicājumu, ar ko sāk politikas nosacījuma izveidi.</span><span class="sxs-lookup"><span data-stu-id="11887-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="11887-114">Tas arī norāda vaicājuma veidu, ko izmanto politikas nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="11887-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="11887-115">Vaicājums nosaka pirmdokumentu, kuru novērtē politikas nosacījums.</span><span class="sxs-lookup"><span data-stu-id="11887-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="11887-116">Tas arī norāda laukus pirmdokumentā, kas identificē gan juridisku personu, gan datumu, kas jāizmanto, kad auditam tiek atlasīti dokumenti.</span><span class="sxs-lookup"><span data-stu-id="11887-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="11887-117">Vaicājuma veids kontrolē noklusējuma laukus vaicājuma lapā un lapā Audita ierobežojuma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="11887-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="11887-118">Šajā tabulā ir parādīti vaicājumu veidi, kas pieejami audita politikas nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="11887-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11887-119">Vaicājuma tips</span><span class="sxs-lookup"><span data-stu-id="11887-119">Query type</span></span></th>
<th><span data-ttu-id="11887-120">Mērķis</span><span class="sxs-lookup"><span data-stu-id="11887-120">Purpose</span></span></th>
<th><span data-ttu-id="11887-121">Papildinformācija</span><span class="sxs-lookup"><span data-stu-id="11887-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11887-122">Nosacījuma</span><span class="sxs-lookup"><span data-stu-id="11887-122">Conditional</span></span></td>
<td><span data-ttu-id="11887-123">Novērtējiet pirmdokumenta atribūtus, salīdzinot tos ar norādītām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="11887-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11887-124">Apkopot</span><span class="sxs-lookup"><span data-stu-id="11887-124">Aggregate</span></span></td>
<td><span data-ttu-id="11887-125">Novērtējiet vairākus pirmdokumentus vai pirmdokumentu rindas, salīdzinot tos ar politikas nosacījumu, apkopojot skaitliskās vērtības.</span><span class="sxs-lookup"><span data-stu-id="11887-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11887-126">Iztveršana</span><span class="sxs-lookup"><span data-stu-id="11887-126">Sampling</span></span></td>
<td><span data-ttu-id="11887-127">Nejaušā secībā atlasiet noteiktu pirmdokumentu procentuālo daļu, lai novērtētu politikas pārkāpumus.</span><span class="sxs-lookup"><span data-stu-id="11887-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="11887-128">Kad šī opcija ir atlasīta, jālieto lapa Audita ierobežojuma nosacījumi, lai norādītu dokumentu procentuālo vērtību, kas nejaušā secībā jāatlasa auditam.</span><span class="sxs-lookup"><span data-stu-id="11887-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11887-129">Dublēt</span><span class="sxs-lookup"><span data-stu-id="11887-129">Duplicate</span></span></td>
<td><span data-ttu-id="11887-130">Novērtējiet pirmdokumentus, lai noteiktu, vai tie satur dublējošos ierakstus norādītajos laukos.</span><span class="sxs-lookup"><span data-stu-id="11887-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="11887-131">Ja šī opcija ir atlasīta, izmantojiet lapu Audita ierobežojuma nosacījumi, lai norādītu dienu skaitu, kas jāpievieno dokumentu atlases datumu diapazona sākumam, kad dokumenti tiek novērtēti uz dublējošo ierakstu klātbūtni.</span><span class="sxs-lookup"><span data-stu-id="11887-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11887-132">Meklēšana sarakstā</span><span class="sxs-lookup"><span data-stu-id="11887-132">List search</span></span></td>
<td><span data-ttu-id="11887-133">Novērtējiet pirmdokumentus uz noteikto entītiju klātbūtni.</span><span class="sxs-lookup"><span data-stu-id="11887-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="11887-134">Vaicājuma saknes dokuments nosaka dokumentu, kuram tiek veikts audits.</span><span class="sxs-lookup"><span data-stu-id="11887-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="11887-135">Vaicājumam jābūt saraksta formā, kurā ietverta atsauce uz tabulu DirPartyTable.</span><span class="sxs-lookup"><span data-stu-id="11887-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="11887-136">Šo opciju var izmantot tikai šādiem AOT vaicājumiem:</span><span class="sxs-lookup"><span data-stu-id="11887-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="11887-137"><span class="ui">AuditPolicyExpenseList</span> (Izdevumu pārskatā pārraudzītie darbinieki)</span><span class="sxs-lookup"><span data-stu-id="11887-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="11887-138"><span class="ui">AuditPolicyPurchList</span> (Pirkšanas pasūtījumā pārraudzītie kreditori)</span><span class="sxs-lookup"><span data-stu-id="11887-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="11887-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Kreditora rēķinā pārraudzītie kreditori)</span><span class="sxs-lookup"><span data-stu-id="11887-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="11887-140">Atlasot šo opciju, norādiet uzraugāmās entītijas lapā Audita ierobežojuma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="11887-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11887-141">Meklēšana pēc atslēgvārdiem</span><span class="sxs-lookup"><span data-stu-id="11887-141">Keyword search</span></span></td>
<td><span data-ttu-id="11887-142">Novērtējiet pirmdokumentus, lai noteiktu, vai tie satur noteiktus vārdus.</span><span class="sxs-lookup"><span data-stu-id="11887-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="11887-143">Atlasot šo opciju, ievadiet meklējamos terminus lapā Audita ierobežojuma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="11887-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="11887-144">Lapā Audita ierobežojuma nosacījumi ir ietvertas arī opcijas, kas ļauj norādīt tabulas un laukus, kurām novērtēt ievadītos vārdus.</span><span class="sxs-lookup"><span data-stu-id="11887-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="11887-145">Vispārīgie parametri</span><span class="sxs-lookup"><span data-stu-id="11887-145">Common parameters</span></span>
<span data-ttu-id="11887-146">Visiem noteiktas audita politikas nosacījumiem ir vienādi pakešuzdevumu parametri un vienāds dokumentu atlases datumu diapazons.</span><span class="sxs-lookup"><span data-stu-id="11887-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="11887-147">Šie parametri tiek norādīti politikai lapā Audita ierobežojuma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="11887-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="11887-148">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="11887-148">Additional resources</span></span>
--------

<span data-ttu-id="11887-149">[Audita ierobežojuma nosacījumu pārkāpumi un gadījumi](audit-policy-violations-cases.md)
[Definēt pirmdokumentu audita politikas](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="11887-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>


