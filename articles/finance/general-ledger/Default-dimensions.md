---
title: Finanšu dimensijas un grāmatošana
description: Šajā rakstā skaidroti komponenti, kas veido kontu plānu un kā komponenti darbojas kopā.
author: aprilolson
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 89696f08755a7ff2b01ec7e0cf8550a3b5914bc0
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715475"
---
# <a name="financial-dimensions-and-posting"></a>Finanšu dimensijas un grāmatošana 

[!include [banner](../includes/banner.md)]

Plānojot un iestatot kontu plānu, ir jāņem vērā, kā dažādi komponenti darbosies kopā, kad grāmatosit dokumentu vai žurnālu. Šie komponenti ir konta struktūras, papildu noteikumi un līdzsvarošanas un fiksētās dimensijas. Šajā rakstā ir izskaidrots, kas ir katrs komponents un kā komponenti darbojas kopā.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Kontu plāns un finanšu dimensiju komponenti

Visaptveroša, uz kārtulām balstīta sistēma tiek izmantota galveno kontus un finanšu dimensiju vērtību derīgo kombināciju definēšanai. Šī sadaļa sniegts īss katra komponenta funkcionalitātes apraksts un skaidrots, kur tas atrodams.

### <a name="account-structures"></a>Kontu struktūras

Iestatot virsgrāmatu, ir nepieciešama konta struktūra. Ir jādefinē un jāaktivizē vismaz viena konta struktūra un tā ir jāpiešķir virsgrāmatai. Konta struktūrā ir jābūt galvenajam kontam. Varat definēt uzņēmumam atbilstošāko segmentu secību. Kad ir definēts galvenais konts, sistēma var noteikt izmantoto konta struktūru. Ievietojot galveno kontu kā pirmo vai struktūras priekšplānā, var ierobežot vērtības, kā arī sistēma var lietot pēdējo zināmo derīgo vērtību kā noklusējuma vērtību. Konta struktūrā var būt līdz pat 10 papildu finanšu dimensijām. Konta struktūra nosaka, kuras dimensijas vērtības ir derīgas apvienojumā ar citām vērtībām. Tā arī nosaka, vai ir jāievada dimensijas vērtības.

### <a name="advanced-rules"></a>Papildu noteikumi

Papildu noteikumi ir izvēles komponents, ko var izmantot, iestatot kontu plānu. Konta struktūrai var pievienot neierobežotu skaitu papildu kārtulu. Papildu kārtulas bieži izmanto, lai apstrādātu scenārijus, kuros ir jāizseko papildu finanšu dimensijas gadījumos, kad izpildās īpaši kritēriji. Piemēram, ja izmantojat komandējuma izdevumu kontu, varat izsekot papildu informāciju, piemēram, informāciju par darbinieka apmeklēto pasākumu. Ja ir vairākas papildu kārtulas, tie tiek lietotas alfabētiskā secībā, pamatojoties uz kārtulu nosaukumiem. Kārtulas pievienotus segmentus var lietot tikai pēc konta struktūra segmentiem.

### <a name="balancing-dimension"></a>Līdzsvarošanas dimensijas

Pēc izvēles varat definēt līdzsvarošanas finanšu dimensiju. Lapā **Virsgrāmata** varat definēt finanšu dimensiju, kas ir jālīdzsvaro. Pēc tam ikreiz, kad tiek grāmatotas attiecīgās finanšu dimensijas transakcijas, sistēma automātiski izveido un grāmato ierakstus, lai līdzsvarotu finanšu dimensiju.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Galvenā konta noklusējuma/fiksētās finanšu dimensijas

Noklusējuma dimensijas tiek iegūtas no dažādām vietām, piemēram, šablona ieraksti (piemēram, debitora vai kreditora ieraksti), dokumenta galvenes un galvenais konts. Šajā rakstā ir fokusējas uz noklusētajām dimensijām galvenajā kontā pēc juridiskās personas. Varat definēt, vai galvenajā kontā katrai finanšu dimensijai ir iestatīta vērtība **Nav fiksēts** vai **Fiksēts**, kas tiek izmantota visās virsgrāmatas konta struktūrās. Ja finanšu dimensijai ir iestatīta vērtība **Nav fiksēts**, tiek izmantota noklusējuma vērtība, bet tā var tikt pārrakstīta. Šis princips attiecas uz visām noklusējuma vērtībām sistēmā, pat no šablona ierakstiem iegūtajām noklusējuma vērtībām. Ja finanšu dimensijai ir iestatīta vērtība **Fiksēts**, šī vērtība tiek lietota vienmēr neatkarīgi no tā, vai tas ir iegūta kā noklusējuma vērtība vai to ievadījis lietotājs.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Noklusējuma dimensiju lietošanas secība grāmatošanas procesā

Lietotājiem bieži vien rodas jautājumi par dažādu komponentu darbības secību. Ir ļoti svarīgi izprast secību, kādā tiek lietotas noklusējuma dimensijas, jo šī secība ietekmē iestatīšanas metodi.

> [!NOTE]
> Šī informācija attiecas tikai uz noklusējuma dimensiju lietošanu lietojumprogrammā. Ja importējat datus, izmantojot Microsoft Excel vai datu pārvaldības struktūru, darbība atšķiras.

### <a name="example-1"></a>1. piemērs

**Konta struktūra**

| Galvenais konts            | Biznesa vienība           | Nodaļa              | Izmaksu centrs             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Ir atļautas visas vērtības. | Ir atļautas visas vērtības. | Ir atļautas visas vērtības. | Ir atļautas visas vērtības. |

**Galvenais konts**

| Galvenais konts | Nosaukums          | Juridiska persona | Nodaļa                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Preces pārdošana | USMF         | Fiksēts — 022 Pārdošanas un mārketinga nodaļa |

Tālāk esošajā attēlā parādīta fiksētā noklusējuma dimensija, kas iestatīta galvenajā kontā 401100.

[![Noklusējuma finanšu dimensijas.](./media/default-dimensions.png)](./media/default-dimensions.png)

Šajā pamata piemērā mēs ievadīsim datus virsgrāmatas žurnālā, kam ir iestatīta dimensijas Nodaļa noklusējuma vērtība **023** (Operācijas). Ievadīsim un grāmatosim virsgrāmatas kontu. Šajā attēlā parādīta virsgrāmatas virsraksta noklusējuma finanšu dimensija.

[![Virsgrāmatas žurnāli.](./media/general-journal.png)](./media/general-journal.png)

Noklusējuma dimensijas žurnāla virsrakstā izraisīs to, ka nodaļa 023 tiks lietota pēc noklusējuma pārdošanas kontā rindā. Tālāk esošajā attēlā parādīta virsgrāmatas žurnāla rinda, kur ir lietota noklusējuma dimensijas vērtība **023** no virsraksta.

[![Žurnāla dokuments.](./media/journal-voucher.png)](./media/journal-voucher.png)

Tomēr, grāmatojot rindu, tiek lietota fiksētā dimensija, un rinda tiek grāmatota nodaļā 022. Tālāk esošajā attēlā parādīts grāmatots dokuments, kur pārdošanas kontā ir lietota fiksētā dimensija.

[![Dokumentu darījumi ar lietotām fiksētām dimensijām.](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>2. piemērs

Šajā piemērā tiek lietoti tādi paši iestatījumi kā pirmajā piemērā. Tomēr mēs pievienosim otru komponentu un izmantosim dimensiju Nodaļa kā līdzsvarošanas dimensiju. Tālāk esošajā attēlā vērtība **Nodaļa** ir iestatīta kā USMF virsgrāmatas līdzsvarošanas finanšu dimensija.

[![Ilustrācija, kas parāda deparatmentu kā līdzsvarošanas finanšu dimensiju.](./media/ledger.png)](./media/ledger.png)

Ja tiek lietots viens un tas pats žurnāla virsraksta iestatījums un tiek grāmatota viena un tā pati transakcija, fiksētā dimensija tiek lietota kā pirmā. Pēc tam tiek lietota līdzsvarošanas loģika, kas palīdz nodrošināt, lai katrai nodaļai būtu līdzsvarots ieraksts. Tālāk esošajā attēlā parādītas dokumenta transakcijas, kurās ietverts līdzsvarojošais ieraksts pēc fiksētās dimensijas lietošanas.

[![Dokumentu darījumi pēc līdzsvarošanas ieraksta lietošanas.](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>3. piemērs

Šajā piemērā mēs pievienosim papildu kārtulu. Papildu kārtulu norāda, ka, ja tiek lietots pārdošanas konts 401100 un nodaļa 022 (Pārdošana un mārketings), sistēmai ir jāizseko papildu segments ar nosaukumu Klients.

Šajā piemērā ir svarīga secība. Konta struktūra tiek noteikta pēc galvenā konta ievadīšanas. Ja sniedzat atsauci uz konta struktūras iestatījumiem, sistēma var noteikt, ka ir būtisks galvenais konts, biznesa vienība, nodaļu un izmaksu centrs. Šajā brīdī papildu kārtula nav aktivizēta, jo fiksētās dimensijas netiek lietotas, kamēr grāmatošanas procesā nav lietotas žurnāla dokumenta noklusējuma dimensijas. Tālāk esošajā attēlā nav klientu segmenta, jo papildu kārtulas kritēriji nav izpildīti.

[![Virsgrāmatas konts.](./media/drop-down.png)](./media/drop-down.png)

Grāmatošanas nebūs veiksmīga, jo procesa beigās tika lietota fiksētā dimensija. Dimensijas apstiprināšanas procesā tika konstatēts, ka, ja galvenais konts ir 401100 un nodaļa ir 022, ir nepieciešams segments Debitors. Grāmatošanu nevar veikt apstiprināšanas kļūdas dēļ. Tālāk esošajā attēlā redzams paziņojums, kas tiek paradīts pēc tam, kad dimensijas apstiprināšanas procesā ir konstatēts, ka nepieciešams segments Debitors.

[![Ziņojuma detalizēta informācija.](./media/message.png)](./media/message.png)

Šajā piemērā ir jāpārraksta noklusējuma vērtība tā, lai tiktu aktivizēta papildu kārtula un varētu ievadīt segmentu Debitors. Tomēr šis risinājums ne vienmēr ir iespējams, un daži lietotāji pat nav informēti par grāmatošanas kārtulām. Tāpēc ir svarīgi izprast secību, kādā tiek lietotas noklusējuma dimensijas, iestatot kontu plānu.

Lai panāktu to, varat mainīt konfigurāciju vairākos veidos. Piemēram, varat izveidot jaunu konta struktūru pārdošanas kontiem un struktūrā ietvert segmentu Debitors. Varat arī pievienot papildu rindas esoša konta struktūrā un norādīt galveno kontu, kā arī derīgas nodaļu vērtības. Pēc tam papildu debitora struktūrā ir noderīgi izveidot atsevišķu pārdošanas konta struktūru, kurā ir iekļauts segments Debitors.

## <a name="additional-resources"></a>Papildu resursi 

Daži no tālāk norādītajiem resursiem attiecas uz mūsu programmatūras vecākām versijām. Tomēr liela daļa iepriekšējās versijās sniegtās informācijas un daudzi jēdzieni par noklusējuma dimensiju lietošanu ir tādi paši un joprojām ir spēkā.

[Saskaņoti starpvienību uzskaites žurnāli](example-balanced-journals-interunit-accounting.md)

[Plānot kontu plānu](plan-chart-of-accounts.md) 

[Kontu plāna plānošanas programmā AX 2012 emuārs](/archive/blogs/axsa/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7) — šī saite ved uz septiņu daļu publikāciju sērijas 1. daļu.

[Dimensiju noklusējuma vērtību lietošana uzskaites sadalēs](/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-in-accounting-distributions-part-1-introduction)

[Dimensiju noklusējuma vērtību lietošana dimensiju struktūrā](/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-part-1-financial-dimensions-discovery)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
