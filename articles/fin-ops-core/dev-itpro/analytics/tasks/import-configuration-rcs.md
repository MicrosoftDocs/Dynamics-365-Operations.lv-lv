---
title: (ER) Konfigurāciju importēšana no RCS
description: Šajā tēmā ir sniegta informācija par to, kā lietotājs var importēt jaunu ER konfigurācijas versiju no RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
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
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55d548a97a2f93bffeb5aa4b0ce6b0c4ca5f8819
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769836"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="39c00-103">(ER) Konfigurāciju importēšana no RCS</span><span class="sxs-lookup"><span data-stu-id="39c00-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39c00-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="39c00-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="39c00-105">Šajā piemērā ir jāatlasa RCS instancē konfigurētā ER konfigurācijas versija un jāimportē tā parauga uzņēmuma Litware, Inc. pašreizējā instancē. Šīs darbības var izpildīt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas starp uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="39c00-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="39c00-106">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas ir aprakstītas tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="39c00-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="39c00-107">Lai veiktu šīs darbības, ir nepieciešama piekļuve arī RCS instancei, kas satur vismaz vienu ER konfigurāciju ar statusu **Pabeigts** vai **Koplietots**.</span><span class="sxs-lookup"><span data-stu-id="39c00-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="39c00-108">Dodieties uz **Organizācijas administrēšana** > **Darbvietas** > **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="39c00-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="39c00-109">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="39c00-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="39c00-110">Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="39c00-110">If you don’t see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="39c00-111">Ja jūsu uzņēmuma nav nodrošināta neviena RCS vide, noklikšķiniet uz ārējās saites **Regulatory services — konfigurācija** un izpildiet norādījumus, lai nodrošinātu RCS vidi.</span><span class="sxs-lookup"><span data-stu-id="39c00-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="39c00-112">Noklikšķiniet uz **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="39c00-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="39c00-113">Noklikšķiniet uz cilnes **RCS**.</span><span class="sxs-lookup"><span data-stu-id="39c00-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="39c00-114">Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapās norādītos URL, lai piekļūtu tai.</span><span class="sxs-lookup"><span data-stu-id="39c00-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="39c00-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="39c00-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="39c00-116">Reģistrējiet jaunu ER repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="39c00-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="39c00-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="39c00-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="39c00-118">Atlasiet pakalpojumu sniedzēju Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="39c00-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="39c00-119">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="39c00-119">Click Repositories.</span></span> 
4. <span data-ttu-id="39c00-120">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="39c00-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="39c00-121">Laukā Konfigurācijas repozitorija veids ievadiet "RCS".</span><span class="sxs-lookup"><span data-stu-id="39c00-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="39c00-122">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="39c00-122">Click Create repository.</span></span> 
7. <span data-ttu-id="39c00-123">RCS vides parādāmā nosaukuma laukā ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="39c00-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="39c00-124">Atlasiet vēlamo RCS instanci.</span><span class="sxs-lookup"><span data-stu-id="39c00-124">Select the desired RCS instance.</span></span> <span data-ttu-id="39c00-125">Ņemiet vērā, ka tās var būt vairākas.</span><span class="sxs-lookup"><span data-stu-id="39c00-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="39c00-126">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="39c00-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="39c00-127">ER konfigurāciju importēšana no RCS repozitorija</span><span class="sxs-lookup"><span data-stu-id="39c00-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="39c00-128">Noklikšķiniet uz **Rādīt filtrus**.</span><span class="sxs-lookup"><span data-stu-id="39c00-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="39c00-129">Laukā **Nosaukums** ievadiet “RCS” filtra vērtību, izmantojot filtra operatoru **sākas ar**.</span><span class="sxs-lookup"><span data-stu-id="39c00-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="39c00-130">Atverot atlasīto repozitoriju, lapā **Izveidot savienojumu ar Regulatory Configuration Services** noklikšķiniet uz saites **Noklikšķiniet šeit, lai izveidotu savienojumu ar Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="39c00-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="39c00-131">Noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="39c00-131">Click **Open**.</span></span> 
5. <span data-ttu-id="39c00-132">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="39c00-132">Click **Close**.</span></span> 
6. <span data-ttu-id="39c00-133">Atlasiet nepieciešamo ER konfigurācijas versiju un noklikšķiniet uz **Importēt**, lai ievietotu to pašreizējā instancē.</span><span class="sxs-lookup"><span data-stu-id="39c00-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>

