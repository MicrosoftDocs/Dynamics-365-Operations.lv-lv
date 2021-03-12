---
title: Nomu pārvaldība, izmantojot nomas importēšanas struktūru
description: Šajā tēmā skaidrots, kā izmantot nomas importēšanas struktūru, lai vienlaicīgi koriģētu vairākas nomas.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d7a7d2afd8f352bc167ec8c0a354ee4ac0a9e77b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445794"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="9998f-103">Nomu pārvaldība, izmantojot nomas importēšanas struktūru</span><span class="sxs-lookup"><span data-stu-id="9998f-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9998f-104">Šajā tēmā skaidrots, kā izmantot nomas importēšanas struktūru, lai ar vienu darbību koriģētu vairākas nomas.</span><span class="sxs-lookup"><span data-stu-id="9998f-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="9998f-105">Izmantojot šo iespēju, varat ietaupīt laiku un varat arī nodrošināt precīzākas korekcijas, samazinot cilvēka kļūdas iespējamību.</span><span class="sxs-lookup"><span data-stu-id="9998f-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="9998f-106">Turklāt šī iespēja var savienot Microsoft Dynamics 365 Finance ar ārējo datu vienībām, lai efektīvi augšupielādētu datus.</span><span class="sxs-lookup"><span data-stu-id="9998f-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="9998f-107">Tālāk norādītos datu elementus var izmantot, lai integrētu līdzekļu nomu ar ārējām sistēmām:</span><span class="sxs-lookup"><span data-stu-id="9998f-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="9998f-108">Nomas sagatavošana</span><span class="sxs-lookup"><span data-stu-id="9998f-108">Lease staging</span></span>
- <span data-ttu-id="9998f-109">Maksājumu līguma sagatavošana</span><span class="sxs-lookup"><span data-stu-id="9998f-109">Payment contract staging</span></span>
- <span data-ttu-id="9998f-110">Izpildes līguma sagatavošana</span><span class="sxs-lookup"><span data-stu-id="9998f-110">Executory contract staging</span></span>

<span data-ttu-id="9998f-111">Varat izmantot importēšanas procesu, lai koriģētu nomu, atjauninātu nefinanšu informāciju vai pievienotu jaunas nomas.</span><span class="sxs-lookup"><span data-stu-id="9998f-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="9998f-112">Pirms importēšanas varat apskatīt un rediģēt nomas datus.</span><span class="sxs-lookup"><span data-stu-id="9998f-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="9998f-113">Sistēma var izpildīt trīs tālāk minētos procesus, izmantojot nomas importēšanas komplektu.</span><span class="sxs-lookup"><span data-stu-id="9998f-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="9998f-114">Procesa tips</span><span class="sxs-lookup"><span data-stu-id="9998f-114">Process type</span></span>  | <span data-ttu-id="9998f-115">Apraksts</span><span class="sxs-lookup"><span data-stu-id="9998f-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="9998f-116">Pievienot ierakstu</span><span class="sxs-lookup"><span data-stu-id="9998f-116">Add record</span></span>    | <span data-ttu-id="9998f-117">Migrētās nomas, kurām ir šis procesa tips, veido nomu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="9998f-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="9998f-118">Maksājumu grafiks ir manuāli jāapstiprina, un sākotnējās atpazīšanas žurnāla ieraksts pēc migrācijas ir manuāli jāiegrāmato.</span><span class="sxs-lookup"><span data-stu-id="9998f-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="9998f-119">Labot ierakstu</span><span class="sxs-lookup"><span data-stu-id="9998f-119">Update record</span></span> | <span data-ttu-id="9998f-120">Migrētās nomas, kurām ir šī procesa tipa atjaunināšanas lauka vērtības nomai, kas jau ir sistēmā.</span><span class="sxs-lookup"><span data-stu-id="9998f-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="9998f-121">Tiek atjaunināti tikai tie lauki, kas ir atlasīti lapā **Atjaunināt lauku atlasi**.</span><span class="sxs-lookup"><span data-stu-id="9998f-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="9998f-122">Mēs iesakām atlasīt nefinanšu laukus lapā **Atjaunināt lauku atlasi**, jo šis procesa tips nepielāgo nomu.</span><span class="sxs-lookup"><span data-stu-id="9998f-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="9998f-123">Koriģēt ierakstu</span><span class="sxs-lookup"><span data-stu-id="9998f-123">Adjust record</span></span> | <span data-ttu-id="9998f-124">Migrētās nomas, kurām ir šis procesa tips, pielāgo nomu.</span><span class="sxs-lookup"><span data-stu-id="9998f-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="9998f-125">Šī korekcija izraisa finanšu nomas modifikāciju.</span><span class="sxs-lookup"><span data-stu-id="9998f-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="9998f-126">Pēc nomas apstrādāšanas sistēma izveido jaunu maksājumu grafiku, izmantojot jaunos datus no nomas importēšanas komplekta.</span><span class="sxs-lookup"><span data-stu-id="9998f-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="9998f-127">Sistēma neapstiprina maksājuma grafiku u negrāmato korekcijas žurnāla ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9998f-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="9998f-128">Pēc informācijas augšupielādes, izmantojot **Datu pārvaldības** darbvietu, atveriet **Virsraksta importēšanas** lapu ( **Līdzekļa noma \>Nomas importēšanas struktūra \> Virsraksta importēšana**).</span><span class="sxs-lookup"><span data-stu-id="9998f-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="9998f-129">Šajā lapā uzskaitītas visas trīs datu entītijas, kas tika uzskaitītas iepriekš.</span><span class="sxs-lookup"><span data-stu-id="9998f-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="9998f-130">Lai skatītu nomas sagatavošanas posmu datus pirms apstrādes palaišanas, atlasiet **Sagatavošanas posmu dati**.</span><span class="sxs-lookup"><span data-stu-id="9998f-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="9998f-131">Salīdzināšanas funkcija ļauj salīdzināt ierakstu, ko importējat, ar atbilstošo ierakstu, kas jau ir jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="9998f-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="9998f-132">Lai salīdzinātu atsevišķu nomas ierakstu, atlasiet nomu un pēc tam atlasiet **Salīdzināt**.</span><span class="sxs-lookup"><span data-stu-id="9998f-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="9998f-133">Šī darbība jāveic, lai ģenerētu pārskatu **Atšķirības**, pirms migrējat nomas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="9998f-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="9998f-134">Salīdzināšanas funkcija salīdzina sagatavošanas posmu datos norādītās vērtības ar to nomu vērtībām, kas pašlaik ir sistēmā.</span><span class="sxs-lookup"><span data-stu-id="9998f-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="9998f-135">Salīdzināšanas funkcionalitāte nedarbojas nomām, kurām ir **pievienošanas ieraksta** procesa tips, jo nav nekā, ko salīdzināt ar šo nomu.</span><span class="sxs-lookup"><span data-stu-id="9998f-135">The Compare functionality doesn't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="9998f-136">Lai vienlaicīgi salīdzinātu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks \> Salīdzināt** un atlasiet **Salīdzināt**.</span><span class="sxs-lookup"><span data-stu-id="9998f-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Compare**, and select **Compare**.</span></span>

<span data-ttu-id="9998f-137">Katram elementam varat apskatīt atšķirības starp to, kas pašlaik ir sistēmā, un to, kas atrodas sagatavošanas posmos.</span><span class="sxs-lookup"><span data-stu-id="9998f-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="9998f-138">Katram elementam sagatavošanas tabulās atlasiet opciju **Skatīt atšķirības**.</span><span class="sxs-lookup"><span data-stu-id="9998f-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="9998f-139">Redzamais dialoglodziņš rāda pašreizējo vērtību un piedāvāto sagatavošanas vērtību.</span><span class="sxs-lookup"><span data-stu-id="9998f-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="9998f-140">Varat arī atjaunināt sagatavošanas posma vērtību, mainot to kolonnā **Jauna vērtība** un pēc tam atlasot **Atjaunināt sagatavošanas posmu**.</span><span class="sxs-lookup"><span data-stu-id="9998f-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="9998f-141">Jūs varat pārbaudīt nomas, lai nodrošinātu, ka ieraksti var tikt ienesti sistēmā, neieviešot kļūdas.</span><span class="sxs-lookup"><span data-stu-id="9998f-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="9998f-142">Pirms nomas ieraksts tiek migrēts, sistēma izpilda vairākas pārbaudes, lai nodrošinātu, ka ieraksts tiks sekmīgi importēts.</span><span class="sxs-lookup"><span data-stu-id="9998f-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="9998f-143">Lai apstiprinātu atsevišķu nomu, atlasiet **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="9998f-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="9998f-144">Lai vienlaicīgi pārbaudītu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks \> Pārbaudīt** un atlasiet **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="9998f-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="9998f-145">Lai apstrādātu atsevišķu nomu, atlasiet **Migrēt nomas ierakstus** lapā **Virsraksta importēšana**.</span><span class="sxs-lookup"><span data-stu-id="9998f-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="9998f-146">Kad noma tiek migrēta, sistēma veic darbību, kas norādīta laukā **Procesa tips**.</span><span class="sxs-lookup"><span data-stu-id="9998f-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="9998f-147">Lai vienlaicīgi pārbaudītu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks \> Pārbaudīt** un atlasiet **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="9998f-147">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="9998f-148">Pēc tam, kad noma ir salīdzināta, varat palaist pārskatu, lai skatītu atšķirības katrai nomai, kas iekļauta importēšanas ID.</span><span class="sxs-lookup"><span data-stu-id="9998f-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="9998f-149">Lai palaistu pārskatu vienam nomas līgumam, atlasiet šo nomu sagatavošanas posma datos un pēc tam atlasiet **Salīdzināt un skatīt pārskatu \> Atšķirību pārskats**.</span><span class="sxs-lookup"><span data-stu-id="9998f-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="9998f-150">Lai vienlaicīgi pārbaudītu vairākas nomas, dodieties uz **Līdzekļu noma \> Pieprasījumi un pārskati \> Atšķirību pārskats** un atlasiet **Salīdzināt**.</span><span class="sxs-lookup"><span data-stu-id="9998f-150">To validate multiple leases at the same time, go to **Asset leasing \> Inquiries and reports \> Differences report**, and select **Compare**.</span></span>

## <a name="set-up-update-fields"></a><span data-ttu-id="9998f-151">Iestatīt atjaunināšanas laukus</span><span class="sxs-lookup"><span data-stu-id="9998f-151">Set up update fields</span></span>

<span data-ttu-id="9998f-152">Ja izmantojat nomas importēšanas struktūru, lai atjauninātu nomas, un procesa tips ir **Atjaunināšanas ieraksts**, varat atlasīt konkrētus laukus, kas jāatjaunina.</span><span class="sxs-lookup"><span data-stu-id="9998f-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="9998f-153">Doties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Iestatīšana \> Atjaunināt lauku atlasi**.</span><span class="sxs-lookup"><span data-stu-id="9998f-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="9998f-154">Parādītajā lapā atlasiet atjaunināmos laukus un pēc tam atlasiet zaļo bultiņu, lai pārvietotu tos uz sarakstu **Atlasītie lauki**.</span><span class="sxs-lookup"><span data-stu-id="9998f-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="9998f-155">Tikai lauki sarakstā **Atlasītie lauki** var tikt atjaunināti, izmantojot nomas importēšanas komplektu.</span><span class="sxs-lookup"><span data-stu-id="9998f-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>