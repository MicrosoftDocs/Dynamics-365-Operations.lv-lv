---
title: SEPA tiešā debeta pilnvarojuma iestatīšana
description: Vienotās eiro maksājumu zonas (Single Euro Payment Area — SEPA) tiešais debets kreditoram ļauj iekasēt līdzekļus no debitora bankas konta ar nosacījumu, ka debitors kreditoram ir piešķīris parakstītu mandātu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6ee3861e967246e79b072aaa69f2be02db9231b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995497"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="5dbb1-103">SEPA tiešā debeta pilnvarojuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5dbb1-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dbb1-104">Vienotās eiro maksājumu zonas (Single Euro Payment Area — SEPA) tiešais debets kreditoram ļauj iekasēt līdzekļus no debitora bankas konta ar nosacījumu, ka debitors kreditoram ir piešķīris parakstītu mandātu.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="5dbb1-105">Debitora parakstītais mandāts pilnvaro kreditoru iekasēt maksājumu un klienta bankai sniedz norādījumus par iekasējamās summas izmaksāšanu.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="5dbb1-106">Šī tēma ir sakārtota, lai parādītu SEPA tiešā debeta mandātu iestatīšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5dbb1-107">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="5dbb1-107">Prerequisites</span></span>
<span data-ttu-id="5dbb1-108">Tālāk esošajā tabulā ir norādīti priekšnoteikumi, kas ir jāizpilda pirms darba sākšanas.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="5dbb1-109">Kategorija</span><span class="sxs-lookup"><span data-stu-id="5dbb1-109">Category</span></span>       | <span data-ttu-id="5dbb1-110">Priekšnosacījums</span><span class="sxs-lookup"><span data-stu-id="5dbb1-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dbb1-111">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="5dbb1-111">Country/region</span></span> | <span data-ttu-id="5dbb1-112">Juridiskās personas primārajai adresei ir jābūt šādās valstīs/reģionos: Austrija, Beļģija, Vācija, Spānija, Francija, Itālija vai Nīderlande.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="5dbb1-113">Numuru sērijas iestatīšana tiešā debeta mandātiem Katram tiešā debeta mandātam ir nepieciešams unikāls numurs.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="5dbb1-114">Lai tiešā debeta mandātiem izveidotu numuru sēriju, izmantojiet lapu **Numuru sērijas**.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="5dbb1-115">Šis identifikators ir jāizmanto, lai tiešā debeta mandātu sistēmai piešķirtu numuru sēriju lapā **Debitoru moduļa parametri**.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="5dbb1-116">Debitoru parādu parametru iestatīšana tiešā debeta mandātiem Lai iestatītu parametrus tiešā debeta mandātiem, izmantojiet lapu **Debitoru moduļa parametri**.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="5dbb1-117">Lai iestatītu parametrus, cilnē **Tiešais debets** pēc nepieciešamības mainiet noklusējuma parametrus.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="5dbb1-118">Pēc tam cilnē **Numuru sērijas** lauku **Tiešā debeta mandāta ID** atjauniniet ar iepriekš iestatīto numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="5dbb1-119">Maksājumu metodes iestatīšana tiešā debeta mandātiem Jums jāiestata maksāšanas metode tiešā debeta mandātiem.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="5dbb1-120">Šo maksāšanas metodi jūs izmantojat, lai veidotu vaicājumus par rēķiniem, kam izveidot tiešā debeta maksājumus.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="5dbb1-121">Lai iestatītu maksāšanas metodi, izmantojiet lapu **Maksāšanas metodes**.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="5dbb1-122">Lai iestatītu maksāšanas metodi tiešā debeta mandātiem, jums ir jāizpilda šādas papildu darbības maksāšanas metodei:</span><span class="sxs-lookup"><span data-stu-id="5dbb1-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="5dbb1-123">Laukā **Maksājuma tips** atlasiet **Elektronisks maksājums**.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="5dbb1-124">Neobligāti: ja plānojat, ka katram klientam būs vairāki mandāti, laukā **Periods** atlasiet vienumu **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="5dbb1-125">Katram rēķinam tiks izveidots atsevišķs maksājums, un katrs maksājums izmantos mandātu, kas ir norādīts rēķinam.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="5dbb1-126">Atlasiet opciju **Pieprasīt mandātu**, lai izveidotu maksājumus, izmantojot tiešā debeta mandātus.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="5dbb1-127">Opcija **Pieprasīt mandātu** ir pieejama tikai tad, ja laukā **Maksājuma tips** atlasāt vērtību **Elektronisks maksājums**.</span><span class="sxs-lookup"><span data-stu-id="5dbb1-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="5dbb1-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5dbb1-128">Additional resources</span></span>

[<span data-ttu-id="5dbb1-129">SEPA tiešā debeta apskats</span><span class="sxs-lookup"><span data-stu-id="5dbb1-129">SEPA direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="5dbb1-130">Tiešā debeta pilnvarojuma izveide debitoram</span><span class="sxs-lookup"><span data-stu-id="5dbb1-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 

