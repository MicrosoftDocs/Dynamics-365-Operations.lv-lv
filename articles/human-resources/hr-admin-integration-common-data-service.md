---
title: Common Data Service integrācijas konfigurēšana
description: Varat ieslēgt vai izslēgt integrāciju starp Common Data Service un Microsoft Dynamics 365 Human Resources. Varat arī skatīt detalizētu informāciju par sinhronizāciju, dzēst izsekošanas datus un vēlreiz sinhronizēt elementu, lai palīdzētu novērst ar datiem saistītās problēmas starp abām vidēm.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8cbead2961c4576a5394080aae2fec109bce3f10
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621308"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="b2af5-104">Common Data Service integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b2af5-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="b2af5-105">Varat ieslēgt vai izslēgt integrāciju starp Common Data Service un Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b2af5-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="b2af5-106">Varat arī skatīt detalizētu informāciju par sinhronizāciju, dzēst izsekošanas datus un vēlreiz sinhronizēt elementu, lai palīdzētu novērst ar datiem saistītās problēmas starp abām vidēm.</span><span class="sxs-lookup"><span data-stu-id="b2af5-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="b2af5-107">Izslēdzot integrāciju, lietotāji var veikt izmaiņas Human Resources vai Common Data Service, bet šīs izmaiņas netiek sinhronizētas starp abām vidēm.</span><span class="sxs-lookup"><span data-stu-id="b2af5-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="b2af5-108">Pēc noklusējuma datu integrācijas starp Personāla vadību un Common Data Service ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="b2af5-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="b2af5-109">Iespējamas, velēsieties izslēgt integrāciju tālāk minētajās situācijās.</span><span class="sxs-lookup"><span data-stu-id="b2af5-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="b2af5-110">Ja aizpildāt datus, izmantojot datu pārvaldības struktūru, un dati ir jāimportē vairākas reizes, lai tie būtu pareizā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="b2af5-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="b2af5-111">Pastāv problēmas ar datiem vai nu Human Resources, vai Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b2af5-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="b2af5-112">Izslēdzot integrāciju, varat dzēst ierakstu vienā vidē, nedzēšot to otrā.</span><span class="sxs-lookup"><span data-stu-id="b2af5-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="b2af5-113">Atkal ieslēdzot integrāciju, ieraksts vidē, kurā tas netika dzēsts, tiek sinhronizēts ar vidi, kurā tas tika dzēsts.</span><span class="sxs-lookup"><span data-stu-id="b2af5-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="b2af5-114">Sinhronizācija sākas nākamajā reizē, kad tiek izpildīts pakešuzdevums **Common Data Service integrācijas neatbildētā pieprasījuma sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="b2af5-115">Izslēdzot datu integrāciju, pārliecinieties, vai nerediģējat vienu un to pašu ierakstu abās vidēs.</span><span class="sxs-lookup"><span data-stu-id="b2af5-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="b2af5-116">Atkal ieslēdzot integrāciju, tiks sinhronizēts pēdējais rediģētais ieraksts.</span><span class="sxs-lookup"><span data-stu-id="b2af5-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="b2af5-117">Tāpēc, ja abās vidēs neveicat vienādas izmaiņas ierakstā, dati var tikt zaudēti.</span><span class="sxs-lookup"><span data-stu-id="b2af5-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="b2af5-118">Piekļūšana Common Data Service integrācijas lapai</span><span class="sxs-lookup"><span data-stu-id="b2af5-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="b2af5-119">Human Resources instancē, kur vēlaties skatīt vai konfigurēt iestatījumus integrācijai ar Common Data Service, atlasiet elementu **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="b2af5-120">[![Sistēmas administrēšanas elements](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="b2af5-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="b2af5-121">Atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="b2af5-122">[![Saišu cilne](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="b2af5-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="b2af5-123">Sadaļā **Integrācijas** atlasiet **Common Data Service konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="b2af5-124">[![Common Data Service konfigurācijas saite](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="b2af5-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="b2af5-125">Datu integrācijas starp Human Resources un Common Data Service ieslēgšana vai izslēgšana</span><span class="sxs-lookup"><span data-stu-id="b2af5-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="b2af5-126">Lai ieslēgtu integrāciju, iestatiet opciju **Iespējot integrāciju uz Common Data Service** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2af5-127">Ieslēdzot integrāciju, dati tiks sinhronizēti nākamajā reizē, kad tiek izpildīts sinhronizēšanas pakešuzdevums **Common Data Service integrācijas neatbildētā pieprasījuma sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="b2af5-128">Pēc pakešuzdevuma pabeigšanas visiem datiem jābūt pieejamiem.</span><span class="sxs-lookup"><span data-stu-id="b2af5-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="b2af5-129">Lai izslēgtu integrāciju, iestatiet opciju uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="b2af5-130">[![Common Data Service integrācijas ieslēgšana vai izslēgšana](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="b2af5-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

> [!WARNING]
> <span data-ttu-id="b2af5-131">Lai veiktu datu migrācijas uzdevumus, ieteicams izslēgt Common Data Service integrāciju.</span><span class="sxs-lookup"><span data-stu-id="b2af5-131">We strongly recommend turning off Common Data Service integration while performing data migration tasks.</span></span> <span data-ttu-id="b2af5-132">Lielas datu augšupielādes var būtiski ietekmēt veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="b2af5-132">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="b2af5-133">Piemēram, 2000 darbinieku augšupielādēšana var aizņemt vairākas stundas, ja integrācija ir iespējota, un mazāk par vienu stundu, kad tā ir atspējota.</span><span class="sxs-lookup"><span data-stu-id="b2af5-133">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="b2af5-134">Šajā piemērā sniegtie numuri ir tikai demonstrācijas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="b2af5-134">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="b2af5-135">Precīzs laika apjoms, kas nepieciešams, lai importētu ierakstus, var būtiski atšķirties atkarībā no daudziem faktoriem.</span><span class="sxs-lookup"><span data-stu-id="b2af5-135">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="b2af5-136">Datu integrācijas detalizētas informācijas skatīšana</span><span class="sxs-lookup"><span data-stu-id="b2af5-136">View data integration details</span></span>

<span data-ttu-id="b2af5-137">Kopsavilkuma cilnē **Administrēšana**, kas atrodas lapā **Common Data Service integrācija**, var redzēt, kā ieraksti ir saistīti kopā starp Human Resources un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b2af5-137">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="b2af5-138">Lai skatītu elementa ierakstus, atlasiet elementu laukā **CDS elementa nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-138">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="b2af5-139">Režģis parāda visus ierakstus, kas ir saistīti ar atlasīto elementu.</span><span class="sxs-lookup"><span data-stu-id="b2af5-139">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="b2af5-140">[![Elementa ierakstu skatīšana](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="b2af5-140">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b2af5-141">Ne visi Common Data Service elementi pašlaik ir uzskaitīti.</span><span class="sxs-lookup"><span data-stu-id="b2af5-141">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="b2af5-142">Režģī parādās tikai tie elementi, kas atbalsta pielāgoto lauku izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="b2af5-142">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="b2af5-143">Jauni elementi kļūst pieejami, izmantojot pastāvīgus Human Resources laidienus.</span><span class="sxs-lookup"><span data-stu-id="b2af5-143">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="b2af5-144">Režģī ir iekļauti tālāk minētie lauki.</span><span class="sxs-lookup"><span data-stu-id="b2af5-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="b2af5-145">**CDS elementa nosaukums** — elementa nosaukums Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b2af5-145">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="b2af5-146">**CDS elementa atsauce** — identifikators, ko Common Data Service izmanto ieraksta identificēšanai.</span><span class="sxs-lookup"><span data-stu-id="b2af5-146">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="b2af5-147">Šī vērtība ir ekvivalenta Human Resources vērtībai **RecId**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="b2af5-148">Identifikatoru varat atrast, atverot Common Data Service elementu Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b2af5-148">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="b2af5-149">**Human Resources elementa nosaukums** — elements, kas pēdējoreiz sinhronizēja datus uz Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b2af5-149">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="b2af5-150">Elementam var būt Common Data Service prefikss vai cits prefikss.</span><span class="sxs-lookup"><span data-stu-id="b2af5-150">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="b2af5-151">**Human Resources atsauce** — vērtība **RecId**, kas saistīta ar Human Resources ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b2af5-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="b2af5-152">**Tika dzēsts no CDS** — vērtība, kas norāda, vai ieraksts tika dzēsts no Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b2af5-152">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="b2af5-153">Human Resources ieraksta saistības noņemšana no Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b2af5-153">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="b2af5-154">Ja izjūtat problēmas datu sinhronizācijas laikā starp Human Resources un Common Data Service, iespējams, varēsiet tās atrisināt, dzēšot izsekošanu un ļaujot vēlreiz sinhronizēt izsekošanas tabulu.</span><span class="sxs-lookup"><span data-stu-id="b2af5-154">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="b2af5-155">Noņemot saistību, un pēc tam mainot vai dzēšot ierakstu Common Data Service, izmaiņas netiks sinhronizētas ar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b2af5-155">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="b2af5-156">Veicot izmaiņas Human Resources, tiek izveidots jauns izsekošanas ieraksts, un ieraksts tiek atjaunināts Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b2af5-156">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="b2af5-157">Lai noņemtu ieraksta saistību starp Human Resources un Common Data Service, atlasiet elementu laukā **CDS elementa nosaukums** un tad atlasiet **Dzēst izsekošanas informāciju**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-157">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="b2af5-158">[![Izsekošanas informācija dzēšana](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="b2af5-158">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="b2af5-159">Lai elementā izpildītu pilnu sinhronizāciju pēc izsekošanas dzēšanas, skatiet nākamo procedūru.</span><span class="sxs-lookup"><span data-stu-id="b2af5-159">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="b2af5-160">Elementa sinhronizācija starp Human Resources un Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b2af5-160">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="b2af5-161">Izmantojiet šo procedūru, ja:</span><span class="sxs-lookup"><span data-stu-id="b2af5-161">Use this procedure when:</span></span>

- <span data-ttu-id="b2af5-162">Izmaiņas no Common Data Service aizņem pārāk daudz laika, lai parādītos Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="b2af5-162">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="b2af5-163">Pēc izsekošanas notīrīšanas ir jāatsvaidzina izsekošanas tabula.</span><span class="sxs-lookup"><span data-stu-id="b2af5-163">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="b2af5-164">Lai veiktu pilnu sinhronizāciju elementā starp Personāla vadību un Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="b2af5-164">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="b2af5-165">Laukā **CDS entītijas nosaukums** atlasiet entītiju.</span><span class="sxs-lookup"><span data-stu-id="b2af5-165">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="b2af5-166">Atlasiet **Sinhronizēt tagad**.</span><span class="sxs-lookup"><span data-stu-id="b2af5-166">Select **Sync now**.</span></span>

<span data-ttu-id="b2af5-167">[![Pilnīgas sinhronizācijas izpilde](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="b2af5-167">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


