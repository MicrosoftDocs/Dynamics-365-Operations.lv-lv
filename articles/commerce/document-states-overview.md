---
title: Dokumenta stāvokļi un dzīves cikls
description: Šajā tēmā ir ietverti dažādi Microsoft Dynamics 365 Commerce lapas elementu dokumenta stāvokļi.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914891"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="577b4-103">Dokumenta stāvokļi un dzīves cikls</span><span class="sxs-lookup"><span data-stu-id="577b4-103">Document states and lifecycle</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="577b4-104">Šajā tēmā ir ietverti dažādi Microsoft Dynamics 365 Commerce lapas elementu dokumenta stāvokļi.</span><span class="sxs-lookup"><span data-stu-id="577b4-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="577b4-105">Dokumenta stāvokļa apraksti</span><span class="sxs-lookup"><span data-stu-id="577b4-105">Document state descriptions</span></span>

<span data-ttu-id="577b4-106">Tēmā [Lapas elementi](page-elements-overview.md) uzskaitīti dažādi dokumentu veidi satura pārvaldības sistēmā (CMS).</span><span class="sxs-lookup"><span data-stu-id="577b4-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="577b4-107">Šiem dokumentu veidiem autorēšanas rīkā var būt vairāki stāvokļi.</span><span class="sxs-lookup"><span data-stu-id="577b4-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="577b4-108">Dokumenta stāvokļi palīdz novērst datu konfliktus un ieviest versiju kontroli.</span><span class="sxs-lookup"><span data-stu-id="577b4-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="577b4-109">Tās nosaka, kurš var mainīt dokumentus, kad to var darīt, un kad citas personas var skatīt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="577b4-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="577b4-110">Tālāk redzamā tabula parāda Commerce iespējamos lapas elementu dokumenta stāvokļus.</span><span class="sxs-lookup"><span data-stu-id="577b4-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="577b4-111">Dokumenta stāvoklis</span><span class="sxs-lookup"><span data-stu-id="577b4-111">Document state</span></span> | <span data-ttu-id="577b4-112">Apraksts</span><span class="sxs-lookup"><span data-stu-id="577b4-112">Description</span></span> |
|---|---|
| <span data-ttu-id="577b4-113">Izrakstījies</span><span class="sxs-lookup"><span data-stu-id="577b4-113">Checked out</span></span> | <span data-ttu-id="577b4-114">Kad CMS elements ir izrakstīts jums, citi autentificēti sistēmas lietotāji to nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="577b4-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="577b4-115">Visas izmaiņas, ko veicat elementā, redzamas tikai jums.</span><span class="sxs-lookup"><span data-stu-id="577b4-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="577b4-116">Reģistrējies</span><span class="sxs-lookup"><span data-stu-id="577b4-116">Checked in</span></span> | <span data-ttu-id="577b4-117">Kad CMS elements ir reģistrēts, visas izmaiņas ir redzamas citiem autentificētiem sistēmas lietotājiem, un šie lietotāji var izrakstīt elementu un to rediģēt.</span><span class="sxs-lookup"><span data-stu-id="577b4-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="577b4-118">Katra reģistrācija izveido dokumenta versijas ierakstu elementa vēsturē.</span><span class="sxs-lookup"><span data-stu-id="577b4-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="577b4-119">Publicēts</span><span class="sxs-lookup"><span data-stu-id="577b4-119">Published</span></span> | <span data-ttu-id="577b4-120">Kad CMS elements ir publicēts, tas tiek iestumts jūsu aktuālajā vietnē un internetā kļūst pamanāms ieautentificētiem ārējiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="577b4-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="577b4-121">Elementus var publicēt tikai tad, ja tie ir reģistrēti.</span><span class="sxs-lookup"><span data-stu-id="577b4-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="577b4-122">Saglabāts</span><span class="sxs-lookup"><span data-stu-id="577b4-122">Saved</span></span> | <span data-ttu-id="577b4-123">Izmaiņas, kas veiktas izrakstītam CMS elementam, var tikt saglabātas CMS pirms elements ir reģistrēts vai publicēts.</span><span class="sxs-lookup"><span data-stu-id="577b4-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="577b4-124">Šīs saglabātās izmaiņas nav redzamas citiem autentificētiem sistēmas lietotājiem, kamēr elements nav reģistrēts.</span><span class="sxs-lookup"><span data-stu-id="577b4-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="577b4-125">Tie nav redzami ārējiem lietotājiem, kamēr elements nav publicēts.</span><span class="sxs-lookup"><span data-stu-id="577b4-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="577b4-126">Atmestā izrakstīšana</span><span class="sxs-lookup"><span data-stu-id="577b4-126">Discarded check out</span></span> | <span data-ttu-id="577b4-127">Kad izrakstītais CMS elements tiek atmests, visas saglabātās izmaiņas tiek dzēstas, un elements atgriežas pēdējā reģistrētajā versijā.</span><span class="sxs-lookup"><span data-stu-id="577b4-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="577b4-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="577b4-128">Additional resources</span></span>

[<span data-ttu-id="577b4-129">Satura pievienošanas veidi</span><span class="sxs-lookup"><span data-stu-id="577b4-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="577b4-130">Lapas modeļa glosārijs</span><span class="sxs-lookup"><span data-stu-id="577b4-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="577b4-131">Darbs ar publicēšanas grupām</span><span class="sxs-lookup"><span data-stu-id="577b4-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="577b4-132">Darbs ar moduļiem</span><span class="sxs-lookup"><span data-stu-id="577b4-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="577b4-133">Darbs ar fragmentiem</span><span class="sxs-lookup"><span data-stu-id="577b4-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="577b4-134">Pārskats par veidnēm un izkārtojumiem</span><span class="sxs-lookup"><span data-stu-id="577b4-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="577b4-135">Vietnes navigācijas pielāgošana</span><span class="sxs-lookup"><span data-stu-id="577b4-135">Customize site navigation</span></span>](customize-site-navigation.md)
