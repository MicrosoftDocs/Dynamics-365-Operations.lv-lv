---
title: Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.26 (2022. gada maijs)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.26.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: db8799aba8095c8144d878c96590e8d90276726b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428205"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Jaunumi un izmaiņas programmā Dynamics 365 Supply Chain Management 10.0.26 (2022. gada maijs)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti Microsoft Dynamics 365 Supply Chain Management versijā 10.0.26. Šai versijai ir būvējuma numurs 10.0.1192, un tas ir pieejams šeit:

- **Priekšskatījuma laidiens:** 2022. gada marts
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada aprīlis
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada maijs

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo rakstu, lai ietvertu līdzekļus, kas to veidojās pēc šī raksta sākotnējā publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Krājumi un loģistika | [Rīcībā esošo krājumu redzamības vaicājums papildu noliktavas pārvaldības krājumu atbalstam](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [Inventory Visibility atbalsts WMS krājumiem](../inventory/inventory-visibility-whs-support.md) | Līdzekļu pārvaldība:<br>*Iespējot noliktavas preces krājumu redzamības pakalpojumā* |
| Krājumi un loģistika | [Pieejams solīšanai krājumu redzamības pievienojumprogrammai](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Krājumu redzamības rīcībā esošo izmaiņu grafiki un pieejamās solīšanai](../inventory/inventory-visibility-available-to-promise.md) | Aktivizē pakalpojuma konfigurācija |
| Ražošana | [Ražošanas izpildes interfeisa pieļaujamā svara krājumi](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Kā nodarbinātie izmanto ražošanas izpildes interfeisu](../production-control/production-floor-execution-use.md) | Līdzekļu pārvaldība:<br>*Sniegt pārskatu par pieļaujamā svara krājumiem no ražošanas izpildes interfeisa* |
| Ražošana | Cilne Mani darbi ražošanas izpildes interfeisā | [Kā nodarbinātie izmanto ražošanas izpildes interfeisu](../production-control/production-floor-execution-use.md) | Līdzekļu pārvaldība:<br>*Cilne Mani darbi ražošanas izpildes interfeisā* |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt jebkuru no šīm funkcijām, tas jādara līdzekļu [pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Sagāde un avoti | Grāmatot uzkrāto preču reģistrēto daudzumu un atgādinājumus par neuzkrātajām precēm kvīšu un kreditoru rēķinu sagatavošanas nolūkā | Šī iespēja izmaina, kā neiekrātu preču (piemēram, pakalpojumu) daudzumi tiek grāmatoti, apstrādājot kreditora rēķinus un ienākošos sūtījumus pret pirkšanas pasūtījumiem. *Funkcija* modificē opciju Reģistrētais daudzums un Pakalpojumu daudzums uzvedību ieejas plūsmu un kreditoru rēķinu grāmatošanai, izmainot *to*, lai tā atbilstu opcijai Reģistrētais daudzums un Uzkrātais preču funkcionalitāte, kas jau pastāv, grāmatojot pārdošanas pavadzīmju daudzumus.<br><br>Kad grāmatojat *produktu* ieejas plūsmas vai kreditora rēķinu, izmantojot opciju Reģistrētais daudzums un Pakalpojumu daudzums, sistēma grāmato uzkrāto preču reģistrēto daudzumu un grāmato atlikušo uzkrāto preču daudzumu (tostarp gan pakalpojumus, gan pakalpojumus, kas nav pakalpojumi). Bez šīs funkcionalitātes sistēma joprojām grāmato reģistrēto uzkrāto preču daudzumu (tostarp pakalpojumus, kas konfigurēti kā uzkrātie krājumi), bet vienmēr grāmato pilnu pasūtīto neuzkrāto pakalpojumu preču daudzumu (un ignorē neuzkrāto preču daudzumu, kas nav *ar* veidu Pakalpojums). |
| Sagāde un avoti | Sinhronizēt izsekošanas dimensijas starpuzņēmumu pārdošanas un pirkšanas pasūtījumu rindās | Šī funkcija ļauj kontrolēt, vai sērijas un paketes numura izsekošanas dimensijas tiek sinhronizētas starpuzņēmuma pārdošanas un pirkšanas pasūtījuma rindām. Tas pievieno jaunus iestatījumus gan pirkšanas **pasūtījumu politikām** **·**, gan pārdošanas pasūtījumu politikas cilnēm starpuzņēmumu iestatīšanas **lapā** debitoriem un kreditoriem. Tiek atjaunināti arī dažu saistītu, tuvējo iestatījumu nosaukumi iestatīšanai Programma.<br><br>Ja izmantojat noliktavas vadības procesus (WMS), tad ņemiet vērā, ka šī funkcija sinhronizēs partijas un sērijas numurus tikai tad, ja šīs dimensijas mērķa rezervāciju hierarhijā atrodas virs novietojuma. |
| Preču informācijas pārvaldība | Tīrīt preces atribūtu vērtības | Šī funkcija pievieno periodisku uzdevumu ar **nosaukumu Tīrīt preces īpašību vērtības**, kas notīra preces īpašību vērtību ierakstus, kas vairs nav saistīti ar preci, izmantojot preču kategoriju. |
| Krājumu un noliktavas pārvaldība | (Krievija) Novērsiet neatbilstības, izsniedzot GTD pirkšanas pasūtījumiem, kuros ir krājumi ar iespējotu WMS | Šī funkcija ir tikai Krievijas lokalizācijai. Tas novērš neatbilstības, kas rodas, izsniedzot Krievijas muitas deklarācijas numurus (GTD) importa pirkšanas pasūtījumiem, kas ietver krājumus, kas iespējoti noliktavas pārvaldības procesiem (WMS). GTD izsniegšanas process izmaina dažas krājumu dimensijas vērtības saistītajās krājumu darbībās rēķiniem, kas iekļauti pielāgotajā žurnālā, kas rada neatbilstības starp darba ierakstiem pirkšanas pasūtījumam un krājumu darbībām pirkumam. Kad šī funkcija ir iespējota, GTD izsniegšanas process ģenerē korekcijas darbu, kas novērš šādas neatbilstības. |
| Noliktavas vadība | Uzlabots GS1 svītrkodu parsētājs | Šī funkcija pievieno uzlabotu parsētāju GS1 simbola datiem. Jaunais parsētājs ievieš GS1 vispārīgās specifikācijas algoritmu GS1 simbolu parsēšanai un nodrošina stiprāku datu apstiprināšanu. Papildinformāciju skatiet GS1 [svītrkoda skenēšanai](../warehousing/gs1-barcodes.md). |
| Noliktavas vadība | Noliktavas pārvaldības lietojumprogramma — tukšs GTD | Šī funkcija ir tikai Krievijas lokalizācijai. Tas ļauj darbiniekiem, kuri izmanto mobilo programmu Noliktavas pārvaldība, atstāt tukšus Krievijas muitas deklarāciju numurus (GTD), ja nepieciešams. Ja GTD izsekošanas dimensija ir iestatīta atļaut tukšas vērtības, sistēma akceptēs tukšas GTD vērtības rīcībā esošo krājumu sniegtajām krājumu operācijām. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Mēs nesen pievienojam vai būtiski atjauninājām šādus palīdzības rakstus. Šiem rakstiem nav obligāti jābūt saistītiem ar jaunajiem līdzekļiem, kas tika pievienoti šim laidienam, kā norādīts iepriekšējās sadaļās. Tomēr tie var palīdzēt iegūt vairāk no esošajiem līdzekļiem.

| Līdzekļu apgabals | Jauni vai atjaunināti raksti |
|---|---|
| Izmaksu pārvaldība | Atjauninātie piemēri un diagrammas tika pievienotas katram no šiem rakstiem:<ul><li>[FIFO ar fizisko vērtību un iezīmēšanu](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO ar fizisko vērtību un iezīmēšanu](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO uz datums ar fizisko vērtību un iezīmēšanu](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Faktiskā vidējo izmaksu cena](../cost-management/running-average-cost-price.md)</li><li>[Vidējā svērtā ar fizisko vērtību un iezīmēšanu](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.26 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet [Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā 10.0.26 (2022. gada maijā](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md)).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.26, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 un rūpniecības mākoņi: 2022. gada 1. laidiena plāns

Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Apskatiet [Dynamics 365 un rūpniecības mākoņi: 2022. gada 1. laidiena plāns](/dynamics365-release-plan/2022wave1/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Noņemtie un novecojušie Supply Chain Management līdzekļi

Noņemtie [vai novecojušie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) rakstā apraksta funkcijas, kas ir noņemtas vai ieplānotas izņemšanai vai nolietojumam Piegādes ķēžu pārvaldībai.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda līdzekļa noņemšanas no preces paziņojums [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) par nolietojumu tiks papildu pievienots 12. rakstu funkcionalitātes Noņemtie vai novecojušie 12 mēnešu skaits pirms noņemšanas.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

