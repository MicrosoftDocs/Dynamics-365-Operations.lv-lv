---
title: Sīkfailu atbilstība
description: Šajā tēmā aprakstīti apsvērumi sīkdatņu atbilstībai un noklusējuma politikas, kas ir iekļautas Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8eb610eb819dee09a30368257e36dc88f855e985
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088391"
---
# <a name="cookie-compliance"></a>Sīkfailu atbilstība

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīti apsvērumi sīkdatņu atbilstībai un noklusējuma politikas, kas ir iekļautas Microsoft Dynamics 365 Commerce.

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
| \_msdyn365___muid_                            | Tiek izmantots, ja vidē ir aktivizēts eksperiments; utilizēts kā lietotāja identifikators eksperimentu nolūkiem. |
| \_msdyn365___exp_                             | Tiek izmantots, ja vidē ir aktivizēts eksperiments; izmanto, lai mērītu veiktspējas noslodzes līdzsvarošanu.         |
| d365mkt                                       | Izmanto, ja atrašanās vietas noteikšana, lai izsekotu lietotāja IP adresi veikala atrašanās vietas ieteikumiem, ir iespējota Commerce vietnes veidotājā **Vietnes iestatījumi > Vispārīgi > Iespējot uz atrašanās vietu balstītu krātuves noteikšanu**.      |

Ja vietas lietotājs izvēlas kādu no sociālās multivides saitēm vietā, sīkfaili šajā tabulā tiks izsekoti arī viņu pārlūkprogrammā.


| Domēns                      | Sīkfaili               | Apraksts                                                  | Modulis                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | LinkedIn reklāmu ID sinhronizēšana                                      | LinkedIn plūsmas un ieskata tags                                |
| .linkedin.com               | li_sugr                  | Pārlūkprogrammas identifikators                                           | LinkedIn Ieskata tags, ja IP adrese nav norādītajā valstī |
| .linkedin.com               | BizographicsOptOut       | Nosaka izvēles statusu trešo pušu izsekošanai.              | LinkedIn viesu vadīklas un nozares izvēles lapas           |
| .linkedin.com               | \_guid                    | Google reklāmu pārlūkprogrammas identifikators.                            | LinkedIn plūsma                                                |
| .linkedin.com               | li_oatml                 | Dalībnieka netiešais identifikators reklāmguvumu uzskaitei, atkārtotai mērķauditorijas atlasei un analīzei. | LinkedIn reklāmas un Ieskata tagi                                |
| Dažādi pirmās puses domēni | li_fat_id                | Dalībnieka netiešais identifikators reklāmguvumu uzskaitei, atkārtotai mērķauditorijas atlasei un analīzei. | LinkedIn reklāmas un Ieskata tagi                                |
| .adsymptotic.com            | U                        | Pārlūkprogrammas identifikators                                           | LinkedIn Ieskata tags, ja IP adrese nav Norādītajā valstī |
| .linkedin.com                | bcookie                  | Pārlūkprogrammas ID sīkfails                                            | LinkedIn pieprasījumi                                         |
| .linkedin.com                | bscookie                 | Drošais pārlūkprogrammas sīkfails                                        | LinkedIn pieprasījumi                                         |
| .linkedin.com               | lang                     | Iestata noklusējuma atrašanās vietas un valodas iestatījumus.                                 | LinkedIn pieprasījumi                                         |
| .linkedin.com                | lidc                     | Lieto maršrutēšanai.                                             | LinkedIn pieprasījumi                                         |
| .linkedin.com               | aam_uuid                 | Adobe mērķauditorijas vadītāja sīkfails                                                     | Iestatīt ID sinhronizācijai                                              |
| .linkedin.com               | \_ga                      | Google Analytics sīkfails                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google Analytics sīkfails                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google Analytics sīkfails                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Sīkfailā ir norādīts tā lietotāja ID, kas pašlaik ir pierakstījies.  |   Facebook                                                           |
| .facebook.com               | datr                     | Tiek izmantots, lai identificētu tīmekļa pārlūkprogrammu, kas tiek izmantota, lai pievienotos Facebook neatkarīgi no lietotāja, kurš ir pierakstījies. | Facebook                                                             |
| .facebook.com               | wd                       | Saglabā pārlūka loga dimensijas un Facebook to izmanto, lai optimizētu lapas atveidošanu. | Facebook                                                             |
| .facebook.com               | xs                       | Divciparu numurs, kas apzīmē sesijas numuru. Otrā vērtības daļa ir sesijas noslēpums. |  Facebook                                                            |
| .facebook.com               | fr                       | Satur unikālu pārlūka un lietotāja ID, kas tiek izmantots mērķētai reklāmai. |  Facebook                                                            |
| .facebook.com               | sb                       | Tiek lietots, lai uzlabotu Facebook draugu ieteikumus.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Sīkfailā ir norādīts tā lietotāja ID, kas pašlaik ir pierakstījies.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Sīkfailā ir norādīts tā lietotāja ID, kas pašlaik ir pierakstījies.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Sīkfails satur lapas, kad lietotājs atlasa Pinterest pogu.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Sīkfails satur lapas, kad lietotājs atlasa Pinterest pogu.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Ietver lietotāja ID un laikspiedolu, kad sīkfails tika izveidots. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Sīkfails satur lapas, kad lietotājs atlasa Pinterest pogu.      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Sīkfails satur lapas, kad lietotājs atlasa Pinterest pogu.      | Pinterest                                                             |
| .pinterest.com              | Lokāla datu krātuve            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Pakalpojumu Darbinieki          |                                                              |  Pinterest                                                            |


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
