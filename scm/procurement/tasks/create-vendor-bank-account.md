--- 
title: Kreditora bankas konta izveide
description: "Šajā procedūrā ir parādīts, kā izveidot bankas kontu kreditoram."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: adb759c59d7275e7323dbb760de56acdef2e3cff
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="540b5-103">Kreditora bankas konta izveide</span><span class="sxs-lookup"><span data-stu-id="540b5-103">Create a vendor bank account</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="540b5-104">Šajā procedūrā ir parādīts, kā izveidot bankas kontu kreditoram.</span><span class="sxs-lookup"><span data-stu-id="540b5-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="540b5-105">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="540b5-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="540b5-106">Pārejiet uz sadaļu Sagāde un avoti > Kreditori > Visi kreditori.</span><span class="sxs-lookup"><span data-stu-id="540b5-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="540b5-107">Atlasiet kreditoru, kuram vēlaties izveidot bankas kontu, un pēc tam noklikšķiniet uz saites vienumā Kreditora konta ID.</span><span class="sxs-lookup"><span data-stu-id="540b5-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="540b5-108">Darbību rūtī noklikšķiniet uz Kreditors.</span><span class="sxs-lookup"><span data-stu-id="540b5-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="540b5-109">Noklikšķiniet uz Banku konti.</span><span class="sxs-lookup"><span data-stu-id="540b5-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="540b5-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="540b5-110">Click New.</span></span>
6. <span data-ttu-id="540b5-111">Ierakstiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="540b5-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="540b5-112">Šis ID tiks izmantots, lai identificētu bankas kontu kreditora ierakstam.</span><span class="sxs-lookup"><span data-stu-id="540b5-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="540b5-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="540b5-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="540b5-114">Ievadiet vai atlasiet vērtību laukā Banku grupas.</span><span class="sxs-lookup"><span data-stu-id="540b5-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="540b5-115">Atlasiet kādu opciju laukā Maršrutēšanas numura tips.</span><span class="sxs-lookup"><span data-stu-id="540b5-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="540b5-116">Šis ir maršrutēšanas numura tips, kas tiek izmantots starptautiskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="540b5-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="540b5-117">Laukā Bankas konta numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="540b5-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="540b5-118">Ierakstiet vērtību laukā SWIFT kods.</span><span class="sxs-lookup"><span data-stu-id="540b5-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="540b5-119">Ievadiet vērtību laukā IBAN.</span><span class="sxs-lookup"><span data-stu-id="540b5-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="540b5-120">IBAN numuram ir jābūt pareizajā formātā.</span><span class="sxs-lookup"><span data-stu-id="540b5-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="540b5-121">Piemēram, varat izmantot DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="540b5-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="540b5-122">Bankas konta statuss ir Aktīvs, ja ir sasniegts Aktīvais datums un nav pārsniegts Beigu datums.</span><span class="sxs-lookup"><span data-stu-id="540b5-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="540b5-123">Tas ir aktīvs arī tad, ja ir tukšs gan lauks Aktīvais datums, gan lauks Beigu datums.</span><span class="sxs-lookup"><span data-stu-id="540b5-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="540b5-124">Ja gan lauka Aktīvais datums, gan lauka Beigu datums datumi vēl nav pienākuši, tad elektroniskie maksājumi nav pieejami.</span><span class="sxs-lookup"><span data-stu-id="540b5-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="540b5-125">Citi maksājumu tipi ir pieejami un šis bankas konts ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="540b5-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="540b5-126">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="540b5-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="540b5-127">Ierakstiet kādu vērtību laukā Teksta kods.</span><span class="sxs-lookup"><span data-stu-id="540b5-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="540b5-128">Šajā laukā ir norādīts kods, kas būs redzams saņēmēja bankas izrakstā.</span><span class="sxs-lookup"><span data-stu-id="540b5-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="540b5-129">Ierakstiet kādu vērtību laukā Ziņojums bankai.</span><span class="sxs-lookup"><span data-stu-id="540b5-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="540b5-130">Ierakstiet kādu vērtību laukā Maiņas kursa atsauce.</span><span class="sxs-lookup"><span data-stu-id="540b5-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="540b5-131">Šis ir atsauces numurs jebkuram turpmākā vai fiksēta termiņa maiņas kursam.</span><span class="sxs-lookup"><span data-stu-id="540b5-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="540b5-132">Laukā Valūta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="540b5-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="540b5-133">Kad tiek izsniegtas pārbaudes, šajā sadaļā ir sniegts apskats par to statusu (gaida vai apstiprināts).</span><span class="sxs-lookup"><span data-stu-id="540b5-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="540b5-134">Izvērsiet sadaļu Adrese.</span><span class="sxs-lookup"><span data-stu-id="540b5-134">Expand the Address section.</span></span>
19. <span data-ttu-id="540b5-135">Izvērsiet atlasi Pārbaudes.</span><span class="sxs-lookup"><span data-stu-id="540b5-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="540b5-136">Izvērsiet sadaļu Kontaktinformācija.</span><span class="sxs-lookup"><span data-stu-id="540b5-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="540b5-137">Laukā Tālrunis ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="540b5-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="540b5-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="540b5-138">Close the page.</span></span>
23. <span data-ttu-id="540b5-139">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="540b5-139">Click Edit.</span></span>
24. <span data-ttu-id="540b5-140">Izvērsiet sadaļu Maksājums.</span><span class="sxs-lookup"><span data-stu-id="540b5-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="540b5-141">Laukā Bankas konts atlasiet tikko izveidoto kontu.</span><span class="sxs-lookup"><span data-stu-id="540b5-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="540b5-142">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="540b5-142">Click Save.</span></span>
    * <span data-ttu-id="540b5-143">Šo adresi var pārmantot no banku grupas, ja tāda ir norādīta, vai šeit varat to pievienot.</span><span class="sxs-lookup"><span data-stu-id="540b5-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  


