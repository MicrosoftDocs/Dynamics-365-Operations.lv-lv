---
title: Mazu paku nosūtīšana
description: Šajā tēmā ir sniegta informācija par mazu paku nosūtīšanas (SPS) līdzekli. Šis līdzeklis ļauj korporācijai Microsoft Dynamics 365 Supply Chain Management iesniegt pārvadātājam datus par iepakotu konteineru un pēc tam no šī pārvadātāja saņemt atpakaļ nosūtīšanas etiķeti, nosūtīšanas likmi un izsekošanas numuru.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910213"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="7db23-104">Mazu paku nosūtīšana</span><span class="sxs-lookup"><span data-stu-id="7db23-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7db23-105">Izmantojot maza sūtījuma (SPS) līdzekli, korporācija Microsoft Dynamics 365 Supply Chain Management var tieši sazināties ar nosūtīšanas pārvadātājiem, izmantojot pārvadātāju API sakaru struktūru.</span><span class="sxs-lookup"><span data-stu-id="7db23-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="7db23-106">Šī funkcionalitāte ir noderīga, ja noslogojiet atsevišķus pārdošanas pasūtījumus caur komerciālajiem kravu pārvadātājiem, nevis izmantojot konteinera nosūtīšanu vai mazāk nekā-kravas (LTL) slodzi.</span><span class="sxs-lookup"><span data-stu-id="7db23-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="7db23-107">SPS funkcija mijiedarbojas ar jūsu sūtījumu pārvadātāju, izmantojot *atvēlēto likmes* programmu.</span><span class="sxs-lookup"><span data-stu-id="7db23-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="7db23-108">Jūsu organizācijai attīstiet šo likmes programmu sadarbības ar jūsu pārvadātāja vai pārvadātāja pārkraušanas centra pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="7db23-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="7db23-109">Šis līdzeklis ļauj Supply Chain Management iesniegt pārvadātājam datus par iepakotu konteineru un pēc tam no šī pārvadātāja saņemt atpakaļ nosūtīšanas etiķeti, nosūtīšanas likmi un izsekošanas numuru.</span><span class="sxs-lookup"><span data-stu-id="7db23-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="7db23-110">Atgrieztā nosūtīšanas likme ir pievienota saistītajam pārdošanas pasūtījumam kā papildmaksa.</span><span class="sxs-lookup"><span data-stu-id="7db23-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="7db23-111">Pēc tam atgriezto nosūtīšanas etiķeti var automātiski izdrukāt, izmantojot Zebra programmēšanas valodas (ZPL) printeri un pielietojot sūtījumam.</span><span class="sxs-lookup"><span data-stu-id="7db23-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="7db23-112">Pārvadātājs skenēs šo nosūtīšanas etiķeti, saņemot savā noliktavā iepakojumus.</span><span class="sxs-lookup"><span data-stu-id="7db23-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="7db23-113">Sistēmas sagatavošana SPS atbalstam</span><span class="sxs-lookup"><span data-stu-id="7db23-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="7db23-114">Pirms varat sākt lietot SPS funkcionalitāti, līdzekļa pārvaldībā ieslēdziet SPS funkciju, pievienojiet likmes programmu un iestatiet **Transportēšanas pārvaldības** un **Noliktavas pārvaldības moduļus** tā atbalstam.</span><span class="sxs-lookup"><span data-stu-id="7db23-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="7db23-115">SPS līdzekļa iespējošana</span><span class="sxs-lookup"><span data-stu-id="7db23-115">Turn on the SPS feature</span></span>

<span data-ttu-id="7db23-116">Lai varētu izmantot SPS līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="7db23-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="7db23-117">Administratori var izmantot [Funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="7db23-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="7db23-118">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="7db23-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7db23-119">**Modulis:** *Transportēšanas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="7db23-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="7db23-120">**Līdzekļa nosaukums:** *Mazu paku nosūtīšana*</span><span class="sxs-lookup"><span data-stu-id="7db23-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="7db23-121">Izvietot un iestatīt likmes programmas</span><span class="sxs-lookup"><span data-stu-id="7db23-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="7db23-122">Supply Chain Management nav ietverta neviena likmes programma.</span><span class="sxs-lookup"><span data-stu-id="7db23-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="7db23-123">Ir jāiegūst vai jāizveido likmes programmas, kas jums nepieciešamas, un pēc tam tās jāpievieno jūsu sistēmai.</span><span class="sxs-lookup"><span data-stu-id="7db23-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="7db23-124">Tomēr Microsoft sniedz likmes paraugprogrammu, ko varat izmantot testēšanai.</span><span class="sxs-lookup"><span data-stu-id="7db23-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="7db23-125">Lejupielādēt un izvietot demonstrācijas likmes programmu</span><span class="sxs-lookup"><span data-stu-id="7db23-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="7db23-126">Izpildiet šīs darbības, lai iegūtu likmes paraugprogrammu.</span><span class="sxs-lookup"><span data-stu-id="7db23-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="7db23-127">GitHub lejupielādēt [dinamiskās saites bibliotēku (DLL) likmes paraugprogrammu](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="7db23-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="7db23-128">Supply Chain Management serverī saglabājiet DLL mapē **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="7db23-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="7db23-129">Izveidot un izvietot funkcionālās likmes programmas</span><span class="sxs-lookup"><span data-stu-id="7db23-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="7db23-130">Informāciju par to, kā izveidot un izvietot funkcionālās likmes programmas, lai tās varētu izmantot ražošanas vai testēšanas vidē, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="7db23-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="7db23-131">Jaunas transportēšanas pārvaldības programmas izveide</span><span class="sxs-lookup"><span data-stu-id="7db23-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="7db23-132">Transportēšanas pārvaldības programmu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7db23-132">Set up transportation management engines</span></span>](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="7db23-133">Papildinformāciju par SPS likmes programmas izveidošanas veidu skatiet tālāk šajā rakstā: [Mazo paku nosūtīšana: kā līdzsvarot mazu paku nosūtīšanas Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="7db23-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="7db23-134">Iestatīt likmes programmu Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7db23-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="7db23-135">Kad esat izveidojis un izvietojis SPS likmes programmu, veiciet šos soļus, lai to iestatītu.</span><span class="sxs-lookup"><span data-stu-id="7db23-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="7db23-136">Dodieties uz **Transportēšanas pārvaldība \> Iestatīšana \> Vērtējums \> Likmes šablons**.</span><span class="sxs-lookup"><span data-stu-id="7db23-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="7db23-137">Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7db23-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="7db23-138">Jaunajā rindā iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7db23-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="7db23-139">**Likmes programma** - ievadiet unikālu likmes programmas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7db23-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="7db23-140">Ja izmantojat demonstrācijas likmes programmu, ievadiet *Likmes paraugprogrammu*.</span><span class="sxs-lookup"><span data-stu-id="7db23-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="7db23-141">**Nosaukums** – ievadiet likmes programmas īsu aprakstu.</span><span class="sxs-lookup"><span data-stu-id="7db23-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="7db23-142">Ja izmantojat demonstrācijas likmes programmu, ievadiet *Likmes paraugprogrammu*.</span><span class="sxs-lookup"><span data-stu-id="7db23-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="7db23-143">**Vērtējuma metadatu ID** - izvēlieties pamatu, kas ir jāizmanto, lai aprēķinātu jūsu likmi.</span><span class="sxs-lookup"><span data-stu-id="7db23-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="7db23-144">Piemēram, jūsu likme var tikt aprēķināta, pamatojoties uz attālumu.</span><span class="sxs-lookup"><span data-stu-id="7db23-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="7db23-145">Ja izmantojat likmes paraugprogrammu, varat atstāt šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="7db23-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="7db23-146">**Programmas komplektācija** - ievadiet izvietotās DLL pakotnes faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7db23-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="7db23-147">Ja izmantojat likmes paraugprogrammu, ievadiet *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="7db23-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="7db23-148">**Programmas klase** – ievadiet klases nosaukumu, kas tika izveidots jūsu likmes programmai.</span><span class="sxs-lookup"><span data-stu-id="7db23-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="7db23-149">Ja izmantojat likmes paraugprogrammu, ievadiet *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="7db23-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="7db23-150">Piemērs</span><span class="sxs-lookup"><span data-stu-id="7db23-150">Example scenario</span></span>

<span data-ttu-id="7db23-151">Šajā piemērā ir parādīts, kā iestatīt un izmantot SPS pēc tam, kad esat sagatavojis sistēmu, kā aprakstīts iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="7db23-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="7db23-152">Šajā scenārijā tiek izmantota iepriekš minētā likmes paraugprogramma.</span><span class="sxs-lookup"><span data-stu-id="7db23-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="7db23-153">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="7db23-153">Make demo data available</span></span>

<span data-ttu-id="7db23-154">Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [paraugdati](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7db23-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="7db23-155">Turklāt pirms sākšanas ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="7db23-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="7db23-156">Scenārija iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7db23-156">Set up the scenario</span></span>

<span data-ttu-id="7db23-157">Šajā piemērā jums ir jābūt demonstrācijas pārvadātājam, pārvadātāju grupai, iepakošanas politikai un iepakošanas profilam.</span><span class="sxs-lookup"><span data-stu-id="7db23-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="7db23-158">Tālākajāš apakšdaļās ir izskaidrots, kā sagatavot scenārijam nepieciešamos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="7db23-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="7db23-159">Ražošanas scenārijā iestatīšanas process parasti ir līdzīgs šeit aprakstītajam procesam.</span><span class="sxs-lookup"><span data-stu-id="7db23-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="7db23-160">Tomēr jūs iestatīsiet dažādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="7db23-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="7db23-161">Sūtījumu pārvadātāju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7db23-161">Set up carriers</span></span>

<span data-ttu-id="7db23-162">Lai iestatītu pārvadātāju, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7db23-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="7db23-163">Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Sūtījumu pārvadātāji**.</span><span class="sxs-lookup"><span data-stu-id="7db23-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="7db23-164">Lai pievienotu pārvadātāju, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7db23-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="7db23-165">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="7db23-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="7db23-166">**Nosūtījuma pārvadātājs:** *Parauga pārvadātājs*</span><span class="sxs-lookup"><span data-stu-id="7db23-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="7db23-167">**Nosaukums:** *Parauga pārvadātājs*</span><span class="sxs-lookup"><span data-stu-id="7db23-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="7db23-168">**Režīms:** *Sauszeme*</span><span class="sxs-lookup"><span data-stu-id="7db23-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="7db23-169">Kopsavilkuma cilnē **Pārskats** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="7db23-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7db23-170">**Aktivizējiet nosūtījuma pārvadātāja:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="7db23-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="7db23-171">**Aktivizējiet pārvadātāja vērtēšanu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="7db23-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="7db23-172">Kopsavilkuma cilnē **Pakalpojumi** atlasiet **Jauns**, lai pievienotu režģim pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="7db23-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="7db23-173">Iestatiet šādas vērtības jaunajam pakalpojumam:</span><span class="sxs-lookup"><span data-stu-id="7db23-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="7db23-174">**Pārvadātāja pakalpojums:** *Parauga pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="7db23-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="7db23-175">**Nosaukums:** *Parauga pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="7db23-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="7db23-176">**Transportēšanas metode:** *Sauszeme*</span><span class="sxs-lookup"><span data-stu-id="7db23-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="7db23-177">Pēc vajadzības ievadiet vērtību visiem citiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="7db23-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="7db23-178">(Saglabājot jauno sūtījuma pārvadātāja ierakstu, tiks izveidots jauns piegādes veids un **Piegādes veida** lauks tiks iestatīts automātiski.)</span><span class="sxs-lookup"><span data-stu-id="7db23-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="7db23-179">Kopsavilkuma cilnē **Novērtējuma profili** noklikšķiniet uz **Jauns**, lai pievienotu režģim novērtējuma profilu.</span><span class="sxs-lookup"><span data-stu-id="7db23-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="7db23-180">Iestatiet šādas vērtības jaunajam profilam:</span><span class="sxs-lookup"><span data-stu-id="7db23-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="7db23-181">**Novērtējuma profils:** *Parauga pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="7db23-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="7db23-182">**Nosaukums:** *Parauga pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="7db23-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="7db23-183">**Likmes likmes programma:** *Likmes paraugprogramma*</span><span class="sxs-lookup"><span data-stu-id="7db23-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="7db23-184">Pēc vajadzības ievadiet vērtību visiem citiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="7db23-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="7db23-185">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7db23-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="7db23-186">Plašāku informāciju par to, kā iestatīt abonementus, skatiet tēmā [Nosūtīšanas pārvadātāju iestatīšana](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="7db23-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="7db23-187">Iestatīt pārvadātāju pakalpojumu kontus</span><span class="sxs-lookup"><span data-stu-id="7db23-187">Set up carrier service accounts</span></span>

<span data-ttu-id="7db23-188">Lai iestatītu pārvadātāja pakalpojuma kontu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="7db23-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="7db23-189">Dodieties uz **Transportēšanas pārvaldība \> Iestatīšana \> Vērtējums \> Pārvadātāja pakalpojuma konts**.</span><span class="sxs-lookup"><span data-stu-id="7db23-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="7db23-190">Lai pievienotu pārvadātāja pakalpojuma kontu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7db23-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="7db23-191">Iestatiet šādas vērtības jaunajam kontam:</span><span class="sxs-lookup"><span data-stu-id="7db23-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="7db23-192">**Nosūtījuma pārvadātājs:** *Parauga pārvadātājs*</span><span class="sxs-lookup"><span data-stu-id="7db23-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="7db23-193">**Pārvadātāja pakalpojums:** *Parauga pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="7db23-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="7db23-194">**Pārvadātāja debitora konta numurs:** Pārvadātāja debitora konta numurs, kas tiek izmantots, lai pārbaudītu un autentificētu savienojumu ar sūtījuma pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="7db23-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="7db23-195">Šo vērtību nodrošina jūsu pārvadātājs.</span><span class="sxs-lookup"><span data-stu-id="7db23-195">Your carrier will provide this value.</span></span> <span data-ttu-id="7db23-196">Ja izmantojat demonstrācijas pakalpojumu, varat ievadīt papildu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7db23-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="7db23-197">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="7db23-197">**Site:** *6*</span></span>
    - <span data-ttu-id="7db23-198">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="7db23-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="7db23-199">Bieži **Pārvadātāja debitora konta numura vērtība** ir vienīgā vērtība, kas nepieciešama, lai autentificētu savienojumu.</span><span class="sxs-lookup"><span data-stu-id="7db23-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="7db23-200">Tomēr, ja jūsu pārvadātājam ir nepieciešami papildu autentifikācijas parametri, jūsu uzņēmumam šī lapa ir jāpielāgo, lai pievienotu atbilstošus papildu laukus.</span><span class="sxs-lookup"><span data-stu-id="7db23-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="7db23-201">Konteineru iepakošanas politiku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7db23-201">Set up a container packing policy</span></span>

<span data-ttu-id="7db23-202">Lai iestatītu konteinera iepakošanas politiku, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7db23-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="7db23-203">Ja vēl neesat iestatījis ZPL printera definīciju, lai to iestatītu, izmantojiet dokumentu maršrutēšanas aģenta programmu.</span><span class="sxs-lookup"><span data-stu-id="7db23-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="7db23-204">Papildinformāciju skatiet [Dokumentu drukāšanas apskatu](../../fin-ops-core/dev-itpro/analytics/print-documents.md) un saistītās tēmas.</span><span class="sxs-lookup"><span data-stu-id="7db23-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="7db23-205">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Konteineri \> Konteineru iepakošanas politikas**.</span><span class="sxs-lookup"><span data-stu-id="7db23-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="7db23-206">Lai pievienotu pārvadātāja pakalpojuma kontu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7db23-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="7db23-207">Jaunās politikas galvenē iestatiet tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="7db23-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="7db23-208">**Konteinera iepakošanas politika:** *Iepakošanas parauga politika*</span><span class="sxs-lookup"><span data-stu-id="7db23-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="7db23-209">**Apraksts:** Politikas apraksts</span><span class="sxs-lookup"><span data-stu-id="7db23-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="7db23-210">Kopsavilkuma cilnē **Pārskats** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="7db23-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7db23-211">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="7db23-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="7db23-212">**Noklusējuma galīgā sūtījuma novietojums:** *Nosūtīšanas krava*</span><span class="sxs-lookup"><span data-stu-id="7db23-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="7db23-213">**Svara vienība:** *KG*</span><span class="sxs-lookup"><span data-stu-id="7db23-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="7db23-214">**Konteineru slēgšanas politika:** *Automātiska izlaide*</span><span class="sxs-lookup"><span data-stu-id="7db23-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="7db23-215">**Konteinera izlaišanas politika:** *Padarīt pieejamu beigu nosūtīšanas vietā*</span><span class="sxs-lookup"><span data-stu-id="7db23-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="7db23-216">Kopsavilkuma cilnē **Konteinera manifests** varat iestatīt šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="7db23-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7db23-217">**Automātisks manifests konteinera slēgšanas laikā:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="7db23-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="7db23-218">**Konteinera manifesta prasības:** *Transportēšanas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="7db23-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="7db23-219">**Drukāt konteinera saturu:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="7db23-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="7db23-220">Kopsavilkuma cilnē **Pārvadātāja etiķetes drukāšana** varat iestatīt šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="7db23-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7db23-221">**Drukāt konteinera nosūtīšanas etiķeti:** *Vienmēr*</span><span class="sxs-lookup"><span data-stu-id="7db23-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="7db23-222">**Printera nosaukums:** ZPL printera nosaukums, kam jādrukā nosūtīšanas etiķetes</span><span class="sxs-lookup"><span data-stu-id="7db23-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="7db23-223">Iepakošanas profila iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7db23-223">Set up a packing profile</span></span>

<span data-ttu-id="7db23-224">Lai iestatītu iepakošanas profilu, veiciet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7db23-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="7db23-225">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Iepakošana \> Iepakošanas profili**.</span><span class="sxs-lookup"><span data-stu-id="7db23-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="7db23-226">Lai pievienotu režģim iepakošanas profilu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7db23-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="7db23-227">Iestatiet šādas vērtības jaunajam profilam:</span><span class="sxs-lookup"><span data-stu-id="7db23-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="7db23-228">**Iepakošanas profila ID:** *Iepakošanas parauga profils*</span><span class="sxs-lookup"><span data-stu-id="7db23-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="7db23-229">**Apraksts:** Profila apraksts</span><span class="sxs-lookup"><span data-stu-id="7db23-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="7db23-230">**Konteinera iepakošanas politika:** *Iepakošanas parauga politika*</span><span class="sxs-lookup"><span data-stu-id="7db23-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="7db23-231">**Konteinera ID režīms:** *Automātiski*</span><span class="sxs-lookup"><span data-stu-id="7db23-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="7db23-232">**Konteinera veids:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="7db23-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="7db23-233">Iestatīt debitoru SPS pārvadātāja izmantošanai</span><span class="sxs-lookup"><span data-stu-id="7db23-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="7db23-234">Veiciet šīs darbības, lai iestatītu debitoru un varētu izmantot izveidoto pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="7db23-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="7db23-235">Dodieties uz sadaļu **Debitori \> debitori \> Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="7db23-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="7db23-236">Režģī atrodiet un atlasiet debitoru *US-027*.</span><span class="sxs-lookup"><span data-stu-id="7db23-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="7db23-237">Darbību rūtī cilnes **Vispārīgi** grupā **Iestatījumi** atlasiet **Pārvadātāja debitora konti**.</span><span class="sxs-lookup"><span data-stu-id="7db23-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="7db23-238">Lapā **Pārvadātāja debitora konti** darbību rūtī atlasiet **Jauns**, lai pievienotu režģim kontu.</span><span class="sxs-lookup"><span data-stu-id="7db23-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="7db23-239">Iestatiet šādas vērtības jaunajam kontam:</span><span class="sxs-lookup"><span data-stu-id="7db23-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="7db23-240">**Nosūtījuma pārvadātājs:** *Parauga pārvadātājs*</span><span class="sxs-lookup"><span data-stu-id="7db23-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="7db23-241">**Pārvadātāja debitora konta numurs:** *12345* (Vērtība nav būtiska šim scenārijam, bet tā tiks pievienota nākamajā sadaļā.)</span><span class="sxs-lookup"><span data-stu-id="7db23-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="7db23-242">Iet cauri piemēra scenārijam</span><span class="sxs-lookup"><span data-stu-id="7db23-242">Go through the example scenario</span></span>

<span data-ttu-id="7db23-243">Pēc visu parauga datu iestatīšanas atbilstoši iepriekšējā sadaļā aprakstītajam, varat iziet cauri piemēra scenārijam.</span><span class="sxs-lookup"><span data-stu-id="7db23-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="7db23-244">Izveidot un apstrādāt pārdošanas pasūtījumu un darbu</span><span class="sxs-lookup"><span data-stu-id="7db23-244">Create a sales order and process the work</span></span>

<span data-ttu-id="7db23-245">Lai izveidotu pārdošanas pasūtījumu, veiciet sekojošās darbības.</span><span class="sxs-lookup"><span data-stu-id="7db23-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="7db23-246">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="7db23-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7db23-247">Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="7db23-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="7db23-248">Dialoglodziņā **Pārdošanas pasūtījuma izveide** **Klienta konta** laukā atlasiet *US-027*.</span><span class="sxs-lookup"><span data-stu-id="7db23-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="7db23-249">Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu un aizvērtu dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7db23-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="7db23-250">Jaunais pārdošanas pasūtījums ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="7db23-250">The new sales order is opened.</span></span> <span data-ttu-id="7db23-251">Kopsavilkuma cilnē **Pārdošanas pasūtījuma galvene** laukā **Pārvadātāja debitora kods** iestatiet vērtību, kuru atlasījāt šim debitoram iepriekš *(12345*).</span><span class="sxs-lookup"><span data-stu-id="7db23-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="7db23-252">Sadaļā **Pārdošanas pasūtījuma rindas** pievienojiet pārdošanas rindu un iestatiet tai šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="7db23-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="7db23-253">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="7db23-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="7db23-254">**Daudzums:** *1*</span><span class="sxs-lookup"><span data-stu-id="7db23-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="7db23-255">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="7db23-255">**Site:** *6*</span></span>
    - <span data-ttu-id="7db23-256">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="7db23-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="7db23-257">Pārejiet uz skatu **Galvene**.</span><span class="sxs-lookup"><span data-stu-id="7db23-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="7db23-258">Kopsavilkuma cilnē **Piegāde** iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="7db23-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7db23-259">**Nosūtījuma pārvadātājs:** *Parauga pārvadātājs*</span><span class="sxs-lookup"><span data-stu-id="7db23-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="7db23-260">**Pārvadātāja pakalpojums:** *Parauga pārvadātāja pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="7db23-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="7db23-261">Pārejiet atpakaļ uz skatu **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="7db23-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="7db23-262">Ja tiek piedāvāts atjaunināt pārdošanas rindu piegādes veidu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7db23-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="7db23-263">Sadaļā **Pārdošanas pasūtījuma rindas** atlasiet iepriekš iestatīto pasūtījuma rindu un pēc tam atlasiet **Krājums \> Rezervēšana**.</span><span class="sxs-lookup"><span data-stu-id="7db23-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="7db23-264">Lapā **Rezervācija** atlasiet **Rezervēt partiju**, lai rezervētu izvēlētās rindas pilno daudzumu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="7db23-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="7db23-265">Aizveriet **Rezervācijas** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="7db23-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="7db23-266">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="7db23-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="7db23-267">Darbs ir izveidots, lai pārvietotu krājumus no izdošanas vietas uz iepakošanas staciju.</span><span class="sxs-lookup"><span data-stu-id="7db23-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="7db23-268">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Noliktava \> Detalizēta informācija par sūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="7db23-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="7db23-269">Lapā **Detalizēta informācija** par sūtījumu atzīmējiet sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="7db23-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="7db23-270">Tas būs nepieciešams, kad iepakosiet sūtījumu iepakošanas stacijā.</span><span class="sxs-lookup"><span data-stu-id="7db23-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="7db23-271">Aizveriet **Detalizēta informācija par sūtījumu** lapu, lai atgrieztos pie pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="7db23-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="7db23-272">Atzīmējiet pārdošanas pasūtījuma numuru un pēc tam dodieties uz darbu **Noliktavas pārvaldība \> Darbs \> Visi darbi**.</span><span class="sxs-lookup"><span data-stu-id="7db23-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="7db23-273">Izmantojiet pārdošanas pasūtījuma numuru, lai atrastu un atlasītu darbu, kas tika izveidots pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="7db23-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="7db23-274">Darbību rūts cilnē **Darbs** atlasiet **Pabeigt darbu**.</span><span class="sxs-lookup"><span data-stu-id="7db23-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="7db23-275">**Darba pabeigšanas** lapas **Lietotāja ID** laukā atlasiet lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="7db23-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="7db23-276">Darbību rūtī atlasiet **Apstiprināt darbu**.</span><span class="sxs-lookup"><span data-stu-id="7db23-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="7db23-277">Ja darbs tiek validēts, atlasiet darbību rūtī **Pabeigt darbu**.</span><span class="sxs-lookup"><span data-stu-id="7db23-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="7db23-278">Darbs ir atzīmēts kā pabeigts, lai simulētu krājumu kustību uz iepakošanas staciju.</span><span class="sxs-lookup"><span data-stu-id="7db23-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="7db23-279">Sūtījuma iepakošana</span><span class="sxs-lookup"><span data-stu-id="7db23-279">Pack the shipment</span></span>

<span data-ttu-id="7db23-280">Lai iepakotu sūtījumu, veiciet sekojošās darbības.</span><span class="sxs-lookup"><span data-stu-id="7db23-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="7db23-281">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbinieks** un pārliecinieties, vai noliktavas pārvaldībai jūsu lietotāja konts ir saistīts ar darbinieka kontu.</span><span class="sxs-lookup"><span data-stu-id="7db23-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="7db23-282">Dodieties uz **Noliktavas pārvaldība \> Izdošana un konteinerizēšana \> Iepakot**.</span><span class="sxs-lookup"><span data-stu-id="7db23-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="7db23-283">Dialoglodziņā **Atlasīt iepakošanas vietu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="7db23-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7db23-284">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="7db23-284">**Site:** *6*</span></span>
    - <span data-ttu-id="7db23-285">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="7db23-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="7db23-286">**Atrašanās vieta:** *Pakotne*</span><span class="sxs-lookup"><span data-stu-id="7db23-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="7db23-287">**Iepakošanas profila ID:** *Iepakošanas parauga profils*</span><span class="sxs-lookup"><span data-stu-id="7db23-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="7db23-288">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7db23-288">Select **OK**.</span></span>
1. <span data-ttu-id="7db23-289">Tiek atvērta lapa **Iepakošana**.</span><span class="sxs-lookup"><span data-stu-id="7db23-289">The **Pack** page appears.</span></span> <span data-ttu-id="7db23-290">Ražošanas scenārijā darbinieks skenēs numura zīmi vai sūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="7db23-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="7db23-291">Tomēr šajā scenārijā atveriet lapu **Visas kravas** un uzmeklēs sūtījuma numuru sūtījumam, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="7db23-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="7db23-292">Pēc tam ievadiet šo vērtību laukā **Numura zīme vai krava** lapā **Iepakošana**.</span><span class="sxs-lookup"><span data-stu-id="7db23-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="7db23-293">Vai arī ievadiet projekta ID, kuru iepriekš atzīmējāt.</span><span class="sxs-lookup"><span data-stu-id="7db23-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="7db23-294">Darbību rūtī atlasiet **Jauns konteiners**.</span><span class="sxs-lookup"><span data-stu-id="7db23-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="7db23-295">Dialoglodziņš, kurā ir redzama detalizēta informācija par jauno konteineru.</span><span class="sxs-lookup"><span data-stu-id="7db23-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="7db23-296">Atstājiet noklusējuma vērtības un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7db23-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="7db23-297">**Pakotnes** lapas **Krājumu iepakojuma** kopsavilkuma cilnes laukā **Identifikators** atlasiet *A0002*, lai šo krājumu iepakotu.</span><span class="sxs-lookup"><span data-stu-id="7db23-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="7db23-298">Krājums ir pievienots konteineram.</span><span class="sxs-lookup"><span data-stu-id="7db23-298">The item is added to the container.</span></span>
1. <span data-ttu-id="7db23-299">Darbību rūtī atlasiet **Sūtījumu konteineri**.</span><span class="sxs-lookup"><span data-stu-id="7db23-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="7db23-300">Parādītajā **Kravas konteineru** lapā ir tā konteinera rinda, kuru tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="7db23-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="7db23-301">Tomēr **Konteinera manifesta ID** lauks šajā rindā pašlaik ir tukšs, jo neesat vēl saņēmis nosūtīšanas etiķeti un izsekošanas numuru no pārvadātāja.</span><span class="sxs-lookup"><span data-stu-id="7db23-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="7db23-302">Darbību rūtī atlasiet **Slēgt konteineru**.</span><span class="sxs-lookup"><span data-stu-id="7db23-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="7db23-303">Dialoglodziņā **Aizvērt konteineru** iestatiet lauku **Bruto svars** uz *1 kg* un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7db23-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="7db23-304">Nosūtīšanas uzlīme tagad ir jādrukā iepriekš atlasītajā ZPL printerī.</span><span class="sxs-lookup"><span data-stu-id="7db23-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="7db23-305">Tiem vajadzētu līdzināties šādam piemēram.</span><span class="sxs-lookup"><span data-stu-id="7db23-305">It should resemble the following example.</span></span>

    <span data-ttu-id="7db23-306">![Nosūtīšanas uzlīmes piemērs](media/sps-label-example.png "Nosūtīšanas uzlīmes piemērs")</span><span class="sxs-lookup"><span data-stu-id="7db23-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="7db23-307">Ievērojiet, ka **Konteinera manifesta ID** un **Kopējās kravas** vērtības ir pievienotas kā saņemtas no pārvadātāja.</span><span class="sxs-lookup"><span data-stu-id="7db23-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]