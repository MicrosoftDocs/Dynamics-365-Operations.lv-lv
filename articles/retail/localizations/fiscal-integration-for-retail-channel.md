---
title: "Finanšu integrācija mazumtirdzniecības kanālam"
description: "Šajā tēmā ir sniegts apskats par finanšu integrāciju programmai Retail POS."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: lv-lv
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="3a5f2-103">Finanšu integrācija mazumtirdzniecības kanālam</span><span class="sxs-lookup"><span data-stu-id="3a5f2-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a5f2-104">Šajā tēmā ir apskats par finanšu integrācijas funkcionalitāti, kas ir pieejama programmā Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="3a5f2-105">Finanšu integrācijas funkcionalitāte ir struktūra, kas ir izstrādāta lokālo finanšu likumu atbalstīšanai ar mērķi novērst krāpšanu mazumtirdzniecības nozarē.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="3a5f2-106">Tālāk ir nepilnīgs saraksts ar tipiskajiem scenārijiem, uz kuriem attiektos finanšu integrācijas lietošana.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="3a5f2-107">Finanšu dokumentu drukāšana un izsniegšana debitoram.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="3a5f2-108">Informācijas iesniegšanas drošināšana saistībā ar POS veikto pārdošanu un atgriešanu uz ārēju pakalpojumu, ko nodrošina iestāde.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="3a5f2-109">Datu aizsardzības izmantošana ar elektronisko parakstu, ko ir autorizējusi iestāde.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="3a5f2-110">Šajā tēmā ir sniegtas vadlīnijas par finanšu integrācijas iestatīšanu, lai lietotāji varētu veikt tālāk norādītos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="3a5f2-111">Konfigurēt finanšu savienotājus, kas ir finanšu ierīces vai pakalpojumi, kurus izmanto finanšu reģistrācijas nolūkiem, piemēram, finanšu datu saglabāšanai, digitālajiem parakstiem un drošinātai iesniegšanai.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="3a5f2-112">Konfigurēt dokumentu nodrošinātāju, kas nosaka finanšu dokumentu ģenerēšanas izvades metodi un algoritmu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="3a5f2-113">Konfigurēt finanšu reģistrācijas procesu, kas nosaka darbību secību un katrā darbībā izmantoto savienotāju grupu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="3a5f2-114">Piešķirt finanšu reģistrācijas procesus POS funkcionalitātes profiliem.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="3a5f2-115">Piešķirt savienotāju tehniskos profilus aparatūras profiliem (lokālajiem finanšu savienotājiem) vai POS funkcionalitātes profiliem (citiem finanšu savienotāju tipiem).</span><span class="sxs-lookup"><span data-stu-id="3a5f2-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="3a5f2-116">Finanšu integrācijas izpildes plūsma</span><span class="sxs-lookup"><span data-stu-id="3a5f2-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="3a5f2-117">Nākamajā scenārijā ir parādīta parastā finanšu integrācijas izpildes plūsma.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="3a5f2-118">Inicializējiet fiskālās reģistrācijas procesu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="3a5f2-119">Kad ir izpildītas kādas darbības, kurām ir nepieciešama finanšu reģistrācija, piemēram, pēc mazumtirdzniecības transakcijas pabeigšanas, šis finanšu reģistrācijas process ir saistīts ar pašreizējo POS funkcionalitātes profilu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="3a5f2-120">Meklējiet finanšu savienotāju.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="3a5f2-121">Katrai finanšu reģistrācijas procesā ietvertajai finanšu reģistrācijas darbībai sistēma nosaka atbilstību ar finanšu savienotāju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="3a5f2-122">Šiem savienotājiem ir funkcionālais profils, kas ir ietverts norādītajā savienotāju grupā, un saraksts ar savienotājiem, kuru tehniskais profils ir saistīts ar pašreizējo aparatūras profilu (tikai savienotāju tipam, kas ir vienāds ar **Lokāls**) vai ar pašreizējo POS funkcionalitātes profilu (citiem savienotāju tipiem).</span><span class="sxs-lookup"><span data-stu-id="3a5f2-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="3a5f2-123">Veiciet finanšu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="3a5f2-124">Sistēma izpilda visas nepieciešamās darbības, kuras nosaka ar atrasto savienotāju saistītā komplektācija.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="3a5f2-125">Tas tiek darīts saskaņā ar šim savienotājam iepriekšējā darbībā atrastā funkcionālā profila un tehniskā profila iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="3a5f2-126">Pirms finanšu integrācijas lietošanas nepieciešamā iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3a5f2-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="3a5f2-127">Pirms sākat lietot finanšu integrācijas funkcionalitāti, vajadzētu definēt tālāk norādītos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="3a5f2-128">Lapā **Mazumtirdzniecības parametri** definējiet numuru sēriju finanšu funkcionālā profila numuram.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="3a5f2-129">Lapā **Mazumtirdzniecības koplietojamie parametri** definējiet numuru sērijas tālāk norādītajām atsaucēm.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="3a5f2-130">Finanšu tehniskā profila numurs</span><span class="sxs-lookup"><span data-stu-id="3a5f2-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="3a5f2-131">Finanšu savienotāja grupas numurs</span><span class="sxs-lookup"><span data-stu-id="3a5f2-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="3a5f2-132">Reģistrācijas procesa numurs</span><span class="sxs-lookup"><span data-stu-id="3a5f2-132">Registration process number</span></span>

- <span data-ttu-id="3a5f2-133">Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Finanšu savienotāji** izveidojiet vienumu **Finanšu savienotājs** katrai ierīcei vai pakalpojumam, ko plānojat izmantot finanšu integrācijas nolūkos.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="3a5f2-134">Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Finanšu dokumentu nodrošinātāji** izveidojiet vienumu **Finanšu dokumentu nodrošinātājs** visiem finanšu savienotājiem.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="3a5f2-135">Datu kartēšana tiek uzskatīta par daļu no finanšu dokumentu nodrošinātāja.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="3a5f2-136">Lai iestatītu citus datu kartējumus tam pašam savienotājam (piemēram, ja pastāv valstij raksturīgi noteikumi), jums vajadzētu izveidot dažādus finanšu dokumentu nodrošinātājus.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="3a5f2-137">Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Savienotāja funkcionālie profili** izveidojiet vienumu **Savienotāja funkcionālais profils** katram finanšu dokumentu nodrošinātājam.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="3a5f2-138">Atlasiet savienotāja nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-138">Select a connector name.</span></span>
  - <span data-ttu-id="3a5f2-139">Atlasiet kādu dokumentu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-139">Select a document provider.</span></span>
  - <span data-ttu-id="3a5f2-140">Cilnē **Pakalpojuma iestatīšana** norādiet PVN likmju iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="3a5f2-141">Cilnē **Datu kartēšana** norādiet PVN kodu kartējumu un norēķinu tipu kartējumu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="3a5f2-142">Piemēri</span><span class="sxs-lookup"><span data-stu-id="3a5f2-142">Examples</span></span> 

  |  | <span data-ttu-id="3a5f2-143">Formāts</span><span class="sxs-lookup"><span data-stu-id="3a5f2-143">Format</span></span> | <span data-ttu-id="3a5f2-144">Piemērs</span><span class="sxs-lookup"><span data-stu-id="3a5f2-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="3a5f2-145">PVN likmju iestatījumi</span><span class="sxs-lookup"><span data-stu-id="3a5f2-145">VAT rates settings</span></span> | <span data-ttu-id="3a5f2-146">value : VATrate</span><span class="sxs-lookup"><span data-stu-id="3a5f2-146">value : VATrate</span></span> | <span data-ttu-id="3a5f2-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="3a5f2-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="3a5f2-148">PVN kodu kartējums</span><span class="sxs-lookup"><span data-stu-id="3a5f2-148">VAT codes mapping</span></span> | <span data-ttu-id="3a5f2-149">VATcode : value</span><span class="sxs-lookup"><span data-stu-id="3a5f2-149">VATcode : value</span></span> | <span data-ttu-id="3a5f2-150">vat20 : 1, vat18 : 2</span><span class="sxs-lookup"><span data-stu-id="3a5f2-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="3a5f2-151">Norēķinu tipu kartējums</span><span class="sxs-lookup"><span data-stu-id="3a5f2-151">Tender types mapping</span></span> | <span data-ttu-id="3a5f2-152">TenderTyp : value</span><span class="sxs-lookup"><span data-stu-id="3a5f2-152">TenderTyp : value</span></span> | <span data-ttu-id="3a5f2-153">Cash : 1, Card : 2</span><span class="sxs-lookup"><span data-stu-id="3a5f2-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="3a5f2-154">Izveidojiet vienumu **Finanšu savienotāju grupas** sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Finanšu savienotāju grupa**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="3a5f2-155">Savienotāju grupa ir apakškopa no funkcionālajiem profiliem, kas ir saistīti ar finanšu savienotājiem, kuri veic identiskas funkcijas un finanšu reģistrācijas procesā tiek izmantoti tajā pašā posmā.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="3a5f2-156">Pievienojiet funkcionālos profilus savienotāju grupai.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="3a5f2-157">Lapā **Funkcionālie profili** noklikšķiniet uz **Pievienot** un atlasiet kādu profila numuru.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="3a5f2-158">Ja vēlaties pārtraukt šī funkcionālā profila izmantošanu, vienumu **Atspējot** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="3a5f2-159">Šīs izmaiņas ietekmē tikai pašreizējo savienotāju grupu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-159">This change affects the current connector group only.</span></span> <span data-ttu-id="3a5f2-160">Varat turpināt tā paša funkcionālā profila lietošanu citās savienotāju grupās.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="3a5f2-161">Vienā savienotāju grupā katram finanšu savienotājam var būt tikai viens funkcionālais profils.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="3a5f2-162">Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Savienotāja tehniskie profili** izveidojiet vienumu **Savienotāja tehniskais profils** katram finanšu savienotājam.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="3a5f2-163">Atlasiet savienotāja nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-163">Select a connector name.</span></span>
  - <span data-ttu-id="3a5f2-164">Atlasiet savienotāja tipu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-164">Select a connector type:</span></span> 
      - <span data-ttu-id="3a5f2-165">**Lokāls** — iestatiet šo tipu fiziskām ierīcēm vai programmām, kas ir instalētas lokāla mašīnā.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="3a5f2-166">**Iekšējs** — iestatiet šo tipu finanšu ierīcēm un pakalpojumiem, kas ir saistīti ar Retail Server.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="3a5f2-167">**Ārējs** — ārējiem finanšu pakalpojumiem, piemēram, tīmekļa portālam, ko nodrošina nodokļu iestāde.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="3a5f2-168">Norādiet iestatījumus cilnē **Savienojums**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="3a5f2-169">Iepriekš ielādētās konfigurācijas atjaunināta versija tiek ielādēta gan funkcionālajam, gan tehniskajam profilam.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="3a5f2-170">Ja atbilstošs savienotājs vai dokumentu nodrošinātājs jau tiek lietots, jums par to tiek paziņots.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="3a5f2-171">Pēc noklusējuma tiek saglabātas visas izmaiņas, kas funkcionālajā un tehniskajā profilā ir veiktas manuāli.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="3a5f2-172">Lai šos profilus pārrakstītu ar noklusējuma parametru kopu no kādas konfigurācijas, noklikšķiniet uz **Atjaunināt** lapā **Savienotāja funkcionālie profili** un lapā **Savienotāja tehniskie profili**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="3a5f2-173">Sadaļā **Retail > Kanāla iestatīšana > Finanšu integrācija > Finanšu reģistrācijas process** izveidojiet vienumu **Finanšu reģistrācijas process** katram unikālajam finanšu integrācijas procesam.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="3a5f2-174">Reģistrācijas procesu nosaka reģistrācijas darbību secība un katrā darbībā izmantotā savienotāju grupa.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="3a5f2-175">Pievienojiet procesam reģistrācijas darbības.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="3a5f2-176">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-176">Click **Add**.</span></span>
      - <span data-ttu-id="3a5f2-177">Atlasiet kādu savienotāja tipu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="3a5f2-178">Šis lauks nosaka, vai sistēma tehniskajā profilā meklē savienotāju, aparatūras profilos meklē savienotāja tipu **Lokāls** vai POS funkcionalitātes profilos meklē citus savienotāju tipus.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="3a5f2-179">Atlasiet savienotāju grupu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="3a5f2-180">Noklikšķiniet uz **Validēt**, lai pārbaudītu reģistrācijas procesa struktūras integritāti.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="3a5f2-181">Validācijas ir ieteicams veikt tālāk aprakstītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="3a5f2-182">Jaunam reģistrācijas procesam, kad ir pabeigti visi iestatījumi, tostarp saistīšana ar POS funkcionalitātes profiliem un aparatūras profiliem.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="3a5f2-183">Pēc atjauninājumu veikšanas esošam reģistrācijas procesam.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="3a5f2-184">Saistiet finanšu reģistrācijas procesus ar POS funkcionalitātes profiliem sadaļā **Retail > Kanāla iestatīšana > POS iestatīšana > POS profili > Funkcionalitātes profili**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="3a5f2-185">Noklikšķiniet uz **Rediģēt** un atlasiet vienumu **Procesa numurs** cilnē **Finanšu reģistrācijas process**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="3a5f2-186">Savienotāju tehniskos profilus saistiet ar aparatūras profiliem sadaļā **Retail > Kanāla iestatīšana > POS iestatīšana > POS profili > Aparatūras profili**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="3a5f2-187">Noklikšķiniet uz **Rediģēt** un pēc tam noklikšķiniet uz **Jauns** cilnē **Finanšu tehniskais profils**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="3a5f2-188">Atlasiet kādu savienotāja tehnisko profilu laukā **Profila numurs**.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="3a5f2-189">Vienam aparatūras profilam varat pievienot vairākus tehnisko profilus.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="3a5f2-190">Taču tas netiek atbalstīts, ja aparatūras profilam ir vairākas krustošanās ar jebkuru savienotāju grupu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="3a5f2-191">Lai nepieļautu nepareizus iestatījumus, pēc visu aparatūras profilu atjaunināšanas ir ieteicams validēt reģistrācijas procesu.</span><span class="sxs-lookup"><span data-stu-id="3a5f2-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

