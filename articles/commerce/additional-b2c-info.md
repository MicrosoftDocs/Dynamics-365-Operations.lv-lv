---
title: B2C papildinformācija
description: Šajā rakstā ir sniegta papildinformācija par to, kā iestatīt uzņēmuma un patērētāja (B2C) nomnieku pakalpojumā Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785809"
---
# <a name="additional-b2c-information"></a>B2C papildinformācija

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegta papildinformācija par to, kā iestatīt uzņēmuma un patērētāja (B2C) nomnieku pakalpojumā Microsoft Dynamics 365 Commerce.

### <a name="customer-migration"></a>Klientu migrācija

Ja apsverat iespēju migrēt klientu ierakstus no iepriekšējas identitātes nodrošinātāja platformas, lūdzu, sazinieties ar Dynamics 365 Commerce grupu, lai pārskatītu jūsu klientu migrācijas vajadzības.

Lai iegūtu papildu Azure AD B2C dokumentāciju par klientu migrāciju, skatiet sadaļu [Migrēt lietotājus uz Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Pielāgotas politikas

Lai iegūtu papildu informāciju par Azure AD B2C mijiedarbību un politikas plūsmu pielāgošanu, kas pārsniedz B2C standarta politiku piedāvāto, skatiet sadaļu [Pielāgotas Azure Active Directory B2C politikas](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Sekundārais administrators

Papildu administratora kontu var pievienot jūsu B2C nomnieka **Lietotāji** sadaļā. Tas var būt tiešais konts vai vispārējais konts. Ja ir jākopīgo konts grupas resursos, var tikt izveidots arī kopīgs konts. Izmantojot Azure AD B2C uzglabāto datu sensivitāti, kopējais konts ir rūpīgi jākontrolē atbilstoši jūsu uzņēmuma drošības praksei.

### <a name="set-up-a-custom-sign-in-domain"></a>Pielāgota pierakstīšanās domēna iestatīšana

Azure AD B2C ļauj iestatīt pielāgotu pierakstīšanās domēnu B2C nomniekam Azure AD. Norādījumus skatiet sadaļā [Pielāgotu domēnu iespējošana Azure Active Directory B2C](/azure/active-directory-b2c/custom-domain). 

Ja izmantojat pielāgotu pierakstīšanās domēnu, domēns ir jāievada Commerce vietņu veidotājā.

Lai vietņu veidotājā ievadītu pielāgotu pierakstīšanās domēnu, veiciet tālāk norādītās darbības.

1. Vietnes veidotāja augšējā labajā stūrī atlasiet vietņu pārslēdzēju un pēc tam atlasiet **Pārvaldīt vietnes**.
1. Kreisajā navigācijas rūtī atlasiet **Nomnieka iestatījumi \> Vietnes autentifikācijas iestatīšana**.
1. **Sadaļā Vietnes autentifikācijas** profili atlasiet **Pārvaldīt**.
1. Izlidošanas izvēlnē labajā pusē atlasiet **pogu Rediģēt** (zīmuļa simbols) blakus vietnes autentifikācijas profilam, kuram vēlaties ievadīt pielāgotu domēnu.
1. Dialoglodziņa **Vietnes autentifikācijas profila** rediģēšana sadaļā **Pieteikšanās pielāgotais domēns** ievadiet savu pielāgoto pierakstīšanās domēnu (piemēram, "login.fabrikam.com").

> [!WARNING]
> Atjauninot uz B2C nomnieka pielāgoto domēnu, izmaiņas ietekmē nomnieka izdevēja informāciju par ģenerēto Azure AD marķieri. Pēc tam detalizēta informācija par izsniedzēju ietvers pielāgoto domēnu, nevis noklusējuma domēnu, ko Azure AD nodrošina B2C. Cita **izdevēja konfigurācija Commerce galvenajā mītnē (** mazumtirdzniecības un komercijas **galvenās mītnes iestatīšanas \> parametri Komercijas koplietojamie parametri \>\> Identitātes nodrošinātāji \>) maina sistēmas mijiedarbību ar vietnes lietotājiem, potenciāli izveidojot jaunu klienta ierakstu, ja lietotājs autentificējas pret jauno izdevēju**. Visas pielāgotā domēna izmaiņas ir rūpīgi jāpārbauda pirms pārslēgšanās uz pielāgoto domēnu reāllaika Azure AD B2C vidē.

## <a name="additional-resources"></a>Papildu resursi

[B2C nomnieka iestatīšana programmā Commerce](set-up-b2c-tenant.md)

[Esoša B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā](create-link-aad-b2c-tenant.md)

[Izveidot B2C pieteikumu](create-b2c-app.md)

[Lietotāja plūsmas izveide](create-user-flow-policies.md)

[Pievienot sociālās identitātes sniedzējus (pēc izvēles)](add-social-identity-providers.md)

[Atjauniniet Commerce galveno mītni ar jauno Azure AD B2C informāciju](update-hq-aad-b2c-info.md)

[Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
