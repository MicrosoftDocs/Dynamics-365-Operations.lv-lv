---
title: Grāmatošanas definīcijas
description: Šajā rakstā ir sniegta informācija par grāmatošanas definīcijām un veidu, kā tās definēt un saistīt. Lai uzskaites ierakstos klasificētu galvenos kontus un finanšu dimensijas, atbalstītajiem grāmatošanas veidiem un dokumentiem var izmantot grāmatošanas definīcijas nevis grāmatošanas metodes.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e9d1e593f58e8fc9e12ddac7664b6e67ecda6a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561018"
---
# <a name="posting-definitions"></a><span data-ttu-id="41f69-104">Grāmatošanas definīcijas</span><span class="sxs-lookup"><span data-stu-id="41f69-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41f69-105">Šajā rakstā ir sniegta informācija par grāmatošanas definīcijām un veidu, kā tās definēt un saistīt.</span><span class="sxs-lookup"><span data-stu-id="41f69-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="41f69-106">Lai uzskaites ierakstos klasificētu galvenos kontus un finanšu dimensijas, atbalstītajiem grāmatošanas veidiem un dokumentiem var izmantot grāmatošanas definīcijas nevis grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="41f69-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="41f69-107">Lai uzskaites ierakstos klasificētu galvenos kontus un finanšu dimensijas, atbalstītajiem grāmatošanas veidiem un dokumentiem var izmantot grāmatošanas definīcijas nevis grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="41f69-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="41f69-108">Atbalstītos dokumentus un grāmatošanas veidus varat skatīt lapā **Transakcijas grāmatošanas definīcijas**.</span><span class="sxs-lookup"><span data-stu-id="41f69-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="41f69-109">Lai sāktu lietot grāmatošanas definīcijas, atlasiet opciju**Izmantot grāmatošanas definīcijas** lapā **Virsgrāmatas parametri**.</span><span class="sxs-lookup"><span data-stu-id="41f69-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="41f69-110">Pat ja izmantojat grāmatošanas definīcijas, vienalga ir jādefinē sākotnējo ierakstu grāmatošanas metodes un neatbalstītie grāmatošanas veidi un dokumenti.</span><span class="sxs-lookup"><span data-stu-id="41f69-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="41f69-111">Lai pirkšanas pasūtījumiem iespējotu apgrūtinājumu uzskaiti un pirkšanas pieprasījumiem iespējotu apgrūtinājumu bez juridiskām saistībām uzskaiti, izmantotjiet grāmatošanas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="41f69-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="41f69-112">Grāmatošanas definīciju definēšana</span><span class="sxs-lookup"><span data-stu-id="41f69-112">Defining posting definitions</span></span>
<span data-ttu-id="41f69-113">Izmantojiet lapu**Grāmatošanas definīcijas**, lai norādītu atbilstības kritērijus un definētu ierakstus, kas ir jāģenerē rodoties atbilstībai.</span><span class="sxs-lookup"><span data-stu-id="41f69-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="41f69-114">Atbilstības kritēriji tiek novērtēti sākotnējiem ierakstiem kā uzskaites sadalēm.</span><span class="sxs-lookup"><span data-stu-id="41f69-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="41f69-115">Lapā **Grāmatošanas definīcijas** var arī piešķirt prioritātes numurus ierakstu rindām, lai kontrolētu secību, kādā rindas tiek novērtētas.</span><span class="sxs-lookup"><span data-stu-id="41f69-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="41f69-116">Rindas, kurām ir zemāks prioritātes numurs, tiek novērtētas vispirms.</span><span class="sxs-lookup"><span data-stu-id="41f69-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="41f69-117">Piemēram, tiek novērtētas visas rindas, kam ir prioritātes numurs 1, pēc tam rindas, kam ir prioritātes numurs 2, un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="41f69-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="41f69-118">Ja konstatēta atbilstība, citi atbilstības kritēriji tiek ignorēti.</span><span class="sxs-lookup"><span data-stu-id="41f69-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="41f69-119">Turklāt, tikai sākotnējai transakcijai atbilstošās grupas kritēriji rada ģenerētos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="41f69-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="41f69-120">Varat pārbaudīt grāmatošanas definīcijas, izmantojot vedni **Grāmatošanas definīcijas pārbaude**.</span><span class="sxs-lookup"><span data-stu-id="41f69-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="41f69-121">Kad ir definēts grāmatošanas definīcijas parauga sākotnējais ieraksts, redzēsit ģenerētos ierakstus.</span><span class="sxs-lookup"><span data-stu-id="41f69-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="41f69-122">Varat izmantot grāmatošanas definīcijas versijas kopā ar spēkā stāšanās datumiem.</span><span class="sxs-lookup"><span data-stu-id="41f69-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="41f69-123">Piemēram, varat izveidot nākamo grāmatošanas definīcijas versiju, lai jaunajā finanšu gadā grāmatotu citā virsgrāmatas kontā.</span><span class="sxs-lookup"><span data-stu-id="41f69-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="41f69-124">Izmantojiet lapu **Transakcijas grāmatošanas definīcijas**, lai grāmatošanas definīcijas piešķirtu darbību veidiem.</span><span class="sxs-lookup"><span data-stu-id="41f69-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="41f69-125">Grāmatošanas definīciju piesaiste</span><span class="sxs-lookup"><span data-stu-id="41f69-125">Linking posting definitions</span></span>
<span data-ttu-id="41f69-126">Piesaisti var veikt no vienas grāmatošanas definīcijas citā, veidojot grāmatošanas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="41f69-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="41f69-127">Pēc tam piesaistītās definīcijas kritēriji tiek ņemti vērā papildus pašreizējās grāmatošanas definīcijas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="41f69-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="41f69-128">Šis līdzeklis palīdz ietaupīt laiku, jo pašreizējai grāmatošanas definīcijai kritēriji nav atkārtoti jāievada kopsavilkuma cilnē **Ieraksti** lapā **Grāmatošanas definīcijas**, ja šīs rindas jau ievadījāt citā definīcijā.</span><span class="sxs-lookup"><span data-stu-id="41f69-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="41f69-129">Diagrammās vai tabulās ietveriet visas saites, ko jūs varētu izmantot.</span><span class="sxs-lookup"><span data-stu-id="41f69-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="41f69-130">Lai izvairītos no konfliktiem ar pašreizējo grāmatošanas definīciju, pārliecinieties, vai visās grāmatošanas definīcijās, kam veicat piesaisti, rindas ir unikālas.</span><span class="sxs-lookup"><span data-stu-id="41f69-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="41f69-131">Veidojot saites grāmatošanas definīcijās, tiek lietoti šādi ierobežojumi:</span><span class="sxs-lookup"><span data-stu-id="41f69-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="41f69-132">norādītajā grāmatošanas definīcijā var būt ietverta saite uz citu grāmatošanas definīciju vai uz to var būt izveidota saite citā grāmatošanas definīcijā, bet vienlaicīgi ne abas saites.</span><span class="sxs-lookup"><span data-stu-id="41f69-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="41f69-133">Tomēr grāmatošanas definīcijā var ietvert saiti uz vairākām grāmatošanas definīcijām;</span><span class="sxs-lookup"><span data-stu-id="41f69-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="41f69-134">varat iestatīt saites tikai starp tām grāmatošanas definīcijām, kas atrodas vienā modulī;</span><span class="sxs-lookup"><span data-stu-id="41f69-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="41f69-135">grāmatošanas definīciju var piešķirt jebkuram transakcijas veidam, bet šim transakcijas veidam jābūt tajā pašā modulī, kur ir grāmatošanas definīcija.</span><span class="sxs-lookup"><span data-stu-id="41f69-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="41f69-136">Izmantojiet lapu **Darījuma grāmatošanas definīcijas**, lai redzētu, kurā modulī ir transakcijas veids.</span><span class="sxs-lookup"><span data-stu-id="41f69-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="41f69-137">Papildinformāciju skatiet tēmā [Grāmatošanas definīciju piemēri](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="41f69-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 


