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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974034"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="1864c-103">Dokumenta stāvokļi un dzīves cikls</span><span class="sxs-lookup"><span data-stu-id="1864c-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1864c-104">Šajā tēmā ir ietverti dažādi Microsoft Dynamics 365 Commerce lapas elementu dokumenta stāvokļi.</span><span class="sxs-lookup"><span data-stu-id="1864c-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="1864c-105">Dokumenta stāvokļa apraksti</span><span class="sxs-lookup"><span data-stu-id="1864c-105">Document state descriptions</span></span>

<span data-ttu-id="1864c-106">Tēmā [Lapas elementi](page-elements-overview.md) uzskaitīti dažādi dokumentu veidi satura pārvaldības sistēmā (CMS).</span><span class="sxs-lookup"><span data-stu-id="1864c-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="1864c-107">Šiem dokumentu veidiem autorēšanas rīkā var būt vairāki stāvokļi.</span><span class="sxs-lookup"><span data-stu-id="1864c-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="1864c-108">Dokumenta stāvokļi palīdz novērst datu konfliktus un ieviest versiju kontroli.</span><span class="sxs-lookup"><span data-stu-id="1864c-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="1864c-109">Tās nosaka, kurš var mainīt dokumentus, kad to var darīt, un kad citas personas var skatīt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="1864c-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="1864c-110">Tālāk redzamā tabula parāda Commerce iespējamos lapas elementu dokumenta stāvokļus.</span><span class="sxs-lookup"><span data-stu-id="1864c-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="1864c-111">Dokumenta stāvoklis</span><span class="sxs-lookup"><span data-stu-id="1864c-111">Document state</span></span>      | <span data-ttu-id="1864c-112">Vietnes veidotāja darbība</span><span class="sxs-lookup"><span data-stu-id="1864c-112">Site builder action</span></span>        | <span data-ttu-id="1864c-113">apraksts</span><span class="sxs-lookup"><span data-stu-id="1864c-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="1864c-114">Izrakstīts</span><span class="sxs-lookup"><span data-stu-id="1864c-114">Checked out</span></span>         | <span data-ttu-id="1864c-115">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="1864c-115">Select **Edit**.</span></span>           | <span data-ttu-id="1864c-116">Piemērotais dokuments tiek paņemts jums.</span><span class="sxs-lookup"><span data-stu-id="1864c-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="1864c-117">Kamēr dokuments ir šajā stāvoklī, to nevar mainīt citi autentificēti sistēmas lietotāji, un visas dokumentā veiktās izmaiņas ir redzamas tikai jums.</span><span class="sxs-lookup"><span data-stu-id="1864c-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="1864c-118">Saglabāts</span><span class="sxs-lookup"><span data-stu-id="1864c-118">Saved</span></span>               | <span data-ttu-id="1864c-119">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1864c-119">Select **Save**.</span></span>           | <span data-ttu-id="1864c-120">Paņemtā dokumentā veiktās izmaiņas tiek saglabātas datu bāzē, bet dokuments vēl nav atdots vai publicēts.</span><span class="sxs-lookup"><span data-stu-id="1864c-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="1864c-121">Saglabātās izmaiņas nav redzamas citiem autentificētiem sistēmas lietotājiem, kamēr autors atlasa **Beigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="1864c-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="1864c-122">Tie nav redzami ārējiem lietotājiem, kamēr elements nav publicēts.</span><span class="sxs-lookup"><span data-stu-id="1864c-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="1864c-123">Atmestā izrakstīšana</span><span class="sxs-lookup"><span data-stu-id="1864c-123">Discarded check out</span></span> | <span data-ttu-id="1864c-124">Atlasiet **Atmest labojumus**.</span><span class="sxs-lookup"><span data-stu-id="1864c-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="1864c-125">Visas izmaiņas paņemtajā dokumentā tiek atmestas, un krājums tiek atgriezts pēdējā versijā, kas tika pārbaudīta.</span><span class="sxs-lookup"><span data-stu-id="1864c-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="1864c-126">Reģistrējies</span><span class="sxs-lookup"><span data-stu-id="1864c-126">Checked in</span></span>          | <span data-ttu-id="1864c-127">Atlasiet **Beigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="1864c-127">Select **Finish editing**.</span></span> | <span data-ttu-id="1864c-128">Rediģētais dokuments ir atdots.</span><span class="sxs-lookup"><span data-stu-id="1864c-128">The edited document is checked in.</span></span> <span data-ttu-id="1864c-129">Visas izmaiņas ir redzamas citiem autentificētiem sistēmas lietotājiem, un šie lietotāji pēc tam var rediģēt dokumentu.</span><span class="sxs-lookup"><span data-stu-id="1864c-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="1864c-130">Katra reģistrācija izveido dokumenta versijas ierakstu elementa vēsturē.</span><span class="sxs-lookup"><span data-stu-id="1864c-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="1864c-131">Publicēts</span><span class="sxs-lookup"><span data-stu-id="1864c-131">Published</span></span>           | <span data-ttu-id="1864c-132">Atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="1864c-132">Select **Publish**.</span></span>        | <span data-ttu-id="1864c-133">Dokuments tiek publicēts, un izmaiņas tiek atstumtas uz jūsu Live vietni un kļūst atklājamas ārējiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="1864c-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="1864c-134">Krājumus var publicēt tikai tad, ja tie vispirms ir pārbaudīti, atlasot **Beigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="1864c-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="1864c-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1864c-135">Additional resources</span></span>

[<span data-ttu-id="1864c-136">Satura pievienošanas veidi</span><span class="sxs-lookup"><span data-stu-id="1864c-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="1864c-137">Lapas modeļa glosārijs</span><span class="sxs-lookup"><span data-stu-id="1864c-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="1864c-138">Darbs ar publicēšanas grupām</span><span class="sxs-lookup"><span data-stu-id="1864c-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="1864c-139">Šķērskanālu kopīgošanas iespējošana un izmantošana</span><span class="sxs-lookup"><span data-stu-id="1864c-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="1864c-140">Darbs ar moduļiem</span><span class="sxs-lookup"><span data-stu-id="1864c-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="1864c-141">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="1864c-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="1864c-142">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="1864c-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="1864c-143">Vietnes navigācijas pielāgošana</span><span class="sxs-lookup"><span data-stu-id="1864c-143">Customize site navigation</span></span>](customize-site-navigation.md)
