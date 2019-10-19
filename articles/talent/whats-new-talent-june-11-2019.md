---
title: Jaunumi un izmaiņas programmatūrā Dynamics 365 Talent (2019. gada 11. jūnijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b06dc0556bd1461573cd56abed602d72333a3f39
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023934"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-11-2019"></a>Jaunumi un izmaiņas programmatūrā Dynamics 365 Talent (2019. gada 11. jūnijs)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

### <a name="search-engine-optimization-for-job-posts"></a>Meklētājprogrammu optimizācija darba sludinājumiem

Kad ieslēdzat opciju **Meklētājprogrammu optimizācija** programmatūras Dynamics 365 Talent: Attract administrēšanas centrā, Attract informē Google indeksēšanas lietojumprogrammu programmēšanas interfeisu (application programming interface — API), ka tīmekļa lapā ir jāveic pārmeklēšana katru reizi, kad aktivizējat un publicējat jaunu darbu vai jau esošu darbu. Šādi darbs tiks rādīts meklēšanas rezultātos gan Google, gan citās meklētājprogrammās.

Līdzīgi arī, kad noņemat kādu darba sludinājumu, Attract informē indeksēšanas API, lai noņemtais darbs vairs netiktu rādīts meklēšanas rezultātos.

> [!NOTE]
> Tīmekļa rāpuļprogrammām nav definēta laika intervāla tīmekļa lapu pārmeklēšanai vai meklēšanas rezultātu atjaunināšanai.

## <a name="coming-soon-in-attract"></a>Drīzumā risinājumā Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Darbu apstiprinājumu rādīšana sākumlapā

Apstiprinājumi tiek rādīti informācijas paneļa sadaļā **Apstiprinājumi**. Apstiprinātāji var pārskatīt savus apstiprinājumus sadaļā **Piešķirts jums**, kur ir norādīts darba ID, amata nosaukums, citi apstiprinātāji un datums, kad šis darbs tika piešķirts. Lietotāji, kuri iesniedz darbu apstiprināšanai, var pārskatīt savus darbus sadaļā **Jūsu pieprasījumi**, kur ir norādīti apstiprinātāji, kam šis iesniegtais darbs joprojām ir jāapstiprina.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2337.

### <a name="platform-update-27-for-finance-and-operations"></a>Finance and Operations Platform update 27

Papildinformāciju par atjauninājumu Finance and Operations Platform update 27 skatiet rakstā [Priekšskatījuma līdzekļi Dynamics 365 Finance and Operations Platform update 27 (2019. gada jūnijs)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>Līdzekļu pārvaldības darbvieta programmā Talent

Darbvieta **Līdzekļu pārvaldība** sadaļā **Sistēmas administrēšana** ļauj jums skatīt, iespējot, atspējot un plānot līdzekļus, kas tiek piegādāti katrā laidienā. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Darbvietu **Līdzekļu pārvaldība** varat izmantot, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service elementu atbalsts pielāgotajiem laukiem

Izdevējiestādes elements tagad atbalsta pielāgotus laukus.

### <a name="new-common-data-service-entities"></a>Jauni Common Data Service elementi

Ir pievienots elements Uzdevumu grupa.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Priekšskatījuma līdzekļi būs iespējoti tikai smilškastes vidēs

Papildinformāciju par to, kā tiek publicētas izmaiņas, skatiet tēmā [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Kad nodrošināt jaunu Talent instanci, varat norādīt, vai šīs instances tips ir Ražošana vai Smilškaste. Instances tips Smilškaste ļauj agri testēt jaunos līdzekļus. Visas esošās programmas Talent instances tiks atjauninātas uz instances tipu **Ražošana**. Ja vēlaties, lai kāda no jūsu esošajām instancēm tiktu atjaunināta uz instances tipu **Smilškaste**, sazinieties ar [atbalsta dienestu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), lai sāktu izmaiņu pieprasījumu.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Atvaļinājumu tipu ierobežošana brīvā laika pieprasījumos

Organizācijas var piedāvāt darbiniekiem daudzus atvaļinājumu tipus. Taču daži brīvā laika pieprasījumu atvaļinājumu tipi var nebūt piemēroti tam, lai tos iesniegtu darbinieki. Tā vietā šos atvaļinājumu tipus var pārvaldīt personāla vadība (Human resources — HR). Šajā laidienā jūs varat konfigurēt, kuriem atvaļinājumu tipiem darbinieki var iesniegt brīvā laika pieprasījumus. 

## <a name="coming-soon-in-core-hr"></a>Drīzumā programmā Core HR

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Paplašinātas informācijas skatīšana par pārskata veiktspēju vadītāja patstāvīgi lietojamajā pakalpojumā

Jauna opcija ļaus vadītājiem apskatīt gan savas tiešās veiktspējas atskaites, gan izvērstās atskaites. Pašlaik rindu pārvaldnieki var piešķirt un atjaunināt veiktspējas mērķus un izdot jaunas atsauksmes. Turklāt tiešie pārvaldnieki un viņu darbinieki var uzturēt un atjaunināt veiktspējas žurnālus, lai palīdzētu garantēt, ka veiktspējas pārskatīšanas process norit raiti. Kad šīs izmaiņas būs ieviestas, papildus savām tiešajām atskaitēm pārvaldnieki varēs skatīt un uzturēt ar veiktspēju saistītu informāciju par savām izvērstajām atskaitēm.

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Darbinieki, pārvaldnieki un HR darbinieki varēs drukāt darbinieku veiktspējas pārskatu.
