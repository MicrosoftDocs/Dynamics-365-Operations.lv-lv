---
title: Integrācijas ar LinkedIn iestatīšana programmai Microsoft Dynamics 365 Talent - Attract
description: Šajā tēmā ir paskaidrots, kā konfigurēt LinkedIn integrāciju programmai Microsoft Dynamics 365 Talent - Attract, lai jūs varētu viegli publicēt darbus LinkedIn no Attract, un lai jūsu personāla atlases speciālisti varētu sinhronizēt savu darbinieku atlases informāciju ar kandidāta LinkedIn profilu.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6b86cafdf364f2de051f3d8ceab7413c2c13c3a5
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009974"
---
# <a name="set-up-linkedin-integration"></a>LinkedIn integrācijas iestatīšana

[!include[banner](../includes/banner.md)]

Palīdziet saviem darba devējiem un darbā pieņemšanas vadītājiem piesaistīt augstākā līmeņa talantu, konfigurējot LinkedIn integrāciju ar programmu Microsoft Dynamics 365 Talent: Attract. Attract ļauj publicēt darbus tieši uzņēmumā LinkedIn, kas ir lielākais profesionālais tiešsaistes tīkls.

Darbi, kurus publicējat pakalpojumā LinkedIn, izmantojot programmu Attract, ir ierobežoti ieraksti un tiek nodrošināti jūsu uzņēmumam bez papildu izmaksām. Šie saraksti ir pieejami tikai ar LinkedIn programmatūras partneru, piemēram, Attract starpniecību. Tie netiek parādīti panelī **Karjeras** jūsu uzņēmuma LinkedIn lapā, jo tajā tiek rādīti tikai maksas saraksti. Tomēr tie tiek parādīti, kad potenciālie kandidāti skata visus pieejamos darbus. Ierobežotie saraksti tiek rādīti arī LinkedIn darbu meklēšanā.

Attract nodrošina divus veidus integrācijai ar LinkedIn, lai palīdzētu jums piesaistīt kandidātus no šīs populārās karjeras vietnes.

- Vakanču publicēšana no pakalpojuma Attract vietnē LinkedIn.
- Piesaistīt kandidātus no LinkedIn pakalpojumam Attract.

Konfigurējiet abas opcijas cilnē **LinkedIn integrācija** Administrēšanas centrā. Lai atvērtu Administrēšanas centru, dodieties uz <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> Lai izmantotu LinkedIn Recruiter integrāciju ar Attract, ir nepieciešams [Visaptverošais darbā pieņemšanas papildinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) un [LinkedIn Recruiter licences](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Papildinformāciju skatiet rakstā [Kura Attract versija?](./attract-comprehensive-hiring.md).

Ja rodas problēmas, publicējot darbus LinkedIn, skatiet sadaļu [Problēmu novēršana integrācijā ar LinkedIn](./attract-troubleshoot-linkedin.md).

Informāciju par citiem veidiem, kā publicēt darbus LinkedIn, skatiet sadaļā [LinkedIn bieži uzdotie jautājumi](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>Darbu publicēšanas LinkedIn konfigurēšana

Lai varētu publicēt darbus no Attract vietnē LinkedIn, ir nepieciešams [LinkedIn uzņēmuma ID.](https://aka.ms/findID) LinkedIn uzņēmuma ID ir skaitļu virkne, kas unikāli identificē jūsu uzņēmumu vietnē LinkedIn. Papildinformāciju skatiet sadaļā [LinkedIn uzņēmuma ID sasaiste ar LinkedIn darba paneli — bieži uzdotie jautājumi ](https://aka.ms/findID).

Attract sūta jūsu darbu sludinājumus uz LinkedIn, un LinkedIn pārbauda plūsmu aptuveni reizi dienā. Var paiet līdz pat 48 stundām, līdz jūsu darbi tiks publicēti vietnē.

Darbi, kas publicēti LinkedIn, ir redzami reāllaika LinkedIn vietnē. LinkedIn nav testēšanas vides darbu publicēšanai. Tāpēc pārliecinieties, vai nejauši nepublicējat nevienu testa darbu. 

1. Augšējā labajā stūrī, izvēlnē **Iestatīšana** (zobrata simbols) atlasiet **Administrēšanas centrs**. Vai arī dodieties uz <https://attract.talent.dynamics.com/adminsettings>.
2. Atlasiet cilni **LinkedIn integrācija**.
3. Sadaļā **Uzņēmuma nosaukums** ievadiet sava uzņēmuma nosaukumu un sadaļā **Uzņēmuma ID** ievadiet savu LinkedIn uzņēmuma ID. Pārliecinieties, ka uzņēmuma nosaukums sakrīt ar uzņēmuma LinkedIn lapā parādīto nosaukumu. Papildinformāciju par LinkedIn uzņēmuma ID skatiet rakstā [LinkedIn uzņēmuma ID sasaiste ar LinkedIn darba paneli — bieži uzdotie jautājumi](https://www.linkedin.com/help/linkedin/answer/98972).

    Ja jums ir jāmaina jebkāda informācija par jūsu organizāciju, skatiet sadaļu [Organizācijas adreses, tehniskās kontaktpersonas un citas informācijas mainīšana](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Ja joprojām pastāv problēmas, sazinieties [ar LinkedIn atbalsta dienestu](https://www.linkedin.com/help/linkedin).

4. Atlasiet **Saglabāt**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>LinkedIn Recruiter iestatīšana ar Attract 

Lai darba devēji varētu veikt atlases darbus, izmantojot LinkedIn Recruiter, ir jākonfigurē integrācija ar LinkedIn Recruiter pakalpojumā Attract. Lai pabeigtu konfigurēšanas procesu, ir jāizmanto lietotāja konts, kas jūsu organizācijas LinkedIn Recruiter līgumā ir norādīts kā administrators.

1. Augšējā labajā stūrī, izvēlnē **Iestatīšana** (zobrata simbols) atlasiet **Administrēšanas centrs**. Vai arī dodieties uz <https://attract.talent.dynamics.com/adminsettings>.
2. Atlasiet cilni **LinkedIn integrācija**.

    [![Attract administratora skats, kurā var sākt LinkedIn Recruiter integrāciju](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Atlasiet **Izveidot savienojumu**, lai sāktu iestatīšanu. Jūs tiksit vadīts cauri LinkedIn pierakstīšanās procesam.
4. Ja jums ir vairāku LinkedIn līgumu licences, atlasiet to līgumu, kam vēlaties izveidot savienojumu ar sistēmu Attract. Ja jums ir tikai viena LinkedIn līguma licence, šo darbību varat izlaist.
5. Sadaļā **Recruiter System Connect (RSC)** atlasiet **Pieprasīt**.

    [![Attract administratora skats, kurā var pieprasīt LinkedIn Recruiter integrāciju](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. **Recruiter System Connect (RSC)** iestatījumam tagad jābūt redzamam kā **Gatavs partnerim**. Ja šajā lapā tiek rādīts statuss **Paziņot partnerim**, uzgaidiet pāris sekundes, atlasiet **Paziņot partnerim** un pēc tam atsvaidziniet lapu. Iestatījumam tagad ir jāparādās kā **Gatavs partnerim**.

    [![Attract administratora skats, kurā var norādīt Attract, ka sistēmā Attract ir pabeigtas pieprasījumu iesniegšanas darbības](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Lai pabeigtu nākamās darbības, ir nepieciešamas administratora privilēģijas, kas ir piešķirtas LinkedIn Recruiter līgumā.

    1. Pierakstieties LinkedIn, izmantojot savu administratora kontu, un pēc tam augšējā labajā stūrī atlasiet **LinkedIn Recruiter**. 
    2. Lapas augšdaļā esošajā izvēlnē **Vairāk** atlasiet **Administratora iestatījumi** un pēc tam natlasiet cilni **ATS**.
    3. Lai iespējotu viena klikšķa eksportēšanu tikai uz vienam līgumam, ieslēdziet opciju **Līguma līmeņa piekļuve (katrai vietai šajā līgumā)**. Lai to iespējotu visam uzņēmumam, ieslēdziet opciju **Uzņēmuma līmeņa piekļuve (katram līgumam jūsu uzņēmumā)**.

    [![Attract integrācijas ieslēgšana LinkedIn Recruiter administratora skatā](./media/EnableRSC.png)](./media/EnableRSC.png)

8. Attract Administrēšanas centrā atlasiet cilni **LinkedIn integrācija.** Tagad iestatījumam **Recruiter System Connect (RSC)** jātiek parādītam kā **Iespējots**.

    [![LinkedIn Recruiter integrācija ir pabeigta](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Piesakies ar LinkedIn iestatīšana programmā Attract

Varat atļaut kandidātiem pieteikties jūsu darbiem, izmantojot viņu LinkedIn profilus. Papildinformāciju par Piesakies ar LinkedIn skatiet [LinkedIn iespējas visur: Piesakies ar LinkedIn ](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Šis līdzeklis pašreiz ir priekšskatījumā. Pirms šo darbību veikšanas pārliecinieties, vai ir iespējota opcija Piesakies ar LinkedIn. Papildinformāciju par to, kā iespējot priekšskatījuma līdzekļus, skatiet rakstā [Piekļuve priekšskatījuma līdzekļiem programmā Talent](./access-preview-feature.md).

1. Augšējā labajā stūrī, izvēlnē **Iestatīšana** (zobrata simbols) atlasiet **Administrēšanas centrs**. Vai arī dodieties uz <https://attract.talent.dynamics.com/adminsettings>.
2. Atlasiet cilni **LinkedIn integrācija**.

    [![Attract administratora skats, kurā var sākt LinkedIn Recruiter integrāciju](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Blakus **Piesakies ar LinkedIn** atlasiet **Izveidot savienojumu**, lai sāktu iestatīšanu. Jūs tiksit vadīts cauri pārējam procesam ar LinkedIn.

## <a name="see-also"></a>Skatiet arī

[LinkedIn bieži uzdotie jautājumi](./attract-linkedin-faq.md)

[Darbu grāmatošana ārējās vietnēs no sistēmas Attract](./posting-jobs-external.md)

[SKandidātu piesaiste, izmantojot LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[Izveidot darbus](./creating-jobs-attract.md)

[Integrācijas ar LinkedIn problēmu novēršana](./attract-troubleshoot-linkedin.md)
