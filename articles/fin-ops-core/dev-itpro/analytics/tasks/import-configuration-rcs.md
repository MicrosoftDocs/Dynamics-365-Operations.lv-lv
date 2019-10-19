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
ms.openlocfilehash: 32c9c17d8b63e4c0806559c2dcc2e11ae9825a53
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184627"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="fd4c6-103">(ER) Konfigurāciju importēšana no RCS</span><span class="sxs-lookup"><span data-stu-id="fd4c6-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd4c6-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var importēt jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas versiju no Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="fd4c6-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="fd4c6-105">Šajā piemērā ir jāatlasa RCS instancē konfigurētā ER konfigurācijas versija un jāimportē tā parauga uzņēmuma Litware, Inc. pašreizējā instancē. Šīs darbības var izpildīt jebkurā uzņēmumā, jo ER konfigurācijas tiek koplietotas starp uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="fd4c6-106">Lai izpildītu šīs darbības, vispirms izpildiet darbības, kas ir aprakstītas tēmā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="fd4c6-106">To complete these steps, you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="fd4c6-107">Lai veiktu šīs darbības, ir nepieciešama piekļuve arī RCS instancei, kas satur vismaz vienu ER konfigurāciju ar statusu **Pabeigts** vai **Koplietots**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="fd4c6-108">Dodieties uz **Organizācijas administrēšana** > **Darbvietas** > **Elektronisko pārskatu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="fd4c6-109">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="fd4c6-110">Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas ir aprakstītas tēmā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="fd4c6-110">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="fd4c6-111">Ja jūsu uzņēmuma nav nodrošināta neviena RCS vide, noklikšķiniet uz ārējās saites **Regulatory services — konfigurācija** un izpildiet norādījumus, lai nodrošinātu RCS vidi.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="fd4c6-112">Noklikšķiniet uz **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="fd4c6-113">Noklikšķiniet uz cilnes **RCS**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="fd4c6-114">Ja RCS vide jūsu uzņēmumam jau ir nodrošināta, izmantojiet lapās norādītos URL, lai piekļūtu tai.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="fd4c6-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="fd4c6-116">Reģistrējiet jaunu ER repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="fd4c6-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="fd4c6-118">Atlasiet pakalpojumu sniedzēju Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="fd4c6-119">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-119">Click Repositories.</span></span> 
4. <span data-ttu-id="fd4c6-120">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="fd4c6-121">Laukā Konfigurācijas repozitorija veids ievadiet "RCS".</span><span class="sxs-lookup"><span data-stu-id="fd4c6-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="fd4c6-122">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-122">Click Create repository.</span></span> 
7. <span data-ttu-id="fd4c6-123">RCS vides parādāmā nosaukuma laukā ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="fd4c6-124">Atlasiet vēlamo RCS instanci.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-124">Select the desired RCS instance.</span></span> <span data-ttu-id="fd4c6-125">Ņemiet vērā, ka tās var būt vairākas.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="fd4c6-126">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="fd4c6-127">ER konfigurāciju importēšana no RCS repozitorija</span><span class="sxs-lookup"><span data-stu-id="fd4c6-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="fd4c6-128">Noklikšķiniet uz **Rādīt filtrus**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="fd4c6-129">Laukā **Nosaukums** ievadiet “RCS” filtra vērtību, izmantojot filtra operatoru **sākas ar**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="fd4c6-130">Atverot atlasīto repozitoriju, lapā **Izveidot savienojumu ar Regulatory Configuration Services** noklikšķiniet uz saites **Noklikšķiniet šeit, lai izveidotu savienojumu ar Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="fd4c6-131">Noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-131">Click **Open**.</span></span> 
5. <span data-ttu-id="fd4c6-132">Noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-132">Click **Close**.</span></span> 
6. <span data-ttu-id="fd4c6-133">Atlasiet nepieciešamo ER konfigurācijas versiju un noklikšķiniet uz **Importēt**, lai ievietotu to pašreizējā instancē.</span><span class="sxs-lookup"><span data-stu-id="fd4c6-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>

