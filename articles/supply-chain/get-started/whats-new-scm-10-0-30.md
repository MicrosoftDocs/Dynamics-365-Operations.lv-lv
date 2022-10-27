---
title: Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.30. (2022. gada novembris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.30.
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2983c113487934fd0751efcef9129e1f28d8dce8
ms.sourcegitcommit: 86c0562ce1ecdf7937125c0f5a6771f178b459e7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714803"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10030-november-2022"></a>Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.30. (2022. gada novembris)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti Microsoft Dynamics 365 Supply Chain Management versijā 10.0.30. Šai versijai ir ražošanas numuru 10.0.1362 un tā ir pieejama šajā grafikā:

- **Laidiena priekšskatījums:** 2022. gada septembris
- **Vispārēja laidiena (pašatjaunināšana) pieejamība:** 2022. gada oktobris
- **Vispārēja laidiena (automātiskā atjaunināšana) pieejamība:** 2022. gada novembris

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo rakstu, lai ietvertu līdzekļus, kas tika pievienoti būvējumam pēc šī raksta sākotnējās publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Ražošana | [Pārraudzīt aprīkojumu ar Sensora datu informāciju](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Sensor Data Intelligence sākumlapa](../sensor-data-intelligence/sdi-home-page.md) | Līdzekļu pārvaldība:<br>*(Priekšskatījums) Sensora datu informācija* |
| Noliktavas vadība | [Noliktavas pārvaldības mobilās programmas vairāklīmeņu darbības](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/multi-level-detours-warehouse-management-mobile-app) | [Konfigurēt novirzīšanas darbības mobilo ierīču izvēlnes vienumos](../warehousing/warehouse-app-detours.md) | Līdzekļu pārvaldība:<br>*Vairāku līmeņu apiešana mobilajai programmai Warehouse Management* |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt jebkuru no šīm funkcijām, tas ir jādara līdzekļa [pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Ražošanas kontrole | Rīcībā esošā informācija ražošanas pasūtījumos, lai izlaistu lapu | Pievieno kolonnu rīcībā esošo krājumu daudzumam rindas **krājumos rindu sadaļā ražošanas pasūtījumi, lai izlaistu** lapu. |
| Transportēšanas pārvaldība | Piešķirt kravas saistītajiem maršruta segmentiem | Šī funkcija ļauj sistēmai precīzāk sadalīt sūtījuma kravas pārvadāšanas izmaksas, tostarp kravām ar vairākiem sūtījumiem, kas tiek piegādāti dažādiem segmentiem vienā maršrutā. Tas piešķir katru sūtījumu vispiemērotākajiem maršruta segmentiem, pamatojoties uz kravas un segmenta mērķa adresēm. Pēc tam funkcija aprēķina katra sūtījuma kravas pārvadāšanas izmaksas kā kravas kopējās kravas izmaksu proporciju, pamatojoties uz sūtījuma relatīvo svaru, apjomu, daudzumu un nobraukto attālumu. Šis līdzeklis attiecas tikai uz kravām, kas pārvaldītas, izmantojot transportēšanas pārvaldības (TMS) moduli. |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.30 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet [Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā 10.0.30 (2022. gada novembrī](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md)).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas ietverti katrā atjauninājumā, kas ir daļa no versijas 10.0.30, piesakieties lifecycle Services (LCS) [un skatiet zināšanu bāzes rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

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
