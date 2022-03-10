---
title: Dynamics 365 Supply Chain Management 10.0.26. priekšskatījums (2022. gada maijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.26.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: fae25eb1cb9dd4059b9d49e47cbb0060e717c9bc
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2022
ms.locfileid: "8386919"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10026-may-2022"></a>Dynamics 365 Supply Chain Management 10.0.26. priekšskatījums (2022. gada maijs)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti Microsoft Dynamics 365 Supply Chain Management preview versijā 10.0.26. Šai versijai ir būvējuma numurs 10.0.1192, un tas ir pieejams šeit:

- **Priekšskatījuma laidiens:** 2022. gada marts
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada aprīlis
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada maijs

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo tēmu, lai iekļautu līdzekļus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Krājumi un loģistika | [Rīcībā esošo krājumu redzamības vaicājums, lai atbalstītu papildu noliktavas pārvaldības krājumus](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | Drīzumā | Līdzekļu pārvaldība:<br>*Iespējot noliktavas preces krājumu redzamības pakalpojumā* |
| Krājumi un loģistika | [Pieejams solījumam krājumu redzamības pievienojumprogrammai](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | Drīzumā | Iespējots ar pakalpojumu konfigurāciju |
| Ražošana | [Pieļaujamā svara krājumi ražošanas grīdas izpildes interfeisam](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Kā nodarbinātie izmanto ražošanas izpildes interfeisu](../production-control/production-floor-execution-use.md) | Līdzekļu pārvaldība:<br>*(Priekšskatījums) Pieļaujamā svara krājumu pārskats no ražošanas izpildes interfeisa* |
| Ražošana | Cilne Mani darbi ražošanas izpildes interfeisā <!-- KFM: Add link to release plan when available --> | [Kā nodarbinātie izmanto ražošanas izpildes interfeisu](../production-control/production-floor-execution-use.md) | Līdzekļu pārvaldība:<br>*Cilne Mani darbi ražošanas izpildes interfeisā* |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt kādu no šiem līdzekļiem, tas jādara [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Sagāde un avoti | Grāmatot uzkrāto preču reģistrēto daudzumu un atgādinājumus par neuzkrātajām precēm kvīšu un kreditoru rēķinu sagatavošanas nolūkā | Šis līdzeklis maina to, kā, apstrādājot kreditoru rēķinus un ienākošās nosūtīšanas pavadzīmes pirkšanas pasūtījumos, tiek grāmatoti neuzglabāto preču (piemēram, pakalpojumu) daudzumi. Šis līdzeklis maina ieejas plūsmu un kreditoru rēķinu grāmatošanas opcijas Reģistrēto daudzumu un pakalpojumu *daudzumu opcijas darbību*, mainot to, lai tā atbilstu opcijas Reģistrētais daudzums un neiekļauto preču *darbībai*, kas jau tiek nodrošināta, grāmatojot daudzumus pārdošanas pavadzīmēm.<br><br>Grāmatojot produktu ieejas plūsmu vai piegādātāja rēķinu, izmantojot opciju *Reģistrētais daudzums un pakalpojumu* daudzums, sistēma grāmato reģistrēto uzglabāto preču daudzumu un grāmato atlikušo neuzkrāto preču daudzumu (ieskaitot gan pakalpojumus, gan pakalpojumus). Bez šīs funkcijas sistēma joprojām grāmato reģistrēto uzglabāto produktu daudzumu (ieskaitot pakalpojumus, kas konfigurēti kā uzkrātās preces), bet vienmēr grāmato pilnu pasūtīto nekrāto pakalpojumu produktu daudzumu (un ignorē neuzkrātus produktus, kuru tips *nav Pakalpojums*). |
| Sagāde un avoti | Sinhronizēt izsekošanas dimensijas starpuzņēmumu pārdošanas un pirkšanas pasūtījumu rindās | Šis līdzeklis ļauj kontrolēt, vai sērijas un partijas numuru izsekošanas dimensijas tiek sinhronizētas starpuzņēmumu pārdošanas un pirkšanas pasūtījuma rindās. Tas pievieno jaunus iestatījumus gan pirkšanas pasūtījumu politikām **, gan** **pārdošanas pasūtījumu politiku** cilnēm **starpuzņēmumu** iestatījumu lapā klientiem un kreditoriem. Skaidrības labad tas arī atjaunina dažu saistītu, tuvumā esošu iestatījumu nosaukumus.<br><br>Ja izmantojat papildu noliktavas pārvaldību (WMS), ņemiet vērā, ka šis līdzeklis sinhronizēs partijas un sērijas numurus tikai tad, ja šīs dimensijas ir virs atrašanās vietas mērķa mērķa rezervēšanas hierarhijā. |
| Preču informācijas pārvaldība | Tīrīt preces atribūtu vērtības | Šis līdzeklis pievieno periodisku uzdevumu ar nosaukumu **Tīrīt preces atribūtu vērtības**, kas attīra produkta atribūta vērtību ierakstus, kuri vairs nav saistīti ne ar vienu produktu, izmantojot produktu kategoriju. |
| Krājumu un noliktavas pārvaldība | (Krievija) Novērsiet neatbilstības, izsniedzot GTD pirkšanas pasūtījumiem, kuros ir krājumi ar iespējotu WMS | Šī funkcija ir paredzēta tikai Krievu lokalizācijai. Tas novērš neatbilstības, kas rodas, izsniedzot Krievijas muitas deklarāciju numurus (GTD) importa iepirkuma pasūtījumiem, kas ietver preces, kas iespējotas papildu uzglabāšanai (WMS). GTD izdošanas process maina dažas krājumu dimensiju vērtības saistītajās krājumu darbībās rēķiniem, kas iekļauti pielāgotajā žurnālā, kas rada neatbilstības starp pirkšanas pasūtījuma darba ierakstiem un pirkšanas krājumu darbībām. Kad šis līdzeklis ir iespējots, GTD izdošanas process ģenerē korekcijas darbu, kas novērš šādas neatbilstības. |
| Noliktavas vadība | Uzlabots GS1 svītrkodu parsētājs | Šis līdzeklis pievieno uzlabotu parsētāju GS1 simbolu datiem. Jaunais parsētājs ievieš GS1 vispārīgās specifikācijas algoritmu GS1 simbolu parsēšanai un nodrošina spēcīgāku datu validāciju. |
| Noliktavas vadība | Jaunas slodzes plānošanas darbagalda lapas | Pievieno divas jaunas slodzes plānošanas darbagalda lapas: **Ienākošās slodzes plānošanas darbagalds** un **Izejošās slodzes plānošanas darbagalds**. |
| Noliktavas vadība | Noliktavas pārvaldības lietojumprogramma — tukšs GTD | Šī funkcija ir paredzēta tikai Krievu lokalizācijai. Tas ļauj darbiniekiem, kas izmanto mobilo lietotni Noliktavas pārvaldība, vajadzības gadījumā atstāt Krievijas muitas deklarāciju numurus (GTD) tukšus. Ja GTD izsekošanas dimensija ir iestatīta tā, lai atļautu tukšas vērtības, sistēma pieņem tukšas GTD vērtības krājumu operācijām, kurām ir pieejami rīcībā esošie krājumi. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Nesen ir pievienotas vai ievērojami atjauninātas tālāk norādītās palīdzības tēmas. Šīs tēmas ne vienmēr ir saistītas ar jaunajiem līdzekļiem, kas tika pievienoti šim laidienam, kā norādīts iepriekšējās sadaļās. Tomēr tie var palīdzēt iegūt vairāk no esošajiem līdzekļiem.

| Līdzekļu apgabals | Jaunas vai atjauninātas tēmas |
|---|---|
| Izmaksu pārvaldība | Atjauninātie piemēri un diagrammas tika pievienotas katrai no šīm tēmām:<ul><li>[FIFO ar fizisko vērtību un iezīmēšanu](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO ar fizisko vērtību un iezīmēšanu](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO uz datums ar fizisko vērtību un iezīmēšanu](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Faktiskā vidējo izmaksu cena](../cost-management/running-average-cost-price.md)</li><li>[Vidējā svērtā ar fizisko vērtību un iezīmēšanu](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |
| Sagāde un avoti | [Pirkšanas pasūtījuma rindas datu neatbilstības](../troubleshooting/procurement/purchase-order-line-data-issues.md) |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.26 ietver platformas atjauninājumus. Papildinformāciju skatiet rakstā [Programmu Finance and Operations versijas 10.0.26 platformas atjauninājumi (2022. gada maijs)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.26, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

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
