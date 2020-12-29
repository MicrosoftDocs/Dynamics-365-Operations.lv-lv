---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 20. marts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
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
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a7a44e1c9d8dcb4b2cc81a682a044d26cdc1149e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461865"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-20-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 20. marts)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

### <a name="setting-the-audience-on-activities"></a>Aktivitāšu auditorijas iestatīšana
Aktivitātēm sistēmā tagad var definēt auditoriju. Ar procesu saistītās aktivitātes (piemēram, aktivitātes Intervija, Grafiks, Atsauksmes un EEO) var iestatīt uz Visi kandidāti, Iekšējie kandidāti un Ārējie kandidāti. Pielāgotās aktivitātes, piemēram, Microsoft Forms, YouTube videoklipus un tīmekļa saturu, var piegādāt grupām Visi kandidāti, Iekšējie kandidāti, Ārējie kandidāti vai Darbā pieņemšanas grupa.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Karjeras vietnes darbu atrodamības uzlabošana: meklētājoptimizācija
Šis līdzeklis dod iespēju meklētāja rāpuļprogrammām sasniegt un indeksēt darba sludinājumus Attract karjeras vietnē. Tas palīdz kandidātiem atrast Attract karjeras vietnē publicētos darbus, izmantojot populāras meklētājprogrammas.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Pieteikšanās norādes rādīšana kandidātiem, kas ir aizmirsuši savus akreditācijas datus
Ja kandidāts ir piemirsis sociālos akreditācijas datus, ar kuriem viņš pieteicās kādam darbam, atverot šim kandidātam sūtītajā e-pasta ziņojumā saglabāto saiti, tagad kandidāts redz norādi ar nodrošinātāja nosaukumu un lietotājvārdu (aizēnotu). Tas palīdz izmantot pareizos akreditācijas datus, lai piekļūtu savam darba pieteikumam.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Palīdzība iekšējiem kandidātiem izpētīt iekšējos darbus
Ir novērsta problēma, kuras dēļ ārējie kandidāti darbam varēja redzēt personāla atlases darbinieka vai par pieņemšanu darbā atbildīgā vadītāja vārdu un uzvārdu. Tagad darbā pieņemšanas grupas dalībniekus darbam var redzēt tikai iekšējie kandidāti. Tāpat iekšējiem kandidātiem ir vienkāršāk apskatīt tikai iekšējos darbus un pieteikties tiem. Kad kandidāts mēģina piekļūt saitei, lai skatītu tikai iekšēju darbu vai pieteiktos tam, kandidātam ir nepieciešams autentificēties ar Azure Active Directory akreditācijas datiem. Iekšējiem kandidātiem ir arī iespēja sazināties ar darbā pieņemšanas grupas dalībnieku, lai izteiktu interesi par darbu vai lai uzzinātu par to vairāk. Šī iespēja ir pieejama visiem darbiem, kas ir paredzēti tikai iekšējiem kandidātiem. Plašāku informāciju skatiet tēmā [Karjeras vietas iestatīšana Microsoft Dynamics 365 Talent - Attract](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Sudraba medaļas ieguvēju norādīšana, lai kandidātiem piešķirtu augstu vērtību turpmākiem amatiem
Personāla atlases darbinieki un par pieņemšanu darbā atbildīgie vadītāji bieži veido sarakstus ar kandidātiem, kuri bija piemēroti amatam, bet kurus nevarēja iekļaut piedāvājumā, jo amats jau bija aizpildīts. Šādi kandidāti, saukti par sudraba medaļas ieguvējiem, ir vērtīgi, jo viņi var samazināt darbā pieņemšanas laiku nākamajā reizē, kad kļūst pieejams līdzīgs amats. Attract tagad ļauj personāla atlases darbiniekiem un par pieņemšanu darbā atbildīgajiem vadītājiem kandidātu sarakstā norādīt sudraba medaļas ieguvējus, ja kandidāts tiek pārcelts uz posmu Piedāvājums. Sudraba medaļas ieguvēja apzīmējums ir redzams attiecīgā darba kandidātu sarakstā, kā arī kandidātu kopas skatā, kad šie kandidāti ir dalībnieki jebkurā personāla atlases darbinieka vai par pieņemšanu darbā atbildīgā vadītāja kopā. Turklāt šis apzīmējums ir redzams arī darbu vēsturē kā daļa no kandidātu kopas profila šim kandidātam. Šo līdzekli varat priekšskatīt, ja administrators to ieslēdz, izmantojot norādījumus rakstā [Līdzekļu pārvaldība administrēšanas centrā](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="add-applicants-to-talent-pools"></a>Kandidātu pievienošana kandidātu kopām
Tagad kandidātu pievienošana talantu kopām ir vienkāršāka, izsaucot jaunu darbību kandidātu sarakstā. Atlasot ikonu **Pievienot kandidātu kopai**, personāla atlases darbinieks vai par pieņemšanu darbā atbildīgais vadītājs var izvēlēties no sava kandidātu kopu saraksta un kandidātus vienkārši pievienot kandidātu kopām tieši no darba kandidātu saraksta.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Konfigurēšana, vai ir nepieciešams CV, lai pieteiktos noteiktam darbam
Pamatojoties uz klientu atsauksmēm, personāla atlases darbinieki tagad var konfigurēt, vai ir nepieciešams CV augšupielādēta faila formā, lai pieteiktos konkrētam darbam. Šī konfigurācija veido daļu no pieteikuma aktivitātes, kura ir pieejama darbā pieņemšanas procesā. Ja tā ir aktivizēta, visiem potenciālajiem kandidātiem tiek aicināts augšupielādēt CV, kad viņi piesakās šim amatam. Pieteikums tiks uzskatīts par pilnīgu tikai tad, ja ir augšupielādēts CV. Tas palīdz mazināt troksni kandidātu kopā, nodrošinot, ka katrs kandidāts sniedz pietiekamu informāciju, lai personāla atlases darbinieks varētu viņus izskatīt.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Kandidāti var pieteikties darbam, izmantojot savu LinkedIn profilu
Kandidāti, kuriem viņu aktuālais profils jau ir pakalpojumā LinkedIn, darbiem var pieteikties tikai ar vienu klikšķi, izmantojot šo profilu.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Izsekošana, kā kandidāta profils sistēmā radās un kur jūsu kandidāti atrada darbus, kuriem viņi piesakās
Tagad varat noskaidrot, kā programmā Attract radās konkrēts kandidāta profils, apskatot profila avotu kandidāta detalizētajā informācijā, pieteikuma lapā **Profils**, vai kandidātu kopas profilā. Līdzīgi varat arī noskaidrot, kā jebkurš kandidāts atrada attiecīgo darbu, apskatot pieteikuma avotu, kurš ir redzams pieteikuma aktivitātes plūsmas sadaļā **Pieteikuma aktivitāte**. Šī informācija ir pieejama arī kandidātu kopas profila darbu vēsturē. Kad darbinieku atlases speciālisti vai par pieņemšanu darbā atbildīgie vadītāji kandidātus pievieno manuāli, viņiem tiek parādīts aicinājums norādīt pieteikuma vai kandidāta profila avotu. Kad kandidāts piesakās pirmo reizi, viņa profila avots ir vienāds ar kandidāta pieteikuma izcelsmi. Šo līdzekli varat priekšskatīt, ja administrators to ieslēdz, izmantojot norādījumus rakstā [Līdzekļu pārvaldība administrēšanas centrā](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature). Ievērojiet, ka esošajiem kandidātiem nav nekādas avota informācijas. Taču darbinieku atlases speciālisti šo informāciju var pievienot manuāli.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attract integrācija pieteikumiem parāda dublēta ieraksta kļūdu
Šajā atjauninājumā ir novērsta problēma ar dublētiem ierakstiem. Šī problēma rodas, atverot darbvietu **Personāla pārvaldība**.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Nevar aizvērt formu, rediģējot nosaukumu secību
Ir veiktas izmaiņas, lai izlabotu problēmu, kad tiek rediģēta nosaukumu secība nodarbinātā formā.

## <a name="coming-soon"></a>Drīzumā

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Papildu atlīdzības drošība (fiksētā un mainīgā)
Daudzās organizācijās atlīdzību un atvieglojumu pārvaldnieki var piekļūt tikai noteiktiem atlīdzības ierakstiem. Piemēram, tie varētu būt par vadītājiem vai reģionālajiem darbiniekiem. Šīs izmaiņas dod iespēju personāla vadībai pārvaldīt un uzturēt atlīdzības plānus dažādām darbinieku grupām organizācijā. Fiksētajiem un mainīgajiem plāniem var piešķirt drošības lomas, kuras nosaka piekļuvi plāniem un ar šiem plāniem saistītajiem darbinieku datiem, piemēram, algu vai prēmiju ierakstiem. Atlīdzību šiem darbiniekiem var apstrādāt tikai lietotāji, kuriem ir lomas ar piešķirtu piekļuvi.

###  <a name="email-support-for-alerts"></a>E-pasta atbalsts brīdinājumiem
Līdz ar platformas atjauninājumu 24 Finance and Operations ieviešanu lietotāji var izveidot brīdinājumu kārtulas, kas automātiski nosūta e-pasta paziņojumus kontaktpersonām, ja kāds notikums tās aktivizē.

### <a name="duplicate-employee-check-interface-changes"></a>Dublētu darbinieku pārbaude: interfeisa izmaiņas
Līdz ar šīs izmaiņas ieviešanu dublikāti tiek noteikti, kad aizpildāt vārda/uzvārda/nosaukuma laukus, un statuss parāda atrasto dublikātu skaitu. Varat atlasīt norādīto saiti, lai atvērtu jaunu lapu, kur novērtēt, vai atrastā atbilstība ir jāizmanto. Dublikātu forma netiek atvērta automātiski, lai izvairītos no datu ievades pārtraukšanas.


