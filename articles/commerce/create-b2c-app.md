---
title: B2C lietojumprogrammas izveide
description: Šajā rakstā ir aprakstīts, kā portālā Microsoft Azure izveidot uzņēmumu un patērētāju (B2C) lietojumprogrammu.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785826"
---
# <a name="create-a-b2c-application"></a>B2C lietojumprogrammas izveide

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā portālā Microsoft Azure izveidot uzņēmumu un patērētāju (B2C) lietojumprogrammu.

Kad jūsu B2C nomnieks ir izveidots, jūs izveidosit B2C lietojumprogrammu savā jaunajā Azure Active Directory (Azure AD) nomniekā, lai mijiedarbotos ar komerciju.

Lai izveidotu B2C pieteikumu, izpildiet tālāk aprakstītās darbības.

1. Azure portālā atlasiet **Lietotnes reģistrācijas**, tad atlasiet **Jauna reģistrācija**.
1. Sadaļā **Nosaukums** ievadiet nosaukumu, kas jāpiešķir Azure AD šai B2C programmai.
1. Zem **Atbalstītie kontu tipi** atlasiet **Konti jebkurā identitātes nodrošinātājā vai organizācijas direktorijā (autentifikācijai lietotājiem ar lietotāju plūsmām)**.
1. Lai **Novirzītu URI**, ievadiet atvēlētos atbildes vietrāžus URL kā **Web** veidu. Skatiet zemāk [Atbildes vietrāži URL](#reply-urls), lai iegūtu informāciju par atbildes vietrāžiem URL un to formatēšanu. Ir jāievada novirzīšanas URI/atbildes URL, lai iespējotu novirzīšanu no Azure AD B2C atpakaļ uz jūsu vietni, kad lietotājs autentificējas. Atbildes URL var pievienot reģistrācijas procesa laikā vai pievienot vēlāk, B2C lietojumprogrammas sadaļas Pārskats izvēlnē Pārskats **atlasot** **saiti** Pievienot novirzīšanas URI **.**
1. **Atļaujām** atlasiet **Piešķirt administratoru atļauju openid un offline_access atļaujas**.
1. Atlasiet **Reģistrēt**.
1. Atlasiet jaunizveidoto lietojumprogrammu un dodieties uz **izvēlni Autentifikācija**. 
1. Ja ir ievadīts atbildes vietrādis URL, sadaļā **Netiešās dotācijas un hibrīdās plūsmas** atlasiet gan **Access pilnvaras**, gan **ID pilnvaru opcijas**, lai tās iespējotu lietojumprogrammai, un pēc tam atlasiet **Saglabāt**. Ja atbildes URL netika ievadīts reģistrācijas laikā, to var pievienot arī šajā lapā, atlasot Pievienot platformu **, atlasot** **Tīmeklis** un pēc tam ievadot lietojumprogrammas novirzīšanas URI. Pēc **tam būs pieejama sadaļa Netiešās dotācijas un hibrīdās plūsmas**, lai atlasītu gan piekļuves pilnvaru, gan **ID** pilnvaru **opcijas**.
1. Dodieties uz **Pārskata** izvēlni portālā Azure un nokopējiet **Programmas (klienta) ID**. Ievērojiet šo ID vēlākām uzstādīšanas darbībām (vēlāk norādīts kā **Klienta GUID**).

Lai iegūtu papildu atsauci uz Programmu reģistrācijām Azure AD B2C, lūdzu, skatiet [Jauno programmas reģistrāciju pieredzi Azure Active Directory B2C](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Atbilžu vietrāži URL

Atbilžu vietrāži URL ir svarīgi, jo tie nodrošina atgriešanās domēnus iekļaut sarakstā, kad jūsu vietne Azure AD B2C pieprasa autentificēt lietotāju. Tas ļauj atgriezt autentificētu lietotāju atpakaļ domēnā, no kura tie piesakās sistēmā (jūsu vietnes domēns). 

Lodziņā **Atbilžu vietrāži URL** ekrānā **Azure AD B2c - Applications \> Jauna programma** jums ir jāpievieno atsevišķas rindas gan jūsu vietnes domēnam, gan (tiklīdz jūsu vide ir nodrošināta) komercijas ģenerētajam vietrādim URL. Šiem URL vienmēr ir jāizmanto derīgs URL formāts, un tiem ir jābūt tikai pamata URL (bez slīpsvītrām vai ceļiem). Pēc tam ``/_msdyn365/authresp`` virkne ir jāpievieno pamata URL, kā tas ir sekojošajos piemēros.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domēnam ir pilnībā jāatbilst e-komercijas domēnam. Ja izmantojat vairākus domēnus, šis URL ir jāpievieno katram domēnam.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>Turpmākās darbības

Lai turpinātu B2C nomnieka iestatīšanas procesu programmā Commerce, pārejiet pie Lietotāju [plūsmas politiku](create-user-flow-policies.md) izveide.

## <a name="additional-resources"></a>Papildu resursi

[B2C nomnieka iestatīšana programmā Commerce](set-up-b2c-tenant.md)

[Esoša B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā](create-link-aad-b2c-tenant.md)

[Lietotāja plūsmas izveide](create-user-flow-policies.md)

[Pievienot sociālās identitātes sniedzējus (pēc izvēles)](add-social-identity-providers.md)

[Atjauniniet Commerce galveno mītni ar jauno Azure AD B2C informāciju](update-hq-aad-b2c-info.md)

[Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā](config-b2c-tenant-site-builder.md)

[B2C papildinformācija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
