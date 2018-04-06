---
title: "Organizācijas administrēšanas sākumlapa"
description: "Šajā tēmā ir norādīti resursi, kas jums palīdzēs izmantot programmatūru Microsoft Dynamics 365 for Finance and Operations savā organizācijā."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: a2c1d846527eac4db0a043c7f1c51da0e73bd796
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="organization-administration-home-page"></a><span data-ttu-id="febc4-103">Organizācijas administrēšanas sākumlapa</span><span class="sxs-lookup"><span data-stu-id="febc4-103">Organization administration home page</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="febc4-104">Šajā tēmā ir norādīts saturs, kas prasmīgiem lietotājiem un administratoriem palīdzēs konfigurēt programmatūru Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="febc4-104">This topic points to content that will help power users and administrators configure Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="febc4-105">Šis saturs viņiem palīdzēs sistēmu konfigurēt tā, lai jūsu organizācijai un komercdarbībai tā darbotos efektīvi un bez traucējumiem.</span><span class="sxs-lookup"><span data-stu-id="febc4-105">This content will help them configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="febc4-106">Liela daļa no šeit uzskaitītā satura attiecas uz līdzekļiem modulī **Organizācijas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="febc4-106">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="febc4-107">Taču ir pāris uzdevumu, piemēram, ieraksta veidņu izveidošana un lietošana, ko var veikt jebkurā modulī, lai palīdzētu jūsu organizācijai darboties efektīvāk.</span><span class="sxs-lookup"><span data-stu-id="febc4-107">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span> 

<a name="number-sequences"></a><span data-ttu-id="febc4-108">Numuru sērijas</span><span class="sxs-lookup"><span data-stu-id="febc4-108">Number sequences</span></span>
----------------
<span data-ttu-id="febc4-109">Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus identifikatorus pamatdatu ierakstiem un transakciju ierakstiem, kam ir nepieciešami identifikatori.</span><span class="sxs-lookup"><span data-stu-id="febc4-109">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="febc4-110">Pamatdatu ieraksts vai darījuma ieraksts, kam nepieciešams identifikators, tiek saukts par *atsauci*.</span><span class="sxs-lookup"><span data-stu-id="febc4-110">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="febc4-111">Pirms atsaucei varat izveidot jaunus ierakstus, ir jāiestata numuru sērija un tā jāsaista ar atsauci.</span><span class="sxs-lookup"><span data-stu-id="febc4-111">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

-   [<span data-ttu-id="febc4-112">Numuru sēriju apskats</span><span class="sxs-lookup"><span data-stu-id="febc4-112">Number sequence overview</span></span>](number-sequence-overview.md)
-   <span data-ttu-id="febc4-113">[Numuru sēriju iestatīšana, izmantojot vedni](tasks/set-up-number-sequences-wizard.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="febc4-113">[Set up number sequences by using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
-   <span data-ttu-id="febc4-114">[Atsevišķu numuru sēriju iestatīšana](tasks/set-up-number-sequences-individual-basis.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="febc4-114">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="febc4-115">Organizācijas</span><span class="sxs-lookup"><span data-stu-id="febc4-115">Organizations</span></span>
<span data-ttu-id="febc4-116">Organizācija ir cilvēku grupa, kas strādā kopā, lai nodrošinātu biznesa procesu vai sasniegtu mērķi.</span><span class="sxs-lookup"><span data-stu-id="febc4-116">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="febc4-117">Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="febc4-117">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="febc4-118">Pirms organizāciju un organizāciju hierarhiju iestatīšanas programmatūrā Finance and Operations noteikti izplānojiet sava uzņēmuma modelēšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="febc4-118">Before you set up organizations and organization hierarchies in Finance and Operations, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="febc4-119">Organizācijas modelis būtiski ietekmē Finance and Operations ieviešanu un biznesa procesus.</span><span class="sxs-lookup"><span data-stu-id="febc4-119">The organization model has a significant effect on the implementation of Finance and Operations and on business processes.</span></span>

-   [<span data-ttu-id="febc4-120">Organizācijas un organizāciju hierarhijas</span><span class="sxs-lookup"><span data-stu-id="febc4-120">Organizations and organizational hierarchies</span></span>](organizations-organizational-hierarchies.md)
-   [<span data-ttu-id="febc4-121">Organizācijas hierarhijas plānošana</span><span class="sxs-lookup"><span data-stu-id="febc4-121">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
-   <span data-ttu-id="febc4-122">[Organizācijas hierarhijas izveide](tasks/create-organization-hierarchy.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="febc4-122">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
-   <span data-ttu-id="febc4-123">[Juridiskas personas izveide](tasks/create-legal-entity.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="febc4-123">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
-   <span data-ttu-id="febc4-124">[Pārvaldības struktūrvienības izveide](tasks/create-operating-unit.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="febc4-124">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="febc4-125">Adrešu grāmatas</span><span class="sxs-lookup"><span data-stu-id="febc4-125">Address books</span></span>
<span data-ttu-id="febc4-126">Globālā adrešu grāmata ir centralizēts repozitorijs pamatdatiem, kas jāglabā par visām iekšējām un ārējām personām un organizācijām, ar kurām uzņēmums mijiedarbojas.</span><span class="sxs-lookup"><span data-stu-id="febc4-126">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="febc4-127">Ar pušu ierakstiem saistītie dati ietver personas nosaukumu/vārdu un uzvārdu, adresi un kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="febc4-127">The data that is associated with party records includes the party's name, address, and contact information.</span></span> 

<span data-ttu-id="febc4-128">Pēc globālās adrešu grāmatas izveidošanas pēc nepieciešamības varat izveidot papildu adrešu grāmatas, piemēram, atsevišķu adrešu grāmatu katram uzņēmumam jūsu organizācijā vai katrai biznesa jomai.</span><span class="sxs-lookup"><span data-stu-id="febc4-128">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> 

-   [<span data-ttu-id="febc4-129">Globālā adrešu grāmata</span><span class="sxs-lookup"><span data-stu-id="febc4-129">Global address book</span></span>](overview-global-address-book.md)
-   [<span data-ttu-id="febc4-130">Globālās adrešu grāmatas un papildu adrešu grāmatu konfigurācijas plānošana</span><span class="sxs-lookup"><span data-stu-id="febc4-130">Plan how to configure the global address book and additional address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="febc4-131">Globālās adrešu grāmatas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="febc4-131">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
-   [<span data-ttu-id="febc4-132">Bieži uzdotie jautājumi par adrešu grāmatām</span><span class="sxs-lookup"><span data-stu-id="febc4-132">Address books FAQ</span></span>](qa-address-books.md)


## <a name="workflow"></a><span data-ttu-id="febc4-133">Darbplūsma</span><span class="sxs-lookup"><span data-stu-id="febc4-133">Workflow</span></span>
<span data-ttu-id="febc4-134">Darbplūsma ir sistēma, kas tiek instalēta ar programmatūru Finance and Operations, un to jūs var izmantot, lai izveidotu atsevišķas darbplūsmas vai biznesa procesus.</span><span class="sxs-lookup"><span data-stu-id="febc4-134">Workflow is a system that is installed with Finance and Operations that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="febc4-135">Kad izveidojat darbplūsmu, jūs norādāt veidu, kā dokuments plūst jeb pārvietojas caur sistēmu, norādot, kam ir jāizpilda uzdevums, jāpieņem lēmums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="febc4-135">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> 

-   [<span data-ttu-id="febc4-136">Darbplūsmas pārskats</span><span class="sxs-lookup"><span data-stu-id="febc4-136">Workflow overview</span></span>](overview-workflow-system.md)
-   [<span data-ttu-id="febc4-137">Darbplūsmas elementi</span><span class="sxs-lookup"><span data-stu-id="febc4-137">Workflow elements</span></span>](workflow-elements.md)
-   [<span data-ttu-id="febc4-138">Darbplūsmas darbības</span><span class="sxs-lookup"><span data-stu-id="febc4-138">Workflow actions</span></span>](workflow-actions.md)
-   [<span data-ttu-id="febc4-139">Izveidot darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="febc4-139">Create a workflow</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="febc4-140">Elektroniskie paraksti</span><span class="sxs-lookup"><span data-stu-id="febc4-140">Electronic signatures</span></span>
<span data-ttu-id="febc4-141">Elektroniskais paraksts apstiprina personas identitāti, kas gatavojas sākt vai apstiprināt skaitļošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="febc4-141">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="febc4-142">Dažās nozarēs elektroniskais paraksts ir tikpat juridiski saistošs kā ar roku veikts paraksts.</span><span class="sxs-lookup"><span data-stu-id="febc4-142">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="febc4-143">Vairākās regulētas nozarēs, piemēram, farmācijas, pārtikas un dzērienu un aviācijas un aizsardzības nozarēs, elektronisko parakstu izmantošana ir normatīva prasība.</span><span class="sxs-lookup"><span data-stu-id="febc4-143">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="febc4-144">Programmatūrā Dynamics 365 for Finance and Operations varat izmantot elektroniskos parakstus īpaši svarīgiem biznesa procesiem.</span><span class="sxs-lookup"><span data-stu-id="febc4-144">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="febc4-145">Dažiem procesiem ir iebūvētas elektronisko parakstu iespējas.</span><span class="sxs-lookup"><span data-stu-id="febc4-145">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="febc4-146">Varat arī izveidot pielāgotas parakstu prasības jebkurai datu bāzes tabulai un laukam.</span><span class="sxs-lookup"><span data-stu-id="febc4-146">You can also create custom signature requirements for any database table and field.</span></span>

-   [<span data-ttu-id="febc4-147">Elektronisko parakstu apskats</span><span class="sxs-lookup"><span data-stu-id="febc4-147">Electronic signature overview</span></span>](electronic-signature-overview.md)
-   <span data-ttu-id="febc4-148">[Elektronisko parakstu iestatīšana](tasks/set-up-electronic-signatures.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="febc4-148">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="febc4-149">Pieteikumu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="febc4-149">Case management</span></span>
<span data-ttu-id="febc4-150">Veicot gadījumu plānošanu, izsekošanu un analīzi, var izstrādāt efektīvus risinājumus, ko var izmantot līdzīgām problēmām.</span><span class="sxs-lookup"><span data-stu-id="febc4-150">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="febc4-151">Piemēram, kad klientu apkalpošanas pārstāvji vai cilvēkresursu nodaļas darbinieki veido gadījumus, zināšanu dokumentos viņi var atrast informāciju, kura viņiem palīdz efektīvāk strādāt ar gadījumiem vai tos atrisināt.</span><span class="sxs-lookup"><span data-stu-id="febc4-151">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span> 

-   [<span data-ttu-id="febc4-152">Pieteikumu pārvaldības apskats</span><span class="sxs-lookup"><span data-stu-id="febc4-152">Case management overview</span></span>](cases.md)
-   [<span data-ttu-id="febc4-153">Konfigurēt pieteikumu drošību, procesus un kategorijas</span><span class="sxs-lookup"><span data-stu-id="febc4-153">Configure case security, processes, and categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="febc4-154">Ierakstu veidnes</span><span class="sxs-lookup"><span data-stu-id="febc4-154">Record templates</span></span>
<span data-ttu-id="febc4-155">Ierakstu veidnes var jums palīdzēt izveidot ierakstus ātrāk.</span><span class="sxs-lookup"><span data-stu-id="febc4-155">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="febc4-156">Varat izveidot ierakstu veidnes, lai katram jaunajam ierakstam nevajadzētu atkārtoti ievadīt bieži izmantotās lauku vērtības.</span><span class="sxs-lookup"><span data-stu-id="febc4-156">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> 

-   [<span data-ttu-id="febc4-157">Ierakstu veidnes</span><span class="sxs-lookup"><span data-stu-id="febc4-157">Record templates</span></span>](record-templates.md)
- <span data-ttu-id="febc4-158">[Ieraksta veidnes izveidošana, lai atvieglotu datu ievadi](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="febc4-158">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="febc4-159">[Ieraksta veidnes izmantošana, lai izveidotu jaunu ierakstu](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="febc4-159">[Use a record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="febc4-160">Vispārīgā organizācijas administrēšana</span><span class="sxs-lookup"><span data-stu-id="febc4-160">General organization administration</span></span>
-   <span data-ttu-id="febc4-161">[Reklāmkaroga vai logotipa maiņa](../get-started/tasks/change-banner-or-logo.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="febc4-161">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="febc4-162">Dokumentu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="febc4-162">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="febc4-163">Konfigurēt un sūtīt e-pastu</span><span class="sxs-lookup"><span data-stu-id="febc4-163">Configure and send email</span></span>](configure-email.md)
-   [<span data-ttu-id="febc4-164">Datuma/laika dati un laika joslas</span><span class="sxs-lookup"><span data-stu-id="febc4-164">Date/time data and time zones</span></span>](date-time-zones.md)








