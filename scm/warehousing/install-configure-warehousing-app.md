---
title: "Jāinstalē un jākonfigurē Microsoft Dynamics 365 Operations & #8211; Noliktavas"
description: "Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt Microsoft Dynamics 365 operācijām - noliktavas."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Jāinstalē un jākonfigurē Microsoft Dynamics 365 Operations & #8211; Noliktavas

Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt Microsoft Dynamics 365 operācijām - noliktavas.

Dinamika 365 operācijām - noliktavas ir programma, kas pieejama Google spēlēt veikalā un Windows krātuvē. Pašreizējā versijā Microsoft Dynamics 365 operācijām, šī app sniedz kā savrupajam komponentu, kas nozīmē sevis izvietošanu uz ierīcēm, ko izmanto noliktavas uzdevumus. Lai izmantotu Dynamics 365 app darbības vidi, jums lejupielādēt app par katru ierīci un konfigurēt tā, lai izveidotu savienojumu ar savu dinamiku 365 darbības vidi. Šajā tēmā aprakstīts, kā instalēt app jūsu ierīcē. Tajā paskaidrots arī, kā konfigurēt app, lai izveidotu savienojumu ar savu dinamiku 365 darbības vidi.

## <a name="prerequisites"></a>Priekšnosacījumi
App ir pieejami Android un Windows operētājsistēmās. Izmantot šo app, jums jābūt vienai no šādām atbalstāmajām operētājsistēmām instalēta jūsu ierīcē. Jums jābūt arī kādu no šīm atbalstītajām versijām Dynamics 365 operācijām. Izmantot informāciju tabulā novērtēt, ja aparatūras un programmatūras vide ir gatava atbalstīt instalāciju.

| Platforma                    | Versija                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | 10. Windows (visas versijas)                                                                                                                                                   |
| Dinamika 365 operācijām | Microsoft Dynamics 365 par operācijas 1611 - vai - Microsoft Dynamics Dynamics AX versija 7.0/7.0.1 un Microsoft Dynamics AX platformu atjaunināt 2 ar hotfix KB 3210014 |

## <a name="get-the-app"></a>Saņemt app
-   Windows (UWP) - [Dynamics 365 operācijām - noliktavas uz Windows krātuvē](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 operācijām - noliktavas Google spēlēt Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Active Directory izveidojiet web pakalpojumu lietojumprogrammu
Iespējot app mijiedarboties ar īpašu dinamiku 365 operācijas serverim, jums jāreģistrējas web pakalpojumu lietojumprogrammu Azure Active Directory Dynamics 365 par nomnieka darbību. Drošības apsvērumu dēļ mēs iesakām izveidot web pakalpojumu lietojumprogrammu, katrai ierīcei, ko lietojat. Lai izveidotu web pakalpojumu lietojumprogrammu Azure Active Directory (AD debeszils), veiciet sekojošās darbības:

1.  Web pārlūkprogrammā dodieties uz <https://manage.windowsazure.com>.
2.  Ievadiet nosaukumu un paroli, lietotājam, kurš piekļūst debeszils abonementu.
3.  Azure portālā, kreisajā navigācijas rūtī noklikšķiniet uz **Active Directory**. [](./media/wh-01-active-directory-example.png)[![wh-01-aktīvā direktorija-piemērs](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Režģī atlasiet Active Directory gadījumu, ko izmanto Dynamics 365 operācijām.
5.  Augšējā rīkjoslā noklikšķiniet uz **pieteikumus**. [![WH-02-aktīvā direktorija-pieteikumi](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Apakšējā rūtī noklikšķiniet uz **pievienot**. **Pievienot pieteikumu** vednis.
7.  Ievadiet nosaukumu pieteikums un izvēlieties **Web lietojumprogrammas un/vai web API**. [![WH-03-Active-Directory-ADD-Application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Ievadiet pieteikšanās URL, kas ir īrnieks, saknes URL operāciju pieteikums URL. Pierakstīšanās URL pašlaik netiek aktīvi izmantots, autentificējot app, bet ir obligāts lauks. Ievadiet to pašu URL laukā App ID URI. [![WH-04-reklāma-pievienot-rekvizīti](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Dodieties uz **Configure** tab. [![WH-05-reklāma-konfigurēt-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Ritiniet uz leju, līdz redzat **atļaujas citiem lietojumiem,** sadaļu. Noklikšķiniet uz **pievienot pieteikumu**. [![WH-06-ad-app-ADD-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Atlasiet **Microsoft Dynamics ERP** sarakstā. Noklikšķiniet uz **pabeigt pārbaudi** pogu labajā stūrī lapā. [![WH 07-reklāma-izvēlieties atļaujas](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Šajā **pārstāvja atļauju** sarakstu, atlasiet visas izvēles rūtiņas. Click **Save**. [![WH 08-reklāma-pārstāvja atļaujas](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Pierakstiet šādu informāciju:
    -   **Klienta ID** -, ritinot uz augšu lapā, jūs redzēsiet **klienta ID** parādīt.
    -   **Atslēga** - jo **atslēgas** iedaļā, izveidot atslēgu, atzīmējot laiku un kopēt taustiņu. Šī atslēga tiks vēlāk saukts par **klienta noslēpumu**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Izveidot un konfigurēt lietotāju kontu Dynamics 365 operācijām
Lai iespējotu Dynamics 365 operācijām izmantot debeszils reklāmas programmu, jums jāveic konfigurācijas šādi:

1.  Izveidot jaunu lietotāja kontu Azure Active Directory Dynamics 365 par nomnieka darbību. Šim lietotāja kontam mērķis ir piekļūt konkrētu pasūtījuma pakalpojumu noliktavas app, kas Dynamics 365 servera darbības apstākļos. Pabeidzot šo darbību, jums būs WMDP lietotāja akreditācijas datus, kas sastāv no WMDP e-pasta adresi un paroli WMDP. Uzzināt par pamatdarbības lietotāju pievienošana debeszils reklāmu un dinamiku 365 operācijām, atsaukties uz šo pamācību: [pierakstīties Microsoft Dynamics 365 periodiskām darbībām](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Izveidotu Dynamics 365 operācijas lietotājam, kas atbilst noliktavas app lietotāja akreditācijas datus.
    1.  Programmā Dynamics 365 operācijām, dodieties uz **sistēmas administrēšanu**&gt;**kopējo**&gt;**lietotājiem**.
    2.  Izveidot jaunu lietotāju.
    3.  Piešķiriet noliktavas mobilās ierīces lietotājam, kā redzams pēc screenshot. [![WH-09-Add-User-Security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Saistīt ar app lietotāja noliktavas Azure Active Directory lietojumprogrammu.
    1.  Programmā Dynamics 365 operācijām, dodieties uz **sistēmas administrēšanu**&gt;**Setup**&gt;**Azure Active Directory lietojumprogrammu**.
    2.  Izveidojiet jaunu rindu.
    3.  Ievadiet **klienta ID** (iegūta pēdējā sadaļā), piešķiriet tam nosaukumu un atlasiet iepriekš izveidoto lietotāju. Mēs iesakām tagu jūsu ierīces, jūs varētu viegli noņemt to piekļūšanu Dynamics 365 operācijas, lai no šīs lapas gadījumam, ja tās tiek nozaudētas. [![WH-10-reklāmas pieteikumi-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurēt programmu
Ierīcē, lai pieslēgtos Dynamics 365 operācijas serverim debeszils AD piemērojot jākonfigurē app. Lai to paveiktu, veiciet sekojošās darbības.

1.  App, dodieties uz **savienojuma uzstādījumus**.
2.  Skaidri **demonstrācijas režīms** lauks. [![WH-11-APP-Connection-Settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Ievadiet šādu informāciju:- **Azure Active directory klienta ID** -klienta ID tiek iegūta 13. solī "Create web lietojumprogrammu pakalpojums Active Directory". - **Azure aktīvā direktorija klienta noslēpumu** -klienta noslēpums iegūst "Create web lietojumprogrammu pakalpojums Active Directory" 13. solī. - **Azure Active directory resursam** -debeszils AD directory resursam attēlots Dynamics 365 operācijas saknes URL. **Piezīme**: nevar beigt šo lauku ar rakstzīmi uz priekšu vērstu slīpsvītru (/). - **Azure aktīvā direktorija īrnieks** -debeszils reklāmu direktorijs nomnieks izmanto ar Dynamics 365 operācijas serveri: https://login.windows.net/&lt;jūsu-AD-īrnieks-ID&gt;. Piemēram: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Piezīme**: nevar beigt šo lauku ar rakstzīmi uz priekšu vērstu slīpsvītru (/). - **Company** -juridiskajai personai ievadīt Dynamics 365 operācijām, kuram vēlaties, lai lietojumprogramma izveidot savienojumu. [![WH 12-app-savienojuma iestatījumus](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Atlasiet **atkal** pogu augšējā kreisajā stūrī pieteikumu. Pieteikums tagad savienos ar Dynamics 365, servera darbību un noliktavas strādniekam pieteikšanās ekrānā tiek parādīts. [![WH 13 pieteikšanās ekrānu](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Noņemt piekļuvi ierīcei
Gadījumā, ja nozaudēta vai apdraudēta ierīci, ir jānoņem piekļuvi Dynamics 365 operācijām attiecībā uz ierīci. Tālākminētajos soļos ir aprakstīts ieteicamo procesu, lai noņemtu piekļuvi.

1.  Programmā Dynamics 365 operācijām, dodieties uz **sistēmas administrēšanu**&gt;**Setup**&gt;**Azure Active Directory lietojumprogrammu**.
2.  Dzēst šo rindu, kas atbilst ierīces, kurā vēlaties noņemt piekļuvi. Pierakstiet **klienta ID** noņemto ierīci izmantot.
3.  Piesakieties debeszils klasiskās portālā pie <https://manage.windowsazure.com>.
4.  Noklikšķiniet uz **Active Directory** ikonu kreisajā izvēlnē un pēc tam noklikšķiniet uz vēlamo direktoriju.
5.  Augšējā izvēlnē noklikšķiniet uz **pieteikumus**, un pēc tam noklikšķiniet uz Attiecināšana, kuru vēlaties konfigurēt. **Quick Start** lappuse tiks rādīta ar vienotās pierakstīšanās un citu konfigurācijas informāciju.
6.  Noklikšķiniet uz **Configure** cilni, ritiniet uz leju un nodrošinātu, ka **klienta ID** pieteikums ir tas pats, kas šajā sadaļā 2. darbība.
7.  Noklikšķiniet uz **dzēst** komandjoslas pogas.
8.  Noklikšķiniet uz **Jā** apstiprinājuma ziņojumā.



