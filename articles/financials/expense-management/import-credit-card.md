---
title: "Kredītkaršu transakciju importēšana un uzturēšana"
description: "Šajā tēmā ir paskaidrots, kā importēt un uzturēt ar izdevumiem saistītas kredītkaršu transakcijas. Šīs transakcijas var iestatīt tā, lai tās regulāri tiktu importētas automātiski, vai tās var importēt manuāli, kad vien nepieciešams."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: 3af32fbe435d92e7ca45b757414c325e6d389ac1
ms.contentlocale: lv-lv
ms.lasthandoff: 01/12/2018

---

# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="4ceaa-104">Kredītkaršu transakciju importēšana un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="4ceaa-104">Import and maintain credit card transactions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4ceaa-105">Ar izdevumiem saistītās kredītkaršu transakcijas var iestatīt tā, lai tās regulāri tiktu importētas automātiski.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="4ceaa-106">Ja vēlaties, šīs transakcijas var importēt arī manuāli, kad tās ir nepieciešamas.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="4ceaa-107">Kredītkaršu transakcijas tiek importētas caur datu elementu Kredītkaršu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="4ceaa-108">Papildinformāciju par datu elementiem skatiet rakstā [Datu elementi](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="4ceaa-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="4ceaa-109">Importēt kredītkartes darbības</span><span class="sxs-lookup"><span data-stu-id="4ceaa-109">Import credit card transactions</span></span>

1. <span data-ttu-id="4ceaa-110">Lapā **Kredītkaršu transakcijas** atlasiet vienumu **Importēt transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="4ceaa-111">Ja datu pārvaldību atverat pirmo reizi, tad pirms turpināšanas sistēmai ir jāatjaunina datu elementu saraksts.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="4ceaa-112">Laukā **Nosaukums** ievadiet unikālu importēšanas darba aprakstu.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="4ceaa-113">Laukā **Avota datu formāts** atlasiet tā faila formātu, kurā ir importējamās kredītkaršu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="4ceaa-114">Atlasiet **Augšupielādēt**, un pēc tam atrodiet un atlasiet importējamo failu.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="4ceaa-115">Kad fails ir augšupielādēts, validējiet kredītkaršu transakciju faila kartējumu un datu elementa Kredītkaršu transakcijas kolonnas, elementā atlasot saiti **Skatīt karti**.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="4ceaa-116">Ja pastāv kartējuma kļūdas vai ja kartējums ir jāmaina, veiciet kartējuma izmaiņas no cilnes **Kartēšanas vizualizēšana** vai cilnes **Detalizēta informācija par kartēšanu**.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="4ceaa-117">Lai kredītkaršu transakcijas automatizētu, atlasiet **Izveidot periodisku datu darbu**.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="4ceaa-118">Pēc tam varat iestatīt periodiskumu, kas nosaka, cik bieži kredītkaršu transakcijas ir nepieciešams importēt.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="4ceaa-119">Pēc pabeigšanas atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="4ceaa-120">Lai atlasīto failu importētu tūlīt, atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="4ceaa-121">Ja importēšanas laikā rodas kļūdas, varat skatīt izpildes žurnālu vai sagatavošanas posmu datus, lai redzētu, kādas kļūdas ir jālabo, nodrošinot sekmīgu importēšanu.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="4ceaa-122">Ja ir jāimportē vairāki failu formāti, tad katram formāta tipam ir jāizveido atsevišķi importēšanas darbi.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="4ceaa-123">Atlaistu darbinieku kredītkaršu transakciju atkārtota piešķiršana</span><span class="sxs-lookup"><span data-stu-id="4ceaa-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="4ceaa-124">Kad darbinieka ieraksts tiek izbeigts, šī darbinieka domēna pakalpojuma Active Directory (AD DS) konts tiek atspējots.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="4ceaa-125">Taču var pastāvēt aktīvas kredītkaršu transakcijas, kuras joprojām ir jāietver izdevumos un ir jākompensē.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="4ceaa-126">No lapas **Kredītkaršu transakcijas** šo darbinieku varat atkārtoti piešķirt jebkurai kredītkartes transakcijai, kur saistītais darbinieks ir atlaists.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="4ceaa-127">Atlasiet vienu vai vairākas kredītkaršu transakcijas un pēc tam atlasiet **Atkārtoti piešķirt transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="4ceaa-128">Pēc tam varat atlasīt citu darbinieku, kuram šīs kredītkaršu transakcijas piešķirt.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="4ceaa-129">Kad kredītkaršu transakcijas ir piešķirtas atkārtoti, tās var atlasīt izdevumu pārskatam un apmaksāt caur izdevumu pārskata kompensēšanas parasto procesu.</span><span class="sxs-lookup"><span data-stu-id="4ceaa-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

