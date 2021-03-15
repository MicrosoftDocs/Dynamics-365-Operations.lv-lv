---
title: Sīkfailu atbilstība
description: Šajā tēmā ir aprakstīti apsvērumi attiecībā uz sīkfailu atbilstību un noklusējuma politikām, kas ir ietvertas pakalpojumā Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 95c5801e69396b21a36c4ae12ce17801e6f7fd88
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993504"
---
# <a name="cookie-compliance"></a>Sīkfailu atbilstība

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīti apsvērumi attiecībā uz sīkfailu atbilstību un noklusējuma politikām, kas ir ietvertas pakalpojumā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Privātums ir svarīgs faktors, kad tiek izmantotas izsekošanas tehnoloģijas, kas ietekmē e-komercijas klientus. Sakarā ar privātuma atbilstības standartiem, piemēram, Vispārīgo datu aizsardzības regulu (VDAR) Eiropas Savienībā (ES), elektroniskas privātuma vadlīnijas ir jānorāda jebkurai vietnei, kas šobrīd darbojas. Tā kā daudzas e-komercijas vietnes pēc noklusējuma ir pieejamas globāli, ir svarīgi pārskatīt e-komercijas vietnes atbilstības standartus.

Lai iegūtu papildinformāciju par pamatprincipiem, kurus Microsoft izmanto sīkfailu atbilstībai, apmeklējiet [Microsoft uzticības centru](https://www.microsoft.com/trust-center). Šajā vietnē varat arī iegūt plašāku informāciju par atbilstības un konfidencialitātes jomām.

Šajā tabulā parādīts pašreizējais sīkfailu atsauču saraksts, ko ievieto Dynamics 365 Commerce vietnes.

| Sīkfaila nosaukums                               | Lietojums                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Saglabāt Microsoft Azure Active Directory (Azure AD) autentifikācijas sīkfailus vienotā pierakstīšanās (SSO). Saglabā šifrētu lietotāja pamatinformāciju (vārds, uzvārds, e-pasts). |
| &#95;msdyn365___cart&#95;                           | Veikalu groza ID, kas tiek izmantots, lai iegūtu preču sarakstu, kas pievienots groza instancei. |
| &#95;msdyn365___ucc&#95;                            | Sīkdatņu atbilstības piekrišanas izsekošana.                          |
| ai_session                                  | Nosaka to, cik lietotāju aktivitāšu sesijas ir iekļāvušas noteiktas programmas lapas un līdzekļus. |
| ai_user                                     | Nosaka, cik cilvēku lieto programmu un tās līdzekļus. Lietotāji tiek skaitīti, izmantojot anonīmus ID. |
| b2cru                                       | Dinamiski saglabā pārvirzīšanas URL.                              |
| JSESSIONID                                  | Izmanto maksājuma savienotāja Adyen, lai saglabātu lietotāja sesiju.       |
| OpenIdConnect.nonce.&#42;                       | Autentifikācija                                               |
| x-ms-cpim-cache:.&#42;                          | Izmanto pieprasījuma stāvokļa uzturēšanai.                      |
| x-ms-cpim-csrf                              | Vairākvietu pieprasījuma viltošanas (CRSF) marķieris, ko izmanto aizsardzībai no CRSF.     |
| x-ms-cpim-dc                                | Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci. |
| x-ms-cpim-rc.&#42;                              | Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci. |
| x-ms-cpim-slice                             | Izmanto, lai maršrutētu pieprasījumus uz atbilstošo ražošanas autentifikācijas servera instanci. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Izmanto SSO sesijas uzturēšanai.                        |
| x-ms-cpim-trans                             | Tiek izmantots, lai izsekotu transakcijas (atvērto ciļņu skaits, kas tiek autentificētas attiecībā uz bizness patērētājam (B2C) vietni), ieskaitot pašreizējo transakciju. |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Vietnes lietotāja sīkfailu piekrišana e-komercijas vietnē 

Ja e-komercijas vietnes līdzeklis vai modulis izmanto nebūtisku sīkfailu, vietnes lietotāja atļauja ir jāsaņem pirms sīkfaila izsekošanas. Lai ļautu vietnes lietotājiem sniegt sīkfailu piekrišanu e-komercijas vietnē, vietnes autoram ir jāpievieno un jākonfigurē sīkfailu piekrišanas modulis lapas virsraksta modulī, lai nodrošinātu, ka piekrišana tiek pieprasīta un saņemta. Lai vietnes lapā varētu atveidot līdzekli vai moduli, kas izmanto nebūtisku sīkfailu, ir jāsaņem vietnes lietotāja piekrišana.

## <a name="additional-resources"></a>Papildu resursi

[Pieejamības līdzekļi un iespējas](accessibility.md)

[Atbilstības pārskats](compliance-overview.md)

[Konfidencialitātes politikas lapas pievienošana](add-privacy-page.md)

[Ar izsekotajām satura izmaiņām saistīto lietotāju ID aizstāšana](replace-IDs-tracked-changes.md)

[Sīkfailu piekrišanas modulis](cookie-consent-module.md) 
 
[Galvenes modulis](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]