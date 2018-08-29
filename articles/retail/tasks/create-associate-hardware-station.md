--- 
title: "Aparatūras staciju izveide"
description: "Šajā procedūrā ir aprakstīts, kā izveidot jaunu aparatūras staciju."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 3551e37c6aae37c01b5cacff8b908faaf75fb3e2
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="create-hardware-stations"></a><span data-ttu-id="46126-103">Aparatūras staciju izveide</span><span class="sxs-lookup"><span data-stu-id="46126-103">Create hardware stations</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="46126-104">Šajā procedūrā ir aprakstīts, kā izveidot jaunu aparatūras staciju.</span><span class="sxs-lookup"><span data-stu-id="46126-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="46126-105">Jauns aparatūras profils tiek izveidots un izmantots, lai jaunas aparatūras stacijas pievienotu iepriekš definētajam veikalam (kanālam).</span><span class="sxs-lookup"><span data-stu-id="46126-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="46126-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="46126-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="46126-107">Dodieties uz Komercijas rekvizīti > Kanāli >..</span><span class="sxs-lookup"><span data-stu-id="46126-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="46126-108">> ..</span><span class="sxs-lookup"><span data-stu-id="46126-108">> ..</span></span> <span data-ttu-id="46126-109">> ..</span><span class="sxs-lookup"><span data-stu-id="46126-109">> ..</span></span> <span data-ttu-id="46126-110">> Aparatūras stacijas profili.</span><span class="sxs-lookup"><span data-stu-id="46126-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="46126-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="46126-111">Click New.</span></span>
3. <span data-ttu-id="46126-112">Laukā Aparatūras stacijas ID ierakstiet TestHWProfile.</span><span class="sxs-lookup"><span data-stu-id="46126-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="46126-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="46126-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="46126-114">Laukā Porta numurs ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="46126-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="46126-115">Laukā Aparatūras profils noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="46126-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="46126-116">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="46126-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="46126-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="46126-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="46126-118">Laukā Pakotnes nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="46126-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="46126-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="46126-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="46126-120">Šis ir standarta pakotne, kurā tiek nodrošināta jauna vide.</span><span class="sxs-lookup"><span data-stu-id="46126-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="46126-121">Versijas numurs var atšķirties.</span><span class="sxs-lookup"><span data-stu-id="46126-121">The version number may vary.</span></span>  
11. <span data-ttu-id="46126-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="46126-122">Click Save.</span></span>
12. <span data-ttu-id="46126-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="46126-123">Close the page.</span></span>
13. <span data-ttu-id="46126-124">Dodieties uz Mazumtirdzniecība un komercija > Kanāli > Visi mazumtirdzniecības veikali.</span><span class="sxs-lookup"><span data-stu-id="46126-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="46126-125">Sarakstā atlasiet 17. rindu.</span><span class="sxs-lookup"><span data-stu-id="46126-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="46126-126">Ja tiek izmantoti demonstrācijas uzņēmuma “USRT” dati, šis ir Houston veikals.</span><span class="sxs-lookup"><span data-stu-id="46126-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="46126-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="46126-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="46126-128">Pārslēdziet sadaļas Aparatūras stacijas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="46126-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="46126-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="46126-129">Click Add.</span></span>
18. <span data-ttu-id="46126-130">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="46126-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="46126-131">Laukā Profila ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="46126-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="46126-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="46126-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="46126-133">Tam ir jābūt jaunajam aparatūras stacijas profilam, kas tika izveidots iepriekšējās darbībās.</span><span class="sxs-lookup"><span data-stu-id="46126-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="46126-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="46126-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="46126-135">Laukā Resursdatora nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46126-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="46126-136">Laukā EFT termināļa ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="46126-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="46126-137">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="46126-137">Click Save.</span></span>


