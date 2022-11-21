---
title: Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā
description: Šajā rakstā ir aprakstīts, kā konfigurēt uzņēmuma un patērētāja (B2C) nomnieku Microsoft Dynamics 365 Commerce vietnes veidotājā.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785831"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt uzņēmuma un patērētāja (B2C) nomnieku Microsoft Dynamics 365 Commerce vietnes veidotājā.

Kad jūsu Azure AD B2C nomnieka iestatīšana ir pabeigta, jums ir jākonfigurē B2C nomnieks Commerce vietņu veidotājā. Konfigurēšanas soļi ietver B2C lietojumprogrammas informācijas vākšanu no Azure portāla, ievadot šo B2C lietojumprogrammas informāciju vietņu veidotājā un pēc tam asociējot B2C programmu ar jūsu vietni un kanālu.

### <a name="collect-the-required-application-information"></a>Apkopot nepieciešamo programmas informāciju

Lai apkopotu nepieciešamo informāciju par programmu, veiciet šīs darbības.

1. Azure portālā dodieties uz Home **\>Azure AD B2C - App registrations**.
1. Atlasiet savu lietojumprogrammu un pēc tam kreisajā navigācijas rūtī atlasiet **Pārskats**, lai iegūtu detalizētu informāciju par lietojumprogrammu.
1. Izmantojot lietojumprogrammas (klienta) ID atsauci, iegūstiet B2C nomniekā izveidotās B2C lietojumprogrammas **ID**. Tas vēlāk tiks ievadīts kā **Klienta GUID** vietņu veidotājā.
1. Atlasiet **Novirzīt URI** un apkopojiet atbildes URL, kas tiek rādīts jūsu vietnei (atbildes URL, kas ievadīts iestatīšanas laikā).
1. Dodieties uz **Sākums \>Azure AD B2C - Lietotāju plūsmas un pēc tam apkopojiet katras lietotāju plūsmas politikas pilnos nosaukumus**.

Šajā attēlā ir parādīts B2C - lietotņu reģistrācijas **Azure AD pārskata lapas piemērs**.

![Azure AD B2C — lietotņu reģistrācijas pārskata lapa ar iezīmētu lietojumprogrammas (klienta) ID](./media/ClientGUID_Application_AzurePortal.png)

Sekojošajā attēlā ir parādīts lietotāja plūsmas politikas piemērs, kas norādīts **Azure AD B2C — lietotāja plūsmas (politikas)** lapā.

![Apkopot katras B2C politikas plūsmas nosaukumus.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>B2C nomnieka lietojumprogrammas informācijas ievadīšana Azure AD programmā Commerce

Jums jāievada Azure AD B2C nomnieka informācija Commerce vietņu veidotājā, pirms asociējat B2C nomnieku ar jūsu vietnēm.

Lai pievienotu B2C Azure AD nomnieka lietojumprogrammas informāciju programmai Commerce, veiciet tālāk norādītās darbības.

1. Piesakieties kā administrators Commerce vietņu veidotājā jūsu videi.
1. Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi**, lai to izvērstu.
1. Sadaļā **Nomnieka iestatījumi** atlasiet **Vietnes autentifikācijas iestatīšana**. 
1. Galvenajā logā blakus **Vietnes autentifikācijas** profili atlasiet **Pārvaldīt**. (Ja jūsu nomnieks tiek parādīts vietnes autentifikācijas profilu sarakstā, administrators to jau ir pievienojis. Pārbaudiet, vai tālāk norādītās 6. darbības vienumi atbilst tiem, kas paredzēti jūsu paredzētajam B2C iestatījumam. Jaunu profilu var izveidot arī, izmantojot līdzīgus Azure AD B2C nomniekus vai lietojumprogrammas, lai ņemtu vērā nelielas atšķirības, piemēram, atšķirīgus lietotāju politiku ID).
1. Atlasiet **Pievienot vietnes autentifikācijas profilu**.
1. Veidlapā ievadiet tālāk norādītos pieprasītos vienumus, izmantojot vērtības no jūsu B2C nomnieka un lietojumprogrammas. Lauki, kas nav nepieciešami (bez zvaigznītes), var tikt atstāti tukši.

    - **Lietojumprogrammas nosaukums**: jūsu B2C lietojumprogrammas nosaukums, piemēram, "Fabrikam B2C".
    - **Nomnieka nosaukums**: jūsu B2C nomnieka nosaukums (piemēram, izmantot "fabrikam", ja domēns parādās kā "fabrikam.onmicrosoft.com" B2C nomniekam). 
    - **Aizmirstas paroles politikas ID**: aizmirstas paroles lietotāja plūsmas politikas ID, piemēram, "B2C_1_PasswordReset".
    - **Reģistrēšanās pierakstīšanās politikas ID: reģistrēšanās un pierakstīšanās lietotāja plūsmas politikas ID**, piemēram, "B2C_1_signup_signin".
    - **Klienta GUID**: B2C lietojumprogrammas ID, piemēram, "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".
    - **Rediģēt profila politikas ID**: profila rediģēšanas lietotāja plūsmas politikas ID, piemēram, "B2C_1A_ProfileEdit".

1. Atlasiet **Labi**. Tagad jums ir jāredz jūsu B2C lietojumprogrammas nosaukums, kas parādās sarakstā.
1. Atlasiet **Saglabāt**, lai saglabātu izmaiņas.

Neobligātais **pielāgotais domēns** Login ir jāizmanto tikai tad, ja iestatāt pielāgotu domēnu B2C nomniekam Azure AD. Papildinformāciju un apsvērumus par lauka Login pielāgotā domēna **izmantošanu skatiet sadaļā** Papildinformācija [par B2C](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Saistīt B2C lietojumprogrammu ar jūsu vietni un kanālu

> [!WARNING]
> - Ja jūsu vietne jau ir saistīta ar B2C lietojumprogrammu, pārejot uz citu B2C programmu, tiks noņemtas pašreizējās atsauces, kas izveidotas lietotājiem, kas jau ir reģistrējušies šajā vidē. Ja tas tiks mainīts, visi akreditācijas dati, kas ir saistīti ar pašlaik piešķirto B2C lietojumprogrammu, lietotājiem nebūs pieejami. 
> - Atjauniniet B2C lietojumprogrammu tikai tad, ja pirmo reizi iestatāt kanāla B2C lietojumprogrammu vai ja plānojat likt lietotājiem vēlreiz reģistrēties ar jauniem akreditācijas datiem šajā kanālā, izmantojot jauno B2C lietojumprogrammu. Esiet piesardzīgs, saistot kanālus ar B2C lietojumprogrammām, un skaidri nosauciet lietojumprogrammas. Ja kanāls nav saistīts ar B2C programmu tālāk norādītajās darbībās, lietotāji, kas piesakās šajā kanālā jūsu vietnei, tiks ievadīti B2C programmā, kas tiek parādīta kā **Noklusējums** **Nomnieka iestatījumi \> B2C iestatījumi** B2C lietojumprogrammu saraksts.

Lai saistītu B2C lietojumprogrammu ar jūsu vietni un kanālu, sekojiet šīm darbībām,

1. Dodieties uz savu vietni Commerce vietņu veidotājā.
1. Kreisās puses navigācijas rūtī atlasiet **Vietnes iestatījumi**, lai to izvērstu.
1. Zem **Vietas iestatījumiem** atlasiet **Kanāli**.
1. Galvenajā logā zem **Kanāli** atlasiet kanālu.
1. Kanāla rekvizītu rūtī labajā pusē nolaižamajā izvēlnē Select B2C Application (**Atlasīt B2C lietojumprogrammu) atlasiet savu B2C lietojumprogrammas** nosaukumu.
1. Atlasiet **Aizvērt** un pēc tam atlasiet **Saglabāt un publicēt**.

## <a name="next-steps"></a>Turpmākās darbības

Lai turpinātu B2C nomnieka iestatīšanas procesu programmatūrā Commerce, pārejiet pie Papildinformācija [par B2C](additional-b2c-info.md).

## <a name="additional-resources"></a>Papildu resursi

[B2C nomnieka iestatīšana programmā Commerce](set-up-b2c-tenant.md)

[Esoša B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā](create-link-aad-b2c-tenant.md)

[Izveidot B2C pieteikumu](create-b2c-app.md)

[Lietotāja plūsmas izveide](create-user-flow-policies.md)

[Pievienot sociālās identitātes sniedzējus (pēc izvēles)](add-social-identity-providers.md)

[Atjauniniet Commerce galveno mītni ar jauno Azure AD B2C informāciju](update-hq-aad-b2c-info.md)

[B2C papildinformācija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
