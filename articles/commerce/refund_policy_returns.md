---
title: Izveidot un atjaunināt kanāla atgriešanas un atmaksas politiku
description: Šajā tēmā izskaidrots, kā iestatīt atgriešanas un atmaksas politiku kanālam.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 03e46a7f8d110bd9ef3b353b150116bbf8a70ad5
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478120"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="b1193-103">Izveidot un atjaunināt kanāla atgriešanas un atmaksas politiku</span><span class="sxs-lookup"><span data-stu-id="b1193-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b1193-104">Kanāla atgriešanas politika Dynamics 365 Commerce ļauj mazumtirgotājiem iestatīt izpildi attiecībā uz to, kurus maksājumu norēķinus var izmantot atgriešanas apstrādei pārdošanas punkta (POS) ierīcē.</span><span class="sxs-lookup"><span data-stu-id="b1193-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="b1193-105">Šajā tēmā izskaidrotas darbības, kā iestatīt atgriešanas un atmaksas politiku kanālam.</span><span class="sxs-lookup"><span data-stu-id="b1193-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="b1193-106">Politikas darbības sfēra pašlaik ir ierobežota, nosakot maksājuma norēķinus, ko var atļaut kanālam.</span><span class="sxs-lookup"><span data-stu-id="b1193-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="b1193-107">"Atļauto" saraksts ir balstīts uz maksājuma metodēm, kas izmantotas, lai veiktu pirkumu.</span><span class="sxs-lookup"><span data-stu-id="b1193-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="b1193-108">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="b1193-108">For example:</span></span>

- <span data-ttu-id="b1193-109">Ja pirkums tika veikts, izmantojot dāvanu karti, veikala politika ir apstrādāt atmaksu tikai uz jaunu dāvanu karti vai sniegt veikala kredītu.</span><span class="sxs-lookup"><span data-stu-id="b1193-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="b1193-110">Ja pārdošana ir veikta, izmantojot skaidru naudu, atmaksai atļautās opcijas ir skaidra nauda, dāvanu kartes un debitora konts, taču ne kredītkarte.</span><span class="sxs-lookup"><span data-stu-id="b1193-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="b1193-111">Atgriešanas politikas iespējošana</span><span class="sxs-lookup"><span data-stu-id="b1193-111">Enable return policy</span></span>

<span data-ttu-id="b1193-112">Lai iespējotu kanāla atgriešanas politikas funkcionalitāti, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="b1193-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="b1193-113">Ejiet uz **Līdzekļu pārvaldības** darbtelpu pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b1193-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="b1193-114">Funkciju nosaukumu sarakstā meklējiet funkciju **iespējot kanāla atgriešanas politikas**.</span><span class="sxs-lookup"><span data-stu-id="b1193-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="b1193-115">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="b1193-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="b1193-116">Atgriešanas politikas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b1193-116">Configure return policy</span></span>

<span data-ttu-id="b1193-117">Veiciet šīs darbības, lai konfigurētu atgriešanas politiku mazumtirdzniecības veikalam vai tiešsaistes mazumtirdzniecības kanālam.</span><span class="sxs-lookup"><span data-stu-id="b1193-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="b1193-118">Dodieties uz **Retail un Commerce** \> **Kanāla iestatīšana** \> **Atgriešana** \> **Kanāla atgriešanas politika**.</span><span class="sxs-lookup"><span data-stu-id="b1193-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="b1193-119">Atlasiet **Jauns**, lai izveidotu atgriešanas politikas veidni.</span><span class="sxs-lookup"><span data-stu-id="b1193-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="b1193-120">Lai izmantotu esošu veidni, atlasiet veidni kreisajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="b1193-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="b1193-121">Jaunām veidnēm pievienojiet nosaukumu un aprakstu, kas palīdzēs identificēt politiku, kad tā tiek piemērota kanālam.</span><span class="sxs-lookup"><span data-stu-id="b1193-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="b1193-122">![Pievienot jaunu atgriešanas politiku](media/Return-policy-page1.png "Pievienot jaunu atgriešanas politiku")</span><span class="sxs-lookup"><span data-stu-id="b1193-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="b1193-123">Sadaļā **Atļautās atmaksas maksājumu metodes** definējiet **atļautos** atgriešanas maksājumu norēķinus, kas ir specifiski katrai maksājuma metodei.</span><span class="sxs-lookup"><span data-stu-id="b1193-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="b1193-124">![Pievienot maksāšanas metodes](media/Return-policy-page2.PNG "Iestatīt atļautās maksājuma metodes maksājuma veidam")</span><span class="sxs-lookup"><span data-stu-id="b1193-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="b1193-125">Maksāšanas metodes tiek atvasinātas no organizācijai iestatītajām maksāšanas metodēm.</span><span class="sxs-lookup"><span data-stu-id="b1193-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="b1193-126">Pievienojot atļauto atgriešanas norēķinu tipu katrai uzskaitītajai maksāšanas metodei, tiek nodrošināts, ka atgriešanu var veikt atļautajam atgriešanas norēķinu veidam.</span><span class="sxs-lookup"><span data-stu-id="b1193-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="b1193-127">Saistiet atgriešanas politikas veidni ar veikaliem, kur tā tiks izmantota.</span><span class="sxs-lookup"><span data-stu-id="b1193-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="b1193-128">Atlasiet **Pievienot** cilnē **Mazumtirdzniecības kanāli** un saistiet pieejamos kanālus.</span><span class="sxs-lookup"><span data-stu-id="b1193-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="b1193-129">Dialoglodziņā **Izvēlēties organizācijas mezglus**, atlasiet veikalus, reģionus un organizācijas, ar kurām veidne jāsaista.</span><span class="sxs-lookup"><span data-stu-id="b1193-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="b1193-130">Ar katru veikalu var saistīt tikai vienu atgriešanas politikas veidni.</span><span class="sxs-lookup"><span data-stu-id="b1193-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="b1193-131">Izmantojiet bulttaustiņus, lai atlasītu veikalus, reģionus vai organizācijas.</span><span class="sxs-lookup"><span data-stu-id="b1193-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="b1193-132">Politikas Spēkā stāšanās datumsir datums, kurā politika tiek piemērota kanāliem un tiek izpildīti kanāla darbi.</span><span class="sxs-lookup"><span data-stu-id="b1193-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="b1193-133">![Izvēlēties organizācijas zaru dialoglodziņu](media/Return-policy-page3.PNG "Izvēlēties organizācijas zaru dialoglodziņu")</span><span class="sxs-lookup"><span data-stu-id="b1193-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="b1193-134">Lapā **Sadales grafiks** palaidiet **1070** darbu, lai kanāla atgriešanas politika būtu pieejama POS.</span><span class="sxs-lookup"><span data-stu-id="b1193-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="b1193-135">Priekšskatīt kanāla atgriešanas politiku POS</span><span class="sxs-lookup"><span data-stu-id="b1193-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="b1193-136">Lai skatītu atļautos atgriešanas norēķinu tipus POS, veiciet kādā no nākamajiem piemēriem norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b1193-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="b1193-137">Piesakieties POS kā kasieris vai menedžeris.</span><span class="sxs-lookup"><span data-stu-id="b1193-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="b1193-138">Sadaļā **Maiņa un atvilktne** atlasiet **Rādīt žurnālu.**</span><span class="sxs-lookup"><span data-stu-id="b1193-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="b1193-139">Atlasiet transakciju, kas ir daļa no atgriešanas.</span><span class="sxs-lookup"><span data-stu-id="b1193-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="b1193-140">Atlasiet atgriežamos krājumus un izvēlieties maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="b1193-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="b1193-141">Ja izvēlētais maksājuma norēķins ir atļauto atgriešanas norēķinu tipu sarakstā, kasieris var pabeigt darbību.</span><span class="sxs-lookup"><span data-stu-id="b1193-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="b1193-142">Ja atlasītais maksājuma norēķins nav atļauts, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="b1193-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="b1193-143">Izvēlieties **Summa apmaksai**, lai parādītu sarakstu ar visiem atļautajiem atgriešanas norēķinu veidiem.</span><span class="sxs-lookup"><span data-stu-id="b1193-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="b1193-144">- vai -</span><span class="sxs-lookup"><span data-stu-id="b1193-144">-or-</span></span>

1. <span data-ttu-id="b1193-145">Piesakieties POS kā kasieris vai menedžeris.</span><span class="sxs-lookup"><span data-stu-id="b1193-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="b1193-146">Atlasiet **Atgriešanas transakcija** un ievadiet saņemšanas ID, izmantojot svītrkoda skenēšanu vai manuālu ievadi.</span><span class="sxs-lookup"><span data-stu-id="b1193-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="b1193-147">Atlasiet transakciju, kas ir daļa no atgriešanas.</span><span class="sxs-lookup"><span data-stu-id="b1193-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="b1193-148">Atlasiet atgriežamos krājumus un izvēlieties maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="b1193-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="b1193-149">Ja izvēlētais maksājuma norēķins ir atļauto atgriešanas norēķinu tipu sarakstā, kasieris var pabeigt darbību.</span><span class="sxs-lookup"><span data-stu-id="b1193-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="b1193-150">Ja atlasītais maksājuma norēķins nav atļauts, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="b1193-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="b1193-151">Izvēlieties **Summa apmaksai**, lai parādītu sarakstu ar visiem atļautajiem atgriešanas norēķinu veidiem.</span><span class="sxs-lookup"><span data-stu-id="b1193-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="b1193-152">![Atmaksa nav atļauta](media/Return-policy-page6.png "Atmaksas veids nav atļauts")</span><span class="sxs-lookup"><span data-stu-id="b1193-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="b1193-153">![Maksāšanas metožu saraksts](media/Return-policy-page5.PNG "Atļautie atmaksas veidi")</span><span class="sxs-lookup"><span data-stu-id="b1193-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
