---
title: Dynamics 365 Supply Chain Management versijas 10.0.25 priekšskatījums (2022. gada aprīlis)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.25.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 0ce9bc4685542cf691d862c0fec76f3f7b40c6b6
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087324"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>Dynamics 365 Supply Chain Management versijas 10.0.25 priekšskatījums (2022. gada aprīlis)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā uzskaitīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti Microsoft Dynamics 365 Supply Chain Management versijas 10.0.25 priekšskatījumā. Šai versijai ir būvējuma numurs 10.0.1149, un tas ir pieejams šeit:

- **Priekšskatījuma laidiens:** 2022. gada februāris
- **Vispārēja laidiena (paša veikts atjauninājums) pieejamība:** 2022. gada marts
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada aprīlis

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo tēmu, lai iekļautu līdzekļus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Līdzekļu apgabals | Funkcija | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Krājumi&nbsp;un&nbsp;loģistika | Bīstamo materiālu uzlabojumi | Šie uzlabojumi balstās uz esošo bīstamo materiālu funkcionalitāti, lai labāk palīdzētu uzņēmumiem ievērot vietējos noteikumus, transportējot bīstamos materiālus dažādās ģeogrāfiskās vietās. <!-- KFM: Update to 2022w1 link when published -->| Funkciju pārvaldība:<br>*Bīstamo materiālu uzlabojumi* |
| Krājumi&nbsp;un&nbsp;loģistika | Iepakošanas darbs pakošanas stacijām | Šī funkcija ievērojami uzlabo jūsu iepakošanas un nosūtīšanas darbību elastību un veiklību. Iepakošanas procesa laikā noliktavas darbinieki tagad var iepakot un nosūtīt atsevišķas pakas, kas saistītas ar vienu un to pašu sūtījumu un kravu. Pasūtījuma rindas, kas ir viena un tā paša sūtījuma daļa, nav obligāti jānosūta kopā, ja dažas preces ir gatavas nosūtīšanai uzreiz. Vienu pasūtījumu var iepakot un nosūtīt vairākās pakās dažādos piegādes laikos, tādējādi samazinot gaidīšanas laiku un palielinot veiklību.<!-- KFM: Update to 2022w1 link when published --> | Funkciju pārvaldība:<br>*Iepakošanas darbs pakošanas stacijām* |
| Krājumi&nbsp;un&nbsp;loģistika | [Skenēt svītrkodus noliktavā, izmantojot GS1 formāta standartus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) <!-- KFM: Update to 2022w1 link when published --> | [GS1 svītrkodi un QR kodi](../warehousing/gs1-barcodes.md) | Funkciju pārvaldība:<br>*Skenēt GS1 svītrkodus* |
| Ražošana | [Materiālu patēriņš un rezervācijas ražošanas grīdas izpildes saskarnē](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Kā nodarbinātie izmanto ražošanas izpildes interfeisu](../production-control/production-floor-execution-use.md) | Funkciju pārvaldība:<br>*(Priekšskatījums) Reģistrēt materiālu patēriņu ražošanas izpildes interfeisā (WMS iespējots)* |
| Ražošana | [Reģistrēt materiālu patēriņu uz mēroga vienībām](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Ražošanas izpildes darba slodzes mākoņa un malas mēroga vienībām](../cloud-edge/cloud-edge-workload-manufacturing.md) | Funkciju pārvaldība:<br>*Reģistrēt materiālu patēriņu mērogošanas vienībā mobilajā programmā* |
| Plānošana | [Plānošana Optimizācijas ieteikumi, lai optimizētu esošo piedāvājumu](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Optimizācijas priekšlikumi](../master-planning/action-messages.md) | Iespējots pēc noklusējuma |
| Plānošana | Plānotie pasūtījumi vienkāršoti | [Plānotie pasūtījumi vienkāršoti](../master-planning/planning-optimization/planned-orders-simplified.md ) | Funkciju pārvaldība:<br>*Plānotie pasūtījumi vienkāršoti* |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt kādu no šīm funkcijām, tas jādara iekšā [funkciju pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Krājumu un noliktavas pārvaldība | (Polija) Ļauj saistīt vairākus SAD rēķinus ar vienu pirkšanas pasūtījuma rindu vienā SAD | Šis līdzeklis ļauj sadalīt pirkšanas pasūtījuma rindas un saistīt tās ar vienu administratīvo dokumentu (VAD), kad šīs pirkšanas pasūtījuma rindas tika grāmatotas vairākiem dažādiem rēķiniem (piemēram, dažādiem sūtījumiem). |
| Sagāde un avoti | Apvienot vairākus pirkšanas pieprasījumus vienā pirkšanas pasūtījumā pēc uzskaites datuma | Šis līdzeklis ļauj apvienot vairākus pirkšanas pieprasījumus vienā pirkšanas pasūtījumā, ja dažādiem pirkšanas pieprasījumiem ir atšķirīgi uzskaites datumi. Pirkšanas pasūtījuma izveides un pieprasījuma konsolidācijas pirkšanas politikas noteikumus var iestatīt, lai automatizētu lēmumu par pieprasījumu rindu grupēšanu pēc uzskaites datuma pirkšanas pasūtījuma līmenī. Pirkuma pasūtījuma konsolidācija pēc uzskaites datuma netiek atbalstīta, ja ir iespējota budžeta kontrole, jo uzskaites datums tiek izmantots budžeta rezervācijām un apgrūtinājumiem. Tāpēc tas ir jāsaglabā, pārejot no pirkšanas pieprasījuma uz pirkšanas pasūtījumu. |
| Sagāde un avoti | Atspējot pirkšanas pieprasījuma izplatīšanas atiestatīšanas pogu | Šī funkcija atspējo **Atiestatīt** pogu uz **Grāmatvedības sadale** lapa pirkuma pieprasījumiem, kas tiek izskatīti. |
| Sagāde un avoti | Parādīt mantotos noklusējuma PP atbildes lauka iestatījumus | Šis līdzeklis atkārtoti ievieš mantotos noklusētos piedāvājuma pieprasījuma (RFQ) atbildes lauka iestatījumus, kas iepriekš tika noņemti no lietotāja interfeisa. Šie iestatījumi nenodrošina nekādu funkcionalitāti, taču tos var pielāgot, lai nodrošinātu to pēc vajadzības. Iespējojiet šo līdzekli, ja jūsu organizācija jau ir pievienojusi funkcionalitāti noklusējuma RFQ atbildes lauka iestatījumiem vai plāno to darīt. Kad šī funkcija ir iespējota, varat piekļūt iestatījumiem, dodoties uz **Iepirkuma un ieguves parametri** lapu, atverot **Piedāvājuma pieprasījums** cilni un atlasot **Noklusējuma pieprasījuma atbildes lauki piedāvājumam**. |
| Sagāde un avoti | Sapludināt kreditora finanšu dimensijas ar aktīvās dimensijas saites finanšu dimensiju pirkšanas pasūtījumā | Šis līdzeklis ļauj sapludināt piegādātāju finanšu dimensijas ar aktīvām dimensiju saites finanšu dimensijām pēc pirkuma pieprasījuma apstiprināšanas, ja iestatāt saikni starp finanšu dimensiju un vietnes krājumu dimensiju. Pirkšanas pasūtījuma izveides un pieprasījuma konsolidācijas pirkšanas politikas noteikumus var iestatīt, lai pieņemtu lēmumu par finanšu dimensiju sapludināšanu no piegādātājiem ar aktīvu dimensiju saites finanšu dimensiju pirkuma pasūtījuma galvenes līmenī. |
| Ražošanas kontrole | (Krievija) Iespējot noklusējuma atrašanās vietas iestatīšanu ražošanas formulai/BOM un automātisku GTD rezervēšanu/patēriņu ražošanā | Funkcija nodrošina papildu iespējas ražošanai no importētajām izejvielām (tikai krievu lokalizācija):<ul><li>Iespēja iestatīt automātisko noklusējuma atrašanās vietu ražošanas formulām un materiālu rēķiniem gan resursu grupās, gan noliktavās.</li><li>Automātiska izejvielu rezervēšana, ko veic *GTD numurs* dimensija WMS aktivizētās noliktavās saskaņā ar rezervēšanas algoritmu, kas nav WMS. Tas attiecas uz gadījumiem, kad darba politika *Izejvielu savākšana* pastāv ar **Darba veidošanas metode** iestatīts uz *Nekad* un noliktavas, atrašanās vietas un preces numura iestatījums atbilst ražošanas (partijas) pasūtījuma krājumu darījumiem.</li><li>Automātisks izejvielu patēriņš līdz *GTD numurs* izmērs pēc komplektēšanas saraksta publicēšanas atbilstoši iepriekš aprakstītajai iegūtajai rezervācijai.</li></ul> |
| Noliktavas vadība | Sagaidāmā saņemšana no kvalitātes pārbaudes pasūtījumiem, kas izmanto aizturēto krājumu paraugus — atspējošana | Šis līdzeklis neļauj sistēmai izveidot paredzamās saņemšanas transakcijas kvalitatīviem pasūtījumiem, kuros krājumu paraugs ir bloķēšanas statuss. Tā kā bloķētie krājumi nav pieejami, šī funkcija noņem paredzētās kvītis. Tas palīdz nodrošināt, ka krājumi nebeidzas ar vairākiem bloķēšanas statusiem, kas var izraisīt datu integritātes problēmas. |
| Noliktavas vadība | (Priekšskatījums) Mērogošanas vienības atbalsts ienākošajiem un izejošajiem noliktavas pasūtījumiem | Šis līdzeklis liek sistēmai izveidot izejošos noliktavas pasūtījumus izlaišanas noliktavā procesa laikā un izveidot ienākošos noliktavas pasūtījumus, kad pārsūtīšanas pasūtījumi tiek grāmatoti kā nosūtīti. Pēc tam sistēma sinhronizē katru ienākošo vai izejošo noliktavas pasūtījumu ar mēroga vienību, kas ir atbildīga par pasūtījuma nosūtīšanu vai saņemšanu. Ņemiet vērā, ka pēc šīs funkcijas iespējošanas jūsu noliktavas izpildes slodzes ir jājaunina. Plašāku informāciju skatiet rakstā [Mākoņa un malas mēroga vienības ražošanas izpilde](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Šai funkcijai ir nepieciešams *Atsaistīt nolikto darbu no ASN* funkciju un nodrošinās iespēju saņemt pārsūtīšanas pasūtījumus, izmantojot numura zīmes saņemšanas procesu mobilajā lietotnē Warehouse Management. |

## <a name="feature-state-changes-in-this-release"></a>Funkcijas stāvokļa izmaiņas šajā laidienā

Šajā tabulā ir uzskaitīti līdzekļi, kas kļuva obligāti vai ieslēgti pēc noklusējuma, sākot ar 10.0.25. Visas šīs funkcijas tiks automātiski ieslēgtas jūsu sistēmā, tiklīdz atjaunināsit uz 10.0.25. Obligātās funkcijas nevar izslēgt, taču funkcijas, kas ir ieslēgtas pēc noklusējuma, joprojām var izslēgt, izmantojot [Funkciju pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabulā ir arī uzskaitīti līdzekļi, kas iepriekš bija publiskajā priekšskatījumā, bet ir mainījušies, lai kļūtu vispārēji pieejami versijā 10.0.25, kas nozīmē, ka tagad tos ieteicams izmantot ražošanas vidēs. Šīs funkcijas pēc noklusējuma ir izslēgtas, ja vien nav norādīts citādi, tāpēc jums tas ir jāizmanto [Funkciju pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lai tos iespējotu, ja vēlaties tos izmantot.

| Modulis | Līdzekļa nosaukums | Līdzekļa statuss |
| --- | --- | --- |
| Līdzekļu pārvaldība | Lietot kārtulas darba pasūtījumu grupēšanas, kad tiek izpildīts uzturēšanas plāns | Vispārēji pieejams |
| Līdzekļu pārvaldība | Uz skaitītāju balstīti uzturēšanas uzlabojumi | Vispārēji pieejams |
| Izmaksu pārvaldība | Izmaksu aprēķina līmenis | Vispārēji pieejams |
| Izmaksu pārvaldība | Lietotāja definēta partijas numura iestatīšanas iespējošana krājumu slēgšanas apgriešanai | Vispārēji pieejams |
| Izmaksu pārvaldība | Detalizēta informācija par krājuma slēgšanas norisi | Vispārēji pieejams |
| Izmaksu pārvaldība | Krājumu standarta izmaksu pārvērtēšanas finanšu dimensiju noklusējuma opcijas | Vispārēji pieejams |
| Izmaksu pārvaldība | Krājumu vērtības pārskata datu tīrīšana | Ieslēgts pēc noklusējuma |
| Izmaksu pārvaldība | Krājumu vērtības pārskata glabāšana | Ieslēgts pēc noklusējuma |
| Izmaksu pārvaldība | Rādīt krājumu slēgšanas žurnālu režģī | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | Izmaiņu pārvaldības iespējošana esošajām precēm | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | Tehnisko izmaiņu pārvaldība | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | Tehniskie paziņojumi ražotājiem | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | Uzlabota atribūtu pārmantošana tehnisko izmaiņu pārvaldībai | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | Pārvaldīt izmaiņas formulās un to komponentos | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | Preces gatavības pārbaudes | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | Tehnisko preču variantu ģenerēšana | Ieslēgts pēc noklusējuma |
| Krājumu un noliktavas pārvaldība | Navigācija uz MK versiju no MK līnijām | Obligāts |
| Vispārējā plānošana | Sērijveida nostiprināšana un apvienošana plānotajiem lielapjoma un pakotņu partiju pasūtījumiem | Vispārēji pieejams |
| Vispārējā plānošana | Resursu plānošana ar uzturēšanu | Vispārēji pieejams |
| Vispārējā plānošana | Iespējot ģenerālplāna iestatīšanas vedņa līdzekļus | Obligāts |
| Vispārējā plānošana | Prognožu modeļa izvēle sadaļas Pieprasījuma apjoma prognoze detalizētās informācijas daļā | Obligāts |
| Vispārējā plānošana | Vispārējās plānošanas norises vizualizācija | Obligāts |
| Vispārējā plānošana | Paralēla plānoto pasūtījumu apstiprināšana | Obligāts |
| Vispārējā plānošana | Plānota pasūtījuma apstiprināšana ar filtrēšanu | Ieslēgts pēc noklusējuma |
| Vispārējā plānošana | Saglabātie skati plānotajiem pasūtījumiem | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Atspējot pirkšanas pieprasījuma izplatīšanas atiestatīšanas pogu | Vispārēji pieejams |
| Sagāde un avoti | Iespējot ar iepirkumu saistīto darbplūsmu atiestatīšanu | Vispārēji pieejams |
| Sagāde un avoti | Iespēja apstiprināt pieņemtus pirkšanas pasūtījumus no kreditora sadarbības partijā | Obligāts |
| Sagāde un avoti | Pirkšanas līguma statuss Slēgts | Obligāts |
| Sagāde un avoti | Pievienot rindas PP rēķiniem, kas saistīti ar pirkšanas līgumu | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Pievienot lauku Pasūtītais daudzums lapā Produktu ieejas plūsmas grāmatošana | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Sniedz iespēju kreditoriem pieteikties iepirkuma kategorijām, sadarbojoties ar kreditoriem | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Ienākošās un izejošās summas pirkšanas pasūtījumos | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Izmaksu iestatīšana vietā un noliktavā | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Iespējot pirkšanas nodokļa aprēķinu, pamatojoties uz gada tarifu | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Par pirkšanas līgumu atbildīgā puse | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Saglabātie pirkšanas pasūtījumu skati | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | Noklusējuma pasūtījumu daudzumu stingra validācija | Obligāts |
| Preču informācijas pārvaldība | Materiālu komplekta pārskata pirmapstrāde, lai izvairītos no taimauta | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | Noklusējuma finanšu dimensijas atsevišķi, izmantojot krājumu veidnes | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | Iespējot preču dimensiju grupas krājumu veidnēm | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | Preces variantu nosaukumu atjaunošana, pamatojoties uz nomenklatūru | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | Variantu ieteikumu lapas uzlabojumi | Ieslēgts pēc noklusējuma |
| Ražošanas kontrole | Uzlabota produkcijas pieļaujamā svara daudzuma atlasīšana | Vispārēji pieejams |
| Ražošanas kontrole | Lapā Job Card Terminal ir pievienota jauna poga, lai apturētu pārtraukumu | Obligāts |
| Ražošanas kontrole | Iespējojiet unikāla noliktavas vienības identifikatora automātisku ģenerēšanu, kad darba kartes ierīcē norādīts pabeigts statuss | Obligāts |
| Ražošanas kontrole | Iespējot apakšlīgumā slēgto preču daļēju saņemšanu un novērst problēmu ar lūžņu aprēķināšanu MK rindām, kuru veids ir piegādātājs | Obligāts |
| Ražošanas kontrole | Līdzeklis darba kartes ierīces un darba kartes termināļa aizturēšanai, lai var veikt to tīrīšanu | Obligāts |
| Ražošanas kontrole | Uzlabojumi apstiprināšanas un pārsūtīšanas darbu dialogos | Obligāts |
| Ražošanas kontrole | Darbu kartes ierīcei ir pievienota unikālai noliktavas vienībai, lai ziņotu par pabeigšanu | Obligāts |
| Ražošanas kontrole | Izdrukāt etiķeti no darba karšu ierīces | Obligāts |
| Ražošanas kontrole | Ražošanas izpilde | Obligāts |
| Ražošanas kontrole | Aktīvu pārvaldības funkcionalitāte ražošanas izpildes interfeisam | Ieslēgts pēc noklusējuma |
| Ražošanas kontrole | Darbu meklēšana ražošanas izpildes saskarnē | Ieslēgts pēc noklusējuma |
| Ražošanas kontrole | Pārlabot noklusējuma ražošanas rezervāciju | Ieslēgts pēc noklusējuma |
| Ražošanas kontrole | Ražotnes izpildes saskarnē rādīt pilnus sērijas, partijas numurus un unikālos noliktavas vienības identifikatorus | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | Pārdošanas pasūtījuma detalizētās informācijas veiktspējas uzlabošana | Vispārēji pieejams |
| Pārdošana un mārketings | Pārdošanas piedāvājuma detalizētās informācijas veiktspējas uzlabošana | Vispārēji pieejams |
| Pārdošana un mārketings | Tādu datu eksportēšanas politika, uz kuriem atsaucas pārdošanas pasūtījums | Obligāts |
| Pārdošana un mārketings | Pārdošanas pasūtījuma un pirkšanas pasūtījuma rindas dzēšanas politika | Obligāts |
| Pārdošana un mārketings | Tādu datu eksportēšanas politika, uz kuriem atsaucas pārdošanas piedāvājums | Obligāts |
| Pārdošana un mārketings | Kontaktpersonas datu entītijas eksporta optimizācija | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | Iespējot meklēšanu pārdošanas piedāvājuma dokumenta ievadam un dokumentu secinājumu laukiem | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | “100 populārāko” klientu pārskata veiktspējas uzlabošana | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | Aprēķinātās debitora bilances automātiska pārrēķināšana | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | Pārdošanas atgriešanas pasūtījuma rindas reģistrācija ar precizitāti līdz decimāldaļām ar un bez pieļaujamā svara | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | Saglabāti pārdošanas un mārketinga skati | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | Viena klikšķa pārdošanas pasūtījuma apstiprinājums | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Pārkraušana sadales centrā — veidnes ar atrašanās vietas norādēm | Vispārēji pieejams |
| Noliktavas vadība | Sagaidāmā saņemšana no kvalitātes pārbaudes pasūtījumiem, kas izmanto aizturēto krājumu paraugus — atspējošana | Vispārēji pieejams |
| Noliktavas vadība | Numurzīmes saņemšanas vēsture | Vispārēji pieejams |
| Noliktavas vadība | Pēc izlaišanas uz noliktavu daudzumus noapaļot līdz tuvākajai pārdošanas vienībai | Vispārēji pieejams |
| Noliktavas vadība | Mērogotās vienības atbalsts noliktavas programmas darbu sarakstiem | Vispārēji pieejams |
| Noliktavas vadība | Sūtījuma kopuma etiķetes detalizētā informācija | Vispārēji pieejams |
| Noliktavas vadība | Izmantojiet ātrāku API konteineru aizvēršanai/atkārtotai atvēršanai iepakošanas stacijā | Vispārēji pieejams |
| Noliktavas vadība | Papildināšanas darbiem atlasīto veidņu apstiprināšana | Vispārēji pieejams |
| Noliktavas vadība | Atļaut papildināšanas veidnei izmantot esošos tūlītējās papildināšanas darbus (visās vienībās) | Obligāts |
| Noliktavas vadība | Automātiska GUID piešķiršana WHS lietotāja izveidei | Obligāts |
| Noliktavas vadība | Preces variantu un izsekošanas dimensiju tveršana noliktavas lietotnē noslodzes krājuma saņemšanas laikā | Obligāts |
| Noliktavas vadība | Mainīt krājumu statusu precēm, kuras kontrolē izsekošanas dimensijas | Obligāts |
| Noliktavas vadība | Mainīt darba pūlu darbam | Obligāts |
| Noliktavas vadība | Klastera pozīcija pilna | Obligāts |
| Noliktavas vadība | Klastera izvietošanas funkcija | Obligāts |
| Noliktavas vadība | Apstiprināt un pārsūtīt | Obligāts |
| Noliktavas vadība | Apstiprināt izejošos sūtījumus no pakešuzdevumiem | Obligāts |
| Noliktavas vadība | Kontrolēt, vai mobilajās ierīcēs rādīt saņemšanas kopsavilkuma lapu | Obligāts |
| Noliktavas vadība | Krājumu manuālas pārvietošanas operācijas atliktā apstrāde | Obligāts |
| Noliktavas vadība | Neļaut veidot slodzes, kas neatbilst viļņu slodzes ēkas šablona prasībām | Obligāts |
| Noliktavas vadība | Uzlaboti noliktavas vienību etiķešu izkārtojumi | Obligāts |
| Noliktavas vadība | Novērtējiet visas vairāku SKU atrašanās vietas direktīvu darbības | Obligāts |
| Noliktavas vadība | Paslēpt lauku Kopējā vērtība lapā “Visas kravas” un “Detalizēta informācija par kravu” | Obligāts |
| Noliktavas vadība | Numurzīmes etiķetes būvēšanas konfigurācija | Obligāts |
| Noliktavas vadība | Noslodzes rindas manuālā korekcija administratoriem vai līdzīgiem uzticamiem lietotājiem | Obligāts |
| Noliktavas vadība | Novietojuma noliktavas vienības pozīcija | Obligāts |
| Noliktavas vadība | Novietojuma produkta dimensijas sajaukšana | Obligāts |
| Noliktavas vadība | Padariet rediģējamu mobilās ierīces krājumu kustības krājumu statusa lauku | Obligāts |
| Noliktavas vadība | Manuālās pārdošanas rindas izdošanas pakalpojums administratoram vai līdzīgiem uzticamiem lietotājiem | Obligāts |
| Noliktavas vadība | Liegt pārsūtīšanas pasūtījumā nosūtīto noliktavas vienību izmantošanu citās noliktavās, izņemot mērķa noliktavu | Obligāts |
| Noliktavas vadība | Piedāvāt atrisināt neskaidrus vienumu “Atrašanās vieta/Noliktavas vienība” nosaukumus | Obligāts |
| Noliktavas vadība | Kvalitātes pārbaude | Obligāts |
| Noliktavas vadība | Jaunās noliktavas programmas lietotāja iestatījumi, ikonas un darbību elementi | Obligāts |
| Noliktavas vadība | Papildu atrašanās vietas zona | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Ātrās validācijas iespējošana noliktavu mobilajām ierīcēm | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Krājumu konsolidācijas novietojuma utilizācija | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Maksimālais izpildes laiks noliktavas vadības rīcībā esošo ierakstu tīrīšanas darbam | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Izejošās darba slodzes vizualizācija | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Apstrādāt noliktavas programmas notikumus | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Saglabāts skats kravu plānošanas rīkam | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Saglabāts skats darba detalizētās informācijas lapai | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Saglabāts skats kopuma apstrādei | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Saglabātie skati noslodzes apstrādei | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Saglabātie skati sūtījuma apstrādei | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Kopuma pakešuzdevuma detalizētā informācija | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Kopuma izpildes paziņojumi | Ieslēgts pēc noklusējuma |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Programmu Finance and Operations platformas atjauninājumi

Microsoft Dynamics 365 Supply Chain Management 10.0.25 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet [Platformas atjauninājumi programmas Finance and Operations versijai 10.0.25 (2022. gada aprīlis)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.25, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 un rūpniecības mākoņi: 2022. gada 1. laidiena plāns

Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Apskatiet [Dynamics 365 un rūpniecības mākoņi: 2022. gada 1. laidiena plāns](/dynamics365-release-plan/2022wave1/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Noņemtie un novecojušie Supply Chain Management līdzekļi

Tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) apraksta līdzekļus, kas ir vai ir ieplānots noņemšanai no Supply Chain Management.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda funkcija tiek noņemta no preces, izslēgšanas paziņojums tiks izziņota tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mēnešu laikā pirms noņemšanas.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
