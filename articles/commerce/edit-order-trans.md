---
title: Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana
description: Šajā tēmā aprakstīts, kā rediģēt un auditēt tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumus programmā Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8fa6f7a71bae759e2b8feb3c5778200bb7bdbfe9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010155"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="9b73f-103">Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="9b73f-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b73f-104">Šajā tēmā aprakstīts, kā rediģēt un auditēt tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumus programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9b73f-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9b73f-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="9b73f-105">Overview</span></span>

<span data-ttu-id="9b73f-106">Starp programmas Commerce versijām 10.0.5 un 10.0.6 tika pievienots atbalsts darījumu, kas ir saistīti ar pārdošanu skaidrā naudā bez piegādes (piemēram, pārdošana un atgriešana), un skaidras naudas pārvaldības darījumu (piemēram, mainīgā ievade un norēķinu noņemšana) rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="9b73f-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="9b73f-107">Programmas Commerce versijā 10.0.7 tika pievienots atbalsts tiešsaistes pasūtījumu darījumu un asinhrono debitoru pasūtījumu darījumu rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="9b73f-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="9b73f-108">Pasūtījumu darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="9b73f-108">Edit and audit order transactions</span></span>

<span data-ttu-id="9b73f-109">Lai rediģētu un auditētu pasūtījumu darījumus komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9b73f-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9b73f-110">Instalējiet [Microsoft Dynamics Office pievienojumprogrammu](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="9b73f-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="9b73f-111">Lapas **Mazumtirdzniecības parametri** cilnes **Debitoru pasūtījumi** kopsavilkuma cilnē **Pasūtījums** norādiet aizturēšanas kodu elementam **Aizturēšanas kods pasūtījumu sinhronizācijas kļūdām**.</span><span class="sxs-lookup"><span data-stu-id="9b73f-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="9b73f-112">Atveriet darbvietu **Veikala finanses**.</span><span class="sxs-lookup"><span data-stu-id="9b73f-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="9b73f-113">Elementi **Tiešsaistes pasūtījumu sinhronizācijas kļūdas** un **Debitoru pasūtījumu sinhronizācijas kļūdas** nodrošina iepriekš filtrētu mazumtirdzniecības darījumu lapas skatu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="9b73f-114">Katrā no tiem ir parādīti darījumu ieraksti, kuru sinhronizācija neizdevās atbilstoši pasūtījuma veidam.</span><span class="sxs-lookup"><span data-stu-id="9b73f-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="9b73f-115">Atveriet lapu **Tiešsaistes pasūtījumu sinhronizācijas kļūdas** vai lapu **Debitoru pasūtījumu sinhronizācijas kļūdas**.</span><span class="sxs-lookup"><span data-stu-id="9b73f-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="9b73f-116">Atlasiet ierakstu, lai skatītu detalizētu informāciju par sinhronizācijas kļūdu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="9b73f-117">Kopsavilkuma cilnē **Sinhronizācijas statuss** ir sniegta tālāk norādītā detalizētā informācija par kļūdu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="9b73f-118">Gaidošā pasūtījuma statuss</span><span class="sxs-lookup"><span data-stu-id="9b73f-118">Pending order status</span></span>
    - <span data-ttu-id="9b73f-119">Detalizēta informācija par pasūtījuma kļūdām</span><span class="sxs-lookup"><span data-stu-id="9b73f-119">Order error details</span></span>
    - <span data-ttu-id="9b73f-120">Modificēšanas datums un laiks</span><span class="sxs-lookup"><span data-stu-id="9b73f-120">Modified date and time</span></span>
    - <span data-ttu-id="9b73f-121">Atkārtoto mēģinājumu skaits</span><span class="sxs-lookup"><span data-stu-id="9b73f-121">Retry count</span></span>

1. <span data-ttu-id="9b73f-122">Ja detalizētajā informācijā par kļūdu ir norādīts, ka ierakstu nepieciešams labot, atlasiet **Office pievienojumprogramma** un pēc tam atlasiet **Rediģēt atlasīto darījumu**.</span><span class="sxs-lookup"><span data-stu-id="9b73f-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="9b73f-123">Tiks atvērts Excel fails, kurā parādīta detalizēta informācija par atlasīto darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="9b73f-124">Ja darījums, kas tiek rediģēts, ir tiešsaistes pasūtījuma darījums, Excel failā ir tālāk norādītās darblapas.</span><span class="sxs-lookup"><span data-stu-id="9b73f-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="9b73f-125">**Darījums** — šī darblapa satur detalizētu informāciju par darījuma galveni.</span><span class="sxs-lookup"><span data-stu-id="9b73f-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="9b73f-126">**Pārdošanas darījums** — šī darblapa satur detalizētu rindas informāciju par darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="9b73f-127">**Maksājumu darījumi** — šī darblapa satur detalizētu informāciju par maksājumu rindām attiecībā uz darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="9b73f-128">**Atlaižu darījumi** — šī darblapa satur detalizētu informāciju par atlaidēm attiecībā uz darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="9b73f-129">**Nodokļu darījumi** — šī darblapa satur detalizētu ar nodokļiem saistītu informāciju par atlaidēm attiecībā uz darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="9b73f-130">**Izmaksu darījumi** — šī darblapa satur ar izmaksām saistītus datus attiecībā uz darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="9b73f-131">Ja darījums, kas tiek rediģēts, ir asinhrons debitora pasūtījuma darījums, Excel failā ir tālāk norādītās darblapas.</span><span class="sxs-lookup"><span data-stu-id="9b73f-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="9b73f-132">**Rindas** — šī darblapa satur detalizētu galvenes un rindas informāciju par darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="9b73f-133">**Maksājumi** — šī darblapa satur detalizētu informāciju par maksājumu rindām attiecībā uz darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="9b73f-134">**Atlaides** — šī darblapa satur detalizētu informāciju par atlaidēm attiecībā uz darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="9b73f-135">**Nodokļi** — šī darblapa satur detalizētu informāciju par nodokļiem attiecībā uz darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="9b73f-136">**Izmaksas** — šī darblapa satur ar izmaksām saistītus datus attiecībā uz darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="9b73f-137">Programmas Excel faila laukā **Gaidošā pasūtījuma statuss** ievadiet **Rediģēšana** un pēc tam publicējiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="9b73f-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="9b73f-138">Tādējādi jūs neļausit veikt darbu **Sinhronizēt pasūtījumu**, kas darbojas pakešveida režīmā, izlaižot šo ierakstu apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="9b73f-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="9b73f-139">Excel failā varat modificēt attiecīgos laukus un pēc tam augšupielādēt datus atpakaļ komponentā Commerce Headquarters, izmantojot Dynamics Excel pievienojumprogrammas publicēšanas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="9b73f-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="9b73f-140">Pēc datu publicēšanas izmaiņas tiks atspoguļotas sistēmā.</span><span class="sxs-lookup"><span data-stu-id="9b73f-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="9b73f-141">Publicēšanas laikā lietotāju veiktajām izmaiņām validācija netiek veikta.</span><span class="sxs-lookup"><span data-stu-id="9b73f-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="9b73f-142">Pilnīgus auditācijas pierakstus varat skatīt, galvenē **Mazumtirdzniecības darījums** (galvenes līmeņa izmaiņu gadījumā) un attiecīgajā sadaļā un ierakstā atbilstošajā darījumu lapā noklikšķinot uz **Skatīt auditācijas pierakstus**.</span><span class="sxs-lookup"><span data-stu-id="9b73f-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="9b73f-143">Piemēram, visas ar pārdošanas rindām saistītās izmaiņas tiks rādītas lapā **Pārdošanas darījumi** un visas ar maksājumiem saistītās izmaiņas tiks rādītas lapā **Maksājumu darījumi**.</span><span class="sxs-lookup"><span data-stu-id="9b73f-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="9b73f-144">Saistībā ar izmaiņām tiek uzturēta tālāk norādītā detalizētā informācija par auditu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="9b73f-145">Modificēšanas datums un laiks</span><span class="sxs-lookup"><span data-stu-id="9b73f-145">Modified date and time</span></span>
    - <span data-ttu-id="9b73f-146">Lauks</span><span class="sxs-lookup"><span data-stu-id="9b73f-146">Field</span></span>
    - <span data-ttu-id="9b73f-147">Vecā vērtība</span><span class="sxs-lookup"><span data-stu-id="9b73f-147">Old value</span></span>
    - <span data-ttu-id="9b73f-148">Jaunā vērtība</span><span class="sxs-lookup"><span data-stu-id="9b73f-148">New value</span></span>
    - <span data-ttu-id="9b73f-149">Modificēja</span><span class="sxs-lookup"><span data-stu-id="9b73f-149">Modified by</span></span>

1. <span data-ttu-id="9b73f-150">Pēc izmaiņu veikšanas un publicēšanas atlasiet **Sinhronizēt pasūtījumu**, lai nekavējoties sāktu sinhronizācijas procesu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="9b73f-151">Varat arī gaidīt sinhronizācijas procesu, kas darbojas pakešveida režīmā, lai apstrādātu darījumu.</span><span class="sxs-lookup"><span data-stu-id="9b73f-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="9b73f-152">Pēc noklusējuma pēc pasūtījumu veiksmīgas sinhronizēšanas tiem tiek piešķirts aizturēšanas statuss, pamatojoties uz aizturēšanas kodu, kas definēts Commerce parametros.</span><span class="sxs-lookup"><span data-stu-id="9b73f-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="9b73f-153">Pasūtījumu aizturēšana ir jānoņem, pirms pasūtījumus var apstrādāt tālākai izpildei vai citām operācijām.</span><span class="sxs-lookup"><span data-stu-id="9b73f-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b73f-154">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9b73f-154">Additional resources</span></span>

[<span data-ttu-id="9b73f-155">Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="9b73f-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="9b73f-156">Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana</span><span class="sxs-lookup"><span data-stu-id="9b73f-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="9b73f-157">Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="9b73f-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="9b73f-158">Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="9b73f-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
