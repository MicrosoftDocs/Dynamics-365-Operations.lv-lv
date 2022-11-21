---
title: B2C nomnieka iestatīšana programmā Commerce
description: Šajā rakstā ir aprakstīts, kā iestatīt savus Azure Active Directory () business-to-consumer (Azure AD B2C) nomniekus lietotāju vietņu autentifikācijai pakalpojumā Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785145"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>B2C nomnieka iestatīšana programmā Commerce

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iestatīt savus Azure Active Directory () business-to-consumer (Azure AD B2C) nomniekus lietotāju vietņu autentifikācijai pakalpojumā Dynamics 365 Commerce.

Dynamics 365 Commerce izmanto Azure AD B2C, lai atbalstītu lietotāja akreditācijas datus un autentifikācijas plūsmas. Lietotājs var pieteikties, pierakstīties un atiestatīt savu paroli, izmantojot šīs plūsmas. Azure AD B2C saglabā lietotāja sensitīvo autentifikācijas informāciju, piemēram, lietotāja vārdu un paroli. Lietotāja ieraksts B2C nomniekā saglabās vai nu B2C lokālā konta ierakstu, vai arī B2C sociālā identitātes nodrošinātāja ierakstu. Šie B2C ieraksti tiks saistīti ar klienta ierakstu tirdzniecības vidē.

> [!WARNING] 
> Azure AD B2C atiestata veco (mantojuma) lietotāju plūsmas uz 2021. gada 1. augustu. Tādēļ jums jāplāno migrēt savas lietotāja plūsmas uz jauno ieteicamo versiju. Jaunā versija nodrošina līdzekļu pārību un jaunas funkcijas. Ar ieteiktajām B2C lietotāju plūsmām ir jāizmanto Commerce versijas 10.0.15 vai jaunāka moduļa bibliotēka. Papildinformāciju skatiet sadaļā [Lietotāju darbplūsmas Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Commerce novērtēšanas vidēs ir iepriekš ielādēts Azure AD B2C nomnieks demonstrācijas nolūkiem. Paša Azure AD B2C nomnieka ielādēšana, izmantojot tālāk aprakstītās darbības, nav nepieciešama novērtēšanas vidēm.

> [!TIP]
> Jūs varat turpmāk aizsargāt savus vietas lietotājus un uzlabot savu Azure AD B2C nomnieku drošību ar Azure AD identitātes aizsardzību un nosacījuma piekļuvi. Lai pārskatītu Azure AD B2C Premium P1 un Premium P2 nomniekiem pieejamās iespējas, skatiet [Pakalpojuma Azure AD B2C identitātes aizsardzība un nosacījuma piekļuve](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Dynamics vides priekšnosacījumi

Pirms sākat, nodrošiniet, lai jūsu Dynamics 365 Commerce vide un e-komercijas kanāls tiktu atbilstoši konfigurēti, izpildot tālāk norādītos priekšnosacījumus.

- Iestatiet POS operāciju vērtību **AllowAnonymousAccess** uz "1" programmā Commerce Headquarters:
    1. Pārejiet uz **POS operācijām**.
    1. Operāciju režģī noklikšķiniet ar peles labo pogu un atlasiet **Personalizēt**.
    1. Atlasiet **Pievienot lauku**.
    1. Pieejamo kolonnu sarakstā atlasiet kolonnu **AllowAnonymousAccess**, lai to pievienotu.
    1. Atlasiet **Atjaunināt**.
    1. Operācijai **612** "Debitora pievienošana" mainiet **AllowAnonymousAccess** uz "1."
    1. Izpildiet darbu **1090 (Reģistri)**.
- Programmā Commerce Headquarters iestatiet numuru sērijas debitora konta **Manuālo** atribūtu uz **Nē**:
    1. Dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Debitoru parametri**.
    1. Atlasīt **Numuru sērijas**.
    1. Rindā **Debitora konts** veiciet dubultklikšķi uz vērtības **Numura sērijas kods**.
    1. Numuru sērijas kopsavilkuma cilnē **Vispārīgi** iestatiet **Manuāli** uz **Nē**.

Pēc vides Dynamics 365 Commerce izvietošanas ir ieteicams arī [Inicializēt sākumdatus](enable-configure-retail-functionality.md) vidē.

## <a name="next-steps"></a>Turpmākās darbības

Lai turpinātu B2C nomnieka iestatīšanas procesu programmatūrā Commerce, pārejiet pie Esoša [B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>Papildu resursi

[Esoša B2C nomnieka izveide vai saistīšana ar to Azure AD Azure portālā](create-link-aad-b2c-tenant.md)

[Izveidot B2C pieteikumu](create-b2c-app.md)

[Lietotāja plūsmas izveide](create-user-flow-policies.md)

[Pievienot sociālās identitātes sniedzējus (pēc izvēles)](add-social-identity-providers.md)

[Atjauniniet Commerce galveno mītni ar jauno Azure AD B2C informāciju](update-hq-aad-b2c-info.md)

[Konfigurējiet savu B2C nomnieku Commerce vietņu veidotājā](config-b2c-tenant-site-builder.md)

[B2C papildinformācija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
