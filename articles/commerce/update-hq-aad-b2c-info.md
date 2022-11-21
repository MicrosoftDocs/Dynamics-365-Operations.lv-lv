---
title: Atjaunināt Commerce Headquarters ar jauno Azure AD B2C informāciju
description: Šajā rakstā ir aprakstīts, kā atjaunināt Microsoft Dynamics 365 Commerce galveno mītni ar jaunu Azure Active Directory (Azure AD) uzņēmuma un patērētāja (B2C) informāciju.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785834"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Atjaunināt Commerce Headquarters ar jauno Azure AD B2C informāciju

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā atjaunināt Microsoft Dynamics 365 Commerce galveno mītni ar jaunu Azure Active Directory (Azure AD) uzņēmuma un patērētāja (B2C) informāciju.

Pēc tam, kad iepriekšminētās Azure AD B2C nodrošināšanas darbības ir pabeigtas, Azure AD B2C lietojumprogrammai ir jābūt reģistrētai jūsu Dynamics 365 Commerce vidē.

Lai atjauninātu programmu Headquarters ar jauno Azure AD B2C informāciju, veiciet sekojošās darbības.

1. Programmā Commerce dodieties uz **Commerce koplietotie parametri** un atlasiet **Identitātes nodrošinātāji** kreisajā izvēlnē.
1. Sadaļā **identitātes nodrošinātāji** veiciet sekojošās darbības:
    1. **Lodziņā Izdevējs** ievadiet identitātes nodrošinātāja izdevēja virkni. Lai atrastu savu izsniedzēja virkni, skatiet tālāk [sadaļu Izdevēja virknes iegūšana galvenās mītnes iestatīšanai](#obtain-issuer-string-for-headquarters-setup).
    1. Lodziņā **Nosaukums** ievadiet izdevēja ieraksta nosaukumu.
    1. Lodziņā **Veids** ievadiet **Azure AD B2C (id_token)**.
1. Sadaļā **Pārbaudītāji** ar iepriekš atlasīto B2C identitātes nodrošinātāja vienumu rīkojieties šādi:
    1. **Lodziņā ClientID** ievadiet savu B2C lietojumprogrammas ID, ko varat atrast **B2C lietojumprogrammas rekvizītu lapas lodziņā Lietojumprogrammas ID**.
    1. Lodziņā **Veids** ievadiet **Publisks**.
    1. Lodziņā **Lietotāja veids** ievadiet **Pircējs**.
1. Darbību rūtī atlasiet **Saglabāt**.
1. Lodziņā Commerce Search meklējiet **Sadales grafiku**
1. Lapas **Sadales grafiki** kreisajā navigācijas izvēlnē atlasiet darbu **1110 globālā konfigurācija**.
1. Darbību rūtī atlasiet **Palaist tagad**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Iegūt izdevēja virkni galvenās mītnes iestatīšanai

Lai iegūtu identitātes nodrošinātāja izdevēja virkni, veiciet tālāk norādītās darbības.

1. Azure Azure AD portāla B2C lapā dodieties uz **Pierakstīšanās un reģistrēšanās** lietotāju plūsmu.
1. Kreisajā navigācijas izvēlnē atlasiet **Lapas izkārtojumi** sadaļā **Izkārtojuma nosaukums** atlasiet **Unificētā pierakstīšanās vai pieteikšanās lapa** un pēc tam atlasiet **Palaist lietotāju plūsmu**.
1. Pārliecinieties, vai jūsu lietojumprogramma ir iestatīta uz paredzēto Azure AD B2C lietojumprogrammu, kas izveidota iepriekš, un pēc tam atlasiet lietotāja plūsmas saiti, kas tiek parādīta **zem Palaist lietotāja plūsmas** galveni, kas ietver ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (Neatlasīt **Palaist lietotāja plūsmu**.) Tiks atvērta jauna cilne, kurā tiks parādīti metadati politikai, lai apkopotu izdevēja virkni.
1. Pārlūkprogrammas cilnē parādītajā metadatu lapā kopējiet identitātes nodrošinātāja izdevēja virkni (izdevēja **vērtība**, kas sākas ar "" un beidzas ar "https:///v2.0/"), kas izskatās līdzīgi tālāk sniegtajam piemēram.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**VAI**: Lai manuāli izveidotu to pašu metadatu URL, veiciet šādas darbības.

1. Izveidot metadatu adreses URL šādā formātā, izmantojot B2C nomnieku un politiku: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Piemērs: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Ievadiet metadatu adreses URL pārlūkprogrammas adreses joslā.
1. Metadatos kopējiet identitātes nodrošinātāja izdevēja URL ( **"izdevēja"** vērtība).
    - Piemērs: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Turpmākās darbības

Lai turpinātu B2C nomnieka iestatīšanas procesu programmatūrā Commerce, pārejiet pie [B2C nomnieka konfigurēšana Commerce vietņu veidotājā](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Papildu resursi

[B2C nomnieka iestatīšana programmā Commerce](set-up-b2c-tenant.md)

[Esoša B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā](create-link-aad-b2c-tenant.md)

[Izveidot B2C pieteikumu](create-b2c-app.md)

[Lietotāja plūsmas izveide](create-user-flow-policies.md)

[Pievienot sociālās identitātes sniedzējus (pēc izvēles)](add-social-identity-providers.md)

[Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā](config-b2c-tenant-site-builder.md)

[B2C papildinformācija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
