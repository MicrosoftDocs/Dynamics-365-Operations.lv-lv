---
title: Sociālās identitātes nodrošinātāju pievienošana
description: Šajā rakstā ir aprakstīts, kā portālā Microsoft Azure pievienot sociālās identitātes nodrošinātājus.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785810"
---
# <a name="add-social-identity-providers"></a>Sociālās identitātes nodrošinātāju pievienošana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā portālā Microsoft Azure pievienot sociālās identitātes nodrošinātājus.

Sociālās identitātes nodrošinātāji ļauj lietotājiem izmantot savu sociālā konta autentifikāciju. Sociālās identitātes nodrošinātāja autentifikācijas pievienošana nav obligāta risinājumā Dynamics 365 Commerce. 

Ja nav pievienota sociālās identitātes nodrošinātāja autentifikācija, noklusējuma Azure Active Directory (Azure AD) B2C profili būs jūsu lietotāju bāzes galvenie profili. Lietotāji atlasīs savu lietotājvārdu (viņu vēlamo e-pasta adresi) un iestatīs paroli. Azure AD B2C lietotājiem tiks autentificēti tieši. 

Ja tiek pievienota sociālā identitātes nodrošinātāja autentifikācija un lietotājs izvēlas vienu no piedāvātajiem sociālās identitātes nodrošinātājiem, tas joprojām ir izveidots ar Azure AD B2C nomniekā. Pēc tam Azure AD B2C autentificēs lietotāja akreditācijas datus ar sociālās identitātes nodrošinātāju.

> [!NOTE]
> Identitātes nodrošinātāja žurnāls izveido ierakstu B2C nomniekā, bet citā formātā, nekā Lokālais konts, jo tas izsauc ārējās sociālās identitātes sniedzēja atsauci autentifikācijai. Lietotājs var izmantot vienu un to pašu e-pasta adresi sociālo identitātes nodrošinātāju starpā, kas nozīmē, ka Autentifikācijai izmantotais e-pasta lietotājvārds var nebūt unikāls nomniekam. Azure AD B2C tikai realizēs to, ka lietotājiem ir unikāla e-pasta adrese vietējos B2C kontos.

Pirms jūs varat pievienot sociālās identitātes nodrošinātāju autentifikācijai, jums ir jādodas uz identitātes nodrošinātāja portālu un jāiestata identitātes nodrošinātāja programma, kā norādīts Azure AD B2C dokumentācijā. Tālāk ir sniegts saraksts ar saitēm uz dokumentāciju.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Viens nomnieks)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft konts](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Pievienot un iestatīt sociālās identitātes nodrošinātāju

> [!NOTE]
> Sociālās identitātes nodrošinātāju pievienošana ir neobligāts solis, izveidojot uzņēmumu un patērētāju (B2C) nomnieku Microsoft Dynamics 365 Commerce.

Lai pievienotu un iestatītu sociālās identitātes nodrošinātāju, veiciet šīs darbības.  

1. Azure portālā dodieties uz **Identitātes nodrošinātājiem**.
1. Atlasiet **Pievienot**. Parādās ekrāns **Pievienot identitātes nodrošinātāju**.
1. Sadaļā **Nosaukums** ievadiet vārdu, kas lietotājiem tiks parādīts pierakstīšanās ekrānā.
1. Sadaļā **Identitātes nodrošinātāja tips** no saraksta atlasiet identitātes nodrošinātāju.
1. Atlasiet **Labi**.
1. Atlasiet **Iestatīt šo identitātes nodrošinātāju**, lai piekļūtu ekrānam **Iestatīt sociālās identitātes nodrošinātāja**.
1. Sadaļā **Klienta ID** ievadiet klienta ID, kas iegūts no identitātes nodrošinātāja programmas uzstādīšanas.
1. Sadaļā **Klienta slepenā atslēga** ievadiet klienta slepeno atslēgu, kas iegūts no identitātes nodrošinātāja programmas uzstādīšanas.
1. Pievienojiet lietotāja plūsmu pierakstīšanās/reģistrēšanās politikām:
1. Doties uz **Azure AD B2C — lietotāja plūsmas (politikas) \> {jūsu pierakstīšanās/pieteikšanās politika} \> identitātes nodrošinātāji**.
1. Lai pievienotu pierakstīšanās/reģistrēšanās lietotāja plūsmas politiku, atlasiet katru identitātes nodrošinātāju, ko esat iestatījis savam kontam. Lai pārbaudītu plūsmas, atlasiet **Palaist lietotāja plūsmu** katram identitātes nodrošinātājam. Jaunā cilnē tiek parādīta pierakstīšanās lapa, kurā redzams jaunā identitātes nodrošinātāja izvēles lodziņš.

Sekojošajā attēlā ir redzami **Pievienot identitātes nodrošinātāju** un **Uzstādīt sociālo identitātes nodrošinātāju** ekrāna piemēri Azure AD B2C.

![Sociālās identitātes nodrošinātāja pievienošana jūsu aplikācijai.](./media/B2CImage_14.png)

Sekojošajā attēlā parādīts piemērs, kā atlasīt identitātes nodrošinātājus Azure AD B2C **Identitātes nodrošinātāju** lapā.

![Atlasiet katru Sociālā identitātes nodrošinātāju, lai iespējotu politiku.](./media/B2CImage_16.png)

Sekojošajā attēlā parādīts noklusējuma pierakstīšanās ekrāna piemērs, kurā ir parādīts sociālās identitātes nodrošinātāja pierakstīšanās poga.

> [!NOTE]
> Ja jūsu lietotāju plūsmām izmantojat sistēmā Commerce iebūvētās pielāgotās lapas, pogas sociālās identitātes nodrošinātājiem jāpievieno, izmantojot Commerce moduļu bibliotēkas paplašināmības līdzekļus. Turklāt, iestatot programmas ar īpašu sociālās identitātes nodrošinātāju, dažos gadījumos URL vai konfigurācijas virknes var būt reģistrjutīgas. Plašākai informācijai meklējiet sava sociālās identitātes nodrošinātāja savienojuma norādījumus.
 
![Tiek parādīts noklusētais pieteikšanās ekrāns ar sociālās identitātes nodrošinātāja pierakstīšanās pogu.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Turpmākās darbības

Lai turpinātu B2C nomnieka iestatīšanas procesu programmatūrā Commerce, pārejiet pie Atjaunināt [komercijas galveno mītni ar jauno Azure AD B2C informāciju](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>Papildu resursi

[B2C nomnieka iestatīšana programmā Commerce](set-up-b2c-tenant.md)

[Esoša B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā](create-link-aad-b2c-tenant.md)

[Izveidot B2C pieteikumu](create-b2c-app.md)

[Lietotāja plūsmas izveide](create-user-flow-policies.md)

[Atjauniniet Commerce galveno mītni ar jauno Azure AD B2C informāciju](update-hq-aad-b2c-info.md)

[Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā](config-b2c-tenant-site-builder.md)

[B2C papildinformācija](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
