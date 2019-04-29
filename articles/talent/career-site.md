---
title: Karjeras vietnes funkcionalitāte programmā Attract
description: Šajā tēmā ir sniegts apskats par kandidātu karjeras vietnes funkcionalitāti programmā Attract.
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: a56f162ccc6b6099fd62e0cb7e10076368d8e653
ms.sourcegitcommit: 063a9296e645e0da182241941869d8102954540a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/26/2019
ms.locfileid: "898935"
---
# <a name="career-site-functionality-in-attract"></a>Karjeras vietnes funkcionalitāte programmā Attract

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegts apskats par kandidātu karjeras vietnes funkcionalitāti programmā Microsoft Dynamics 365 for Talent: Attract. Tajā arī ir paskaidrots, kā iestatīt šo funkcionalitāti.

Attract nodrošina vienu karjeras vietni katrai nomnieka videi. Piemēram, ja organizācijai ir izstrādes vide un testēšanas vide, viena karjeras vietne ir paredzēta izstrādes videi un otra karjeras vietne ir paredzēta testēšanas videi. Katra karjeras vietne ir pilnībā izolēta, un tām ir savs autentifikācijas mehānisms. Darbi un kandidātu profili netiek kopīgoti starp karjeras vietnēm.

Pēc noklusējuma karjeras vietne ir publiska. Tāpēc kandidāti nepierakstoties var skatīt visus darbus, kas atzīmēti kā ārēji. Tomēr, lai veiktu pārējās darbības, kandidātiem ir jāpierakstās.

## <a name="career-site-management"></a>Karjeras vietnes pārvaldība

Lai iestatītu vērtības tālāk minētajiem vienumiem, pierakstieties programmā Attract kā administrators, izvēlnē **Iestatījumi** (zobrata simbols) atlasiet vienumu **Administrēšanas centrs** un pēc tam atlasiet cilni **Uzņēmuma informācija**.

-   **Organizācijas nosaukums** — organizācijas nosaukums parādās navigācijas joslā karjeras vietnes augšdaļā. Atlasot organizācijas nosaukumu, kandidāti pāriet uz lapu, kurā norādīti visi atvērtie darbi.

-   **Organizācijas logotips** — organizācijas logotipa attēls parādās karjeras vietnes augšējā kreisajā stūrī. Atlasot organizācijas logotipa attēlu, kandidāti pāriet uz lapu, kurā norādīti visi atvērtie darbi.

    > [!NOTE] 
    > Logotipa attēlam, kas parādās karjeras vietnē, ir fiksēts augstums 20 pikseļi (px). Attēls, ko pievienojat administrēšanas centrā, tiek mērogots atbilstoši vajadzīgajam izmēram. Tāpēc atkarībā no attēla platums var mainīties.
 
Lai iestatītu vērtības tālāk minētajiem vienumiem, pierakstieties programmā Attract kā administrators, izvēlnē **Iestatījumi** atlasiet vienumu **Administrēšanas centrs** un pēc tam atlasiet cilni **Karjeras vietnes pārvaldība**.

-   **Meklētājoptimizācija** — ja šis vienums ir iespējots, visus publiskos darbus, kas publicēti Attract karjeras vietnē, varēs atrast, izmantojot meklētājprogrammas, piemēram, Bing un Google.

    > [!NOTE] 
    > Var būt aizkave starp šī iestatījuma ieslēgšanu un meklēšanas rezultātu parādīšanu atkarībā no izmantotajām meklētājprogrammām.
         
## <a name="career-site-urls"></a>Karjeras vietnes vietrāži URL

Tālāk minēti bieži lietotie karjeras vietnes vietrāži URL un tas, kā tiem piekļūt.

-   **Karjeras vietnes sākumlapas vietrādis URL** — lai skatītu karjeras vietnes sākumlapas vietrādi URL, pierakstieties programmā Attract kā administrators, atlasiet vienumu **Administrēšanas centrs** izvēlnē **Iestatījumi** un pēc tam atlasiet cilni **Karjeras vietnes pārvaldība**.

-   **Atsevišķa darba sludinājuma pieteikuma vietrādis URL** — kad pirmo reizi [publicējat ārējo darbu](Creating-jobs-Attract.md#postings), jūs varat kopēt saiti **Pieteikties** no programmas Attract. Šīs saites vietrādis URL būs šādā formātā: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **Atsevišķa darba sludinājuma vietrādis URL** — darba sludinājuma vietrādis URL ir pieteikšanās vietrāža URL apakšvirkne. To veido visi elementi līdz darba numuram. Tādējādi iepriekšējam pieteikšanās vietrādim URL darba sludinājuma vietrādis URL ir [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)

## <a name="authentication-options"></a>Autentifikācijas opcijas

Kandidātiem ir pieejamas šādas pierakstīšanās opcijas Attract karjeras vietnē.

-   Personiskais konts:

    -   LinkedIn

    -   Microsoft 

    -   Google

    -   Facebook

-   Darba vai mācību konts:

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD pierakstīšanās ir paredzēta tikai iekšējiem kandidātiem. Tāpēc to var lietot tikai iekšējie kandidāti, kuri izmanto attiecīgā uzņēmuma Azure AD akreditācijas datus. Piemēram, kandidāts, kas pašlaik ir Contoso Ltd darbinieks, vēlas pieteikties darbam nesaistītā uzņēmumā Alpine Ski House. Šajā gadījumā pierakstīšanās būs neveiksmīga, ja darbinieks mēģina lietot savus Azure AD akreditācijas datus no Contoso Ltd. 

Kandidātiem jāpiesakās, izmantojot Azure AD, ja darbs, kuru viņi skata vai kuram viņi piesakās, ir norādīts kā tikai iekšējs.

## <a name="create-and-maintain-a-profile"></a>Profila izveide un uzturēšana

Pēc kandidātu pierakstīšanās karjeras vietnē viņi var atlasīt **Mans profils** navigācijas joslā lapas augšdaļā, lai izveidotu un uzturētu savu profilu.
Profils ietver personisko informāciju, informāciju par darba pieredzi, izglītības informāciju, dokumentus, saites un informāciju par prasmju kopām. Pēc tam, kad profils ir izveidots, to var izmantot, lai pieteiktos kandidātu interesējošiem darbiem. Profili arī palīdz programmai Attract ieteikt kandidātiem piemērotus darbus.

> [!NOTE]
> Ja kandidāts izmanto e-pasta ID, lai pierakstītos, lietojot kādu no iepriekš minētajiem autentifikācijas nodrošinātājiem, minētais e-pasta ID tiks atiestatīts uz kontaktpersonas e-pasta ID, kas saistīts ar attiecīgo profilu. Tomēr kontaktpersonas e-pasta ID var mainīt jebkurā laikā, un tas ir pilnīgi neatkarīgs no e-pasta ID. Programma Attract vienmēr izmantos kontaktpersonas e-pasta ID, kas tiks saistīts ar jūsu profilu, visiem e-pasta ziņojumiem.

## <a name="find-the-right-job"></a>Piemērota darba atrašana

Darbu saraksta lapā kandidāti var meklēt konkrētu darbu, ievadot meklējamos vārdus. Meklēšanas funkcionalitāte veic meklējamo vārdu meklēšanu amatu nosaukumos un darba aprakstos un rezultātos parāda atbilstīgos darbus. Kandidāti var filtrēt rezultātus jebkurā laikā, pamatojoties uz darba atrašanās vietu vai darba funkciju.

Kandidāti var apskatīt arī ieteikto darbu kopu karjeras vietnē. Kandidātam ieteiktie darbi balstās uz kandidāta iepriekšējiem pieteikumiem, profilu un CV.

> [!NOTE] 
> Darba ieteikumi tiek rādīti tikai tad, ja karjeras vietnē ir publicēti vismaz 10 darbi un ja kandidāts ir aizpildījis savu profilu.

Iekšējie kandidāti var arī redzēt, kurš ir katra darba par pieņemšanu darbā atbildīgais vadītājs un/vai personāla atlases darbinieks, ja viņi vēlas sazināties ar šiem darbā pieņemšanas grupas dalībniekiem. Tomēr ārējie kandidāti nevienam darbam nevar skatīt darbā pieņemšanas grupu.

## <a name="contact-the-hiring-team"></a>Sazināties ar darbā pieņemšanas grupu
Tikai iekšējie kandidāti var sazināties ar darbā pieņemšanas grupu. Šis ierobežojums attiecas uz visiem darbiem neatkarīgi no tā, vai tie ir tikai iekšēji vai izlikti publiskai apskatei.

Kandidāti var vēlēties sazināties ar darbā pieņemšanas grupu, lai paustu interesi par publiskoto darbu vai uzzinātu par to vairāk. Viņi var sazināties ar jebkuru darbā pieņemšanas grupas dalībnieku, kurš ir uzskaitīts (par pieņemšanu darbā atbildīgais vadītājs vai personāla atlases darbinieki). Viņi pēc izvēles var arī pievienot ziņojumam CV vai atlasīt esošu CV, kuru viņi iepriekš augšupielādējuši kā daļu no sava profila.

Pēc tam, kad iekšējais kandidāts atlasa darbā pieņemšanas grupas dalībniekus, ar kuriem sazināties, Attract nosūta e-pasta ziņojumu šīm personām kandidāta vārdā. Vienlaikus kandidāta profils tiek pievienots posmam **Potenciālais klients**, ja šis posms darbam ir pieejams. Posmā **Potenciālais klients** personāla atlases darbinieki vai par darbā pieņemšanu atbildīgie vadītāji var skatīt kandidātus, kuri ir sazinājušies ar viņiem. Viņi var arī pārskatīt kandidātu profilus un aicināt potenciālos kandidātus pieteikties.

Kandidāti var pieteikties darbam, par kuru viņi jau ir sazinājušies ar darbā pieņemšanas grupas dalībniekiem. Pēc pieteikšanās kandidāti vairs nevar sazināties ar darbā pieņemšanas grupu, izmantojot karjeras vietni.

## <a name="apply-for-jobs"></a>Pieteikšanās darbiem

Pēc tam, kad kandidāti ir atraduši piemērotu darbu, viņi var pieteikties, izmantojot pogu **Pieteikties** lapā **Darba informācija**. Šajā brīdī kandidāti var izveidot jaunu profilu vai pārskatīt informāciju savā esošajā profilā.
Ja nepieciešams, kandidāti var arī augšupielādēt CV un pēc tam iesniegt darba pieteikumu.

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a>Pieteikšanās iespējošana darbiem, izmantojot LinkedIn profilus

Varat atvieglo kandidātiem pieteikšanos jūsu amatiem, konfigurējot Attract tā, lai viņi varētu pieteikties, izmantojot LinkedIn.

> [!NOTE] 
> Jums nepieciešama viena vai vairākas personāla atlases darbinieka licences no LinkedIn, pirms varat atļaut kandidātiem pieteikties, izmantojot LinkedIn.

1. Piesakieties pakalpojumā Attract kā administrators.
2. Atlasiet pogu **Iestatījumi** (zobrata simbols) lapas labās puses augšējā stūrī un pēc tam atlasiet **Administrēšanas centrs**.
3. Atlasiet cilni **LinkedIn integrācija** un izveidojiet savienojumu ar LinkedIn personāla atlases darbinieka kontu.
4. Sadaļā **LinkedIn Recruiter System Connect integrācija** iestatījumam **Pieteikties, izmantojot LinkedIn** atlasiet opciju **Iespējots**.

Pēc tam, kad iestatījums ir iespējots, kandidāti var pieteikties, izmantojot viņu esošā LinkedIn profila datus. Ja kandidāti piesakās, izvēloties pogu **Pieteikties, izmantojot LinkedIn**, viņi tiek aicināti autentificēties ar LinkedIn, ja viņi vēl nav pieteikusies. Pēc tam, kad viņi ir autentificēti, viņu LinkedIn profils aizstāj visus esošos profila datus, kas redzami pieteikuma lapā. Kandidāti var rediģēt informāciju pēc nepieciešamības un pēc tam iesniegt pieteikumu. Ja kandidāts pāriet prom no lapas, nepiesakoties darbam, viņa profila dati netiek atjaunināti programmā Attract.

## <a name="check-application-status"></a>Pieteikuma statusa pārbaude

Pēc tam, kad kandidāti piesakās vienam vai vairākiem darbiem, viņi var atlasīt vienumu **Pieteikumi** navigācijas joslā lapas augšdaļā, lai skatītu savus atvērtos un slēgtos pieteikumus. Kad kandidāti atver kādu no saviem pieteikumiem, viņi redz pašreizējo posmu un veicamās darbības. Piemēram, ja kandidātam ir jānorāda iespējamie datumi intervijai klātienē, lapā ir parādītas pieejamās iespējas.

## <a name="internal-jobs"></a>Iekšējie darbi

Pašlaik darbi, kas ir atzīmēti kā iekšējie darbi un publicēti Attract karjeras vietnē, netiek parādīti karjeras vietnē. Tie ir pieejami, izmantojot tiešo vietrādi URL **Pieteikties**, ko var kopēt no programmas Attract.
