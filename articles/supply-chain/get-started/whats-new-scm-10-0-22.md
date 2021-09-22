---
title: Pakalpojuma Dynamics 365 Supply Chain Management priekšskatījums 10.0.22 (2021. gada novembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.22.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6fc4b9d0a0f5319c8a75e7d687ee82ea81497844
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471864"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10022-november-2021"></a>Pakalpojuma Dynamics 365 Supply Chain Management priekšskatījums 10.0.22 (2021. gada novembris)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā uzskaitīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti Microsoft Dynamics 365 Supply Chain Management versijas 10.0.22 priekšskatījumā. Šai versijai ir būvējuma numurs 10.0.995, un tas ir pieejams šeit:

- **Laidiena priekšskatījums:** 2021. gada septembris
- **Vispārēja laidiena (pašatjaunināšana) pieejamība:** 2021. gada oktobris
- **Vispārēja laidiena (automātiskā atjaunināšana) pieejamība:** 2021. gada novembris

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Kolonna *Līdzeklis* nodrošina saites uz [izlaišanas plānu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), kur varat redzēt oficiālos izlaišanas datumus katram līdzeklim. Kolonna *Vairāk informācijas* sniedz detalizētu informāciju un/vai saites uz saistīto dokumentāciju. Lai noteiktu, kā ieslēgt līdzekli, skatiet kolonnu *Iespējots pēc*. Papildinformāciju par to, ka izmantot līdzekļu pārvaldību skatiet [Pārskats par līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Mēs varētu atjaunināt šo tēmu, lai iekļautu līdzekļus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Līdzekļu apgabals | Funkcija | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Plānošana | [Plānošanas optimizācijas atbalsts resursu sadalījumam, kas pamatots uz iespējām](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Plānošana ar neierobežotu noslodzi](../master-planning/planning-optimization/infinite-capacity-planning.md) | Līdzekļu pārvaldība (*Bezgalīga noslodzes plānošana plānošanas optimizācijai*) |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi). Ja vēlaties izmantot kādu no šiem līdzekļiem, tos ir skaidri jāiespējo [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Līdzekļu apgabals | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Izmaksu pārvaldība | Izveidot saistītos dokumentus standarta izmaksu noapaļošanas pārvērtēšanai | <p>Kad tiek veikta krājumu finansiālā grāmatošana (piemēram, pārdošanas pasūtījuma rēķins vai krājumu darbība), šī funkcija liek sistēmai izveidot atsevišķu dokumentu jebkurām saistītām standarta izmaksu noapaļošanas pārvērtēšanām un pievienot to finanšu grāmatošanas dokumentam kā saistīto dokumentu.</p><p>Bez šīs funkcijas sistēma reģistrē standarta izmaksu noapaļošanas pārvērtēšanu vienā un tajā pašā dokumenta grāmatošanā. Šī darbība reizēm var radīt konfliktējošu datuma informāciju, jo pārvērtēšana izmanto sesijas vai sistēmas datumu, bet finanšu grāmatojumi izmanto grāmatošanas datumu.</p> |
| Dalītā hibrīda topoloģija | *(Līdzekļu pārvaldība nav nepieciešama.)* | <p>Šis laidiens paplašina noliktavas pārvaldības darba noslodzes izejošās noslodzes plānošanas iespējas mākoņa un malas apjoma vienībām.</p><p>Plašāku informāciju skatiet rakstā [Mākoņa un malas mēroga vienības ražošanas izpilde](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Tehnisko izmaiņu pārvaldība | Tehnisko preču variantu ģenerēšana | <p>Šī funkcija ļauj ģenerēt vairākus variantus tehniskais precei, balstoties uz tās krāsu, izmēru, stilu vai konfigurācijas dimensijām.</p><p>Papildinformāciju skatiet [Tehnisko preču variantu ģenerēšana](../engineering-change-management/engineering-variants.md).</p> |
| Krājumu un noliktavas pārvaldība | Krājumu redzamības integrācija ar rezervācijas nobīdi | <p>Šo funkciju var aktivizēt tikai pēc tam, kad ir aktivizēta funkcija *Krājumu redzamības integrācija*. Tā nodrošina funkcionalitāti, lai kompensētu rezervācijas, kas veiktas krājumu redzamībai.</p><p>Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](../inventory/inventory-visibility-reservations.md).</p> |
| Pārdošana un mārketings | Ierobežot grāmatošanai atlasāmo pārdošanas pasūtījumu skaitu | <p>Šis līdzeklis ir iespējots automātiski. Tas pievieno lauku **Maksimālais pārdošanas pasūtījumu skaits grāmatošanai** **Debitoru parādu parametru** lapā. Šis lauks ļauj definēt maksimālo pārdošanas pasūtījumu skaitu, ko var atlasīt, grāmatojot apstiprinājumus, izdošanas sarakstus, pavadzīmes un rēķinus no pārdošanas pasūtījuma saraksta lapas. Noklusējuma vērtība ir *100*.</p><p>Šis līdzeklis palīdz uzlabot pārdošanas pasūtījumu saraksta lapas veiktspēju, kad ir atlasīts liels skaits pārdošanas pasūtījumu. Tas neietekmē pārdošanas pasūtījumu skaitu, ko var apstrādāt periodisks uzdevums.</p> |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Nesen ir pievienotas vai ievērojami atjauninātas tālāk norādītās palīdzības tēmas. Šīm tēmām nav obligāti jābūt saistītām ar jaunajiem līdzekļiem, kas tika pievienoti šim laidienam, kā norādīts iepriekšējā sadaļā. Tomēr tie var palīdzēt iegūt vairāk no esošajiem līdzekļiem.

| Līdzekļu apgabals | Jaunas vai atjauninātas tēmas |
|---|---|
| Tehnisko izmaiņu pārvaldība | [Inženierzinātnes izmaiņu pārvaldības pārskats](../engineering-change-management/product-engineering-overview.md) tagad uzskaita visus saistītos, neobligātos līdzekļus, kas pieejami līdzekļu pārvaldībā |
| Vispārējā plānošana | [Pieprasījuma prognozēšanas iestatīšana](../master-planning/demand-forecasting-setup.md) |
| Vispārējā plānošana | [Neto prasības un piesaistes informācija darbā ar plānošanas optimizāciju](../master-planning/planning-optimization/net-requirements.md) |
| Noliktavas vadība | [Izlaist uz noliktavu](../warehousing/release-to-warehouse-process.md) sniedz detalizētu pārskatu par pilnīgu nodošanu noliktavā |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.22 ietver platformas atjauninājumus. Lai iegūtu papildinformāciju, skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.22 (2021. gada novembris)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md). <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.22, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

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
