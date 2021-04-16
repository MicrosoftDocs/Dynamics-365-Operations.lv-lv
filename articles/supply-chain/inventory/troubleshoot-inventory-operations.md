---
title: Krājumu problēmu novēršanas operācijas
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar krājumu darbībām.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832062"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="672bd-103">Krājumu problēmu novēršanas operācijas</span><span class="sxs-lookup"><span data-stu-id="672bd-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="672bd-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar krājumu darbībām.</span><span class="sxs-lookup"><span data-stu-id="672bd-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="672bd-105">Nevar atrast nolaižamo dialoglodziņu Darbplūsma krājumu žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="672bd-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="672bd-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="672bd-106">Issue description</span></span>

<span data-ttu-id="672bd-107">Žurnāla lapā nevar atrast **Darbplūsmas** nolaižamo dialoglodziņu, vai arī saistītās darbplūsmas operācijas nav pieejamas.</span><span class="sxs-lookup"><span data-stu-id="672bd-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="672bd-108">Šī problēma var rasties trīs iemeslu dēļ, kā aprakstīts tālāk aprakstītajās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="672bd-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="672bd-109">1. problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="672bd-109">Issue resolution 1</span></span>

<span data-ttu-id="672bd-110">Ja problēma attiecas uz visiem lietotājiem, var rasties, jo apstiprināšanas darbplūsma nav piešķirta žurnāla nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="672bd-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="672bd-111">Lai novērstu problēmu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="672bd-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="672bd-112">Dodieties uz **Krājumu pārvaldība &gt; Iestatīšana &gt; Žurnālu nosaukumi &gt; Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="672bd-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="672bd-113">Atlasiet žurnāla nosaukumu no saraksta kolonnas, lai atvērtu tās iestatījumu lapu.</span><span class="sxs-lookup"><span data-stu-id="672bd-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="672bd-114">Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Darbplūsmas apstiprināšana** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="672bd-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="672bd-115">Atlasiet **Jā**, ja jums tiek piedāvāts apstiprināt izmaiņās.</span><span class="sxs-lookup"><span data-stu-id="672bd-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="672bd-116">Laukā **Darbplūsma** atlasiet izdevumu pārskatītāju konfigurāciju, kuru vēlaties izmantot šim atlasītajam žurnāla nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="672bd-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="672bd-117">2. problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="672bd-117">Issue resolution 2</span></span>

<span data-ttu-id="672bd-118">Ja darbplūsma izmanto pielāgotu kodu, pēc sistēmas jaunināšanas var rasties problēmas.</span><span class="sxs-lookup"><span data-stu-id="672bd-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="672bd-119">Piemēram, žurnāla darbplūsmā poga **Iesniegt** var būt pelēkota, tāpēc jūs nevarat to atlasīt, lai apstiprinātu iesniegšanu.</span><span class="sxs-lookup"><span data-stu-id="672bd-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="672bd-120">Ja poga **Iesniegt** ir iepelēkota, iespējams, ka darbplūsma ir pielāgota, kas nozīmē darbplūsmas metodi, sadaļā `canSubmitToWorkflow()`ir `FormDataUtil`paplašināta.</span><span class="sxs-lookup"><span data-stu-id="672bd-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="672bd-121">Lai novērstu šo problēmu, mainiet veidu, kā paplašināt metodes `canSubmitToWorkflow()`struktūras izmantošanai šajā piemērā.</span><span class="sxs-lookup"><span data-stu-id="672bd-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="672bd-122">3. problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="672bd-122">Issue resolution 3</span></span>

<span data-ttu-id="672bd-123">Ja problēma attiecas tikai uz dažiem specifiskiem lietotājiem, iespējams, šiem lietotājiem nav drošības privilēģiju, kas nepieciešamas darbplūsmas operāciju palaišanai krājumu žurnālos.</span><span class="sxs-lookup"><span data-stu-id="672bd-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="672bd-124">Pārbaudiet, vai katram ietekmētam lietotājam ir drošības privilēģija *Uzturēt krājumu žurnāla darbplūsmu*.</span><span class="sxs-lookup"><span data-stu-id="672bd-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="672bd-125">Pēc noklusējuma šī privilēģija tiek piešķirta pienākumam ar tādu pašu nosaukumu un šis pienākums tiek attiecināts uz lomām *Noliktavas darbinieks* un *Noliktavas vadītājs*.</span><span class="sxs-lookup"><span data-stu-id="672bd-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="672bd-126">Mans krājumu žurnāls paliek sistēmas bloķētā statusā un darbplūsmas pakešuzdevums nedarbojas.</span><span class="sxs-lookup"><span data-stu-id="672bd-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="672bd-127">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="672bd-127">Issue description</span></span>

<span data-ttu-id="672bd-128">Kādu no jūsu krājumu žurnāliem ir bloķējusi kāda operācija un tā nav nodota izpildei.</span><span class="sxs-lookup"><span data-stu-id="672bd-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="672bd-129">Piemēram, ja grāmatošanas laikā rodas nezināma kļūda (kas ir sistēmas bloķēšanas operācija), žurnālam var būt sistēmas bloķēts statuss.</span><span class="sxs-lookup"><span data-stu-id="672bd-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="672bd-130">Šajā gadījumā darbplūsmas darba vienuma apdarinātājam rodas kļūda, bloķējot validāciju.</span><span class="sxs-lookup"><span data-stu-id="672bd-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="672bd-131">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="672bd-131">Issue resolution</span></span>

<span data-ttu-id="672bd-132">Piesakieties SQL Server instancē Supply Chain Management un pārbaudiet, vai **InventJournalTable.SystemBlocked** ir iestatīts uz *1*.</span><span class="sxs-lookup"><span data-stu-id="672bd-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="672bd-133">Pārliecinieties, vai žurnāla statuss nav bloķēts, un pēc tam atiestatiet **InventJournalTable.SystemBlocked** uz *0*.</span><span class="sxs-lookup"><span data-stu-id="672bd-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="672bd-134">Mana krājumu žurnāla darbplūsma nekad netiek pabeigta, un žurnālu nevar rediģēt vai grāmatot.</span><span class="sxs-lookup"><span data-stu-id="672bd-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="672bd-135">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="672bd-135">Issue description</span></span>

<span data-ttu-id="672bd-136">Kad esat iesniedzis žurnāla apstiprināšanas darbplūsmu, darbplūsmas apstrāde pārstāj reaģēt un jūs nevarat rediģēt vai apstrādāt žurnālus.</span><span class="sxs-lookup"><span data-stu-id="672bd-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="672bd-137">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="672bd-137">Issue resolution</span></span>

<span data-ttu-id="672bd-138">Ir vairāki iemesli, kādēļ darbplūsmas apstrāde var nebūt pabeigta.</span><span class="sxs-lookup"><span data-stu-id="672bd-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="672bd-139">Pārbaudiet šādas problēmas:</span><span class="sxs-lookup"><span data-stu-id="672bd-139">Check for the following issues:</span></span>

- <span data-ttu-id="672bd-140">Dodieties uz **Krājumu pārvaldība &gt; Iestatījumi &gt; Krājumu pārvaldības darbplūsmas** un pārskatiet ietekmētās darbplūsmas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="672bd-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="672bd-141">Papildinformāciju skatiet [Krājumu žurnāla apstiprināšanas darbplūsmas](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="672bd-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="672bd-142">Darbplūsma, iespējams, var saskarties ar izņēmumu vai kļūdu.</span><span class="sxs-lookup"><span data-stu-id="672bd-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="672bd-143">Pārskatiet ietekmētās darbplūsmas darba vienuma vēsturi, lai redzētu, vai tā ietver lietojumprogrammas kļūdu, kas pārtrauc darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="672bd-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="672bd-144">Krājumu žurnālu var atjaunināt vai rediģēt tikai tad, ja tas ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="672bd-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="672bd-145">Ja atsaukšana ir aktīva, varat mēģināt atsaukt žurnālu.</span><span class="sxs-lookup"><span data-stu-id="672bd-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="672bd-146">Darbplūsmas pakešuzdevuma izpilde var tikt pārtraukta vairāku iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="672bd-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="672bd-147">Daži no šiem iemesliem, iespējams, ir radušies darbplūsmas struktūras problēma.</span><span class="sxs-lookup"><span data-stu-id="672bd-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="672bd-148">Krājumu žurnāla darbplūsmas nosacījumi attiecas tikai uz žurnāla līmeni, nevis rindu līmeni</span><span class="sxs-lookup"><span data-stu-id="672bd-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="672bd-149">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="672bd-149">Issue description</span></span>

<span data-ttu-id="672bd-150">Jums var rasties šī problēma, ja, piemēram, mēģināt iestatīt krājumu žurnāla darbplūsmas nosacījumu izmaksu summai.</span><span class="sxs-lookup"><span data-stu-id="672bd-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="672bd-151">Iestatiet nosacījumu tā, ka 1. solis tiek palaists tikai tad, ja izmaksu summa ir mazāka par 100.</span><span class="sxs-lookup"><span data-stu-id="672bd-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="672bd-152">Iestatiet nosacījumu tā, ka 2. solis tiek palaists tikai tad, ja izmaksu summa ir lielāka vai vienāda ar 100.</span><span class="sxs-lookup"><span data-stu-id="672bd-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="672bd-153">Pēc tam, kad darbplūsma darbojas, darbplūsmas vēsture rāda tikai vienu rindu, un pirmais nosacījums vienmēr tiek novērtēts kā *patiess* neatkarīgi no iesniegtās vērtības.</span><span class="sxs-lookup"><span data-stu-id="672bd-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="672bd-154">Problēmas aprisinājums</span><span class="sxs-lookup"><span data-stu-id="672bd-154">Issue workaround</span></span>

<span data-ttu-id="672bd-155">Esošajā laidienā krājumu darbplūsmas nosacījumi attiecas tikai uz žurnāla līmeni, nevis rindu līmeni.</span><span class="sxs-lookup"><span data-stu-id="672bd-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="672bd-156">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="672bd-156">This behavior is by design.</span></span> <span data-ttu-id="672bd-157">Nosacījuma kritērijus ieteicams iestatīt tikai žurnāla līmeņa atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="672bd-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="672bd-158">Filtra rūts rīcībā esošo krājumu saraksta lapā nefiltrē rezultātus, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="672bd-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="672bd-159">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="672bd-159">Issue description</span></span>

<span data-ttu-id="672bd-160">Filtra rūts filtri **Rīcībā esošo krājumu saraksta**  lapā nefiltrē rezultātus, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="672bd-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="672bd-161">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="672bd-161">Issue resolution</span></span>

<span data-ttu-id="672bd-162">Tas tiek darīts ar nolūku.</span><span class="sxs-lookup"><span data-stu-id="672bd-162">This behavior is by design.</span></span>

<span data-ttu-id="672bd-163"> *\*Rīcībā esošo krājumu saraksta**  lapa tiek apkopota no detalizētas rīcībā esošo krājumu tabulas, kas ietver visas pieejamās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="672bd-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="672bd-164">Tomēr saraksts šajā lapā ir kopsavilkums.</span><span class="sxs-lookup"><span data-stu-id="672bd-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="672bd-165">Tāpēc tā var apvienot rindas no avota tabulas, apkopojot vērtības atbilstoši parādītajām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="672bd-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="672bd-166">Filtri, ko iestatāt Filtru rūtī, attiecas uz avota tabulu, nevis uz apkopoto sarakstu.</span><span class="sxs-lookup"><span data-stu-id="672bd-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="672bd-167">Dažreiz šī uzvedība var radīt neparedzētus rezultātus, kā parādīts [šajos piemēros](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="672bd-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="672bd-168">Tomēr  [režģī sniegtie filtri](inventory-on-hand-list.md#grid-filters) *attiecas*  uz apkopoto sarakstu.</span><span class="sxs-lookup"><span data-stu-id="672bd-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="672bd-169">Šie filtri ietver gan QuickFilter režģa augšpusē, gan katra kolonnas virsraksta filtru.</span><span class="sxs-lookup"><span data-stu-id="672bd-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="672bd-170">Krājumu žurnālā mērvienības un mērvienību daudzums nedarbojas pareizi.</span><span class="sxs-lookup"><span data-stu-id="672bd-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="672bd-171">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="672bd-171">Issue description</span></span>

<span data-ttu-id="672bd-172">Strādājot ar mērvienībām un daudzumiem krājumu žurnālā, varat saskarties ar vienu vai abiem šiem jautājumiem:</span><span class="sxs-lookup"><span data-stu-id="672bd-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="672bd-173">Jūs krājuma žurnālā neredzat mērvienības vai vienību daudzumus, kamēr izlaistai precei ir iestatīta pārvēršanas mērvienība, un krājumu žurnālā nevarat mainīt šo mērvienību.</span><span class="sxs-lookup"><span data-stu-id="672bd-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="672bd-174">Krājumu žurnālā ir redzami lauki **Daudzums** un **Mērvienība**, taču nav redzams lauks **Mērvienības daudzums**.</span><span class="sxs-lookup"><span data-stu-id="672bd-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="672bd-175">Mainot mērvienību, ievadiet daudzumu un grāmatojiet žurnālu, žurnālā joprojām tiek parādīta sākotnējā mērvienība šim daudzumam.</span><span class="sxs-lookup"><span data-stu-id="672bd-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="672bd-176">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="672bd-176">Issue resolution</span></span>

<span data-ttu-id="672bd-177">Lai novērstu šo problēmu, izpildiet sekojošās darbības.</span><span class="sxs-lookup"><span data-stu-id="672bd-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="672bd-178">**Līdzekļu pārvaldības** darbvietā pārliecinieties, vai krājumu žurnālu līdzekļa funkcija *Izmanto mērvienību un mērvienību daudzumu* ir ieslēgta.</span><span class="sxs-lookup"><span data-stu-id="672bd-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="672bd-179">Ar šo žurnālam tiek pievienots lauks **Mērvienība** un **Mērvienības daudzums**.</span><span class="sxs-lookup"><span data-stu-id="672bd-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="672bd-180">Kad funkcija ir ieslēgta, lietojiet lauku **Daudzums**, **Mērvienības daudzums** un **Mērvienība** šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="672bd-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="672bd-181">**Daudzums** – norādiet daudzumu, izmantojot izpildei nodotai precei noteikto noklusējuma mērvienību.</span><span class="sxs-lookup"><span data-stu-id="672bd-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="672bd-182">Tomēr noklusētā mērvienība šeit netiek rādīta.</span><span class="sxs-lookup"><span data-stu-id="672bd-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="672bd-183">Ja ir iestatīta pārvēršana starp noklusējuma mērvienību un laukā **Mērvienība** atlasīto vienību, lauks **Daudzums** tiek automātiski atjaunināts, pamatojoties uz lauku **Mērvienība** un **Mērvienības daudzums** atlasi.</span><span class="sxs-lookup"><span data-stu-id="672bd-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="672bd-184">**Mērvienības daudzums** - norādiet daudzumu, izmantojot laukā **Mērvienība** atlasīto mērvienību.</span><span class="sxs-lookup"><span data-stu-id="672bd-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="672bd-185">**Mērvienība** – atlasiet mērvienību, ko piemērot vērtībai laukā **Mērvienības daudzums**.</span><span class="sxs-lookup"><span data-stu-id="672bd-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="672bd-186">Saņemu šādu kļūdas ziņojumu: "Maksimālais decimāldaļu skaits noliktavas mērvienībai ir 0."</span><span class="sxs-lookup"><span data-stu-id="672bd-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="672bd-187">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="672bd-187">Issue description</span></span>

<span data-ttu-id="672bd-188">Mēģinot grāmatot krājumu darbību vai krājumu rezervēšanu, tiek saņemts šāds kļūdas ziņojums: "Maksimālais decimāldaļu skaits noliktavas mērvienībai ir 0."</span><span class="sxs-lookup"><span data-stu-id="672bd-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="672bd-189">Šī problēma rodas, ja krājumu darbības daudzums ir norādīts kā decimālskaitļa vērtība, kas ir zem precizitātes līmeņa, ko lauks atbalsta.</span><span class="sxs-lookup"><span data-stu-id="672bd-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="672bd-190">Piemēram, krājuma darbībai norādīts daudzums *0,5*, bet tiek atbalstīti tikai veseli skaitļi.</span><span class="sxs-lookup"><span data-stu-id="672bd-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="672bd-191">Tāpēc vērtībai ir jābūt *1*, nevis *0,5*.</span><span class="sxs-lookup"><span data-stu-id="672bd-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="672bd-192">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="672bd-192">Issue resolution</span></span>

1. <span data-ttu-id="672bd-193">Lai krājumu darbībās noapaļotu daudzumus, palaidiet SQL Server instancē šādu skriptu.</span><span class="sxs-lookup"><span data-stu-id="672bd-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="672bd-194">Šis skripts izlabos vērtības tabulā **inventTrans**.</span><span class="sxs-lookup"><span data-stu-id="672bd-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="672bd-195">Palaidiet rīcībā esošo konsekvences pārbaudi, ja ir ieslēgta opcija **labot kļūdas**.</span><span class="sxs-lookup"><span data-stu-id="672bd-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="672bd-196">Šis skripts izlabos vērtības tabulā **inventSum**.</span><span class="sxs-lookup"><span data-stu-id="672bd-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="672bd-197">Ir stingri ieteicams rūpīgi rediģēt skriptu, kā tas nepieciešams jūsu videi, pārbaudīt to pārbaudes vidē un pēc tam pārbaudīt iegūtos datus pirms skripta palaišanas ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="672bd-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]