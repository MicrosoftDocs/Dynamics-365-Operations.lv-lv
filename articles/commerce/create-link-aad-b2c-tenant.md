---
title: Esoša B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā
description: Šajā rakstā ir aprakstīts, kā portālā Azure Active Directory izveidot esošu (Azure AD) business-to-consumer (B2C) nomnieku vai izveidot saiti uz to Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785827"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Esoša B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā portālā izveidot () uzņēmumu un patērētāju (Azure Active Directory B2C) nomnieku Azure AD Microsoft Azure vai izveidot saiti uz to. Papildinformāciju skatiet sadaļā [Apmācība: B2C nomnieka Azure Active Directory](/azure/active-directory-b2c/tutorial-create-tenant) izveide.

Lai Azure portālā izveidotu esošu B2C nomnieku vai izveidotu saiti uz to Azure AD, veiciet tālāk norādītās darbības.

1. Pierakstieties [Azure portālā](https://portal.azure.com/).
1. No Azure portāla izvēlnes atlasiet **Izveidot resursu**. Noteikti izmantojiet abonementu un direktoriju, kas tiks savienots ar jūsu komercijas vidi.

    ![Resursa izveide Azure portālā.](./media/B2CImage_1.png)

1. Doties uz **Identitātes \> Azure Active Directory B2C**.
1. Kad atrodaties lapā **Izveidot jaunu B2C nomnieku vai saistīt uz esošo nomnieku**, izmantojiet vienu no zemāk norādītajām opcijām, kas vislabāk atbilst jūsu uzņēmuma vajadzībām:

    - **Jauna Azure AD B2C nomnieka izveide: izmantojiet šo opciju, lai izveidotu jaunu** B2C nomnieku Azure AD.
        1. Atlasiet **Izveidot jaunu Azure AD B2C nomnieku**.
        1. Sadaļā **Organizācijas nosaukums** ievadiet organizācijas nosaukumu.
        1. Sadaļā **Sākotnējais domēna nosaukums** ievadiet sākotnējo domēna nosaukumu.
        1. Sadaļā **Valsts vai reģions** atlasiet valsti vai reģionu.
        1. Atlasiet **Izveidot**, lai izveidotu nomnieku.

     ![Izveidot jaunu Azure AD nomnieku.](./media/B2CImage_2.png)

     - **Saistīt esošu Azure AD B2C nomnieku uz manu Azure abonementu**: lietojiet šo opciju, ja jums jau ir Azure AD B2C nomnieks, ar kuru vēlaties veidot saiti.
        1. Atlasiet **Saistīt esošu Azure AD B2C nomnieku uz manu Azure abonementu**.
        1. Sadaļā **Azure AD B2C nomnieks** atlasiet atbilstošo B2C nomnieku. Ja atlasīšanas lodziņā tiek parādīts ziņojums "Nevar atrast piemērotus B2C nomniekus", jums nav esoša piemērota B2C nomnieka, un jums būs jāizveido jauns.
        1. Sadaļā **Resursu grupa** atlasiet **Izveidot jaunu**. Ievadiet **Nosaukumu** resursu grupai, kurā būs nomnieks, atlasiet **Resursu grupas atrašanās vietu** un pēc tam atlasiet **Izveidot**.

    ![Saistīt esošu Azure AD B2C nomnieku uz Azure abonementu.](./media/B2CImage_3.png)

1. Kad tiek izveidots jauns Azure AD B2C direktorijs (tas var ilgt kādu brīdi), saite uz jauno direktoriju parādīsies informācijas panelī. Šī saite novirzīs jūs uz lapu "Laipni lūdzam Azure Active Directory B2C".

    ![Saite uz jauno Azure AD direktoriju](./media/B2CImage_4.png)

> [!NOTE]
> Ja jūsu Azure kontā ir vairāki abonementi vai arī esat iestatījis B2C nomnieku, neveidojot saiti uz aktīvu abonementu, reklāmkarogs **Problēmu novēršana** jūs novirzīs, lai palīdzētu saistīt nomnieku ar abonementu. Atlasiet problēmu novēršanas ziņojumu un izpildiet norādījumus, lai atrisinātu abonementa problēmu.

Šis attēls rāda Azure AD B2C **Problēmu novēršanas** reklāmkaroga piemēru.

![Brīdinājumam, kas rāda direktoriju, nav aktīva abonementa.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Turpmākās darbības

Lai turpinātu B2C nomnieka iestatīšanas procesu programmatūrā Commerce, pārejiet pie B2C [lietojumprogrammas](create-b2c-app.md) izveide.

## <a name="additional-resources"></a>Papildu resursi

[B2C nomnieka iestatīšana programmā Commerce](set-up-b2c-tenant.md)

[Izveidot B2C pieteikumu](create-b2c-app.md)

[Lietotāja plūsmas izveide](create-user-flow-policies.md)

[Pievienot sociālās identitātes sniedzējus (pēc izvēles)](add-social-identity-providers.md)

[Atjauniniet Commerce galveno mītni ar jauno Azure AD B2C informāciju](update-hq-aad-b2c-info.md)

[Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā](config-b2c-tenant-site-builder.md)

[B2C papildinformācija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
