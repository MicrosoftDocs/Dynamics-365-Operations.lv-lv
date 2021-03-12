---
title: Organizācijas administrēšanas sākumlapa
description: Šajā tēmā ir norādīti resursi, kas jums palīdzēs jūsu organizācijā.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b91963b9ccb5fb339b3c0fc41e8483628135c4c8
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797027"
---
# <a name="organization-administration-home-page"></a><span data-ttu-id="5978f-103">Organizācijas administrēšanas sākumlapa</span><span class="sxs-lookup"><span data-stu-id="5978f-103">Organization administration home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5978f-104">Šajā tēmā ir norādīts saturs, kas palīdzēs pilnvarot lietotājus un administratorus, lai viņi sistēmu konfigurētu tā, ka jūsu organizācijai un komercdarbībai tā darbotos efektīvi un bez traucējumiem.</span><span class="sxs-lookup"><span data-stu-id="5978f-104">This topic points to content that will help power users and administrators configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="5978f-105">Liela daļa no šeit uzskaitītā satura attiecas uz līdzekļiem modulī **Organizācijas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="5978f-105">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="5978f-106">Taču ir pāris uzdevumu, piemēram, ieraksta veidņu izveidošana un lietošana, ko var veikt jebkurā modulī, lai palīdzētu jūsu organizācijai darboties efektīvāk.</span><span class="sxs-lookup"><span data-stu-id="5978f-106">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span>

## <a name="number-sequences"></a><span data-ttu-id="5978f-107">Numuru sērijas</span><span class="sxs-lookup"><span data-stu-id="5978f-107">Number sequences</span></span>

<span data-ttu-id="5978f-108">Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus identifikatorus pamatdatu ierakstiem un transakciju ierakstiem, kam ir nepieciešami identifikatori.</span><span class="sxs-lookup"><span data-stu-id="5978f-108">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="5978f-109">Pamatdatu ieraksts vai darījuma ieraksts, kam nepieciešams identifikators, tiek saukts par *atsauci*.</span><span class="sxs-lookup"><span data-stu-id="5978f-109">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="5978f-110">Pirms atsaucei varat izveidot jaunus ierakstus, ir jāiestata numuru sērija un tā jāsaista ar atsauci.</span><span class="sxs-lookup"><span data-stu-id="5978f-110">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

- [<span data-ttu-id="5978f-111">Pārskats par numuru sērijām</span><span class="sxs-lookup"><span data-stu-id="5978f-111">Number sequences overview</span></span>](number-sequence-overview.md)
- <span data-ttu-id="5978f-112">[Numuru sēriju iestatīšana, izmantojot vedni](tasks/set-up-number-sequences-wizard.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="5978f-112">[Set up number sequences using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
- <span data-ttu-id="5978f-113">[Atsevišķu numuru sēriju iestatīšana](tasks/set-up-number-sequences-individual-basis.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="5978f-113">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="5978f-114">Organizācijas</span><span class="sxs-lookup"><span data-stu-id="5978f-114">Organizations</span></span>

<span data-ttu-id="5978f-115">Organizācija ir cilvēku grupa, kas strādā kopā, lai nodrošinātu biznesa procesu vai sasniegtu mērķi.</span><span class="sxs-lookup"><span data-stu-id="5978f-115">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="5978f-116">Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="5978f-116">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="5978f-117">Pirms organizāciju un organizāciju hierarhiju iestatīšanas noteikti plānojiet uzņēmuma modelēšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="5978f-117">Before you set up organizations and organization hierarchies, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="5978f-118">Organizācijas modelim ir nozīmīga ietekme uz īstenošanu un biznesa procesiem.</span><span class="sxs-lookup"><span data-stu-id="5978f-118">The organization model has a significant effect on implementation and business processes.</span></span>

- [<span data-ttu-id="5978f-119">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="5978f-119">Organizations and organizational hierarchies overview</span></span>](organizations-organizational-hierarchies.md)
- [<span data-ttu-id="5978f-120">Organizācijas hierarhijas plānošana</span><span class="sxs-lookup"><span data-stu-id="5978f-120">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
- <span data-ttu-id="5978f-121">[Organizācijas hierarhijas izveide](tasks/create-organization-hierarchy.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="5978f-121">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
- <span data-ttu-id="5978f-122">[Juridiskas personas izveide](tasks/create-legal-entity.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="5978f-122">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
- <span data-ttu-id="5978f-123">[Pārvaldības struktūrvienības izveide](tasks/create-operating-unit.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="5978f-123">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="5978f-124">Adrešu grāmatas</span><span class="sxs-lookup"><span data-stu-id="5978f-124">Address books</span></span>

<span data-ttu-id="5978f-125">Globālā adrešu grāmata ir centralizēts repozitorijs pamatdatiem, kas jāglabā par visām iekšējām un ārējām personām un organizācijām, ar kurām uzņēmums mijiedarbojas.</span><span class="sxs-lookup"><span data-stu-id="5978f-125">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="5978f-126">Ar pušu ierakstiem saistītie dati ietver personas nosaukumu/vārdu un uzvārdu, adresi un kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="5978f-126">The data that is associated with party records includes the party's name, address, and contact information.</span></span>

<span data-ttu-id="5978f-127">Pēc globālās adrešu grāmatas izveidošanas pēc nepieciešamības varat izveidot papildu adrešu grāmatas, piemēram, atsevišķu adrešu grāmatu katram uzņēmumam jūsu organizācijā vai katrai biznesa jomai.</span><span class="sxs-lookup"><span data-stu-id="5978f-127">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span>

- [<span data-ttu-id="5978f-128">Pārskats par globālo adrešu grāmatu</span><span class="sxs-lookup"><span data-stu-id="5978f-128">Global address book overview</span></span>](overview-global-address-book.md)
- [<span data-ttu-id="5978f-129">Plāns globālajai adrešu grāmatai un citām adrešu grāmatām</span><span class="sxs-lookup"><span data-stu-id="5978f-129">Plan for the global address book and other address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="5978f-130">Globālās adrešu grāmatas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5978f-130">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
- [<span data-ttu-id="5978f-131">Bieži uzdotie jautājumi par adrešu grāmatām</span><span class="sxs-lookup"><span data-stu-id="5978f-131">Address books FAQ</span></span>](qa-address-books.md)

## <a name="workflow"></a><span data-ttu-id="5978f-132">Darbplūsma</span><span class="sxs-lookup"><span data-stu-id="5978f-132">Workflow</span></span>

<span data-ttu-id="5978f-133">Darbplūsma ir sistēma, kuru jūs varat izmantot, lai izveidotu individuālas darbplūsmas vai biznesa procesus.</span><span class="sxs-lookup"><span data-stu-id="5978f-133">Workflow is a system that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="5978f-134">Kad izveidojat darbplūsmu, jūs norādāt veidu, kā dokuments plūst jeb pārvietojas caur sistēmu, norādot, kam ir jāizpilda uzdevums, jāpieņem lēmums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="5978f-134">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span>

- [<span data-ttu-id="5978f-135">Darbplūsmu sistēmas apskats</span><span class="sxs-lookup"><span data-stu-id="5978f-135">Workflow system overview</span></span>](overview-workflow-system.md)
- [<span data-ttu-id="5978f-136">Darbplūsmas elementi</span><span class="sxs-lookup"><span data-stu-id="5978f-136">Workflow elements</span></span>](workflow-elements.md)
- [<span data-ttu-id="5978f-137">Darbības darbplūsmas apstiprināšanas procesos</span><span class="sxs-lookup"><span data-stu-id="5978f-137">Actions in workflow approval processes</span></span>](workflow-actions.md)
- [<span data-ttu-id="5978f-138">Izveidot darbplūsmu pārskatu</span><span class="sxs-lookup"><span data-stu-id="5978f-138">Create workflows overview</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="5978f-139">Elektroniskie paraksti</span><span class="sxs-lookup"><span data-stu-id="5978f-139">Electronic signatures</span></span>

<span data-ttu-id="5978f-140">Elektroniskais paraksts apstiprina personas identitāti, kas gatavojas sākt vai apstiprināt skaitļošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="5978f-140">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="5978f-141">Dažās nozarēs elektroniskais paraksts ir tikpat juridiski saistošs kā ar roku veikts paraksts.</span><span class="sxs-lookup"><span data-stu-id="5978f-141">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="5978f-142">Vairākās regulētas nozarēs, piemēram, farmācijas, pārtikas un dzērienu un aviācijas un aizsardzības nozarēs, elektronisko parakstu izmantošana ir normatīva prasība.</span><span class="sxs-lookup"><span data-stu-id="5978f-142">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="5978f-143">Būtiskiem biznesa procesiem varat izmantot elektroniskos parakstus.</span><span class="sxs-lookup"><span data-stu-id="5978f-143">You can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="5978f-144">Dažiem procesiem ir iebūvētas elektronisko parakstu iespējas.</span><span class="sxs-lookup"><span data-stu-id="5978f-144">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="5978f-145">Varat arī izveidot pielāgotas parakstu prasības jebkurai datu bāzes tabulai un laukam.</span><span class="sxs-lookup"><span data-stu-id="5978f-145">You can also create custom signature requirements for any database table and field.</span></span>

- [<span data-ttu-id="5978f-146">Elektronisko parakstu pārskats</span><span class="sxs-lookup"><span data-stu-id="5978f-146">Electronic signatures overview</span></span>](electronic-signature-overview.md)
- <span data-ttu-id="5978f-147">[Elektronisko parakstu iestatīšana](tasks/set-up-electronic-signatures.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="5978f-147">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="5978f-148">Pieteikumu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="5978f-148">Case management</span></span>

<span data-ttu-id="5978f-149">Veicot gadījumu plānošanu, izsekošanu un analīzi, var izstrādāt efektīvus risinājumus, ko var izmantot līdzīgām problēmām.</span><span class="sxs-lookup"><span data-stu-id="5978f-149">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="5978f-150">Piemēram, kad klientu apkalpošanas pārstāvji vai cilvēkresursu nodaļas darbinieki veido gadījumus, zināšanu dokumentos viņi var atrast informāciju, kura viņiem palīdz efektīvāk strādāt ar gadījumiem vai tos atrisināt.</span><span class="sxs-lookup"><span data-stu-id="5978f-150">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span>

- [<span data-ttu-id="5978f-151">Pārskats par pieteikumu pārvaldību</span><span class="sxs-lookup"><span data-stu-id="5978f-151">Case management overview</span></span>](cases.md)
- [<span data-ttu-id="5978f-152">Pieteikumu kategorijas drošības, pieteikumu procesu un pieteikumu kategoriju plānošana</span><span class="sxs-lookup"><span data-stu-id="5978f-152">Plan case category security, case processes, and case categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="5978f-153">Ierakstu veidnes</span><span class="sxs-lookup"><span data-stu-id="5978f-153">Record templates</span></span>

<span data-ttu-id="5978f-154">Ierakstu veidnes var jums palīdzēt izveidot ierakstus ātrāk.</span><span class="sxs-lookup"><span data-stu-id="5978f-154">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="5978f-155">Varat izveidot ierakstu veidnes, lai katram jaunajam ierakstam nevajadzētu atkārtoti ievadīt bieži izmantotās lauku vērtības.</span><span class="sxs-lookup"><span data-stu-id="5978f-155">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span>

- [<span data-ttu-id="5978f-156">Ierakstu veidņu pārskats</span><span class="sxs-lookup"><span data-stu-id="5978f-156">Record templates overview</span></span>](record-templates.md)
- <span data-ttu-id="5978f-157">[Ieraksta veidnes izveidošana, lai atvieglotu datu ievadi](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="5978f-157">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="5978f-158">[Ieraksta veidnes izmantošana, lai izveidotu jaunu ierakstu](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="5978f-158">[Use record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="5978f-159">Vispārīgā organizācijas administrēšana</span><span class="sxs-lookup"><span data-stu-id="5978f-159">General organization administration</span></span>

- <span data-ttu-id="5978f-160">[Reklāmkaroga vai logotipa maiņa](../get-started/tasks/change-banner-or-logo.md) (uzdevuma ceļvedis)</span><span class="sxs-lookup"><span data-stu-id="5978f-160">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="5978f-161">Dokumentu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5978f-161">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="5978f-162">Konfigurēt un sūtīt e-pastu</span><span class="sxs-lookup"><span data-stu-id="5978f-162">Configure and send email</span></span>](configure-email.md)
- [<span data-ttu-id="5978f-163">Datuma/laika dati un laika joslas</span><span class="sxs-lookup"><span data-stu-id="5978f-163">Date/time data and time zones</span></span>](date-time-zones.md)
