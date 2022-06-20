---
title: Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.23. (2022. gada janvāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.23.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: acffe97cf1844f16a70c716a7f2078b1e9a072d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849479"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10023-january-2022"></a>Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.23. (2022. gada janvāris)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti Microsoft Dynamics 365 Supply Chain Management versijā 10.0.23. Šai versijai ir būvējuma numurs 10.0.1037, un tas ir pieejams šeit:

- **Laidiena priekšskatījums:** 2021. gada oktobris
- **Vispārēja laidiena (pašatjauninājums) pieejamība:** 2021. gada decembris
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada janvāris

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Kolonna *Līdzeklis* nodrošina saites uz [izlaišanas plānu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), kur varat redzēt oficiālos izlaišanas datumus katram līdzeklim. Kolonna *Vairāk informācijas* sniedz detalizētu informāciju un/vai saites uz saistīto dokumentāciju. Lai noteiktu, kā ieslēgt līdzekli, skatiet kolonnu *Iespējots pēc*. Papildinformāciju par to, ka izmantot līdzekļu pārvaldību skatiet [Pārskats par līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Mēs varētu atjaunināt šo rakstu, lai ietvertu līdzekļus, kas to veidojās pēc šī raksta sākotnējā publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Globālā adrešu grāmata | Norādīt noklusējuma štatu/provinci katrai valstij/reģionam adreses iestatījumos | Tagad ir iespējams noteikt noklusējuma štatu/provinci katrai valstij/reģionam globālās adrešu grāmatas adrešu iestatījumos. Iestatot noklusēto štatu/provinci, tā būs noklusējuma vērtība, kas tiek ievadīta valsts/rajona laukos, kad tai tiek izveidots jauns apgabala vai pilsētas ieraksts. Skatīt arī [Adreses iestatījumus](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Aktivizēts pēc noklusējuma. |
| Krājumi&nbsp;un&nbsp;loģistika | [Pauzēt uzdevumus mobilajā programmā Warehouse Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Konfigurēt novirzīšanas darbības mobilo ierīču izvēlnes vienumos](../warehousing/warehouse-app-detours.md) | Līdzekļu pārvaldība: (*Warehouse management programmas novirzīšana*) |
| Krājumi&nbsp;un&nbsp;loģistika | [Reklamētie lauki programmā Warehouse](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Konfigurējiet veicinātos laukus darbībām mobilajā ierīcē](../warehousing/warehouse-app-promoted-fields.md)| Līdzekļu pārvaldība (*Warehouse programmas veicinātie lauki*) |
| Ražošana | [Ražošanas izpildes sistēmu integrācija](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-systems-integration) | [Integrācija ar trešās puses ražošanas izpildes sistēmām](../production-control/mes-integration.md) | Līdzekļu pārvaldība (*ražošanas izpildes sistēmas integrācija*) |
| Ražošana | [Pārskats par līdzproduktiem un blakusproduktiem no ražošanas izpildes saskarnes](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Kā nodarbinātie izmanto ražošanas izpildes interfeisu](../production-control/production-floor-execution-use.md) | Līdzekļu pārvaldība (*Pārskats par līdzproduktiem un blakusproduktiem no ražošanas izpildes saskarnes*) |
| Plānošana | [Uz prioritāti balstītas plānošanas optimizācijas atbalsta plānošana](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-priority-based-planning) | [Uz prioritāti balstīta plānošana](../master-planning/planning-optimization/priority-based-planning.md) | Līdzekļu pārvaldība (prioritātes *vadīts MRP atbalsts plānošanas optimizēšanai*) |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidiena jaunie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt jebkuru no šiem līdzekļiem, tas ir jādara [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kur tie ir uzskaitīti, izmantojot nosaukumus, kas parādīti šīs tabulas kolonnā *Līdzekļu nosaukums līdzekļu pārvaldībā*.

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Līdzekļu pārvaldība | Korespondējošie konti izdevumiem darba pasūtījumu žurnālos | Šis līdzeklis ļauj norādīt korespondējošo kontu katram izdevumam, kas uzskaitīts darba pasūtījumu žurnālā. Parasti kreditora kontu var saistīt ar katru izdevumu, bet tiek atbalstīti arī citi kontu tipi. Tā pievieno divas jaunas kolonnas (**Korespondējošā konta tips** un **Korespondējošais konts**) kopsavilkuma cilnei **Izdevumi** lapā **Darba pasūtījumu žurnāls**.|
| Izmaksu pārvaldība | Izveidot saistītas dokumentu summas standarta izmaksu noapaļošanas pārvērtēšanai | <p>Kad tiek veikta krājumu finansiālā grāmatošana (piemēram, pārdošanas pasūtījuma rēķins vai krājumu darbība), šī funkcija liek sistēmai izveidot atsevišķu dokumentu jebkurām saistītām standarta izmaksu noapaļošanas pārvērtēšanām un pievienot to finanšu grāmatošanas dokumentam kā saistīto dokumentu.</p><p>Bez šīs funkcijas sistēma reģistrē standarta izmaksu noapaļošanas pārvērtēšanu vienā un tajā pašā dokumenta grāmatošanā. Šī darbība reizēm var radīt konfliktējošu datuma informāciju, jo pārvērtēšana izmanto sesijas vai sistēmas datumu, bet finanšu grāmatojumi izmanto grāmatošanas datumu.</p> |
| Krājumu un noliktavas pārvaldība | \[Krievija\] Finanšu krājumu darījumi pēc Storno saskaņā ar korekcijas karodziņu pārdošanas pasūtījumu finanšu kuponā | Šis līdzeklis ietekmē kredīta notas labojumu funkcionalitāti Krievijai. Tas ļauj pārdošanas rēķiniem grāmatot krājumu darbības saskaņā ar Virsgrāmatas labojumu opciju. Kad ir aktivizēts šis līdzeklis, starp krājumu darbību finanšu dokumenta **Labošanas** karodziņu un krājumu darbībās **Storno** karodziņu nesakritība vairs nepastāv. |
| Krājumu un noliktavas pārvaldība | (Krievija) Krājumu bilances apgrozījuma pārskata aprēķinu izpilde pakešveidā | Krievijas Supply Chain Management lokalizācijām šis līdzeklis nodrošina iespēju izpildīt *Krājumu bilances apgrozījuma* pārskatus pakešveidā, saglabāt un skatīt iepriekš ģenerētos pārskatus. |
| Krājumu un noliktavas pārvaldība | (Krievija) Krājumu pārvaldībā izmantojiet tulkojumus vietējā valodā valsts/reģiona specifiskajās pamata veidlapās | Krievijas Supply Chain Management lokalizācijām šis līdzeklis sniedz iespēju izmantot krievu valodas tulkojumus produktu/krājumu nosaukumiem un mērvienībām šādās Krievijai raksturīgās krājumu izdrukās: Uzskaites saraksts (INV-3), Uzskaites saraksts (INV-5), Uzskaites saraksts (INV-6). |
| Vispārējā plānošana | Azure algoritmiskās mācīšanās pakalpojums pieprasījuma prognozēšanai | Izmantojot šo līdzekli, Azure datora apmācības pakalpojums var ģenerēt pieprasījuma apjoma prognozes, pamatojoties uz vēsturiskajiem datiem. Papildinformāciju skatiet pieprasījuma [prognozēšanas iestatījumos](../master-planning/demand-forecasting-setup.md). |
| Sagāde un avoti | Pirkšanas pasūtījumu atjauninājumu vēstures tīrīšana | Šis līdzeklis ļauj notīrīt pagaidu vēsturiskos ierakstus, kas ir saistīti ar pirkšanas pasūtījuma atjauninājumiem. Tas pievieno jaunu pogu ar nosaukumu **Pirkšanas atjauninājumu tīrīšanas vēsture** darbību rūtij **Visu pirkšanas pasūtījumu** lapā. Šis līdzeklis ir iespējots pēc noklusējuma. |
| Ražošanas kontrole | (Priekšskatījums) Noliktavā iespējotu materiālu automātiska atlasīšana automātiski grāmatotiem izdošanas sarakstiem | Šis līdzeklis sniedz iespēju automātiski izvēlēties un atrisināt krājumu dimensijas automātiski grāmatotiem, atvasinātiem un atgriezeniskiem izdošanas sarakstu žurnāliem. |
| Ražošanas kontrole | Pārbaudīt izejmateriālu beigu datumu, salīdzinot tos ar plānoto patēriņa datumu | Šis līdzeklis izmaina to, kā tiek validēti partijas beigu datumi, rezervējot izejmateriālu partiju, kas tiks lietota ražošanas laikā. Ja šis līdzeklis ir iespējots, partijas beigu datums tiek pārbaudīts attiecībā pret plānoto patēriņa datumu (izejmateriālu datumu), kā noteikts ražošanas MK rindā vai partijas pasūtījuma formulas rindā. Ja šis līdzeklis ir atspējots, partijas beigu datums tiek pārbaudīts pret plānoto ražošanas vai partijas pasūtījuma piegādes datumu (kā iepriekš). |
| Pārdošana un mārketings | Pārdošanas atjauninājumu vēstures tīrīšana, pamatojoties uz vecumu | Šī funkcija ļauj iestatīt maksimālo ierakstu vecumu, kas jāsaglabā, palaižot pārdošanas **atjaunināšanas vēstures tīrīšanas** periodisko uzdevumu. Vecāki ieraksti tiks dzēsti. Tas noder, iestatot uzdevumu periodiskai izpildei, jo vecums vienmēr tiek aprēķināts attiecībā pret uzdevuma palaišanas datumu. Bez šīs funkcionalitātes var iestatīt tikai specifisku datumu vecākajiem ierakstiem, kas jāsaglabā. Papildinformāciju skatiet pārdošanas [vēstures datu plānošanas sadaļā](../sales-marketing/sales-update-history-cleanup-performance-improvements.md). |
| Pārdošana un mārketings | “100 populārāko” klientu pārskata veiktspējas uzlabošana | Šis līdzeklis uzlabo **100 populārāko** debitoru pārskata veiktspēju, vienmēr palaižot pārskatu visiem debitoriem (kas ir paredzēts lietošanai), nevis pieļaujot pielāgotos vaicājumus. Ja šis līdzeklis ir aktivizēts, visi **Iekļaujamo ierakstu** iestatījumi, tiek atspējoti **100 populārāko** pārskata dialogā. |
| Noliktavas vadība | Mērogoto vienību atbalsts izlaišanai izejošo pasūtījumu noliktavā | Kad šis līdzeklis ir iespējots, izejošos pasūtījumus var izlaist no centrmezgla tieši mērogotajā vienībā, kur pasūtījumi tiks izpildīti. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Mēs nesen pievienojam vai būtiski atjauninājām šādus palīdzības rakstus. Šiem rakstiem nav obligāti jābūt saistītiem ar jaunajiem līdzekļiem, kas tika pievienoti šim laidienam, kā norādīts iepriekšējā sadaļā. Tomēr tie var palīdzēt iegūt vairāk no esošajiem līdzekļiem.

| Līdzekļu apgabals | Jauni vai atjaunināti raksti |
|---|---|
| Tehnisko izmaiņu pārvaldība | [Tehniskie atribūti un tehnisko atribūtu meklēšana](../engineering-change-management/engineering-attributes-and-search.md) tagad tiek aprakstīts, kā darbojas tehniskā atribūta pārmantošana. |
| Vispārējā plānošana | [Vispārējā plānošana ar pieprasījuma apjoma prognozēm](../master-planning/planning-optimization/demand-forecast.md) un [Prognozes samazināšanas principi](../master-planning/reduction-keys.md) tagad sniedz plašāku informāciju par to, kā strādāt ar samazināšanas principiem. |
| Vispārējā plānošana | [Krājumu drošības rezerves izpilde](../master-planning/safety-stock-replenishment.md) tagad sniedz papildu informāciju par minimuma/maksimuma atslēgu lietošanu. |
| Vispārējā plānošana | [Krājumu prognozes](../master-planning/inventory-forecast.md) tagad sniedz papildu informāciju par prognožu piešķiršanu. |
| Vispārējā plānošana | [Piegādes grafiks](../master-planning/supply-schedule.md) |
| Noliktavas vadība | [Globālie mobilās ierīces parametri](../warehousing/mobile-device-parameters.md) |
| Noliktavas vadība | [Noenkurošana](../warehousing/anchoring.md) |
| Pārdošana un mārketings | Starpuzņēmumu tirdzniecība tagad ir detalizēti aprakstīta, sākot [ar starpuzņēmumu tirdzniecības iestatīšanas](../sales-marketing/intercompany-trade-set-up.md) un ar to saistītajiem rakstiem. |
| Pārdošana un mārketings | [Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumi](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Krājumu vadība | Krājumu redzamības dokumentācija ir izvērsta un atjaunināta, [sākot ar krājumu redzamības pievienojumprogrammas apskatu](../inventory/inventory-visibility.md) un ar to saistītajiem rakstiem. |
| Noliktavas vadība | [Mobilās ierīces lietotāju konti](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.23 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet [Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā 10.0.23 (2021. gada novembrī](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md)).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.23, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 un rūpniecības mākoņi: 2021. gada 2. laidiena plāns

Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Apskatiet [Dynamics 365 un rūpniecības mākoņi: 2021. gada 2. laidiena plāns](/dynamics365-release-plan/2021wave2/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Noņemtie un novecojušie Supply Chain Management līdzekļi

Noņemtie [vai novecojušie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) rakstā apraksta funkcijas, kas ir noņemtas vai ieplānotas izņemšanai vai nolietojumam Piegādes ķēžu pārvaldībai.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda līdzekļa noņemšanas no preces paziņojums [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) par nolietojumu tiks papildu pievienots 12. rakstu funkcionalitātes Noņemtie vai novecojušie 12 mēnešu skaits pirms noņemšanas.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
