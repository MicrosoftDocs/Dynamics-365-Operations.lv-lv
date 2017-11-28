---
title: "Programmas Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing instalēšana un konfigurēšana"
description: "Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt programmu Microsoft Dynamics 365 for Finance and Operations – Warehousing"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4b3d068ddbf6f0b28c97618f5fa10fa486f3af51
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Programmas Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing instalēšana un konfigurēšana

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt programmu Microsoft Dynamics 365 for Finance and Operations – Warehousing

Finance and Operations – Warehousing is ir programma, kas ir pieejama Google Play veikalā un Windows veikalā. Pašreizējai Finance and Operations versijai šī programma tiek nodrošināta kā savrups komponents, tāpēc jums pašiem tā ir jāizvieto ierīcēs, kas tiek izmantotas noliktavas uzdevumu veikšanai. Lai programmu varētu lietot Finance and Operations vidē, šo programmu ir nepieciešams lejupielādēt katrā ierīcē un to konfigurēt savienojuma izveidei ar Finance and Operations vidi. Šajā tēmā ir aprakstīts, kā instalēt programmu ierīcēs. Tajā ir arī paskaidrots, kā konfigurēt programmu savienojuma izveidei ar Finance and Operations vidi.

## <a name="prerequisites"></a>Priekšnosacījumi
Programma ir pieejama operētājsistēmās Android un Windows. Lai varētu lietot šo programmu, ierīcē ir jābūt instalētai kādai no tālāk norādītajām atbalstītajām operētājsistēmām. Jums ir jālieto arī kāda no tālāk norādītajām atbalstītajām Finance and Operations versijām. Izmantojiet tālāk esošajā tabulā sniegto informāciju, lai novērtētu, vai aparatūras un programmatūras vide ir piemērota programmas instalēšanai.

| Platforma                    | Versija                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (visas versijas)                                                                                                                                                   |
| Finance and Operations | Microsoft Finance and Operations versija 1611 <br>- vai - <br>Microsoft Dynamics AX versija 7.0/7.0.1 un Microsoft Dynamics AX 2. platformas atjauninājums ar labojumfailu KB 3210014 |

## <a name="get-the-app"></a>Iegūt programmu
-   Windows (UWP): [Finance and Operations - Warehousing Windows veikalā](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android:
    - [Finance and Operations - Warehousing Google Play veikalā](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - Warehousing veikalā Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a>Tīmekļa pakalpojuma lietojumprogrammas izveide pakalpojumā Active Directory
Lai programma varētu mijiedarboties ar noteiktu Finance and Operations serveri, pakalpojumā Azure Active Directory programmas Finance and Operations nomniekam ir jāreģistrē tīmekļa pakalpojuma programma. Drošības apsvērumu dēļ ir ieteicams izveidot tīmekļa pakalpojuma lietojumprogrammu katrai izmantotajai ierīcei. Lai izveidotu tīmekļa pakalpojuma lietojumprogrammu pakalpojumā Azure Active Directory (Azure AD), veiciet tālāk norādītās darbības.

1.  Tīmekļa pārlūkprogrammā atveriet vietni <https://manage.windowsazure.com>.
2.  Ievadiet tā lietotāja vārdu un paroli, kurš var piekļūt Azure abonementam.
3.  Azure portāla kreisajā navigācijas rūtī noklikšķiniet uz **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Režģī atlasiet Active Directory instanci, kas tiek izmantota programmatūrā Finance and Operations.
5.  Augšējā rīkjoslā noklikšķiniet uz **Lietojumprogrammas**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Apakšējā rūtī noklikšķiniet uz **Pievienot**. Tiek palaists vednis **Lietojumprogrammas pievienošana**.
7.  Ievadiet lietojumprogrammas nosaukumu un atlasiet **Tīmekļa lietojumprogramma un/vai tīmekļa API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Ievadiet reģistrēšanās vietrādi URL, kurš ir jūsu tīmekļa programmas vietrādis URL. Šis URL ir tāds pats kā jūsu izvietošanas URL, bet beigās tiek pievienots oauth. Ievadiet programmas ID URI — šī vērtība ir obligāta, bet autentificēšanai tā nav nepieciešama. Pārliecinieties, lai šis programmas ID URI ir viltus URI, piemēram, https://contosooperations/wmapp, jo jūsu izvietojuma vietrāža URL lietošana var izraisīt pierakstīšanās problēmas citās AAD programmās, piemēram, Excel pievienojumprogrammā. [![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)
9.  Dodieties uz cilni **Konfigurēt**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Ritiniet uz leju līdz sadaļai **Atļaujas citām lietojumprogrammām**. Noklikšķiniet uz **Pievienot lietojumprogrammu**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Sarakstā atlasiet **Microsoft Dynamics ERP**. Noklikšķiniet uz atzīmes pogas **Pabeigt** lapas labajā stūrī. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Sarakstā **Deleģēt atļaujas** atzīmējiet visas izvēles rūtiņas. Noklikšķiniet uz **Saglabāt**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Pievērsiet uzmanību tālāk norādītajai informācijai.
    -   **Klienta ID** — ritinot lapu uz augšu, ir redzams lauks **Klienta ID**.
    -   **Atslēga** — sadaļā **Atslēgas** izveidojiet atslēgu, atlasot ilgumu, un kopējiet atslēgu. Vēlāk atslēga tiks saukta par **klienta noslēpumu**.

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Izveidot un konfigurēt lietotāja kontu programmatūrā Finance and Operations
Lai programmatūrā Finance and Operations varētu izmantot jūsu Azure AD programmu, ir jāveic tālāk norādītās konfigurēšanas darbības.

1.  Pakalpojumā Azure Active Directory izveidojiet jaunu lietotāja kontu Finance and Operations nomniekam. Šī lietotāja konta mērķis ir piekļūt konkrētajam noliktavu programmas pielāgotajam pakalpojumam, ko nodrošina Finance and Operations serveris. Pēc šīs darbības veikšanas jums ir pieejami WMDP lietotāja akreditācijas dati, kas sastāv no WMDP e-pasta adreses un WMDP paroles. Lai uzzinātu par pamata darbībām, kas ir jāveic, lai pievienotu lietotājus pakalpojumā Azure AD un programmatūrā Finance and Operations, skatiet pamācību: [Reģistrēties Finance and Operations abonementam](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).
2.  Izveidojiet Finance and Operations lietotāju, kas atbilst noliktavu programmas lietotāja akreditācijas datiem.
    1.  Programmatūrā Finance and Operations pārejiet uz sadaļu **Sistēmas administrēšana** &gt; **Vispārīgi** &gt; **Lietotāji**.
    2.  Izveidojiet jaunu lietotāju.
    3.  Piešķiriet lomu Noliktavas mobilās ierīces lietotājs, kā tas ir redzams tālāk esošajā ekrānuzņēmumā. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Saistiet savu Azure Active Directory lietojumprogrammu ar noliktavu programmas lietotāju.
    1.  Programmatūrā Finance and Operations pārejiet uz sadaļu **Sistēmas administrēšana** &gt; **Iestatīšana** &gt; **Azure Active Directory programmas**.
    2.  Izveidojiet jaunu rindu.
    3.  Aizpildiet laiku **Klienta ID** (ievadot pēdējā sadaļā iegūto informāciju), piešķiriet nosaukumu un atlasiet iepriekš izveidoto lietotāju. Ieteicams atzīmēt visas jūsu ierīces, lai to nozaudēšanas gadījumā varētu viegli liegt to piekļuvi programmatūrai Finance and Operations, izmantojot šo lapu. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Lietojumprogrammas konfigurēšana
Ierīcē instalētā programma ir jākonfigurē savienojuma izveidei ar Finance and Operations serveri, izmantojot Azure AD programmu. Lai to paveiktu, veiciet tālāk norādītās darbības.

1.  Programmā pārejiet uz sadaļu **Savienojuma iestatījumi**.
2.  Noņemiet atzīmi no lauka **Demonstrācijas režīms**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Ievadiet sekojošo informāciju: 
    + **Azure Active Directory klienta ID** — klienta ID tiek iegūts, veicot 13. darbību sadaļā “Izveidot tīmekļa pakalpojuma programmu pakalpojumā Active Directory”. 
    + **Azure Active Directory klienta noslēpums** — klienta noslēpums tiek iegūts, veicot 13. darbību sadaļā “Izveidot tīmekļa pakalpojuma programmu pakalpojumā Active Directory”. 
    + **Azure Active Directory resurss** — Azure AD direktorija resurss atbilst Finance and Operations saknes URL. **Piezīme**. Šī lauka vērtības beigās nedrīkst ievadīt uz priekšu vērstās slīpsvītras rakstzīmi (/). 
    + **Azure Active Directory nomnieks** — Azure AD direktorija nomnieks, kas tiek izmantots ar Finance and Operations serveri: https://login.windows.net/jūsu-AD-nomnieka-ID. Piemēram: https://login.windows.net/contosooperations.onmicrosoft.com.
    <br>**Piezīme**. Šī lauka vērtības beigās nedrīkst ievadīt uz priekšu vērstās slīpsvītras rakstzīmi (/). 
    + **Uzņēmums** — ievadiet to juridisko personu programmatūrā Finance and Operations, ar programmai ir jāizveido savienojums. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Atlasiet pogu **Atpakaļ** lietojumprogrammas apakšējā kreisajā stūrī. Tagad programmā tiek izveidots savienojums ar Finance and Operations serveri un parādīts noliktavas darbinieka pieteikšanās ekrāns. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Ierīces piekļuves liegšana
Ja ierīce ir nozaudēta vai apdraudēta, ir jāliedz šīs ierīces piekļuve programmatūrai Finance and Operations. Tālāk ir norādītas ieteicamā piekļuves liegšanas procesa darbības.

1.  Programmatūrā Finance and Operations pārejiet uz sadaļu **Sistēmas administrēšana** &gt; **Iestatīšana** &gt; **Azure Active Directory programmas**.
2.  Dzēsiet rindu, kas atbilst ierīcei, kuras piekļuvi vēlaties liegt. Pierakstiet šīs ierīces parametra **Klienta ID** vērtību.
3.  Pierakstieties Azure klasiskajā portālā: <https://manage.windowsazure.com>.
4.  Noklikšķiniet uz ikonas **Active Directory** kreisās puses izvēlnē un pēc tam noklikšķiniet uz vajadzīgā direktorija.
5.  Augšējā izvēlnē noklikšķiniet uz **Lietojumprogrammas** un pēc tam noklikšķiniet uz lietojumprogrammas, ko vēlaties konfigurēt. Tiek parādīta lapa **Īsā pamācība**, kurā ir pieejama vienotās pieteikšanās un cita konfigurācijas informācija.
6.  Noklikšķiniet uz cilnes **Konfigurēšana**, ritiniet uz leju un pārliecinieties, ka lietojumprogrammas parametra **Klienta ID** vērtība ir vienāda ar vērtību, ko pierakstījāt, veicot 2. darbību šajā sadaļā.
7.  Noklikšķiniet uz komandjoslas pogas **Dzēst**.
8.  Apstiprinājuma ziņojumā noklikšķiniet uz **Jā**.





