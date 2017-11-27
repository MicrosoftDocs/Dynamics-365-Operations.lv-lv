---
title: "Audita ierobežojuma nosacījumu pārkāpumi un gadījumi"
description: "Rakstā ir paskaidrots, kā no audita ierobežojumu nosacījumu pārkāpumiem tiek ģenerēti audita gadījumi. Tajā ir iekļauta arī informācija par dažādiem veidiem, kā audita ierobežojumi izmanto dokumentu atlases datumu diapazonu."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2376a1d6e86eba9f5021cc08dcfaea52f131a3d7
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="9dcb4-104">Audita ierobežojuma nosacījumu pārkāpumi un gadījumi</span><span class="sxs-lookup"><span data-stu-id="9dcb4-104">Audit policy violations and cases</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9dcb4-105">Rakstā ir paskaidrots, kā no audita ierobežojumu nosacījumu pārkāpumiem tiek ģenerēti audita gadījumi.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="9dcb4-106">Tajā ir iekļauta arī informācija par dažādiem veidiem, kā audita ierobežojumi izmanto dokumentu atlases datumu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="9dcb4-107">Audita gadījumu ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="9dcb4-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="9dcb4-108">Audita politikas tiek izmantotas, lai identificētu izdevumu pārskatus, pirkšanas pasūtījumus un kreditoru rēķinus, kas neatbilst biznesa kārtulām, ko definē un konfigurē atbilstoši audita ierobežojuma nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="9dcb4-109">Audita ierobežojumi tiek palaisti pakešveida režīmā.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="9dcb4-110">Palaižot audita ierobežojumu, visi ierobežojuma nosacījumi, kas ir ietverti konkrētajā ierobežojumā, tiek palaisti vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="9dcb4-111">Visi ierobežojuma nosacījumi novērtē dokumentu kopu.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="9dcb4-112">Ierobežojuma nosacījums atlasa dokumentus, kas atrodas dokumentu atlases datumu diapazonā un atbilst norādītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="9dcb4-113">Piemēram, viens ierobežojuma nosacījums var atlasīt izdevumu pārskatus, kur ir ietvertas maltītes, kuru vērtība pārsniedz 50,00.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="9dcb4-114">Cits ierobežojuma nosacījums var atlasīt kreditora rēķinus, kas ir jāsamaksā noteiktam kreditoram.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="9dcb4-115">Visiem dokumentiem, kas kopā tiek atlasīti, tiek ģenerēts pārkāpums.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="9dcb4-116">Šis pārkāpums ir ieraksts par to, ka noteikts dokuments, piemēram, rēķins Nr. 12345, neatbilst ierobežojuma nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="9dcb4-117">Vairāki ierobežojuma nosacījumu ieraksti tiek grupēti un saistīti ar audita gadījumiem.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="9dcb4-118">Pēc noklusējuma katra audita ierobežojuma gadījumi tiek grupēti pēc audita ierobežojuma nosacījuma.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="9dcb4-119">Varat arī atlasīt citu grupēšanas kritēriju, izmantojot lapu **Gadījumu grupēšanas kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="9dcb4-120">Piemēram, izdevumu virsrakstus varat grupēt pēc projekta ID, savukārt kreditora rēķinus — pēc kreditora konta.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="9dcb4-121">Šajā gadījumā visi izdevumu virsraksta pārkāpumi, kam ir vienāds projekta ID, tiks grupēti vienā gadījumā, savukārt visi kreditora rēķini, kuriem ir vienāds kreditora konts, tiks grupēti tajā pašā gadījumā.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="9dcb4-122">Audita ierobežojuma nosacījumiem, kuru pamatā ir vaicājuma tips **Dublikāts**, pārkāpumi netiek grupēti pēc ierobežojuma nosacījuma vai pēc kritērijiem, kas norādīti lapā **Gadījumu grupēšanas kritēriji**.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="9dcb4-123">Tā vietā tie tiek grupēti pēc noklusējuma audita ierobežojuma nosacījumu kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="9dcb4-124">Piemēram, ja ierobežojuma nosacījums novērtē, vai izdevumu pārskatos ir izdevumu dublikāti ar vienādu summu, tirgotāja ID un datumu, visi izdevumi, kam šajos laukos ir vienādas vērtības, būs viens gadījums.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="9dcb4-125">Visis izdevumi, kam ir atšķirīgas vērtības, būs atsevišķs gadījums.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="9dcb4-126">Pēc audita gadījumu ģenerēšanas tie tiek apstrādāti, izmantojot standarta lietu pārvaldības procesus.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="9dcb4-127">Dokumentu atlases datumu diapazoni</span><span class="sxs-lookup"><span data-stu-id="9dcb4-127">Document selection date ranges</span></span>
<span data-ttu-id="9dcb4-128">Palaižot audita ierobežojumu, visi ierobežojuma nosacījumi atlasa norādītā veida dokumentu ar datumu, kas atrodas dokumentu atlases datumu diapazonā.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="9dcb4-129">Dokumentu atlases datumu diapazons tiek norādīts lapā **Papildu opcijas**.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="9dcb4-130">Daudziem dokumentiem ir piesaistīti vairāki datumi.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="9dcb4-131">Datuma lauks, ko izmanto audita ierobežojuma nosacījums, tiek norādīts lapā **Ierobežojuma nosacījumu tips**.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="9dcb4-132">Tālāk ir minēti daži citi veidi, kā audita ierobežojums izmanto dokumentu atlases datumu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="9dcb4-133">Ierobežojums izmanto katra ierobežojuma nosacījuma versiju, kas ir spēkā dokumenta atlases datumu diapazona pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="9dcb4-134">Visu ierobežojuma nosacījumu spēkā stāšanās datumus varat skatīt saraksta lapā **Audita ierobežojumi**.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="9dcb4-135">Ierobežojums izmanto organizācijas mezglus, kas ir saistīti ar ierobežojumu, pēdējā dokumentu atlases datumu diapazona dienā.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="9dcb4-136">Saraksta lapā **Audita ierobežojumi** tiek rādīti tikai tie organizācijas mezgli, kas pašlaik ir saistīti ar ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="9dcb4-137">Saistībā ar ierobežojuma nosacījumiem, kuru pamatā ir vaicājuma veids **Meklēšana sarakstā**, ierobežojums novērtē to uzraudzīto elementu dokumentus, kas ir spēkā dokumentu atlases datumu diapazona pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="9dcb4-138">Plašāku informāciju skatiet rakstā [Audita ierobežojuma nosacījumi](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="9dcb4-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>




