---
title: Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.29 (2022. gada oktobris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti Microsoft Dynamics 365 Supply Chain Management 10.0.29.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 8f6ba18096cffe907c339ad525c99535bc5ee568
ms.sourcegitcommit: 7745c4bd3ab3aace4b4cb814eaf0cfdbae4a0cbd
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9784698"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10029-october-2022"></a>Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.29 (2022. gada oktobris)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti Microsoft Dynamics 365 Supply Chain Management versijā 10.0.29. Šai versijai ir būvējuma numurs 10.0.1326, un tā ir pieejama šādā grafikā:

- **Laidiena priekšskatījums:** 2022. gada augusts
- **Vispārēja laidiena (pašatjauninājums) pieejamība:** 2022. gada septembris
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada oktobris

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varam atjaunināt šo rakstu, lai iekļautu līdzekļus, kas tika pievienoti būvējumam pēc šī raksta sākotnējās publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Krājumi un loģistika | [WMS vienumu piešķiršana un rezervēšana krājumu redzamībā](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | [Inventory Visibility atbalsts WMS krājumiem](../inventory/inventory-visibility-whs-support.md) | Iespējots pēc noklusējuma |
| Krājumi un loģistika | [Rīcībā esošo krājumu sarakstu iepriekšēja ielāde](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | [Inventory Visibility programmas lietošana](../inventory/inventory-visibility-power-platform.md) | Iespējots pēc pakalpojuma konfigurācijas |
| Veidošanas pasūtījumā piegādes automatizācija | [Veidošanas pasūtījumā piegādes automatizācija](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Veidošanas pasūtījumā piegādes automatizācija](../master-planning/make-to-order-supply-automation.md) | Līdzekļu pārvaldība:<br>*Veidošanas pasūtījumā piegādes automatizācija* |
| Plānošana | [Skatīt un lietot detalizētus ieskatus par DDMRP](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Uz pieprasījumu balstītu materiālu prasību plānošanas pārskats](../master-planning/planning-optimization/ddmrp-overview.md) | Līdzekļu pārvaldība:<br>*(Priekšskatījums) DDMRP plānošanas optimizācijai* |
| Ražošanas kontrole | [Gatavo preču padarīšana par fiziski pieejamām pirms grāmatošanas žurnālos](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Gatavo preču padarīšana par fiziski pieejamām pirms grāmatošanas žurnālos](../production-control/deferred-posting.md) | Līdzekļu pārvaldība:<br>*(Priekšskatījums) Padarīt gatavās preces fiziski pieejamas pirms grāmatošanas žurnālos* |
| Noliktavas vadība | [Meklējiet atbilstošos datus noliktavas mobilajā programmā](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Vaicājumu dati, izmantojot mobilās programmas Warehouse Management apiešanu](../warehousing/warehouse-app-data-inquiry.md) | Līdzekļu pārvaldība:<br>*Warehouse Management programmas datu uzziņu plūsma* |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt kādu no šiem līdzekļiem, tas ir jādara līdzekļu [pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Izmaksu pārvaldība | Gaidoša līdzprodukta cenas aprēķina optimizācija | Šis līdzeklis novērš konfliktu, kas dažkārt var rasties, ja līdzproduktu cenas tiek aprēķinātas, izmantojot vairākus pavedienus. Tas liek sistēmai pārliecināties, ka katra līdzprodukta cena tiek aprēķināta tikai vienu reizi. Šī aprēķina rezultāts pēc tam tiek izmantots kā ievaddati visiem pārējiem aprēķiniem. Ja gaidošā cena jau pastāv, šī cena tiek izmantota. |
| Vispārējā plānošana | Grupu darījumi Plānošanas optimizācijā | Šis līdzeklis var palīdzēt samazināt plānoto pasūtījumu skaitu, kas tiek ģenerēti, lai nodrošinātu vienu pārdošanas pasūtījuma rindu, kad izmantojat plānošanas optimizāciju. Ja šis līdzeklis ir ieslēgts, plānošanas optimizācija grupēs visas krājumu transakcijas pasūtījuma rindai vienā prasībā pilnam daudzumam. (Šī darbība atbilst iebūvētās plānošanas programmas darbībai.) Piedāvājums un pieprasījums ir sagrupēti atsevišķi. Tāpēc šis līdzeklis palīdz samazināt transakciju apjomu, ja jums ir sadalītas transakcijas un ja izmantojat dimensijas (piemēram, partijas numurus vai sērijas numurus), kas nav pārklājuma kategorijas. |
| Sagāde un avoti | Kreditora aizturēšana pirkšanas pasūtījumiem | Šis līdzeklis ļauj aizturēt pirkšanas pasūtījumu kreditoru. Tas pievieno jaunu *pirkšanas pasūtījuma* aizturēšanas tipu, kas atzīmē kreditoru kā aizturētu pirkšanas pasūtījumiem. Jūs nevarēsit izveidot jaunus pirkšanas pasūtījumus kreditoriem, kas ir aizturēti pirkšanas pasūtījumiem, bet jūs joprojām varēsit turpināt visus atvērtos rēķinus vai maksājumus par šiem kreditoriem. |
| Pārdošana un mārketings | Aprēķināt rindas neto summu importējot | Šis līdzeklis ļauj kontrolēt, vai sistēmai ir jāpārrēķina rindu kopsummas, importējot datus, izmantojot pārdošanas pasūtījuma rindas *,* *pārdošanas piedāvājuma rindas* vai atgriešanas pasūtījuma rindu *entītiju, izmantojot OData vai* dubulto rakstīšanu. Tam ir ietekme tikai tad, ja ir ieviestas arī tirdzniecības līgumu novērtēšanas politikas, kas ierobežo izmaiņas **pārdošanas pasūtījuma rindu, pārdošanas piedāvājuma rindu un/vai atgriešanas pasūtījuma rindu laukā Neto summa**. Tas pievieno iestatījumu ar nosaukumu **Aprēķināt rindas neto summu** **lapai Debitoru parādi > iestatīšana > debitoru parādu parametri**. Ja šis iestatījums ir iestatīts uz Jā *, sistēma vienmēr pārrēķinās rindu summas, kad tas būs nepieciešams (tādējādi ignorējot tirdzniecības nolīguma novērtēšanas politiku attiecībā uz* rindas neto summu). Ja iestatījums ir iestatīts uz *Nē*, sistēma nekad automātiski neaprēķinās rindas neto summu, pat ja ienākošās rindas cenas, daudzuma un/vai diskonta izmaiņas nozīmētu, ka rindas neto summa ir jāpārrēķina. Šis līdzeklis ir iespējots pēc noklusējuma un sākotnēji iestata **opciju Aprēķināt rindas neto summu** uz *Jā*. Iestatījums *No* atbilst sistēmas darbībai pirms versijas 10.0.23 un tiek nodrošināts galvenokārt, lai atbalstītu mantotos integrācijas scenārijus.<br><br>Papildinformāciju skatiet sadaļā [Rindu neto summu pārrēķināšana, importējot pārdošanas pasūtījumus, piedāvājumus un atgriezes](../sales-marketing/calc-line-net-amounts-import.md). |
| Pārdošana un mārketings | Aprēķināt pārdošanas kopsummas, izmantojot vairākus pavedienus | Šis līdzeklis palīdz uzlabot veiktspēju, ļaujot sistēmai izmantot paralēlo apstrādi, aprēķinot pārdošanas kopsummas partijā. Šis līdzeklis pievieno jaunu **lauku Pavedienu** skaits dialoglodziņam **Pārdošanas kopsummu** aprēķināšana. Ja izvēlaties izpildīt aprēķinu pakešveidā, varat izmantot šo lauku, lai iestatītu maksimālo pavedienu skaitu. Ja iestatāt vērtību uz *0* (nulle) vai *1*, tiks izmantots viens pavediens. Vērtības, kas pārsniedz 1, iespējo vairākpavedienu veidošanu. |
| Pārdošana un mārketings | Atjaunināt starpuzņēmumam manuāli ievadītās cenas un atlaides | Šis līdzeklis pievieno atbalstu manuālām izmaiņu politikām starpuzņēmumu pasūtījumiem. Tas ietver atbalstu manuālu izmaiņu politiku pārsūtīšanai starp starpuzņēmumu pārdošanas un pirkšanas pasūtījumiem. Iepriekš manuālo izmaiņu politikas tika atbalstītas tikai pasūtījumiem, kas nav starpuzņēmumu pasūtījumi. Kad šis līdzeklis ir iespējots, sistēma sniegs jums iespēju atjaunināt cenas un atlaides pēc izmaiņu saglabāšanas starpuzņēmumu pasūtījumā. Šī opcija ļauj izvēlēties, vai starpuzņēmumu pasūtījumam vēlaties lietot jaunās cenas un detalizētu informāciju par atlaidēm vai atstāt pasūtījumu nemainītu. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Nesen esam pievienojuši vai ievērojami atjauninājuši tālāk norādītos palīdzības rakstus. Šie raksti ne vienmēr ir saistīti ar jaunajiem līdzekļiem, kas tika pievienoti šim laidienam, kā norādīts iepriekšējās sadaļās. Tomēr tie var palīdzēt jums iegūt vairāk no esošajām funkcijām.

| Līdzekļu apgabals | Jauni vai atjaunināti raksti |
|---|---|
| Vispārējā plānošana, CTP | [Pārdošanas pasūtījuma piegādes datumu aprēķināšana, izmantojot CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Vispārējā plānošana, DDMRP | [Uz pieprasījumu balstītu materiālu prasību plānošanas pārskats](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Ieslēdziet DDMRP līdzekli savā sistēmā](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Krājumu pozīcija](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Bufera profils un līmeņi](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Uz pieprasījumu balstīta plānošana](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Vizuāla un sadarbības izpilde](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Noliktavas vadība | [Konteineru iepakošana nosūtīšanai](../warehousing/packing-containers.md)<br>[Iepakošanas darbs izejošo konteineru iepakošanai un sūtījumu apstrādei](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Līdzekļu stāvokļa izmaiņas šajā laidienā

Šajā tabulā ir uzskaitīti līdzekļi, kas versijā 10.0.29 kļuva obligāti vai ieslēgti pēc noklusējuma. Visi šie līdzekļi tiks automātiski ieslēgti jūsu sistēmā, tiklīdz atjaunināsit uz versiju 10.0.29. Obligātos līdzekļus nevar izslēgt, bet līdzekļus, kas ir ieslēgti pēc noklusējuma, joprojām var izslēgt, izmantojot [līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabulā ir uzskaitīti arī līdzekļi, kas iepriekš bija publiskajā priekšskatījumā, bet ir mainīti, kļūstot vispārēji pieejami versijā 10.0.29. Šīs izmaiņas norāda, ka līdzekļus tagad ieteicams izmantot ražošanas vidēs. Šie līdzekļi pēc noklusējuma ir izslēgti, ja vien nav norādīts citādi. Tāpēc jums ir jāizmanto [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai tos iespējotu, ja vēlaties tos izmantot.

| Modulis | Līdzekļa nosaukums | Jauns līdzekļu stāvoklis |
| --- | --- | --- |
| Līdzekļu pārvaldība | [Aktīvu pārvaldības funkcionalitāte ražošanas izpildes interfeisam](../production-control/production-floor-execution-configure.md) | Obligāts |
| Izmaksu pārvaldība | [Mainīt atcelšanas etiķeti vienumā Slēgšana un korekciju uz operāciju Atsaukt](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Obligāts |
| Izmaksu pārvaldība | Notīrīt MK aprēķina detaļas par šķērsizmaksu versijām | Obligāts |
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
| Krājumu un noliktavas pārvaldība | Krājumu pārsūtīšanas pasūtījuma rindu numuru automātiska palielināšana | Obligāts |
| Krājumu un noliktavas pārvaldība | Izveidot pārsūtīšanas pasūtījumu no pārdošanas rindas | Obligāts |
| Krājumu un noliktavas pārvaldība | Atspējot krājumu žurnāla rindas lauku darbplūsmā | Obligāts |
| Krājumu un noliktavas pārvaldība | Iespējojiet krājumu kvalitātes pārvaldības parametru brīdināšanas funkciju | Obligāts |
| Krājumu un noliktavas pārvaldība | (Ķīna) Izslēdziet fiziskās saņemšanas un izdošanas izmaksas no mēneša vidējām izmaksām | Ieslēgts pēc noklusējuma |
| Krājumu un noliktavas pārvaldība | [Krājumu žurnāla apstiprināšanas darbplūsma](../inventory/inventory-journal-workflow.md) | Obligāts |
| Krājumu un noliktavas pārvaldība | [Krājumu rīcībā esošā pārskata glabāšana](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Obligāts |
| Krājumu un noliktavas pārvaldība | [Saglabāti skati krājumu pārvaldībai](saved-views-scm.md) | Obligāts |
| Krājumu un noliktavas pārvaldība | Pārskaitījuma pasūtījuma atcelšana | Obligāts |
| Krājumu un noliktavas pārvaldība | Mērvienības un vienības daudzuma izmantošana krājumu žurnālos | Obligāts |
| Krājumu un noliktavas pārvaldība | Krājumu žurnāla atbloķēšana | Obligāts |
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
| Sagāde un avoti | Maksa par pirkšanas pasūtījumiem un to summām | Obligāts |
| Sagāde un avoti | Poga Atspējot pirkšanas pieprasījuma izplatīšanu Atiestatīt | Ieslēgts pēc noklusējuma |
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
| Noliktavas vadība | [Jaunas slodzes plānošanas darbgalda lapas](whats-new-scm-10-0-24.md) | Vispārēji pieejams |
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

### <a name="platform-updates-for-finance-and-operations-apps"></a>Programmu Finance and Operations platformas atjauninājumi

Microsoft Dynamics 365 Supply Chain Management 10.0.29 ietver platformas atjauninājumus. Papildinformāciju skatiet rakstā [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.29 (2022. gada oktobris)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā atjauninājumā, kas ir daļa no versijas 10.0.29, piesakieties Lifecycle Services (LCS) un skatiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 un rūpniecības mākoņi: 2022. gada 1. laidiena plāns

Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Apskatiet [Dynamics 365 un rūpniecības mākoņi: 2022. gada 2. laidiena plāns](/dynamics365-release-plan/2022wave2/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Noņemtie un novecojušie Supply Chain Management līdzekļi

Rakstā Noņemtie [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) vai novecojušie līdzekļi apraksta līdzekļus, kas ir noņemti vai ir plānoti noņemšanai vai novecošanai programmatūrā Supply Chain Management.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda līdzekļa noņemšanas no produkta 12 mēnešus pirms noņemšanas paziņojums par novecošanu tiks paziņots [raksta sadaļā Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) Noņemtie vai novecojušie līdzekļi.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
