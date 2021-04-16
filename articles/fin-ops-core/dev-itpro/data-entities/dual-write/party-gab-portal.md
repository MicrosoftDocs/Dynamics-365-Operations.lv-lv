---
title: Power Portal izmantošana kopā ar pušu datu modeli
description: Šajā tēmā aprakstītas izmaiņas Power Portal tīmekļa lomās, kas ir veiktas, jo puses datu modelis ir dubultrakstīšanā.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833094"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="0f396-103">Power Portal izmantošana kopā ar pušu datu modeli</span><span class="sxs-lookup"><span data-stu-id="0f396-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0f396-104">Dubultās rakstīšanas lietojumprogrammas orhestrācijas risinājuma versijā 2.0.999.0 un jaunākās ir iekļautas datu modeļa izmaiņas pušu un globālajā adrešu grāmatā tabulām Konts un Kontaktpersona.</span><span class="sxs-lookup"><span data-stu-id="0f396-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="0f396-105">Izmaiņas ļauj attiecības daudzi pret daudziem, kas atbalsta detalizētus biznesa scenārijus.</span><span class="sxs-lookup"><span data-stu-id="0f396-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="0f396-106">Šīs izmaiņas neatbalsta portāla tīmekļa lomas, tostarp klientu portāls, kas tiek piegādāts ārpus saraksta vai kas pastāv vidē pirms dubultrakstīšanas instalēšanas.</span><span class="sxs-lookup"><span data-stu-id="0f396-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="0f396-107">Lai tīmekļa lomas darbotos kā paredzēts, ir jāizveido jaunas tīmekļa lomas, izmantojot jauno datu modeli.</span><span class="sxs-lookup"><span data-stu-id="0f396-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="0f396-108">Kopumā tabulu mijiedarbības veids ir mainījies, bet tabulas atļaujas debitora portālā nav mainītas.</span><span class="sxs-lookup"><span data-stu-id="0f396-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="0f396-109">Šajā tēmā skaidrots, kā izveidot jaunas tīmekļa lomas, kas darbojas ar jauno uzlaboto datu modeli.</span><span class="sxs-lookup"><span data-stu-id="0f396-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="0f396-110">Šajā diagrammā parādītas tabulas attiecības **bez** puses un globālās adrešu grāmatas datu modeļa:</span><span class="sxs-lookup"><span data-stu-id="0f396-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![bez puses modeļa](media/without-party-model.PNG)

<span data-ttu-id="0f396-112">Šajā diagrammā parādītas tabulas attiecības **ar** puses un globālās adrešu grāmatas datu modeli:</span><span class="sxs-lookup"><span data-stu-id="0f396-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![ar puses modeļi](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="0f396-114">Izveidot jaunu tabulas atļauju</span><span class="sxs-lookup"><span data-stu-id="0f396-114">Create a new table permission</span></span>

<span data-ttu-id="0f396-115">Lai izveidotu šīs jaunās tabulas atļaujas, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="0f396-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="0f396-116">Pieteikties [Power Apps](https://make.powerapps.com) un doties uz jūsu programmām.</span><span class="sxs-lookup"><span data-stu-id="0f396-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="0f396-117">Atlasiet savu portāla pārvaldības programmu.</span><span class="sxs-lookup"><span data-stu-id="0f396-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="0f396-118">Līdzjoslā atlasiet **Drošība > Tabulas atļaujas**.</span><span class="sxs-lookup"><span data-stu-id="0f396-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="0f396-119">Jums ir jāizveido trīs jaunas atļaujas:</span><span class="sxs-lookup"><span data-stu-id="0f396-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="0f396-120">Savienojums kontaktpesona ar pusi</span><span class="sxs-lookup"><span data-stu-id="0f396-120">Contact to Party connection</span></span>
    + <span data-ttu-id="0f396-121">Savienojums puse ar kontu</span><span class="sxs-lookup"><span data-stu-id="0f396-121">Party to Account connection</span></span>
    + <span data-ttu-id="0f396-122">Savienojums konts ar pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="0f396-122">Account to Order connection</span></span>

4. <span data-ttu-id="0f396-123">Izveidojiet un saglabājiet jaunu atļauju savienojumam kontaktpersona ar pusi, iestatot šādus parametrus:</span><span class="sxs-lookup"><span data-stu-id="0f396-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="0f396-124">**Nosaukums**: savienojums puse ar kontu (vai jūsu izvēle)</span><span class="sxs-lookup"><span data-stu-id="0f396-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="0f396-125">**Tabulas nosaukums**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="0f396-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="0f396-126">**Tīmekļa vietne**: Debitoru portāls</span><span class="sxs-lookup"><span data-stu-id="0f396-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="0f396-127">**Tvērums**: kontaktpersona</span><span class="sxs-lookup"><span data-stu-id="0f396-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="0f396-128">**Privilēģijas**: atlasīt visu</span><span class="sxs-lookup"><span data-stu-id="0f396-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="0f396-129">**Tīmekļa lomas**: autentificētie lietotāji, debitora pārstāvis (vai jūsu izvēle)</span><span class="sxs-lookup"><span data-stu-id="0f396-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="0f396-130">Izveidojiet un saglabājiet jaunu atļauju savienojumam puse ar kontu, iestatot šādus parametrus:</span><span class="sxs-lookup"><span data-stu-id="0f396-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="0f396-131">**Nosaukums**: savienojums puse ar kontu (vai jūsu izvēle)</span><span class="sxs-lookup"><span data-stu-id="0f396-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="0f396-132">**Tabulas nosaukums**: konts</span><span class="sxs-lookup"><span data-stu-id="0f396-132">**Table Name**: account</span></span>
    + <span data-ttu-id="0f396-133">**Tīmekļa vietne**: Debitoru portāls</span><span class="sxs-lookup"><span data-stu-id="0f396-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="0f396-134">**Tvērums**: pamatelements</span><span class="sxs-lookup"><span data-stu-id="0f396-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="0f396-135">**Privilēģijas**: atlasīt visu</span><span class="sxs-lookup"><span data-stu-id="0f396-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="0f396-136">**Vecāktabavas atļauja**: savienojumam kontaktpersona ar pusi</span><span class="sxs-lookup"><span data-stu-id="0f396-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="0f396-137">Izveidojiet un saglabājiet jaunu atļauju savienojumam konts ar pasūtījumu, iestatot šādus parametrus:</span><span class="sxs-lookup"><span data-stu-id="0f396-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="0f396-138">**Nosaukums**: savienojums konts ar pasūtījumu (vai jūsu izvēle)</span><span class="sxs-lookup"><span data-stu-id="0f396-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="0f396-139">**Tabulas nosaukums**: pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="0f396-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="0f396-140">**Tīmekļa vietne**: Debitoru portāls</span><span class="sxs-lookup"><span data-stu-id="0f396-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="0f396-141">**Tvērums**: pamatelements</span><span class="sxs-lookup"><span data-stu-id="0f396-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="0f396-142">**Privilēģijas**: atlasīt visu</span><span class="sxs-lookup"><span data-stu-id="0f396-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="0f396-143">**Vecāktabavas atļauja**: savienojumam puse ar kontu</span><span class="sxs-lookup"><span data-stu-id="0f396-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
