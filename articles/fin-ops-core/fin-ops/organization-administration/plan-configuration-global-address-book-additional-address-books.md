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
ms.openlocfilehash: 7d83d6536d85100ef6a91e909be5a8e57e423371
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693934"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Plāns globālajai adrešu grāmatai un citām adrešu grāmatām

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti apsvērumi un lēmumi, kas ir jāņem vērā un jāpieņem plānošanas procesa laikā pirms globālās adrešu grāmatas un jebkuru papildu adrešu grāmatu iestatīšanas un konfigurēšanas. Dažu lēmumu pieņemšanas nolūkos ir nepieciešams apstiprināt lēmumus, kas jau ir pieņemti citās preces jomās, piemēram, organizācijas hierarhijā.

## <a name="global-address-book"></a>Globālā adrešu grāmata

Pirms sākat strādāt ar globālo adrešu grāmatu, jums tai ir jānosaka noklusējuma vērtības. Šīs noklusējuma vērtības pēc tam tiek lietotas visām jūsu izveidotajām papildu adrešu grāmatām.

**Lēmumi:**

- Kādā secībā rādīt nosaukumus/vārdus pušu ierakstiem ar tipu **Persona**? Piemēram, viena iespējamā secība ir uzvārds, otrais vārds, vārds.
- Vai pušu ieraksti ir jādzēš no adrešu grāmatas, kad lomas ieraksts tiek dzēsts? Piemēram, ja debitora ieraksts tiek dzēsts, vai ir jādzēš arī puses ieraksts?
- Kad tiek veidots jauns ieraksts, vai lietotājiem ir jāpaziņo, ja globālajā adrešu grāmatā ir konstatēts ieraksta dublikāts?
- Vai universālās datu numerācijas sistēmas (Data Universal Numbering System — DUNS) numurs ir jāiekļauj puses ieraksta informācijā?
- Ja DUNS numurs tiek iekļauts puses ierakstā — vai ir jāpārbauda numura unikalitāte?
- Kad puses ieraksts tiek izveidots globālajā adrešu grāmatā, vai vēlaties izmantot noklusējuma puses tipu, personu vai organizāciju?
- Kurām lietotāju lomām ir piekļuve pušu ierakstu privātajām adresēm un kontaktinformācijai?

## <a name="additional-address-books"></a>Papildu adrešu grāmatas

Pēc globālās adrešu grāmatas izveidošanas pēc nepieciešamības varat izveidot papildu adrešu grāmatas, piemēram, atsevišķu adrešu grāmatu katram uzņēmumam jūsu organizācijā vai katrai biznesa jomai. Piemēram, Fabrikam ir starptautiska organizācija, kurai ir vairāki uzņēmumi un kas darbojas vairākās biznesa jomās. Fabrikam plāno izveidot adrešu grāmatu katrai biznesa jomai. Biznesa jomām, kas tiek izmantotas vairākās vietās, piemēram, pneimatisko instrumentu biznesam, Fabrikam plāno izveidot adrešu grāmatu katrai atrašanās vietai. Fabrikam IT vadītājs Kriss ir izveidojis tālāk norādīto sarakstu ar nepieciešamajām adrešu grāmatām. Šajā sarakstā ir aprakstīti arī pušu ieraksti, kam ir jābūt ietvertiem katrā adrešu grāmatā.

- **Publiskā sektora līgumi (PubSC)** — pušu ieraksti visām pusēm, kas ir iesaistītas Fabrikam noslēgtajos publiskā sektora līgumos.
- **Privātā sektora līgumi (PriSC)** — pušu ieraksti visām pusēm, kas ir iesaistītas Fabrikam noslēgtajos privātā sektora līgumos.
- **Elektroniskie instrumenti (ET)** — pušu ieraksti visām pusēm, kas ir iesaistītas elektronisko instrumentu pirkšanā vai pārdošanā, vai kas kā citādi mijiedarbojas ar elektroniskajiem instrumentiem, kurus nodrošina Fabrikam vai kuri tiek iegādāti Fabrikam nolūkiem Fabrikam-Japānas uzņēmumā.
- **Pneimatiskie instrumenti (PTJPN)** — pušu ieraksti visām pusēm, kas ir iesaistītas pneimatisko instrumentu pirkšanā vai pārdošanā, vai kas kā citādi mijiedarbojas ar pneimatiskajiem instrumentiem, kurus nodrošina Fabrikam vai kuri tiek iegādāti Fabrikam nolūkiem Fabrikam-Japānas uzņēmumā.
- **Pneimatiskie instrumenti (PTUSA)** — pušu ieraksti visām pusēm, kas ir iesaistītas pneimatisko instrumentu pirkšanā vai pārdošanā, vai kas kā citādi mijiedarbojas ar pneimatiskajiem instrumentiem, kurus nodrošina Fabrikam vai kuri tiek iegādāti Fabrikam nolūkiem Fabrikam-ASV uzņēmumā.

**Lēmums:**

- Cik daudz papildu adrešu grāmatas jūs izveidosiet?
