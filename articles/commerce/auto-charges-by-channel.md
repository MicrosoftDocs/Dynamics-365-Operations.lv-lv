---
title: Automātisko maksu iespējošana un konfigurēšana katram kanālam
description: Šajā tēmā paskaidrots, kā iespējot un konfigurēt automātiskās izmaksas pēc kanāla risinājumā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 23d02cf96faf3753303435acc148bf71e487d791
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799920"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="39402-103">Automātisko maksu iespējošana un konfigurēšana katram kanālam</span><span class="sxs-lookup"><span data-stu-id="39402-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="39402-104">Šajā tēmā paskaidrots, kā iespējot un konfigurēt automātiskās izmaksas pēc kanāla risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="39402-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="39402-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="39402-105">Overview</span></span>

<span data-ttu-id="39402-106">Jūs varat izmantot scenārijus, kuros maksas par pārstrādi vai citām maksām ir jāpiemēro preču grupai, kas tiek pārdota visos vai dažos veikalos noteiktā štatā (piemēram, Kalifornijā).</span><span class="sxs-lookup"><span data-stu-id="39402-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="39402-107">**Iespējot filtra automātiskās izmaksas pēc kanāla** līdzeklis programmā Commerce ļauj norādīt automātiskās maksas pēc kanāla (piemēram, fiziskas pārdošanas kanāls).</span><span class="sxs-lookup"><span data-stu-id="39402-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="39402-108">Šis līdzeklis ir pieejams programmā Dynamics 365 Commerce 10.0.10 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="39402-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="39402-109">Lai iespējotu un konfigurētu automātiskās izmaksas pēc kanāla, ir jāveic šādi uzdevumi:</span><span class="sxs-lookup"><span data-stu-id="39402-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="39402-110">Ieslēdziet līdzekli **Iespējot filtra automātiskās izmaksas pēc kanāla**.</span><span class="sxs-lookup"><span data-stu-id="39402-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="39402-111">Konfigurējiet organizācijas hierarhijas nolūku.</span><span class="sxs-lookup"><span data-stu-id="39402-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="39402-112">Definēt automātiskās izmaksas pēc kanāla.</span><span class="sxs-lookup"><span data-stu-id="39402-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="39402-113">**Iespējot filtra automātiskās izmaksas pēc kanāla** līdzeklis darbojas tikai tad, ja ir ieslēgts arī papildu automātiskās izmaksas līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="39402-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="39402-114">Informāciju par to, kā ieslēgt papildu automātiskās izmaksas līdzekli, skatiet [Omni-Channel Advanced automātiskā izmaksas](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="39402-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="39402-115">Ieslēdziet līdzekli Iespējot filtra automātiskās izmaksas pēc kanāla</span><span class="sxs-lookup"><span data-stu-id="39402-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="39402-116">Lai aktivizētu automātiskās izmaksas pēc kanāla programmā Commerce, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="39402-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="39402-117">Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="39402-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="39402-118">Cilnē **Neiespējots**, kas atrodas sarakstā **Līdzekļa nosaukums**, atrodiet un atlasiet opciju **Iespējot filtra automātiskas izmaksas pēc kanāla**.</span><span class="sxs-lookup"><span data-stu-id="39402-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="39402-119">Labajā apakšējā stūrī atlasiet opciju **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="39402-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="39402-120">Pēc tam, kad līdzeklis ir ieslēgts, tas tiks parādīts cilnes **Visas** sarakstā.</span><span class="sxs-lookup"><span data-stu-id="39402-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="39402-121">Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="39402-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="39402-122">Kreisajā rūtī atrodiet un atlasiet **1110** (**Globālā konfigurācija**) darbu.</span><span class="sxs-lookup"><span data-stu-id="39402-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="39402-123">Darbības rūtī atlasiet **Palaist tagad**, lai ieviestu konfigurācijas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="39402-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="39402-124">Izslēdzot līdzekli **Iespējot filtra automātiskās izmaksas pēc kanāla** pēc tam, kad esat to jau izmantojis, **Mazumtirdzniecības kanālu relāciju** lauks sadaļā **Automātiskās izmaksas** vairs netiks rādīts un jūs pazaudēsiet visas esošās konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="39402-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="39402-125">Ja **Mazumtirdzniecības kanāla relāciju** konfigurāciju noņemšana izraisīs automātisku izmaksu noteikumu dublēšanos, mēģinājums izslēgt līdzekli būs neveiksmīgs.</span><span class="sxs-lookup"><span data-stu-id="39402-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="39402-126">Pirms līdzekļa izslēgšanas noteikti pārskatiet visus automātiskās izmaksas nosacījumus un veiciet nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="39402-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="39402-127">Konfigurējiet organizācijas hierarhijas nolūku</span><span class="sxs-lookup"><span data-stu-id="39402-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="39402-128">Tiek izveidots jauns organizācijas hierarhijas nolūks ar nosaukumu **Mazumtirdzniecības automātiskā izmaksa**, kas ir izveidota, lai pārvaldītu automātisko izmaksu hierarhiju pēc kanāla.</span><span class="sxs-lookup"><span data-stu-id="39402-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="39402-129">Lai piešķirtu noklusējuma hierarhiju uzņēmuma hierarhijas mērķim programmā Commerce, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="39402-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="39402-130">Dodieties uz **Organizācijas administrēšana \> Organizācijas \> Organizācijas hierarhijas nolūki**.</span><span class="sxs-lookup"><span data-stu-id="39402-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="39402-131">Kreisajā rūtī atlasiet **Mazumtirdzniecības automātiskā izmaksa**.</span><span class="sxs-lookup"><span data-stu-id="39402-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="39402-132">Sadaļā **Piešķirtās hierarhijas** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="39402-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="39402-133">Dialoglodziņā **Organizācijas hierarhijas** atlasiet organizācijas hierarhiju (piemēram, **Mazumtirdzniecības veikali pēc reģiona**) un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="39402-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="39402-134">Sadaļā **Piešķirtās hierarhijas** atlasiet **Iestatīt kā noklusējumu**.</span><span class="sxs-lookup"><span data-stu-id="39402-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="39402-135">Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="39402-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="39402-136">Kreisajā rūtī atrodiet un atlasiet **1040** (**Preces**) darbu.</span><span class="sxs-lookup"><span data-stu-id="39402-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="39402-137">Darbību rūtī atlasiet **Palaist tagad**.</span><span class="sxs-lookup"><span data-stu-id="39402-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="39402-138">Atkārtojiet iepriekšējos divus soļus, lai palaistu **1070** (**Kanāla konfigurācija**) un **1110** (**Globālā konfigurācija**) darbus.</span><span class="sxs-lookup"><span data-stu-id="39402-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Mazumtirdzniecības automātiskās izmaksas organizācijas hierarhijas nolūka konfigurācija](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="39402-140">Definēt automātiskās izmaksas pēc kanāla</span><span class="sxs-lookup"><span data-stu-id="39402-140">Define auto charges by channel</span></span>

<span data-ttu-id="39402-141">Pēc tam, kad esat ieslēdzis līdzekli **Iespējot filtra automātiskās izmaksas pēc kanāla** un konfigurējis **Mazumtirdzniecības automātiskās izmaksas** organizācijas hierarhijas mērķi, automātiskās izmaksas pēc kanāla var definēt vai nu pasūtījuma virsraksta līmenī, vai pasūtījuma rindas līmenī.</span><span class="sxs-lookup"><span data-stu-id="39402-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="39402-142">Lai definētu automātiskās izmaksas pēc kanāla programmā Commerce, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="39402-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="39402-143">Pārejiet uz sadaļu **Debitori \> Izmaksu iestatīšana \> Automātiskās izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="39402-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="39402-144">Kreisajā rūtī laukā **Līmenis** izvēlieties vai nu **Galveni** vai **Rindu** atkarībā no jūsu biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="39402-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="39402-145">Laukā **Mazumtirdzniecības kanāla kods** izvēlieties atbilstošo kanāla kodu (piemēram, **Tabula** vai **Grupa**).</span><span class="sxs-lookup"><span data-stu-id="39402-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="39402-146">Ja tiek izmantots noklusētais iestatījums **Visi**, izmaksas noteikumi tiek piemēroti visiem kanāliem.</span><span class="sxs-lookup"><span data-stu-id="39402-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="39402-147">Ja atlasāt **Grupu**, pārliecinieties, ka mazumtirdzniecības kanāla izmaksu grupa tiek izveidota sadaļā **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Izmaksas \> Mazumtirdzniecības kanāla izmaksas grupas**.</span><span class="sxs-lookup"><span data-stu-id="39402-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="39402-148">Ja atlasāt **Tabulu**, jūs varat atlasīt noteiktu kanālu (piemēram, **Sanfrancisko**) laukā **Mazumtirdzniecības kanāla relācija**.</span><span class="sxs-lookup"><span data-stu-id="39402-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="39402-149">Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="39402-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="39402-150">Kreisajā rūtī atrodiet un atlasiet **1040** (**Preces**) darbu.</span><span class="sxs-lookup"><span data-stu-id="39402-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="39402-151">Darbību rūtī atlasiet **Palaist tagad**.</span><span class="sxs-lookup"><span data-stu-id="39402-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="39402-152">Atkārtojiet iepriekšējos divus soļus, lai palaistu **1070** (**Kanāla konfigurācija**) un **1110** (**Globālā konfigurācija**) darbus.</span><span class="sxs-lookup"><span data-stu-id="39402-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Automātiskās izmaksas definētas pēc kanāla](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="39402-154">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="39402-154">Example scenario</span></span>

<span data-ttu-id="39402-155">Sekojošajā piemērā aprakstīti soļi, kas nepieciešami preces konfigurēšanai, lai otrreizējās pārstrādes izmaksas tiktu iekasētas, kad prece tiek pārdota, izmantojot Sanfrancisko faktiskās pārdošanas kanālu.</span><span class="sxs-lookup"><span data-stu-id="39402-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="39402-156">Piemērā ir arī parādīts, kā automātiskās izmaksas parādās Commerce pārdošanas punkta (POS) programmā.</span><span class="sxs-lookup"><span data-stu-id="39402-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="39402-157">Organizācija nosaka izmaksu kodu ar nosaukumu **PĀRSTRĀDE**, kā parādīts sekojošajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="39402-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![PĀRSTRĀDES izmaksu kods](media/Auto-charges-charge-code.png)

<span data-ttu-id="39402-159">Automātiska izmaksa ir izveidota rindas līmenī.</span><span class="sxs-lookup"><span data-stu-id="39402-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="39402-160">Tai ir tālāk minētā konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="39402-160">It has the following configuration:</span></span>

- <span data-ttu-id="39402-161">Lauks **Konta kods** ir iestatīts uz **Visi**.</span><span class="sxs-lookup"><span data-stu-id="39402-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="39402-162">Lauks **Krājuma kods** ir iestatīts uz **Tabula**.</span><span class="sxs-lookup"><span data-stu-id="39402-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="39402-163">Lauks **Krājuma relācija** ir iestatīts uz preces ID **91001**.</span><span class="sxs-lookup"><span data-stu-id="39402-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="39402-164">Lauks **Piegādes veida kods** ir iestatīts uz **Visi**.</span><span class="sxs-lookup"><span data-stu-id="39402-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="39402-165">Lauks **Mazumtirdzniecības kanāla kods** ir iestatīts uz **Tabula**.</span><span class="sxs-lookup"><span data-stu-id="39402-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="39402-166">Lauks **Mazumtirdzniecības kanāla relācija** ir iestatīts uz **Sanfrancisko** veikalu.</span><span class="sxs-lookup"><span data-stu-id="39402-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="39402-167">Tiek izveidota automātiskā izmaksu rinda.</span><span class="sxs-lookup"><span data-stu-id="39402-167">An auto charges line is created.</span></span> <span data-ttu-id="39402-168">Tai ir tālāk minētā konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="39402-168">It has the following configuration:</span></span>

- <span data-ttu-id="39402-169">Lauks **Valūta** ir iestatīts uz **USD**.</span><span class="sxs-lookup"><span data-stu-id="39402-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="39402-170">Lauks **Izmaksu kods** ir iestatīts uz **PĀRSTRĀDE**.</span><span class="sxs-lookup"><span data-stu-id="39402-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="39402-171">Lauks **Kategorija** ir iestatīts uz **Fiksēts**.</span><span class="sxs-lookup"><span data-stu-id="39402-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="39402-172">Lauks **Izmaksas** ir iestatīts uz **$6.25**.</span><span class="sxs-lookup"><span data-stu-id="39402-172">The **Charges** field is set to **$6.25**.</span></span>

![Rindas līmeņa automātiskās izmaksas un automātiskās izmaksas rindas konfigurācija](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="39402-174">POS programmā ir izveidots pārdošanas pasūtījums **Sanfrancisko** veikala kanālā.</span><span class="sxs-lookup"><span data-stu-id="39402-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="39402-175">**Izmaksu** rindā ir redzama pārstrādes izmaksa **$6.25**.</span><span class="sxs-lookup"><span data-stu-id="39402-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="39402-176">Atlasot **Transakciju opcijas \> Izmaksas \> Pārvaldīt maksas** POS programmā, varat skatīt izmaksu kodu un aprakstu par pārstrādes izmaksu.</span><span class="sxs-lookup"><span data-stu-id="39402-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Otrreizējās pārstrādes maksa POS programmā](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="39402-178">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="39402-178">Additional resources</span></span>

[<span data-ttu-id="39402-179">Omni kanāla papildu automātiskās maksas</span><span class="sxs-lookup"><span data-stu-id="39402-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="39402-180">Proporcionāla virsraksta maksu sadalīšana atbilstošajās pārdošanas rindās</span><span class="sxs-lookup"><span data-stu-id="39402-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]