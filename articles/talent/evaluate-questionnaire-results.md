---
title: Anketu rezultātu skatīšana un novērtēšana
description: Šajā tēmā ir skaidrots, kā varat skatīt un novērtēt respondentu aizpildīto anketu rezultātus.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 38b694b6dd4b1b9a198452e409bd64d7934b4685
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "859671"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a><span data-ttu-id="d4e35-103">Anketu rezultātu skatīšana un novērtēšana</span><span class="sxs-lookup"><span data-stu-id="d4e35-103">View and evaluate the results of questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4e35-104">Šajā tēmā ir skaidrots, kā varat skatīt un novērtēt respondentu aizpildīto anketu rezultātus.</span><span class="sxs-lookup"><span data-stu-id="d4e35-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="d4e35-105">Kad respondenti ir izpildījuši anketu, anketas rezultātus varat skatīt un novērtēt vairākos veidos:</span><span class="sxs-lookup"><span data-stu-id="d4e35-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="d4e35-106">**Pabeigtās atbilžu sesijas** — skatiet detalizētu informāciju par anketām, ko respondenti ir aizpildījuši, un ģenerējiet atskaites, lai apkopotu atbildes un jebkādus iegūtos punktu.</span><span class="sxs-lookup"><span data-stu-id="d4e35-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="d4e35-107">**Rezultātu grupas** — skatiet informāciju par anketu rezultātu grupām un statistiku.</span><span class="sxs-lookup"><span data-stu-id="d4e35-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="d4e35-108">Rezultātu grupu statistiku var ģenerēt vienai anketas atbilžu sesijai vai visām atbilžu sesijām.</span><span class="sxs-lookup"><span data-stu-id="d4e35-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="d4e35-109">**Anketu statistika** — norādiet kritērijus, lai aprēķinātu statistiku attiecībā uz noteiktu respondentu grupu.</span><span class="sxs-lookup"><span data-stu-id="d4e35-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="d4e35-110">Varat arī veidot dažādas atskaites, lai skatītu rezultātus, kas ir sakārtoti pēc personas, atbilžu sesijas vai rezultātu grupas.</span><span class="sxs-lookup"><span data-stu-id="d4e35-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="d4e35-111">Ir pieejamas tālāk norādītās atskaites, kas ir saistītas ar aizpildītajām anketām.</span><span class="sxs-lookup"><span data-stu-id="d4e35-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="d4e35-112">Atbildes</span><span class="sxs-lookup"><span data-stu-id="d4e35-112">Answers</span></span>
-   <span data-ttu-id="d4e35-113">Atbildes pa anketām</span><span class="sxs-lookup"><span data-stu-id="d4e35-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="d4e35-114">Atbildes pa personām</span><span class="sxs-lookup"><span data-stu-id="d4e35-114">Answers per person</span></span>
-   <span data-ttu-id="d4e35-115">Atsauksmju analīze</span><span class="sxs-lookup"><span data-stu-id="d4e35-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="d4e35-116">Atbilžu sesijas rezultāti</span><span class="sxs-lookup"><span data-stu-id="d4e35-116">Answer session results</span></span>
<span data-ttu-id="d4e35-117">Kad respondenti ir aizpildījuši kādu anketu, varat skatīt aizpildīto atbilžu sesiju rezultātus.</span><span class="sxs-lookup"><span data-stu-id="d4e35-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="d4e35-118">Atbilžu sesija ir viena lietotāja atbildes uz anketas jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="d4e35-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="d4e35-119">Detalizētu informāciju par aizpildītajām atbilžu sesijām varat skatīt lapā **Atbildes**.</span><span class="sxs-lookup"><span data-stu-id="d4e35-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="d4e35-120">Atbilžu sesijas, kas ir iekļautas lapā **Atbildes**, tiek dažādi filtrētas atkarībā no veida, kādā atverat šo lapu:</span><span class="sxs-lookup"><span data-stu-id="d4e35-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="d4e35-121">Visas anketas</span><span class="sxs-lookup"><span data-stu-id="d4e35-121">All questionnaires</span></span>
-   <span data-ttu-id="d4e35-122">Noteikta anketa</span><span class="sxs-lookup"><span data-stu-id="d4e35-122">A specific questionnaire</span></span>
-   <span data-ttu-id="d4e35-123">Noteikta persona</span><span class="sxs-lookup"><span data-stu-id="d4e35-123">A specific person</span></span>

<span data-ttu-id="d4e35-124">Lapā **Atbildes** varat skatīt detalizētu informāciju par atbildēm, iegūto punktu skaitu, respondenta atbildēm katrā rezultātu grupā, kā arī jautājumu hierarhiju, kas tika izmantota atlasītajā anketā, ja tika izmantota jautājumu hierarhija.</span><span class="sxs-lookup"><span data-stu-id="d4e35-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="d4e35-125">Var arī ģenerēt un drukāt šādas atskaites:</span><span class="sxs-lookup"><span data-stu-id="d4e35-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="d4e35-126">**Rezultātu atskaite** — šajā atskaitē tiek rādīts grafisks attēlojums par nopelnīto punktu skaitu katrai rezultātu grupai atlasītajai atbilžu sesijai.</span><span class="sxs-lookup"><span data-stu-id="d4e35-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="d4e35-127">**Atbilžu atskaite** — šajā atskaitē tiek rādītas atbildes, ko respondents atlasīja katram anketas jautājumam.</span><span class="sxs-lookup"><span data-stu-id="d4e35-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="d4e35-128">**Nepareizās atbildes** — šajā atskaitē tiek rādīta informācija, kas ir saistīta ar respondenta atlasītajām nepareizajām atbildēm.</span><span class="sxs-lookup"><span data-stu-id="d4e35-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="d4e35-129">**Piezīme.** Atskaite **Rezultāti** ir pieejama tikai tad, ja anketai lietojat rezultātu grupas un ja lapā **Anketas** atlasījāt vienumu **Rezultātu lapa**.</span><span class="sxs-lookup"><span data-stu-id="d4e35-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="d4e35-130">Atskaite **Atbilde** un atskaite **Nepareizās atbildes** ir pieejamas tikai tad, ja lapā **Anketas** atlasījāt vienumu **Atbilžu atskaite**.</span><span class="sxs-lookup"><span data-stu-id="d4e35-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="d4e35-131">Anketu statistika</span><span class="sxs-lookup"><span data-stu-id="d4e35-131">Questionnaire statistics</span></span>
<span data-ttu-id="d4e35-132">Anketu statistiku varat izmantot, lai analizētu aizpildīto anketu rezultātus, pamatojoties uz jūsu definētajiem aprēķiniem.</span><span class="sxs-lookup"><span data-stu-id="d4e35-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="d4e35-133">Lai definētu aprēķinus, jums ir jāizpilda šādi uzdevumi:</span><span class="sxs-lookup"><span data-stu-id="d4e35-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="d4e35-134">Atlasiet kritēriju statistikas aprēķināšanai un parādīšanai.</span><span class="sxs-lookup"><span data-stu-id="d4e35-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="d4e35-135">Statistisko informāciju varat rādīt pēc anketas, jautājuma, jautājumu rindām vai rezultātu grupām.</span><span class="sxs-lookup"><span data-stu-id="d4e35-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="d4e35-136">Atlasiet diagrammas tipu, kas tiks izmantots rezultātu skatīšanai.</span><span class="sxs-lookup"><span data-stu-id="d4e35-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="d4e35-137">Atlasiet personu tipus no tīkla, piemēram, darbiniekus, kontaktpersonas vai kandidātus, par kuriem iekļaut atbildes.</span><span class="sxs-lookup"><span data-stu-id="d4e35-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="d4e35-138">Varat arī iekļaut atbildes no anketām, kas tika aizpildītas anonīmi.</span><span class="sxs-lookup"><span data-stu-id="d4e35-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="d4e35-139">Lai analizētu rezultātus, iestatiet intervālus, kuru pamatā ir vecums vai stāžs.</span><span class="sxs-lookup"><span data-stu-id="d4e35-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="d4e35-140">Atlasiet vai apstipriniet iestatījumus, kas precizē statistiskās informācijas objektu.</span><span class="sxs-lookup"><span data-stu-id="d4e35-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="d4e35-141">Piemēram, atlasot vienumu Pasta indekss, varat analizēt rezultātus visiem respondentiem, kas atrodas konkrētā ģeogrāfiskajā apgabalā.</span><span class="sxs-lookup"><span data-stu-id="d4e35-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="d4e35-142">Atlasiet vai apstipriniet kritērijus, lai rezultātus analizētu pēc respondenta vai anketas īpašībām.</span><span class="sxs-lookup"><span data-stu-id="d4e35-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="d4e35-143">Piemēram, atlasot vienumu **Pasta indekss**, varat analizēt korelāciju starp respondenta atrašanās vietu un pareizajām atbildēm.</span><span class="sxs-lookup"><span data-stu-id="d4e35-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="d4e35-144">Jūsu definētie iestatījumi tiek saglabāti, un tos var izmantot periodiskai rezultātu pārrēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="d4e35-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="additional-resources"></a><span data-ttu-id="d4e35-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d4e35-145">Additional resources</span></span>
--------

[<span data-ttu-id="d4e35-146">Anketu veidošana</span><span class="sxs-lookup"><span data-stu-id="d4e35-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="d4e35-147">Anketu lietošana</span><span class="sxs-lookup"><span data-stu-id="d4e35-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="d4e35-148">Anketu izplatīšana un aizpildīšana</span><span class="sxs-lookup"><span data-stu-id="d4e35-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)

