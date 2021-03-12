---
title: Bankas iestāžu iestatīšana un garantijas vēstuļu grāmatošanas profili
description: Šis uzdevums izveido bankas iestādes un grāmatošanas profilu, kas ir vajadzīgs, lai apstrādātu garantijas vēstuli.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6da3b9358192997de1d0231e5c9c8eaba92a23b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976271"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="7b356-103">Bankas iestāžu iestatīšana un garantijas vēstuļu grāmatošanas profili</span><span class="sxs-lookup"><span data-stu-id="7b356-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b356-104">Šis uzdevums izveido bankas iestādes un grāmatošanas profilu, kas ir vajadzīgs, lai apstrādātu garantijas vēstuli.</span><span class="sxs-lookup"><span data-stu-id="7b356-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="7b356-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="7b356-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="7b356-106">Virsgrāmatas parametrs</span><span class="sxs-lookup"><span data-stu-id="7b356-106">General ledger parameter</span></span>
1. <span data-ttu-id="7b356-107">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="7b356-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="7b356-108">Izvērsiet sadaļu Bankas dokuments.</span><span class="sxs-lookup"><span data-stu-id="7b356-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="7b356-109">Atlasiet opciju Iespējot garantijas vēstuli.</span><span class="sxs-lookup"><span data-stu-id="7b356-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="7b356-110">Laukā Darbību žurnāls noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7b356-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7b356-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7b356-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="7b356-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7b356-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7b356-113">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="7b356-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="7b356-114">Numuru sērijas koda definēšana garantijas vēstules numuram un garantijas vēstuļu transakciju atsaucēm</span><span class="sxs-lookup"><span data-stu-id="7b356-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="7b356-115">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7b356-115">Click Save.</span></span>
9. <span data-ttu-id="7b356-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7b356-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="7b356-117">Bankas iestādes izveide</span><span class="sxs-lookup"><span data-stu-id="7b356-117">Create Bank facility</span></span>
1. <span data-ttu-id="7b356-118">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Bankas iestādes.</span><span class="sxs-lookup"><span data-stu-id="7b356-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="7b356-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7b356-119">Click New.</span></span>
3. <span data-ttu-id="7b356-120">Laukā Iestādes grupa ievadiet bankas iestāžu grupas nosaukumu garantijas vēstules transakcijai.</span><span class="sxs-lookup"><span data-stu-id="7b356-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="7b356-121">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="7b356-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7b356-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7b356-122">Click Save.</span></span>
6. <span data-ttu-id="7b356-123">Noklikšķiniet uz cilnes Iestādes tipi.</span><span class="sxs-lookup"><span data-stu-id="7b356-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="7b356-124">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7b356-124">Click New.</span></span>
8. <span data-ttu-id="7b356-125">Laukā Iestādes tips ievadiet tā bankas iestāžu tipa nosaukumu, kas saistīts ar bankas iestādes līgumu.</span><span class="sxs-lookup"><span data-stu-id="7b356-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="7b356-126">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7b356-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="7b356-127">Laukā Iestādes grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7b356-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7b356-128">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7b356-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="7b356-129">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7b356-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="7b356-130">Laukā Iestādes būtība atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="7b356-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="7b356-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7b356-131">Click Save.</span></span>
15. <span data-ttu-id="7b356-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7b356-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="7b356-133">Bankas grāmatošanas profils</span><span class="sxs-lookup"><span data-stu-id="7b356-133">Bank posting profile</span></span>
1. <span data-ttu-id="7b356-134">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Bankas dokumentu grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="7b356-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="7b356-135">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7b356-135">Click New.</span></span>
3. <span data-ttu-id="7b356-136">Laukā Konta/grupas numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7b356-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7b356-137">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7b356-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7b356-138">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7b356-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7b356-139">Laukā Apmaksāt konta rēķinus atlasiet galveno norēķinu kontu.</span><span class="sxs-lookup"><span data-stu-id="7b356-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="7b356-140">Laukā Maksājumu konts atlasiet kontu izdevumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="7b356-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="7b356-141">Laukā Uzcenojuma konts atlasiet kontu uzcenojuma transakcijai.</span><span class="sxs-lookup"><span data-stu-id="7b356-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="7b356-142">Laukā Likvidācijas konts atlasiet likvidācijas kontu garantijas vēstules transakcijai.</span><span class="sxs-lookup"><span data-stu-id="7b356-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="7b356-143">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7b356-143">Click Save.</span></span>
11. <span data-ttu-id="7b356-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7b356-144">Close the page.</span></span>

