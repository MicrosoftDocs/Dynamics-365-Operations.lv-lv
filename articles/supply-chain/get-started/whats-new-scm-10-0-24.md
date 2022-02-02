---
title: Jaunumi vai izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.24. (2022. gada februāris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.24.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d7dd3bbb0d1aa701757ad7fa525aba04fe9419c9
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986307"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Jaunumi vai izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.24. (2022. gada februāris)

[!include [banner](../includes/banner.md)]

Šī tēma uzskaita līdzekļus, kas ir vai nu jauni, vai kas ir mainīti programmas Microsoft Dynamics 365 Supply Chain Management versijā 10.0.24. Šai versijai ir būvējuma numurs 10.0.1084, un tas ir pieejams šeit:

- **Izlaides priekšskatījums:** 2021. gada decembris
- **Vispārēja laidiena (paša veikts atjauninājums) pieejamība:** 2022. gada janvāris
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada februāris

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo tēmu, lai iekļautu līdzekļus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Līdzekļu apgabals | Funkcija | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Dalītā hibrīda topoloģija | [Uzlabota noliktavas izpildes darba noslodze mēroga vienībās](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Noliktavas pārvaldības darba slodzes mākoņa un malas mēroga vienībām](../cloud-edge/cloud-edge-workload-warehousing.md) | Aktivizēts pēc noklusējuma. |
| Plānošana | [Plānošanas optimizācijas atbalsts atkārtota pasūtījuma uzcenojums un izejas plūsmas rezerve](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Drošības rezerves](../master-planning/planning-optimization/safety-margins.md) | Aktivizēts pēc noklusējuma. |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt jebkuru no šīm funkcijām, tas jādara līdzekļu [pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Ražošanas kontrole | Ražošanas pasūtījumu materiālu pieejamības pārbaude pēc pieprasījuma | Ar šo funkciju tiek ātrāk atvērta lapa Ražošanas pasūtījumi, kas ir **pieejama** ražošanas pārvaldības **darbvietā**. Bez šīs funkcijas sistēma automātiski pārbauda, vai materiāli ir pieejami visiem norādītajiem ražošanas pasūtījumiem, tiklīdz atverat lapu, kas var aizņemt nozīmīgu laiku, ja ir liels pasūtījumu skaits. Kad šī funkcija ir iespējota, sistēma tā vietā nodrošina rīkjoslas pogu, kuru varat izmantot, lai sāktu materiālu pārbaudi tikai atlasītajiem pasūtījumiem un, kad nepieciešams. |
| Ražošanas kontrole | (Priekšskatījums) Materiālu patēriņa reģistrācija ražotnes izpildes saskarnē (bez WMS) | Šī funkcija ļauj darbiniekiem izmantot ražošanas izpildes interfeisu, lai reģistrētu materiālu patēriņu, partijas numurus un sērijas numurus. Šī funkcija atbalsta tikai tos krājumus, kas nav iespējoti papildu noliktavas procesu (WMS) izmantošanai. Atbalsts WMS iespējotiem krājumiem ir ieplānots turpmākajos laidienos.<p>Dažiem ražotājiem, it īpaši tiem, kas ietilpst procesa nozarēs, ir skaidri jāreģistrē par katru partiju vai ražošanas pasūtījumu patērēto materiālu daudzums. Piemēram, darbinieki var izmantot skalu, lai, sverot patērēto materiālu daudzumu, kad tie strādā. Lai nodrošinātu pilnīgu materiālu izsekošanu, šīm organizācijām jāreģistrē arī tie partijas numuri, kas patērēti, ražojot katru preci. |
| Ražošanas kontrole | Ziņot kā par pabeigtu noliktavas pārvaldības darba slodzē mākoņa un malas mēroga vienībai | Izmantojot šo līdzekli, darbinieki izmanto mobilo programmu Noliktavas pārvaldība, lai ziņotu par ražošanas vai partijas pasūtījuma pabeigšanu, ja programma darbojas attiecībā pret noliktavas pārvaldības darba slodzi mākonī vai malas mēroga vienībā. Papildinformāciju skatiet [sadaļā "Ziņot, kā pabeigts" un "putaway" uz svaru](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF) vienības. |
| Ražošanas kontrole | Sākt noliktavas pārvaldības darba noslodzi noliktavas pārvaldības darba noslodzei, kas ir paredzēts mākoņa un malas mēroga vienībai | Izmantojot šo līdzekli, darbinieki var izmantot mobilo programmu Noliktavas pārvaldība, lai sāktu ražošanas vai partijas pasūtījumu, ja programma darbojas attiecībā pret noliktavas pārvaldības darba slodzi mākonī vai malas mēroga vienībā. |
| Noliktavas vadība | Jaunas noslodzes plānošanas darba lapas | Iespējo divas jaunas noslodzes plānošanas darba lapas: ienākošās noslodzes plānošanas līdzeklis **un** **izejošās noslodzes plānošanas** līdzeklis. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Nesen ir pievienotas vai ievērojami atjauninātas tālāk norādītās palīdzības tēmas. Šīm tēmām nav obligāti jābūt saistītām ar jaunajiem līdzekļiem, kas tika pievienoti šim laidienam, kā norādīts iepriekšējā sadaļā. Tomēr tie var palīdzēt iegūt vairāk no esošajiem līdzekļiem.

| Līdzekļu apgabals | Jaunas vai atjauninātas tēmas |
|---|---|
| Izmaksu pārvaldība | [Krājumu vērtības pārskati](../cost-management/inventory-value-report-storage.md) |
| Izmaksu pārvaldība | [Krājumu vērtības pārskatu piemēri un loģika](../cost-management/inventory-value-report-examples.md) |
| Vispārējā plānošana | [Datuma un laika parametri, kas tiek izmantoti plānošanas optimizācijai](../master-planning/planning-optimization/date-time-used.md) |
| Vispārējā plānošana | [Pieprasījuma prognozēšanas iestatīšana](../master-planning/demand-forecasting-setup.md) |
| Vispārējā plānošana | [Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo krājumu segumu](../master-planning/safety-stock-journal.md) |
| Ražošanas kontrole | [Ražošanas izpildes interfeisa pielāgošana](../production-control/production-floor-execution-customize.md) |
| Ražošanas kontrole | [Ražošanas izpildes interfeisa stils](../production-control/production-floor-execution-styles.md) |
| Pārdošana un mārketings | [Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumi](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Noliktavas vadība | [Mobilās ierīces lietotāju konti](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.24 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā [10.0.24 (2021. gada](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md) novembrī).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.24, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

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
