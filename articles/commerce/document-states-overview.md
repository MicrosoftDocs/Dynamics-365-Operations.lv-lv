---
title: Dokumenta stāvokļi un dzīves cikls
description: Šajā tēmā ir ietverti dažādi Microsoft Dynamics 365 Commerce lapas elementu dokumenta stāvokļi.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c30932800beda13ac8fe6b0386fe29efe93f79c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982620"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="06161-103">Dokumenta stāvokļi un dzīves cikls</span><span class="sxs-lookup"><span data-stu-id="06161-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06161-104">Šajā tēmā ir ietverti dažādi Microsoft Dynamics 365 Commerce lapas elementu dokumenta stāvokļi.</span><span class="sxs-lookup"><span data-stu-id="06161-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="06161-105">Dokumenta stāvokļa apraksti</span><span class="sxs-lookup"><span data-stu-id="06161-105">Document state descriptions</span></span>

<span data-ttu-id="06161-106">Tēmā [Lapas elementi](page-elements-overview.md) uzskaitīti dažādi dokumentu veidi satura pārvaldības sistēmā (CMS).</span><span class="sxs-lookup"><span data-stu-id="06161-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="06161-107">Šiem dokumentu veidiem autorēšanas rīkā var būt vairāki stāvokļi.</span><span class="sxs-lookup"><span data-stu-id="06161-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="06161-108">Dokumenta stāvokļi palīdz novērst datu konfliktus un ieviest versiju kontroli.</span><span class="sxs-lookup"><span data-stu-id="06161-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="06161-109">Tās nosaka, kurš var mainīt dokumentus, kad to var darīt, un kad citas personas var skatīt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="06161-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="06161-110">Tālāk redzamā tabula parāda Commerce iespējamos lapas elementu dokumenta stāvokļus.</span><span class="sxs-lookup"><span data-stu-id="06161-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="06161-111">Dokumenta stāvoklis</span><span class="sxs-lookup"><span data-stu-id="06161-111">Document state</span></span>      | <span data-ttu-id="06161-112">Vietnes veidotāja darbība</span><span class="sxs-lookup"><span data-stu-id="06161-112">Site builder action</span></span>        | <span data-ttu-id="06161-113">apraksts</span><span class="sxs-lookup"><span data-stu-id="06161-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="06161-114">Izrakstīts</span><span class="sxs-lookup"><span data-stu-id="06161-114">Checked out</span></span>         | <span data-ttu-id="06161-115">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="06161-115">Select **Edit**.</span></span>           | <span data-ttu-id="06161-116">Piemērotais dokuments tiek paņemts jums.</span><span class="sxs-lookup"><span data-stu-id="06161-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="06161-117">Kamēr dokuments ir šajā stāvoklī, to nevar mainīt citi autentificēti sistēmas lietotāji, un visas dokumentā veiktās izmaiņas ir redzamas tikai jums.</span><span class="sxs-lookup"><span data-stu-id="06161-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="06161-118">Saglabāts</span><span class="sxs-lookup"><span data-stu-id="06161-118">Saved</span></span>               | <span data-ttu-id="06161-119">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="06161-119">Select **Save**.</span></span>           | <span data-ttu-id="06161-120">Paņemtā dokumentā veiktās izmaiņas tiek saglabātas datu bāzē, bet dokuments vēl nav atdots vai publicēts.</span><span class="sxs-lookup"><span data-stu-id="06161-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="06161-121">Saglabātās izmaiņas nav redzamas citiem autentificētiem sistēmas lietotājiem, kamēr autors atlasa **Beigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="06161-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="06161-122">Tie nav redzami ārējiem lietotājiem, kamēr elements nav publicēts.</span><span class="sxs-lookup"><span data-stu-id="06161-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="06161-123">Atmestā izrakstīšana</span><span class="sxs-lookup"><span data-stu-id="06161-123">Discarded check out</span></span> | <span data-ttu-id="06161-124">Atlasiet **Atmest labojumus**.</span><span class="sxs-lookup"><span data-stu-id="06161-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="06161-125">Visas izmaiņas paņemtajā dokumentā tiek atmestas, un krājums tiek atgriezts pēdējā versijā, kas tika pārbaudīta.</span><span class="sxs-lookup"><span data-stu-id="06161-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="06161-126">Reģistrējies</span><span class="sxs-lookup"><span data-stu-id="06161-126">Checked in</span></span>          | <span data-ttu-id="06161-127">Atlasiet **Beigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="06161-127">Select **Finish editing**.</span></span> | <span data-ttu-id="06161-128">Rediģētais dokuments ir atdots.</span><span class="sxs-lookup"><span data-stu-id="06161-128">The edited document is checked in.</span></span> <span data-ttu-id="06161-129">Visas izmaiņas ir redzamas citiem autentificētiem sistēmas lietotājiem, un šie lietotāji pēc tam var rediģēt dokumentu.</span><span class="sxs-lookup"><span data-stu-id="06161-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="06161-130">Katra reģistrācija izveido dokumenta versijas ierakstu elementa vēsturē.</span><span class="sxs-lookup"><span data-stu-id="06161-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="06161-131">Publicēts</span><span class="sxs-lookup"><span data-stu-id="06161-131">Published</span></span>           | <span data-ttu-id="06161-132">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="06161-132">Select **Publish**.</span></span>        | <span data-ttu-id="06161-133">Dokuments tiek publicēts, un izmaiņas tiek atstumtas uz jūsu Live vietni un kļūst atklājamas ārējiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="06161-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="06161-134">Krājumus var publicēt tikai tad, ja tie vispirms ir pārbaudīti, atlasot **Beigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="06161-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="06161-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="06161-135">Additional resources</span></span>

[<span data-ttu-id="06161-136">Satura pievienošanas veidi</span><span class="sxs-lookup"><span data-stu-id="06161-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="06161-137">Lapas modeļa glosārijs</span><span class="sxs-lookup"><span data-stu-id="06161-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="06161-138">Darbs ar publicēšanas grupām</span><span class="sxs-lookup"><span data-stu-id="06161-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="06161-139">Šķērskanālu kopīgošanas iespējošana un izmantošana</span><span class="sxs-lookup"><span data-stu-id="06161-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="06161-140">Darbs ar moduļiem</span><span class="sxs-lookup"><span data-stu-id="06161-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="06161-141">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="06161-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="06161-142">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="06161-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="06161-143">Vietnes navigācijas pielāgošana</span><span class="sxs-lookup"><span data-stu-id="06161-143">Customize site navigation</span></span>](customize-site-navigation.md)
