---
title: Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.21 (2021. gada oktobris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Dynamics 365 Supply Chain Management 10.0.21.
author: kamaybac
ms.date: 10/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 91462cc589be6170418f7f78267feea5e25c037d
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123784"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.21 (2021. gada oktobris)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti Microsoft Dynamics 365 Supply Chain Management versijā 10.0.21. Šai versijai ir būvējuma numurs 10.0.960, un tas ir pieejams šeit:

- **Laidiena priekšskatījums:** 2021. gada augusts
- **Vispārēja laidiena (pašatjauninājums) pieejamība:** 2021. gada septembris
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2021. gada oktobris

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Kolonna *Līdzeklis* nodrošina saites uz [izlaišanas plānu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), kur varat redzēt oficiālos izlaišanas datumus katram līdzeklim. Kolonna *Vairāk informācijas* sniedz detalizētu informāciju un/vai saites uz saistīto dokumentāciju.

Vairumam šo līdzekļu ir jābūt iespējotiem, izmantojot [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), pirms varat tos izmantot.

| Līdzekļu apgabals | Funkcija | Papildinformācija |
|---|---|---|
| Krājumi&nbsp;un&nbsp;loģistika | [Globālā krājumu uzskaites pievienojumprogramma Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Globālās krājumu uzskaites sākumlapa](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Rīcībā esošo korekciju grāmatošana, izmantojot kodus, kas saistīti ar korespondējošo kontu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Krājumu inventarizācijas iemeslu kodi](../warehousing/reason-codes-for-counting-journals.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Tādu datu eksportēšanas politika, uz kuriem atsaucas pārdošanas piedāvājums](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Izvēlieties, vai izmaiņas datos, uz kuriem atsaucas piedāvājumi, izraisīs šo piedāvājumu (vai rindu) iekļaušanu nākamajā inkrementālajā eksportā. Inkrementālais eksports notiks ātrāk, ja izvēlaties neiekļaut šādus piedāvājumus vai rindas.<br><br>Šis līdzeklis pievieno iestatījumu ar nosaukumu **Izlaist pārdošanas piedāvājumu atsauces datus izmaiņu izsekošanas laikā** lapā **Debitoru parametri**. |
| Krājumi&nbsp;un&nbsp;loģistika | [Aizzīmogotā izsole](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sealed-bidding) | [Slēgta piedāvājumu izteikšana PP](../procurement/sealed-bidding.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Vieglā rezervācija krājumu redzamības pievienojumprogrammai](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Krājumu redzamības rezervācija](../inventory/inventory-visibility-reservations.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Ieturējumu un pieļaujamā svara uzlabojumi atlaižu pārvaldībai](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Ieturējumu pārvaldība, izmantojot ieturējumu rīku](../rebate-management/deduction-workbench.md )<br><br>[Atlaižu apstrāde, pārskatīšana un grāmatošana](../rebate-management/process-review-post.md)<br><br>[Atlaižu pārvaldības darījumi](../rebate-management/rebate-management-deals.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Norādījumi par noliktavas programmas darbībām](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Darbību nosaukumu un instrukciju pielāgošana Warehouse Management mobilajai programmai](../warehousing/mobile-app-titles-instructions.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Darba pārtraukumi un izsekošanas atjauninājumi izkraušanas izmaksām](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Atjaunināt izsekošanu izvietošanai](../landed-cost/update-tracking-putaway.md )<br><br>[Tranzīta preču apstrāde](../landed-cost/in-transit-processing.md) |
| Vispārējā plānošana | [Negatīvās dienas optimizācijas plānošanai](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Aizkaves tolerance (negatīvās dienas)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi). Ja vēlaties izmantot kādu no šiem līdzekļiem, tos ir skaidri jāiespējo [Līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa&nbsp;nosaukums&nbsp;līdzekļu&nbsp;pārvaldībā | Papildinformācija |
|---|---|---|
| Izmaksu pārvaldība | Detalizēta informācija par krājuma slēgšanas norisi | Šis priekšskatījuma līdzeklis iespējo detalizētu krājumu slēgšanas progresa pārskatu. |
| Sagāde un avoti | Novērsiet vispārīgu budžeta rezervāciju pārmērīgu patēriņu, ja darbplūsmā ir vairāki pirkšanas pieprasījumi | Šis priekšskatījuma līdzeklis uzlabo kļūdu pārbaudi, kad lietotāji iesniedz un apstiprina pirkšanas pieprasījumus, kas pārsniedz vispārējās budžeta rezervēšanas rindas atlikušo bilanci. Tas palīdz novērst vispārējo budžeta rezervāciju pārtvēršanu, ja vairāki pirkšanas pieprasījumi atrodas darbplūsmā. |
| Ražošanas kontrole | Ražotnes izpildes saskarnē rādīt pilnus sērijas, partijas numurus un unikālos noliktavas vienības identifikatorus | Šis līdzeklis nodrošina uzlabotu pieredzi sarakstu apskatīšanai ar sērijas, partijas un numura zīmes numuriem ražošanas izpildes interfeisā. Rādīšanas izmaiņas no karšu skata ar ierobežotu rakstzīmju skaitu uz saraksta skatu, kas nodrošina pietiekami daudz vietas pilnu vērtību rādīšanai. Šis saraksts arī nodrošina iespēju meklēt noteiktus numurus. |
| Pārdošana un mārketings | Ierobežot grāmatošanai atlasāmo pārdošanas pasūtījumu skaitu | Šī funkcija ļauj definēt maksimālo pārdošanas pasūtījumu skaitu, ko var atlasīt, grāmatojot apstiprinājumus, izdošanas sarakstus, pavadzīmes un rēķinus no pārdošanas pasūtījumu saraksta lapas. Tas tiek aktivizēts automātiski. Šis līdzeklis pievieno iestatījumu ar nosaukumu **Maksimālais pārdošanas pasūtījumu skaits grāmatošanai** **Debitoru parādu parametru** lapā. Jaunais iestatījums pēc noklusējuma ir *100*. Šī funkcija palīdz uzlabot pārdošanas pasūtījumu saraksta lapas veiktspēju, kad ir atlasīts liels skaits pārdošanas pasūtījumu. Tas neietekmē pārdošanas pasūtījumu skaitu, ko var apstrādāt periodisks uzdevums. |
| Noliktavas vadība | Izvietošanas darba atvienošana no IPPN | Šis līdzeklis ir nepieciešams, lai sūtītu un saņemtu iepriekšējus paziņojumus par nosūtīšanu (IPPN), kad palaižat noliktavas vadības darba slodzi mēroga vienībā (kā daļu no sadalītās transportlīdzekļa topoloģijas). Tajā ir pievienota jauna datu bāzes tabula, kas atvēlēta informācijas glabāšanai par izvietošanas darbu. Iepriekš šī informācija tika glabāta tabulās, kas tiek izmantotas arī IPPN. |
| Noliktavas pārvaldība | Slotu jauktās vienības | Ļauj sistēmai slota krājumus vietās, kas ietver jauktas vienības (piemēram, kastes un kārbas). Katrai slotas veidnes rindai šis līdzeklis ļauj izvēlēties, vai rindai vajadzētu sadalīt vienumus jauktas vienības vai vienas vienības vietās. |
| Noliktavas pārvaldība | Izmantojiet ātrāku API konteineru aizvēršanai/atkārtotai atvēršanai iepakošanas stacijā | Kad ir iespējots šis priekšskatījuma līdzeklis, krājumu darbības, kas saistītas ar konteineriem, tiek izveidotas, izmantojot jaunu bezsvara procesu, kas uzlabo konteineru slēgšanas vai atvēršanas veiktspēju manuālas iepakošanas stacijas apstrādes laikā. |

## <a name="features-turned-on-by-default-in-this-release"></a>Līdzekļi, kas šajā laidienā ir ieslēgti pēc noklusējuma

Šajā tabulā ir uzskaitīti līdzekļi, kas pēc noklusējuma ir ieslēgtas 10.0.21. Lielāko daļu līdzekļu, kas ir atomātiiski ieslēgti, var izslēgt [Līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Līdzekļa nosaukums | Iespējošanas datums | Līdzeklis pievienots | Līdzekļa statuss | Modulis |
| :--- | :--- | :--- | :--- | :--- |
| Krājumu rīcībā esošā pārskata glabāšana | 9/1/2021 | 4/1/2020 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Pārsūtīt pasūtījuma atcelšanu | 9/1/2021 | 7/13/2020 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Atbloķēt krājumu žurnālu | 9/1/2021 | 8/17/2020 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Saglabātie krājumu pārvaldības skati | 9/1/2021 | 30.09.2020. | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Navigācija no MK versijas no MK rindām | 9/1/2021 | 11/11/2019 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Mērvienības un vienības daudzuma izmantošana krājumu žurnālos | 9/1/2021 | 11/11/2019 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Atļaut tukšas partijas atribūtu vērtības | 9/1/2021 | 11/11/2019 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Automātiski palielināt krājumu pārsūtīšanas pasūtījuma rindu numurus | 9/1/2021 | 10/11/2019 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Krājumu žurnāla apstiprināšanas darbplūsma | 9/1/2021 | 1/6/2020 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Iespējojiet krājumu kvalitātes pārvaldības parametru brīdināšanas funkciju | 9/1/2021 | 10/7/2019 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Izveidot pārsūtīšanas pasūtījumu no pārdošanas rindas | 9/1/2021 | 8/31/2019 | Ieslēgts pēc noklusējuma | Krājumu un noliktavas pārvaldība |
| Prognožu modeļa izvēle sadaļas Pieprasījuma apjoma prognoze detalizētās informācijas daļā | 9/1/2021 | 10/11/2019 | Ieslēgts pēc noklusējuma | Vispārējā plānošana |
| Vispārējās plānošanas norises vizualizācija | 9/1/2021 | 10/7/2019 | Ieslēgts pēc noklusējuma | Vispārējā plānošana |
| Plānošanas optimizācijas automātiskā apstiprināšana | 9/1/2021 | 10/11/2019 | Ieslēgts pēc noklusējuma | Vispārējā plānošana |
| Paralēla plānoto pasūtījumu apstiprināšana | 9/1/2021 | 8/31/2019 | Ieslēgts pēc noklusējuma | Vispārējā plānošana |
| Ziņojums par piedāvājuma sekmīgu iesniegšanu | 9/1/2021 | 5/15/2019 | Ieslēgts pēc noklusējuma | Sagāde un avoti |
| Pirkšanas pasūtījumam pievienota PP atsauces saite | 9/1/2021 | 8/31/2019 | Ieslēgts pēc noklusējuma | Sagāde un avoti |
| Iespēja apstiprināt pieņemtus pirkšanas pasūtījumus no kreditora sadarbības partijā | 9/1/2021 | 9/10/2019 | Ieslēgts pēc noklusējuma | Sagāde un avoti |
| CXML uzlabojumu iegāde | 9/1/2021 | 11/11/2019 | Ieslēgts pēc noklusējuma | Sagāde un avoti |
| Rādīt saiti &quot;Atvērt publicētos piedāvājuma pieprasījumus&quot; kā elementu | 9/1/2021 | 30.09.2020. | Ieslēgts pēc noklusējuma | Sagāde un avoti |
| PP jautājumi un atbildes | 9/1/2021 | 2/19/2020 | Ieslēgts pēc noklusējuma | Sagāde un avoti |
| Bīstamo materiālu preču informācija un nosūtīšanas dokumentācija | 9/1/2021 | 6/14/2020 | Ieslēgts pēc noklusējuma | Preču informācijas pārvaldība |
| Noklusējuma pasūtījumu daudzumu stingra validācija | 9/1/2021 | 6/24/2020 | Ieslēgts pēc noklusējuma | Preču informācijas pārvaldība |
| Izcelsmes valsts/reģiona pārvaldības līdzeklis | 9/1/2021 | 7/13/2020 | Ieslēgts pēc noklusējuma | Preču informācijas pārvaldība |
| Saglabātie izlaisto preču skati | 9/1/2021 | 30.09.2020. | Ieslēgts pēc noklusējuma | Preču informācijas pārvaldība |
| Uzlabojumi apstiprināšanas un pārsūtīšanas darbu dialogos | 9/1/2021 | 10/11/2019 | Ieslēgts pēc noklusējuma | Ražošanas kontrole |
| Darbu kartes ierīcei ir pievienota noliktavas vienībai, lai ziņotu par pabeigšanu | 9/1/2021 | 8/31/2019 | Ieslēgts pēc noklusējuma | Ražošanas kontrole |
| Darba kartes termināļa lapai ir pievienota jauna poga pārtraukuma apturēšanai | 9/1/2021 | 2/19/2020 | Ieslēgts pēc noklusējuma | Ražošanas kontrole |
| Iespējojiet daļēju apakšlīgumu elementu saņemšanu un novērsiet problēmu ar kreditora veida MK rindu brāķa aprēķināšanu. | 9/1/2021 | 11/11/2019 | Ieslēgts pēc noklusējuma | Ražošanas kontrole |
| Saglabātie skati ražošanas kontrolei | 9/1/2021 | 8/17/2020 | Ieslēgts pēc noklusējuma | Ražošanas kontrole |
| Dynamics 365 Guides ražošanai | 9/1/2021 | 7/13/2020 | Ieslēgts pēc noklusējuma | Ražošanas kontrole |
| Ražošanas izpilde | 9/1/2021 | 30.09.2020. | Ieslēgts pēc noklusējuma | Ražošanas kontrole |
| Līdzeklis darba kartes ierīces un darba kartes termināļa aizturēšanai, lai var veikt to tīrīšanu | 9/1/2021 | 5/10/2020 | Ieslēgts pēc noklusējuma | Ražošanas kontrole |
| Izmaksu sadalījums pārdošanas pasūtījumā | 9/1/2021 | 30.09.2020. | Ieslēgts pēc noklusējuma | Pārdošana un mārketings |
| Ierobežot grāmatošanai atlasāmo pārdošanas pasūtījumu skaitu | 9/1/2021 | 9/1/2021 | Ieslēgts pēc noklusējuma | Pārdošana un mārketings |
| Pārdošanas pasūtījumu atjauninājumu vēstures tīrīšana | 9/1/2021 | 9/1/2021 | Ieslēgts pēc noklusējuma | Pārdošana un mārketings |
| Mainīt cikla inventarizācijas darba skaitļu secību | 9/1/2021 | 10/7/2019 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Kopuma pieprasījuma papildināšana, pamatojoties uz nodokļiem | 9/1/2021 | 10/7/2019 | Obligāts | Noliktavas vadība |
| Paslēpt lauku Kopējā vērtība &quot;Visas kravas&quot; un &quot;Detalizēta informācija par kravu&quot; lapās | 9/1/2021 | 10/7/2019 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Kopuma etiķešu drukāšana | 9/1/2021 | 2/19/2020 | Obligāts | Noliktavas vadība |
| Saistīt pirkšanas pasūtījuma krājumu transakcijas ar kravu | 9/1/2021 | 1/6/2020 | Obligāts | Noliktavas vadība |
| Uzlaboti noliktavas vienību etiķešu izkārtojumi | 9/1/2021 | 2/19/2020 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Organizācijas mēroga darba aizturēšana | 9/1/2021 | 2/19/2020 | Obligāts | Noliktavas vadība |
| Detalizēta darba rindas informācija | 9/1/2021 | 10/11/2019 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Padariet rediģējamu mobilās ierīces krājumu kustības krājumu statusa lauku | 9/1/2021 | 10/16/2019 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Apstiprināt izejošos sūtījumus no pakešuzdevumiem | 9/1/2021 | 7/13/2020 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Kontrolēt, vai mobilajās ierīcēs rādīt saņemšanas kopsavilkuma lapu | 9/1/2021 | 4/1/2020 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Piedāvāt atrisināt neskaidrus vienumu &#39;Atrašanās vieta/Noliktavas vienība&#39; nosaukumus | 9/1/2021 | 4/1/2020 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Preces variantu un izsekošanas dimensiju tveršana noliktavas lietotnē noslodzes krājuma saņemšanas laikā | 9/1/2021 | 5/10/2020 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Neļaujiet radīt noslodzes, kas neatbilst kopuma noslodzes izveides veidnes prasībām. | 9/1/2021 | 8/17/2020 | Ieslēgts pēc noklusējuma | Noliktavas vadība |
| Novērtējiet visas vairāku SKU atrašanās vietas direktīvu darbības | 9/1/2021 | 30.09.2020. | Ieslēgts pēc noklusējuma | Noliktavas vadība |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Mēs nesen pievienojam vai būtiski atjauninājām šādus palīdzības rakstus. Tās ne vienmēr ir saistītas ar jaunajiem līdzekļiem, kas pievienoti šim laidienam, kā uzskaitīts iepriekšējā sadaļā, taču tās var palīdzēt jums pilnīgāk izmantot esošos līdzekļus.

| Līdzekļu apgabals | Jauni vai atjaunināti raksti |
|---|---|
| Vispārējā plānošana | [Krājumu prognozes](../master-planning/inventory-forecast.md) |
| Vispārējā plānošana | [Parametri, kas netiek izmantoti plānošanas optimizācijai](../master-planning/planning-optimization/not-used-parameters.md) |
| Vispārējā plānošana | [Papildināšanas metodes un daudzuma modificēšana](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Vispārējā plānošana | [Plānošana ar neierobežotu noslodzi](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Vispārējā plānošana | [Plāna vēstures un plānošanas žurnālu skatīšana](../master-planning/planning-optimization/plan-history-logs.md) |
| Noliktavas pārvaldība | [Konteineru iepakošanas stratēģijas](../warehousing/container-packing-strategy-overview.md) |
| Noliktavas pārvaldība | [Cikla inventarizācijas piemēru scenāriji](../warehousing/cycle-counting-scenarios.md) |
| Noliktavas vadība | [Ienākošo IPPN importēšana, izmantojot V3 datu elementu](../warehousing/import-asn-data-entity.md) |
| Noliktavas vadība | [Pārdošanas pasūtījumu un pārsūtīšanas pasūtījumu pārmērīga izdošana](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Noliktavas pārvaldība | [Kopuma etiķešu drukāšanas plānošana kopuma laikā](../warehousing/configure-task-based-wave-label-printing.md) |
| Noliktavas pārvaldība | [Kas jauns vai mainīts mobilajā programmā Warehouse Management](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.21 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet [Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā 10.0.21 (2021. gada oktobris)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.21, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

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

