---
title: Kreditora bankas konta izveide
description: Šajā procedūrā ir parādīts, kā izveidot bankas kontu kreditoram.
author: mkirknel
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab0a108b5c8b7f2f90a4d33d8a9ff088335c18d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207667"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="67f5e-103">Kreditora bankas konta izveide</span><span class="sxs-lookup"><span data-stu-id="67f5e-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67f5e-104">Šajā procedūrā ir parādīts, kā izveidot bankas kontu kreditoram.</span><span class="sxs-lookup"><span data-stu-id="67f5e-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="67f5e-105">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="67f5e-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="67f5e-106">Ejiet uz **Navigācijas rūts > Moduļi > Iepirkumi un ārpakalpojumi > Piegādātāji > Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="67f5e-107">Atlasiet piegādātāju, kam vēlaties izveidot bankas kontu, un tad noklikšķiniet uz saites **Piegādātāja konta ID**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="67f5e-108">**Darbību rūtī** noklikšķiniet uz **Piegādātājs**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-108">On the **Action pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="67f5e-109">Noklikšķiniet uz **Bankas konti**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="67f5e-110">**Darbību rūtī** noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-110">On the **Action pane**, click **New**.</span></span>
6. <span data-ttu-id="67f5e-111">Laukā **Bankas konts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="67f5e-112">Šis ID tiks izmantots, lai identificētu bankas kontu kreditora ierakstam.</span><span class="sxs-lookup"><span data-stu-id="67f5e-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="67f5e-113">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="67f5e-114">Laukā **Banku grupas** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="67f5e-115">Laukā **Maršrutēšanas numura veids** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="67f5e-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="67f5e-116">Šis ir maršrutēšanas numura tips, kas tiek izmantots starptautiskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="67f5e-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="67f5e-117">Laukā **Bankas konta numurs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="67f5e-118">Laukā **SWIFT kods** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="67f5e-119">Laukā **IBAN** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="67f5e-120">IBAN numuram ir jābūt pareizajā formātā.</span><span class="sxs-lookup"><span data-stu-id="67f5e-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="67f5e-121">Piemēram, varat izmantot DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="67f5e-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="67f5e-122">Bankas konta statuss ir Aktīvs, ja ir sasniegts Aktīvais datums un nav pārsniegts Beigu datums.</span><span class="sxs-lookup"><span data-stu-id="67f5e-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="67f5e-123">Tas ir aktīvs arī tad, ja ir tukšs gan lauks Aktīvais datums, gan lauks Beigu datums.</span><span class="sxs-lookup"><span data-stu-id="67f5e-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="67f5e-124">Ja gan lauka Aktīvais datums, gan lauka Beigu datums datumi vēl nav pienākuši, tad elektroniskie maksājumi nav pieejami.</span><span class="sxs-lookup"><span data-stu-id="67f5e-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="67f5e-125">Citi maksājumu tipi ir pieejami un šis bankas konts ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="67f5e-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="67f5e-126">Izvērsiet sadaļu **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="67f5e-127">Laukā **Teksta kods** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="67f5e-128">Šajā laukā ir norādīts kods, kas būs redzams saņēmēja bankas izrakstā.</span><span class="sxs-lookup"><span data-stu-id="67f5e-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="67f5e-129">Laukā **Ziņojums bankai** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="67f5e-130">Ievadiet vērtību laukā **Maiņas atsauce**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="67f5e-131">Šis ir atsauces numurs jebkuram turpmākā vai fiksēta termiņa maiņas kursam.</span><span class="sxs-lookup"><span data-stu-id="67f5e-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="67f5e-132">Laukā **Valūta** ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="67f5e-133">Kad tiek izsniegtas pārbaudes, šajā sadaļā ir sniegts apskats par to statusu (gaida vai apstiprināts).</span><span class="sxs-lookup"><span data-stu-id="67f5e-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="67f5e-134">Izvērsiet sadaļu **Adrese**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="67f5e-135">Izvērsiet sadaļu **Iepriekšējas piezīmes**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="67f5e-136">Izvērsiet sadaļu **Kontaktinformācija**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="67f5e-137">Laukā **Tālrunis** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="67f5e-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="67f5e-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="67f5e-138">Close the page.</span></span>
23. <span data-ttu-id="67f5e-139">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-139">Click **Edit**.</span></span>
24. <span data-ttu-id="67f5e-140">Izvērsiet sadaļu **Maksājums**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="67f5e-141">Laukā **Bankas konts** atlasiet kontu, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="67f5e-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="67f5e-142">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="67f5e-142">Click **Save**.</span></span> <span data-ttu-id="67f5e-143">Šo adresi var pārmantot no banku grupas, ja tāda ir norādīta, vai šeit varat to pievienot.</span><span class="sxs-lookup"><span data-stu-id="67f5e-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

