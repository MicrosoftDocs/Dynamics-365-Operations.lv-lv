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
ms.openlocfilehash: 068e65d0bd76d7a9af36c6c3539d0c813efd528a
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384542"
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

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Krājumi&nbsp;un&nbsp;loģistika | [Bīstamo materiālu uzlabojumi](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | Drīzumā | Līdzekļu pārvaldība:<br>*Bīstamo materiālu uzlabojumi* |
| Krājumi&nbsp;un&nbsp;loģistika | [Iepakošanas darbs pakošanas stacijām](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | Drīzumā | Līdzekļu pārvaldība:<br>*Iepakošanas darbs pakošanas stacijām* |
| Krājumi&nbsp;un&nbsp;loģistika | [Skenēt svītrkodus noliktavā, izmantojot GS1 formāta standartus](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 svītrkodi un QR kodi](../warehousing/gs1-barcodes.md) | Līdzekļu pārvaldība:<br>*Skenēt GS1 svītrkodus* |
| Ražošana | [Materiālu patēriņš un rezervācijas ražošanas grīdas izpildes saskarnē](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Kā nodarbinātie izmanto ražošanas izpildes interfeisu](../production-control/production-floor-execution-use.md) | Līdzekļu pārvaldība:<br>*(Priekšskatījums) Materiālu patēriņa reģistrācija ražotnes izpildes saskarnē (bez WMS)*<br><br>Un/vai:<br><br>Līdzekļu pārvaldība:<br>*(Priekšskatījums) Reģistrēt materiālu patēriņu ražošanas izpildes interfeisā (WMS iespējots)* |
| Ražošana | [Reģistrēt materiālu patēriņu mēroga vienībās](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Ražošanas izpildes darba slodzes mākoņa un malas mēroga vienībām](../cloud-edge/cloud-edge-workload-manufacturing.md) | Līdzekļu pārvaldība:<br>*Reģistrēt materiālu patēriņu mērogošanas vienībā mobilajā programmā* |
| Plānošana | [Optimizācijas ieteikumu plānošana, lai optimizētu esošo piedāvājumu](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Optimizācijas priekšlikumi](../master-planning/action-messages.md) | Iespējots pēc noklusējuma |
| Plānošana | Plānotie pasūtījumi vienkāršoti | [Plānotie pasūtījumi vienkāršoti](../master-planning/planning-optimization/planned-orders-simplified.md ) | Līdzekļu pārvaldība:<br>*Plānotie pasūtījumi vienkāršoti* |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt kādu no šiem līdzekļiem, tas jādara [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Krājumu un noliktavas pārvaldība | (Polija) Ļauj saistīt vairākus SAD rēķinus ar vienu pirkšanas pasūtījuma rindu vienā SAD | Šis līdzeklis ļauj sadalīt pirkšanas pasūtījuma rindas un saistīt tās ar vienu administratīvo dokumentu (VAD), kad šīs pirkšanas pasūtījuma rindas tika grāmatotas vairākiem dažādiem rēķiniem (piemēram, dažādām nosūtīšanas pavadzīmēm). |
| Sagāde un avoti | Apvienot vairākus pirkšanas pieprasījumus vienā pirkšanas pasūtījumā pēc uzskaites datuma | Šis līdzeklis ļauj apvienot vairākus pirkšanas pieprasījumus vienā pirkšanas pasūtījumā, ja dažādiem pirkšanas pieprasījumiem ir atšķirīgi grāmatvedības datumi. Pirkšanas pasūtījuma izveides un pieprasījuma konsolidācijas pirkšanas politikas noteikumus var iestatīt, lai automatizētu lēmumu par pieprasījuma rindu grupēšanu pēc uzskaites datuma pirkšanas pasūtījuma līmenī. Pirkšanas pasūtījuma konsolidācija pēc uzskaites datuma netiek atbalstīta, ja budžeta kontrole ir aktivizēta, jo grāmatvedības datums tiek izmantots budžeta rezervācijām un apgrūtinājumiem. Tāpēc tas jāsaglabā pārejas laikā no pirkšanas pieprasījuma uz pirkšanas pasūtījumu. |
| Sagāde un avoti | Parādīt mantotos noklusējuma PP atbildes lauka iestatījumus | Šis līdzeklis atkārtoti ievieš mantotos noklusējuma piedāvājuma pieprasījuma (PIEDĀVĀJUMA PIEPRASĪJUMA) atbildes lauka iestatījumus, kas iepriekš tika noņemti no lietotāja interfeisa. Šie iestatījumi nenodrošina nekādu funkcionalitāti ārpus kastes, bet tos var pielāgot, lai nodrošinātu to pēc vajadzības. Ieslēdziet šo līdzekli, ja jūsu organizācija jau ir pievienojusi funkcionalitāti noklusējuma PIEDĀVĀJUMA PIEPRASĪJUMA atbildes lauka iestatījumiem vai plāno to darīt. Kad šis līdzeklis ir iespējots, iestatījumiem var piekļūt, dodoties uz **lapu Sagādes un sagādes parametri**, atverot **cilni Piedāvājuma** pieprasījums un atlasot **Noklusējuma piedāvājuma pieprasījuma atbildes laukus**. |
| Sagāde un avoti | Sapludināt kreditora finanšu dimensijas ar aktīvās dimensijas saites finanšu dimensiju pirkšanas pasūtījumā | Šis līdzeklis ļauj sapludināt finanšu dimensijas no piegādātājiem ar aktīvās dimensijas saistīt finanšu dimensijas pēc pirkšanas pieprasījuma apstiprināšanas, ja iestatāt saiti starp finanšu dimensiju un vietnes krājumu dimensiju. Pirkšanas pasūtījuma izveides un pieprasījuma konsolidācijas pirkšanas politikas nosacījumus var iestatīt, lai virzītu lēmumu par finanšu dimensiju apvienošanu no kreditoriem ar aktīvās dimensijas saites finanšu dimensiju pirkšanas pasūtījuma virsraksta līmenī. |
| Ražošanas kontrole | (Krievija) Iespējot noklusētos novietojuma iestatījumus ražošanas formulai/MK un automātisko GTD rezervāciju/patēriņu ražošanā | Šī funkcija iespējo papildu iespējas ražošanai no importētām izejvielām (tikai Krievijas lokalizācijai):<ul><li>Iespēja iestatīt automātisku noklusējuma atrašanās vietu ražošanas formulām un materiālu komplektiem gan resursu grupās, gan noliktavās.</li><li>Automātiska izejvielu rezervēšana pēc *GTD numura* dimensijas WMS aktivizētās noliktavās saskaņā ar ne-WMS rezervēšanas algoritmu. Tas attiecas uz gadījumiem, kad pastāv darba politika izejmateriālu savākšanai *ar* **darba izveides metodi**, kas iestatīta uz *Nekad*, un noliktavas, novietojuma un krājuma koda iestatījumi atbilst ražošanas (partijas) pasūtījuma krājumu darbībām.</li><li>Automātiska izejmateriālu patēriņš pēc *GTD numura* dimensijas izdošanas saraksta grāmatošanas laikā atbilstoši iepriekš aprakstītajai iegādātajai rezervācijai.</li></ul> |
| Noliktavas vadība | (Priekšskatījums) Mērogošanas vienības atbalsts ienākošajiem un izejošajiem noliktavas pasūtījumiem | Šis līdzeklis liek sistēmai izveidot izejošos noliktavas pasūtījumus transportēšanas uz noliktavu apstrādes laikā un izveidot ienākošos noliktavas pasūtījumus, kad pārsūtīšanas pasūtījumi tiek grāmatoti kā nosūtīti. Pēc tam sistēma sinhronizē katru ienākošo vai izejošo noliktavas pasūtījumu ar skalas vienību, kas atbild par pasūtījuma nosūtīšanu vai saņemšanu. Ņemiet vērā, ka pēc šī līdzekļa iespējošanas noliktavas izpildes darba slodze ir jājaunina. Plašāku informāciju skatiet rakstā [Mākoņa un malas mēroga vienības ražošanas izpilde](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Šim līdzeklim *ir nepieciešams atšifrēšanas izvietošanas darbs no ASN* līdzekļa, un tas ļaus saņemt pārsūtīšanas pasūtījumus, izmantojot numura zīmes saņemšanas procesu noliktavas pārvaldības mobilajā lietotnē. |

## <a name="feature-state-changes-in-this-release"></a>Līdzekļu stāvokļa izmaiņas šajā laidienā

Šajā tabulā ir uzskaitīti līdzekļi, kas kļuva obligāti vai pēc noklusējuma, sākot no 10.0.25. Visi šie līdzekļi tiks automātiski ieslēgti jūsu sistēmai, tiklīdz atjaunināsit uz 10.0.25. Obligātos līdzekļus nevar izslēgt, bet līdzekļus, kas ir ieslēgti pēc noklusējuma, joprojām var izslēgt, izmantojot [līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabulā ir uzskaitīti arī līdzekļi, kas iepriekš bija publiski pieejami, bet ir mainījušies, lai kļūtu vispārēji pieejami 10.0.25. punktā, kas nozīmē, ka tagad tos ieteicams izmantot ražošanas vidēs. Šie līdzekļi pēc noklusējuma ir izslēgti, ja vien nav norādīts citādi, tāpēc, ja vēlaties tos izmantot, ir jāizmanto [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai tos iespējotu.

| Modulis | Līdzekļa nosaukums | Līdzekļa statuss |
| --- | --- | --- |
| Līdzekļu pārvaldība | [Piemērot kāŗtules darba pasūtījumu grupēšanai, palaižot uzturēšanas plānu](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Vispārēji pieejams |
| Līdzekļu pārvaldība | [Uz skaitītāju balstīti uzturēšanas uzlabojumi](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Vispārēji pieejams |
| Izmaksu pārvaldība | [Izmaksu aprēķina līmenis](../cost-management/cost-calculation-level.md) | Vispārēji pieejams |
| Izmaksu pārvaldība | Lietotāja definēta partijas numura iestatīšanas iespējošana krājumu slēgšanas apgriešanai | Vispārēji pieejams |
| Izmaksu pārvaldība | [Detalizēta informācija par krājuma slēgšanas norisi](whats-new-scm-10-0-21.md) | Vispārēji pieejams |
| Izmaksu pārvaldība | [Krājumu standarta izmaksu pārvērtēšanas finanšu dimensiju noklusējuma opcijas](../cost-management/manage-standard-cost-updates.md) | Vispārēji pieejams |
| Izmaksu pārvaldība | Krājumu vērtības pārskata datu tīrīšana | Ieslēgts pēc noklusējuma |
| Izmaksu pārvaldība | [Krājumu vērtības pārskata glabāšana](../cost-management/inventory-value-report-storage.md) | Ieslēgts pēc noklusējuma |
| Izmaksu pārvaldība | Rādīt krājumu slēgšanas žurnālu režģī | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | [Izmaiņu pārvaldības iespējošana esošajiem produktiem](../engineering-change-management/change-management-existing-products.md) | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | [Inženiertehnisko izmaiņu vadība](../engineering-change-management/product-engineering-overview.md) | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | [Tehniskie paziņojumi ražotājiem](../engineering-change-management/engineering-change-management.md) | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | [Uzlabota atribūtu pārmantošana tehnisko izmaiņu pārvaldībai](../engineering-change-management/engineering-attributes-and-search.md) | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | [Pārvaldīt izmaiņas formulās un to komponentos](../engineering-change-management/manage-formula-changes.md) | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | [Preces gatavības pārbaudes](../engineering-change-management/product-readiness.md) | Ieslēgts pēc noklusējuma |
| Tehnisko izmaiņu pārvaldība | [Tehnisko preču variantu ģenerēšana](../engineering-change-management/engineering-variants.md) | Ieslēgts pēc noklusējuma |
| Krājumu un noliktavas pārvaldība | Navigācija uz MK versiju no MK rindām | Obligāts |
| Vispārējā plānošana | [Sērijveida nostiprināšana un apvienošana plānotajiem lielapjoma un pakotņu partiju pasūtījumiem](whats-new-scm-10-0-20.md) | Vispārēji pieejams |
| Vispārējā plānošana | Resursu plānošana ar uzturēšanu | Vispārēji pieejams |
| Vispārējā plānošana | Vispārējā plāna iestatīšanas vedņa līdzekļu iespējošana | Obligāts |
| Vispārējā plānošana | [Prognožu modeļa izvēle sadaļas Pieprasījuma apjoma prognoze detalizētās informācijas daļā](../master-planning/manual-adjustments-baseline-forecast.md) | Obligāts |
| Vispārējā plānošana | [Vispārējās plānošanas norises vizualizācija](../master-planning/tasks/monitor-master-planning-run.md) | Obligāts |
| Vispārējā plānošana | [Paralēla plānoto pasūtījumu apstiprināšana](../master-planning/planning-optimization/planned-order-firming.md) | Obligāts |
| Vispārējā plānošana | [Plānota pasūtījuma apstiprināšana ar filtrēšanu](../master-planning/planning-optimization/planned-order-firming.md) | Ieslēgts pēc noklusējuma |
| Vispārējā plānošana | [Saglabātie plānoto pasūtījumu skati](saved-views-scm.md) | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Atspējot pirkšanas pieprasījuma izplatīšanas atiestatīšanas pogu | Vispārēji pieejams |
| Sagāde un avoti | [Iespējot ar iepirkumu saistīto darbplūsmu atiestatīšanu](whats-new-scm-10-0-20.md) | Vispārēji pieejams |
| Sagāde un avoti | Iespēja apstiprināt pieņemtus pirkšanas pasūtījumus no kreditora sadarbības partijā | Obligāts |
| Sagāde un avoti | Pirkšanas līguma statuss Slēgts | Obligāts |
| Sagāde un avoti | Pievienot rindas PP rēķiniem, kas saistīti ar pirkšanas līgumu | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Pievienot lauku Pasūtītais daudzums lapā Produktu ieejas plūsmas grāmatošana | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | [Sniedz iespēju kreditoriem pieteikties iepirkuma kategorijām, sadarbojoties ar kreditoriem](../procurement/category-requests-from-vendors.md) | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Ienākošās un izejošās summas pirkšanas pasūtījumos | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Izmaksu iestatīšana vietā un noliktavā | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | Iespējot pirkšanas nodokļa aprēķinu, pamatojoties uz gada tarifu | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | [Par pirkšanas līgumu atbildīgā puse](../procurement/purchase-agreements.md) | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | [Saglabātie pirkšanas pasūtījumu skati](saved-views-scm.md) | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | [Noklusējuma pasūtījumu daudzumu stingra validācija](../production-control/default-order-settings.md) | Obligāts |
| Preču informācijas pārvaldība | Materiālu komplekta pārskata pirmapstrāde, lai izvairītos no taimauta | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | Noklusējuma finanšu dimensijas atsevišķi, izmantojot krājumu veidnes | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | Iespējot preču dimensiju grupas krājumu veidnēm | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | Preces variantu nosaukumu atjaunošana, pamatojoties uz nomenklatūru | Ieslēgts pēc noklusējuma |
| Preču informācijas pārvaldība | [Variantu ieteikumu lapas uzlabojumi](../pim/tasks/create-predefined-product-variants.md) | Ieslēgts pēc noklusējuma |
| Ražošanas kontrole | Uzlabota produkcijas pieļaujamā svara daudzuma atlasīšana | Vispārēji pieejams |
| Ražošanas kontrole | Darba kartes termināļa lapai ir pievienota jauna poga pārtraukuma apturēšanai | Obligāts |
| Ražošanas kontrole | [Iespējojiet unikāla noliktavas vienības identifikatora automātisku ģenerēšanu, kad darba kartes ierīcē norādīts pabeigts statuss](../production-control/production-floor-execution-configure.md) | Obligāts |
| Ražošanas kontrole | Iespējot apakšuzņēmēju krājumu daļēju saņemšanu un novērst problēmu ar brāķa aprēķinu MK rindām, kuru tips ir Kreditors | Obligāts |
| Ražošanas kontrole | [Līdzeklis darba kartes ierīces un darba kartes termināļa aizturēšanai, lai var veikt to tīrīšanu](../production-control/production-floor-execution-configure.md) | Obligāts |
| Ražošanas kontrole | Uzlabojumi apstiprināšanas un pārsūtīšanas darbu dialogos | Obligāts |
| Ražošanas kontrole | [Darbu kartes ierīcei ir pievienota unikālai noliktavas vienībai, lai ziņotu par pabeigšanu](../production-control/production-floor-execution-configure.md) | Obligāts |
| Ražošanas kontrole | [Izdrukāt etiķeti no darba karšu ierīces](../production-control/production-floor-execution-configure.md) | Obligāts |
| Ražošanas kontrole | [Ražošanas izpilde](../production-control/production-floor-execution-configure.md) | Obligāts |
| Ražošanas kontrole | [Aktīvu pārvaldības funkcionalitāte ražošanas izpildes interfeisam](../production-control/production-floor-execution-configure.md) | Ieslēgts pēc noklusējuma |
| Ražošanas kontrole | [Darbu meklēšana ražošanas izpildes saskarnē](../production-control/production-floor-execution-configure.md) | Ieslēgts pēc noklusējuma |
| Ražošanas kontrole | [Pārlabot noklusējuma ražošanas rezervāciju](../production-control/override-default-reservation-principle.md) | Ieslēgts pēc noklusējuma |
| Ražošanas kontrole | [Ražotnes izpildes saskarnē rādīt pilnus sērijas, partijas numurus un unikālos noliktavas vienības identifikatorus](whats-new-scm-10-0-21.md) | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | [Pārdošanas pasūtījuma detalizētās informācijas veiktspējas uzlabošana](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Vispārēji pieejams |
| Pārdošana un mārketings | Pārdošanas piedāvājuma detalizētās informācijas veiktspējas uzlabošana | Vispārēji pieejams |
| Pārdošana un mārketings | Tādu datu eksportēšanas politika, uz kuriem atsaucas pārdošanas pasūtījums | Obligāts |
| Pārdošana un mārketings | [Pārdošanas pasūtījuma un pirkšanas pasūtījuma rindas dzēšanas politika](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Obligāts |
| Pārdošana un mārketings | [Tādu datu eksportēšanas politika, uz kuriem atsaucas pārdošanas piedāvājums](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Obligāts |
| Pārdošana un mārketings | [Kontaktpersonas datu entītijas eksporta optimizācija](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | Iespējot meklēšanu pārdošanas piedāvājuma dokumenta ievadam un dokumentu secinājumu laukiem | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | [“100 populārāko” klientu pārskata veiktspējas uzlabošana](whats-new-scm-10-0-23.md) | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | Aprēķinātās debitora bilances automātiska pārrēķināšana | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | [Pārdošanas atgriešanas pasūtījuma rindas reģistrācija ar precizitāti līdz decimāldaļām ar un bez pieļaujamā svara](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | [Saglabāti pārdošanas un mārketinga skati](saved-views-scm.md) | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | Viena klikšķa pārdošanas pasūtījuma apstiprinājums | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Pārkraušana sadales centrā — veidnes ar atrašanās vietas norādēm](../warehousing/planned-cross-docking.md) | Vispārēji pieejams |
| Noliktavas vadība | [Sagaidāmā saņemšana no kvalitātes pārbaudes pasūtījumiem, kas izmanto aizturēto krājumu paraugus — atspējošana](../inventory/inventory-blocking.md) | Vispārēji pieejams |
| Noliktavas vadība | Numurzīmes saņemšanas vēsture | Vispārēji pieejams |
| Noliktavas vadība | [Materiālu apstrādes aprīkojuma interfeiss](../warehousing/mhax.md) | Vispārēji pieejams |
| Noliktavas vadība | [Pēc izlaišanas uz noliktavu daudzumus noapaļot līdz tuvākajai pārdošanas vienībai](whats-new-scm-10-0-19.md) | Vispārēji pieejams |
| Noliktavas vadība | Mērogotās vienības atbalsts noliktavas programmas darbu sarakstiem | Vispārēji pieejams |
| Noliktavas vadība | Sūtījuma kopuma etiķetes detalizētā informācija | Vispārēji pieejams |
| Noliktavas vadība | [Izmantojiet ātrāku API konteineru aizvēršanai/atkārtotai atvēršanai iepakošanas stacijā](whats-new-scm-10-0-21.md) | Vispārēji pieejams |
| Noliktavas vadība | [Papildināšanas darbiem atlasīto veidņu apstiprināšana](whats-new-scm-10-0-20.md) | Vispārēji pieejams |
| Noliktavas vadība | Atļaut papildināšanas veidnei izmantot esošos tūlītējās papildināšanas darbus (visās vienībās) | Obligāts |
| Noliktavas vadība | Automātiska GUID piešķiršana WHS lietotāju izveidei | Obligāts |
| Noliktavas vadība | Preces variantu un izsekošanas dimensiju tveršana noliktavas lietotnē noslodzes krājuma saņemšanas laikā | Obligāts |
| Noliktavas vadība | [Mainīt krājumu statusu precēm, kuras kontrolē izsekošanas dimensijas](../inventory/inventory-statuses.md) | Obligāts |
| Noliktavas vadība | [Mainīt darba pūlu darbam](../warehousing/change-work-pool-on-work.md) | Obligāts |
| Noliktavas vadība | [Klastera pozīcija pilna](../warehousing/cluster-position-full.md) | Obligāts |
| Noliktavas vadība | [Klastera izvietošanas funkcija](../warehousing/putaway-clusters.md) | Obligāts |
| Noliktavas vadība | [Apstiprināt un pārsūtīt](../warehousing/confirm-and-transfer.md) | Obligāts |
| Noliktavas vadība | [Apstiprināt izejošos sūtījumus no pakešuzdevumiem](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Obligāts |
| Noliktavas vadība | [Kontrolēt, vai mobilajās ierīcēs rādīt saņemšanas kopsavilkuma lapu](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Obligāts |
| Noliktavas vadība | [Krājumu manuālas pārvietošanas operācijas atliktā apstrāde](../warehousing/deferred-processing-manual-inventory-movement.md) | Obligāts |
| Noliktavas vadība | Neļaujiet izveidot slodzes, kas neatbilst viļņu slodzes veidošanas veidnes prasībām | Obligāts |
| Noliktavas vadība | [Uzlaboti noliktavas vienību etiķešu izkārtojumi](../warehousing/document-routing-layout-for-license-plates.md) | Obligāts |
| Noliktavas vadība | [Novērtējiet visas vairāku SKU atrašanās vietas direktīvu darbības](../troubleshooting/warehousing/evaluate-multiple-location-directive-actions.md) | Obligāts |
| Noliktavas vadība | Paslēpt lauku Kopējā vērtība lapā “Visas kravas” un “Detalizēta informācija par kravu” | Obligāts |
| Noliktavas vadība | Numurzīmes etiķetes būvēšanas konfigurācija | Obligāts |
| Noliktavas vadība | Noslodzes rindas manuālā korekcija administratoriem vai līdzīgiem uzticamiem lietotājiem | Obligāts |
| Noliktavas vadība | [Novietojuma noliktavas vienības pozīcija](../warehousing/location-license-plate-positioning.md) | Obligāts |
| Noliktavas vadība | [Novietojuma produkta dimensijas sajaukšana](../warehousing/location-product-dimension-mixing.md) | Obligāts |
| Noliktavas vadība | Padariet rediģējamu mobilās ierīces krājumu kustības krājumu statusa lauku | Obligāts |
| Noliktavas vadība | Manuālās pārdošanas rindas izdošanas pakalpojums administratoram vai līdzīgiem uzticamiem lietotājiem | Obligāts |
| Noliktavas vadība | [Liegt pārsūtīšanas pasūtījumā nosūtīto noliktavas vienību izmantošanu citās noliktavās, izņemot mērķa noliktavu](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Obligāts |
| Noliktavas vadība | Piedāvāt atrisināt neskaidrus vienumu “Atrašanās vieta/Noliktavas vienība” nosaukumus | Obligāts |
| Noliktavas vadība | [Kvalitātes pārbaude](../warehousing/quality-check.md) | Obligāts |
| Noliktavas vadība | [Jaunās noliktavas programmas lietotāja iestatījumi, ikonas un darbību elementi](../warehousing/install-configure-warehouse-management-app.md) | Obligāts |
| Noliktavas vadība | [Papildu atrašanās vietas zona](../warehousing/additional-location-zones.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas](../warehousing/create-transfer-order-from-warehouse-app.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Ātrās validācijas iespējošana noliktavu mobilajām ierīcēm | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Maksimālais izpildes laiks noliktavas vadības rīcībā esošo ierakstu tīrīšanas darbam](../warehousing/onhand-cleanup.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Izejošās darba slodzes vizualizācija](../warehousing/outbound-workload-visualization.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Apstrādāt noliktavas programmas notikumus](../warehousing/warehouse-app-events.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Saglabāts skats kravu plānošanas rīkam](saved-views-scm.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Saglabāts skats darba detalizētās informācijas lapai](saved-views-scm.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Saglabāts skats kopuma apstrādei](saved-views-scm.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Saglabātie skati noslodzes apstrādei](saved-views-scm.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Saglabātie skati sūtījuma apstrādei](saved-views-scm.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Kopuma pakešuzdevuma detalizētā informācija](../warehousing/wave-processing.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Kopuma izpildes paziņojumi](../warehousing/wave-execution-notifications.md) | Ieslēgts pēc noklusējuma |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.25 ietver platformas atjauninājumus. Papildinformāciju skatiet rakstā [Programmu Finance and Operations versijas 10.0.25 platformas atjauninājumi (2022. gada aprīlis)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

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
