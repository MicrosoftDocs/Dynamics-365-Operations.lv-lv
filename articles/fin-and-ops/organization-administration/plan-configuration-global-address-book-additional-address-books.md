---
title: "Globālās adrešu grāmatas un papildu adrešu grāmatu konfigurācijas plānošana"
description: "Šajā rakstā ir aprakstīti apsvērumi un lēmumi, kas ir jāņem vērā un jāpieņem plānošanas procesa laikā pirms globālo adrešu grāmatu un jebkādu papildu adrešu grāmatu iestatīšanas un konfigurēšanas programmatūrā Microsoft Dynamics 365 for Finance and Operations. Dažu lēmumu pieņemšanas nolūkos ir nepieciešams apstiprināt lēmumus, kas jau ir pieņemti citās preces jomās, piemēram, organizācijas hierarhijā."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a>Globālās adrešu grāmatas un papildu adrešu grāmatu konfigurācijas plānošana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīti apsvērumi un lēmumi, kas ir jāņem vērā un jāpieņem plānošanas procesa laikā pirms globālo adrešu grāmatu un jebkādu papildu adrešu grāmatu iestatīšanas un konfigurēšanas programmatūrā Microsoft Dynamics 365 for Finance and Operations. Dažu lēmumu pieņemšanas nolūkos ir nepieciešams apstiprināt lēmumus, kas jau ir pieņemti citās preces jomās, piemēram, organizācijas hierarhijā.

<a name="global-address-book"></a>Globālā adrešu grāmata
-------------------

Pirms sākat strādāt ar globālo adrešu grāmatu, jums tai ir jānosaka noklusējuma vērtības. Šīs noklusējuma vērtības pēc tam tiek lietotas visām jūsu izveidotajām papildu adrešu grāmatām. 

**Lēmumi:**

-   Kādā secībā rādīt nosaukumus/vārdus pušu ierakstiem ar tipu **Persona**? Piemēram, viena iespējamā secība ir uzvārds, otrais vārds, vārds.
-   Vai pušu ieraksti ir jādzēš no adrešu grāmatas, kad lomas ieraksts tiek dzēsts? Piemēram, ja debitora ieraksts tiek dzēsts, vai ir jādzēš arī puses ieraksts?
-   Kad tiek veidots jauns ieraksts, vai lietotājiem ir jāpaziņo, ja globālajā adrešu grāmatā ir konstatēts ieraksta dublikāts?
-   Vai universālās datu numerācijas sistēmas (Data Universal Numbering System — DUNS) numurs ir jāiekļauj puses ieraksta informācijā?
-   Ja DUNS numurs tiek iekļauts puses ierakstā — vai ir jāpārbauda numura unikalitāte?
-   Kad puses ieraksts tiek izveidots globālajā adrešu grāmatā, vai vēlaties izmantot noklusējuma puses tipu, personu vai organizāciju?
-   Kurām lietotāju lomām ir piekļuve pušu ierakstu privātajām adresēm un kontaktinformācijai?

## <a name="additional-address-books"></a>Papildu adrešu grāmatas
Pēc globālās adrešu grāmatas izveidošanas pēc nepieciešamības varat izveidot papildu adrešu grāmatas, piemēram, atsevišķu adrešu grāmatu katram uzņēmumam jūsu organizācijā vai katrai biznesa jomai. Piemēram, Fabrikam ir starptautiska organizācija, kurai ir vairāki uzņēmumi un kas darbojas vairākās biznesa jomās. Fabrikam plāno izveidot adrešu grāmatu katrai biznesa jomai. Biznesa jomām, kas tiek izmantotas vairākās vietās, piemēram, pneimatisko instrumentu biznesam, Fabrikam plāno izveidot adrešu grāmatu katrai atrašanās vietai. Fabrikam IT vadītājs Kriss ir izveidojis tālāk norādīto sarakstu ar nepieciešamajām adrešu grāmatām. Šajā sarakstā ir aprakstīti arī pušu ieraksti, kas ir jāietver katrā adrešu grāmatā.

-   **Publiskā sektora līgumi (PubSC)** — pušu ieraksti visām pusēm, kas ir iesaistītas Fabrikam noslēgtajos publiskā sektora līgumos.
-   **Privātā sektora līgumi (PriSC)** — pušu ieraksti visām pusēm, kas ir iesaistītas Fabrikam noslēgtajos privātā sektora līgumos.
-   **Elektroniskie instrumenti (ET)** — pušu ieraksti visām pusēm, kas ir iesaistītas elektronisko instrumentu pirkšanā vai pārdošanā, vai kas kā citādi mijiedarbojas ar elektroniskajiem instrumentiem, kurus nodrošina Fabrikam vai kuri tiek iegādāti Fabrikam nolūkiem Fabrikam-Japānas uzņēmumā.
-   **Pneimatiskie instrumenti (PTJPN)** — pušu ieraksti visām pusēm, kas ir iesaistītas pneimatisko instrumentu pirkšanā vai pārdošanā, vai kas kā citādi mijiedarbojas ar pneimatiskajiem instrumentiem, kurus nodrošina Fabrikam vai kuri tiek iegādāti Fabrikam nolūkiem Fabrikam-Japānas uzņēmumā.
-   **Pneimatiskie instrumenti (PTUSA)** — pušu ieraksti visām pusēm, kas ir iesaistītas pneimatisko instrumentu pirkšanā vai pārdošanā, vai kas kā citādi mijiedarbojas ar pneimatiskajiem instrumentiem, kurus nodrošina Fabrikam vai kuri tiek iegādāti Fabrikam nolūkiem Fabrikam-ASV uzņēmumā.

**Lēmums:**

-   Cik daudz papildu adrešu grāmatas jūs izveidosiet?

### <a name="address-book-security"></a>Adrešu grāmatas drošība

Adrešu grāmatas varat izveidot jebkurā laikā, kā arī jebkurā laikā varat iestatīt drošības parametrus šīm adrešu grāmatām. Adrešu grāmatai jums nav obligāti jāiestata drošības privilēģijas, bet ja to nedarāt, tad visi darbinieki jūsu organizācijā var skatīt visus pušu ierakstus šajā adrešu grāmatā. Varat iestatīt drošības privilēģijas attiecībā uz pušu ierakstiem, izmantojot adrešu grāmatas. Drošības privilēģijas ir balstītas uz darba grupām. Šāda pieeja garantē, ka pušu ierakstus kādā adrešu grāmatā var skatīt tikai darbinieki, kas ir piešķirti kādai darba grupai, kurai ir piekļuve šai adrešu grāmatai. Jums ir jāatlasa grupas, kam ir piekļuve katrai adrešu grāmatai. Attiecībā uz katru adrešu grāmatu varat iestatīt drošības privilēģijas, kas ļauj vai liedz piekļuvi noteiktām darba grupām. Ja piešķirat darba grupas privilēģijas attiecībā uz kādu adrešu grāmatu, visi šīs grupas dalībnieki var skatīt ierakstus šajā adrešu grāmatā. Ja kādai adrešu grāmatai nepiešķirat darba grupas piekļuvi, tad šīs grupas dalībnieki nevar skatīt šo adrešu grāmatu vai tās saturu. 

**Lēmums:**

-   Kurām grupām ir piekļuve katrai jaunajai adrešu grāmatai, ko jūs veidosiet?




