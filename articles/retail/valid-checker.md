---
title: Mazumtirdzniecības transakciju konsekvences pārbaudītājs
description: Šajā tēmā ir aprakstīta mazumtirdzniecības transakciju konsekvences pārbaudītāja funkcionalitāte programmā Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "302595"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="c533a-103">Mazumtirdzniecības transakciju konsekvences pārbaudītājs</span><span class="sxs-lookup"><span data-stu-id="c533a-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="c533a-104">Šajā tēmā ir aprakstīta mazumtirdzniecības transakciju konsekvences pārbaudītāja funkcionalitāte, kas ir ieviesta Microsoft Dynamics 365 for Finance and Operations versijā 8.1.3.</span><span class="sxs-lookup"><span data-stu-id="c533a-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="c533a-105">Konsekvences pārbaudītājs identificē un izolē nekonsekventas transakcijas, pirms tās ir uzņemtas pārskatu grāmatošanas procesā.</span><span class="sxs-lookup"><span data-stu-id="c533a-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="c533a-106">Kad pārskats tiek grāmatots programmā Retail, grāmatošana var būt nesekmīga, jo mazumtirdzniecības transakciju tabulās pastāv nekonsekventi dati.</span><span class="sxs-lookup"><span data-stu-id="c533a-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="c533a-107">Šādu datu problēmu var būt izraisījušas neparedzētas problēmas pārdošanas punkta (point of sale — POS) programmā, kā arī tādas var rasties, ja transakcijas tika nepareizi importētas no trešās puses POS sistēmām.</span><span class="sxs-lookup"><span data-stu-id="c533a-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="c533a-108">Tālāk ir uzskaitīti daži no šādas nekonsekvences potenciālās rašanās piemēriem.</span><span class="sxs-lookup"><span data-stu-id="c533a-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="c533a-109">Transakcijas kopsumma virsraksta tabulā neatbilst transakcijas kopsummai rindās.</span><span class="sxs-lookup"><span data-stu-id="c533a-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="c533a-110">Rindu skaits virsraksta tabulā neatbilst rindu skaitam transakcijas tabulā.</span><span class="sxs-lookup"><span data-stu-id="c533a-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="c533a-111">Nodokļi virsraksta tabulā neatbilst nodokļu summai rindās.</span><span class="sxs-lookup"><span data-stu-id="c533a-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="c533a-112">Kad pārskatu grāmatošanas process uzņem nekonsekventas transakcijas, tiek izveidoti nekonsekventi pārdošanas rēķini un maksājumu žurnāli, līdz ar to viss pārskata grāmatošanas process ir nesekmīgs.</span><span class="sxs-lookup"><span data-stu-id="c533a-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="c533a-113">Lai atkoptu pārskatus no šāda stāvokļa, ir jāizmanto sarežģīti datu labojumi vairākās transakciju tabulās.</span><span class="sxs-lookup"><span data-stu-id="c533a-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="c533a-114">Mazumtirdzniecības transakciju konsekvences pārbaudītājs neļauj šādu problēmu rašanos.</span><span class="sxs-lookup"><span data-stu-id="c533a-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="c533a-115">Nākamajā diagrammā ir parādīts grāmatošanas process ar transakciju konsekvences pārbaudītāju.</span><span class="sxs-lookup"><span data-stu-id="c533a-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="c533a-116">![Pārskatu grāmatošanas process ar mazumtirdzniecības transakciju konsistences pārbaudītāju](./media/validchecker.png "Pārskatu grāmatošanas process ar mazumtirdzniecības transakciju konsistences pārbaudītāju")</span><span class="sxs-lookup"><span data-stu-id="c533a-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transsaction consistency checker")</span></span>

<span data-ttu-id="c533a-117">Pakešuzdevums **Validēt veikala transakcijas** pārbauda mazumtirdzniecības transakciju tabulu konsekvenci tālāk norādītajos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="c533a-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="c533a-118">Debitora konts — pārliecinās, vai HQ debitoru pamatdatu mazumtirdzniecības transakciju tabulās pastāv attiecīgais debitora konts.</span><span class="sxs-lookup"><span data-stu-id="c533a-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="c533a-119">Rindu skaits — pārliecinās, vai transakciju virsrakstu tabulā norādītais rindu skaits atbilst rindu skaitam pārdošanas transakciju tabulās.</span><span class="sxs-lookup"><span data-stu-id="c533a-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="c533a-120">Konsekvences pārbaudītāja iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c533a-120">Set up the consistency checker</span></span>
<span data-ttu-id="c533a-121">Konfigurējiet pakešuzdevumu “Validēt veikala transakcijas” regulārai izpildīšanai sadaļā **Mazumtirdzniecība \> Mazumtirdzniecības IT \> POS grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="c533a-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="c533a-122">Pakešuzdevumu var plānot atkarībā no veikala organizācijas hierarhijas, līdzīgi kā tiek iestatīti procesi “Aprēķināt pārskatu partijā” un “Grāmatot pārskatu partijā”.</span><span class="sxs-lookup"><span data-stu-id="c533a-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="c533a-123">Iesakām šo pakešuzdevumu konfigurēt tā, lai dienas laikā tas tiktu izpildīts vairākas reizes, un to ieplānot tā, lai tas tiktu izpildīts katras P darba izpildes beigās.</span><span class="sxs-lookup"><span data-stu-id="c533a-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="c533a-124">Validēšanas procesa rezultāti</span><span class="sxs-lookup"><span data-stu-id="c533a-124">Results of validation process</span></span>
<span data-ttu-id="c533a-125">Šī pakešuzdevuma validēšanas pārbaudes rezultāti tiek atzīmēti atbilstošajā mazumtirdzniecības transakcijā.</span><span class="sxs-lookup"><span data-stu-id="c533a-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="c533a-126">Lauks **Validācijas statuss** mazumtirdzniecības transakcijas ierakstā ir iestatīts uz **Sekmīgs** vai **Kļūda**, un pēdējās validēšanas izpildes datums ir redzams laukā **Pēdējās validēšanas laiks**.</span><span class="sxs-lookup"><span data-stu-id="c533a-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="c533a-127">Lai redzētu aprakstošāku kļūdas tekstu saistībā ar validēšanas kļūmi, atlasiet attiecīgo mazumtirdzniecības veikala transakcijas ierakstu un noklikšķiniet uz pogas **Validācijas kļūdas**.</span><span class="sxs-lookup"><span data-stu-id="c533a-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="c533a-128">Uz pārskatiem netiek nogādātas transakcijas, kam validācijas pārbaude ir nesekmīga, un transakcijas, kas vēl nav validētas.</span><span class="sxs-lookup"><span data-stu-id="c533a-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="c533a-129">Procesa “Aprēķināt pārskatu” laikā lietotājiem tiek ziņots, vai pastāv transakcijas, kas varēja tikt ietvertas pārskatā, bet netika tajā ietvertas.</span><span class="sxs-lookup"><span data-stu-id="c533a-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="c533a-130">Ja tiek atrasta kāda validācijas kļūda, vienīgais veids, kā šo kļūdu novērst, ir sazināties ar Microsoft atbalsta dienestu.</span><span class="sxs-lookup"><span data-stu-id="c533a-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="c533a-131">Turpmākajos laidienos tiks pievienota iespēja lietotājiem izlabot nesekmīgos ierakstus, izmantojot lietotāja interfeisu.</span><span class="sxs-lookup"><span data-stu-id="c533a-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="c533a-132">Kļūs pieejamas arī reģistrēšanas un auditēšanas iespējas, lai izsekotu modifikāciju vēsturi.</span><span class="sxs-lookup"><span data-stu-id="c533a-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="c533a-133">Kādā no turpmākajiem laidieniem tiks pievienotas papildu validēšanas kārtulas, lai atbalstītu vairāk scenāriju.</span><span class="sxs-lookup"><span data-stu-id="c533a-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
