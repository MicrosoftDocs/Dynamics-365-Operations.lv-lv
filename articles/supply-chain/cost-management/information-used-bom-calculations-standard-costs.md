---
title: Informācija, kas tiek izmantota MK aprēķinos ar standarta izmaksām
description: Lai aprēķinātu saražotā krājuma standarta izmaksas, materiālu komplektu (MK) aprēķini izmanto vairāku avotu datus. Avoti ietver informāciju par krājumiem, komplektu maršrutēšanu, netiešo izmaksu aprēķina formulas un aprēķina versiju.
author: AndersGirke
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b1aa33c11f7cfbbde2a278bef25189ac697d19
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575127"
---
# <a name="information-used-in-bom-calculations-with-standard-costs"></a>Informācija, kas tiek izmantota MK aprēķinos ar standarta izmaksām

[!include [banner](../includes/banner.md)]

Lai aprēķinātu saražotā krājuma standarta izmaksas, materiālu komplektu (MK) aprēķini izmanto vairāku avotu datus. Avoti ietver informāciju par krājumiem, komplektu maršrutēšanu, netiešo izmaksu aprēķina formulas un aprēķina versiju.

Iepirktā krājuma informācija, kas tiek izmantota standarta izmaksu MK aprēķinā, ietver sekojošo:
-   Izmaksas — iepirkto krājumu izmaksas tiek saglabātas, kā vietai raksturīgi ieraksti standarta izmaksu aprēķina versijā. Katram izmaksu ierakstam ir spēkā esošs datums, un MK aprēķina datums nosaka, kurš izmaksu ieraksts tiks izmantots. Piemēram, MK aprēķins ar turpmāko aprēķina datumu var izmanto izmaksu ierakstu ar nepabeigtu statusu un turpmāko spēkā esošo datumu.
-   Izmaksu grupa − izmaksu grupa, kas tiek piešķirta iepirktajam krājumam, nodrošina pamatu izmaksu segmentācijai saražotā krājuma aprēķinātajās izmaksās.
-   Brīdinājuma nosacījumi, kas iegulti krājuma MK aprēķina grupā, aktivizē MK aprēķinu, lai noteiktu potenciālās problēmas. Tas var būt, kad iepirktajam krājumam ir nulles izmaksas, nulles daudzums materiālu komplektā (MK) vai novecojis izmaksu ieraksts. Inicializējot MK aprēķinu, piemērotos brīdinājuma nosacījumus var ignorēt.

Saražotā krājuma informācija, kas tiek izmantota standarta izmaksu MK aprēķinā, ietver sekojošo:
-   Krājuma standarta pasūtījuma daudzums — krājuma standarta pasūtījuma daudzums (krājumam) darbojas, kā noklusējuma uzskaites partijas apjoms pastāvīgu izmaksu amortizēšanai MK aprēķinā. Uzskaites partijas apjoms atspoguļos arī pasūtījuma apjoma daudzumu, ja norādīts.
-   Brīdinājuma nosacījumi, kas iegulti krājuma MK aprēķina grupā, aktivizē MK aprēķinu, lai noteiktu potenciālās problēmas. Viens piemērs varētu būt šāds: ražotajam krājumam nav MK vai maršruta. Inicializējot MK aprēķinu, piemērotos brīdinājuma nosacījumus var ignorēt.

Materiālu komplekta informācija, kas tiek izmantota standarta izmaksu MK aprēķinā, ietver sekojošo:
-   MK versija − MK versija, kas tiek piešķirta saražotajam krājumam, ir spēkā esoša no un līdz datumiem, un tai ir apstiprināts un aktīvs statuss. Komplekta versija var būt uzņēmuma plaši izmantota vai raksturīga vietai, un tā var izvēles veidā atspoguļot daudzuma pārtraukumpunktus.
-   MK rindas krājuma daudzums − parasti sastāvdaļai ir nepieciešams dažāds daudzums, bet tas var arī būt konstants. Sastāvdaļas kvalitāte parasti tiek izteikta viena pamatkrājuma ražošanai, bet var būt izteikta uz 100 vai 1000, lai rīkotos ar decimālu precizitātes iznākumiem. Sastāvdaļas daudzumu var arī aprēķināt, balstoties uz mērījumiem.
-   MK rindas krājuma brāķis − sastāvdaļai var būt mainīgs vai konstants daudzums plānotajam brāķim.
-   MK rindas krājuma spēkā esošie datumi − sastāvdaļa var būt spēkā no un līdz datumiem.
-   MK rindas krājuma ražošanas tips — partijas apjoma aprēķins nemainīgu izmaksu amortizācijai atspoguļos MK aprēķina daudzumu un izpildes pēc pasūtījuma izvēršanas režīmu, jo MK aprēķins pieņem, ka saražotā sastāvdaļa tiks ražota precīzā daudzumā (nevis tā standarta pasūtījuma daudzumā).
-   Pakārtotais MK saražotajai sastāvdaļai − izvēles veidā saražotajai sastāvdaļai var būt noteikta MK versija, kas tiktu izmantota krājuma pašreizējās aktīvās MK versijas vietā MK aprēķinā.
-   Pakārtotais maršruts saražotajai sastāvdaļai - izvēles veidā saražotajai sastāvdaļai var būt noteikta maršruta versija, kas tiktu izmantota krājuma pašreizējās aktīvās maršruta versijas vietā MK aprēķinā.
-   Operācijas numurs un operāciju brāķu procentu ietekme − operācijas numurs sasaista sastāvdaļu ar specifisku operāciju, un operācijām var būt brāķu procenti. Savienojums ļauj MK aprēķiniem aprēķināt brāķa procentus un kopīgos brāķa procentus (no vairākām operācijām) sastāvdaļas nepieciešamajā daudzumā.
-   Ignorējiet MK rindu krājumu izmaksu aprēķinos − sastāvdaļu var ignorēt MK aprēķinu mērķiem.

Operācijas resursu informācija, kas tiek izmantota standarta izmaksu MK aprēķinā, ietver:
-   Stundas izmaksas — stundas izmaksas, kas saistītas operācijas resursiem, ir izteiktas izmaksu kategoriju izteiksmē, un šīs kategorijas tiek piešķirtas uzstādīšanas laikam un izpildes laikam. Šīs izmaksu kategorijas ir jānosaka resursu grupām un operācijas resursiem. Stundas izmaksas, kas tiek saistītas ar izmaksu kategoriju, var būt vietas raksturīgas vai plaši izmantotas uzņēmumā.
-   Izmaksas uz vienu vienību — dažas ražošanas vides piešķir operācijas resursus uz vienu ražošanas vienību, kas būs izteikta, kā atsevišķa izmaksu kategorija daudzumam. Piemēram, uz daudzuma attiecināmās izmaksas var atspoguļot gabaldarba likmes darbaspēkam, vai krāsu ražotājs var piešķirt operācijas resursus uz vienu ražojumu galonu.
-   Operācijas resursu informācijas ignorēšana par maršrutēšanas darbībām — resursu informācija par izmaksu kategorijām tiks pārmantota ar darbībām, kur to var ignorēt. MK aprēķini izmantos izmaksu kategorijas informāciju, kas norādīta maršrutēšanas darbībām.
-   Izmaksu grupa izmaksu kategorijai − izmaksu grupa, kas ir piešķirta izmaksu kategorijai, nodrošina izmaksu segmentāciju saražotā krājuma aprēķinātajās izmaksās. Piemēram, atšķirīgas izmaksu grupas var tik izmantotas, lai segmentētu aprēķinātās izmaksas, kas tiek saistītas ar mašīnām un darbaspēku vai ar iestatīšanas un izpildes laiku.

Maršruta informācija, kas tiek izmantota standarta izmaksu MK aprēķinā, ietver:
-   Maršruta versija - maršruta versija, kas tiek piešķirta saražotajam krājumam, ir spēkā esoša no un līdz datumiem, un tai ir apstiprināts un aktīvs statuss. Maršruta versijai ir jābūt uzņēmuma plaši izmantotai vai raksturīgai vietai, un tā var izvēles veidā atspoguļot daudzuma pārtraukumpunktus.
-   Maršrutēšanas operāciju laiks − laiku var noteikt izpildes laikam un uzstādīšanas laikam. Stundas laiks parasti tiek izteikts viena pamatkrājuma ražošanai, bet var būt izteikts uz 100 vai 1000, lai rīkotos ar decimālu precizitātes iznākumiem.
-   Maršrutēšanas darbības laiks sekundārajiem resursiem — sekundārajam resursam ir tas pats operācijas numurs, kā primārajam resursam, un tam ir tas pats maršrutēšanas darbības laiks. Piemēram, operācijai var būt nepieciešama mašīna, kā primārais resurss, un darbaspēks un rīki, kā sekundārie resursi.
-   Maršrutēšanas darbības brāķa procenti —MK aprēķini aprēķinās brāķa procentus un kopīgos brāķa procentus no vairākām operācijām. Tas attiecas uz nepieciešamo maršrutēšanas operāciju laiku un nepieciešamo komponentu daudzumu, kas saistīts ar operācijas numuriem.
-   Izmaksu kategorijas maršrutēšanas operācijai — operāciju resursu informācija par izmaksu kategorijām tiks pārmantota ar darbībām, kur to var ignorēt. MK aprēķini izmantos izmaksu kategorijas informāciju, kas norādīta maršrutēšanas operācijām.

Ražošanas papildu atbalsta informācija, kas tiek izmantota standarta izmaksu MK aprēķinā, ietver:
-   Piemaksa − piemaksu aprēķina formula atspoguļo vērtību procentos, piemēram, 100 procenti, kas tiek piesaistīta specifiskai izmaksu grupai, piemēram, darbaspēkam.
-   Likme − likmes aprēķina formula atspoguļo summu uz vienu vienību, piemēram, 10,00 USD stundā, kas tiek piesaistīta specifiskai izmaksu grupai, piemēram, darbaspēkam.
-   Uz laiku balstīts pret uz materiālu balstīts papildu atbalsts − ražošanas papildu atbalstu var piesaistīt maršrutēšanas darbībām vai materiālu komponentiem.

Aprēķina versijas informācija, kas tiek izmantota standarta izmaksu MK aprēķinā, ietver sekojošo:
-   Aprēķina tips — izmaksu versijai ir jāietver standarta izmaksas. Uz tiek MK aprēķiniem, kuros izmanto standarta izmaksas, attiecas vairāki ierobežojumi. Piemēram, šie ierobežojumi norāda, ka papildmaksas jāietver vienību izmaksās un MK aprēķina izvēršanas režīmam jābūt vienam līmenim.
-   Sankcionētais regresa princips – aprēķina versija var sankcionēt regresa principa izmantošanu, piemēram, specifiskās aprēķina versijas vai aktīvo izmaksu ierakstu izmantošana. Parasti sankcionēts regresa princips attiecas uz aprēķina versiju, kas parāda inkrementālos atjauninājumus divu versiju pieejā izmaksu atjauninājumiem.
-   Bloķēšanas karodziņš nepabeigtām izmaksām − bloķēšanas karodziņš var novērst nepabeigtu izmaksu MK aprēķinus saražotiem krājumiem.
-   Noteikts no datuma − noteikts no datuma rīkosies, kā noklusējuma aprēķina datums visiem MK aprēķiniem, kas ietver aprēķina versiju.
-   Noteikta vieta − noteikta vieta ierobežos MK aprēķinus vienā vietā.
-   Aprēķinu versijas saturam ir jāietver izmaksas − saturam ir jāietver izmaksas. Izvēles veidā tas var ietvert pārdošanas cenas, lai aprēķinātu ieteicamās pārdošanas cenas saražotajiem krājumiem.

Vairākus informācijas avotus var norādīt, inicializējot MK aprēķinu. Tas ietver vietu, aprēķina datumu un aprēķina versiju.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]