---
title: Elektronisko pārskatu veidošanas (ER) konfigurāciju dzīves cikla pārvaldība
description: Šajā tēmā ir aprakstīts, kā pārvaldīt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurāciju Microsoft Dynamics 365 Finance risinājumam.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b1b5ac8e256835332a4c53ed2872ee609253ad9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568729"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="c205a-103">Elektronisko pārskatu veidošanas (ER) konfigurāciju dzīves cikla pārvaldība</span><span class="sxs-lookup"><span data-stu-id="c205a-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c205a-104">Šajā tēmā ir aprakstīts, kā pārvaldīt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurāciju Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c205a-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="c205a-105">Kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="c205a-105">Overview</span></span>

<span data-ttu-id="c205a-106">Elektronisko pārskatu izveide (ER) ir programma, kas nodrošina ar likumu noteikto un valstij raksturīgo elektronisko dokumentu atbalstu.</span><span class="sxs-lookup"><span data-stu-id="c205a-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="c205a-107">Kopumā ER spēj veikt šādus uzdevumus attiecībā uz vienu elektronisko dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c205a-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="c205a-108">Papildinformāciju skatiet tēmā [Pārskats par elektronisko pārskatu (EP) veidošanu](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="c205a-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="c205a-109">Izveidot elektroniskā dokumenta veidni:</span><span class="sxs-lookup"><span data-stu-id="c205a-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="c205a-110">Identificēt nepieciešamos datu avotus, ko var prezentēt šajā dokumentā:</span><span class="sxs-lookup"><span data-stu-id="c205a-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="c205a-111">Pamata dati, piemēram, datu tabulas, datu ieraksti un klases.</span><span class="sxs-lookup"><span data-stu-id="c205a-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="c205a-112">Procesam specifiskie rekvizīti, piemēram, izpildes datums un laiks, laika josla.</span><span class="sxs-lookup"><span data-stu-id="c205a-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="c205a-113">Lietotāja ievadītie parametri, ko lietotājs norāda izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="c205a-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="c205a-114">Definēt nepieciešamos dokumenta elementus un to topoloģiju, lai norādītu galīgā dokumenta formātu.</span><span class="sxs-lookup"><span data-stu-id="c205a-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="c205a-115">Konfigurēt vēlamo datu plūsmu no atlasītajiem datu avotiem definētajiem dokumenta elementiem (izmantojot datu avota saistījumus dokumenta formāta komponentiem) un norādīt procesa kontroles loģiku.</span><span class="sxs-lookup"><span data-stu-id="c205a-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="c205a-116">Padarīt veidni pieejamu, lai to varētu izmantot citās instancēs:</span><span class="sxs-lookup"><span data-stu-id="c205a-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="c205a-117">Pārveidot dokumenta veidni, kas izveidota programmā Dynamics AX, par ER konfigurāciju un eksportēt konfigurāciju no pašreizējās programmas instances kā XML pakotni, kuru var glabāt lokāli vai LCS.</span><span class="sxs-lookup"><span data-stu-id="c205a-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="c205a-118">Pārveidot ER konfigurāciju par programmas dokumenta veidni.</span><span class="sxs-lookup"><span data-stu-id="c205a-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="c205a-119">Importēt XML pakotni, kas tiek glabāta lokāli vai LCS pašreizējā instancē.</span><span class="sxs-lookup"><span data-stu-id="c205a-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="c205a-120">Pielāgot elektroniskā dokumenta veidni:</span><span class="sxs-lookup"><span data-stu-id="c205a-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="c205a-121">Pārnest veidni no LCS uz pašreizējo instanci kā ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c205a-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="c205a-122">Izveidot ER konfigurācijas pielāgotu versiju un saglabāt atsauci uz tās bāzes versiju.</span><span class="sxs-lookup"><span data-stu-id="c205a-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="c205a-123">Integrēt veidni noteiktā biznesa procesā, lai tā būtu pieejama programmā:</span><span class="sxs-lookup"><span data-stu-id="c205a-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="c205a-124">Konfigurēt iestatījumus, lai programma sāktu izmantot ER konfigurāciju, atsaucoties uz attiecīgo konfigurāciju ar procesu saistītā parametrā.</span><span class="sxs-lookup"><span data-stu-id="c205a-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="c205a-125">Piemēram, ietveriet atsauci uz ER konfigurāciju noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="c205a-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="c205a-126">Izmantot veidni noteiktā biznesa procesā:</span><span class="sxs-lookup"><span data-stu-id="c205a-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="c205a-127">Izpildīt ER konfigurāciju konkrētā biznesa procesā.</span><span class="sxs-lookup"><span data-stu-id="c205a-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="c205a-128">Piemēram, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu, ja ir atlasīta maksājumu metode ar atsauci uz ER konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c205a-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="c205a-129">Koncepcijas</span><span class="sxs-lookup"><span data-stu-id="c205a-129">Concepts</span></span>
<span data-ttu-id="c205a-130">Ar ER konfigurācijas dzīves ciklu ir saistītas tālāk norādītās lomas un saistītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c205a-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="c205a-131">Loma</span><span class="sxs-lookup"><span data-stu-id="c205a-131">Role</span></span>                                       | <span data-ttu-id="c205a-132">Aktivitātes</span><span class="sxs-lookup"><span data-stu-id="c205a-132">Activities</span></span>                                                      | <span data-ttu-id="c205a-133">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c205a-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="c205a-134">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="c205a-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="c205a-135">Izveidojiet un pārvaldiet ER komponentus (modeļus un formātus).</span><span class="sxs-lookup"><span data-stu-id="c205a-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="c205a-136">Biznesa procesos iesaistīta persona, kura izstrādā ER domēnam specifiskos datu modeļu, izstrādā nepieciešamās elektronisko dokumentu veidnes un atbilstoši tās saista.</span><span class="sxs-lookup"><span data-stu-id="c205a-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="c205a-137">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="c205a-137">Electronic reporting developer</span></span>             | <span data-ttu-id="c205a-138">Izveidojiet un pārvaldiet datu modeļu kartējumus.</span><span class="sxs-lookup"><span data-stu-id="c205a-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="c205a-139">Dynamics AX speciālists, kurš atlasa nepieciešamos Finance datu avotus un saista tos ar ER domēnam specifiskiem datu modeļiem.</span><span class="sxs-lookup"><span data-stu-id="c205a-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="c205a-140">Uzskaites supervizors</span><span class="sxs-lookup"><span data-stu-id="c205a-140">Accounting supervisor</span></span>                      | <span data-ttu-id="c205a-141">Konfigurēt ar procesu saistītos iestatījumus, kam ir atsauce uz ER artefaktiem.</span><span class="sxs-lookup"><span data-stu-id="c205a-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="c205a-142">Piemēram, loma **Uzskaites supervizors**, kas sniedz iespēju ER konfigurācijas iestatījumus izmantot noteiktā kreditoru parādu maksājumu metodē, lai ģenerētu rēķinu apstrādes elektronisko maksājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="c205a-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="c205a-143">Kreditoriem maksājamo rēķinu darbinieks</span><span class="sxs-lookup"><span data-stu-id="c205a-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="c205a-144">Izmantot ER artefaktus noteiktā biznesa procesā.</span><span class="sxs-lookup"><span data-stu-id="c205a-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="c205a-145">Piemēram, loma **Kreditoriem maksājamo rēķinu darbinieks**, kas sniedz iespēju ģenerēt rēķinu apstrādes elektroniskos maksājumu ziņojumus, pamatojoties uz ER formātu, kas ir konfigurēts noteiktai maksājumu metodei.</span><span class="sxs-lookup"><span data-stu-id="c205a-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="c205a-146">ER konfigurācijas izstrādes dzīves cikls</span><span class="sxs-lookup"><span data-stu-id="c205a-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="c205a-147">Tālāk minēto ar ER saistīto apsvērumu dēļ ER konfigurācijas ir ieteicams veidot izstrādes vidē kā atsevišķā Finance and Operations instancē:</span><span class="sxs-lookup"><span data-stu-id="c205a-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="c205a-148">Lietotāji, kam ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var rediģēt konfigurācijas un palaist tās testēšanas nolūkos.</span><span class="sxs-lookup"><span data-stu-id="c205a-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="c205a-149">Šis scenārijs var izraisīt klašu un tabulu metožu izsaukumus, kas var kaitēt biznesa datiem un instances izmantošanas veiktspējai.</span><span class="sxs-lookup"><span data-stu-id="c205a-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="c205a-150">Klašu un tabulu metožu kā ER konfigurāciju ER datu avotu izsaukumus neierobežo ieejas punkti un reģistrēts uzņēmuma saturs.</span><span class="sxs-lookup"><span data-stu-id="c205a-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="c205a-151">Tādēļ lietotāji, kuriem ir loma **Elektronisko pārskatu izstrādātājs** vai **Elektronisko pārskatu veidošanas funkcionālais konsultants**, var piekļūt konfidenciāliem uzņēmuma datiem.</span><span class="sxs-lookup"><span data-stu-id="c205a-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="c205a-152">Izstrādes vidē izstrādātās ER konfigurācijas var augšupielādēt testēšanas vidē konfigurācijas novērtēšanai (pareiza procesu integrācija, pareizi rezultāti un veiktspēja) un kvalitātes nodrošināšanai (pareizas lomu piekļuves tiesības un pienākumu sadale).</span><span class="sxs-lookup"><span data-stu-id="c205a-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="c205a-153">Šim nolūkam var izmantot ER konfigurāciju apmaiņas līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="c205a-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="c205a-154">Visbeidzot apstiprinātās ER konfigurācijas var augšupielādēt LCS, kur tās var koplietot ar pakalpojumu abonentiem, vai ražošanas vidē iekšējai lietošanai, kā tas ir redzams tālāk esošajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="c205a-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![ER konfigurācijas dzīves cikls](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="c205a-156">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c205a-156">Additional resources</span></span>

[<span data-ttu-id="c205a-157">Elektronisko ziņojumu (ER) pārskats</span><span class="sxs-lookup"><span data-stu-id="c205a-157">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]