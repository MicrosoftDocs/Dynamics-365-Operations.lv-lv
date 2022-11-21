---
title: Lietotāja plūsmas izveide
description: Šajā rakstā ir aprakstīts, kā portālā Microsoft Azure izveidot lietotāju plūsmas politikas.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785830"
---
# <a name="create-user-flow-policies"></a>Lietotāja plūsmas izveide

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā portālā Microsoft Azure izveidot lietotāju plūsmas politikas.

Lietotāju plūsmas ir politikas Azure Active Directory () business-to-consumer (Azure AD B2C), ko izmanto, lai nodrošinātu drošu pieteikšanos, reģistrēšanos, profila rediģēšanu un paroles lietotāja pieredzes aizmiršanu. Dynamics 365 Commerce izmanto šīs plūsmas, lai veiktu politikas darbības, lai mijiedarbotos ar Azure AD B2C nomnieku. Kad lietotājs mijiedarbojas ar šīm politikām, viņš tiek novirzīts uz B2C nomnieku Azure AD, lai veiktu šīs darbības.

Azure AD B2C sniedz trīs pamata lietotāju plūsmas tipus:
- Pierakstīties un pieteikties
- Profila labošana
- Paroles atiestatīšana

Varat izvēlēties izmantot noklusējuma lietotāju plūsmas, ko Azure AD nodrošina, kas parādīs B2C viesotu Azure AD lapu. Līdzīgi varat izveidot HTML lapu, lai kontrolētu šo lietotāju plūsmas pieredzes izskatu un iespaidu. 

Lai pielāgotu lietotāja politikas lapas Dynamics 365 Commerce, skatiet sadaļu [Pielāgotu lapu iestatīšana lietotāju pieteikšanās tiesībām](custom-pages-user-logins.md). Papildinformāciju skatiet sadaļā [Lietotāja pieredzes Azure Active Directory interfeisa pielāgošana B2C](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Reģistrēšanās un pierakstīšanās lietotāju plūsmas politikas izveide

Lai izveidotu reģistrēšanās un pierakstīšanās lietotāju plūsmas politiku, veiciet tālāk norādītās darbības.

1. Azure portālā kreisajā navigācijas rūtī atlasiet **Lietotāju plūsmas (politikas)**.
1. Lapā **Azure AD B2C — lietotāja plūsmas (politikas)** atlasiet **Jauna lietotāja plūsma**.
1. Atlasiet **Pierakstīšanās un reģistrācijas** politiku, tad atlasiet versiju **Ieteikts**.
1. Sadaļā **Nosaukums** ievadiet politikas nosaukumu. Pēc tam šis nosaukums tiks parādīts ar prefiksu, kuru portāls piešķir (piemēram, "B2C_1_").
1. Sadaļas **Identitātes nodrošinātāji** sadaļā Lokālie **konti** atlasiet **Reģistrēšanās** pa e-pastu. E-pasta autentifikācija tiek izmantota visizplatītākajos Commerce scenārijos. Ja izmantojat arī sociālās identitātes nodrošinātāja autentifikāciju, varat arī atlasīt tos šajā laikā.
1. Saskaņā ar **Daudzfaktoru autentifikāciju** atlasiet atbilstošo jūsu uzņēmuma izvēli. 
1. Sadaļā **Lietotāja atribūti un prasības** atlasiet opcijas, lai apkopotu atbilstošos atribūtus vai atgriešanas prasības. Atlasiet **Rādīt vairāk...**, lai iegūtu pilnu atribūtu un pretenziju opciju sarakstu. Commerce ir nepieciešamas šādas noklusējuma opcijas:

    | **Savākt atribūtu** | **Atgriešanas prasība** |
    | ---------------------- | ----------------- |
    | E-pasta adrese          | E-pasta adreses   |
    | Norādītais nosaukums             | Norādītais nosaukums        |
    |                        | Identitātes nodrošinātājs |
    | Uzvārds                | Uzvārds           |
    |                        | Lietotāja objekta ID  |

1. Atlasiet **Izveidot**.

Šis attēls ir B2C reģistrēšanās un pierakstīšanās lietotāju plūsmas piemērs Azure AD.

![Parakstīšanās un pieteikšanās politikas iestatījumi.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Izveidot profila rediģēšanas lietotāja plūsmas politiku

Lai izveidotu profila rediģēšanas lietotāja plūsmas politiku, veiciet tālāk minētās darbības.

1. Azure portālā kreisajā navigācijas rūtī atlasiet **Lietotāju plūsmas (politikas)**.
1. Lapā **Azure AD B2C — lietotāja plūsmas (politikas)** atlasiet **Jauna lietotāja plūsma**.
1. Atlasiet **Profila rediģēšana** un pēc tam atlasiet **Ieteicamo** versiju.
1. Sadaļā **Nosaukums** ievadiet profila rediģēšanas lietotāja plūsmu. Pēc tam šis nosaukums tiks parādīts ar prefiksu, kuru portāls piešķir (piemēram, "B2C_1_").
1. Sadaļas **Identitātes nodrošinātāji** sadaļā Lokālie **konti** atlasiet **E-pasta pierakstīšanās**.
1. Sadaļā **Lietotāja atribūti** atlasiet kādu no tālāk norādītajām izvēles rūtiņām:
    
    | **Savākt atribūtu** | **Atgriešanas prasība** |
    | ---------------------- | ----------------- |
    |                        | E-pasta adreses   |
    | Norādītais nosaukums             | Norādītais nosaukums        |
    |                        | Identitātes nodrošinātājs |
    | Uzvārds                | Uzvārds           |
    |                        | Lietotāja objekta ID  |
    
1. Atlasiet **Izveidot**.

Sekojošajā attēlā parādīts piemērs ar Azure AD B2C profila rediģēšanas lietotāja plūsmu.

![B2C profila rediģēšanas lietotāja plūsmas piemērs Azure AD](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Izveidot paroles atiestatīšanas lietotāja plūsmas politiku

Lai izveidotu paroles atiestatīšanas lietotāja plūsmas politiku, veiciet tālāk minētās darbības.

1. Azure portālā kreisajā navigācijas rūtī atlasiet **Lietotāju plūsmas (politikas)**.
1. Lapā **Azure AD B2C — lietotāja plūsmas (politikas)** atlasiet **Jauna lietotāja plūsma**.
1. Atlasiet **Profila rediģēšana** un pēc tam atlasiet **Ieteicamo** versiju.
1. Sadaļā **Nosaukums** ievadiet paroles atiestatīšanas lietotāja plūsmas nosaukumu.
1. Sadaļā **Identitātes nodrošinātāji** atlasiet **Atiestatīt paroli, izmantojot e-pasta adresi**.
1. Atlasiet **Izveidot**.
1. Sadaļā **Pieteikumu prasības** atlasiet kādu no tālāk norādītajām izvēles rūtiņām:
    - **E-pasta adreses**
    - **Norādītais nosaukums**
    - **Uzvārds**
    - **Lietotāja objekta ID**
1. Atlasiet **Izveidot**.

Sekojošajā attēlā parādīts, kur iestatīt **Atiestatīšanas paroli, izmantojot pasta adresi** Azure AD B2C paroles atiestatīšanas lietotāja plūsmā.

![Iestatiet "Atiestatīt paroli, izmantojot pasta adresi" paroles atiestatīšanas politikā](./media/B2CImage_13.png)

## <a name="next-steps"></a>Turpmākās darbības

Lai turpinātu B2C nomnieka iestatīšanas procesu programmatūrā Commerce, turpiniet sadaļu [Sociālās identitātes nodrošinātāju](add-social-identity-providers.md) pievienošana.

## <a name="additional-resources"></a>Papildu resursi

[B2C nomnieka iestatīšana programmā Commerce](set-up-b2c-tenant.md)

[Esoša B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā](create-link-aad-b2c-tenant.md)

[Izveidot B2C pieteikumu](create-b2c-app.md)

[Pievienot sociālās identitātes sniedzējus (pēc izvēles)](add-social-identity-providers.md)

[Atjauniniet Commerce galveno mītni ar jauno Azure AD B2C informāciju](update-hq-aad-b2c-info.md)

[Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā](config-b2c-tenant-site-builder.md)

[B2C papildinformācija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
