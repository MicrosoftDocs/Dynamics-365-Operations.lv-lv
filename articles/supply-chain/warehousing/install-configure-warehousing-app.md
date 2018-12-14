---
title: "Programmas Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing instalēšana un konfigurēšana"
description: "Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt programmu Microsoft Dynamics 365 for Finance and Operations – Warehousing"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0967b10c2037c24c044f38c49b1b998f6771c66b
ms.openlocfilehash: a1f3cb65e370154e8f3f94780ffb5cab223c85f8
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Programmas Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing instalēšana un konfigurēšana

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Šajā tēmā aprakstīts, kā noliktavas konfigurēt mākoņa izvietojumiem. Ja meklējat informāciju par to, kā noliktavas konfigurēt lokālajiem izvietojumiem, skatiet rakstu [Noliktavas lokālajiem izvietojumiem](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt programmu Microsoft Dynamics 365 for Finance and Operations – Warehousing

Finance and Operations – Warehousing is ir programma, kas ir pieejama Google Play veikalā un Windows veikalā. Pašreizējai Finance and Operations versijai šī programma tiek nodrošināta kā savrups komponents, tāpēc jums pašiem tā ir jāizvieto ierīcēs, kas tiek izmantotas noliktavas uzdevumu veikšanai. Lai programmu varētu lietot Finance and Operations vidē, šo programmu ir nepieciešams lejupielādēt katrā ierīcē un to konfigurēt savienojuma izveidei ar Finance and Operations vidi. Šajā tēmā ir aprakstīts, kā instalēt programmu ierīcēs. Tajā ir arī paskaidrots, kā konfigurēt programmu savienojuma izveidei ar Finance and Operations vidi.

## <a name="prerequisites"></a>Priekšnosacījumi
Programma ir pieejama operētājsistēmās Android un Windows. Lai varētu lietot šo programmu, ierīcē ir jābūt instalētai kādai no tālāk norādītajām atbalstītajām operētājsistēmām. Jums ir jālieto arī kāda no tālāk norādītajām atbalstītajām Finance and Operations versijām. Izmantojiet tālāk esošajā tabulā sniegto informāciju, lai novērtētu, vai aparatūras un programmatūras vide ir piemērota programmas instalēšanai.

| Platforma                    | Versija                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (visas versijas)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, versija 1611 <br>- vai - <br>Microsoft Dynamics AX versija 7.0/7.0.1 un Microsoft Dynamics AX 2. platformas atjauninājums ar labojumfailu KB 3210014 |

## <a name="get-the-app"></a>Iegūt programmu
-   Windows (UWP)
     - [Finance and Operations — noliktavas pakalpojumā Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - Warehousing Google Play veikalā](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - Warehousing veikalā Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Tīmekļa pakalpojuma programmas izveide pakalpojumā Azure Active Directory
Lai programma varētu mijiedarboties ar noteiktu Finance and Operations serveri, pakalpojumā Azure Active Directory programmas Finance and Operations nomniekam ir jāreģistrē tīmekļa pakalpojuma programma. Drošības apsvērumu dēļ ir ieteicams izveidot tīmekļa pakalpojuma lietojumprogrammu katrai izmantotajai ierīcei. Lai izveidotu tīmekļa pakalpojuma lietojumprogrammu pakalpojumā Azure Active Directory (Azure AD), veiciet tālāk norādītās darbības.

1.  Tīmekļa pārlūkā dodieties uz vietni <https://portal.azure.com>.
2.  Ievadiet tā lietotāja vārdu un paroli, kurš var piekļūt Azure abonementam.
3.  Azure portāla kreisajā navigācijas rūtī noklikšķiniet uz **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Nodrošiniet, ka Active Directory instance atbilst instancei, kas izmantota programmā Finance and Operations.
5.  Sarakstā noklikšķiniet uz **Programmu reģistrācijas**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Augšējā rūtī noklikšķiniet uz **Jauna programmas reģistrācija**. Tiek palaists vednis **Lietojumprogrammas pievienošana**.
7.  Ievadiet programmas nosaukumu un atlasiet vienumu **Tīmekļa lietojumprogramma/tīmekļa API**. Ievadiet reģistrēšanās vietrādi URL, kurš ir jūsu tīmekļa programmas vietrādis URL. Šis URL ir tāds pats kā jūsu izvietošanas URL, bet beigās tiek pievienots oauth. Noklikšķiniet uz **Izveidot**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Sarakstā atlasiet jauno programmu. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Iegaumējiet **Programmas ID**, jo tas būs vēlāk nepieciešams. **Programmas ID** vēlāk tiks dēvēts par **Klienta ID**.
10. Rūtī **Iestatījumi** noklikšķiniet uz **Atslēgas**. Izveidojiet atslēgu, sadaļā **Paroles** ievadot atslēgas aprakstu un ilgumu. 
11. Noklikšķiniet uz **Saglabāt** un nokopējiet atslēgu. Vēlāk atslēga tiks saukta par **klienta noslēpumu**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Izveidot un konfigurēt lietotāja kontu programmatūrā Finance and Operations
Lai programmatūrā Finance and Operations varētu izmantot jūsu Azure AD programmu, ir jāveic tālāk norādītās konfigurēšanas darbības.

1.  Izveidojiet Finance and Operations lietotāju, kas atbilst noliktavu programmas lietotāja akreditācijas datiem.
    1.  Programmatūrā Finance and Operations pārejiet uz sadaļu **Sistēmas administrēšana** &gt; **Vispārīgi** &gt; **Lietotāji**.
    2.  Izveidojiet jaunu lietotāju.
    3.  Piešķiriet lomu Noliktavas mobilās ierīces lietotājs, kā tas ir redzams tālāk esošajā ekrānuzņēmumā. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Saistiet savu Azure Active Directory lietojumprogrammu ar noliktavu programmas lietotāju.
    1.  Programmatūrā Finance and Operations pārejiet uz sadaļu **Sistēmas administrēšana** &gt; **Iestatīšana** &gt; **Azure Active Directory programmas**.
    2.  Izveidojiet jaunu rindu.
    3.  Aizpildiet laiku **Klienta ID** (ievadot pēdējā sadaļā iegūto informāciju), piešķiriet nosaukumu un atlasiet iepriekš izveidoto lietotāju. Ieteicams atzīmēt visas jūsu ierīces, lai to nozaudēšanas gadījumā varētu viegli liegt to piekļuvi programmatūrai Finance and Operations, izmantojot šo lapu. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Lietojumprogrammas konfigurēšana
Ierīcē instalētā programma ir jākonfigurē savienojuma izveidei ar Finance and Operations serveri, izmantojot Azure AD programmu. Lai to paveiktu, veiciet tālāk norādītās darbības.

1.  Programmā pārejiet uz sadaļu **Savienojuma iestatījumi**.
2.  Noņemiet atzīmi no lauka **Demonstrācijas režīms**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Ievadiet sekojošo informāciju: 
    + **Azure Active Directory klienta ID** — klienta ID tiek iegūts, veicot 9. darbību sadaļā “Izveidot tīmekļa pakalpojuma programmu pakalpojumā Active Directory”. 
    + **Azure Active Directory klienta noslēpums** — klienta noslēpums tiek iegūts, veicot 11. darbību sadaļā “Izveidot tīmekļa pakalpojuma programmu pakalpojumā Active Directory”. 
    + **Azure Active Directory resurss** — Azure AD direktorija resurss atbilst Finance and Operations saknes URL. **Piezīme**. Šī lauka vērtības beigās nedrīkst ievadīt uz priekšu vērstās slīpsvītras rakstzīmi (/). 
    + **Azure Active Directory nomnieks** — Azure AD direktorija nomnieks, kas tiek izmantots ar Finance and Operations serveri: `https://login.windows.net/your-AD-tenant-ID`. Piemēram: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Piezīme**. Šī lauka vērtības beigās nedrīkst ievadīt uz priekšu vērstās slīpsvītras rakstzīmi (/). 
    + **Uzņēmums** — ievadiet to juridisko personu programmatūrā Finance and Operations, ar programmai ir jāizveido savienojums. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Atlasiet pogu **Atpakaļ** lietojumprogrammas apakšējā kreisajā stūrī. Tagad programmā tiek izveidots savienojums ar Finance and Operations serveri un parādīts noliktavas darbinieka pieteikšanās ekrāns. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Informāciju par to, kā iestatīt Dynamics 365 for Finance and Operations – Warehousing, lai skenētu svītrkodus, izmantojot kameru mobilajā ierīcē, skatiet [Svītrkodu skanēšana, izmantojot kameru programmā Dynamics 365 for Finance and Operations –Warehousing](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Ierīces piekļuves liegšana
Ja ierīce ir nozaudēta vai apdraudēta, ir jāliedz šīs ierīces piekļuve programmatūrai Finance and Operations. Tālāk ir norādītas ieteicamā piekļuves liegšanas procesa darbības.

1.  Programmatūrā Finance and Operations pārejiet uz sadaļu **Sistēmas administrēšana** &gt; **Iestatīšana** &gt; **Azure Active Directory programmas**.
2.  Dzēsiet rindu, kas atbilst ierīcei, kuras piekļuvi vēlaties liegt. Iegaumējiet noņemtajai ierīcei izmantoto **Klienta ID**, jo tas būs vēlāk nepieciešams.
3.  Pierakstieties Azure portālā vietnē <https://portal.azure.com>.
4.  Kreisajā izvēlnē noklikšķiniet uz ikonas **Active Directory** un pārliecinieties, vai atrodaties pareizajā direktorijā.
5.  Sarakstā noklikšķiniet uz **Programmu reģistrācijas** un pēc tam noklikšķiniet uz programmas, ko vēlaties konfigurēt. Tiks parādīta lapa **Iestatījumi** ar konfigurācijas informāciju.
6.  Nodrošiniet, lai programmas **Klienta ID** atbilstu šīs sadaļas 2. darbībā izmantotajam.
7.  Augšējā rūtī noklikšķiniet uz pogas **Dzēst**.
8.  Apstiprinājuma ziņojumā noklikšķiniet uz **Jā**.

