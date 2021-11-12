---
title: Jaunumi un izmaiņas risinājumā Dynamics 365 Supply Chain Management 10.0.20 (2021. gada augusts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Supply Chain Management 10.0.20.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8f46165a89f064878d2e8af1b0b174b04eca37e
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647318"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>Jaunumi un izmaiņas risinājumā Dynamics 365 Supply Chain Management 10.0.20 (2021. gada augusts)

[!include [banner](../includes/banner.md)]

Šī tēma uzskaita līdzekļus, kas ir vai nu jauni, vai kas ir mainīti programmas Microsoft Dynamics 365 Supply Chain Management versijā 10.0.20. Šai versijai ir būvējuma numurs 10.0.886, un tas ir pieejams šeit:

- **Priekšskatījuma laidiens:** 2021. gada maijs
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2021. gada jūlijs
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2021. gada augusts

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Kolonna *Līdzeklis* nodrošina saites uz [izlaišanas plānu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), kur varat redzēt oficiālos izlaišanas datumus katram līdzeklim. Kolonna *Vairāk informācijas* sniedz detalizētu informāciju un/vai saites uz saistīto dokumentāciju.

Vairumam šo līdzekļu ir jābūt iespējotiem, izmantojot [Līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), pirms varat tos izmantot.

| Līdzekļu apgabals | Funkcija | Papildinformācija |
|---|---|---|
| Krājumi&nbsp;un&nbsp;loģistika | [Pārdošanas pasūtījuma detalizētās informācijas veiktspējas uzlabošana](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Atverot pārdošanas pasūtījumus, jo īpaši pasūtījumus, kas ietver daudzas rindas, šī funkcija padara lietotāja interfeisu lielāku. |
| Ražošana | [Izsaukt procesa automatizācijas plūsmas, lai izveidotu kvalitātes pasūtījumus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Izsaukt procesa automatizācijas plūsmas, lai izveidotu kvalitātes pasūtījumus](../production-control/process-automation-quality-orders.md ) |
| Ražošana | [Uzlabots ražošanas izpildes interfeiss ražošanai](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [Ražošanas izpildes interfeisa konfigurēšana](../production-control/production-floor-execution-configure.md) |
| Plānošana | [Bezgalīga noslodzes plānošana plānošanas optimizācijai](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [Plānošana ar neierobežotu noslodzi](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Preču informācijas pārvaldība | [Izmaiņu pārvaldība formulās un to komponentos](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Pārvaldīt izmaiņas formulās un to sastāvdaļās](../engineering-change-management/manage-formula-changes.md) |
| Preču informācijas pārvaldība | [Preces gatavības pārbaudes](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Preces gatavība](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļa uzlabojumi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļu uzlabojumi. Katrs no šiem nodrošina inkrementālu uzlabojumu esošajai funkcijai. Tā kā tie ir tikai uzlabojumi, tie nav uzskaitīti [izlaišanas plānā](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Tomēr, lai nodrošinātu, ka šie uzlabojumi nenonāk pretrunā ar esošajiem pielāgojumiem vai preferencēm, katrs no tiem tiek izslēgts pēc noklusējuma (ja vien nav norādīts citādi). Ja vēlaties izmantot kādu no šiem līdzekļiem, tos ir skaidri jāiespējo [Līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modulis | Līdzekļa&nbsp;nosaukums&nbsp;līdzekļu&nbsp;pārvaldībā | Papildinformācija |
|---|---|---|
| Vispārējā plānošana | Koriģētas pieprasījuma apjoma prognozes paralēla pilnvarošana | Šis līdzeklis ļauj pielāgotās pieprasījuma apjoma prognozes paralēlu autorizāciju no **Pielāgotās pieprasījuma apjoma prognozes** lapas. Šīs funkcijas nolūks ir palielināt veiktspēju, kad ir autorizēts liels prognožu skaits. Autorizējoties lietotājs var norādīt **Pavedienu skaitu** autorizācijas dialogā. |
| Vispārējā plānošana | (Priekšskatījums) Sērijveida nostiprināšana un apvienošana plānotajiem lielapjoma un pakotņu partiju pasūtījumiem | Šis līdzeklis sniedz iespēju izmantot pakešuzdevumus, lai nostiprinātu un konsolidētu plānotos lielapjoma un pakotņu pasūtījumus. |
| Ražošanas kontrole | Kopēt vispārīgus maršrutus | Šī funkcija uzlabo maršruta kopēšanas funkciju, lai ļautu lietotājiem kopēt maršrutus, kas nav specifiski krājumiem. Tas iespējo sistēmu atjaunināt visu atbilstošo informāciju (piemēram, vietni, maršrutu grupu, resursu vajadzības un dažādus laikus) pēc maršruta kopēšanas funkcijas izmantošanas, lai pārrakstītu maršrutu, kas vēl nav piešķirts krājumam. |
| Ražošanas kontrole | Saistīto resursu pieprasījumu atjaunināšana pēc maršruta darbības maiņas | Šis līdzeklis sistēmā iespējo saistīto resursu pieprasījumu atjaunināšanu pēc tam, kad lietotājs izmaina esošas maršruta darbības operāciju. |
| Preču informācijas pārvaldība | Materiālu komplekta pārskata iepriekšēja apstrāde, lai novērstu noildzes | Šī funkcija izraisa materiālu komplekta pārskata priekšapstrādi. Šādi var izvairīties no noildzes problēmām, ja atskaitei ir liela datu noslodze. |
| Sagāde un avoti | Iespējot ar iepirkumu saistīto darbplūsmu atiestatīšanu | Šis priekšskatījuma līdzeklis ļauj jums atiestatīt šādas darbplūsmas uz melnraksta statusu: Pirkšanas pasūtījums, Kreditora maiņa un Pirkšanas pieprasījumi. |
| Transportēšanas pārvaldība | Iespējo kreditora rēķinu žurnāla izveidi pēc vedmaksas rēķina atmešanas | Kad šī funkcija ir aktivizēta, atbilstošs kreditora rēķinu žurnāls tiks izveidots tikai saskaņošanas iemeslu dēļ, ja izmantosiet opciju Maksāt kreditoram. Pretējā gadījumā vienmēr tiks izveidots rēķinu žurnāls. |
| Noliktavas vadība | Papildināšanas darbiem atlasīto veidņu apstiprināšana | Šī funkcija palīdz nodrošināt, ka lietotāji, iestatot papildināšanas darbu, atlasa derīgas papildināšanas veidnes. Tas neļauj lietotājiem izveidot papildināšanas darbu bez veidnes un atlasīt *Kopuma pieprasījuma* tipa veidnes, kas neizveidos papildināšanas darbu un var aizņemt ilgāku laiku. |

## <a name="new-and-updated-documentation-resources"></a>Jauni un atjaunināti dokumentācijas resursi

Nesen ir pievienotas vai ievērojami atjauninātas tālāk norādītās palīdzības tēmas. Tās ne vienmēr ir saistītas ar jaunajiem līdzekļiem, kas pievienoti šim laidienam, kā uzskaitīts iepriekšējā sadaļā, taču tās var palīdzēt jums pilnīgāk izmantot esošos līdzekļus.

| Līdzekļu apgabals | Jaunas vai atjauninātas tēmas |
|---|---|
| Tehnisko izmaiņu pārvaldība | [Preču dzīves cikla stāvokļi un darījumi](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Krājumu vadība | [Krājumu redzamības pievienojumprogramma](../inventory/inventory-visibility.md)<br><br>[Kvalitātes un neatbilstības pārvaldības pārskats](../inventory/quality-management-processes.md) (plus visas saistītās kvalitātes pārvaldības tēmas) |
| Sagāde un avoti | [Kreditora sertifikācijas uzturēšana](../../finance/public-sector/manage-vendor-certification.md) |
| Ražošanas kontrole | [Ražošanas izpildes interfeisa stils](../production-control/production-floor-execution-styles.md) |
| Noliktavas vadība | [Darbību ikonu un nosaukumu piešķiršana Warehouse Management mobilajai programmai](../warehousing/step-icons-titles.md)<br><br>[Atliktā manuālās krājumu kustības apstrāde](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmām

Microsoft Dynamics 365 Supply Chain Management 10.0.20 ietver platformas atjauninājumus. Lai iegūtu papildinformāciju, skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.20 (2021. gada jūlijs)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas iekļauti katrā no atjauninājumiem, kas ir daļa no 10.0.20, piesakieties Lifecycle Services (LCS) pakalpojumos un aplūkojiet [KB rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8). 

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
