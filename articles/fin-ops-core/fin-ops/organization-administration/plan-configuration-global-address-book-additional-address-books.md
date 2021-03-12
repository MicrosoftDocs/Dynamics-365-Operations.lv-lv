---
title: Globālās adrešu grāmatas un citu adrešu grāmatu plānošana
description: Šajā tēmā ir aprakstīti apsvērumi un lēmumi, kas ir jāņem vērā un jāpieņem plānošanas procesa laikā pirms globālās adrešu grāmatas un jebkuru papildu adrešu grāmatu iestatīšanas un konfigurēšanas.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f0a53e1f9b378759e0c5adbe0612a5fa8cddc82
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796950"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="c0318-103">Plāns globālajai adrešu grāmatai un citām adrešu grāmatām</span><span class="sxs-lookup"><span data-stu-id="c0318-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0318-104">Šajā tēmā ir aprakstīti apsvērumi un lēmumi, kas ir jāņem vērā un jāpieņem plānošanas procesa laikā pirms globālās adrešu grāmatas un jebkuru papildu adrešu grāmatu iestatīšanas un konfigurēšanas.</span><span class="sxs-lookup"><span data-stu-id="c0318-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="c0318-105">Dažu lēmumu pieņemšanas nolūkos ir nepieciešams apstiprināt lēmumus, kas jau ir pieņemti citās preces jomās, piemēram, organizācijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="c0318-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="c0318-106">Globālā adrešu grāmata</span><span class="sxs-lookup"><span data-stu-id="c0318-106">Global address book</span></span>

<span data-ttu-id="c0318-107">Pirms sākat strādāt ar globālo adrešu grāmatu, jums tai ir jānosaka noklusējuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="c0318-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="c0318-108">Šīs noklusējuma vērtības pēc tam tiek lietotas visām jūsu izveidotajām papildu adrešu grāmatām.</span><span class="sxs-lookup"><span data-stu-id="c0318-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="c0318-109">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="c0318-109">**Decisions**</span></span>

- <span data-ttu-id="c0318-110">Kādā secībā rādīt nosaukumus/vārdus pušu ierakstiem ar tipu **Persona**?</span><span class="sxs-lookup"><span data-stu-id="c0318-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="c0318-111">Piemēram, viena iespējamā secība ir uzvārds, otrais vārds, vārds.</span><span class="sxs-lookup"><span data-stu-id="c0318-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="c0318-112">Vai pušu ieraksti ir jādzēš no adrešu grāmatas, kad lomas ieraksts tiek dzēsts?</span><span class="sxs-lookup"><span data-stu-id="c0318-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="c0318-113">Piemēram, ja debitora ieraksts tiek dzēsts, vai ir jādzēš arī puses ieraksts?</span><span class="sxs-lookup"><span data-stu-id="c0318-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="c0318-114">Kad tiek veidots jauns ieraksts, vai lietotājiem ir jāpaziņo, ja globālajā adrešu grāmatā ir konstatēts ieraksta dublikāts?</span><span class="sxs-lookup"><span data-stu-id="c0318-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="c0318-115">Vai universālās datu numerācijas sistēmas (Data Universal Numbering System — DUNS) numurs ir jāiekļauj puses ieraksta informācijā?</span><span class="sxs-lookup"><span data-stu-id="c0318-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="c0318-116">Ja DUNS numurs tiek iekļauts puses ierakstā — vai ir jāpārbauda numura unikalitāte?</span><span class="sxs-lookup"><span data-stu-id="c0318-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="c0318-117">Kad puses ieraksts tiek izveidots globālajā adrešu grāmatā, vai vēlaties izmantot noklusējuma puses tipu, personu vai organizāciju?</span><span class="sxs-lookup"><span data-stu-id="c0318-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="c0318-118">Kurām lietotāju lomām ir piekļuve pušu ierakstu privātajām adresēm un kontaktinformācijai?</span><span class="sxs-lookup"><span data-stu-id="c0318-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="c0318-119">Papildu adrešu grāmatas</span><span class="sxs-lookup"><span data-stu-id="c0318-119">Additional address books</span></span>

<span data-ttu-id="c0318-120">Pēc globālās adrešu grāmatas izveidošanas pēc nepieciešamības varat izveidot papildu adrešu grāmatas, piemēram, atsevišķu adrešu grāmatu katram uzņēmumam jūsu organizācijā vai katrai biznesa jomai.</span><span class="sxs-lookup"><span data-stu-id="c0318-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="c0318-121">Piemēram, Fabrikam ir starptautiska organizācija, kurai ir vairāki uzņēmumi un kas darbojas vairākās biznesa jomās.</span><span class="sxs-lookup"><span data-stu-id="c0318-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="c0318-122">Fabrikam plāno izveidot adrešu grāmatu katrai biznesa jomai.</span><span class="sxs-lookup"><span data-stu-id="c0318-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="c0318-123">Biznesa jomām, kas tiek izmantotas vairākās vietās, piemēram, pneimatisko instrumentu biznesam, Fabrikam plāno izveidot adrešu grāmatu katrai atrašanās vietai.</span><span class="sxs-lookup"><span data-stu-id="c0318-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="c0318-124">Fabrikam IT vadītājs Kriss ir izveidojis tālāk norādīto sarakstu ar nepieciešamajām adrešu grāmatām.</span><span class="sxs-lookup"><span data-stu-id="c0318-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="c0318-125">Šajā sarakstā ir aprakstīti arī pušu ieraksti, kam ir jābūt ietvertiem katrā adrešu grāmatā.</span><span class="sxs-lookup"><span data-stu-id="c0318-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="c0318-126">**Publiskā sektora līgumi (PubSC)** — pušu ieraksti visām pusēm, kas ir iesaistītas Fabrikam noslēgtajos publiskā sektora līgumos.</span><span class="sxs-lookup"><span data-stu-id="c0318-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="c0318-127">**Privātā sektora līgumi (PriSC)** — pušu ieraksti visām pusēm, kas ir iesaistītas Fabrikam noslēgtajos privātā sektora līgumos.</span><span class="sxs-lookup"><span data-stu-id="c0318-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="c0318-128">**Elektroniskie instrumenti (ET)** — pušu ieraksti visām pusēm, kas ir iesaistītas elektronisko instrumentu pirkšanā vai pārdošanā, vai kas kā citādi mijiedarbojas ar elektroniskajiem instrumentiem, kurus nodrošina Fabrikam vai kuri tiek iegādāti Fabrikam nolūkiem Fabrikam-Japānas uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="c0318-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="c0318-129">**Pneimatiskie instrumenti (PTJPN)** — pušu ieraksti visām pusēm, kas ir iesaistītas pneimatisko instrumentu pirkšanā vai pārdošanā, vai kas kā citādi mijiedarbojas ar pneimatiskajiem instrumentiem, kurus nodrošina Fabrikam vai kuri tiek iegādāti Fabrikam nolūkiem Fabrikam-Japānas uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="c0318-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="c0318-130">**Pneimatiskie instrumenti (PTUSA)** — pušu ieraksti visām pusēm, kas ir iesaistītas pneimatisko instrumentu pirkšanā vai pārdošanā, vai kas kā citādi mijiedarbojas ar pneimatiskajiem instrumentiem, kurus nodrošina Fabrikam vai kuri tiek iegādāti Fabrikam nolūkiem Fabrikam-ASV uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="c0318-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="c0318-131">**Lēmums:**</span><span class="sxs-lookup"><span data-stu-id="c0318-131">**Decision:**</span></span>

- <span data-ttu-id="c0318-132">Cik daudz papildu adrešu grāmatas jūs izveidosiet?</span><span class="sxs-lookup"><span data-stu-id="c0318-132">How many additional address books will you create?</span></span>
