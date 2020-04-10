---
title: Programmas metadatu sagatavošana lietošanai ar RCS
description: Šīs tēmas darbībās ir paskaidrots, kā lietotājs var izveidot jaunu elektronisko pārskatu (Electronic reporting — ER) konfigurāciju, kas ietver programmas metadatus ER modeļa kartēšanas konfigurāciju veidošanai pakalpojumā Regulatory Configuration Service (RCS).
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d091cd835cfcb7164f83259b69e3bc1d7c09dc4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143158"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="2eb0a-103">Programmas metadatu sagatavošana lietošanai ar RCS</span><span class="sxs-lookup"><span data-stu-id="2eb0a-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2eb0a-104">Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var izveidot jaunu elektronisko pārskatu (Electronic reporting — ER) konfigurāciju, kurā ir programmas metadati ER modeļa kartēšanas konfigurāciju veidošanai pakalpojumā Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="2eb0a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="2eb0a-105">Šī konfigurācija tiks izmantota, lai izstrādātu parauga ER modeļa kartēšanas konfigurāciju, kura ir paredzēta piekļūšanai ārējās tirdzniecības transakcijām.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="2eb0a-106">Šajā piemērā tiek izveidota konfigurācija parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="2eb0a-107">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas ir aprakstītas tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2eb0a-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2eb0a-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="2eb0a-108">Prerequisites</span></span>
1.    <span data-ttu-id="2eb0a-109">Dodieties uz **Organizācijas administrēšana** > **Darbvietas** > **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="2eb0a-110">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="2eb0a-111">Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2eb0a-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="2eb0a-112">Noklikšķiniet uz **Metadatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="2eb0a-113">Pieņemsim, ka pakalpojums RCS tiks izmantots, lai izveidotu ER risinājumu kādai Finance and Operation programmai, kas ģenerēs elektroniskus dokumentus, kuros ir informācija no ārējās tirdzniecības uzņēmējdarbības jomas.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="2eb0a-114">Lai norādītu kartēšanu starp ER datu modeli un nepieciešamo datu avotiem, pakalpojumā RCS mums ir nepieciešama piekļuve Finance and Operation programmas metadatiem.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="2eb0a-115">Tādēļ ER risinājuma veidošanas gaitā mums ir jākonfigurē jauna ER metadatu konfigurācija, kas ietver visus metadatus, kuri pašlaik ir nepieciešami ER pārskatu veidošanai atlasītajai uzņēmējdarbības jomai.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="2eb0a-116">Metadatu konfigurācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="2eb0a-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="2eb0a-117">Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="2eb0a-118">Laukā **Nosaukums** ierakstiet “Ārējās tirdzniecības metadati”.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="2eb0a-119">Noklikšķiniet uz **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="2eb0a-120">Noklikšķiniet uz **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="2eb0a-121">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2eb0a-122">Varat atlasīt visus metadatus visai programmai vai atlasītajiem modeļiem, vai atlasītajiem moduļiem.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="2eb0a-123">Ņemiet vērā, ka tādā gadījumā automātiski tiks pievienoti šādi metadati: ierakstu tabulas, uzskaitījumi un paplašinātie datu tipi.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="2eb0a-124">Ja ir nepieciešami papildu metadatu tipi, tie ir jāpievieno manuāli.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="2eb0a-125">Mums ir daži ar ārējās tirdzniecības transakcijām saistīti metadati, kuri tika iegūti, atlasot metadatu vienumus manuāli.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="2eb0a-126">Noklikšķiniet uz **Pievienot datu avotu**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="2eb0a-127">Noklikšķiniet uz **Tabulas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="2eb0a-128">Izmantojiet ātro filtru, lai filtrētu pēc lauka **Nosaukums** ar vērtību “Intrastat”.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="2eb0a-129">Atlasiet **Intrastat** tabulas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="2eb0a-130">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-130">Click **OK**.</span></span>
  
<span data-ttu-id="2eb0a-131">Mēs pievienojām metadatu informāciju par Intrastat ierakstu tabulu.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="2eb0a-132">Koka struktūrā izvērsiet zaru **Tabulas ieraksti Intrastat**\>**Relācijas**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="2eb0a-133">Koka struktūrā atlasiet **Tabulas ieraksti Intrastat**\>**Relācijas\IntrastatCommodity (Tabulas ieraksti EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="2eb0a-134">Noklikšķiniet uz **Pievienot metadatus**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2eb0a-135">Metadati par nepieciešamajām relācijām atlasītajai ierakstu tabulai ir jāpievieno manuāli.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="2eb0a-136">Noklikšķiniet uz **Pievienot datu avotu**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="2eb0a-137">Noklikšķiniet uz **Uzskaitījums**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="2eb0a-138">Izmantojiet ātro filtru, lai filtrētu pēc lauka **Nosaukums** ar vērtību “IntrastatDirection”.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="2eb0a-139">Atlasiet uzskaitījuma ierakstu **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="2eb0a-140">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="2eb0a-141">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="2eb0a-142">Aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="2eb0a-143">Metadatu konfigurācijas melnraksta versijas pabeigšana</span><span class="sxs-lookup"><span data-stu-id="2eb0a-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="2eb0a-144">Noklikšķiniet uz **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="2eb0a-145">Noklikšķiniet uz **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="2eb0a-146">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="2eb0a-147">Atlasiet **1**. pabeigto versiju.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="2eb0a-148">Pabeigtās metadatu konfigurācijas versijas eksportēšana no programmas XML faila veidā</span><span class="sxs-lookup"><span data-stu-id="2eb0a-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="2eb0a-149">Noklikšķiniet uz **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="2eb0a-150">Noklikšķiniet uz **Eksportēt kā XML failu**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="2eb0a-151">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-151">Click **OK**.</span></span> 
    
<span data-ttu-id="2eb0a-152">Izveidotā ER metadatu konfigurācija ir saglabāta kā XML fails, kuru var importēt pakalpojumā RCS un izmantot kā avotu informācijai par metadatiem ārējās tirdzniecības uzņēmējdarbības jomai.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="2eb0a-153">Balstoties uz šo informāciju, mēs varam norādīt kartējumu starp programmas metadatiem un ER datu modeli.</span><span class="sxs-lookup"><span data-stu-id="2eb0a-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
