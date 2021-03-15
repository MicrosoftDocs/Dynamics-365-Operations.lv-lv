---
title: E-komercijas vietnes izveide
description: Šajā tēmā ir aprakstītas darbības un informācija, kas nepieciešama, lai vietņu veidotājā Dynamics 365 Commerce izveidotu jaunu e-komercijas vietni.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cf084f90d203d84c91ddf7c0d963780b895ef23d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963039"
---
# <a name="create-an-e-commerce-site"></a>E-komercijas vietnes izveide

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstītas darbības un informācija, kas nepieciešama, lai vietņu veidotājā Dynamics 365 Commerce izveidotu jaunu e-komercijas vietni.

Licencējot Dynamics 365 Commerce iespējas, vietnes veidotājam tiks nodrošināta sākuma vieta, kuru varat izmantot kā pamatu savai vietnei. Tomēr, vēloties sākt no jauna vai vēloties izveidot otru vietni, jums vietnes autorēšanas vidē būs jāizveido jauna vietne. 

## <a name="set-up-your-site"></a>Savas vietnes iestatīšana

Vietnes iestatīšanai izpildiet šādas darbības.

1. Atveriet vietņu veidotāja vidi. Saiti uz vietņu veidotāju var atrast pakalpojumos Microsoft Lifecycle Services (LCS), kas atrodas Commerce paredzētajā vides līdzekļu lapā.
1. Vietnes autorēšanas sākumlapā atlasiet **Jauna vietne**.
1. Dialoglodziņā **Jauna vietne** ievadiet tālāk norādīto informāciju.

| Lauks                               | Apraksts |
|-------------------------------------|-------------|
| Vietnes nosaukums                           | Ievadiet parādāmo nosaukumu, kas jāizmanto vietnei vietnes autorēšanas vidē. Šis nosaukums ir redzams tikai autorēšanas vidē, un tas netiks rādīts klientiem. |
| Vietnes administratora drošības grupa | Norādiet Microsoft Azure Active Directory (Azure AD) drošības grupu, kas pārvalda lietotājus, kuriem ir šīs vietnes administratora loma. |
| Noklusējuma kanāls (pārvaldības struktūrvienības numurs) | Atlasiet tiešsaistes veikalu, kuram vietne kalpos kā tīmekļa vitrīna. Ja vēlaties, lai e-komercijas vietne atbalsta vairākus tiešsaistes veikalus, tad pēc vietnes iestatīšanas ir jāsaista veikali ar savu vietni, izvēloties **Vietnes iestatījumi**. |
| Noklusējuma valoda                            | Norādiet noklusējuma valodu šim tiešsaistes veikalam un tirgum. Tiešsaistes veikals var atbalstīt vairākas valodas. Ja vēlaties atbalstīt vairākas valodas šim tiešsaistes veikalam vai citam tiešsaistes veikalam, tad pēc vietnes iestatīšanas varat konfigurēt šo atbalstu, izvēloties **Vietnes iestatījumi**.  |
| Domēns                              | Atlasiet domēna nosaukumu, kas būs šī tiešsaistes veikala domēns. Ja neesat konfigurējis nevienu domēnu pakalpojumā LCS, varat atstāt šo lauku tukšu. Pēc tam, kad jūsu domēns ir konfigurēts pakalpojumā LCS, tas ir jāpievieno tiešsaistes veikalam, izvēloties **Vietnes iestatījumi**.  |
| Ceļš                              | Ja jūsu vietne atbalsta vairāk nekā vienu valodu dotajam domēna vārdam, izmantojiet ceļa lauku, lai izveidotu unikālu vietnes URL šim domēnam un valodu kombinācijai. Ja valoda, ko norādījāt laukā **Noklusējuma valodā**, ir vienīgā valoda, ko atbalstīsiet šim domēnam, vai arī turpmāk būs noklusējuma valoda, pēc tam, kad būsiet lokalizējuši savu vietni citās valodās, iesakām atstāt šo lauku tukšu. |


Pēc vietnes izveides varat pārbaudīt, vai tā ir saistīta ar jūsu tiešsaistes veikalu, atlasot cilni **Preces**. Jābūt redzamam preču klāstam, kas tika piešķirts tiešsaistes veikalam. Lai piekļūtu piešķirtajām precēm pēc kategorijas, varat arī izmantot nolaižamo izvēlni lapas augšējā kreisajā malā.

## <a name="additional-resources"></a>Papildu resursi

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Jauna e-tirdzniecības nomnieka izvietošana](deploy-ecommerce-site.md)

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

[Failu robots.txt pārvaldība](manage-robots-txt-files.md)

[Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

[B2C nomnieka iestatīšana programmā Commerce](set-up-B2C-tenant.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

[Vairāku B2C nomnieku konfigurēšana Commerce vidē](configure-multi-B2C-tenants.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]