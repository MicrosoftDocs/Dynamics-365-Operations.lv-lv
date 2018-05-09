---
title: "Datu importēšana no Excel datu elementu veidnēm ar vairākām darblapām"
description: "Šajā tēmā ir aprakstīts, kā importēt datus programmā Microsoft Dynamics 365 for Finance and Operations, izmantojot Excel datu elementu veidnes."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cfaf17a8279026bf9bc8b581afd07e4fdbd3f03a
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="excel-templates-with-multiple-worksheets"></a><span data-ttu-id="a7274-103">Excel veidnes ar vairākām darblapām</span><span class="sxs-lookup"><span data-stu-id="a7274-103">Excel templates with multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7274-104">Datu pārvaldība programmā Microsoft Dynamics 365 for Finance and Operations atbalsta ar programmu Microsoft Excel saistītas datu elementu veidnes.</span><span class="sxs-lookup"><span data-stu-id="a7274-104">Data management in Microsoft Dynamics 365 for Finance and Operations supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="a7274-105">Šajās veidnēs var būt viena vai vairākas darblapas.</span><span class="sxs-lookup"><span data-stu-id="a7274-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="a7274-106">Veidnes ar vairākām darblapām bieži tiek izmantotas, kad ir vēlams datus pārvaldīt vienā failā un to importēt vairākos datu elementos.</span><span class="sxs-lookup"><span data-stu-id="a7274-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="a7274-107">Kā piemēru varētu minēt vietas un noliktavas.</span><span class="sxs-lookup"><span data-stu-id="a7274-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="a7274-108">Faila augšupielādēšana vienu reizi un kartēšana uz visiem elementiem</span><span class="sxs-lookup"><span data-stu-id="a7274-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="a7274-109">Apskatīsim piemēru, kur vienā Excel failā ir darblapas ar nosaukumu **Vietas** un **Noliktavas**.</span><span class="sxs-lookup"><span data-stu-id="a7274-109">Let’s take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="a7274-110">Lai iestatītu datu importēšanas projektu, jūs pievienotu pirmo datu elementu, **Vietas**, un pēc tam augšupielādētu šo failu.</span><span class="sxs-lookup"><span data-stu-id="a7274-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="a7274-111">Kā šim elementam izmantojamo darblapu varat atlasīt **Vietas**.</span><span class="sxs-lookup"><span data-stu-id="a7274-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="a7274-112">Ja pievienojat otro elementu, **Noliktavas**, neaizverot formu **Pievienot failu**, darblapas uzmeklēšana jums ļauj atlasīt darblapu **Noliktavas** bez nepieciešamības šo failu augšupielādēt vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="a7274-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="a7274-113">Vienīgais iemesls augšupielādēt jaunu failu būtu tad, ja dati **Noliktavas** atrastos citā failā.</span><span class="sxs-lookup"><span data-stu-id="a7274-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Vairākas darblapas](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="a7274-115">Darblapas norādīšana elementa kartēšanai</span><span class="sxs-lookup"><span data-stu-id="a7274-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="a7274-116">Darblapas kartēšanu uz kādu datu elementu importēšanas darbā var norādīt no režģa.</span><span class="sxs-lookup"><span data-stu-id="a7274-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="a7274-117">Režģa kolonnā **Darblapa** tiek rādītas darblapas no faila, kurš tika kartēts.</span><span class="sxs-lookup"><span data-stu-id="a7274-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="a7274-118">Nolaižamajā izvēlnē varat izvēlēties citu darblapu.</span><span class="sxs-lookup"><span data-stu-id="a7274-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="a7274-119">Ja izvēlētā darblapa jau tiek kartēta uz kādu elementu datu projektā, sistēma jums lūdz apstiprināt šīs izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="a7274-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="a7274-120">Ieteicams norādīt visus kartējumus režģī.</span><span class="sxs-lookup"><span data-stu-id="a7274-120">We recommend that you fix all mappings in the grid.</span></span>

![Darblapas kartējuma atjaunināšana](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="a7274-122">Pārkartēšana uz jaunu failu</span><span class="sxs-lookup"><span data-stu-id="a7274-122">Re-map to a new file</span></span>

<span data-ttu-id="a7274-123">Gadījumos, kad kādā datu projektā esošiem elementiem ir nepieciešams augšupielādēt tā paša faila jaunu versiju vai pilnīgi jaunu failu, jums ir jālieto funkcionalitāte **Pievienot failu** un jāpievieno šie elementi vēlreiz, it kā tie tiktu pievienoti pirmo reizi.</span><span class="sxs-lookup"><span data-stu-id="a7274-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="a7274-124">Pirms turpināšanas sistēma pārliecināsies, vai vēlaties pārrakstīt esošos elementus datu projektā.</span><span class="sxs-lookup"><span data-stu-id="a7274-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="a7274-125">Elementi, kas netiek pievienoti vēlreiz (vai pārrakstīti), turpina izmantot iepriekšējos kartējumus no iepriekšējā faila.</span><span class="sxs-lookup"><span data-stu-id="a7274-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="a7274-126">Faila augšupielādēšana, izmantojot opciju Palaist projektu</span><span class="sxs-lookup"><span data-stu-id="a7274-126">Upload a file using Run project</span></span>

<span data-ttu-id="a7274-127">Varat augšupielādēt Excel failu, kamēr izmantojat opciju **Palaist projektu**, lai izpildītu importēšanas projektu.</span><span class="sxs-lookup"><span data-stu-id="a7274-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="a7274-128">Uzmanieties, lai augšupielādētu tikai failus, kuros ir tādas pašas darblapas kā esošajiem kartējumiem uz datu elementiem datu projektā.</span><span class="sxs-lookup"><span data-stu-id="a7274-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="a7274-129">Ja no jauna augšupielādētajā failā kāda darblapa netiek atrasta, sistēma parāda kļūdas ziņojumu un pārtrauc importēšanu.</span><span class="sxs-lookup"><span data-stu-id="a7274-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="a7274-130">Ja kādam elementam ir jāmaina kartēšana uz darblapu, tad kartējumi datu projektā vispirms ir jāatjaunina no datu projekta, un tikai pēc tam šo failu var izmantot funkcionalitātē **Palaist projektu**.</span><span class="sxs-lookup"><span data-stu-id="a7274-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>


