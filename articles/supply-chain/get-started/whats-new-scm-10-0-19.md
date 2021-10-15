---
title: Jaunumi un izmaiņas programmas Dynamics 365 Supply Chain Management versijā 10.0.19 (2021. gada jūnijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Supply Chain Management 10.0.19.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7c8994a11c9d1d90fd8b66b17900248f941e307b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579788"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Jaunumi un izmaiņas programmas Dynamics 365 Supply Chain Management versijā 10.0.19 (2021. gada jūnijs)

[!include [banner](../includes/banner.md)]

Šī tēma uzskaita līdzekļus, kas ir vai nu jauni, vai kas ir mainīti programmas Microsoft Dynamics 365 Supply Chain Management versijā 10.0.19. Šai versijai ir būvējuma numurs 10.0.837, un tas ir pieejams šeit:

- **Laidiena priekšskatījums:** 2021. gada aprīlis
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2021. gada jūnijs
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2021. gada jūnijs

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Kolonna *Līdzeklis* nodrošina saites uz [izlaišanas plānu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), kur varat redzēt oficiālos izlaišanas datumus katram līdzeklim. Kolonna *Vairāk informācijas* sniedz detalizētu informāciju un/vai saites uz saistīto dokumentāciju.

Vairumam šo līdzekļu ir jābūt iespējotiem, izmantojot [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), pirms varat tos izmantot.

| Līdzekļu apgabals | Funkcija | Papildinformācija |
|---|---|---|
| Krājumi&nbsp;un&nbsp;loģistika | [Apstiprināt un saglabāt kreditora iesniegto bankas informāciju](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Kreditora bankas konta informācijas uzturēšana](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Krājumi un loģistika | [Kontaktpersonas datu entītijas eksporta optimizācija](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Iespējojot šo līdzekli, izmaiņas atsauces datos neļaus saistītās kontaktpersonas iekļaut nākamajā inkrementālā eksportā. Atspējojot šo līdzekli, izmaiņas atsauces datos ļaus saistītās kontaktpersonas iekļaut nākamajā inkrementālā eksportā. |
| Krājumi un loģistika | [Inkrementāli uzlabojumi noliktavas izpildes iespējām ar apjoma vienībām](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Ziņojumu apstrādātāja ziņojumi](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Noliktavas krājumu korekcija](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Noliktavas pārvaldības darba slodzes mākoņa un malas mēroga vienībām](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Krājumi un loģistika | [Uzmeklēšanas funkcionalitāte dokumenta ievada un dokumenta noslēgšanas laukiem pārdošanas piedāvājuma lapā](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Šis līdzeklis pievieno uzmeklēšanas funkcionalitāti **Dokumenta ievada** un **Dokumenta noslēgšanas** laukiem **Pārdošanas piedāvājuma** lapā.<br><br>Šis līdzeklis ir iespējots pēc noklusējuma. |
| Krājumi un loģistika | [Noliktavas izpilde ar pielāgotas aparatūras malas skalas vienībām](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Izvietot malas skalas vienības pielāgotajā aparatūrā, izmantojot LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Ražošana | [Ražošanas izpilde ar pielāgotas aparatūras malas skalas vienībām](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Izvietot malas skalas vienības pielāgotajā aparatūrā, izmantojot LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Plānošana | Plānoto pasūtījumu apstiprināšana, pamatojoties uz vaicājumu | [Plānoto pasūtījumu apstiprināšana](../master-planning/planning-optimization/planned-order-firming.md) |
| Preču informācijas pārvaldība | [Variantu ieteikumu lapas uzlabojumi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Iepriekš definētu preces variantu izveide](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi). Ja vēlaties izmantot kādu no šiem līdzekļiem, tos ir skaidri jāiespējo [Līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Līdzekļu apgabals | Līdzekļa&nbsp;nosaukums&nbsp;līdzekļu&nbsp;pārvaldībā | Papildinformācija |
|---|---|---|
| Pārdošana un mārketings | Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumi | Pārdošanas vēstures tīrīšana var aizņemt ilgu laiku, ja retos gadījumos tiek palaista vidēs ar augstu pārdošanas atjauninājumu daudzumu. Lai samazinātu ilgumu un uzlabotu uzticamību, šis līdzeklis sadala tīrīšanu partijās, kas tiek palaistas uz ierobežotu laiku. Ja iespējams, datu bāzes iespējas tiks līdzsvarotas, lai samazinātu bloķēšanu un izvairītos no darbību tabulu pievienošanas tīrīšanas laikā. |
| Pārdošana un mārketings | Atjaunināt pieprasīto saņemšanas datumu ar starpuzņēmumu pasūtījumu apstiprināto datumu | Šī funkcija ļauj kontrolēt, kas notiks ar pārdošanas un pirkšanas datuma lauka vērtībām, izmantojot starpuzņēmumu tiešo piegādi. Varat izvēlēties, vai sistēma atjauninās pieprasītos datumus vai izlaidīs to atjaunināšanu. Ja izlaižat atjaunināšanu, pieprasītie datumi atainos debitora pieprasīto informāciju. Ja iespējojat atjaunināšanu, pieprasītie datumi (izmantojot piegādes datuma kontroli) sākotnēji parāda, ko debitors pieprasa. Piegādes datuma kontrole, ja tā atšķiras no *Neviena*, ignorēs sākotnējo pieprasīto informāciju. Šo opciju var iestatīt, izmantojot jauno iestatījumu **Atjaunināt pieprasīto rēķina datumu ar apstiprinātu datumu** starpuzņēmumu kreditora vai debitora iestatījumos.<br><br>Ja līdzeklis ir deaktivizēts, sistēma pārrakstīs pieprasīto rēķina datumu sākotnējos pārdošanas pasūtījumos, pamatojoties uz piegādes datuma kontroles nosacījumiem, bet pieprasītais nosūtīšanas datums paliks tāds pats. |
| Noliktavas pārvaldība | Pēc izlaišanas uz noliktavu daudzumus noapaļot līdz tuvākajai pārdošanas vienībai | Šī funkcija pievieno opciju, kas var ierobežot pasūtījuma daudzumu, kad tiek izlaista nosūtīšana uz noliktavu. Ja aktivizēta, pasūtījuma daudzumi tiek noapaļoti uz leju līdz tuvākajai veselai pārdošanas vienībai, un pasūtījumi, kuros iekļauti daudzumi mazāk nekā vienai pārdošanas vienībai, tiks noraidīti izlaišanai. |
| Noliktavas pārvaldība | Organizācijas mēroga kopuma metode “Ieplānot darba izveidi” | *Plānošanas darba izveides* kopuma metode tiks konfigurēta tā, lai tā darbotos paralēli visām juridiskajām personām. Tiks ietekmēti arī vairāki papildu iestatījumi. Lai iegūtu pilnu informāciju, skatiet [Darba izveides plānošana kopuma laikā](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Nesen ir pievienotas vai ievērojami atjauninātas tālāk norādītās palīdzības tēmas. Tās ne vienmēr ir saistītas ar jaunajiem līdzekļiem, kas pievienoti šim laidienam, kā uzskaitīts iepriekšējā sadaļā, taču tās var palīdzēt jums pilnīgāk izmantot esošos līdzekļus.

| Līdzekļu apgabals | Jaunas vai atjauninātas tēmas |
|---|---|
| Tehnisko izmaiņu pārvaldība | [Bieži uzdoti jautājumi par tehnisko izmaiņu pārvaldību](../engineering-change-management/change-management-faq.md) |
| Sagāde un avoti | [Kategorijas pieprasījumi no kreditoriem](../procurement/category-requests-from-vendors.md) |
| Preču informācijas pārvaldība | [Mērvienības pārvaldība](../pim/tasks/manage-unit-measure.md)<br><br>[Preces konfigurācijas modeļa aprēķini](../pim/config-model-calculations.md) |
| Ražošanas kontrole | [Vienota darbu ID numuru secība](../production-control/unified-job-ids.md) |
| Transportēšanas pārvaldība | [LTL klases](../transportation/ltl-class.md)<br><br>[NMFC kodi](../transportation/nmfc-codes.md) |
| Noliktavas pārvaldība, kopuma izveide un apstrāde | [Kopumu izveide un apstrāde](../warehousing/wave-processing.md)<br><br>[Noliktavas parametri kopuma apstrādei](../warehousing/wave-warehouse-parameters.md)<br><br>[Kopumu veidnes](../warehousing/wave-templates.md)<br><br>[Kopumu sadalījums](../warehousing/wave-allocation-method.md)<br><br>[Darba izveides plānošana kopuma laikā](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Konteinerizēšana](../warehousing/wave-containerization.md)<br><br>[Kopuma izpildes paziņojumi](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.19 ietver platformas atjauninājumus. Lai iegūtu papildinformāciju, skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.19 (2021. gada jūnijs)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.19, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021. gada 1. kopuma plāns

Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Pārbaudiet [Dynamics 365: 2021. gada 1. kopuma plānu](/dynamics365-release-plan/2021wave1/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Noņemtie un novecojušie Supply Chain Management līdzekļi

Tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) apraksta līdzekļus, kas ir vai ir ieplānots noņemšanai no Supply Chain Management.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda funkcija tiek noņemta no preces, izslēgšanas paziņojums tiks izziņota tēma [Noņemtie vai novecošie līdzekļi Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 mēnešu laikā pirms noņemšanas.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
