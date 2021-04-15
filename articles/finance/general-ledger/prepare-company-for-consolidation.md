---
title: Juridiskas personas sagatavošana konsolidācijas procesam
description: Konsolidācijas procesā darījumi no vairākām juridiskās personas kontu kopām tiek apkopoti vienā juridiskās personas kontu kopā. Šajā tēmā ir paskaidrots, kā sagatavot juridisku personu konsolidēšanai.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6f718bef3b1b07d3bb03dbf6acbf1cdf58aa7b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815480"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="90143-104">Juridiskas personas sagatavošana konsolidācijas procesam</span><span class="sxs-lookup"><span data-stu-id="90143-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90143-105">Konsolidācijas procesā darījumi no vairākām juridiskās personas kontu kopām tiek apkopoti vienā juridiskās personas kontu kopā.</span><span class="sxs-lookup"><span data-stu-id="90143-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="90143-106">Šajā tēmā ir paskaidrots, kā sagatavot juridisku personu konsolidēšanai.</span><span class="sxs-lookup"><span data-stu-id="90143-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="90143-107">Ieteicams izmantot Management Reporter programmai Microsoft Dynamics 365 Finance, lai apvienotu finanšu rezultātus vairākām juridiskām personām konsolidētā formātā.</span><span class="sxs-lookup"><span data-stu-id="90143-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="90143-108">Management Reporter ļauj izveidot konsolidētus finanšu pārskatus starp juridiskajām personām, izmantot Excel, lai importētu konsolidēšanas datus no citiem avotiem, un pārvērst summas jebkurā pārskatu valūtā bez vajadzības veikt konsolidācijas procesu Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="90143-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="90143-109">Varat drukāt konsolidētās juridiskās personas pārskatus, piemēram, finanšu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="90143-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="90143-110">Tomēr konsolidēto juridisko personu nevar izmantot ikdienas darījumiem.</span><span class="sxs-lookup"><span data-stu-id="90143-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="90143-111">Varat konsolidēt datus no juridiskām personām, kuras izmanto datu bāzes, kas atšķiras no konsolidētās juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="90143-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="90143-112">Šāds konsolidācijas process tiek dēvēts par *importa konsolidāciju*.</span><span class="sxs-lookup"><span data-stu-id="90143-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="90143-113">Juridiskās personas var arī izmantot to pašu datu bāzi, ko izmanto konsolidētā juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="90143-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="90143-114">Šāds konsolidācijas process tiek dēvēts par *tiešsaistes konsolidāciju*.</span><span class="sxs-lookup"><span data-stu-id="90143-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="90143-115">Konsolidētā juridiskā persona apkopo meitasuzņēmuma rezultātus un bilances.</span><span class="sxs-lookup"><span data-stu-id="90143-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="90143-116">Lai konsolidēto juridisko personu sagatavotu konsolidācijai, izpildiet tālāk minētos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="90143-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="90143-117">Dodieties uz **Virsgrāmata \> Iestatīšana \> Organizācija \> Juridiskās personas**.</span><span class="sxs-lookup"><span data-stu-id="90143-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="90143-118">Lai izveidotu juridisku personu, kas būs konsolidētā juridiskā persona, atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="90143-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="90143-119">Atzīmējiet izvēles rūtiņu **Izmantot finanšu konsolidācijas procesam** un pēc tam ievadiet informāciju par konsolidēto juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="90143-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="90143-120">Pārliecinieties, vai ievadāt šo informāciju tieši tā, kā vēlaties to redzēt konsolidētās juridiskās personas finanšu pārskatos.</span><span class="sxs-lookup"><span data-stu-id="90143-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="90143-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90143-121">Close the page.</span></span>
5. <span data-ttu-id="90143-122">Atlasiet konsolidēto juridisko personu laukā lapas augšējā labajā stūrī un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="90143-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="90143-123">Dodieties uz **Virsgrāmata \> Iestatīšana \> Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="90143-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="90143-124">Atlasiet kontu plānus, finanšu kalendāru, uzskaites valūtu, izvēles pārskata valūtu un konsolidētās juridiskās personas noklusējuma maiņas kursa veidu.</span><span class="sxs-lookup"><span data-stu-id="90143-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="90143-125">Dodieties uz **Virsgrāmata \> Iestatīšana \> Valūta \> Valūtas maiņas kursi**.</span><span class="sxs-lookup"><span data-stu-id="90143-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="90143-126">Meitasuzņēmuma juridisko personu valūtām iestatiet valūtas maiņas kursus atbilstošajiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="90143-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="90143-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90143-127">Close the page.</span></span>
11. <span data-ttu-id="90143-128">Ja konsolidētajai juridiskajai personai ir meitasuzņēmumi, kas izmanto ārvalstu valūtas, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="90143-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="90143-129">Dodieties uz **Virsgrāmata \> Iestatīšana \> Grāmatošana \> Automātisko darījumu konti**.</span><span class="sxs-lookup"><span data-stu-id="90143-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="90143-130">Laukā **Grāmatošanas veids** atlasiet atbilstošo kontu:</span><span class="sxs-lookup"><span data-stu-id="90143-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="90143-131">Ja juridiskajai personai ir ārvalstu meitasuzņēmumi, kas finansiāli vai funkcionāli ir atkarīgi no mātes juridiskās personas, atlasiet atbilstošo kontu grāmatojuma veidam **Peļņas un zaudējumu konts konsolidācijas starpībai**.</span><span class="sxs-lookup"><span data-stu-id="90143-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="90143-132">Ja konsolidējat meitasuzņēmumu, kas finansiāli un funkcionāli ir neatkarīgs no mātes juridiskās personas, vai juridiskas personas, kurā ir ietverti rezultāti no vairākiem meitasuzņēmumiem, kas ir finansiāli un funkcionāli neatkarīgi no mātes juridiskās personas, un ja datu konsolidēšanā izmantojat pārrēķināšanas metodes, atlasiet atbilstošo kontu grāmatojuma veidam **Bilances konts konsolidācijas starpībai**.</span><span class="sxs-lookup"><span data-stu-id="90143-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="90143-133">Laukā **Galvenais konts** atlasiet galvenos kontus, kas jāizmanto ārvalstu valūtu pārvērtēšanas korekcijās.</span><span class="sxs-lookup"><span data-stu-id="90143-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="90143-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90143-134">Close the page.</span></span>

    <span data-ttu-id="90143-135">Ja konsolidēto juridisko personu izveidojāt agrāk periodā, varat pārvērtēt ārvalstu valūtu daudzumus, konsolidācijas periodā mainoties valūtu kursiem.</span><span class="sxs-lookup"><span data-stu-id="90143-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="90143-136">Periodiskajam darbam **Konsolidēt** tagad ir iestatīta konsolidētā juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="90143-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="90143-137">Varat veikt importa konsolidāciju vai tiešsaistes konsolidāciju.</span><span class="sxs-lookup"><span data-stu-id="90143-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="90143-138">Lai veiktu importa konsolidāciju, dodieties uz **Virsgrāmata \> Periodiski \> Konsolidācija \> Konsolidēt \[Importēt\]**.</span><span class="sxs-lookup"><span data-stu-id="90143-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="90143-139">Lai veiktu tiešsaistes konsolidāciju, dodieties uz **Virsgrāmata \> Periodiski \> Konsolidācija \> Konsolidēt \[Tiešsaiste\]**.</span><span class="sxs-lookup"><span data-stu-id="90143-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="90143-140">Pirms konsolidācijas apstrādāšanas meitasuzņēmumu juridiskās personas ir jāsagatavo konsolidēšanai.</span><span class="sxs-lookup"><span data-stu-id="90143-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="90143-141">Papildinformāciju skatiet sadaļā [Meitasuzņēmuma juridiskās personas konsolidācijas iestatīšana](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="90143-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]