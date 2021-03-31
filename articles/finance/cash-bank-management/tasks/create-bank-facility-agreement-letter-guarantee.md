---
title: Bankas iestādes līguma izveide garantijas vēstulei
description: Šis uzdevums izveido bankas iestādes līgumu, lai apstrādātu garantijas vēstuli.
author: panolte
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9c93a76bc7e29cb98834b9028748330710a4cef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225468"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="ff065-103">Bankas iestādes līguma izveide garantijas vēstulei</span><span class="sxs-lookup"><span data-stu-id="ff065-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff065-104">Šis uzdevums izveido bankas iestādes līgumu, lai apstrādātu garantijas vēstuli.</span><span class="sxs-lookup"><span data-stu-id="ff065-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="ff065-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="ff065-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="ff065-106">Izveidot bankas iestādes līgumu</span><span class="sxs-lookup"><span data-stu-id="ff065-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="ff065-107">Pārejiet uz sadaļu Kases un bankas pārvaldība > Garantijas vēstules > Bankas iestādes līgumi.</span><span class="sxs-lookup"><span data-stu-id="ff065-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="ff065-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ff065-108">Click New.</span></span>
3. <span data-ttu-id="ff065-109">Laukā Līguma numurs ievadiet darījuma bankas līguma numuru.</span><span class="sxs-lookup"><span data-stu-id="ff065-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="ff065-110">Laukā Bankas konts atlasiet bankas konta numuru, kuram ir atvērta garantijas vēstule.</span><span class="sxs-lookup"><span data-stu-id="ff065-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="ff065-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ff065-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ff065-112">Laukā Sākuma datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="ff065-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="ff065-113">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="ff065-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="ff065-114">Pārslēdziet sadaļas Vispārīgi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="ff065-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="ff065-115">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="ff065-115">Click Add line.</span></span>
10. <span data-ttu-id="ff065-116">Laukā Iestādes tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="ff065-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ff065-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ff065-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ff065-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="ff065-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="ff065-119">Laukā Ierobežojums ievadiet summu, par kuru ir veikta vienošanās ar banku.</span><span class="sxs-lookup"><span data-stu-id="ff065-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="ff065-120">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff065-120">Click Save.</span></span>
15. <span data-ttu-id="ff065-121">Pārslēdziet sadaļas Garantijas vēstule paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="ff065-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="ff065-122">Laukā Aprēķina metode atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="ff065-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="ff065-123">Ievadiet nepieciešamo aprēķina metodi un procentu informāciju par naudas summu, izdošanas komisiju, akreditīva pagarināšanas komisiju, vērtības paaugstināšanas komisiju vai vērtības pazemināšanas komisiju.</span><span class="sxs-lookup"><span data-stu-id="ff065-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="ff065-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff065-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="ff065-125">Bankas iestādes līguma pagarināšana</span><span class="sxs-lookup"><span data-stu-id="ff065-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="ff065-126">Noklikšķiniet uz Paplašināt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ff065-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="ff065-127">Laukā Jauns līguma numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ff065-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="ff065-128">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="ff065-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="ff065-129">Noklikšķiniet uz Paplašināt.</span><span class="sxs-lookup"><span data-stu-id="ff065-129">Click Extend.</span></span>
5. <span data-ttu-id="ff065-130">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ff065-130">Click Save.</span></span>
6. <span data-ttu-id="ff065-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ff065-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]