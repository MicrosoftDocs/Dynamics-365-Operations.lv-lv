---
title: Atgādinājuma vēstuļu apstrādes piemērs
description: Šajā tēmā aplūkots piemērs, kas parāda atgādinājuma vēstuļu izveides, drukāšanas un grāmatošanas procesu.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: fb2651644efd2cadfccb91e48c34dfddc8383e1f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021420"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="4d2f5-103">Atgādinājuma vēstuļu apstrādes piemērs</span><span class="sxs-lookup"><span data-stu-id="4d2f5-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d2f5-104">Šajā tēmā aplūkots piemērs, kas parāda atgādinājuma vēstuļu izveides, drukāšanas un grāmatošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="4d2f5-105">Piemērs ir pamatots uz opciju **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** sadaļā Kredīts un iekasēšana.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="4d2f5-106">Tas izmanto datus USMF demonstrācijas uzņēmumā un jaunu debitoru — US-045.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="4d2f5-107">Lai sāktu, pārejiet uz sadaļu **Debitoru parādi \> Debitori \> Visi debitori**, atlasiet **Jauns** un pēc tam ievadiet nepieciešamo informāciju, lai izveidotu debitoru US-045.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="4d2f5-108">Kad esat pabeidzis, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="4d2f5-109">Pārejiet uz sadaļu **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Iestatīt atgādinājuma vēstuļu secību** un iestatiet atgādinājuma vēstuļu secību, kā parādīts tabulā zemāk, kas ir piešķirta debitora grāmatošanas profilam.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="4d2f5-110">Atgādinājuma vēstules kods</span><span class="sxs-lookup"><span data-stu-id="4d2f5-110">Collection   letter code</span></span>      |     <span data-ttu-id="4d2f5-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4d2f5-111">Description</span></span>                           |     <span data-ttu-id="4d2f5-112">Valūta</span><span class="sxs-lookup"><span data-stu-id="4d2f5-112">Currency</span></span>      |     <span data-ttu-id="4d2f5-113">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="4d2f5-113">Main   account</span></span>        |     <span data-ttu-id="4d2f5-114">Papildmaksa valūtā</span><span class="sxs-lookup"><span data-stu-id="4d2f5-114">Fee   in currency</span></span>     |     <span data-ttu-id="4d2f5-115">Minimālais nokavētais</span><span class="sxs-lookup"><span data-stu-id="4d2f5-115">Minimum   over</span></span>        |     <span data-ttu-id="4d2f5-116">Dienu bloķēšana</span><span class="sxs-lookup"><span data-stu-id="4d2f5-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="4d2f5-117">Atgādinājuma vēstule Nr. 1</span><span class="sxs-lookup"><span data-stu-id="4d2f5-117">Collection   letter 1</span></span>         |     <span data-ttu-id="4d2f5-118">Otrais paziņojums ar papildu maksu</span><span class="sxs-lookup"><span data-stu-id="4d2f5-118">Second   notification with fee</span></span>        |     <span data-ttu-id="4d2f5-119">USD</span><span class="sxs-lookup"><span data-stu-id="4d2f5-119">USD</span></span>           |                           |     <span data-ttu-id="4d2f5-120">0.00</span><span class="sxs-lookup"><span data-stu-id="4d2f5-120">0.00</span></span>                  |     <span data-ttu-id="4d2f5-121">0.00</span><span class="sxs-lookup"><span data-stu-id="4d2f5-121">0.00</span></span>                  |     <span data-ttu-id="4d2f5-122">2</span><span class="sxs-lookup"><span data-stu-id="4d2f5-122">2</span></span>                 |
|     <span data-ttu-id="4d2f5-123">Atgādinājuma vēstule Nr. 2</span><span class="sxs-lookup"><span data-stu-id="4d2f5-123">Collection   letter 2</span></span>         |     <span data-ttu-id="4d2f5-124">Otrais paziņojums ar papildu maksu</span><span class="sxs-lookup"><span data-stu-id="4d2f5-124">Second   notification with fee</span></span>        |     <span data-ttu-id="4d2f5-125">USC</span><span class="sxs-lookup"><span data-stu-id="4d2f5-125">USC</span></span>           |     <span data-ttu-id="4d2f5-126">403150</span><span class="sxs-lookup"><span data-stu-id="4d2f5-126">403150</span></span>                |     <span data-ttu-id="4d2f5-127">20.00</span><span class="sxs-lookup"><span data-stu-id="4d2f5-127">20.00</span></span>                 |     <span data-ttu-id="4d2f5-128">10,00</span><span class="sxs-lookup"><span data-stu-id="4d2f5-128">10.00</span></span>                 |     <span data-ttu-id="4d2f5-129">3</span><span class="sxs-lookup"><span data-stu-id="4d2f5-129">3</span></span>                 |
|     <span data-ttu-id="4d2f5-130">Iekasēšana</span><span class="sxs-lookup"><span data-stu-id="4d2f5-130">Collection</span></span>                    |     <span data-ttu-id="4d2f5-131">Galīgais paziņojums ar papildu maksu</span><span class="sxs-lookup"><span data-stu-id="4d2f5-131">Final   notification with fee</span></span>         |     <span data-ttu-id="4d2f5-132">USD</span><span class="sxs-lookup"><span data-stu-id="4d2f5-132">USD</span></span>           |     <span data-ttu-id="4d2f5-133">403150</span><span class="sxs-lookup"><span data-stu-id="4d2f5-133">403150</span></span>                |     <span data-ttu-id="4d2f5-134">50.00</span><span class="sxs-lookup"><span data-stu-id="4d2f5-134">50.00</span></span>                 |     <span data-ttu-id="4d2f5-135">100.00</span><span class="sxs-lookup"><span data-stu-id="4d2f5-135">100.00</span></span>                |     <span data-ttu-id="4d2f5-136">15</span><span class="sxs-lookup"><span data-stu-id="4d2f5-136">15</span></span>                |

<span data-ttu-id="4d2f5-137">Ilustrācijā zemāk ir parādīta tabulā esošā informācija tā, kā tā būtu redzama lapā **Atgādinājuma vēstules**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="4d2f5-138">[![Atgādinājuma vēstuļu secības iestatīšana](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="4d2f5-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="4d2f5-139">Tagad jāiestata divi parametri, kas nepieciešami šim piemēram.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="4d2f5-140">Pārejiet uz sadaļu **Kredīts un iekasēšana \> Iestatījumi \> Debitoru parādu parametri** un izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="4d2f5-141">Cilnē **Iekasēšana** iestatiet opciju **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="4d2f5-142">Pārliecinieties, vai lauks **Izveidot atgādinājuma vēstuli katram** ir iestatīts uz **Debitors**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="4d2f5-143">[![Debitoru parādu parametru iestatīšana kredīta iekasēšanai](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="4d2f5-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="4d2f5-144">Pārejiet uz sadaļu **Debitoru parādi \> Rēķini \> Visi brīva teksta rēķini**, atlasiet **Jauns** un pēc tam izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="4d2f5-145">Laukā **Debitora konts** atlasiet **US-045**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="4d2f5-146">Laukā **Rēķina datums** ievadiet **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="4d2f5-147">Laukā **Apmaksas datums** ievadiet **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="4d2f5-148">Kopsavilkuma cilnes **Rēķina rindas** laukā **Galvenais konts** ievadiet **401100**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="4d2f5-149">Laukā **Vienības cena** ievadiet **500.00**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="4d2f5-150">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-150">Select **Post**.</span></span>

    <span data-ttu-id="4d2f5-151">Tagad jāievada divas debitora kredīta notas.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="4d2f5-152">Atlasiet **Jauns**, tad veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="4d2f5-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="4d2f5-153">Laukā **Debitora konts** atlasiet **US-045**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="4d2f5-154">Laukā **Rēķina datums** ievadiet **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="4d2f5-155">Laukā **Apmaksas datums** ievadiet **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="4d2f5-156">Kopsavilkuma cilnes **Rēķina rindas** laukā **Galvenais konts** ievadiet **401100**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="4d2f5-157">Laukā **Vienības cena** ievadiet **-100,00**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="4d2f5-158">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-158">Select **Post**.</span></span>

5. <span data-ttu-id="4d2f5-159">Atkārtojiet 4. darbību, bet ievadiet **-200,00** laukā **Vienības cena**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="4d2f5-160">Pārejiet uz **Debitoru parādi \> Debitori \> Visi debitori** un atlasiet debitoru **US-045**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="4d2f5-161">Pēc tam Darbību rūtī atlasiet **Darījumi \> Darījumi**, lai pārskatītu debitora darbības, ko iepriekš iegrāmatojāt.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="4d2f5-162">[![Grāmatoto debitoru darījumu pārskatīšana](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="4d2f5-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="4d2f5-163">Tagad jāizveido atgādinājuma vēstules debitoram US-045.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="4d2f5-164">Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Izveidot atgādinājuma vēstules** un izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="4d2f5-165">Iestatiet opcijas **Rēķins** un **Kredīta nota** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="4d2f5-166">Pēc noklusējuma laukam **Atgādinājuma vēstules** jābūt iestatītam uz **Atgādinājums katram debitoram**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="4d2f5-167">Laukā **Atgādinājuma vēstules datums** ievadiet **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="4d2f5-168">Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrēt** un pēc tam laukā **Debitora konts** pievienojiet debitoru **US-045**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="4d2f5-169">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-169">Select **OK**.</span></span>
    5. <span data-ttu-id="4d2f5-170">Atlasiet **Labi**, lai izveidotu atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="4d2f5-171">Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Pārskatīt un apstrādāt atgādinājuma vēstules** un izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="4d2f5-172">Ņemiet vērā, ka atgādinājuma vēstules kods gan virsrakstā, gan darbības rindās ir **1. atgādinājuma vēstule**, jo šī atgādinājuma vēstule secībā ir pirmā atgādinājuma vēstule.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="4d2f5-173">(Lai skatītu darbību rindas, iespējams, būs jāatlasa kopsavilkuma cilne **Darījumi**.)</span><span class="sxs-lookup"><span data-stu-id="4d2f5-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="4d2f5-174">[![Pārbaude, vai galvenē un rindās ir viens un tas pats atgādinājuma vēstules kods](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="4d2f5-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="4d2f5-175">Darbību rūtī atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="4d2f5-176">Laukā **Grāmatošanas datums** ievadiet **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="4d2f5-177">Tagad vēlreiz jāizveido atgādinājuma vēstules debitoram US-045.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="4d2f5-178">Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Izveidot atgādinājuma vēstules** un izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="4d2f5-179">Iestatiet opcijas **Rēķins** un **Kredīta nota** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="4d2f5-180">Pēc noklusējuma laukam **Atgādinājuma vēstules** jābūt iestatītam uz **Atgādinājums katram debitoram**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="4d2f5-181">Laukā **Atgādinājuma vēstules datums** ievadiet **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="4d2f5-182">Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrēt** un pēc tam laukā **Debitora konts** pievienojiet debitoru **US-045**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="4d2f5-183">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-183">Select **OK**.</span></span>
    5. <span data-ttu-id="4d2f5-184">Atlasiet **Labi**, lai izveidotu atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="4d2f5-185">Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Pārskatīt un apstrādāt atgādinājuma vēstules** un izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="4d2f5-186">Ņemiet vērā, ka atgādinājuma vēstules kods galvenē ir **1. atgādinājuma vēstule**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="4d2f5-187">Tomēr kods darījuma rindās ir **2. atgādinājuma vēstule**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="4d2f5-188">[![Pārbaude, vai galvenē un rindās ir dažādi atgādinājuma vēstules kodi](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="4d2f5-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="4d2f5-189">Kodi atšķiras, jo opcija **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** ir iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="4d2f5-190">Negrāmatojiet šo atgādinājuma vēstuli.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="4d2f5-191">Pārejiet uz sadaļu **Kredīts un iekasēšana \> Iestatīšana \> Debitoru parādu parametri** un pēc tam cilnē **Atgādinājumi** iestatiet opciju **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="4d2f5-192">[![Opcijas Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu, iestatīšana uz Nē](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="4d2f5-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="4d2f5-193">Tagad vēlreiz jāizveido atgādinājuma vēstules debitoram US-045.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="4d2f5-194">Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Izveidot atgādinājuma vēstules** un izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="4d2f5-195">Iestatiet opcijas **Rēķins** un **Kredīta nota** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="4d2f5-196">Pēc noklusējuma laukam **Atgādinājuma vēstules** jābūt iestatītam uz **Atgādinājums katram debitoram**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="4d2f5-197">Laukā **Atgādinājuma vēstules datums** ievadiet **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="4d2f5-198">Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrēt** un pēc tam laukā **Debitora konts** pievienojiet debitoru **US-045**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="4d2f5-199">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-199">Select **OK**.</span></span>
    5. <span data-ttu-id="4d2f5-200">Atlasiet **Labi**, lai izveidotu atgādinājuma vēstules.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="4d2f5-201">Pārejiet uz sadaļu **Kredīts un ieksēšana \> Atgādinājuma vēstule \> Pārskatīt un apstrādāt atgādinājuma vēstules** un ņemiet vērā, ka atgādinājuma vēstules kods gan virsrakstā, gan darbības rindās ir **2. atgādinājuma vēstule**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="4d2f5-202">[![Parādīšana vēlreiz, ka galvenē un rindās ir viens un tas pats atgādinājuma vēstules kods](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="4d2f5-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="4d2f5-203">Viens un tas pats kods parādās abās vietās, jo opcija **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** tagad ir iestatīta uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="4d2f5-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
