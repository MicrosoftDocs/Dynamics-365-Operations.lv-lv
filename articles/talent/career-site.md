---
title: "Karjeras vietnes funkcionalitāte programmā Attract"
description: "Šajā rakstā ir sniegts apskats par kandidātu karjeras vietnes funkcionalitāti programmatūrā Microsoft Dynamics 365 for Talent - Attract. Tajā arī ir paskaidrots, kā iestatīt šo funkcionalitāti."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: lv-lv
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Karjeras vietnes funkcionalitāte programmā Attract

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegts apskats par kandidātu karjeras vietnes funkcionalitāti programmatūrā Microsoft Dynamics 365 for Talent: Attract. Tajā arī ir paskaidrots, kā iestatīt šo funkcionalitāti.

## <a name="overview"></a>Pārskats

Attract nodrošina vienu karjeras vietni katrai nomnieka videi. Piemēram, ja organizācijai ir izstrādes vide un testēšanas vide, viena karjeras vietne ir paredzēta izstrādes videi un otra karjeras vietne ir paredzēta testēšanas videi. Katra karjeras vietne ir **pilnībā izolēta**, un tām ir savs autentifikācijas mehānisms. Darbi un kandidātu profili netiek kopīgoti starp karjeras vietnēm.

Pēc noklusējuma karjeras vietne ir publiska. Tāpēc kandidāti nepierakstoties var skatīt visus darbus, kas atzīmēti kā ārēji. Tomēr, lai veiktu pārējās darbības, kandidātiem ir jāpierakstās.

## <a name="career-site-management"></a>Karjeras vietnes pārvaldība

Iestatījumi kontrolē šādus karjeras vietnes vienumus.

- **Organizācijas nosaukums:** organizācijas nosaukums parādās navigācijas joslā karjeras vietnes augšdaļā. Atlasot organizācijas nosaukumu, kandidāti pāriet uz lapu, kurā norādīti visi atvērtie darbi.
- **Organizācijas logotips:** organizācijas logotipa attēls parādās karjeras vietnes augšējā kreisajā stūrī. Atlasot organizācijas logotipa attēlu, kandidāti pāriet uz lapu, kurā norādīti visi atvērtie darbi.

Lai iestatītu vērtības tādiem vienumiem kā organizācijas nosaukums un logotips, pierakstieties programmā Attract kā administrators, izvēlnē **Iestatījumi** (zobrata simbols) atlasiet vienumu **Administrēšanas centrs** un pēc tam atlasiet cilni **Uzņēmuma informācija**.

> [!NOTE]
> Logotipa attēlam, kas parādās karjeras vietnē, ir fiksēts augstums 20 pikseļi (px). Attēls, ko pievienojat administrēšanas centrā, tiek mērogots atbilstoši vajadzīgajam izmēram. Tāpēc atkarībā no attēla platums var mainīties.

## <a name="career-site-url"></a>Karjeras vietnes vietrādis URL

Kad pirmo reizi [publicējat ārējo darbu](./Creating-jobs-Attract.md#postings), jūs varat kopēt saiti **Pieteikties** no programmas Attract. Šīs saites vietrādis URL būs šādā formātā: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

Karjeras vietnes vietrādis URL ir vietrāža URL **Pieteikties** apakšvirkne. To veido visi elementi līdz uzņēmuma nosaukumam. Tāpēc iepriekšējam vietrādim URL **Pieteikties** karjeras vietnes vietrādis URL ir `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Autentifikācija opcijas

Kandidātiem ir pieejamas šādas pierakstīšanās opcijas Attract karjeras vietnē.

- Personiskais konts:

    - LinkedIn
    - Microsoft 
    - Google
    - Facebook

- Darba vai mācību konts:

    - Microsoft Azure Active Directory (Azure AD)

Azure AD pierakstīšanās ir paredzēta tikai iekšējiem kandidātiem. Tāpēc to var lietot tikai iekšējie kandidāti, kuri izmanto attiecīgā uzņēmuma Azure AD akreditācijas datus. Piemēram, kandidāts, kas pašlaik ir Contoso Ltd darbinieks, vēlas pieteikties darbam nesaistītā uzņēmumā Alpine Ski House. Šajā gadījumā pierakstīšanās būs neveiksmīga, ja darbinieks mēģina lietot savus Azure AD akreditācijas datus no Contoso Ltd.

## <a name="create-and-maintain-a-profile"></a>Profila izveide un uzturēšana

Pēc kandidātu pierakstīšanās karjeras vietnē viņi var atlasīt **Mans profils** navigācijas joslā lapas augšdaļā, lai izveidotu un uzturētu savu profilu. Profils ietver personisko informāciju, informāciju par darba pieredzi, izglītības informāciju, dokumentus, saites un informāciju par prasmju kopām. Pēc tam, kad profils ir izveidots, to var izmantot, lai pieteiktos kandidātu interesējošiem darbiem. Profili arī palīdz programmai Attract ieteikt kandidātiem piemērotus darbus.

## <a name="find-the-right-job"></a>Piemērota darba atrašana

Darbu saraksta lapā kandidāti var meklēt konkrētu darbu, ievadot meklējamos vārdus. Meklēšanas funkcionalitāte veic meklējamo vārdu meklēšanu amatu nosaukumos un darba aprakstos un rezultātos parāda atbilstīgos darbus. Kandidāti var filtrēt rezultātus jebkurā laikā, pamatojoties uz darba atrašanās vietu vai darba funkciju.

Kandidāti var apskatīt arī ieteikto darbu kopu karjeras vietnē. Kandidātam ieteiktie darbi balstās uz kandidāta iepriekšējiem pieteikumiem, profilu un CV.

> [!NOTE]
> Darba ieteikumi tiek rādīti tikai tad, ja karjeras vietnē ir publicēti vismaz 10 darbi un ja kandidāts ir aizpildījis savu profilu.

## <a name="apply-for-jobs"></a>Pieteikšanās darbiem

Pēc tam, kad kandidāti ir atraduši piemērotu darbu, viņi var pieteikties, izmantojot pogu **Pieteikties** darba informācijas lapā. Šajā brīdī kandidāti var izveidot jaunu profilu vai pārskatīt informāciju savā esošajā profilā. Ja nepieciešams, kandidāti var arī augšupielādēt CV un pēc tam iesniegt darba pieteikumu.

## <a name="check-application-status"></a>Pieteikuma statusa pārbaude

Pēc tam, kad kandidāti piesakās vienam vai vairākiem darbiem, viņi var atlasīt vienumu **Pieteikumi** navigācijas joslā lapas augšdaļā, lai skatītu savus atvērtos un slēgtos pieteikumus. Kad kandidāti atver kādu no saviem pieteikumiem, viņi redz pašreizējo posmu un veicamās darbības. Piemēram, ja kandidātam ir jānorāda iespējamie datumi intervijai klātienē, lapā ir parādītas pieejamās iespējas.

## <a name="internal-jobs"></a>Iekšējie darbi

Pašlaik, darbi, kas ir atzīmēti kā iekšējie darbi un publicēti Attract karjeras vietnē, netiek parādīti karjeras vietnē. Tie ir pieejami, tikai izmantojot tiešo vietrādi URL **Pieteikties**, ko var kopēt no programmas Attract.

