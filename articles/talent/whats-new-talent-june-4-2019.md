---
title: Jaunumi un izmaiņas programmatūrā Dynamics 365 for Talent (2019. gada 4. jūnijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a93ad140fb9116ffb0c486b7f3175f90859f125
ms.sourcegitcommit: 7b5ff31c0a82809641beb681510201b942932c74
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621866"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-4-2019"></a>Jaunumi un izmaiņas programmatūrā Dynamics 365 for Talent (2019. gada 4. jūnijs)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli programmas Dynamics 365 for Talent: Attract kļūdu labojumi.

## <a name="coming-soon-in-attract"></a>Drīzumā risinājumā Attract

### <a name="job-approvals-on-the-home-page"></a>Darbu apstiprinājumi sākumlapā

Apstiprinājumi tiek rādīti informācijas paneļa sadaļā **Apstiprinājumi**. Apstiprinātāji var pārskatīt savus apstiprinājumus sadaļā **Piešķirts jums**. Šajā sadaļā tiek rādīts darba ID, amata nosaukums, citi apstiprinātāji un datums, kad darbs tika piešķirts. Lietotāji, kuri iesniedz darbu apstiprināšanai, var pārskatīt savus darbus sadaļā **Jūsu pieprasījumi**. Šajā sadaļā tiek rādīti apstiprinātāji, kam šis iesniegtais darbs joprojām ir jāapstiprina.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli programmas Dynamics 365 for Talent: Onboard kļūdu labojumi.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Jauna lapa amatu hierarhijas datu pārbaudei

Personāla vadības (Human resources — HR) darbinieki un administratori var validēt visu to riņķveida atsauču pārvaldības hierarhiju, kas tika netīši importētas. Šai jaunajai lapai varat piekļūt sadaļā **Organizācijas administrēšana \> Saites \> Amati \> Amatu hierarhijas pārbaude**.

### <a name="specify-reason-codes-on-leave-types"></a>Atvaļinājumu tipu iemeslu kodu norādīšana

Organizācijām, iespējams, ir nepieciešama papildinformācija par brīvā laika pieprasījumiem. Tagad atvaļinājumu tipiem varat norādīt iemeslu kodus un ļaut darbiniekiem savos brīvā laika pieprasījumos atlasīt iemesla kodu.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Iemeslu kodu pieprasīšana noteiktiem atvaļinājumu tipiem brīvā laika pieprasījumos

Organizācijām var būt nepieciešami iemeslu kodi noteiktiem atvaļinājumu tipiem, kad darbinieki iesniedz brīvā laika pieprasījumu. Šī prasība var pastāvēt uzņēmuma politikas vai reglamentējošo prasību dēļ. Varat norādīt, kuriem atvaļinājumu tipiem ir nepieciešams iemesla kods, un varat pieprasīt, lai darbinieki savos brīvā laika pieprasījumos atvaļinājuma tipam norādītu iemesla kodu.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Atvaļinājumu un kavējumu transakciju sarakstu nodrošināšana personāla vadībai

Iespēja izsekot darbinieku brīvajam laikam un saprast, kā tiek aprēķināts brīvais laiks, ne tikai palīdz personāla vadībai (Human Resources — HR) atbildēt uz darbinieku jautājumiem, bet arī palīdz garantēt darbiniekiem precīzas brīvā laika piemaksas. Personāla vadībai tagad ir jauns skats uz transakcijām (dotācijām, uzkrājumiem, korekcijām un pieprasījumiem), lai personāla vadības darbinieki redzētu brīvā laika bilanču aprēķinu ietekmējošos faktorus.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Dzēšot ierakstu no Talent, šis ieraksts netiek noņemts no Common Data Service

Ieraksti, kas tiek noņemti no Talent Core HR, tagad tiek noņemti arī no Common Data Service.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Netiek ievēroti mainīgās atlīdzības plāna datumi “derīgs no/līdz”

Šajā laidienā jūs nevarat darbinieku reģistrēt mainīgās atlīdzības plānā, ja sākuma datums ir agrāks par plāna sākuma datumu vai beigu datums ir vēlāks par plāna beigu datumu. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Kad lietotāji atlasa Atcelt, veiktspējas pārskatu komentāri tiek noņemti

Šajā laidienā ir izlabota problēma, kur pārskata komentāri tiek noņemti, ja lietotājs sāk mainīt komentāru, bet pēc tam atlasa **Atcelt**. 

## <a name="in-preview"></a>Priekšskatījumā

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Priekšskatījuma līdzekļi ir iespējoti tikai smilškastes instancēs

Kad nodrošināt jaunu Talent instanci, varat norādīt, vai šīs instances tips ir **Ražošana** vai **Smilškaste**. Instances, kuru tips ir **Smilškaste**, ļauj agri testēt jaunos līdzekļus. Visas esošās programmas Talent instances tiks atjauninātas uz instances tipu **Ražošana**. Ja vēlaties, lai kāda no jūsu esošajām instancēm tiktu atjaunināta uz instances tipu **Smilškaste**, sazinieties ar [atbalsta dienestu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), lai sāktu izmaiņu pieprasījumu.

Papildinformāciju par to, kā tiek publicētas izmaiņas, skatiet tēmā [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Atvaļinājumu tipu ierobežošana brīvā laika pieprasījumos

Organizācijas var piedāvāt darbiniekiem daudz dažādus atvaļinājumu tipus. Taču daži brīvā laika pieprasījumu atvaļinājumu tipi var nebūt piemēroti tam, lai tos iesniegtu darbinieki. Tā vietā šos atvaļinājumu tipus var pārvaldīt personāla vadība (HR). Šajā laidienā jūs varat konfigurēt, kuriem atvaļinājumu tipiem darbinieki var iesniegt brīvā laika pieprasījumus. 

## <a name="coming-soon-in-core-hr"></a>Drīzumā programmā Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Paplašinātas informācijas skatīšana par veiktspēju vadītāja patstāvīgi lietojamajā pakalpojumā

Jauna opcija ļaus vadītājiem apskatīt gan savas tiešās veiktspējas atskaites, gan izvērstās atskaites. Pašlaik rindu pārvaldnieki var piešķirt un atjaunināt veiktspējas mērķus un izdot jaunus pārskatus, kuru pārvaldīšanā ir jāpiedalās viņu darbiniekiem. Turklāt tiešie pārvaldnieki un viņu darbinieki var uzturēt un atjaunināt veiktspējas žurnālus, lai palīdzētu garantēt, ka veiktspējas pārskatīšanas process norit raiti. Kad šīs izmaiņas būs ieviestas, papildus savām tiešajām atskaitēm pārvaldnieki varēs skatīt un uzturēt ar veiktspēju saistītu informāciju par savām izvērstajām atskaitēm. 

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Darbinieki, pārvaldnieki un HR darbinieki varēs drukāt darbinieku veiktspējas pārskatu.
