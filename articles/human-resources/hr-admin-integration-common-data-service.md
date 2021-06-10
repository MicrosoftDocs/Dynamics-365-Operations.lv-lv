---
title: Dataverse integrācijas konfigurēšana
description: Varat ieslēgt vai izslēgt integrāciju starp Microsoft Dataverse un Microsoft Dynamics 365 Human Resources. Varat arī skatīt detalizētu informāciju par sinhronizāciju, dzēst izsekošanas datus un vēlreiz sinhronizēt tabulu, lai palīdzētu novērst ar datiem saistītās problēmas starp abām vidēm.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 721799c9a6fafe0a809f447189ce6814b30ca863
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052461"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="67fcf-104">Dataverse integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="67fcf-104">Configure Dataverse integration</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="67fcf-105">Varat ieslēgt vai izslēgt integrāciju starp Microsoft Dataverse un Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="67fcf-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="67fcf-106">Varat arī skatīt detalizētu informāciju par sinhronizāciju, dzēst izsekošanas datus un vēlreiz sinhronizēt tabulu, lai palīdzētu novērst ar datiem saistītās problēmas starp abām vidēm.</span><span class="sxs-lookup"><span data-stu-id="67fcf-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="67fcf-107">Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="67fcf-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="67fcf-108">Izslēdzot integrāciju, lietotāji var veikt izmaiņas Human Resources vai Dataverse, bet šīs izmaiņas netiek sinhronizētas starp abām vidēm.</span><span class="sxs-lookup"><span data-stu-id="67fcf-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="67fcf-109">Pēc noklusējuma datu integrācijas starp Personāla vadību un Dataverse ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="67fcf-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="67fcf-110">Iespējamas, velēsieties izslēgt integrāciju tālāk minētajās situācijās.</span><span class="sxs-lookup"><span data-stu-id="67fcf-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="67fcf-111">Ja aizpildāt datus, izmantojot datu pārvaldības struktūru, un dati ir jāimportē vairākas reizes, lai tie būtu pareizā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="67fcf-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="67fcf-112">Pastāv problēmas ar datiem vai nu Human Resources, vai Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67fcf-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="67fcf-113">Izslēdzot integrāciju, varat dzēst ierakstu vienā vidē, nedzēšot to otrā.</span><span class="sxs-lookup"><span data-stu-id="67fcf-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="67fcf-114">Atkal ieslēdzot integrāciju, ieraksts vidē, kurā tas netika dzēsts, tiek sinhronizēts ar vidi, kurā tas tika dzēsts.</span><span class="sxs-lookup"><span data-stu-id="67fcf-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="67fcf-115">Sinhronizācija sākas nākamajā reizē, kad tiek izpildīts pakešuzdevums **Dataverse integrācijas neatbildētā pieprasījuma sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="67fcf-116">Izslēdzot datu integrāciju, pārliecinieties, vai nerediģējat vienu un to pašu ierakstu abās vidēs.</span><span class="sxs-lookup"><span data-stu-id="67fcf-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="67fcf-117">Atkal ieslēdzot integrāciju, tiks sinhronizēts pēdējais rediģētais ieraksts.</span><span class="sxs-lookup"><span data-stu-id="67fcf-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="67fcf-118">Tāpēc, ja abās vidēs neveicat vienādas izmaiņas ierakstā, dati var tikt zaudēti.</span><span class="sxs-lookup"><span data-stu-id="67fcf-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="67fcf-119">Piekļūšana Dataverse integrācijas lapai</span><span class="sxs-lookup"><span data-stu-id="67fcf-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="67fcf-120">Human Resources instancē, kur vēlaties skatīt vai konfigurēt iestatījumus integrācijai ar Dataverse, atlasiet elementu **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="67fcf-121">[![Sistēmas administrēšanas elements](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="67fcf-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="67fcf-122">Atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="67fcf-123">[![Saišu cilne](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="67fcf-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="67fcf-124">Sadaļā **Integrācijas** atlasiet **Dataverse konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="67fcf-125">[![Dataverse konfigurācijas saite](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="67fcf-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="67fcf-126">Datu integrācijas starp Human Resources un Dataverse ieslēgšana vai izslēgšana</span><span class="sxs-lookup"><span data-stu-id="67fcf-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="67fcf-127">Lai ieslēgtu integrāciju, iestatiet opciju **Iespējot Dataverse integrāciju** uz **Jā** lapā **Microsoft Dataverse integrācija**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="67fcf-128">Ieslēdzot integrāciju, dati tiks sinhronizēti nākamajā reizē, kad tiek izpildīts sinhronizēšanas pakešuzdevums **Dataverse integrācijas neatbildētā pieprasījuma sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="67fcf-129">Pēc pakešuzdevuma pabeigšanas visiem datiem jābūt pieejamiem.</span><span class="sxs-lookup"><span data-stu-id="67fcf-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="67fcf-130">Lai izslēgtu integrāciju, iestatiet opciju uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="67fcf-131">[![Pakalpojuma Dataverse integrācijas ieslēgšana vai izslēgšana](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="67fcf-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="67fcf-132">Lai veiktu datu migrācijas uzdevumus, ieteicams izslēgt Dataverse integrāciju.</span><span class="sxs-lookup"><span data-stu-id="67fcf-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="67fcf-133">Lielas datu augšupielādes var būtiski ietekmēt veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="67fcf-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="67fcf-134">Piemēram, 2000 darbinieku augšupielādēšana var aizņemt vairākas stundas, ja integrācija ir iespējota, un mazāk par vienu stundu, kad tā ir atspējota.</span><span class="sxs-lookup"><span data-stu-id="67fcf-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="67fcf-135">Šajā piemērā sniegtie numuri ir tikai demonstrācijas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="67fcf-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="67fcf-136">Precīzs laika apjoms, kas nepieciešams, lai importētu ierakstus, var būtiski atšķirties atkarībā no daudziem faktoriem.</span><span class="sxs-lookup"><span data-stu-id="67fcf-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="67fcf-137">Datu integrācijas detalizētas informācijas skatīšana</span><span class="sxs-lookup"><span data-stu-id="67fcf-137">View data integration details</span></span>

<span data-ttu-id="67fcf-138">Kopsavilkuma cilnē **Administrēšana**, kas atrodas lapā **Microsoft Dataverse integrācija**, var redzēt, kā rindas ir saistītas kopā starp Human Resources un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67fcf-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="67fcf-139">Lai skatītu tabulas rindas, atlasiet tabulu laukā **Dataverse tabulas**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="67fcf-140">Režģis parāda visas rindas, kas ir saistītas ar atlasīto tabulu.</span><span class="sxs-lookup"><span data-stu-id="67fcf-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="67fcf-141">Ne visas Dataverse tabulas pašlaik ir uzskaitītas.</span><span class="sxs-lookup"><span data-stu-id="67fcf-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="67fcf-142">Režģī parādās tikai tās tabulas, kas atbalsta pielāgoto lauku izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="67fcf-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="67fcf-143">Jaunas tabulas kļūst pieejamas, izmantojot pastāvīgus Human Resources laidienus.</span><span class="sxs-lookup"><span data-stu-id="67fcf-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="67fcf-144">Režģī ir iekļauti tālāk minētie lauki.</span><span class="sxs-lookup"><span data-stu-id="67fcf-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="67fcf-145">**Dataverse tabula** – tabulas nosaukums Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67fcf-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="67fcf-146">**Dataverse tabulas atsauce** – identifikators, ko Dataverse izmanto ieraksta identificēšanai.</span><span class="sxs-lookup"><span data-stu-id="67fcf-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="67fcf-147">Šī vērtība ir ekvivalenta Human Resources vērtībai **RecId**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="67fcf-148">Identifikatoru varat atrast, atverot Dataverse tabulu Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="67fcf-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="67fcf-149">**Human Resources elementa nosaukums** — Human Resources elements, kas pēdējoreiz sinhronizēja datus uz Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67fcf-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="67fcf-150">Elementam var būt Dataverse prefikss vai cits prefikss.</span><span class="sxs-lookup"><span data-stu-id="67fcf-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="67fcf-151">**Human Resources atsauce** — vērtība **RecId**, kas saistīta ar Human Resources ierakstu.</span><span class="sxs-lookup"><span data-stu-id="67fcf-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="67fcf-152">**Tika dzēsts no Dataverse** – vērtība, kas norāda, vai rinda tika dzēsta no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67fcf-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="67fcf-153">Ieraksti Human Resources atbilst rindām, kas atrodas Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67fcf-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="67fcf-154">Human Resources ieraksta saistības noņemšana no Dataverse rindas</span><span class="sxs-lookup"><span data-stu-id="67fcf-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="67fcf-155">Ja izjūtat problēmas datu sinhronizācijas laikā starp Human Resources un Dataverse, iespējams, varēsiet tās atrisināt, dzēšot izsekošanu un ļaujot vēlreiz sinhronizēt izsekošanas tabulu.</span><span class="sxs-lookup"><span data-stu-id="67fcf-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="67fcf-156">Noņemot saistību, un pēc tam mainot vai dzēšot rindu Dataverse, izmaiņas netiks sinhronizētas ar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="67fcf-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="67fcf-157">Veicot izmaiņas Human Resources, tiek izveidots jauns izsekošanas ieraksts, un rinda tiek atjaunināta Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67fcf-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="67fcf-158">Lai noņemtu ieraksta saistību starp Resources ierakstu un Dataverse rindu, atlasiet tabulu laukā **Dataverse tabula** un pēc tam atlasiet **Dzēst izsekošanas informāciju**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="67fcf-159">[![Izsekošanas informācija dzēšana](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="67fcf-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="67fcf-160">Lai tabulā izpildītu pilnu sinhronizāciju pēc izsekošanas dzēšanas, skatiet nākamo procedūru.</span><span class="sxs-lookup"><span data-stu-id="67fcf-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="67fcf-161">Tabulas sinhronizācija starp Human Resources un Dataverse</span><span class="sxs-lookup"><span data-stu-id="67fcf-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="67fcf-162">Izmantojiet šo procedūru, ja:</span><span class="sxs-lookup"><span data-stu-id="67fcf-162">Use this procedure when:</span></span>

- <span data-ttu-id="67fcf-163">Izmaiņas no Dataverse aizņem pārāk daudz laika, lai parādītos Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="67fcf-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="67fcf-164">Pēc izsekošanas notīrīšanas ir jāatsvaidzina izsekošanas tabula.</span><span class="sxs-lookup"><span data-stu-id="67fcf-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="67fcf-165">Lai veiktu pilnu sinhronizāciju tabulā starp Human Resources un Dataverse:</span><span class="sxs-lookup"><span data-stu-id="67fcf-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="67fcf-166">Atlasiet tavulu laukā **Dataverse tabula**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="67fcf-167">Atlasiet **Sinhronizēt tagad**.</span><span class="sxs-lookup"><span data-stu-id="67fcf-167">Select **Sync now**.</span></span>

<span data-ttu-id="67fcf-168">[![Pilnīgas sinhronizācijas izpilde](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="67fcf-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="67fcf-169">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="67fcf-169">See also</span></span>

[<span data-ttu-id="67fcf-170">Dataverse tabulas</span><span class="sxs-lookup"><span data-stu-id="67fcf-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="67fcf-171">Pakalpojuma Dataverse virtuālo tabulu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="67fcf-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="67fcf-172">Human Resources virtuālās tabulas: Bieži uzdotie jautājumi</span><span class="sxs-lookup"><span data-stu-id="67fcf-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="67fcf-173">Kas ir Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="67fcf-173">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="67fcf-174">Terminoloģijas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="67fcf-174">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]