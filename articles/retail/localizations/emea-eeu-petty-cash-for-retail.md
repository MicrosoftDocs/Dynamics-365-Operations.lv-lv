---
title: "Mazo kases posteņu pārvaldība programmai Retail Austrumeiropā"
description: "Šajā tēmā ir aprakstīts, kā iestatīt un izmantot kases pārvaldības līdzekļus programmā Retail Austrumeiropā."
author: epopov
manager: annbe
ms.date: 10/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 01239f0eff3e59f62188fca64f99e93be843d2e2
ms.openlocfilehash: c198cedba9268229dc1057711d9f16ca33acebac
ms.contentlocale: lv-lv
ms.lasthandoff: 10/24/2018

---

# <a name="petty-cash-management-for-retail-for-eastern-europe"></a><span data-ttu-id="70a7b-103">Mazo kases posteņu pārvaldība programmai Retail Austrumeiropā</span><span class="sxs-lookup"><span data-stu-id="70a7b-103">Petty cash management for Retail for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70a7b-104">Šajā rakstā ir informācija par mazumtirdzniecības nozarei raksturīgo Austrumeiropas lokalizāciju.</span><span class="sxs-lookup"><span data-stu-id="70a7b-104">This article contains information about Eastern European localization specific for the Retail industry.</span></span> 

<span data-ttu-id="70a7b-105">Atbilstoši Austrumeiropas valstu grāmatvedības prasībām ir iespējams iestatīt operācijas skaidras naudas kontiem, lai automatizētu procesus ieņēmumiem, skaidras naudas dokumentiem un skaidras naudas pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="70a7b-105">In accordance with the Eastern Europe accounting requirements, you can set up operations for cash accounts to automate the processes for receipts, cash documents and cash reports.</span></span> <span data-ttu-id="70a7b-106">Plašāku informāciju skatiet šeit: [(EEUR) Parametru iestatīšana kases pārvaldībai](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span><span class="sxs-lookup"><span data-stu-id="70a7b-106">For more information, go to [(EEUR) Set up parameters for cash management](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span></span> 

<span data-ttu-id="70a7b-107">Mazumtirgotāji var pieņemt dažāda veida maksājumus apmaiņā pret pārdotajām precēm un pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="70a7b-107">Retailers can accept various types of payment in exchange for the products and services that they sell.</span></span> <span data-ttu-id="70a7b-108">Kaut gan skaidra nauda ir visizplatītākais maksājumu veids, mazumtirgotāji var arī saņemt maksājumus čeku, karšu vai dokumentu formā.</span><span class="sxs-lookup"><span data-stu-id="70a7b-108">Although cash is the most common form of payment, retailers can also receive payment in the form of checks, cards, or vouchers.</span></span> <span data-ttu-id="70a7b-109">Mazumtirdzniecības punktā (POS), skaidra nauda, kredītkaršu kvītis un citi maksājumi tiek apstrādāti, izmantojot kasi.</span><span class="sxs-lookup"><span data-stu-id="70a7b-109">In Retail point of sale (POS), cash, credit card receipts, and other payments are processed through a cash office.</span></span>

<span data-ttu-id="70a7b-110">To var izdarīt, programmā Retail izmantojot līdzekli Kases pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="70a7b-110">You can do the following by using Cash management in Retail:</span></span>

- <span data-ttu-id="70a7b-111">Izveidojiet kases kontu katra mazumtirdzniecības veikala atlasītajai maksāšanas metodei.</span><span class="sxs-lookup"><span data-stu-id="70a7b-111">Create a cash account for the selected payment method for each retail store.</span></span>
- <span data-ttu-id="70a7b-112">Lai grāmatotu skaidras naudas transakcijas un debitoru maksājumus, kas tiek saņemti mazumtirdzniecības POS, izmantojiet kases žurnālus.</span><span class="sxs-lookup"><span data-stu-id="70a7b-112">Use cash journals to post cash transactions and customer payments that are received at a retail POS.</span></span>
- <span data-ttu-id="70a7b-113">Kad grāmatojat mazumtirdzniecības pārskatu, apkopojiet transakcijas pārskata rindā.</span><span class="sxs-lookup"><span data-stu-id="70a7b-113">Aggregate transactions in a statement line when you post a retail statement.</span></span> <span data-ttu-id="70a7b-114">Varat apkopot noguldījumus seifā, noguldījumus bankā, dokumentu transakcijas, noņemt norēķinu darījumus, mainīgo ierakstu transakcijas, ienākumu transakcijas, izdevumu transakcijas, debitoru maksājumus, pārdošanas transakcijas un atgriešanas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="70a7b-114">You can aggregate safe drops, bank drops, voucher transactions, remove tender transactions, float entry transactions, income transactions, expense transactions, customer payments, sales transactions, and return transactions.</span></span>

<span data-ttu-id="70a7b-115">Visas transakcijas, kas notiek Retail POS tiek grāmatotas, izmantojot Virsgrāmatas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="70a7b-115">All transactions that take place in Retail POS are posted using a ledger journal.</span></span> <span data-ttu-id="70a7b-116">Pārskatu izveidei un grāmatošanai var izmantot skaidras naudas maksājumu žurnālus, debitoru maksājumu žurnālus un Virsgrāmatas žurnālus.</span><span class="sxs-lookup"><span data-stu-id="70a7b-116">You can use cash payment journals, customer payment journals, and general journals to create and post the statements.</span></span> <span data-ttu-id="70a7b-117">Plašāku informāciju skatiet šeit: [Mazumtirdzniecības veikala izrakstu izveidošana, aprēķināšana un grāmatošana](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span><span class="sxs-lookup"><span data-stu-id="70a7b-117">For more information, go to [Create, calculate, and post statements for a retail store](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span></span>

<span data-ttu-id="70a7b-118">Lapā **Grāmatotie izraksti**, darbību rūtī varat izpildīt tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="70a7b-118">On the **Posted statements** page, on the Action Pane, you can do the following:</span></span>
  - <span data-ttu-id="70a7b-119">Dodieties uz **Uzziņas > Žurnāls maksājumiem skaidrā naudā**, lai piekļūtu ar šo izrakstu saistītajiem skaidras naudas maksājumu žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="70a7b-119">Go to **Inquiries > Cash payment journal** to access the cash payment journals that are related to the statement.</span></span>
  - <span data-ttu-id="70a7b-120">Dodieties uz **Uzziņas > Vispārējs žurnāls**, lai piekļūtu ar šo izrakstu saistītajiem virsgrāmatas žurnāliem, kas nav debitoru maksājumu un skaidras naudas maksājumu žurnāli.</span><span class="sxs-lookup"><span data-stu-id="70a7b-120">Go to **Inquiries > General journal** to access the ledger journals that are related to the statement, other than customer payments and cash payments.</span></span>

## <a name="set-up-for-cash-management-for-retail-pos"></a><span data-ttu-id="70a7b-121">Retail POS kases pārvaldības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="70a7b-121">Set up for cash management for Retail POS</span></span>

<span data-ttu-id="70a7b-122">Pirms Retail kases pārvaldības izmantošanas ir jāveic tālāk aprakstītā iestatīšanas procedūra.</span><span class="sxs-lookup"><span data-stu-id="70a7b-122">You must complete the following setup procedure before you use cash management in Retail:</span></span>
- <span data-ttu-id="70a7b-123">Lapā **Maksāšanas metodes** iestatiet maksāšanas metodi katram mazumtirgotāja akceptētajam maksājuma tipam.</span><span class="sxs-lookup"><span data-stu-id="70a7b-123">Set up a payment method for each payment type that the retailer accepts on the **Payment methods** page.</span></span> <span data-ttu-id="70a7b-124">Transakciju grāmatošanai programmā Retail POS varat izmantot dažādas maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="70a7b-124">You can use different payment methods for posting transactions in Retail POS.</span></span> <span data-ttu-id="70a7b-125">Plašāku informāciju par maksāšanas metodēm programmā Retail skatiet šeit: [Maksāšanas metodes](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/payment-methods).</span><span class="sxs-lookup"><span data-stu-id="70a7b-125">For more information about payment methods in Retail, see [Payment methods](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/payment-methods).</span></span>

- <span data-ttu-id="70a7b-126">Iestatiet mazumtirdzniecības parametrus skaidras naudas operācijām.</span><span class="sxs-lookup"><span data-stu-id="70a7b-126">Set up retail parameters for cash operations.</span></span>

- <span data-ttu-id="70a7b-127">Iestatiet maksāšanas metodi maksājumiem skaidrā naudā mazumtirdzniecības veikalā.</span><span class="sxs-lookup"><span data-stu-id="70a7b-127">Set up a payment method for cash payments in a retail store.</span></span>

### <a name="set-up-retail-parameters-for-cash-operations"></a><span data-ttu-id="70a7b-128">Mazumtirdzniecības parametru iestatīšana skaidras naudas operācijām</span><span class="sxs-lookup"><span data-stu-id="70a7b-128">Set up retail parameters for cash operations</span></span>

<span data-ttu-id="70a7b-129">Varat iestatīt parametrus, lai mazumtirdzniecībai izveidotu un grāmatotu skaidras naudas darījumus.</span><span class="sxs-lookup"><span data-stu-id="70a7b-129">You can set up parameters to create and post cash transactions in Retail.</span></span> <span data-ttu-id="70a7b-130">Lai programmā Retail POS grāmatotu pārdošanas transakcijas un maksājumu transakcijas, varat izmantot skaidras naudas maksājumu žurnālus, debitoru maksājumu žurnālus vai vispārējus žurnālus.</span><span class="sxs-lookup"><span data-stu-id="70a7b-130">You can use cash payment journals, customer payment journals, or general journals to post sales transactions and payment transactions in the Retail POS.</span></span> <span data-ttu-id="70a7b-131">Kad grāmatojat pārskatu, varat apkopot darījumus, kuriem ir vienādi rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="70a7b-131">You can aggregate transactions that have the same properties when you post a statement.</span></span> 

1. <span data-ttu-id="70a7b-132">Dodieties uz **Retail > Headquarters iestatīšana > Parametri > Mazumtirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="70a7b-132">Go to **Retail > Headquarters setup > Parameters > Retail parameters**.</span></span> <span data-ttu-id="70a7b-133">Kreisajā rūtī noklikšķiniet uz **Grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="70a7b-133">In the left pane, click **Posting**</span></span>

2. <span data-ttu-id="70a7b-134">Apgabalā **Grāmatošana**, kopsavilkuma cilnē **Apkopojums** vienumu **Norēķinu noņemšana/mainīšana** iestatiet uz **Jā**, lai apkopotu norēķinu noņemšanas vai maiņas transakcijas, kuras izraksta grāmatošanas laikā ir saistītas ar izraksta rindu.</span><span class="sxs-lookup"><span data-stu-id="70a7b-134">In the **Posting** area, on the **Aggregation** FastTab, set **Tender remove/float** to **Yes** to aggregate the remove tender transactions or float entry transactions that are associated with a statement line when you post the statement.</span></span> <span data-ttu-id="70a7b-135">Norēķinu darījuma noņemšana tiek izveidota, kad no POS naudas kastes izņemat skaidru naudu.</span><span class="sxs-lookup"><span data-stu-id="70a7b-135">A remove tender transaction is created when you withdraw cash from the POS cash drawer.</span></span> <span data-ttu-id="70a7b-136">Mainīgo ierakstu darījums tiek izveidots, kad POS naudas kastē ieliekat skaidru naudu.</span><span class="sxs-lookup"><span data-stu-id="70a7b-136">A float entry transaction is created when you deposit cash in the POS cash drawer.</span></span>

3. <span data-ttu-id="70a7b-137">Aktivizējiet tālāk uzskaitītos atsevišķos parametrus, lai apkopotu transakcijas, kuras izraksta grāmatošanas laikā ir saistītas ar izraksta rindu.</span><span class="sxs-lookup"><span data-stu-id="70a7b-137">Activate the individual parameters listed below to aggregate the transactions that are associated with a statement line when you post the statement:</span></span>
   - <span data-ttu-id="70a7b-138">**Noguldījums bankā** — apkopot bankas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="70a7b-138">**Bank drop** – Aggregate bank transactions.</span></span>
   - <span data-ttu-id="70a7b-139">**Noguldījums seifā** — apkopot seifa transakcijas.</span><span class="sxs-lookup"><span data-stu-id="70a7b-139">**Safe drop** – Aggregate safe transactions.</span></span>
   - <span data-ttu-id="70a7b-140">**Ieņēmumu/izdevumu transakcijas** — apkopot ienākumu transakcijas vai izdevumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="70a7b-140">**Income/Expense transactions** – Aggregate income transactions or expense transactions.</span></span>
   - <span data-ttu-id="70a7b-141">**Dokumentu transakcijas** — apkopot dokumentu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="70a7b-141">**Voucher transactions** – Aggregate voucher transactions.</span></span>
   - <span data-ttu-id="70a7b-142">**Debitoru maksājumi** — apkopot debitoru maksājumus.</span><span class="sxs-lookup"><span data-stu-id="70a7b-142">**Customer payments** – Aggregate customer payments.</span></span>
   - <span data-ttu-id="70a7b-143">**Pārdošana un ieņēmumi** — apkopot pārdošanas un ieņēmumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="70a7b-143">**Sales and returns** – Aggregate sales and returns transactions.</span></span>

4. <span data-ttu-id="70a7b-144">Kopsavilkuma cilnē **Maksājumi** atlasiet noklusējuma žurnāla nosaukumu tālāk norādītajām opcijām.</span><span class="sxs-lookup"><span data-stu-id="70a7b-144">On the **Payments** FastTab, select a default journal name for the following options:</span></span>
     - <span data-ttu-id="70a7b-145">**Debitoru maksājumu žurnāls** — šis žurnāls tiek izmantots debitoru maksājumu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="70a7b-145">**Customer payment journal** – This journal is used to post customer payments.</span></span>
     - <span data-ttu-id="70a7b-146">**Žurnāls maksājumiem skaidrā naudā** — šis žurnāls tiek izmantots skaidras naudas maksājumu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="70a7b-146">**Cash payment journal** – This journal is used to post cash payments.</span></span>
     - <span data-ttu-id="70a7b-147">**Vispārējs žurnāls** — šis žurnāls tiek izmantots, lai grāmatotu transakcijas, kas nav maksājumi skaidrā naudā un nav debitoru maksājumi.</span><span class="sxs-lookup"><span data-stu-id="70a7b-147">**General journal** – This journal is used to post transactions other than cash payments and customer payments.</span></span>

### <a name="set-up-a-payment-method-for-cash-payments-in-a-retail-store"></a><span data-ttu-id="70a7b-148">Maksāšanas metodes iestatīšana skaidras naudas maksājumiem mazumtirdzniecības veikalā</span><span class="sxs-lookup"><span data-stu-id="70a7b-148">Set up a payment method for cash payments in a retail store</span></span>

<span data-ttu-id="70a7b-149">Izmantojiet šādu procedūru, lai iestatītu maksājuma metodi maksājumiem skaidrā naudā mazumtirdzniecības veikalā.</span><span class="sxs-lookup"><span data-stu-id="70a7b-149">Use the following procedure to set up a payment method for cash payments in a retail store.</span></span>

1. <span data-ttu-id="70a7b-150">Dodieties uz **Retail > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali**.</span><span class="sxs-lookup"><span data-stu-id="70a7b-150">Go to **Retail > Channels > Retail stores > All retail stores**.</span></span>

2. <span data-ttu-id="70a7b-151">Sarakstu lapā **Visi mazumtirdzniecības veikali** atlasiet veikalu, kam iestatīt maksāšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="70a7b-151">On the **All retail stores** list page, select the store to set up a payment method for.</span></span>

3. <span data-ttu-id="70a7b-152">Darbību rūts cilnes **Iestatīt** grupā **Iestatīt** noklikšķiniet uz **Maksāšanas metodes**.</span><span class="sxs-lookup"><span data-stu-id="70a7b-152">On the Action Pane, on the **Set up** tab, in the **Set up** group, click **Payment methods**.</span></span>

4. <span data-ttu-id="70a7b-153">Lapā **Maksāšanas metode** izveidojiet vai atlasiet kādu maksāšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="70a7b-153">On the **Payment method** page, create or select a payment method.</span></span> 

5. <span data-ttu-id="70a7b-154">Kopsavilkuma cilnes **Grāmatošana** lauku grupā **Konts**, laukā **Konta tips** atlasiet **Kases konts**.</span><span class="sxs-lookup"><span data-stu-id="70a7b-154">On the **Posting** FastTab, in the **Account** field group, in the **Account type** field, select **Cash account**.</span></span>

   > [!NOTE]
    > <span data-ttu-id="70a7b-155">Vienumu **Kases konts** laukā **Konta tips** varat atlasīt tikai tad, ja laukā **Funkcija** ir atlasīta vērtība **Parasts** vai **Norēķinu noņemšana/mainīšana**.</span><span class="sxs-lookup"><span data-stu-id="70a7b-155">You can select **Cash account** in the **Account type** field only if you select **Normal** or **Tender remove/float** in the **Function** field.</span></span>

6. <span data-ttu-id="70a7b-156">Laukā **Konta numurs** atlasiet kādu kases konta numuru šai maksāšanas metodei.</span><span class="sxs-lookup"><span data-stu-id="70a7b-156">In the **Account number** field, select a cash account number for the payment method.</span></span>

7. <span data-ttu-id="70a7b-157">Lauku grupas **Norēķinu noņemšana/mainīšana** laukā **Korespondējošais konts** atlasiet korespondējošo kontu, kur grāmatot norēķinu noņemšanas vai mainīšanas transakcijas šai maksāšanas metodei.</span><span class="sxs-lookup"><span data-stu-id="70a7b-157">In the **Tender remove/float** field group, in the **Offset account** field, select the offset account to post remove tender or float entry transactions for the payment method.</span></span>

> [!NOTE]
> <span data-ttu-id="70a7b-158">Korespondējošie konti veikalam ir jāiestata gan kases norēķinu maksāšanas metodei, gan norēķinu noņemšanas vai mainīšanas ierakstu maksāšanas metodei.</span><span class="sxs-lookup"><span data-stu-id="70a7b-158">You must set up offset accounts for both the cash tender payment method and the remove tender or float entry payment method for a store.</span></span> <span data-ttu-id="70a7b-159">Šādi norēķinu noņemšanas vai mainīšanas ierakstu transakcijām tiek izveidoti līdzsvaroti virsgrāmatas ieraksti.</span><span class="sxs-lookup"><span data-stu-id="70a7b-159">This creates balanced general ledger entries for remove tender or float entry transactions.</span></span>

