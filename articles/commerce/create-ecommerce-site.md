---
title: E-komercijas vietnes izveide
description: Šajā rakstā ir aprakstīti soļi un informācija, kas nepieciešama jaunas e-komercijas vietnes izveidošanai vietu Dynamics 365 Commerce veidotājā.
author: bicyclingfool
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: ea9afd89ce9ff79edbe5bff609b9843026005493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270242"
---
# <a name="create-an-e-commerce-site"></a>E-komercijas vietnes izveide

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīti soļi un informācija, kas nepieciešama jaunas e-komercijas vietnes izveidošanai vietu Dynamics 365 Commerce veidotājā.

Licencējot Dynamics 365 Commerce iespējas, vietnes veidotājam tiks nodrošināta sākuma vieta, kuru varat izmantot kā pamatu savai vietnei. Tomēr, vēloties sākt no jauna vai vēloties izveidot otru vietni, jums vietnes autorēšanas vidē būs jāizveido jauna vietne. 

## <a name="site-creation-prerequisites"></a>Vietas izveides priekšnosacījumi

Vietas veidotāja lietotājam jābūt Microsoft Azure Active Directory (Azure AD) lietotāja kontam, kas iekļauts Azure AD e-komercijas sistēmas administratoriem piešķirtajām drošības grupām. Papildinformāciju skatiet sadaļā [Jauna e-komercijas nomnieka izvietošana](deploy-ecommerce-site.md).

> [!NOTE]
> Azure AD viesa lietotājiem var būt dažādas piekļuves atļaujas jūsu nomniekam Azure AD. Pat ja Azure AD tas ir iekļauts drošības grupā, kas piešķirta e-komercijas sistēmas administratoriem, viesa lietotājam, iespējams, Azure AD **būs** jāpielāgo ārējo lietotāju atļauju iestatījumi, lai izveidotu e-komercijas vietni sistēmā Commerce. 

Lai pielāgotu Azure AD **ārējo lietotāju** iestatījumus, sekojiet šiem soļiem.

1. Azure portālā dodieties uz nomnieku Azure AD.
1. Dodieties **uz Lietotāja iestatījumiem \> Ārējie** lietotāji un atlasiet **saiti Pārvaldīt ārējās sadarbības** iestatījumus. Tiek atvērta lapa Ārējās **sadarbības iestatījumi,** kur var iestatīt viesa lietotāja piekļuvi, viesa ielūdza iestatījumus un sadarbības ierobežojumus. 
1. Pielāgojiet ārējās sadarbības iestatījumus saskaņā ar uzņēmuma drošības politikām. 

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

## <a name="rename-your-site"></a>Vietnes pārdēvēšana

Lai pārdēvētu vietni vietnes veidotājā, sekojiet šiem soļiem.

1. Lai atvērtu vietnes saraksta skatu, atlasiet **Vietas pārslēgšanās** augšējā labajā stūrī un pēc tam atlasiet **Pārvaldīt vietnes**. 
1. Atzīmējiet izvēles rūtiņu blakus vietai, kuru vēlaties pārdēvēt, un pēc tam atlasiet **Pārdēvēt** komandjoslā.
1. Dialoglodziņā Jaunas **vietnes nosaukums** ievadiet jaunās vietnes nosaukumu un pēc tam atlasiet **Labi**. Vietņu saraksts tiks atjaunināts, lai parādītu vietnes jauno nosaukumu.

## <a name="delete-a-site"></a>Vietnes dzēšana

Lai dzēstu vietu vietas veidotājā, sekojiet šiem soļiem.

1. Lai atvērtu vietnes saraksta skatu, atlasiet **Vietas pārslēgšanās** augšējā labajā stūrī un pēc tam atlasiet **Pārvaldīt vietnes**.
1. Atlasiet vietni, kuru vēlaties dzēst, un pēc tam komandjoslā **atlasiet** Dzēst.
1. Dialoglodziņā Dzēst **\<site name\>** ievadiet vietnes nosaukumu un pēc tam atlasiet **Dzēst**.

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
