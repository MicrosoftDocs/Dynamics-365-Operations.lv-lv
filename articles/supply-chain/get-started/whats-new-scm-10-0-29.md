---
title: Izlaiduma Dynamics 365 Supply Chain Management 10.0.29 priekšskatījums (2022. gada oktobris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.29.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 316650de19d3275f2c60c79c10d6ac8a8c79e1aa
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427879"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10029-october-2022"></a>Izlaiduma Dynamics 365 Supply Chain Management 10.0.29 priekšskatījums (2022. gada oktobris)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā rakstā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti Microsoft priekšskatījuma Dynamics 365 Supply Chain Management versijā 10.0.29. Šai versijai ir ražošanas numuru 10.0.1326 un tā ir pieejama šajā grafikā:

- **Laidiena priekšskatījums:** 2022. gada augusts
- **Vispārēja laidiena (pašatjauninājums) pieejamība:** 2022. gada septembris
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada oktobris

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo rakstu, lai ietvertu līdzekļus, kas tika pievienoti būvējumam pēc šī raksta sākotnējās publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Krājumi un loģistika | [PIEŠĶIRT un rezervēt WMS krājumus krājumu redzamībai](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Drīzumā | Aktivizēts pēc noklusējuma |
| Krājumi un loģistika | [Iepriekšējas ielādēt racionālus rīcībā esošo krājumu sarakstus](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | Drīzumā | Aktivizēts pēc noklusējuma |
| Veidošanas pasūtījumā piegādes automatizācija | [Veidošanas pasūtījumā piegādes automatizācija](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Veidošanas pasūtījumā piegādes automatizācija](../master-planning/make-to-order-supply-automation.md) | Līdzekļu pārvaldība:<br>*Veidošanas pasūtījumā piegādes automatizācija* |
| Plānošana | [Skatīt un pielietot detalizētus ieskatus par DDMRP](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Pieprasījumam noteiktu materiālu prasību plānošanas apskats](../master-planning/planning-optimization/ddmrp-overview.md) | Līdzekļu pārvaldība:<br>*(Priekšskatījums) DDMRP plānošanas optimizācijai* |
| Ražošanas kontrole | [Gatavo preču padarīšana par fiziski pieejamām pirms grāmatošanas žurnālos](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Gatavo preču padarīšana par fiziski pieejamām pirms grāmatošanas žurnālos](../production-control/deferred-posting.md) | Līdzekļu pārvaldība:<br>*(Priekšskatījums) Padarīt gatavās preces fiziski pieejamas pirms grāmatošanas žurnālos* |
| Noliktavas vadība | [Uzmeklē atbilstošos datus noliktavas mobilajā programmā](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Vaicājumu dati, izmantojot mobilās programmas Warehouse Management apiešanu](../warehousing/warehouse-app-data-inquiry.md) | Līdzekļu pārvaldība:<br>*Warehouse Management programmas datu uzziņu plūsma* |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt jebkuru no šīm funkcijām, tas ir jādara līdzekļa [pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Izmaksu pārvaldība | Līdzprodukta gaidošā cenu aprēķina optimizācija | Šī funkcija labo konfliktu, kas reizēm var rasties, kad līdzprodukta cenas tiek aprēķinātas, izmantojot vairākus pavedienus. Tas liek sistēmai pārliecināties, vai katra līdzprodukta cena tiek aprēķināta tikai vienu reizi. Pēc tam šā aprēķina rezultāts tiek izmantots kā ievade visiem citiem aprēķiniem. Ja gaidoša cena jau eksistē, šī cena tiek izmantota. |
| Vispārējā plānošana | Grupu darījumi Plānošanas optimizācijā | Izmantojot plānošanas optimizāciju, šis līdzeklis var palīdzēt samazināt plānoto pasūtījumu skaitu, kas tiek ģenerēti vienas pārdošanas pasūtījuma rindas piegādei. Ja ir ieslēgta šī funkcija, plānošanas optimizācija grupēs visas krājumu darbības pasūtījuma rindai vienā pilna daudzuma prasībā. (Šī funkcionalitāte atbilst iebūvētās plānošanas programmas funkcionalitātei.) Piedāvājums un pieprasījums tiek grupēti atsevišķi. Tāpēc šī funkcija palīdz samazināt darbības apjomu, kad ir sadalītas darbības un kad lietojat dimensijas (piemēram, partijas numurus vai sērijas numurus), kas nav vajadzības dimensijas. |
| Sagāde un avoti | Kreditora aizturēšana pirkšanas pasūtījumiem | Šī funkcija ļauj aizturēt kreditoru pirkšanas pasūtījumiem. Tas pievieno jaunu pirkšanas *pasūtījuma aizturēšanas* veidu, kas pirkšanas pasūtījumiem atzīmē kreditoru kā aizturētu. Jūs nevarēsit izveidot jaunus pirkšanas pasūtījumus kreditoriem, kas ir aizturēti pirkšanas pasūtījumiem, bet joprojām būs iespējams turpināt ar atvērtiem rēķiniem vai maksājumiem šiem kreditoriem. |
| Pārdošana un mārketings | Aprēķināt rindas neto summu importējot | Šī funkcija ļauj jums kontrolēt, vai sistēmai ir jāpārrēķina rindu kopsummas, kad importējat datus caur pārdošanas pasūtījuma rindām, *pārdošanas* piedāvājuma rindām vai atgriešanas *pasūtījuma* rindu elementu, *izmantojot* OData vai duālo rakstiet. Tas stājas spēkā tikai **tad**, kad jums ir arī tirdzniecības līgumu vērtēšanas politikas, kas ierobežo izmaiņas neto summas laukā pārdošanas pasūtījuma rindām, pārdošanas piedāvājuma rindām un/vai atgriešanas pasūtījuma rindām. Tas pievieno iestatījumu ar nosaukumu Aprēķināt **rindas neto summu** debitoru **parādu > iestatīšana > debitoru parādu parametru** lapai. Ja šis iestatījums ir iestatīts *uz* Jā, sistēma vienmēr nepieciešamības gadījumā pārrēķinās rindu summas (ignorējot jebkuru tirdzniecības līguma novērtējuma politiku rindas neto summai). *Ja iestatījums ir iestatīts uz Nē*, sistēma nekad automātiski aprēķinās rindas neto summu, pat ja ienākošās izmaiņas rindas cenā, daudzumā un/vai atlaidē nozīmē, ka rindas neto summa ir jāpārrēķina. Šī funkcija tiek aktivizēta pēc noklusējuma un sākotnēji iestata **rindas neto summas aprēķinam vērtību** *Jā*. Neviens *iestatījums* neatbilst sistēmas uzvedībai pirms versijas 10.0.23 un ir sniegts galvenokārt, lai atbalstītu mantojuma integrācijas scenārijus.<br><br>Papildinformāciju skatiet sadaļā Rindas [neto summu pārrēķins, importējot pārdošanas pasūtījumus, piedāvājumus un atgrieztos](../sales-marketing/calc-line-net-amounts-import.md). |
| Pārdošana un mārketings | Aprēķināt pārdošanas kopsummas, izmantojot vairākus pavedienus | Šī funkcija palīdz uzlabot veiktspēju, iespējojot sistēmu paralēlās apstrādes izmantošanu, aprēķinot paketē pārdošanas kopsummas. Šī funkcija pievieno jaunu **pavedienu lauku pārdošanas kopsummas** **aprēķināšanas** dialoglodziņam. Ja izvēlaties palaist aprēķinu paketē, šo lauku var izmantot, lai iestatītu maksimālo pavedienu skaitu. Ja iestatīsiet vērtību *kā 0* (nulle *) vai 1*, tiks izmantots viens pavediens. Vērtības virs 1 iespējo vairākpaveides. |
| Pārdošana un mārketings | Atjaunināt starpuzņēmumam manuāli ievadītās cenas un atlaides | Šī funkcija pievieno atbalstu starpuzņēmumu pasūtījumu manuālai izmaiņu politikai. Tas ietver atbalstu manuālo izmaiņu politiku pārsūtīšanai starp starpuzņēmumu pārdošanas un pirkšanas pasūtījumiem. Iepriekš manuālas izmaiņu politikas tika atbalstītas tikai pasūtījumiem, kas nav starpuzņēmumu pasūtījumi. Kad šī funkcija ir aktivizēta, sistēma dos jums opciju atjaunināt cenas un atlaides pēc izmaiņu saglabāšanas starpuzņēmumu pasūtījumā. Šī opcija ļauj izvēlēties, vai starpuzņēmumu pasūtījumam lietot jauno cenu un atlaižu informāciju vai atstāt pasūtījumu nemainītu. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Mēs nesen pievienojam vai būtiski atjauninājām šādus Palīdzības rakstus. Šiem rakstiem nav obligāti jābūt saistītiem ar jaunajiem līdzekļiem, kas tika pievienoti šim laidienam, kā norādīts iepriekšējās sadaļās. Tomēr tie var palīdzēt iegūt vairāk no esošajām funkcijām.

| Līdzekļu apgabals | Jauni vai atjaunināti raksti |
|---|---|
| Vispārējā plānošana, CTP | [Pārdošanas pasūtījuma piegādes datumus aprēķināšana, izmantojot CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Vispārējā plānošana, DDMRP | [Pieprasījumam noteiktu materiālu prasību plānošanas apskats](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Ieslēdziet DDMRP līdzekli savā sistēmā](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Krājumu pozīcija](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Bufera profils un līmeņi](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Uz pieprasījumu balstīta plānošana](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Vizuāla un sadarbības izpilde](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Noliktavas vadība | [Konteineru iepakošana nosūtīšanai](../warehousing/packing-containers.md)<br>[Iepakošanas darbs izejošo konteineru iepakošanai un sūtījumu apstrādei](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Līdzekļu stāvokļa izmaiņas šajā laidienā

Šajā tabulā uzskaitīti līdzekļi, kas bija obligāti vai pēc noklusējuma iekļauti versijā 10.0.29. Visas šīs funkcijas automātiski tiks ieslēgtas jūsu sistēmai, tiklīdz atjaunināsiet uz versiju 10.0.29. Obligātos līdzekļus nevar izslēgt, bet līdzekļus, kas ir ieslēgti pēc noklusējuma, joprojām var izslēgt, izmantojot līdzekļu [pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabulā ir uzskaitīti arī līdzekļi, kas iepriekš bija publiskā priekšskatījumā, bet ir mainīti, lai kļūtu plaši pieejami versijā 10.0.29. Šīs izmaiņas norāda, ka tagad funkcijas ir ieteicamas izmantošanai ražošanas vidēs. Šīs funkcijas pēc noklusējuma ir izslēgtas, ja vien nav norādīts citādi. Tāpēc jums ir jāizmanto Līdzekļu [pārvaldība,](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lai tos iespējotu, ja vēlaties tos lietot.

| Modulis | Līdzekļa nosaukums | Jauna līdzekļa stāvoklis |
| --- | --- | --- |
| Līdzekļu pārvaldība | [Aktīvu pārvaldības funkcionalitāte ražošanas izpildes interfeisam](../production-control/production-floor-execution-configure.md) | Obligāts |
| Izmaksu pārvaldība | [Mainīt atcelšanas etiķeti vienumā Slēgšana un korekciju uz operāciju Atsaukt](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Obligāts |
| Izmaksu pārvaldība | Tīrīt MK aprēķina detalizētas informācijas šķērs izmaksu aprēķināšanas versijas | Obligāts |
| Izmaksu pārvaldība | [Preču cenu/glabāšanas salīdzinājums](../cost-management/compare-item-price.md) | Obligāts |
| Izmaksu pārvaldība | [Izmaksu aprēķina līmenis](../cost-management/cost-calculation-level.md) | Ieslēgts pēc noklusējuma |
| Izmaksu pārvaldība | Lietotāja definēta partijas numura iestatīšanas iespējošana krājumu slēgšanas apgriešanai | Ieslēgts pēc noklusējuma |
| Izmaksu pārvaldība | [Detalizēta informācija par krājuma slēgšanas norisi](whats-new-scm-10-0-21.md) | Ieslēgts pēc noklusējuma |
| Izmaksu pārvaldība | [Krājumu vērtības pārskata glabāšana](../cost-management/inventory-value-report-storage.md) | Obligāts |
| Izmaksu pārvaldība | Krājumu vērtības pārskata datu tīrīšana | Obligāts |
| Izmaksu pārvaldība | Slīdošā vidējā pārvietošana, regresa izmaksu secība | Obligāts |
| Izmaksu pārvaldība | Rādīt krājumu slēgšanas žurnālu režģī | Obligāts |
| Izmaksu pārvaldība | Rādīt krājumus ar pilnībā nenosegtiem darījumiem kopsavilkuma formātā | Obligāts |
| Krājumu un noliktavas pārvaldība | Atļaut tukšas partijas atribūtu vērtības | Obligāts |
| Krājumu un noliktavas pārvaldība | Automātiski palielināt krājumu pārsūtīšanas pasūtījuma rindu numurus | Obligāts |
| Krājumu un noliktavas pārvaldība | Izveidot pārsūtīšanas pasūtījumu no pārdošanas rindas | Obligāts |
| Krājumu un noliktavas pārvaldība | Atspējot krājumu žurnāla rindas lauku darbplūsmā | Obligāts |
| Krājumu un noliktavas pārvaldība | Iespējojiet krājumu kvalitātes pārvaldības parametru brīdināšanas funkciju | Obligāts |
| Krājumu un noliktavas pārvaldība | (Ķīna) Izslēdziet fiziskās saņemšanas un izdošanas izmaksas no mēneša vidējām izmaksām | Ieslēgts pēc noklusējuma |
| Krājumu un noliktavas pārvaldība | [Krājumu žurnāla apstiprināšanas darbplūsma](../inventory/inventory-journal-workflow.md) | Obligāts |
| Krājumu un noliktavas pārvaldība | [Krājumu rīcībā esošā pārskata glabāšana](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Obligāts |
| Krājumu un noliktavas pārvaldība | [Saglabātie skati krājumu pārvaldībai](saved-views-scm.md) | Obligāts |
| Krājumu un noliktavas pārvaldība | Pārsūtīšanas pasūtījuma atcelšana | Obligāts |
| Krājumu un noliktavas pārvaldība | Mērvienības un vienības daudzuma izmantošana krājumu žurnālos | Obligāts |
| Krājumu un noliktavas pārvaldība | Atbloķēt krājumu žurnālu | Obligāts |
| Ražošana | [Noliktavā iespējotu materiālu automātiska atlasīšana automātiski grāmatotiem izdošanas sarakstiem](whats-new-scm-10-0-23.md) | Vispārēji pieejams |
| Ražošana | Iespējot krājumu dimensiju parādīšanu materiālu sarakstā ražošanas maršruta operācijām | Obligāts |
| Ražošana | [Iespējojiet, lai ievadītu partijas un sērijas numurus, vienlaikus ziņojot kā par pabeigtu no Darbu kartes ierīces](../production-control/report-finished-job-device.md) | Ieslēgts pēc noklusējuma |
| Ražošana | Uzlabota produkcijas pieļaujamā svara daudzuma atlasīšana | Ieslēgts pēc noklusējuma |
| Ražošana | [Darbu meklēšana ražošanas izpildes saskarnē](../production-control/production-floor-execution-configure.md) | Obligāts |
| Ražošana | [Ražošanas izpildes sistēmas integrācija](../production-control/mes-integration.md) | Ieslēgts pēc noklusējuma |
| Ražošana | [Skats “Mana diena” ražošanas izpildes interfeisam](../production-control/production-floor-execution-configure.md) | Ieslēgts pēc noklusējuma |
| Ražošana | [Ražošanas pasūtījumu materiālu pieejamības pārbaude pēc pieprasījuma](whats-new-scm-10-0-24.md) | Ieslēgts pēc noklusējuma |
| Ražošana | [Pārlabot noklusējuma ražošanas rezervāciju](../production-control/override-default-reservation-principle.md) | Obligāts |
| Ražošana | [Materiālu patēriņa reģistrācija ražotnes izpildes saskarnē (bez WMS)](../production-control/production-floor-execution-configure.md) | Vispārēji pieejams |
| Ražošana | [Sniegt pārskatu par pieļaujamā svara krājumiem no ražošanas izpildes interfeisa](../production-control/production-floor-execution-configure.md) | Vispārēji pieejams |
| Ražošana | [Pārskats par līdzproduktiem un blakusproduktiem no ražošanas izpildes saskarnes](../production-control/production-floor-execution-configure.md) | Ieslēgts pēc noklusējuma |
| Ražošana | [Plānošanas krājumu pārskats ražošanas izpildes interfeisā](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Ieslēgts pēc noklusējuma |
| Ražošana | [Ražošanas kontroles saglabātie skati](saved-views-scm.md) | Obligāts |
| Ražošana | [Ražotnes izpildes saskarnē rādīt pilnus sērijas, partijas numurus un unikālos noliktavas vienības identifikatorus](../production-control/production-floor-execution-configure.md) | Obligāts |
| Ražošana | [Pārbaudīt izejmateriālu beigu datumu, salīdzinot tos ar plānoto patēriņa datumu](whats-new-scm-10-0-23.md) | Ieslēgts pēc noklusējuma |
| Vispārējā plānošana | [Plānošanas optimizācijas automātiskā apstiprināšana](../master-planning/planning-optimization/planned-order-firming.md) | Obligāts |
| Vispārējā plānošana | [Sērijveida nostiprināšana un apvienošana plānotajiem lielapjoma un pakotņu partiju pasūtījumiem](whats-new-scm-10-0-20.md) | Ieslēgts pēc noklusējuma |
| Vispārējā plānošana | [Iekļaut rīcībā esošus krājumus, kad ir iespējoti priekšapstrādes filtri](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Ieslēgts pēc noklusējuma |
| Vispārējā plānošana | [Bezgalīga noslodzes plānošana plānošanas optimizācijai](../master-planning/planning-optimization/infinite-capacity-planning.md) | Ieslēgts pēc noklusējuma |
| Vispārējā plānošana | [Plānošanas optimizācijas robežas](../master-planning/planning-optimization/safety-margins.md) | Obligāts |
| Vispārējā plānošana | [Negatīvās dienas optimizācijas plānošanai](../master-planning/planning-optimization/delay-tolerance.md) | Obligāts |
| Vispārējā plānošana | [Koriģētas pieprasījuma apjoma prognozes paralēla pilnvarošana](whats-new-scm-10-0-20.md) | Obligāts |
| Vispārējā plānošana | [Plānota pasūtījuma apstiprināšana ar filtrēšanu](../master-planning/planning-optimization/planned-order-firming.md) | Obligāts |
| Vispārējā plānošana | [Plānotie ražošanas pasūtījumi plānošanas optimizēšanai](../master-planning/planning-optimization/production-planning.md) | Obligāts |
| Vispārējā plānošana | [Pirkšanas tirdzniecības līgumi funkcijai Plānošanas optimizēšana](../master-planning/planning-optimization/purchase-trade-agreement.md) | Obligāts |
| Vispārējā plānošana | [Saglabātie plānoto pasūtījumu skati](saved-views-scm.md) | Obligāts |
| Sagāde un avoti | Maksas no pirkšanas pasūtījumiem un līdz summām | Obligāts |
| Sagāde un avoti | Atspējot pirkšanas pieprasījuma sadales atiestatīšanas pogu | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | [Iespējot ar iepirkumu saistīto darbplūsmu atiestatīšanu](whats-new-scm-10-0-20.md) | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | [Ierobežot pirkšanas pasūtījuma rindu skaitu vienam pakešuzdevumam](whats-new-scm-10-0-27.md) | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | [Sapludināt kreditora finanšu dimensijas ar aktīvās dimensijas saites finanšu dimensiju pirkšanas pasūtījumā](whats-new-scm-10-0-25.md) | Obligāts |
| Sagāde un avoti | [Grāmatot uzkrāto preču reģistrēto daudzumu un atgādinājumus par neuzkrātajām precēm kvīšu un kreditoru rēķinu sagatavošanas nolūkā](whats-new-scm-10-0-26.md) | Vispārēji pieejams |
| Sagāde un avoti | [Novērsiet vispārīgu budžeta rezervāciju pārmērīgu patēriņu, ja darbplūsmā ir vairāki pirkšanas pieprasījumi](whats-new-scm-10-0-21.md) | Ieslēgts pēc noklusējuma |
| Sagāde un avoti | [Par pirkšanas līgumu atbildīgā puse](../procurement/purchase-agreements.md) | Obligāts |
| Sagāde un avoti | [Saglabātie pirkšanas pasūtījumu skati](saved-views-scm.md) | Obligāts |
| Preču informācijas pārvaldība | Materiālu komplekta pārskata pirmapstrāde, lai izvairītos no taimauta | Obligāts |
| Preču informācijas pārvaldība | Noklusējuma finanšu dimensijas atsevišķi, izmantojot krājumu veidnes | Obligāts |
| Preču informācijas pārvaldība | Iespējot preču dimensiju grupas krājumu veidnēm | Obligāts |
| Preču informācijas pārvaldība | Krājums — svītrkodu elementu uzlabojumi | Obligāts |
| Preču informācijas pārvaldība | Preces variantu nosaukumu atjaunošana, pamatojoties uz nomenklatūru | Obligāts |
| Preču informācijas pārvaldība | [Saglabātie izlaisto preču skati](saved-views-scm.md) | Obligāts |
| Preču informācijas pārvaldība | [Variantu ieteikumu lapas uzlabojumi](../pim/tasks/create-predefined-product-variants.md) | Obligāts |
| Pārdošana un mārketings | [Izmaksu sadalījums pārdošanas pasūtījumā](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Obligāts |
| Pārdošana un mārketings | Pārdošanas pasūtījumu atjauninājumu vēstures tīrīšana | Obligāts |
| Pārdošana un mārketings | [Pārdošanas atjauninājumu vēstures tīrīšana, pamatojoties uz vecumu](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Obligāts |
| Pārdošana un mārketings | [Kontaktpersonas datu entītijas eksporta optimizācija](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Obligāts |
| Pārdošana un mārketings | Kopēt pārdošanas kredīta notas kopējo atlaižu grupu | Obligāts |
| Pārdošana un mārketings | [Iespējot meklēšanu pārdošanas piedāvājuma dokumenta ievadam un dokumentu secinājumu laukiem](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Obligāts |
| Pārdošana un mārketings | [“100 populārāko” klientu pārskata veiktspējas uzlabošana](whats-new-scm-10-0-23.md) | Obligāts |
| Pārdošana un mārketings | Iekļaut gaidīšanas ierakstus vēstures tīrīšanas uzdevumos | Obligāts |
| Pārdošana un mārketings | Ierobežot pārdošanas pasūtījuma rindu skaitu vienam pakešuzdevumam | Ieslēgts pēc noklusējuma |
| Pārdošana un mārketings | [Ierobežot grāmatošanai atlasāmo pārdošanas pasūtījumu skaitu](whats-new-scm-10-0-21.md) | Obligāts |
| Pārdošana un mārketings | Aprēķinātās debitora bilances automātiska pārrēķināšana | Obligāts |
| Pārdošana un mārketings | [Pārdošanas atgriešanas pasūtījuma rindas reģistrācija ar precizitāti līdz decimāldaļām ar un bez pieļaujamā svara](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Obligāts |
| Pārdošana un mārketings | [Pārdošanas un mārketinga moduļa saglabātie skati](saved-views-scm.md) | Obligāts |
| Pārdošana un mārketings | [Viena klikšķa pārdošanas pasūtījuma apstiprinājums](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Obligāts |
| Transportēšanas pārvaldība | Atļaut kravas pavadzīmju nesaskaņošanu ar kravas rēķinu rindām bez iegrāmatota kreditora rēķinu žurnāla | Ieslēgts pēc noklusējuma |
| Transportēšanas pārvaldība | [Iespējo kreditora rēķinu žurnāla izveidi pēc vedmaksas rēķina atmešanas](whats-new-scm-10-0-20.md) | Ieslēgts pēc noklusējuma |
| Transportēšanas pārvaldība | [Mazu paku nosūtīšana](../warehousing/small-parcel-shipping.md) | Obligāts |
| Transportēšanas pārvaldība | [USMCA izcelsmes sertifikāta dokuments](../transportation/usmca-certification-of-origin.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Papildu atrašanās vietas zona](../warehousing/additional-location-zones.md) | Obligāts |
| Noliktavas vadība | [Atcelt darbu](../warehousing/cancel-warehouse-work.md) | Obligāts |
| Noliktavas vadība | [Konsolidēt sūtījumu](../warehousing/configure-shipment-consolidation-policies.md) | Obligāts |
| Noliktavas vadība | [Izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas](../warehousing/create-transfer-order-from-warehouse-app.md) | Obligāts |
| Noliktavas vadība | Pārkraušana sadales centrā — veidnes ar atrašanās vietas norādēm | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Izvietošanas darba atvienošana no IPPN](whats-new-scm-10-0-21.md) | Obligāts |
| Noliktavas vadība | [Atliktas izvietošanas operācijas](../warehousing/deferred-processing-manual-inventory-movement.md) | Obligāts |
| Noliktavas vadība | Atliktā izvietošana — konteiners | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Atliktās izvietošanas apstrāde — iespējot audita veidnes līdzeklim ar aktivizēšanas notikumu, kas iestatīts kā Iepriekšējais | Obligāts |
| Noliktavas vadība | [Sagaidāmā saņemšana no kvalitātes pārbaudes pasūtījumiem, kas izmanto aizturēto krājumu paraugus — atspējošana](../inventory/inventory-blocking.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Ātrās validācijas iespējošana noliktavu mobilajām ierīcēm | Obligāts |
| Noliktavas vadība | [Uzlabots GS1 svītrkodu parsētājs](../warehousing/gs1-barcodes.md) | Vispārēji pieejams |
| Noliktavas vadība | [Elastīga numura zīmes pasūtījuma rezervācija](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Obligāts |
| Noliktavas vadība | [Elastīga noliktavas līmeņa dimensijas rezervācija](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Obligāts |
| Noliktavas vadība | [Krājumu konsolidācijas novietojuma utilizācija](../warehousing/item-consolidation-location-utilization.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | Numurzīmes saņemšanas vēsture | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Manuāla sūtījumu konsolidācija](../warehousing/consolidate-shipments-manual-workbench.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Manuālās pārsūtīšanas rindas izdošanas pakalpojums administratoram vai līdzīgiem uzticamiem lietotājiem](whats-new-scm-10-0-28.md) | Vispārēji pieejams |
| Noliktavas vadība | [Materiālu apstrādes aprīkojuma interfeiss](../warehousing/mhax.md) | Obligāts |
| Noliktavas vadība | [Jaunas noslodzes plānošanas darba lapas](whats-new-scm-10-0-24.md) | Vispārēji pieejams |
| Noliktavas vadība | [Izejošās darba slodzes vizualizācija](../warehousing/outbound-workload-visualization.md) | Obligāts |
| Noliktavas vadība | [Plānotā pārkraušana sadales centrā](../warehousing/planned-cross-docking.md) | Obligāts |
| Noliktavas vadība | [Apstrādāt noliktavas programmas notikumus](../warehousing/warehouse-app-events.md) | Obligāts |
| Noliktavas vadība | Līdzprodukta un blakusprodukta vaicājuma uzlabošana aizkavē darba veidni | Obligāts |
| Noliktavas vadība | [Pēc izlaišanas uz noliktavu daudzumus noapaļot līdz tuvākajai pārdošanas vienībai](whats-new-scm-10-0-19.md) | Obligāts |
| Noliktavas vadība | [Saglabāts skats kravu plānošanas rīkam](saved-views-scm.md) | Obligāts |
| Noliktavas vadība | [Saglabāts skats darba detalizētās informācijas lapai](saved-views-scm.md) | Obligāts |
| Noliktavas vadība | [Saglabāts skats kopuma apstrādei](saved-views-scm.md) | Obligāts |
| Noliktavas vadība | [Saglabātie skati noslodzes apstrādei](saved-views-scm.md) | Obligāts |
| Noliktavas vadība | [Saglabātie skati sūtījuma apstrādei](saved-views-scm.md) | Obligāts |
| Noliktavas vadība | [Skenēt GS1 svītrkodus](../warehousing/gs1-barcodes.md) | Vispārēji pieejams |
| Noliktavas vadība | Sūtījuma kopuma etiķetes detalizētā informācija | Obligāts |
| Noliktavas vadība | [Slotu jauktās vienības](whats-new-scm-10-0-21.md) | Obligāts |
| Noliktavas vadība | [Izmantojiet ātrāku API konteineru aizvēršanai/atkārtotai atvēršanai iepakošanas stacijā](whats-new-scm-10-0-21.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Papildināšanas darbiem atlasīto veidņu apstiprināšana](whats-new-scm-10-0-20.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Reklamētie lauki programmā Warehouse](../warehousing/warehouse-app-promoted-fields.md) | Obligāts |
| Noliktavas vadība | [Norādījumi par noliktavas programmas darbībām](../warehousing/mobile-app-titles-instructions.md) | Obligāts |
| Noliktavas vadība | [Noliktavas vietas statuss](../warehousing/warehouse-location-status.md) | Obligāts |
| Noliktavas vadība | [Programmas Warehouse Management apiešana](../warehousing/warehouse-app-detours.md) | Ieslēgts pēc noklusējuma |
| Noliktavas vadība | [Kopuma pakešuzdevuma detalizētā informācija](../warehousing/wave-processing.md) | Obligāts |
| Noliktavas vadība | [Kopuma izpildes paziņojumi](../warehousing/wave-execution-notifications.md) | Obligāts |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.29 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet [Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā 10.0.29 (2022. gada oktobris)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas ietverti katrā atjauninājumā, kas ir daļa no versijas 10.0.29, piesakieties lifecycle Services (LCS) [un skatiet zināšanu bāzes rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 un rūpniecības mākoņi: 2022. gada 1. laidiena plāns

Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Apskatiet [Dynamics 365 un rūpniecības mākoņi: 2022. gada 2. laidiena plāns](/dynamics365-release-plan/2022wave2/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Noņemtie un novecojušie Supply Chain Management līdzekļi

Noņemtie [vai novecojušie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) rakstā apraksta funkcijas, kas ir noņemtas vai ieplānotas izņemšanai vai nolietojumam Piegādes ķēžu pārvaldībai.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda līdzekļa noņemšanas no preces paziņojums [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) par nolietojumu tiks papildu pievienots 12. rakstu funkcionalitātes Noņemtie vai novecojušie 12 mēnešu skaits pirms noņemšanas.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
