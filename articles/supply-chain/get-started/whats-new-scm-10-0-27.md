---
title: Pakalpojuma Dynamics 365 Supply Chain Management 10.0.27. priekšskatījums (2022. gada jūlijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.27.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 77c79c88b08844bf7e399a762bb9eb9746ffb71a
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2022
ms.locfileid: "8812949"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10027-july-2022"></a>Pakalpojuma Dynamics 365 Supply Chain Management 10.0.27. priekšskatījums (2022. gada jūlijs)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti Microsoft priekšskatījuma Dynamics 365 Supply Chain Management versijā 10.0.27. Šai versijai ir ražošanas numuru 10.0.1227 un tā ir pieejama šajā grafikā:

- **Laidiena priekšskatījums:** 2022. gada aprīlis
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada jūnijs
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada jūlijs

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo tēmu, lai iekļautu līdzekļus, kas tika pievienoti būvējumam pēc šīs tēmas sākotnējo publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Krājumi un loģistika | [Krājumu sadalījuma krājumu redzamības pievienojumprogramma](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [Krājumu redzamības krājumu sadalījums](../inventory/inventory-visibility-allocation.md) | Aktivizēts pēc noklusējuma |
| Ražošana | Skats “Mana diena” ražošanas izpildes interfeisam | [Kā darbinieki ražošanas izpildes interfeisā un rādīt](../production-control/production-floor-execution-use.md)[atvaļinājuma bilances ražošanas izpildes interfeisā](../production-control/production-floor-execution-payroll-stats.md) | Līdzekļu pārvaldība:<br>*Skats “Mana diena” ražošanas izpildes interfeisam* |
| Plānošana | [Plānošanas optimizācijas atbalsts apakšlīgumu slēgšanai](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Ražošanas apakšuzņēmēja darba pārvaldība](../production-control/manage-subcontract-work-production.md) | Aktivizēts pēc noklusējuma |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt jebkuru no šīm funkcijām, tas ir jādara līdzekļa [pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Vispārējā plānošana | Veidojot plānoto pārsūtīšanas pasūtījumu, ņemiet vērā krājumu izpildes laiku | Kad plānotais pārsūtīšanas pasūtījums ir izveidots, šī iespēja liek sistēmai ņemt vērā krājumu izpildes laiku, kas ir norādīts krājuma noklusējuma pasūtījuma iestatījumos, kad tas aprēķina plānotā *pārsūtīšanas* *pasūtījuma saņemšanas datumu piegādes datuma kontroles iestatījumam kā izpildes laiku nav vai pārdošanas* tips. Ja ir norādīts pārsūtīšanas izpildes laiks, tā vērtība tiks izmantota saņemšanas datuma aprēķināšanai, un transportēšanas dienas netiks ņemtas vērā. |
| Sagāde un avoti | Noklusējuma starpnieka līguma nodokļu informācija kreditoru rēķinu rindās | Šī funkcija ievieš loģiku, lai iestatītu noklusējuma vērtības PVN **un krājuma** **PVN laukiem starpnieka** līguma kreditora rēķina rindās. Šī loģika tiek lietota tikai tad, ja maksas veids starpnieka līguma rindā ir Virsgrāmata/Virsgrāmata. Krājumu PVN grupa izmantos noklusējuma vērtību vai nu no starpnieku sagādes kategorijas (ja tā iestatīta), vai no maksas veida. PVN grupa izmantos noklusēto vērtību no kreditora konta. |
| Sagāde un avoti | Ierobežot pirkšanas pasūtījuma rindu skaitu vienam pakešuzdevumam | Šī funkcija palīdz optimizēt sistēmas veiktspēju, grāmatojot apstiprinājumus un produktu ieejas plūsmas. Tas pievieno jaunu iestatījumu, kura nosaukums ir **Rindas katram** **uzdevumam,** sagādes **un plānošanas parametru lapas cilnei** Piegāde. Šis jaunais iestatījums ļauj ierobežot pirkšanas pasūtījuma rindu skaitu, ko katra pakešuzdevuma apstrādā. Tāpēc tas var palīdzēt izvairīties no liela pakešuzdevumu darba palēninot sistēmu. |
| Preču informācijas pārvaldība | Aizpildīt preces īpašību vērtības | Šī funkcija pievieno periodisku uzdevumu ar nosaukumu Aizpildīt *preces īpašību vērtības*. Šis jaunais periodiskais uzdevums izveido trūkst preču īpašību vērtību ierakstus atribūtiem, kas ir saistīti ar precēm, izmantojot preču kategoriju. |
| Ražošanas kontrole | Papildu konfigurācija ražošanas izpildes interfeisā | <p>Šī funkcija pievieno šādas opcijas lapai **Konfigurēt ražošanas izpildes** izpildi:</p><ul><li>**Automātiski atvērts sākšanas dialoglodziņš meklēšanas pabeigšanas laikā** – kad šī opcija ir aktivizēta, automātiski tiek atvērts darba sākšanas dialoglodziņš, **kad** darbinieki lieto meklēšanas joslu, lai atrastu darbu.</li><li>**Automātiski atvērt pārskata norises dialogu meklēšanas pabeigšanas laikā** — kad šī opcija ir iespējota, **darba** pārskata norises dialoglodziņš tiek automātiski atvērts, kad darbinieki izmanto meklēšanas joslu darba atrašanai.</li><li>**Noklusējuma atlikušais daudzums pārskata norises dialogā** – ja šī opcija ir aktivizēta, **pārskata** progresa dialoglodziņš parāda atlikušo daudzumu pārskatam par ražošanas darbu.</li></ul><p>Papildinformāciju skatiet sadaļā [Ražošanas izpildes interfeisa konfigurēšana](../production-control/production-floor-execution-configure.md).</p> |
| Ražošanas kontrole | Ražošanas grupas ražošanas izpildes interfeisā | <p>Ja vienam ražošanas darbam ir piešķirti vairāki darbinieki, viņi tagad var nominēt vienu darbinieku kā atbildīgo. Pārējie darbinieki automātiski kļūst par šī vadītāja asistentiem. Iegūtajai komandai tikai vadītājs reģistrē darba statusu, bet laika ieraksti attiecas uz visiem grupas dalībniekiem. Šī funkcija atbalsta arī scenāriju, kas tiek saukts par *palīdzības resursu*. Šajā scenārijā darbinieks var reģistrēties kā cita darbinieka asistents, kurš kļūs par jaunizveidotās grupas atbildīgo.</p><p>Papildinformāciju skatiet sadaļā Kā [darbinieki izmanto ražošanas izpildes interfeisu](../production-control/production-floor-execution-use.md).</p> |
| Ražošanas kontrole | Plānošanas krājumu pārskats ražošanas izpildes interfeisā | Šī funkcija vienkāršo partijas pasūtījumu pārskatu veidošanas procesu ražošanas izpildes interfeisa plānošanas krājumiem. Kad partijas pasūtījums *ir* izveidots precei, kuras ražošanas tips ir Plānošanas krājums, ziņošanu par pabeigšanu var veikt tikai šī partijas pasūtījuma līdzproduktiem un blakusproduktiem. Parasti ražošanas krājumu partijas pasūtījumus izmanto, lai atbalstītu izjakšanas procesus, kur izejmateriāls ir izjaukts vairākās atšķirīgas precēs. Kad darbinieks ziņo par partijas pasūtījumu plānošanas krājumam kā pabeigtu, **dialoglodziņā** Ziņot par progresu tiks parādītas tikai līdzprodukti un blakusprodukti. Iepriekš tas arī rāda plānošanas krājumu, un šī uzvedība varētu konutrādiet darbiniekus. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Mēs nesen esam pievienojis vai būtiski atjaunināuši šādas Palīdzības tēmas. Šīm tēmām nav obligāti jābūt saistītām ar jaunajiem līdzekļiem, kas tika pievienoti šim laidienam, kā norādīts iepriekšējās sadaļās. Tomēr tie var palīdzēt iegūt vairāk no esošajām funkcijām.

| Līdzekļu apgabals | Jaunas vai atjauninātas tēmas |
|---|---|
| Izmaksu pārvaldība | [Svērtais vidējais datums ar iekļaut fizisko vērtību un iezīmēšanu](../cost-management/weighted-average-date.md) |
| Dalītā hibrīda topoloģija | [Izmēģināt mēroga vienības sadalītajā hibrīdajā topoloģijā](../cloud-edge/cloud-edge-try-out.md) |
| Duālais ieraksts | [Sinhronizēt ar Supply Chain Management cenu noteikšanas programmu pēc pieprasījuma](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Noliktavas vadība | [Izlaist uz noliktavu](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.27 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet [Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā 10.0.27 (2022. gada jūnijs](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md)).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.27, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

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
