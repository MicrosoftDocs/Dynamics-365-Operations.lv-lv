---
title: Sūtījumu krājumu īpašumtiesību maiņa, pamatojoties uz ražošanas pieprasījumu
description: Šajā procedūrā parādīts kā nomainīt sūtījuma krājumu īpašnieku no kreditora uz jūsu juridisko personu, ja ražošanā ir pieprasījums pēc krājuma.
author: perlynne
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6385fba0b6288416a85f1b7de73d3bb4972a852a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834125"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="dc2d1-103">Sūtījumu krājumu īpašumtiesību maiņa, pamatojoties uz ražošanas pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="dc2d1-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc2d1-104">Šajā procedūrā parādīts kā nomainīt sūtījuma krājumu īpašnieku no kreditora uz jūsu juridisko personu, ja ražošanā ir pieprasījums pēc krājuma.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="dc2d1-105">Šī īpašumtiesību maiņa notiek, izveidojot un grāmatojot krājumu īpašumtiesību izmaiņu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="dc2d1-106">Īpašumtiesību izmaiņu žurnāla rindas var izveidot manuāli, vai, kā norādīts šajā ierakstā, pamatojoties uz esošo ražošanas pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="dc2d1-107">Parasti ražotnes vadītājs veic šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="dc2d1-108">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="dc2d1-109">Ja izmantojat savus datus, pārliecinieties, ka ir izpildīti šādi priekšnosacījumi: krājumu žurnāla nosaukums, kas ir iestatīta krājumu īpašumtiesību izmaiņai, fiziski reģistrēti kreditoram piederoši rīcībā esoši krājumi, un viena vai vairākas ražošanas pasūtījuma rindas materiālam.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="dc2d1-110">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="dc2d1-111">Ārējo sūtījumu procesi netiek atbalstīti iebūvētajā versijā, un automātiskā īpašumtiesību žurnāla apstrāde netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="dc2d1-112">Izveidot krājumu īpašumtiesību žurnālu</span><span class="sxs-lookup"><span data-stu-id="dc2d1-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="dc2d1-113">Dodieties uz Krājumu vadība > Žurnāla ieraksti > Krājumi > Krājumu īpašumtiesību izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="dc2d1-114">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-114">Click New.</span></span>
    * <span data-ttu-id="dc2d1-115">Krājumu īpašumtiesību izmaiņu žurnāls tiek izmantots, lai mainītu sūtījuma krājumu īpašnieku no kreditora uz pašreizējo juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="dc2d1-116">Šī īpašnieka maiņa tiek veikta, nododot rīcībā esošos krājumus, kas pieder kreditoram, un pēc tam saņemot šos krājumus pašreizējā juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="dc2d1-117">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="dc2d1-118">Jūs varat atlasīt tikai krājumu žurnālu nosaukumus ar žurnāla tipu Īpašumtiesību izmaiņa.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="dc2d1-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-119">Click OK.</span></span>
5. <span data-ttu-id="dc2d1-120">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-120">Click Functions.</span></span>
6. <span data-ttu-id="dc2d1-121">Noklikšķiniet uz Izveidot žurnāla rindas no ražošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="dc2d1-122">Jūs varat sākt īpašumtiesību izmaiņas procesu, nosūtot vaicājumu visām ražošanas līnijām, kurām ir patēriņa izejvielu pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="dc2d1-123">Laukā Ietveramie krājumu izejas plūsmu statusi atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="dc2d1-124">Šī iespēja ļauj filtrēt pēc krājumu darbību izejas plūsmas statusa.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="dc2d1-125">Piemēram, jūs varat izveidot žurnāla rindas krājumiem ar statusiem Izdots un fiziski rezervēts.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="dc2d1-126">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="dc2d1-127">Šī sadaļa ļauj jums pielietot papildu filtrēšanu.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="dc2d1-128">Piemēram, jūs varat atlasīt noteiktu izejmateriālu reģistrēšanas datumu.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="dc2d1-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="dc2d1-130">Grāmatot krājumu īpašumtiesību izmaiņu žurnālu</span><span class="sxs-lookup"><span data-stu-id="dc2d1-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="dc2d1-131">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-131">Click Post.</span></span>
    * <span data-ttu-id="dc2d1-132">Kad žurnāls ir grāmatots, kreditora krājumi tiek nodoti, izmantojot atsauci "Īpašumtiesību maiņa”.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="dc2d1-133">Krājumi tiek saņemti kā rīcībā esoši, izmantojot krājuma darbību, kas tiek atjaunināta ar pirkšanas pasūtījuma produktu ieejas plūsmu.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="dc2d1-134">Ņemiet vērā, ka tiek izveidotas tikai darbības, kas ir saistītas ar grāmatoto žurnālu.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="dc2d1-135">Netiek izveidotas nekādas paredzētās Krājumu darbības.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="dc2d1-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-136">Click OK.</span></span>
3. <span data-ttu-id="dc2d1-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dc2d1-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]