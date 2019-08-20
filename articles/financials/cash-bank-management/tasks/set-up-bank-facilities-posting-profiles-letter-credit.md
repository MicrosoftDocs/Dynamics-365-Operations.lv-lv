---
title: Bankas iestāžu iestatīšana un kredītvēstuļu grāmatošanas profili
description: Šajā procedūrā ir aprakstīts, kā izveidot bankas iestādi un grāmatošanas profilu, lai apstrādātu akreditīvus.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3d35bd265ad31da083d2437fae886569766085
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841901"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="c5f12-103">Bankas iestāžu iestatīšana un kredītvēstuļu grāmatošanas profili</span><span class="sxs-lookup"><span data-stu-id="c5f12-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5f12-104">Šajā procedūrā ir aprakstīts, kā izveidot bankas iestādi un grāmatošanas profilu, lai apstrādātu akreditīvus.</span><span class="sxs-lookup"><span data-stu-id="c5f12-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="c5f12-105">Šajos uzdevumos tiek izmantots demonstrācijas uzņēmums "USMF".</span><span class="sxs-lookup"><span data-stu-id="c5f12-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="c5f12-106">Virsgrāmatas parametrs</span><span class="sxs-lookup"><span data-stu-id="c5f12-106">General ledger parameter</span></span>
1. <span data-ttu-id="c5f12-107">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="c5f12-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="c5f12-108">Izvērsiet sadaļu Bankas dokuments.</span><span class="sxs-lookup"><span data-stu-id="c5f12-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="c5f12-109">Atlasiet opciju Iespējot akreditīva importu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="c5f12-110">Atlasiet opciju Iespējot akreditīva eksportu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="c5f12-111">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c5f12-111">Click Save.</span></span>
6. <span data-ttu-id="c5f12-112">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="c5f12-113">Bankas iestādes izveide</span><span class="sxs-lookup"><span data-stu-id="c5f12-113">Create Bank facility</span></span>
1. <span data-ttu-id="c5f12-114">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Bankas iestādes.</span><span class="sxs-lookup"><span data-stu-id="c5f12-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="c5f12-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c5f12-115">Click New.</span></span>
3. <span data-ttu-id="c5f12-116">Laukā Iestādes grupa ievadiet bankas iestāžu grupas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="c5f12-117">Laukā Apraksts ievadiet bankas iestāžu grupas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="c5f12-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c5f12-118">Click Save.</span></span>
6. <span data-ttu-id="c5f12-119">Noklikšķiniet uz cilnes Iestādes tipi.</span><span class="sxs-lookup"><span data-stu-id="c5f12-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="c5f12-120">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c5f12-120">Click New.</span></span>
8. <span data-ttu-id="c5f12-121">Laukā Iestādes tips ierakstiet unikālu kodu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="c5f12-122">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c5f12-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="c5f12-123">Laukā Iestādes grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="c5f12-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="c5f12-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c5f12-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="c5f12-126">Laukā Iestādes būtība atlasiet bankas iestādes būtību.</span><span class="sxs-lookup"><span data-stu-id="c5f12-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="c5f12-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c5f12-127">Click Save.</span></span>
15. <span data-ttu-id="c5f12-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="c5f12-129">Bankas grāmatošanas profils</span><span class="sxs-lookup"><span data-stu-id="c5f12-129">Bank posting profile</span></span>
1. <span data-ttu-id="c5f12-130">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Bankas dokumentu grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="c5f12-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="c5f12-131">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c5f12-131">Click New.</span></span>
3. <span data-ttu-id="c5f12-132">Laukā Konta/grupas numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c5f12-133">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c5f12-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c5f12-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c5f12-135">Atlasiet galveno norēķinu kontu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="c5f12-136">Šis konts tiek izmantots, aprēķinot naudas plūsmas prognozi.</span><span class="sxs-lookup"><span data-stu-id="c5f12-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="c5f12-137">Laukā Maksājumu konts atlasiet kontu izdevumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="c5f12-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="c5f12-138">Laukā Uzcenojuma konts atlasiet kontu uzcenojuma transakcijām.</span><span class="sxs-lookup"><span data-stu-id="c5f12-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="c5f12-139">Šis konts tiek debetēts, ja atvēršanas rezerve ir grāmatota un kreditēta, grāmatojot maksājumu.</span><span class="sxs-lookup"><span data-stu-id="c5f12-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="c5f12-140">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c5f12-140">Click Save.</span></span>

