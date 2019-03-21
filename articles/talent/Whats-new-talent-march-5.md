---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 5. marts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6b490a696dc0a00c47e56f57373f330d0e53dde
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/08/2019
ms.locfileid: "782941"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 5. marts)

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīti jaunie vai izmainītie programmas Talent līdzekļi.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

### <a name="extending-option-sets-in-attract"></a>Opciju kopu paplašināšana programmā Attract

Programmā Attract ir vairāki lauki, kas ir opciju kopas pakalpojumā Common Data Service (CDS). Ir ieviestas jaunas iespējas, lai paplašinātu opciju kopas, tostarp lauks **Noraidīšanas pamatojums**, lauks **Nodarbinātības veids** un lauks **Darba stāža veids**.

> [!IMPORTANT]
> Lai izmantotu darba publicēšanas pakalpojumā LinkedIn funkcionalitāti, ir jāizmanto lauki **Nodarbinātības veids** un **Darba stāžs veids** lapā **Darba informācija**. Šo lauku noklusējuma vērtības nodrošina pakalpojums LinkedIn, un tās tiek rādītas, kad darbs tiek publicēts. Ja publicējat darbus pakalpojumā LinkedIn un izmaināt šo lauku esošās opciju kopas vērtības, darbs joprojām tiek publicēts, taču pakalpojumā LinkedIn netiek parādītas pielāgotās lauku **Nodarbinātības veids** un **Darba stāža veids** vērtības.

## <a name="changes-in-onboarding"></a>Izmaiņas pievienošanas procesā

### <a name="private-preview-for-onboard-teams"></a>Pievienošanas darba grupu privāts priekšskatījums
Tagad varat viegli kopīgot veidnes un sadarboties to izmantošanā visā savā organizācijā. Papildinformāciju skatiet rakstā [Dalīšanās ar labākās prakses piemēriem savā organizācijā, izmantojot pievienošanas darba grupas](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Uzdevumu veicēju vietturu privāts priekšskatījums
Varat paplašināt savas veidnes, piešķirot aktivitātes lomām, nevis personām. Pēc tam lomas tiek piešķirtas personām ceļveža izveides laikā. Papildinformāciju skatiet rakstā [Ceļvežu administrēšanas racionalizācija, piešķirot aktivitātes lomām](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR
**8.1.2178 būvējums**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Darbplūsmas konfigurēšana automātiskai pieprasījuma apstiprināšanai vai darbplūsmas izpildei, ja personāla vadības speciālists vai rindas vadītājs iesniedz vai atjaunina brīvā laika pieprasījumus
Ir pievienoti jauni darbplūsmas nosacījumi, kas sniedz iespēju automātiski apstiprināt brīvā laika pieprasījumus, ja tos ir iesniedzis darbinieka vadītājs vai personāla vadības speciālists. Viens veids, kā darbplūsmā panākt šo automātisko apstiprināšanu, ir iespējot automātisku darbību, ko aktivizē darbplūsmas apstiprināšana.

Tālāk ir norādīti pievienotie nosacījumi.

- Iesniedza — tiek izmantots, lai novērtētu tā sistēmas lietotāja ID, kurš ir iesniedzis pieprasījumu darbplūsmai.
- Kā vārdā iesniegts — tiek izmantots, lai novērtētu to, vai prombūtnes pieprasījums ir ticis iesniegts ar pieprasījumu saistītā nodarbinātā vārdā.
- Iesniedzis personāla vadības speciālists — tiek izmantots, lai novērtētu to, vai sistēmas lietotājam, kurš ir iesniedzis pieprasījumu darbplūsmai, ir piešķirta personāla vadības speciālista loma.
- Iesniedzis vadītājs — tiek izmantots, lai novērtētu to, vai lietotājs, kurš ir iesniedzis brīvā laika pieprasījumu darbplūsmai, ir ar pieprasījumu saistītā darbinieka vadītājs rindas hierarhijā.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Fiksētas atlīdzības iespējošana darbiniekiem ar gaidāmām amatu piešķirēm
Bieži vien darbinieki pievienojas organizācijai ar vēlāku sākuma datumu. Šīs izmaiņas sniedz iespēju definēt fiksētu atlīdzību darbiniekiem, kuriem ir gaidāmas amatu piešķires.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Tukši amata algas lauki amata rediģēšanas laikā
Šīs izmaiņas nodrošina, ka tagad, pierasot esošo amatu izmaiņas, algas laukos pēc noklusējuma tiek norādītas pašreizējās vērtības.

### <a name="other-miscellaneous-bug-fixes"></a>Citi dažādu kļūdu labojumi
Šajā laidienā ir ietverti citi nelieli kļūdu labojumi.

### <a name="upgrade-to-cds-for-apps"></a>Pakalpojuma CDS programmām jauninājums
Drīz būs pienācis jaunināšanas uz pakalpojumu CDS programmām termiņš. Pierakstieties PowerApps administrēšanas centrā, lai noteiktu, vai jūsu datu bāzi ir nepieciešams jaunināt. Papildinformāciju par termiņiem un jaunināšanai nepieciešamajām darbībām skatiet rakstā [Jaunināšana uz pakalpojumu Common Data Service programmām](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Drīzumā

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Papildu atlīdzības drošība (fiksētā un mainīgā)
Daudzās organizācijās atlīdzības un atvieglojumu pārvaldnieki var piekļūt tikai noteiktiem atlīdzības ierakstiem, piemēram, vadītāju vai reģionālo darbinieku ierakstiem. Šīs izmaiņas sniedz iespēju pārvaldīt un uzturēt atlīdzības plānus dažādām darbinieku grupām organizācijā. Fiksētajiem un mainīgajiem plāniem var piešķirt drošības lomas, no kurām ir atkarīga piekļuve plāniem un ar tiem saistītajiem darbinieku datiem, piemēram, algu vai prēmiju ierakstiem. Šo atlīdzību šiem darbiniekiem var apstrādāt tikai lietotāji, kuriem ir piešķirtas lomas ar konkrētajām piekļuves atļaujām.

###  <a name="platform-update-24"></a>Platformas update 24
Papildinformāciju par 24. platformas atjauninājumu skatiet [Jaunumi un izmaiņas Finance and Operations 24. platformas atjauninājumā (2019. gada marts)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
