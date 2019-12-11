---
title: E-komercijas vietnes izveide
description: Šajā tēmā aprakstīti uzdevumi, kas ir saistīti ar jaunas E-komercijas vietnes izveidi programmā Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697133"
---
# <a name="create-an-e-commerce-site"></a>E-komercijas vietnes izveide

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīti uzdevumi, kas ir saistīti ar jaunas E-komercijas vietnes izveidi programmā Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Lai sāktu attīstīt savu E-komercijas vietni, vispirms ir jāizveido jauna vietne vietnes autorēšanas vidē. Pirms varat izveidot jaunu vietni, jāizveido vismaz viens tiešsaistes veikals programmā Dynamics 365 Retail. 

## <a name="set-up-your-site"></a>Savas vietnes iestatīšana

Vietnes iestatīšanai izpildiet šādas darbības.

1. Portālā Microsoft Lifecycle Services (LCS) atlasiet saiti vietnes autorēšanas videi. 
1. Vietnes autorēšanas sākumlapā atlasiet **Jauna vietne**.
1. Dialoglodziņā **Jauna vietne** ievadiet tālāk norādīto informāciju.

| Lauks                               | Apraksts |
|-------------------------------------|-------------|
| Vietnes nosaukums                           | Ievadiet parādāmo nosaukumu, kas jāizmanto vietnei vietnes autorēšanas vidē. Šis nosaukums ir redzams tikai autorēšanas vidē, un tas netiks rādīts klientiem. |
| Vietnes administratora drošības grupa | Norādiet Microsoft Azure Active Directory (Azure AD) drošības grupu, kas pārvalda lietotājus, kuriem ir šīs vietnes administratora loma. |
| Noklusējuma kanāls (pārvaldības struktūrvienības numurs) | Atlasiet tiešsaistes veikalu, kuram vietne kalpos kā tīmekļa vitrīna. Ja vēlaties, lai E-komercijas vietne atbalsta vairākus tiešsaistes veikalus, tad pēc vietnes iestatīšanas ir jāsaista veikali ar savu vietni, izvēloties **Vietnes iestatījumi**. |
| Noklusējuma valoda                            | Norādiet noklusējuma valodu šim tiešsaistes veikalam un tirgum. Tiešsaistes veikals var atbalstīt vairākas valodas. Ja vēlaties atbalstīt vairākas valodas šim tiešsaistes veikalam vai citam tiešsaistes veikalam, tad pēc vietnes iestatīšanas varat konfigurēt šo atbalstu, izvēloties **Vietnes iestatījumi**.  |
| Domēns                              | Atlasiet domēna nosaukumu, kas būs šī tiešsaistes veikala domēns. Ja neesat konfigurējis nevienu domēnu pakalpojumā LCS, varat atstāt šo lauku tukšu. Pēc tam, kad jūsu domēns ir konfigurēts pakalpojumā LCS, tas ir jāpievieno tiešsaistes veikalam, izvēloties **Vietnes iestatījumi**.  |
| Ceļš                              | Ja jūsu vietne atbalsta vairāk nekā vienu valodu dotajam domēna vārdam, izmantojiet ceļa lauku, lai izveidotu unikālu vietnes URL šim domēnam un valodu kombinācijai. Ja valoda, ko norādījāt laukā **Noklusējuma valodā**, ir vienīgā valoda, ko atbalstīsiet šim domēnam, vai arī turpmāk būs noklusējuma valoda, pēc tam, kad būsiet lokalizējuši savu vietni citās valodās, iesakām atstāt šo lauku tukšu. |


Pēc vietnes izveides varat pārbaudīt, vai tā ir saistīta ar jūsu tiešsaistes veikalu, atlasot cilni **Preces**. Jābūt redzamam preču klāstam, kas tika piešķirts tiešsaistes veikalam. Lai piekļūtu piešķirtajām precēm pēc kategorijas, varat arī izmantot nolaižamo izvēlni lapas augšējā kreisajā malā.

## <a name="additional-resources"></a>Papildu resursi

[Tiešsaistes veikala apskats](online-store-overview.md)

[Jaunas e-komercijas vietnes izvietošana](deploy-ecommerce-site.md)

[Tiešsaistes vietnes saistīšana ar kanālu](associate-site-online-store.md)

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

[Autorēšanas mājas lapas pārskats](authoring-home-overview.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)
