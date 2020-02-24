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
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 66bb9bbd338561315f2f69ae4aff86a67513b190
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3023359"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="b0f83-103">Izveidot un atjaunināt kanāla atgriešanas un atmaksas politiku</span><span class="sxs-lookup"><span data-stu-id="b0f83-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]


## <a name="overview"></a><span data-ttu-id="b0f83-104">Pārskats</span><span class="sxs-lookup"><span data-stu-id="b0f83-104">Overview</span></span>

<span data-ttu-id="b0f83-105">Kanāla atgriešanas politika Dynamics 365 Commerce ļauj mazumtirgotājiem iestatīt izpildi attiecībā uz to, kurus maksājumu norēķinus var izmantot atgriešanas apstrādei pārdošanas punkta (POS) ierīcē.</span><span class="sxs-lookup"><span data-stu-id="b0f83-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="b0f83-106">Šajā tēmā izskaidrotas darbības, kā iestatīt atgriešanas un atmaksas politiku kanālam.</span><span class="sxs-lookup"><span data-stu-id="b0f83-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="b0f83-107">Politikas darbības sfēra pašlaik ir ierobežota, nosakot maksājuma norēķinus, ko var atļaut kanālam.</span><span class="sxs-lookup"><span data-stu-id="b0f83-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="b0f83-108">"Atļauto" saraksts ir balstīts uz maksājuma metodēm, kas izmantotas, lai veiktu pirkumu.</span><span class="sxs-lookup"><span data-stu-id="b0f83-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="b0f83-109">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="b0f83-109">For example:</span></span>

- <span data-ttu-id="b0f83-110">Ja pirkums tika veikts, izmantojot dāvanu karti, veikala politika ir apstrādāt atmaksu tikai uz jaunu dāvanu karti vai sniegt veikala kredītu.</span><span class="sxs-lookup"><span data-stu-id="b0f83-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="b0f83-111">Ja pārdošana ir veikta, izmantojot skaidru naudu, atmaksai atļautās opcijas ir skaidra nauda, dāvanu kartes un debitora konts, taču ne kredītkarte.</span><span class="sxs-lookup"><span data-stu-id="b0f83-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="b0f83-112">Atgriešanas politikas iespējošana</span><span class="sxs-lookup"><span data-stu-id="b0f83-112">Enable return policy</span></span>

<span data-ttu-id="b0f83-113">Lai iespējotu kanāla atgriešanas politikas funkcionalitāti, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="b0f83-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="b0f83-114">Ejiet uz **Līdzekļu pārvaldības** darbtelpu pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b0f83-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="b0f83-115">Funkciju nosaukumu sarakstā meklējiet funkciju **iespējot kanāla atgriešanas politikas**.</span><span class="sxs-lookup"><span data-stu-id="b0f83-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="b0f83-116">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="b0f83-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="b0f83-117">Atgriešanas politikas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b0f83-117">Configure return policy</span></span>

<span data-ttu-id="b0f83-118">Veiciet šīs darbības, lai konfigurētu atgriešanas politiku mazumtirdzniecības veikalam vai tiešsaistes mazumtirdzniecības kanālam.</span><span class="sxs-lookup"><span data-stu-id="b0f83-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="b0f83-119">Dodieties uz **Retail un Commerce** \> **Kanāla iestatīšana** \> **Atgriešana** \> **Kanāla atgriešanas politika**.</span><span class="sxs-lookup"><span data-stu-id="b0f83-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="b0f83-120">Atlasiet **Jauns**, lai izveidotu atgriešanas politikas veidni.</span><span class="sxs-lookup"><span data-stu-id="b0f83-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="b0f83-121">Lai izmantotu esošu veidni, atlasiet veidni kreisajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="b0f83-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="b0f83-122">Jaunām veidnēm pievienojiet nosaukumu un aprakstu, kas palīdzēs identificēt politiku, kad tā tiek piemērota kanālam.</span><span class="sxs-lookup"><span data-stu-id="b0f83-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="b0f83-123">![Pievienot jaunu atgriešanas politiku](media/Return-policy-page1.png "Pievienot jaunu atgriešanas politiku")</span><span class="sxs-lookup"><span data-stu-id="b0f83-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="b0f83-124">Sadaļā **Atļautās atmaksas maksājumu metodes** definējiet **atļautos** atgriešanas maksājumu norēķinus, kas ir specifiski katrai maksājuma metodei.</span><span class="sxs-lookup"><span data-stu-id="b0f83-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="b0f83-125">![Pievienot maksāšanas metodes](media/Return-policy-page2.PNG "Iestatīt atļautās maksājuma metodes maksājuma veidam")</span><span class="sxs-lookup"><span data-stu-id="b0f83-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="b0f83-126">Maksāšanas metodes tiek atvasinātas no organizācijai iestatītajām maksāšanas metodēm.</span><span class="sxs-lookup"><span data-stu-id="b0f83-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="b0f83-127">Pievienojot atļauto atgriešanas norēķinu tipu katrai uzskaitītajai maksāšanas metodei, tiek nodrošināts, ka atgriešanu var veikt atļautajam atgriešanas norēķinu veidam.</span><span class="sxs-lookup"><span data-stu-id="b0f83-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="b0f83-128">Saistiet atgriešanas politikas veidni ar veikaliem, kur tā tiks izmantota.</span><span class="sxs-lookup"><span data-stu-id="b0f83-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="b0f83-129">Atlasiet **Pievienot** cilnē **Mazumtirdzniecības kanāli** un saistiet pieejamos kanālus.</span><span class="sxs-lookup"><span data-stu-id="b0f83-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="b0f83-130">Dialoglodziņā **Izvēlēties organizācijas mezglus**, atlasiet veikalus, reģionus un organizācijas, ar kurām veidne jāsaista.</span><span class="sxs-lookup"><span data-stu-id="b0f83-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="b0f83-131">Ar katru veikalu var saistīt tikai vienu atgriešanas politikas veidni.</span><span class="sxs-lookup"><span data-stu-id="b0f83-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="b0f83-132">Izmantojiet bulttaustiņus, lai atlasītu veikalus, reģionus vai organizācijas.</span><span class="sxs-lookup"><span data-stu-id="b0f83-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="b0f83-133">Politikas Spēkā stāšanās datumsir datums, kurā politika tiek piemērota kanāliem un tiek izpildīti kanāla darbi.</span><span class="sxs-lookup"><span data-stu-id="b0f83-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="b0f83-134">![Izvēlēties organizācijas zaru dialoglodziņu](media/Return-policy-page3.PNG "Izvēlēties organizācijas zaru dialoglodziņu")</span><span class="sxs-lookup"><span data-stu-id="b0f83-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="b0f83-135">Lapā **Sadales grafiks** palaidiet **1070** darbu, lai kanāla atgriešanas politika būtu pieejama POS.</span><span class="sxs-lookup"><span data-stu-id="b0f83-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="b0f83-136">Priekšskatīt kanāla atgriešanas politiku POS</span><span class="sxs-lookup"><span data-stu-id="b0f83-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="b0f83-137">Lai skatītu atļautos atgriešanas norēķinu tipus POS, veiciet kādā no nākamajiem piemēriem norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b0f83-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="b0f83-138">Piesakieties POS kā kasieris vai menedžeris.</span><span class="sxs-lookup"><span data-stu-id="b0f83-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="b0f83-139">Sadaļā **Maiņa un atvilktne**atlasiet **Rādīt žurnālu.**</span><span class="sxs-lookup"><span data-stu-id="b0f83-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="b0f83-140">Atlasiet transakciju, kas ir daļa no atgriešanas.</span><span class="sxs-lookup"><span data-stu-id="b0f83-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="b0f83-141">Atlasiet atgriežamos krājumus un izvēlieties maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="b0f83-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="b0f83-142">Ja izvēlētais maksājuma norēķins ir atļauto atgriešanas norēķinu tipu sarakstā, kasieris var pabeigt darbību.</span><span class="sxs-lookup"><span data-stu-id="b0f83-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="b0f83-143">Ja atlasītais maksājuma norēķins nav atļauts, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="b0f83-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="b0f83-144">Izvēlieties **Summa apmaksai**, lai parādītu sarakstu ar visiem atļautajiem atgriešanas norēķinu veidiem.</span><span class="sxs-lookup"><span data-stu-id="b0f83-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="b0f83-145">- vai -</span><span class="sxs-lookup"><span data-stu-id="b0f83-145">-or-</span></span>

1. <span data-ttu-id="b0f83-146">Piesakieties POS kā kasieris vai menedžeris.</span><span class="sxs-lookup"><span data-stu-id="b0f83-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="b0f83-147">Atlasiet **Atgriešanas transakcija** un ievadiet saņemšanas ID, izmantojot svītrkoda skenēšanu vai manuālu ievadi.</span><span class="sxs-lookup"><span data-stu-id="b0f83-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="b0f83-148">Atlasiet transakciju, kas ir daļa no atgriešanas.</span><span class="sxs-lookup"><span data-stu-id="b0f83-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="b0f83-149">Atlasiet atgriežamos krājumus un izvēlieties maksājuma metodi.</span><span class="sxs-lookup"><span data-stu-id="b0f83-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="b0f83-150">Ja izvēlētais maksājuma norēķins ir atļauto atgriešanas norēķinu tipu sarakstā, kasieris var pabeigt darbību.</span><span class="sxs-lookup"><span data-stu-id="b0f83-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="b0f83-151">Ja atlasītais maksājuma norēķins nav atļauts, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="b0f83-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="b0f83-152">Izvēlieties **Summa apmaksai**, lai parādītu sarakstu ar visiem atļautajiem atgriešanas norēķinu veidiem.</span><span class="sxs-lookup"><span data-stu-id="b0f83-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="b0f83-153">![Atmaksa nav atļauta](media/Return-policy-page6.png "Atmaksas veids nav atļauts")</span><span class="sxs-lookup"><span data-stu-id="b0f83-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="b0f83-154">![Maksāšanas metožu saraksts](media/Return-policy-page5.PNG "Atļautie atmaksas veidi")</span><span class="sxs-lookup"><span data-stu-id="b0f83-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
