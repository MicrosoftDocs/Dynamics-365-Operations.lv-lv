---
title: Jaunumi un izmaiņas risinājumā Dynamics 365 for Talent (2019. gada 27. augusts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d7e5be0d9ba5e372e57f06fec77326561196626
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899247"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Jaunumi un izmaiņas risinājumā Dynamics 365 for Talent (2019. gada 27. augusts)

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2447. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Priekšskatījuma līdzekļi ir iespējoti tikai smilškastes instancēs

Kad nodrošināt jaunu Talent instanci, varat norādīt, vai šīs instances tips ir Ražošana vai Smilškaste. Instances, kuru tips ir Smilškaste, ļauj agri testēt jaunos līdzekļus. Visas esošās programmas Talent instances tiks atjauninātas uz instances tipu Ražošana. Ja vēlaties, lai kāda no jūsu esošajām instancēm tiktu atjaunināta uz instances tipu Smilškaste, sazinieties ar atbalsta dienestu, lai sāktu izmaiņu pieprasījumu.

Papildinformāciju par to, kā tiek publicētas izmaiņas, skatiet tēmā [Talent nodrošinājums](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Paplašinātas informācijas skatīšana par veiktspēju vadītāja patstāvīgi lietojamajā pakalpojumā

Jauna opcija ļaus vadītājiem apskatīt gan savas tiešās veiktspējas atskaites, gan izvērstās atskaites. Pašlaik rindu pārvaldnieki var piešķirt un atjaunināt veiktspējas mērķus un izdot jaunas atsauksmes. Turklāt tiešie vadītāji un viņu darbinieki var uzturēt un atjaunināt veiktspējas žurnālus, lai palīdzētu nodrošināt, ka veiktspējas pārskatīšanas process norit raiti. Kad šīs izmaiņas būs ieviestas, papildus savām tiešajām atskaitēm pārvaldnieki varēs skatīt un uzturēt ar veiktspēju saistītu informāciju par savām izvērstajām atskaitēm.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Juridisko personu dzēšana nav atļauta, ja uzņēmumā ir darbinieki (339849)

Šo izmaiņu dēļ nevar noņemt vai dzēst uzņēmumus, ja juridiskajai personai ir darbinieki un citi saistītie dati.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Atlīdzības pārvaldības biznesa inteliģences analīze neatbilst atlīdzības darbvietā (322493)

Šajā laidienā atlīdzības analīzes ir pielāgotas, lai precīzi atspoguļotu darbiniekiem piešķirtos plānus.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Darbplūsmas vietturis %uzņēmums% parāda DAT, kad darbinieki tiek nolīgti, izmantojot darbplūsmu (343905)

Ar šo laidienu uzņēmuma vietturis parāda juridisko personu, kas ir saistīta ar jaunā darbinieka nodarbinātību.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>Elements CDSJobPosition parāda kļūdu, kad ir iestatīts derīgs beigu datums (349387)

Šajā laidienā **Amata informācija** un **Amata ilgums** datu avoti elementā **CDSJobPosition** ļauj rediģēt no Common Data Service uz laukiem **Sākuma datums**. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>Darbinieka darba attiecību pārtraukšanas gadījumā nostrādātā pēdējā diena tiek aizpildīta Norīkojuma beigu datumā (332496)

Šī izmaiņa tagad maina noklusējumu pozīcijai **Piešķires beigu datums** uz **Nodarbinātības beigu datums**. Varat mainīt šos noklusējumus, ievadot datus.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Juridiskās personas nav ierobežotas ar nolīgšanu (338871)
 
Šīs izmaiņas ierobežo nolīgšanas procesu, lai parādītu tikai tās juridiskās personas, kurām lietotājam ir piekļuve.  

## <a name="in-preview"></a>Priekšskatījumā

### <a name="streamlined-employee-entry-and-navigation"></a>Racionalizēta darbinieku ievade un navigācija

Šī funkcionalitāte tagad ir pieejama smilškastes un izmēģinājuma vidē. Lai ieslēgtu šo līdzekli, dodieties uz **Sistēmas administrēšana > Saites > Iestatīšana > Sistēmas parametri > Priekšskatījuma līdzekļi**. Atlasiet **Uzlabotā darbinieka veidlapa un navigācija**. Tas ļauj iespējot šīs izmaiņas visiem lietotājiem. Šo opciju varat izslēgt jebkurā laikā.

Papildinformāciju skatiet rakstā [Racionalizēts darbinieka ieraksts un navigācija](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Drīzumā

### <a name="platform-update-29"></a>Platformas update 29

Papildinformāciju par atjauninājumu Platform update 29 skatiet rakstā [Priekšskatījuma līdzekļi versijā Dynamics 365 for Finance and Operations Platform update 29 (2019. gada oktobris)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
