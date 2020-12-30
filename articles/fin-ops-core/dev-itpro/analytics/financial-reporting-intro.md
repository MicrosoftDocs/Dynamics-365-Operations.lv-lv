---
title: Finanšu pārskatu veidošana
description: Finanšu pārskatu veidošana finanšu un biznesa speciālistiem ļauj veidot, uzturēt, izvietot un skatīt finanšu pārskatus. Tā pārvar tradicionālos pārskatu veidošanas ierobežojumus, lai jums palīdzētu efektīvi veidot dažāda veida pārskatus.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7da0d1aa4bb10658c66fce996e00b5714125f100
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682700"
---
# <a name="financial-reporting"></a><span data-ttu-id="e3624-104">Finanšu pārskatu veidošana</span><span class="sxs-lookup"><span data-stu-id="e3624-104">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3624-105">Finanšu atskaišu veidošana programmai finanšu un biznesa speciālistiem ļauj veidot, uzturēt, izvietot un skatīt finanšu atskaites.</span><span class="sxs-lookup"><span data-stu-id="e3624-105">Financial reporting for the application allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="e3624-106">Tā pārvar tradicionālos pārskatu veidošanas ierobežojumus, lai jums palīdzētu efektīvi veidot dažāda veida pārskatus.</span><span class="sxs-lookup"><span data-stu-id="e3624-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="e3624-107">Finanšu atskaišu veidošana ietver dimensiju atbalstu.</span><span class="sxs-lookup"><span data-stu-id="e3624-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="e3624-108">Tāpēc uzreiz ir pieejami kontu segmenti vai dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e3624-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="e3624-109">Nav nepieciešami nekādi papildu rīki vai konfigurācijas darbības.</span><span class="sxs-lookup"><span data-stu-id="e3624-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="e3624-110">Finanšu pārskatu iestatījumi</span><span class="sxs-lookup"><span data-stu-id="e3624-110">Financial reporting setup</span></span>
<span data-ttu-id="e3624-111">Lapā **Finanšu pārskatu iestatījumi** ir saraksts ar visām sistēmas finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="e3624-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="e3624-112">**Virsgrāmata** \> **Virsgrāmatas iestatīšana** \> **Finanšu pārskatu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="e3624-112">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="e3624-113">Lapā **Finanšu pārskatu iestatījumi** ir divas sadaļas, kas nosaka finanšu pārskatos ziņotos datus:</span><span class="sxs-lookup"><span data-stu-id="e3624-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="e3624-114">**Cilne Dimensijas** — tā kā dažādi uzņēmumi izmanto dažādas dimensijas un kontu struktūras, nav iespējams noteikt secību, kādā lietotāji pārskatos vēlas skatīt visas finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e3624-114">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="e3624-115">Šī lapa ļauj jums iestatīt secību, kādā vēlaties rādīt finanšu dimensijas, kad veidojat pārskatu līdzeklī Finanšu pārskati.</span><span class="sxs-lookup"><span data-stu-id="e3624-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="e3624-116">**Cilne Atribūti** ir vieta, kur varat atlasīt, vai filtrēšanai un pārskatu noformēšanai vēlaties spēt izmantot atribūtus **Kreditori** un **Debitori**.</span><span class="sxs-lookup"><span data-stu-id="e3624-116">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="e3624-117">Pārskatu veidošana par atribūtiem Kreditors un Debitors ir vērtīga tikai tad, ja transakciju grāmatošanas laikā vienā dokumentā neievadāt vairākus kreditorus vai debitorus.</span><span class="sxs-lookup"><span data-stu-id="e3624-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="e3624-118">Izvēloties atribūtu Kreditors un/vai Debitors, integrācijai tiek pievienots papildu laiks.</span><span class="sxs-lookup"><span data-stu-id="e3624-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="e3624-119">Finanšu atskaišu veidošanas komponenti</span><span class="sxs-lookup"><span data-stu-id="e3624-119">Financial reporting components</span></span>
<span data-ttu-id="e3624-120">Tālāk aprakstītie finanšu atskaišu veidošanas komponenti ļauj atskaites ērti veidot, skatīt un plānot.</span><span class="sxs-lookup"><span data-stu-id="e3624-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="e3624-121">Komponents</span><span class="sxs-lookup"><span data-stu-id="e3624-121">Component</span></span>        | <span data-ttu-id="e3624-122">Funkcijas</span><span class="sxs-lookup"><span data-stu-id="e3624-122">Functions</span></span> | <span data-ttu-id="e3624-123">Papildinformācija</span><span class="sxs-lookup"><span data-stu-id="e3624-123">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="e3624-124">Pārskata veidotājs</span><span class="sxs-lookup"><span data-stu-id="e3624-124">Report Designer</span></span>  | <span data-ttu-id="e3624-125">Izveidojiet atskaišu veidošanas blokus, kurus var kombinēt, lai definētu un ģenerētu atskaiti.</span><span class="sxs-lookup"><span data-stu-id="e3624-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="e3624-126">Pārskatu ceļvedis kalpo par veidošanas palīgrīku mazāk pieredzējušiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="e3624-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="e3624-127">Pieredzējuši lietotāji var veidot jaunus atskaišu veidošanas blokus vai modificēt jau esošos veidošanas blokus atbilstoši savām prasībām.</span><span class="sxs-lookup"><span data-stu-id="e3624-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="e3624-128">Pārskatu grafiki</span><span class="sxs-lookup"><span data-stu-id="e3624-128">Report schedules</span></span> | <span data-ttu-id="e3624-129">Plānojiet atsevišķu atskaiti vai atskaišu grupu, lai tās tiktu regulāri ģenerētas.</span><span class="sxs-lookup"><span data-stu-id="e3624-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="e3624-130">Ģenerēt finanšu pārskatus</span><span class="sxs-lookup"><span data-stu-id="e3624-130">Generate financial reports</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="e3624-131">Līdzekļi</span><span class="sxs-lookup"><span data-stu-id="e3624-131">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="e3624-132">Līdzeklis</span><span class="sxs-lookup"><span data-stu-id="e3624-132">Feature</span></span></th>
<th><span data-ttu-id="e3624-133">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e3624-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e3624-134">Pārskata noformējuma elastība</span><span class="sxs-lookup"><span data-stu-id="e3624-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="e3624-135">Kad veidojat atskaiti, atskaišu veidotājs nodrošina šādas atskaišu veidošanas opcijas.</span><span class="sxs-lookup"><span data-stu-id="e3624-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="e3624-136">Saglabāt dimensiju kombinācijas un atkārtoti lietot dimensijas vairākās atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="e3624-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="e3624-137">Kontrolēt, kā dimensiju apraksti tiek formatēti un attēloti.</span><span class="sxs-lookup"><span data-stu-id="e3624-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="e3624-138">Identificēt kontus vai dimensijas, kas nav ietverti pārskatu veidošanas blokos.</span><span class="sxs-lookup"><span data-stu-id="e3624-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="e3624-139">Formatēt virsrakstus slīdošās prognozēs.</span><span class="sxs-lookup"><span data-stu-id="e3624-139">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e3624-140">Sadarbība finanšu pārskatos</span><span class="sxs-lookup"><span data-stu-id="e3624-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="e3624-141">Šādas funkcijas palīdz pārvaldīt pārskatu ģenerēšanu un izplatīšanu.</span><span class="sxs-lookup"><span data-stu-id="e3624-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="e3624-142">Plānot atskaites, lai tās automātiski tiktu ģenerētas katru dienu, katru nedēļu, katru mēnesi vai katru gadu.</span><span class="sxs-lookup"><span data-stu-id="e3624-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="e3624-143">Eksportēt tikai lasāmu XPS formātu, kas sniedz labāku dokumentu drošību, izmantojot elektroniskos parakstus.</span><span class="sxs-lookup"><span data-stu-id="e3624-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="e3624-144">Eksportēt uz Microsoft Excel darblapu.</span><span class="sxs-lookup"><span data-stu-id="e3624-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="e3624-145">Lai atskaites kopīgotu, varat izveidot e-pasta ziņojumus, kas satur saites uz šīm atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="e3624-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e3624-146">Interaktīva pārskatu skatīšana</span><span class="sxs-lookup"><span data-stu-id="e3624-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="e3624-147">Interaktīvi līdzekļi jums ļauj veikt šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="e3624-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="e3624-148">Mainīt skatītās atskaites datumu.</span><span class="sxs-lookup"><span data-stu-id="e3624-148">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="e3624-149">Mainīt skatītas atskaites valūtu.</span><span class="sxs-lookup"><span data-stu-id="e3624-149">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="e3624-150">Skatīt atskaiti kopsavilkuma skatā vai detalizētajā skatā.</span><span class="sxs-lookup"><span data-stu-id="e3624-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="e3624-151">Pievienot dimensiju filtrus, lai ierobežotu atskaites saturu līdz noteiktai dimensijai vai dimensiju kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="e3624-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="e3624-152">Pievienot atribūtu filtrus, lai ierobežotu atskaites saturu līdz noteiktam atribūtam vai atribūtu kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="e3624-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="e3624-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e3624-153">Additional resources</span></span>
[<span data-ttu-id="e3624-154">Ģenerēt finanšu pārskatus</span><span class="sxs-lookup"><span data-stu-id="e3624-154">Generate financial reports</span></span>](generate-financial-report.md)
