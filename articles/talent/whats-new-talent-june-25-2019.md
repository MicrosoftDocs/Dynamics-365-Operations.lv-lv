---
title: Jaunumi un izmaiņas programmatūrā Dynamics 365 Talent (2019. gada 25. jūnijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 98ac7df9fa33635814b390427fd3292bdc1175ed
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528649"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-25-2019"></a>Jaunumi un izmaiņas programmatūrā Dynamics 365 Talent (2019. gada 25. jūnijs)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Drīzumā risinājumā Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Darbu apstiprinājumu rādīšana sākumlapā

Apstiprinājumi tiek rādīti informācijas paneļa sadaļā **Apstiprinājumi**. Apstiprinātāji var pārskatīt savus apstiprinājumus sadaļā **Piešķirts jums**, kur ir norādīts darba ID, amata nosaukums, citi apstiprinātāji un datums, kad šis darbs tika piešķirts. Lietotāji, kuri iesniedz darbu apstiprināšanai, var pārskatīt savus darbus sadaļā **Jūsu pieprasījumi**, kur ir norādīti apstiprinātāji, kam šis iesniegtais darbs joprojām ir jāapstiprina.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard
Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2357.

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>Galvenajam amatam tiek rādīta nepareiza vērtība (314266)

Šīs izmaiņas iestatījumu **Galvenais amats** visās lapās rādīs konsekventi.

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>Pārskatā nevar rediģēt pēc darbplūsmas atkārtotas izsaukšanas (318180)

Pārskatus, kas ir izsaukti atkārtoti, izmantojot darbplūsmu, tagad var rediģēt.

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>Beigu komentāru lauks pārskatos netiek tulkots (325921)

Programmā Talent etiķete **Beigu komentāri** tiks tulkota.

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Priekšskatījuma līdzekļi būs iespējoti tikai smilškastes vidēs

Kad nodrošināt jaunu Talent instanci, varat norādīt, vai šīs instances tips ir **Ražošana** vai **Smilškaste**. Instances tips **Smilškaste** ļauj agri testēt jaunos līdzekļus. Visas esošās programmas Talent instances tiks atjauninātas uz instances tipu **Ražošana**. Ja vēlaties, lai kāda no jūsu esošajām instancēm tiktu atjaunināta uz instances tipu **Smilškaste**, sazinieties ar [atbalsta dienestu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), lai sāktu izmaiņu pieprasījumu.

Papildinformāciju par to, kā tiek publicētas izmaiņas, skatiet tēmā [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

## <a name="in-preview"></a>Priekšskatījumā

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Atvaļinājumu tipu ierobežošana brīvā laika pieprasījumos

Organizācijas var piedāvāt darbiniekiem daudzus atvaļinājumu tipus. Taču daži brīvā laika pieprasījumu atvaļinājumu tipi var nebūt piemēroti tam, lai tos iesniegtu darbinieki. Tā vietā šos atvaļinājumu tipus var pārvaldīt personāla vadība (Human resources — HR). Šajā laidienā jūs varat konfigurēt, kuriem atvaļinājumu tipiem darbinieki var iesniegt brīvā laika pieprasījumus. 

## <a name="coming-soon-in-core-hr"></a>Drīzumā programmā Core HR

### <a name="feature-management-area-in-talent"></a>Līdzekļu pārvaldības apgabals programmā Talent

Rīks **Līdzekļu pārvaldība** tiks noņemts no sadaļas **Sistēmas administrēšana**, jo šis līdzeklis izraisa problēmas. Mēs to atkal ieviesīsim kādā no nākamajiem rīka **Līdzekļu pārvaldība** laidieniem. 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service elementu atbalsts pielāgotajiem laukiem

Pielāgotus laukus atbalstīs šādi elementi: **Algas ienākumu veida kods**, **Fiksētas atlīdzības notikums**, **Atlīdzību režģis**, **Apmaksas periods** un **Atlīdzības atsauces punkts**. 

### <a name="new-common-data-service-entities"></a>Jauni Common Data Service elementi

Programmai Common Data Service tiks pievienots elements **Iemeslu kodi**.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Veiktspējas informācijas skatīšana tiešajām un izvērstajām atskaitēm vadītāja patstāvīgi lietojamajā pakalpojumā

Jauna opcija ļaus vadītājiem apskatīt gan savas tiešās veiktspējas atskaites, gan izvērstās atskaites. Pašlaik rindu pārvaldnieki var piešķirt un atjaunināt veiktspējas mērķus un izdot jaunas atsauksmes. Turklāt tiešie vadītāji un viņu darbinieki var uzturēt un atjaunināt veiktspējas žurnālus, lai palīdzētu nodrošināt, ka veiktspējas pārskatīšanas process norit raiti. Kad šīs izmaiņas būs ieviestas, papildus savām tiešajām atskaitēm pārvaldnieki varēs skatīt un uzturēt ar veiktspēju saistītu informāciju par savām izvērstajām atskaitēm.

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Darbinieki, pārvaldnieki un HR darbinieki varēs drukāt darbinieku veiktspējas pārskatu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]