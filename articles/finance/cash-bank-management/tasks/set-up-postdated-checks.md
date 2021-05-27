---
title: Ar iepriekšēju datumu datētu čeku iestatīšana
description: Šajā tēmā izskaidrots, kā norādīt, vai grāmatot ar iepriekšēju datumu datētu čeku žurnāla ierakstus, ko izmantot ierakstu dzēšanai un kreditoru maksājumiem.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026209"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="28036-103">Ar iepriekšēju datumu datētu čeku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="28036-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28036-104">Šajā tēmā izskaidrots, kā norādīt, vai grāmatot ar iepriekšēju datumu datētu čeku žurnāla ierakstus, ko izmantot ierakstu dzēšanai un kreditoru maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="28036-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="28036-105">Varat arī norādīt izsniegto čeku, saņemt čeku un ieturētā nodokļa klīringa kontus.</span><span class="sxs-lookup"><span data-stu-id="28036-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="28036-106">Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā.</span><span class="sxs-lookup"><span data-stu-id="28036-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="28036-107">Varat norādīt, vai čekam ir jābūt atspoguļotam uzskaites grāmatās pirms tās dzēšanas termiņa.</span><span class="sxs-lookup"><span data-stu-id="28036-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="28036-108">Šīs procedūras izpildei nepieciešama loma Kasieris.</span><span class="sxs-lookup"><span data-stu-id="28036-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="28036-109">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="28036-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="28036-110">Ar iepriekšēju datumu datētu čeku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="28036-110">Set up postdated checks</span></span>
1. <span data-ttu-id="28036-111">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="28036-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="28036-112">Noklikšķiniet uz cilnes Ar iepriekšēju datumu datēti čeki.</span><span class="sxs-lookup"><span data-stu-id="28036-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="28036-113">Atzīmējiet vai notīriet izvēles rūtiņu Iespējot čekus, kas datēti ar iepriekšēju datumu.</span><span class="sxs-lookup"><span data-stu-id="28036-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="28036-114">Atzīmējiet vai notīriet izvēles rūtiņu Grāmatot žurnāla ierakstus, kas atbilst čekiem, kas datēti ar iepriekšēju datumu.</span><span class="sxs-lookup"><span data-stu-id="28036-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="28036-115">Laukā Klīringa konts izsniegtajiem čekiem norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="28036-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="28036-116">Laukā Klīringa konts saņemtajiem čekiem norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="28036-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="28036-117">Laukā Virsgrāmatas žurnāls ierakstu dzēšanai ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="28036-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="28036-118">Laukā Pārsūtīt ar iepriekšēju datumu datētus čekus uz šo kreditoru maksājumu žurnālu ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="28036-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="28036-119">Laukā Ieturētā nodokļa tīrīšanas konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="28036-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="28036-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="28036-120">Click Save.</span></span>
11. <span data-ttu-id="28036-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="28036-121">Close the page.</span></span>
12. <span data-ttu-id="28036-122">Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="28036-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="28036-123">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="28036-123">Click New.</span></span>
14. <span data-ttu-id="28036-124">Ierakstiet vērtību laukā Maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="28036-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="28036-125">Atlasiet opciju Ar iepriekšēju datumu datētu čeku klīringa grāmatošana, lai norādītu, ka čeka summa ir iegrāmatota klīringa kontā.</span><span class="sxs-lookup"><span data-stu-id="28036-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="28036-126">Laukā Konta tips atlasiet Banka.</span><span class="sxs-lookup"><span data-stu-id="28036-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="28036-127">Maksājuma metodes korespondējošais konts būs banka.</span><span class="sxs-lookup"><span data-stu-id="28036-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="28036-128">Laukā Maksājumu konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="28036-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="28036-129">Atlasiet bankas kontu, kas tiek izmantots, lai atskaitītu rēķina summu.</span><span class="sxs-lookup"><span data-stu-id="28036-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="28036-130">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="28036-130">Click Save.</span></span>
19. <span data-ttu-id="28036-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="28036-131">Close the page.</span></span>
> [!NOTE]
> <span data-ttu-id="28036-132">Lai varētu bankas kontā grāmatot ar datumu dalāmu čeku, ja sesijas datums ir lielāks par vai vienāds ar samaksas beigu datumu, ir jāiespējo līdzeklis **Termiņa beigu datuma pārbaude maksājumu žurnāla grāmatošanai grāmatotiem čekiem bankas kontā**.</span><span class="sxs-lookup"><span data-stu-id="28036-132">To be able to post a postdated check to a bank account when the session date is greater than or equal to the maturity date, you must enable the feature **Maturity date validation of posting payment journal with postdated checks to bank account**.</span></span> <span data-ttu-id="28036-133">Šī funkcija ļauj grāmatot maksājumu žurnālus kreditoriem vai debitoriem ar grāmatotiem čekiem, ja sesijas datums ir lielāks vai vienāds ar termiņa beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="28036-133">This feature allows you to post payment journals for vendors or customers with postdated checks, when the session date is greater than or equal to the maturity date.</span></span>
> 
> <span data-ttu-id="28036-134">Iestatot **Maksāšanas metodi** (**Kreditori > Maksājumu iestatījumi > Maksājuma metodes**), neaizpildiet **Pagaidu kontu**.</span><span class="sxs-lookup"><span data-stu-id="28036-134">When setting the **Method of payment** (**Accounts payable > Payment setup > Methods of payment**), do not fill in **Bridging account**.</span></span> <span data-ttu-id="28036-135">Šajā gadījumā korespondējošais konts tiek aizpildīts ar bankas kontu, kas iestatīts **Maksājuma metodē**.</span><span class="sxs-lookup"><span data-stu-id="28036-135">In this case, the offset account is filled in with the bank account, which is set up in the **Method of payment**.</span></span>
>  
> <span data-ttu-id="28036-136">Ja ir aktivizēta šī funkcija un sesijas datums ir pirms termiņa beigu datuma, grāmatojot maksājumu žurnālu, tiek parādīts šāds kļūdas ziņojums: "Termiņa beigu datumam ir jābūt mazākam par sesijas datumu vai vienādam ar to, ja korespondējošā konta tips ir Banka".</span><span class="sxs-lookup"><span data-stu-id="28036-136">When the feature is enabled and the session date is less than the maturity date, the following error message is displayed when posting a payment journal, "Maturity date must be less or equal to the session date if offset account type is Bank".</span></span> <span data-ttu-id="28036-137">Ja šī funkcija nav aktivizēta, varat grāmatot maksājumu žurnālu ar vēlāku datumu, ja sesijas datums ir pirms termiņa beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="28036-137">If the feature is not enabled, you can post a payment journal with a postdated check when the session date is less than the maturity date.</span></span>    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
