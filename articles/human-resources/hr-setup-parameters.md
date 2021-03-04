---
title: Personāla vadības resursu konfigurēšana
description: Dažu personāla vadības parametru iestatījumi tiek koplietoti uzņēmumu starpā, savukārt citu parametru iestatījumi ir raksturīgi noteiktam uzņēmumam. Šajā rakstā ir paskaidrots, kā iestatīt uzņēmumam raksturīgus PV parametrus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bac50c5f302797e28df2bc792893c8a682899a93
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419489"
---
# <a name="configure-human-resources-parameters"></a>Personāla vadības resursu konfigurēšana

Dažu personāla vadības (PV) parametru iestatījumi tiek koplietoti uzņēmumu starpā, savukārt citu parametru iestatījumi ir raksturīgi noteiktam uzņēmumam. Šajā rakstā ir paskaidrots, kā iestatīt uzņēmumam raksturīgus PV parametrus.

Divas lapas tiek izmantotas, lai iestatītu personāla vadības parametrus (PV). Parametriem, kas ir kopīgi visiem uzņēmumiem, izmanto lapu **Personāla vadības kopīgie parametri**. Parametriem, kas ir specifiski uzņēmumam (citiem vārdiem sakot, iestatījumi attiecas uz vienu uzņēmumu), izmanto lapu **Personāla vadības parametri**. Lapā **Personāla vadības parametri** iestatījumi ir sadalīti sešās cilnēs:

-   Vispārējs
-   Personāla atlase — tā nav iekļauta programmā Dynamics 365 Human Resources
-   Atlīdzība
-   Numuru sērijas
-   Likums par ģimenes un medicīniskajiem atvaļinājumiem (FMLA)
-   Darbinieku pašapkalpošanās

Katra cilne ietver informāciju, kas attiecas uz vienu uzņēmumu. Iestatījumi lapā **Vispārīgi** nosaka informācijas parādīšanos par kavējumu, traumu un slimību un jaunām pieņemšanām darbā. Šīs cilnes iestatījumi definē arī dažus noklusējuma ierakstus, kas parādās darba laikā. Konkrētāk, šī cilne ļauj atlasīt krāsu, kuru izmantot atvērtām prombūtnes darbībām, norādīt stilu lapu pārskatiem, aktivizēt integrāciju starp apmācību kursiem un prombūtnes reģistrēšanu un izvēlieties prombūtnes kodu, kas tiek izmantots šīs integrācijas kontrolēšanai. Var arī norādīt, cik ilgi traumu un slimību gadījumu incidentus būtu jāglabā un norādīt noklusējuma identifikācijas numuru, kas tiek parādīts, kad tiek pieņemts darbā jauns darbinieks. 

Iestatījumi cilnē **Personāla atlase** definē dokumentu tipus, kas tiek izmantoti korespondencei, kas tiek automātiski nosūtīta kandidātiem, un personāla atlases projektu, ko izmanto nevēlamiem pieteikumiem (pieteikumiem, kas nav paredzēti konkrētam personāla atlases projektam). Periods, kas tiek noteiks personāla atlases projekta vecumstruktūrai, nosaka personāla atlases projektus, kas iekļauti elementā **Vecumstruktūras projekti** darbvietā **Personāla atlases pārvaldība**. Periods, kas noteikts brīdinājumam par pieteikuma iesniegšanas termiņu, tiek izmantots, lai parādītu personāla atlases projektus, kuriem tuvojas pieteikumu iesniegšanas termiņš elementā **Tuvojas pieteikuma iesniegšanas beigu termiņš** darbvirsmā **Personāla atlase**. 

Iestatījumi cilnē **Atlīdzība** definē, vai lietotājiem ir jāapstiprina, ka viņi vēlas saglabāt informāciju fiksēto vai mainīgo atlīdzību plānam. Ja atzīmējat izvēles rūtiņu **Iespējot saglabāšanas pārbaudi**, ikreiz, kad lietotāji aizver ar atlīdzību saistītu lapu, viņi saņem ziņojumu ar jautājumu, vai viņi vēlas saglabāt ierakstu. Dažas atlīdzības pārvaldības lapas neļauj lietotājiem dzēst informāciju. Tāpēc prasot lietotājiem apstiprināt, ka viņi vēlas saglabāt informāciju, var ierobežot informācijas daudzumu, kas tiek saglabāts un ko nevar izdzēst vēlāk. Ja izvēles rūtiņa **Iespējot saglabāšanas pārbaudi** ir notīrīta, ieraksti tiek vienmēr saglabāti nekavējoties, iespējams pirms lietotājs ir gatavs. Ja jūs izmantojat veiktspējas pārvaldību, cilne **Atlīdzība** ļauj jums izvēlēties vērtēšanas modeli, ko veiktspējas vērtēšanas laikā lietot modeļa, kas piešķirts atlīdzības plāniem, vietā. 

### <a name="previously-released-functionality"></a>Iepriekš izlaistā funkcionalitāte

Iestatījumi cilnē **Numuru sērija** nosaka sērijas, kas tiek izmantotas, lai automātiski piešķirtu ID krājumiem Personāla vadībā, piemēram, pieteikumiem, kavējumu reģistrācijām, atlīdzības procesa rezultātiem, lietas numuriem, kursiem un kursu darba kārtībām. Lai saglabātu numuru sēriju atsauces un kodus, lietojiet saraksta lapu **Numuru sērijas** (noklikšķiniet uz **Organizācijas administrēšana** &gt; **Numuru sērijas** &gt; **Numuru sērijas**).

> [!NOTE]
> Nostrādāto stundu skaits nedrīkst pārsniegt 1250 un nodarbinātības garums nedrīkst pārsniegt 12 mēnešus. Šīs maksimālās vērtības ir saskaņā ar federālo likumu Amerikas Savienotajās Valstīs. Visbeidzot, iestatījumi cilnē **Darbinieku pašapkalpošanās** nosaka informāciju, ko vadītāji var ievadīt savu darbinieku vārdā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]