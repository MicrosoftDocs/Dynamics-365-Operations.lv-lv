---
title: Debitora maksājumu prognožu iespējošana (priekšskatījums)
description: Šajā tēmā paskaidrots, kā ieslēgt un konfigurēt debitora maksājumu prognozēšanas līdzekli Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222590"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="7cd50-103">Debitora maksājumu prognožu iespējošana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="7cd50-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7cd50-104">Šajā tēmā paskaidrots, kā ieslēgt un konfigurēt debitora maksājumu prognozēšanas līdzekli Finanšu ieskatos.</span><span class="sxs-lookup"><span data-stu-id="7cd50-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="7cd50-105">Ieslēdziet līdzekli darbvietā **Līdzekļu pārvaldība** un ievadiet konfigurācijas iestatījumus lapā **Finanšu ieskatu parametri**.</span><span class="sxs-lookup"><span data-stu-id="7cd50-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="7cd50-106">Šajā tēmā iekļauta arī informācija, kas var palīdzēt efektīvi izmantot līdzekli.</span><span class="sxs-lookup"><span data-stu-id="7cd50-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="7cd50-107">Pirms veicat tālāk norādītās darbības, pārliecinieties, vai ir paveiktas priekšnosacījumu darbības tēmā [Finanšu ieskatu konfigurēšana](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="7cd50-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="7cd50-108">Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi.</span><span class="sxs-lookup"><span data-stu-id="7cd50-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="7cd50-109">Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="7cd50-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="7cd50-110">(Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="7cd50-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="7cd50-111">Izlaidiet šo darbību, ja izmantojat versiju 10.0.20 vai jaunāku versiju, vai, ja izmantojat Service Fabric izvietojumu.</span><span class="sxs-lookup"><span data-stu-id="7cd50-111">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="7cd50-112">Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli.</span><span class="sxs-lookup"><span data-stu-id="7cd50-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="7cd50-113">Ja neredzat līdzekli darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, mēģinot to ieslēgt, sazinieties ar <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="7cd50-113">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span> 

2. <span data-ttu-id="7cd50-114">Ieslēdziet debitora maksājumu ieskatu līdzekli:</span><span class="sxs-lookup"><span data-stu-id="7cd50-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="7cd50-115">Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="7cd50-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="7cd50-116">Atrodiet līdzekli, kura nosaukums ir **Debitora maksājumu ieskati (priekšskatījums)**.</span><span class="sxs-lookup"><span data-stu-id="7cd50-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="7cd50-117">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="7cd50-117">Select **Enable now**.</span></span>

    <span data-ttu-id="7cd50-118">Debitora maksājumu ieskatu līdzeklis tagad ir ieslēgts un gatavs konfigurēšanai.</span><span class="sxs-lookup"><span data-stu-id="7cd50-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="7cd50-119">Konfigurējiet debitora maksājumu ieskatu līdzekli:</span><span class="sxs-lookup"><span data-stu-id="7cd50-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="7cd50-120">Doties uz **Kredīti un iekasēšana \> Iestatījumi \> Finanšu ieskati \> Finanšu ieskatu parametri**.</span><span class="sxs-lookup"><span data-stu-id="7cd50-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="7cd50-121">[![Finanšu ieskatu parametru lapa pirms līdzekļa konfigurēšanas](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="7cd50-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="7cd50-122">Lapā **Finanšu ieskatu parametri**, kas atrodas cilnē **Debitora maksājumu ieskati** atlasiet saiti **Skatīt datu laukus, kas izmantoti prognozēšanas modelī**, lai atvērtu lapu **Datu lauki prognozēšanas modelim**.</span><span class="sxs-lookup"><span data-stu-id="7cd50-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="7cd50-123">Tur varat apskatīt noklusējuma sarakstu ar laukiem, kas tiek izmantoti, lai izveidotu mākslīgā intelekta prognozēšanas modeli debitora maksājumu prognozēm.</span><span class="sxs-lookup"><span data-stu-id="7cd50-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="7cd50-124">Lai izmantotu noklusējuma lauku sarakstu un izveidotu prognozēšanas modeli, aizveriet lapu **Datu lauki prognozēšanas modelim** un pēc tam lapā **Finanšu ieskatu parametri** iestatiet opciju **Iespējot līdzekli** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7cd50-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="7cd50-125">Nosakiet darījumu periodu "ļoti novēloti", lai definētu, ko jūsu biznesam nozīmē prognozēšanas grozs **Ļoti novēloti**.</span><span class="sxs-lookup"><span data-stu-id="7cd50-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="7cd50-126">Katram atvērtajam rēķinam sistēma prognozē maksājuma iespējamību trīs grozos: **Savlaicīgi**, **Novēloti** un **Ļoti novēloti**.</span><span class="sxs-lookup"><span data-stu-id="7cd50-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="7cd50-127">**Savlaicīgi** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti darījuma termiņā vai pirms tā.</span><span class="sxs-lookup"><span data-stu-id="7cd50-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="7cd50-128">**Novēloti** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti pēc darījuma termiņa beigām, bet pirms darījuma perioda "ļoti novēloti" sākuma.</span><span class="sxs-lookup"><span data-stu-id="7cd50-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="7cd50-129">**Ļoti novēloti** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti pēc darījuma perioda "ļoti novēloti" sākuma.</span><span class="sxs-lookup"><span data-stu-id="7cd50-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7cd50-130">Ja maināt darījumu periodu "ļoti novēloti" un atlasāt **Mainīt novēlošanas slieksni** pēc tam, kad ir izveidots mākslīgā intelekta modelis debitora maksājumiem, esošais prognozēšanas modelis tiek dzēsts, un tiek izveidots jauns modelis.</span><span class="sxs-lookup"><span data-stu-id="7cd50-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="7cd50-131">Jaunais prognozēšanas modelis pārvietos darījumus uz periodu "ļoti novēloti", pamatojoties uz iestatījumiem, kas tika ievadīti, to definējot.</span><span class="sxs-lookup"><span data-stu-id="7cd50-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="7cd50-132">Pēc tam, kad esat pabeidzis definēt darījumu periodu "ļoti novēloti", atlasiet **Izveidot prognozēšanas modeli**, lai izveidotu prognozēšanas modeli.</span><span class="sxs-lookup"><span data-stu-id="7cd50-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="7cd50-133">Sadaļa **Prognozēšanas modelis** lapā **Finanšu ieskatu parametri** parāda prognozēšanas modeļa statusu.</span><span class="sxs-lookup"><span data-stu-id="7cd50-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7cd50-134">Jebkurā laikā, kamēr tiek veidots prognozēšanas modelis, varat atlasīt **Atiestatīt modeļa izveidi**, lai atiestatītu procesu.</span><span class="sxs-lookup"><span data-stu-id="7cd50-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="7cd50-135">Līdzeklis tagad ir konfigurēts un ir gatavs lietošanai.</span><span class="sxs-lookup"><span data-stu-id="7cd50-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="7cd50-136">Pēc tam, kad līdzeklis ir ieslēgts un konfigurēts, un prognozēšanas modelis ir izveidots un darbojas, sadaļā **Prognozēšanas modelis** lapā **Finanšu ieskatu parametri** redzama modeļa precizitāte, kā parādīts tālāk redzamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="7cd50-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="7cd50-137">[![Prognozēšanas modeļa precizitāte finanšu ieskatu parametru lapā](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="7cd50-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="7cd50-138">Informācija par izlaišanu</span><span class="sxs-lookup"><span data-stu-id="7cd50-138">Release details</span></span>

<span data-ttu-id="7cd50-139">Finanšu ieskatu publiskais priekšskatījums izmēģinājuma izvietošanai ir pieejams Amerikas Savienotajās Valstīs, Eiropā un Apvienotajā Karalistē.</span><span class="sxs-lookup"><span data-stu-id="7cd50-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="7cd50-140">Korporācija Microsoft pakāpeniski pievieno atbalstu citiem reģioniem.</span><span class="sxs-lookup"><span data-stu-id="7cd50-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="7cd50-141">Publiskā priekšskatījuma līdzekļus var un vajadzētu ieslēgt tikai 2. līmeņa smilškastes vidēs.</span><span class="sxs-lookup"><span data-stu-id="7cd50-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="7cd50-142">Iestatīšanas un mākslīgā intelekta modeļus, kas izveidoti smilškastes vidē, nevar migrēt uz ražošanas vidi.</span><span class="sxs-lookup"><span data-stu-id="7cd50-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="7cd50-143">Lai iegūtu papildu informāciju, skatiet rakstu [Pakalpojuma Microsoft Dynamics 365 Previews lietošanas papildu nosacījumi](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="7cd50-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
