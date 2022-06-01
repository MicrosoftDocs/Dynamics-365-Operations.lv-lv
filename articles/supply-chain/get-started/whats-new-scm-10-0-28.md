---
title: Dynamics 365 Supply Chain Management 10.0.28. priekšskatījums (2022. gada augusts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Supply Chain Management 10.0.28.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 306ff9be80c7a7a947b9132e3c9b4b9ec799b265
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813168"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10028-august-2022"></a>Dynamics 365 Supply Chain Management 10.0.28. priekšskatījums (2022. gada augusts)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti Microsoft Priekšskatījuma Dynamics 365 Supply Chain Management versijā 10.0.28. Šai versijai ir ražošanas numuru 10.0.1264 un tā ir pieejama šajā grafikā:

- **Priekšskatījuma laidiens:** 2022. gada maijs
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada jūlijs
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2022. gada jūlijs

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo tēmu, lai iekļautu līdzekļus, kas tika pievienoti būvējumam pēc šīs tēmas sākotnējo publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Krājumi un loģistika | [Landed izmaksu integrācijas entītijas trešās puses kravas ekspediktiem](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Pārskats par zemes izmaksu elementiem](../landed-cost/landed-cost-entities-overview.md) | Aktivizēts pēc noklusējuma |
| Plānošana | [Glabāšanas laika optimizācijas atbalsta plānošana](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | Drīzumā <!-- KFM: Vendor is preparing this. Expected May 20. --> | Aktivizēts pēc noklusējuma |

<!-- KFM: Confirm status of this feature:
| Planning | [Demand Driven Material Requirements Planning (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | Coming soon | Feature management:<br>*(Preview) DDMRP for Planning Optimization* | -->

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem papildinājumiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi).

Ja vēlaties ieslēgt vai izslēgt jebkuru no šīm funkcijām, tas ir jādara līdzekļa [pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa nosaukums līdzekļu pārvaldībā | Papildinformācija |
|---|---|---|
| Krājumu un noliktavas pārvaldība | Aktivizēt starpuzņēmumu rīcībā esošos, lai rādītu tikai rīcībā esošo nedrukāto daudzumu | Šī funkcija ļauj izvēlēties, vai krājumi ar rīcībā esošo daudzumu ir jāiekļauj starpuzņēmumu rīcībā esošo sarakstu. Šo opciju **var** kontrolēt, ja starpuzņēmumu rīcībā esošo sarakstu iestatījumos, kuru šis līdzeklis pievieno lapai Krājumu un noliktavas pārvaldības parametri, nerādīt rīcībā esošo krājumu ar nulles **vērtību**. |
| Krājumu un noliktavas pārvaldība | (Indija) Pārsūtīšanas cenu kārtulām ignorēt atrašanās vietu, ja opcijai “No noliktavas koda” ir norādīts iestatījums “Visi” | <p>Šis līdzeklis attiecas tikai uz Indijas lokalizācijām. Tas atvieglo pārsūtīšanas cenu iestatīšanu krājumiem krājumu pārsūtīšanā.</p><p>Pārsūtīšanas cenas var iestatīt, konfigurējot katru krājumu ar pārsūtīšanas cenu noteikšanas nosacījumiem. Viens šīs konfigurācijas darbības veids ir tādas kārtulas rindas ietveršanas, kur lauks **No noliktavas koda** ir iestatīts uz *Visi*. Šis iestatījums norāda, ka rindas definētā pārsūtīšanas cena ir jālieto neatkarīgi no noliktavas, no kuras krājums ir izdots. Kad iespējots šis līdzeklis, pārsūtīšanas cenu kārtulas, **kur lauks No noliktavas** koda ir iestatīts uz *Visi*, ignorēs iestatījumu **Atrašanās** vieta. Tāpēc noteikumi tiks piemēroti neatkarīgi no pārsūtīšanas pasūtījumā norādītās atrašanās vietas. Tas, iespējams, ir tas, kas tiek gaidīts, jo novietojums atrodas noliktavas dimensiju hierarhijā zem noliktavas.</p><p>Bez šīs funkcijas sistēma piemēros šī tipa noteikumus tikai tad, kad atrašanās vieta pārsūtīšanas pasūtījumā precīzi sakrīt ar atrašanās vietu, kas iestatīta noteikumam. (Ja kārtulai iestatīta tukša atrašanās vieta, sistēma piemēros noteikumu tikai pārsūtīšanas pasūtījumiem, kuriem atrašanās vieta ir arī tukša vērtība.)</p> |
| Krājumu un noliktavas pārvaldība | Rīcībā esošo krājumu pārskata datu tīrīšana | Šī funkcija nodrošina veidu, kā iztīrīt datus, kas tiek izmantoti, lai izveidotu rīcībā *esošo krājumu pārskatu glabāšanas* pārskatus. |
| Ražošanas kontrole | Piešķirt projekta darbības pakalpojumu līgumam un pakalpojumu pasūtījumu rindām | Šī iespēja pievieno lauku ar nosaukumu Projekta **aktivitāte** pakalpojumu līgumam un pakalpojuma pasūtījuma rindām, tādējādi jūs variet iestatīt projekta aktivitāti tiem. Šis līdzeklis palīdzēs novērst bloķēšanas kļūdas, kad iegrāmatosiet pakalpojumu pārvaldības projekta žurnālus, kas pieprasa iestatīt projekta aktivitāti.  |
| Noliktavas vadība | Manuālās pārsūtīšanas rindas izdošanas pakalpojums administratoram vai līdzīgiem uzticamiem lietotājiem | Šis līdzeklis ļauj administratoriem manuāli izdot krājumu darbības, kas ir saistītas ar pārsūtīšanas rindām. Šīs rindas ietver rindas, kas jau ir nodotas izpildei noliktavā. Administratoriem šī izdošana jāveic tikai izņēmuma gadījumos, piemēram, ja sistēma ir bojātā stāvoklī. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Mēs nesen esam pievienojis vai būtiski atjaunināuši šādas Palīdzības tēmas. Šīm tēmām nav obligāti jābūt saistītām ar jaunajiem līdzekļiem, kas tika pievienoti šim laidienam, kā norādīts iepriekšējās sadaļās. Tomēr tie var palīdzēt iegūt vairāk no esošajām funkcijām.

| Līdzekļu apgabals | Jaunas vai atjauninātas tēmas |
|---|---|
| Izmaksu pārvaldība | [Fiksēta saņemtā krājuma cena](../cost-management/fixed-receipt-price.md) |
| Izmaksu pārvaldība | [Bieži uzdotie jautājumi par krājumu izmaksu ošanu](../cost-management/inventory-costing-faq.md) |
| Izmaksu pārvaldība | [Grāmatot izmaksu konta uzskaites principu](../cost-management/post-to-charge-account-accounting-principle.md) |
| Krājumu vadība | [Krājumu darbību papildinformācija](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.28 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet [Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā 10.0.28 (2022. gada jūnijs](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md)).<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.28, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

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
