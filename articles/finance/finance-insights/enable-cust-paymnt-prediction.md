---
title: Debitora maksājumu prognožu iespējošana (priekšskatījums)
description: Šajā tēmā paskaidrots, kā ieslēgt un konfigurēt debitora maksājumu prognozēšanas līdzekli Finanšu ieskatos.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 584c1af5f9252a4b8c88a8866a64184bd0595b2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009422"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="a694b-103">Debitora maksājumu prognožu iespējošana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="a694b-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a694b-104">Šajā tēmā paskaidrots, kā ieslēgt un konfigurēt debitora maksājumu prognozēšanas līdzekli Finanšu ieskatos.</span><span class="sxs-lookup"><span data-stu-id="a694b-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="a694b-105">Ieslēdziet līdzekli darbvietā **Līdzekļu pārvaldība** un ievadiet konfigurācijas iestatījumus lapā **Finanšu ieskatu parametri**.</span><span class="sxs-lookup"><span data-stu-id="a694b-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="a694b-106">Šajā tēmā iekļauta arī informācija, kas var palīdzēt efektīvi izmantot līdzekli.</span><span class="sxs-lookup"><span data-stu-id="a694b-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="a694b-107">Pirms veicat tālāk norādītās darbības, pārliecinieties, vai ir paveiktas priekšnosacījumu darbības tēmā [Finanšu ieskatu konfigurēšana](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="a694b-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="a694b-108">Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi.</span><span class="sxs-lookup"><span data-stu-id="a694b-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="a694b-109">Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="a694b-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="a694b-110">(Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="a694b-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="a694b-111">Ja jūsu Microsoft Dynamics 365 Finance izvietošana ir Service Fabric izvietošana, varat izlaist šo darbību.</span><span class="sxs-lookup"><span data-stu-id="a694b-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="a694b-112">Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli.</span><span class="sxs-lookup"><span data-stu-id="a694b-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="a694b-113">Ja neredzat līdzekli darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, mēģinot to ieslēgt, sazinieties ar <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="a694b-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="a694b-114">Ieslēdziet debitora maksājumu ieskatu līdzekli:</span><span class="sxs-lookup"><span data-stu-id="a694b-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="a694b-115">Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="a694b-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="a694b-116">Atrodiet līdzekli, kura nosaukums ir **Debitora maksājumu ieskati (priekšskatījums)**.</span><span class="sxs-lookup"><span data-stu-id="a694b-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="a694b-117">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="a694b-117">Select **Enable now**.</span></span>

    <span data-ttu-id="a694b-118">Debitora maksājumu ieskatu līdzeklis tagad ir ieslēgts un gatavs konfigurēšanai.</span><span class="sxs-lookup"><span data-stu-id="a694b-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="a694b-119">Konfigurējiet debitora maksājumu ieskatu līdzekli:</span><span class="sxs-lookup"><span data-stu-id="a694b-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="a694b-120">Doties uz **Kredīti un iekasēšana \> Iestatījumi \> Finanšu ieskati \> Finanšu ieskatu parametri**.</span><span class="sxs-lookup"><span data-stu-id="a694b-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="a694b-121">[![Finanšu ieskatu parametru lapa pirms līdzekļa konfigurēšanas](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="a694b-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="a694b-122">Lapā **Finanšu ieskatu parametri**, kas atrodas cilnē **Debitora maksājumu ieskati** atlasiet saiti **Skatīt datu laukus, kas izmantoti prognozēšanas modelī**, lai atvērtu lapu **Datu lauki prognozēšanas modelim**.</span><span class="sxs-lookup"><span data-stu-id="a694b-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="a694b-123">Tur varat apskatīt noklusējuma sarakstu ar laukiem, kas tiek izmantoti, lai izveidotu mākslīgā intelekta prognozēšanas modeli debitora maksājumu prognozēm.</span><span class="sxs-lookup"><span data-stu-id="a694b-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="a694b-124">Lai izmantotu noklusējuma lauku sarakstu un izveidotu prognozēšanas modeli, aizveriet lapu **Datu lauki prognozēšanas modelim** un pēc tam lapā **Finanšu ieskatu parametri** iestatiet opciju **Iespējot līdzekli** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="a694b-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="a694b-125">Nosakiet darījumu periodu "ļoti novēloti", lai definētu, ko jūsu biznesam nozīmē prognozēšanas grozs **Ļoti novēloti**.</span><span class="sxs-lookup"><span data-stu-id="a694b-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="a694b-126">Katram atvērtajam rēķinam sistēma prognozē maksājuma iespējamību trīs grozos: **Savlaicīgi**, **Novēloti** un **Ļoti novēloti**.</span><span class="sxs-lookup"><span data-stu-id="a694b-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="a694b-127">**Savlaicīgi** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti darījuma termiņā vai pirms tā.</span><span class="sxs-lookup"><span data-stu-id="a694b-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="a694b-128">**Novēloti** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti pēc darījuma termiņa beigām, bet pirms darījuma perioda "ļoti novēloti" sākuma.</span><span class="sxs-lookup"><span data-stu-id="a694b-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="a694b-129">**Ļoti novēloti** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti pēc darījuma perioda "ļoti novēloti" sākuma.</span><span class="sxs-lookup"><span data-stu-id="a694b-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a694b-130">Ja maināt darījumu periodu "ļoti novēloti" un atlasāt **Mainīt novēlošanas slieksni** pēc tam, kad ir izveidots mākslīgā intelekta modelis debitora maksājumiem, esošais prognozēšanas modelis tiek dzēsts, un tiek izveidots jauns modelis.</span><span class="sxs-lookup"><span data-stu-id="a694b-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="a694b-131">Jaunais prognozēšanas modelis pārvietos darījumus uz periodu "ļoti novēloti", pamatojoties uz iestatījumiem, kas tika ievadīti, to definējot.</span><span class="sxs-lookup"><span data-stu-id="a694b-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="a694b-132">Pēc tam, kad esat pabeidzis definēt darījumu periodu "ļoti novēloti", atlasiet **Izveidot prognozēšanas modeli**, lai izveidotu prognozēšanas modeli.</span><span class="sxs-lookup"><span data-stu-id="a694b-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="a694b-133">Sadaļa **Prognozēšanas modelis** lapā **Finanšu ieskatu parametri** parāda prognozēšanas modeļa statusu.</span><span class="sxs-lookup"><span data-stu-id="a694b-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a694b-134">Jebkurā laikā, kamēr tiek veidots prognozēšanas modelis, varat atlasīt **Atiestatīt modeļa izveidi**, lai atiestatītu procesu.</span><span class="sxs-lookup"><span data-stu-id="a694b-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="a694b-135">Līdzeklis tagad ir konfigurēts un ir gatavs lietošanai.</span><span class="sxs-lookup"><span data-stu-id="a694b-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="a694b-136">Pēc tam, kad līdzeklis ir ieslēgts un konfigurēts, un prognozēšanas modelis ir izveidots un darbojas, sadaļā **Prognozēšanas modelis** lapā **Finanšu ieskatu parametri** redzama modeļa precizitāte, kā parādīts tālāk redzamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="a694b-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="a694b-137">[![Prognozēšanas modeļa precizitāte finanšu ieskatu parametru lapā](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="a694b-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="a694b-138">Informācija par izlaišanu</span><span class="sxs-lookup"><span data-stu-id="a694b-138">Release details</span></span>

<span data-ttu-id="a694b-139">Finanšu ieskatu publiskais priekšskatījums izmēģinājuma izvietošanai ir pieejams Amerikas Savienotajās Valstīs, Eiropā un Apvienotajā Karalistē.</span><span class="sxs-lookup"><span data-stu-id="a694b-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="a694b-140">Korporācija Microsoft pakāpeniski pievieno atbalstu citiem reģioniem.</span><span class="sxs-lookup"><span data-stu-id="a694b-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="a694b-141">Publiskā priekšskatījuma līdzekļus var un vajadzētu ieslēgt tikai 2. līmeņa smilškastes vidēs.</span><span class="sxs-lookup"><span data-stu-id="a694b-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="a694b-142">Iestatīšanas un mākslīgā intelekta modeļus, kas izveidoti smilškastes vidē, nevar migrēt uz ražošanas vidi.</span><span class="sxs-lookup"><span data-stu-id="a694b-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="a694b-143">Lai iegūtu papildu informāciju, skatiet rakstu [Microsoft Dynamics 365 Previews lietošanas papildu nosacījumi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="a694b-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="a694b-144">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="a694b-144">Privacy notice</span></span>

<span data-ttu-id="a694b-145">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="a694b-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
