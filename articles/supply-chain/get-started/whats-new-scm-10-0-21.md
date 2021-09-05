---
title: Izlaiduma Dynamics 365 Supply Chain Management 10.0.21 priekšskatījums (2021. gada oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Supply Chain Management 10.0.21.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 42d296cb0402b5e96f23d628f08a28fb35683d5f
ms.sourcegitcommit: 5a44eb4f555bf5ee0b1293f0ecdc37ee8b53aa24
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/17/2021
ms.locfileid: "7391212"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>Izlaiduma Dynamics 365 Supply Chain Management 10.0.21 priekšskatījums (2021. gada oktobris)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā uzskaitīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti Microsoft Dynamics 365 Supply Chain Management versijas 10.0.21 priekšskatījumā. Šai versijai ir būvējuma numurs 10.0.960, un tas ir pieejams šeit:

- **Laidiena priekšskatījums:** 2021. gada augusts
- **Vispārēja laidiena (pašatjauninājums) pieejamība:** 2021. gada septembris
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2021. gada oktobris

## <a name="known-deployment-issue"></a>Zināma izvietošanas problēma

Izvietojot laidienu 10.0.21 vietnē IaaS, varat saņemt šādu izvietošanas brīdinājumu:

**Brīdinājuma kods:** 95017

**Brīdinājuma ziņojums:** Skriptu \[SetupDiagnostics\] neizdevās izpildīt pret VM

Izvietošana darbosies, neskatoties uz brīdinājumu. Tomēr programmā Lifecycle Services (LCS) var rasties šādas zināmās problēmas:

- Lapā **Vides uzraudzība** nebūs redzama saite **Skatīt detalizētās versijas informāciju**, tādēļ nevarēsit redzēt specifiskās moduļu versijas, kas ir instalētas jūsu vidē. Ja nav pieejami šie dati, turpmākie labojumfaili var neizdoties, jo labojumfailu lietošanas process izmanto šos datus, lai pārbaudītu, vai moduļa versijas priekšnosacījumi ir izpildīti. Tā kā nav iespējams izmantot PEAP/Priekšskatījuma būvējumu ražošanā vai lietot labojumfailus, ietekmei ir jābūt minimālai.
- Cilnes **Veiktspējas rādītāji** un **Indeksu analīze** lapā **Vides uzraudzība** zem SQL Insights netiks parādīti dati. Visi pārējie **Vides uzraudzības** līdzekļi darbosies, kā paredzēts.
- Lapai **Pilnas sistēmas diagnostika** nevar piekļūt. Netiks rādīti arī ar tā noteikumiem noteikti saistītie dati par nakts kolektora izpildes statusu un problēmām.

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Kolonna *Līdzeklis* nodrošina saites uz [izlaišanas plānu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), kur varat redzēt oficiālos izlaišanas datumus katram līdzeklim. Kolonna *Vairāk informācijas* sniedz detalizētu informāciju un/vai saites uz saistīto dokumentāciju.

Vairumam šo līdzekļu ir jābūt iespējotiem, izmantojot [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), pirms varat tos izmantot. Daži no norādītajiem līdzekļiem joprojām ir pieejami priekšskatījumā, kamēr citi, iespējams, jau ir vispārīgi pieejami.

| Līdzekļu apgabals | Funkcija | Papildinformācija |
|---|---|---|
| Krājumi&nbsp;un&nbsp;loģistika | [Globālā krājumu uzskaites pievienojumprogramma Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Globālās krājumu uzskaites sākumlapa](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Rīcībā esošo korekciju grāmatošana, izmantojot kodus, kas saistīti ar korespondējošo kontu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Krājumu inventarizācijas iemeslu kodi](../warehousing/reason-codes-for-counting-journals.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Tādu datu eksportēšanas politika, uz kuriem atsaucas pārdošanas piedāvājums](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Izvēlieties, vai izmaiņas datos, uz kuriem atsaucas piedāvājumi, izraisīs šo piedāvājumu (vai rindu) iekļaušanu nākamajā inkrementālajā eksportā. Inkrementālais eksports notiks ātrāk, ja izvēlaties neiekļaut šādus piedāvājumus vai rindas.<br><br>Šis līdzeklis pievieno iestatījumu ar nosaukumu **Izlaist pārdošanas piedāvājumu atsauces datus izmaiņu izsekošanas laikā** lapā **Debitoru parametri**. |
| Krājumi&nbsp;un&nbsp;loģistika | [Skenēt svītrkodus noliktavā, izmantojot GS1 formāta standartus](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 svītrkodi un QR kodi](../warehousing/gs1-barcodes.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Vieglā rezervācija krājumu redzamības pievienojumprogrammai](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Krājumu redzamības rezervācija](../inventory/inventory-visibility-reservations.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Ieturējumu un pieļaujamā svara uzlabojumi atlaižu pārvaldībai](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Ieturējumu pārvaldība, izmantojot ieturējumu rīku](../rebate-management/deduction-workbench.md )<br><br>[Atlaižu apstrāde, pārskatīšana un grāmatošana](../rebate-management/process-review-post.md)<br><br>[Atlaižu pārvaldības darījumi](../rebate-management/rebate-management-deals.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Norādījumi par noliktavas programmas darbībām](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Darbību nosaukumu un instrukciju pielāgošana Warehouse Management mobilajai programmai](../warehousing/mobile-app-titles-instructions.md) |
| Krājumi&nbsp;un&nbsp;loģistika | [Darba pārtraukumi un izsekošanas atjauninājumi izkraušanas izmaksām](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Atjaunināt izsekošanu izvietošanai](../landed-cost/update-tracking-putaway.md )<br><br>[Tranzīta preču apstrāde](../landed-cost/in-transit-processing.md) |
| Vispārējā plānošana | [Negatīvās dienas optimizācijas plānošanai](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Aizkaves tolerance (negatīvās dienas)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi). Ja vēlaties izmantot kādu no šiem līdzekļiem, tos ir skaidri jāiespējo [Līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Līdzekļu apgabals | Līdzekļa&nbsp;nosaukums&nbsp;līdzekļu&nbsp;pārvaldībā | Papildinformācija |
|---|---|---|
| Izmaksu pārvaldība | Detalizēta informācija par krājuma slēgšanas norisi | Šis priekšskatījuma līdzeklis iespējo detalizētu krājumu slēgšanas progresa pārskatu. |
| Sagāde un avoti | Novērsiet vispārīgu budžeta rezervāciju pārmērīgu patēriņu, ja darbplūsmā ir vairāki pirkšanas pieprasījumi | Šis priekšskatījuma līdzeklis uzlabo kļūdu pārbaudi, kad lietotāji iesniedz un apstiprina pirkšanas pieprasījumus, kas pārsniedz vispārējās budžeta rezervēšanas rindas atlikušo bilanci. Tas palīdz novērst vispārējo budžeta rezervāciju pārtvēršanu, ja vairāki pirkšanas pieprasījumi atrodas darbplūsmā. |
| Ražošanas kontrole | Ražotnes izpildes saskarnē rādīt pilnus sērijas, partijas numurus un unikālos noliktavas vienības identifikatorus | Šis līdzeklis nodrošina uzlabotu pieredzi sarakstu apskatīšanai ar sērijas, partijas un numura zīmes numuriem ražošanas izpildes interfeisā. Rādīšanas izmaiņas no karšu skata ar ierobežotu rakstzīmju skaitu uz saraksta skatu, kas nodrošina pietiekami daudz vietas pilnu vērtību rādīšanai. Šis saraksts arī nodrošina iespēju meklēt noteiktus numurus. |
| Pārdošana un mārketings | Ierobežot grāmatošanai atlasāmo pārdošanas pasūtījumu skaitu | Šī funkcija ļauj definēt maksimālo pārdošanas pasūtījumu skaitu, ko var atlasīt, grāmatojot apstiprinājumus, izdošanas sarakstus, pavadzīmes un rēķinus no pārdošanas pasūtījumu saraksta lapas. Tas tiek aktivizēts automātiski. Šis līdzeklis pievieno iestatījumu ar nosaukumu **Maksimālais pārdošanas pasūtījumu skaits grāmatošanai** **Debitoru parādu parametru** lapā. Jaunais iestatījums pēc noklusējuma ir *100*. Šī funkcija palīdz uzlabot pārdošanas pasūtījumu saraksta lapas veiktspēju, kad ir atlasīts liels skaits pārdošanas pasūtījumu. Tas neietekmē pārdošanas pasūtījumu skaitu, ko var apstrādāt periodisks uzdevums. |
| Noliktavas vadība | Izvietošanas darba atvienošana no IPPN | Šis līdzeklis ir nepieciešams, lai sūtītu un saņemtu iepriekšējus paziņojumus par nosūtīšanu (IPPN), kad palaižat noliktavas vadības darba slodzi mēroga vienībā (kā daļu no sadalītās transportlīdzekļa topoloģijas). Tajā ir pievienota jauna datu bāzes tabula, kas atvēlēta informācijas glabāšanai par izvietošanas darbu. Iepriekš šī informācija tika glabāta tabulās, kas tiek izmantotas arī IPPN. |
| Noliktavas pārvaldība | Slotu jauktās vienības | Ļauj sistēmai slota krājumus vietās, kas ietver jauktas vienības (piemēram, kastes un kārbas). Katrai slotas veidnes rindai šis līdzeklis ļauj izvēlēties, vai rindai vajadzētu sadalīt vienumus jauktas vienības vai vienas vienības vietās. |
| Noliktavas pārvaldība | Izmantojiet ātrāku API konteineru aizvēršanai/atkārtotai atvēršanai iepakošanas stacijā | Kad ir iespējots šis priekšskatījuma līdzeklis, krājumu darbības, kas saistītas ar konteineriem, tiek izveidotas, izmantojot jaunu bezsvara procesu, kas uzlabo konteineru slēgšanas vai atvēršanas veiktspēju manuālas iepakošanas stacijas apstrādes laikā. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Nesen ir pievienotas vai ievērojami atjauninātas tālāk norādītās palīdzības tēmas. Tās ne vienmēr ir saistītas ar jaunajiem līdzekļiem, kas pievienoti šim laidienam, kā uzskaitīts iepriekšējā sadaļā, taču tās var palīdzēt jums pilnīgāk izmantot esošos līdzekļus.

| Līdzekļu apgabals | Jaunas vai atjauninātas tēmas |
|---|---|
| Vispārējā plānošana | [Krājumu prognozes](../master-planning/inventory-forecast.md) |
| Vispārējā plānošana | [Parametri, kas netiek izmantoti plānošanas optimizācijai](../master-planning/planning-optimization/not-used-parameters.md) |
| Vispārējā plānošana | [Papildināšanas metodes un daudzuma modificēšana](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Vispārējā plānošana | [Plānošana ar neierobežotu noslodzi](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Vispārējā plānošana | [Plāna vēstures un plānošanas žurnālu skatīšana](../master-planning/planning-optimization/plan-history-logs.md) |
| Noliktavas pārvaldība | [Konteineru iepakošanas stratēģijas](../warehousing/container-packing-strategy-overview.md) |
| Noliktavas pārvaldība | [Cikla inventarizācijas piemēru scenāriji](../warehousing/cycle-counting-scenarios.md) |
| Noliktavas pārvaldība | [Ienākošo IPPN importēšana, izmantojot V2 datu elementu](../warehousing/import-asn-v2-data-entity.md) |
| Noliktavas pārvaldība | [Pārdošanas pasūtījumu un pārsūtīšanas pasūtījumu pārmērīga izdošana](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Noliktavas pārvaldība | [Kopuma etiķešu drukāšanas plānošana kopuma laikā](../warehousing/configure-task-based-wave-label-printing.md) |
| Noliktavas pārvaldība | [Kas jauns vai mainīts mobilajā programmā Warehouse Management](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.21 ietver platformas atjauninājumus. Lai iegūtu papildinformāciju, skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.21 (2021. gada oktobris)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.21, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 un rūpniecības mākoņi: 2021. gada 2. laidiena plāns

Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Apskatiet [Dynamics 365 un rūpniecības mākoņi: 2021. gada 2. laidiena plāns](/dynamics365-release-plan/2021wave2/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Noņemtie un novecojušie Supply Chain Management līdzekļi

Tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) apraksta līdzekļus, kas ir vai ir ieplānots noņemšanai no Supply Chain Management.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda funkcija tiek noņemta no preces, izslēgšanas paziņojums tiks izziņota tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mēnešu laikā pirms noņemšanas.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
