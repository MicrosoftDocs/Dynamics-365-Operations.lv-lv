---
title: Bieži uzdotie jautājumi par Commerce katalogiem B2B vietnēm
description: Šajā rakstā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Commerce katalogiem.
author: ashishmsft
ms.date: 07/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 68c648c5caf2667f413b236dc437fc2c74c40d07
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168990"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>Bieži uzdotie jautājumi par Commerce katalogiem B2B vietnēm

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegtas atbildes uz bieži uzdotiem Microsoft Dynamics 365 Commerce [jautājumiem par "bizness-biznesam" katalogiem](catalogs-b2b-sites.md).

### <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Kādēļ es nevaru konfigurēt katalogam raksturīgu navigācijas hierarhiju vai skatīt opciju, lai saistītu debitora hierarhiju?

Nodrošiniet, **lai Commerce headquarters** **līdzekļu pārvaldības darbvietā iespējotu vairāku katalogu izmantošanu mazumtirdzniecības kanālos**, un jūsu vide ir Commerce versija 10.0.27 vai jaunāka tās izlaide. Pārliecinieties, ka esat atlasījis **B2B** zem **kataloga tipa**.

### <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Vai es varētu skatīt katalogam raksturīgo hierarhiju un bagātināt kategoriju lapas Commerce Site Builder?

Jā, Komercijas vietnes veidotāja lietotāji, kuriem **ir** pieeja lapai Preces vietas veidotājā, var atlasīt katalogu un skatīt katalogam raksturīgo hierarhiju. **Lapā Preces** lietotāji var arī bagātināt kategorijas lapu noteiktai kategorijai katalogā. Plašāku informāciju skatiet tēmā [Kategorijas ielādes lapas bagātināšana](enrich-category-page.md). Ja vēlaties bagātināšanu, kas ir raksturīga katalogam, ieteicams šim katalogam izveidot atšķirīgu un unikālu navigācijas hierarhiju.

### <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Vai vienā kasē var veikt B2B ražotnes pirkumu no vairākiem katalogiem?

Jā, ir atļauts veikt pirkumus no vairākiem katalogiem vienā paņemšanu. B2B ražotnes var izmantot kataloga indikatoru groza skatā, lai noteiktu, no kuriem krājumiem tika pievienoti katalogi.

### <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Ja B2B ražotne iegādājas vienu krājumu no dažādiem katalogiem, kāda ir paredzamā uzvedība?

Lai arī dotam lietotājam, iespējams, ir piekļuve vairākiem katalogiem konkrētā laikā, paredzams, ka preces šajos katalogos būs savstarpēji izslēdzošas. Citiem vārdiem sakot, ideālā veidā, viena prece vienam lietotājam nedrīkst būt daļa no vairākiem katalogiem.

Tomēr, ja rodas situācija, kad viena prece pieder vairākiem katalogiem, sistēma šai precei uzturēs vairākas groza rindas. Katram katalogam būs atsevišķa rinda. Izdrukas laikā netiks sapludināta viena un tā pati prece no diviem dažādiem katalogiem.

### <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Kad B2B ražotne iepirkties, vai ir kāda kataloga pieejamības pārbaude?

Jā. B2B ražotnei būs atļauts veikt paņemšanu tikai tad, ja visi grozā eskalācijas krājumi ir no derīgiem katalogiem. Ja kāda groza krājumiem ir beidzies derīgums vai atsaukti katalogi, tie tiks noņemti, un lietotājs tiks informēts.

### <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Vai iepirkumu pieredzes laikā ir katalogam raksturīgi meklēšanas un preču atklājumi (tostarp saistītās un rekomendētās preču kolekcijas)?

Jā. Tiklīdz lietotājs atlasa noteiktu katalogu, visa iepirkumu katalogā kļūst katalogam raksturīga. Šajā ceļojuma laikā ir ietverta preču atklājumu pieredze, piemēram, meklēšanas ieteikumi, meklēšanas rezultāti, kategoriju rezultāti, uzlabotāji, cenu noteikšana, atribūti un ieteiktās preces (piemēram, jauni, labākais pārdošanas veids, tendences, bieži pirkti kopā un saistītie produkti).

### <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Vai B2B ražotnes pirkumu var iegādāties no noklusējuma preču klāsta (catalogID=0)?

Nē, B2B shopper nav atļauts iegādāties no noklusējuma klāsta. Šis preču klāsts ir paredzēts tikai anonīmai pārlūkošanai. Ja B2B ražotnei nav piešķires (no administrēšanas gaida atjauninājumus), viņi nevarēs skatīt katalogus, kurus var izvēlēties, un kategoriju hierarhija būs redzama.

### <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Vai mārketinga saturu var izmantot precei, kas ir raksturīga katalogam?

Pašlaik preču bagātināšana tiek atbalstīta tikai vietas un kanāla līmenī. Citiem vārdiem, ja prece ir bagātināta un tiek koplietota vairākos katalogos, attiecīgā bagātinātās preces informācijas lapa (PDP) attiecībā uz šo preci tiks atveidota tāpat visās attiecīgās vietas katalogos. 

### <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Vai kataloga atbalsts ir pieejams gan B2B, gan "bizness-patērētājam" (B2C) tiešsaistes kanāliem?

Pašlaik commerce katalogi ir paredzēti darbam tikai ar B2B tiešsaistes kanāliem.

### <a name="a-new-customer-was-added-to-the-customer-hierarchy-or-a-new-hierarchy-was-associated-with-the-catalog-but-the-catalog-is-not-available-to-the-user-why"></a>Ar katalogu tika pievienots jauns debitors, vai ar katalogu tika saistīta jauna hierarhija, taču lietotājam nav pieejams katalogs. Kādēļ?

Pārliecinieties, ka esat izpildījuši **1010** darbus pēc tam, kad jaunais debitors ir saistīts ar esošo debitoru hierarhiju, un kad izveidojāt jauno debitoru hierarhiju. Ar debitoru hierarhiju saistītie katalogi būs redzami tikai pēc **1010** darba veiksmīgas pabeigšanas. Ja katalogs ir arī jauns, nodrošiniet, **lai tiktuos 1150** (kataloga) **darbs, kā arī 1010** darbi. Tāpat kā jebkuram jaunam katalogam, atļaujiet kādu laiku datu sinhronizācijai ar kanālu un meklēšanas indeksu. Ja darba statuss ir Pielietots, tas nozīmē, ka dati tiek sinhronizēti ar kanāla datu bāzi, bet ir nepieciešams papildu laiks, lai dati sinhronizētu ar meklēšanas indeksu. 

### <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Vai mēs varam iestatīt katalogam raksturīgus pārdošanas/šķērspārd pārdošanas krājumus?

Pašlaik tiek atbalstīta tikai saistīto preču funkcionalitāte. Tomēr zvanu centriem ir pieejamas upsell un šķērspārd pārdošanas krājumu konfigurācijas.

Šādas funkcijas tiek atbalstītas arī tikai zvanu centriem:

- Kataloga avotu kodi
- Avota DATU lietošana, lai izsekotu izmaksas un atbilžu likmes
- Katalogam raksturīgi pasūtījuma un krājumu skripti
- Kataloga lapas analīze
- Kataloga pieprasījumi
- Maksājumu grafiki
- Bezmaksas preces, balstītas uz pirmkodiem

### <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Vai mēs varam izmantot kataloga pirmkodus B2B pasūtījumiem, izmantojot e-komercijas portālu?

Nē. Kataloga avota kodi tiek atbalstīti tikai zvanu centra kanāliem.

## <a name="additional-resources"></a>Papildu resursi

[Commerce katalogu izveide B2B vietnēm](catalogs-b2b-sites.md)

[Kataloga izdošanas modulis](catalog-picker.md)

[Commerce katalogu paplašināmības ietekme B2B pielāgojumiem](catalogs-b2b-sites-dev.md)
