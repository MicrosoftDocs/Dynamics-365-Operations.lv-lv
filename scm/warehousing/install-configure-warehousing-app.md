---
title: "Microsoft Dynamics 365 for Operations &#8211; Warehousing instalēšana un konfigurēšana"
description: "Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt lietojumprogrammu Microsoft Dynamics 365 for Operations — Warehousing"
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

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Operations &#8211; Warehousing instalēšana un konfigurēšana

Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt lietojumprogrammu Microsoft Dynamics 365 for Operations — Warehousing

Dynamics 365 for Operations — Warehousing ir lietojumprogramma, kas ir pieejama Google Play veikalā un Windows veikalā. Pašreizējai Microsoft Dynamics 365 for Operations versijai šī programma tiek nodrošināta kā savrups komponents, tāpēc tā ir pašiem jāizvieto ierīcēs, kas tiek izmantotas noliktavas uzdevumu veikšanai. Lai varētu lietot šo programmu Dynamics 365 for Operations vidē, ir nepieciešams lejupielādēt programmu katrā lietotnē un konfigurēt to savienojuma izveidei ar Dynamics 365 for Operations vidi. Šajā tēmā ir aprakstīts, kā instalēt programmu ierīcēs. Tajā ir arī paskaidrots, kā konfigurēt programmu savienojuma izveidei ar Dynamics 365 for Operations vidi.

## <a name="prerequisites"></a>Priekšnosacījumi
Programma ir pieejama operētājsistēmās Android un Windows. Lai varētu lietot šo programmu, ierīcē ir jābūt instalētai kādai no tālāk norādītajām atbalstītajām operētājsistēmām. Jums ir jālieto arī kāda no tālāk norādītajām atbalstītajām Dynamics 365 for Operations versijām. Izmantojiet tālāk esošajā tabulā sniegto informāciju, lai novērtētu, vai aparatūras un programmatūras vide ir piemērota programmas instalēšanai.

| Platforma                    | Versija                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (visas versijas)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations versija 1611 vai Microsoft Dynamics AX versija 7.0/7.0.1 un Microsoft Dynamics AX 2. platformas atjauninājums ar labojumfailu KB 3210014 |

## <a name="get-the-app"></a>Iegūt programmu
-   Windows (UWP): [Dynamics 365 for Operations — Warehousing Windows veikalā](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android: [Dynamics 365 for Operations — Warehousing Google Play veikalā](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Active Directory
Lai programma varētu mijiedarboties ar noteiktu Dynamics 365 for Operations serveri, pakalpojumā Azure Active Directory ir jāreģistrē tīmekļa pakalpojuma lietojumprogramma Dynamics 365 for Operations nomniekam. Drošības apsvērumu dēļ ir ieteicams izveidot tīmekļa pakalpojuma lietojumprogrammu katrai izmantotajai ierīcei. Lai izveidotu tīmekļa pakalpojuma lietojumprogrammu pakalpojumā Azure Active Directory (Azure AD), veiciet tālāk norādītās darbības.

1.  Tīmekļa pārlūkprogrammā atveriet vietni <https://manage.windowsazure.com>.
2.  Ievadiet tā lietotāja vārdu un paroli, kurš var piekļūt Azure abonementam.
3.  Azure portāla kreisajā navigācijas rūtī noklikšķiniet uz **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Režģī atlasiet Active Directory instanci, kas tiek izmantota programmatūrā Dynamics 365 for Operations.
5.  Augšējā rīkjoslā noklikšķiniet uz **Lietojumprogrammas**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Apakšējā rūtī noklikšķiniet uz **Pievienot**. Tiek palaists vednis **Lietojumprogrammas pievienošana**.
7.  Ievadiet lietojumprogrammas nosaukumu un atlasiet **Tīmekļa lietojumprogramma un/vai tīmekļa API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Ievadiet pierakstīšanās URL, kas ir lietojumprogrammas URL jūsu nomniekā, Operations saknes URL. Pašlaik pierakstīšanās URL netiek aktīvi izmantots programmas autentifikācijai, taču tas ir obligāts lauks. Ievadiet to pašu URL laukā Programmas ID URI. [![wh-04-ad-add-properties](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Pārejiet uz cilni **Konfigurēšana**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Ritiniet uz leju līdz sadaļai **Atļaujas citām lietojumprogrammām**. Noklikšķiniet uz **Pievienot lietojumprogrammu**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Sarakstā atlasiet **Microsoft Dynamics ERP**. Noklikšķiniet uz atzīmes pogas **Pabeigt** lapas labajā stūrī. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Sarakstā **Deleģēt atļaujas** atzīmējiet visas izvēles rūtiņas. Noklikšķiniet uz **Saglabāt**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Pievērsiet uzmanību tālāk norādītajai informācijai.
    -   **Klienta ID** — ritinot lapu uz augšu, ir redzams lauks **Klienta ID**.
    -   **Atslēga** — sadaļā **Atslēgas** izveidojiet atslēgu, atlasot ilgumu, un kopējiet atslēgu. Vēlāk atslēga tiks saukta par **klienta noslēpumu**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Lietotāja konta izveide un konfigurēšana programmatūrā Dynamics 365 for Operations
Lai programmatūrā Dynamics 365 for Operations varētu izmantot jūsu Azure AD lietojumprogrammu, ir jāveic tālāk norādītās konfigurēšanas darbības.

1.  Pakalpojumā Azure Active Directory izveidojiet jaunu lietotāja kontu Dynamics 365 for Operations nomniekam. Šī konta mērķis ir piekļūt konkrētajam noliktavu programmas pielāgotajam pakalpojumam, ko nodrošina Dynamics 365 for Operations serveris. Pēc šīs darbības veikšanas jums ir pieejami WMDP lietotāja akreditācijas dati, kas sastāv no WMDP e-pasta adreses un WMDP paroles. Lai uzzinātu par pamata darbībām, kas ir jāveic, lai pievienotu lietotājus pakalpojumā Azure AD un programmatūrā Dynamics 365 for Operations, skatiet pamācību: [Reģistrācija Microsoft Dynamics 365 for Operations abonementam](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Izveidojiet Dynamics 365 for Operations lietotāju, kas atbilst noliktavu programmas lietotāja akreditācijas datiem.
    1.  Programmatūrā Dynamics 365 for Operations pārejiet uz sadaļu **Sistēmas administrēšana** &gt; **Vispārīgi** &gt; **Lietotāji**.
    2.  Izveidojiet jaunu lietotāju.
    3.  Piešķiriet lomu Noliktavas mobilās ierīces lietotājs, kā tas ir redzams tālāk esošajā ekrānuzņēmumā. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Saistiet savu Azure Active Directory lietojumprogrammu ar noliktavu programmas lietotāju.
    1.  Programmatūrā Dynamics 365 for Operations pārejiet uz sadaļu **Sistēmas administrēšana** &gt; **Iestatījumi** &gt; **Azure Active Directory lietojumprogrammas**.
    2.  Izveidojiet jaunu rindu.
    3.  Aizpildiet laiku **Klienta ID** (ievadot pēdējā sadaļā iegūto informāciju), piešķiriet nosaukumu un atlasiet iepriekš izveidoto lietotāju. Ir ieteicams atzīmēt visas ierīces, lai to nozaudēšanas gadījumā varētu viegli liegt to piekļuvi programmatūrai Dynamics 365 for Operations, izmantojot šo lapu. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Lietojumprogrammas konfigurēšana
Ierīcē instalētā programma ir jākonfigurē savienojuma izveidei ar Dynamics 365 for Operations serveri, izmantojot Azure AD lietojumprogrammu. Lai to paveiktu, veiciet tālāk norādītās darbības.

1.  Programmā pārejiet uz sadaļu **Savienojuma iestatījumi**.
2.  Noņemiet atzīmi no lauka **Demonstrācijas režīms**. [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Ievadiet tālāk norādīto informāciju. - **Azure Active Directory klienta ID** — klienta ID tiek iegūts, veicot 13. darbību sadaļā “Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Active Directory”. - **Azure Active Directory klienta noslēpums** — klienta noslēpums tiek iegūts, veicot 13. darbību sadaļā “Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Active Directory”. - **Azure Active Directory resurss** — Azure AD direktorija resurss atbilst Dynamics 365 for Operations saknes URL. **Piezīme**. Šī lauka vērtības beigās nedrīkst ievadīt uz priekšu vērstās slīpsvītras rakstzīmi (/). - **Azure Active Directory nomnieks** — Azure AD direktorija nomnieks, kas tiek izmantots ar Dynamics 365 for Operations serveri: https://login.windows.net/&lt;jūsu-AD-nomnieka-ID&gt;. Piemēram: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Piezīme**. Šī lauka vērtības beigās nedrīkst ievadīt uz priekšu vērstās slīpsvītras rakstzīmi (/). - **Uzņēmums** — ievadiet to juridisko personu programmatūrā Dynamics 365 for Operations, ar kuru ir jāveido lietojumprogrammas savienojums. [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Atlasiet pogu **Atpakaļ** lietojumprogrammas apakšējā kreisajā stūrī. Tagad lietojumprogrammā tiek izveidots savienojums ar Dynamics 365 for Operations serveri un parādīts noliktavas nodarbinātā pieteikšanās ekrāns. [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Ierīces piekļuves liegšana
Ja ierīce ir nozaudēta vai apdraudēta, ir jāliedz šīs ierīces piekļuve programmatūrai Dynamics 365 for Operations. Tālāk ir norādītas ieteicamā piekļuves liegšanas procesa darbības.

1.  Programmatūrā Dynamics 365 for Operations pārejiet uz sadaļu **Sistēmas administrēšana** &gt; **Iestatījumi** &gt; **Azure Active Directory lietojumprogrammas**.
2.  Dzēsiet rindu, kas atbilst ierīcei, kuras piekļuvi vēlaties liegt. Pierakstiet šīs ierīces parametra **Klienta ID** vērtību.
3.  Pierakstieties Azure klasiskajā portālā: <https://manage.windowsazure.com>.
4.  Noklikšķiniet uz ikonas **Active Directory** kreisās puses izvēlnē un pēc tam noklikšķiniet uz vajadzīgā direktorija.
5.  Augšējā izvēlnē noklikšķiniet uz **Lietojumprogrammas** un pēc tam noklikšķiniet uz lietojumprogrammas, ko vēlaties konfigurēt. Tiek parādīta lapa **Īsā pamācība**, kurā ir pieejama vienotās pieteikšanās un cita konfigurācijas informācija.
6.  Noklikšķiniet uz cilnes **Konfigurēšana**, ritiniet uz leju un pārliecinieties, ka lietojumprogrammas parametra **Klienta ID** vērtība ir vienāda ar vērtību, ko pierakstījāt, veicot 2. darbību šajā sadaļā.
7.  Noklikšķiniet uz komandjoslas pogas **Dzēst**.
8.  Apstiprinājuma ziņojumā noklikšķiniet uz **Jā**.



