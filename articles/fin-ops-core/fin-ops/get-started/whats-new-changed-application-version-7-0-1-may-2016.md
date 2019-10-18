---
title: Jaunumi un izmaiņas Dynamics AX programmas versijā 7.0.1 (2016. gada maijs)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti Microsoft Dynamics AX programmas versijā 7.0.1. Šī versija tika izlaista 2016. gada maijā, un tās būvējuma numurs ir 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6bd40873d6890bc837188cba1aa1125d874f6bda
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178964"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="19aa8-104">Jaunumi un izmaiņas Dynamics AX programmas versijā 7.0.1 (2016. gada maijs)</span><span class="sxs-lookup"><span data-stu-id="19aa8-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19aa8-105">Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti Microsoft Dynamics AX programmas versijā 7.0.1.</span><span class="sxs-lookup"><span data-stu-id="19aa8-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="19aa8-106">Šī versija tika izlaista 2016. gada maijā, un tās būvējuma numurs ir 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="19aa8-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="19aa8-107">Elektronisko atskaišu veidošana (ER)</span><span class="sxs-lookup"><span data-stu-id="19aa8-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="19aa8-108">Ko iespējams izdarīt?</span><span class="sxs-lookup"><span data-stu-id="19aa8-108">What can you do?</span></span> | <span data-ttu-id="19aa8-109">Kāpēc tas ir svarīgi?</span><span class="sxs-lookup"><span data-stu-id="19aa8-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="19aa8-110">Konfigurējiet izpildlaika dialoglodziņu elektronisko atskaišu veidošanas (Electronic reporting —ER) atskaišu noformēšanai, lai lietotāji varētu izvēlēties vēlamās finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="19aa8-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="19aa8-111">Izpildlaikā ER atskaites izpildes dialoglodziņā lietotāji var atlasīt vairākas finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="19aa8-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="19aa8-112">Atlasīto finanšu dimensiju detalizētā informācija tiek rādīta elektroniskajā dokumentā, kas tiek ģenerēts.</span><span class="sxs-lookup"><span data-stu-id="19aa8-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="19aa8-113">Konfigurēt piekļuvi vairākām finanšu dimensijām ER atskaites veidošanas laikā, izmantojot vienu kartēšanu uz nepieciešamo datu avotu.</span><span class="sxs-lookup"><span data-stu-id="19aa8-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="19aa8-114">To pašu ER atskaites konfigurāciju var izmantot, lai veidotu elektroniskus dokumentus, kuros transakciju dati ir norādīti kopā ar informāciju par finanšu dimensijām, neatkarīgi no lietotāja atlasīto vai pašreizējai juridiskajai personai vai instancei konfigurēto finanšu dimensiju skaita.</span><span class="sxs-lookup"><span data-stu-id="19aa8-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="19aa8-115">Konfigurējiet ER atskaiti, lai ievadītu datus dinamiski ģenerētās elektroniska dokumenta kolonnās, kurš tiek veidots OPENXML darblapas formātā.</span><span class="sxs-lookup"><span data-stu-id="19aa8-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="19aa8-116">ER atskaite var ievadīt datus OPENXML darblapā, kas tiek ģenerēta, horizontāli replicējot kolonnas.</span><span class="sxs-lookup"><span data-stu-id="19aa8-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="19aa8-117">Līdz ar to tādu pašu ER atskaites konfigurāciju var izmantot atkārtoti, lai ģenerētu elektroniskus dokumentus, kuros ir atšķirīgs dinamiski ģenerēto kolonnu skaits.</span><span class="sxs-lookup"><span data-stu-id="19aa8-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="19aa8-118">Konfigurējiet ER galamērķus, lai formāta izvades rezultāts būtu vērsts uz konkrētu galamērķi: failu, e-pasta ziņojumu vai arhīvu (Microsoft SharePoint mape vai Microsoft Azure krātuve).</span><span class="sxs-lookup"><span data-stu-id="19aa8-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="19aa8-119">Iepriekš, kad izpildījāt ER konfigurēšanu, tika parādīts ziņojuma lodziņš, kas lietotājam pieprasīja kaut ko darīt, lai failu saglabātu vai atvērtu.</span><span class="sxs-lookup"><span data-stu-id="19aa8-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="19aa8-120">Tagad varat jau iepriekš konfigurēt adresātu katrai formāta konfigurācijai un katram izvades komponentam (mapei vai failam) atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="19aa8-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="19aa8-121">Lietotāji, kuriem ir atbilstošas piekļuves tiesības, mērķa iestatījumus var modificēt arī izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="19aa8-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="19aa8-122">POS – Microsoft Dynamics AX Retail</span><span class="sxs-lookup"><span data-stu-id="19aa8-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="19aa8-123">Ko iespējams izdarīt?</span><span class="sxs-lookup"><span data-stu-id="19aa8-123">What can you do?</span></span> | <span data-ttu-id="19aa8-124">Kāpēc tas ir svarīgi?</span><span class="sxs-lookup"><span data-stu-id="19aa8-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="19aa8-125">Izmantojiet pārlūku Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="19aa8-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="19aa8-126">Mazumtirgotāji tagad var palaist Cloud POS no pārlūkprogrammas Chrome un var baudīt visu funkcionalitāti, kas ir pieejama Cloud POS Microsoft Edge un Internet Explorer versijā.</span><span class="sxs-lookup"><span data-stu-id="19aa8-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="19aa8-127">Finanšu pārskati</span><span class="sxs-lookup"><span data-stu-id="19aa8-127">Financial reporting</span></span>

| <span data-ttu-id="19aa8-128">Ko iespējams izdarīt?</span><span class="sxs-lookup"><span data-stu-id="19aa8-128">What can you do?</span></span> | <span data-ttu-id="19aa8-129">Kāpēc tas ir svarīgi?</span><span class="sxs-lookup"><span data-stu-id="19aa8-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="19aa8-130">Atkārtoti izveidojiet finanšu atskaišu veidošanas datuvi.</span><span class="sxs-lookup"><span data-stu-id="19aa8-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="19aa8-131">Ja Dynamics AX datu bāze tiek pārvietota uz citu vidi vai tiek veiktas citas būtiskas vides izmaiņas, iespējams, ir atkārtoti jāizveido finanšu pārskatu datu bāze.</span><span class="sxs-lookup"><span data-stu-id="19aa8-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="19aa8-132">Tagad ir pieejams Windows PowerShell skripts, kas nodrošina datu bāzes atkārtotu izveidi.</span><span class="sxs-lookup"><span data-stu-id="19aa8-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="19aa8-133">Vairs nevarat atlasīt atskaišu veidotāja opcijas, kas nav derīgas.</span><span class="sxs-lookup"><span data-stu-id="19aa8-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="19aa8-134">Vairākas atskaišu veidotāja opcijas, kas tika izmantotas tirgū pieejamajās Management Reporter versijās, netiek izmantotas šajā Dynamics AX versijā.</span><span class="sxs-lookup"><span data-stu-id="19aa8-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="19aa8-135">Šīs opcijas bija saistītas ar finanšu pārskatu izstrādi, izvadi un saistīšanu.</span><span class="sxs-lookup"><span data-stu-id="19aa8-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="19aa8-136">Šīs opcijas ir noņemtas no finanšu pārskatu veidotāja, lai nepieļautu lietotāja kļūdas.</span><span class="sxs-lookup"><span data-stu-id="19aa8-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="19aa8-137">Finanšu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="19aa8-137">Financial management</span></span>

| <span data-ttu-id="19aa8-138">Ko iespējams izdarīt?</span><span class="sxs-lookup"><span data-stu-id="19aa8-138">What can you do?</span></span> | <span data-ttu-id="19aa8-139">Kāpēc tas ir svarīgi?</span><span class="sxs-lookup"><span data-stu-id="19aa8-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="19aa8-140">Ģenerējiet pozitīvo maksājumu failus kreditoriem veicamajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="19aa8-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="19aa8-141">Pozitīvā maksājuma failus var ģenerēt, lai palīdzētu novērst krāpšanos ar čekiem.</span><span class="sxs-lookup"><span data-stu-id="19aa8-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="19aa8-142">Noliktava un ražošana</span><span class="sxs-lookup"><span data-stu-id="19aa8-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19aa8-143">Ko iespējams izdarīt?</span><span class="sxs-lookup"><span data-stu-id="19aa8-143">What can you do?</span></span></th>
<th><span data-ttu-id="19aa8-144">Kāpēc tas ir svarīgi?</span><span class="sxs-lookup"><span data-stu-id="19aa8-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19aa8-145">Definējiet noliktavas darba politiku, kas kontrolē darba izveidošanu preču kopai konkrētos novietojumos.</span><span class="sxs-lookup"><span data-stu-id="19aa8-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="19aa8-146">Ne vienmēr noliktavas procesi ietver darbu.</span><span class="sxs-lookup"><span data-stu-id="19aa8-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="19aa8-147">Izmantojot jauno noliktavu darba politiku, varat novērst darba izveidošanu izejmateriālu izdošanai un gatavās produkcijas izvietošanai kādai preču kopai konkrētos novietojumos.</span><span class="sxs-lookup"><span data-stu-id="19aa8-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19aa8-148">Norādiet, ka ražošanas izlaides novietojums nav atkarīgs no numura zīmes.</span><span class="sxs-lookup"><span data-stu-id="19aa8-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="19aa8-149">Tagad varat norādīt, ka preces izvades novietojums nav atkarīgs no numura zīmes.</span><span class="sxs-lookup"><span data-stu-id="19aa8-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="19aa8-150">Piemēram, šis līdzeklis noder, kad augšupstraumes ražošanas pasūtījums par krājumiem kā pabeigtiem ziņo tieši uz novietojumu, kas darbojas kā ražošanas ievades novietojums kādam lejupstraumes ražošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="19aa8-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19aa8-151">Atbalstiet MK, kuros ir ietverti krājumi ar tā paša krājuma atšķirīgām preces dimensijām.</span><span class="sxs-lookup"><span data-stu-id="19aa8-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="19aa8-152">Ja ražošanā lietojat vienu vai vairākas preces dimensijas, var rasties situācijas, kad vēlaties ražot kādu krājumu, balstoties uz citu tā paša krājuma variantu.</span><span class="sxs-lookup"><span data-stu-id="19aa8-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="19aa8-153">Papildinformāciju skatiet <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">šajā emuārā</a>.</span><span class="sxs-lookup"><span data-stu-id="19aa8-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19aa8-154">Ražošanas pasūtījumi ar cikliskajām struktūrām to MK pirmajā līmenī tiek izslēgtas no MK līmeņa aprēķina materiālo resursu plānošanai.</span><span class="sxs-lookup"><span data-stu-id="19aa8-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="19aa8-155">Nav iespējams piešķirt pareizus MK līmeņus preču variantiem tādos ražošanas pasūtījumos, kas MK hierarhijā izraisa cikliskumu.</span><span class="sxs-lookup"><span data-stu-id="19aa8-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19aa8-156">Aprēķiniet atsevišķus MK līmeņus materiālo resursu plānošanai un izmaksu aprēķinam:</span><span class="sxs-lookup"><span data-stu-id="19aa8-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="19aa8-157">Materiālo resursu plānošanai MK līmeņi tiek aprēķināti jaunajā tabulā <strong>ReqItemLevel</strong>.</span><span class="sxs-lookup"><span data-stu-id="19aa8-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="19aa8-158">Pabeigtie ražošanas pasūtījumi šajā aprēķinā netiek ņemti vērā.</span><span class="sxs-lookup"><span data-stu-id="19aa8-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="19aa8-159">Ražošanas izmaksu aprēķināšanai MK līmeņi tiek aprēķināti tabulā <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="19aa8-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="19aa8-160">Pabeigtie ražošanas pasūtījumi tiek iekļauti šajā aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="19aa8-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="19aa8-161">Izpildot materiālo resursu plānošanu, piemēram, vispārējās plānošanas plāna grafika izveidošanu un izvēršanu, ir nepieciešams pārrēķināt tikai tos MK līmeņus, kas tika izmantoti materiālo resursu plānošanai.</span><span class="sxs-lookup"><span data-stu-id="19aa8-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="19aa8-162">Citiem vārdiem sakot, nav nepieciešams aprēķināt ražošanas izmaksu aprēķināšanai izmantotos MK līmeņus.</span><span class="sxs-lookup"><span data-stu-id="19aa8-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="19aa8-163">Izpildot izmaksu aprēķināšanas operācijas, piemēram, krājumu slēgšanu, ir jāpārrēķina tikai tie MK līmeņi, kas ir izmantoti ražošanas izmaksu aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="19aa8-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="19aa8-164">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="19aa8-164">Additional resources</span></span>

[<span data-ttu-id="19aa8-165">Jaunumi un izmaiņas</span><span class="sxs-lookup"><span data-stu-id="19aa8-165">What's new or changed</span></span>](whats-new-changed.md)

[<span data-ttu-id="19aa8-166">Jauni vai atjaunināti uzdevumu ceļveži (2016. gada maijs)</span><span class="sxs-lookup"><span data-stu-id="19aa8-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
