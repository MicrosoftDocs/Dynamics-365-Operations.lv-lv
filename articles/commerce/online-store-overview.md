---
title: E-tirdzniecības vietnes pārskats
description: Šajā tēmā sniegts pārskats par e-tirdzniecības vietņu atbalstu programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 55c40029082e49c1fbc9d9d5e9361218e5ddc5a0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022476"
---
# <a name="e-commerce-site-overview"></a>E-komercijas vietnes apskats

[!include [banner](includes/banner.md)]

Šajā tēmā sniegts pārskats par e-tirdzniecības vietņu atbalstu programmā Microsoft Dynamics 365 Commerce. Tajā ir iekļauta informācija par to, kā e-tirdzniecības tiešsaistes veikali tiek inicializēti un pārvaldīti risinājumā Dynamics 365 Commerce. Tajā ir sniegtas arī saites uz papildinformāciju par tiešsaistes veikaliem un informāciju par to, kā iestatīt un konfigurēt e-tirdzniecības vietni. Kaut arī šis temats aptver daudzus pamatprincipus, tas neaptver visu, kas nepieciešams, lai iestatītu ražošanas e-tirdzniecības vietni. Papildu tēmas var atrast Dynamics 365 Commerce dokumentācijā.

## <a name="online-store-channel"></a>Tiešsaistes veikala kanāls

Pirms varat izveidot savu vietni pakalpojumā Dynamics 365 Commerce, ir jāizveido vismaz viens tiešsaistes veikala kanāls. Papildinformāciju skatiet šeit: [Tiešsaistes kanāla iestatīšana](channel-setup-online.md). 

Pakalpojumā Dynamics 365 Commerce jūs varat izmantot tiešsaistes veikala kanālu, lai noteiktu preces, cenas, valodas, maksājumu metodes, piegādes režīmus, izpildes centrus un citus tiešsaistes pieredzes aspektus, kas ir pieejami jūsu klientiem.

Lai sāktu darbu Dynamics 365 Commerce, ir jāiestata tikai viens tiešsaistes veikala kanāls. Tomēr viena e-komercijas vietne var nodrošināt tiešsaistes pieredzi vairākiem tiešsaistes veikaliem. Piemēram, ja vairāki tiešsaistes veikali ir iestatīti, lai atbalstītu dažādus ģeogrāfiskos reģionus, var izmantot vienu e-komercijas lapu kopu, lai nodrošinātu katra veikala definēto unikālo pieredzi. Papildinformāciju par to, kā konfigurēt vietni, lai atbalstītu vairākus tiešsaistes veikalus, skatiet sadaļā [Tiešsaistes vietnes saistīšana ar kanālu ](associate-site-online-store.md).

Kad tiešsaistes veikals ir izveidots, to var saistīt ar Dynamics 365 Commerce vietni, kas kalpos kā jūsu tiešsaistes vietne. Papildinformāciju par tiešsaistes veikaliem un to iestatīšanu skatiet sadaļā [Tiešsaistes veikalu iestatīšana](/dynamics365/unified-operations/retail/online-stores).

## <a name="deploy-a-new-e-commerce-tenant"></a>Jauna e-tirdzniecības nomnieka izvietošana

E-tirdzniecības vietnes inicializēšanas laikā ir jānorāda domēna nosaukums. Plašāku informāciju par domēniem Commerce skatiet sadaļā [Konfigurēt jūsu domēna nosaukumu](configure-your-domain-name.md) un [Domēni risinājumā Dynamics 365 Commerce](domains-commerce.md). Lai izvietotu jaunu e-tirdzniecības nomnieku, izmantojot [Microsoft Dynamics Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), veiciet darbības, lai [Izvietotu jaunu e-tirdzniecības nomnieku](deploy-ecommerce-site.md). Pēc tam, kad jūsu e-tirdzniecības nomnieks ir iestatīts LCS, tiks sniegta saite uz Commerce Site Builder. Pēc tam varat izmantot Commerce Site Builder, lai inicializētu un konfigurētu e-tirdzniecības vietnes.

## <a name="initialize-your-e-commerce-site"></a>Jūsu e-tirdzniecības vietnes inicializēšana

Kad uzsākat Commerce Site Builder no LCS, tiek parādīta lapa **Vietnes**. Šajā lapā ir iekļautas divas iepriekš konfigurētas vietnes - **noklusējums** un **fabrikam**, kā parādīts sekojošajā ilustrācijas piemērā.

![Vietnes lapa Commerce Site Builder](media/e-commerce-site-01.png)

Kad atlasāt kādu no šīm vietnēm, saņemsit aicinājumu atlasīt domēna nosaukumu, noklusējuma tiešsaistes veikala kanālu, atlasītā kanāla atbalstīto valodu un ceļu. Ja tiek izmantots tikai viens kanāls, šo ceļu varat atstāt tukšu. Papildu tiešsaistes veikala kanālus vai valodas var konfigurēt vēlāk Commerce Site Builder. Katram papildu kanālam vai valodai būs nepieciešams unikāls ceļš. Piemēram, jums ir divi tiešsaistes kanāli, kas ir saistīti ar vienu vietu un domēna nosaukums vietnei ir `www.fabrikam.com`. Šādā gadījumā ceļš vienam kanālam var būt noklusētā vērtība, kam nav ceļa (`https://www.fabrikam.com`), un otru kanālu var iestatīt uz jaunu ceļu, piemēram, **site2**, kuram būs vietrādis URL `https://www.fabrikam.com/site2`. Sekojošajā attēlā parādīts vietnes inicializēšanas dialoglodziņa piemērs Commerce Site Builder.

![Vietnes inicializēšanas dialoglodziņš Commerce Site Builder](media/e-commerce-site-02.png)

Lapā **Vietnes** ir ietverta arī poga **Jauna vietne**. Dialoglodziņš, kas parādās, kad atlasāt šo pogu, atgādina vietnes inicializēšanas dialoglodziņu, bet tas tiek izmantots, lai izveidotu jaunu vietni. Jaunas vietnes ir tukšas. Tajās nav iekļautas tās pašas noklusējuma veidnes, fragmenti, lapas un attēli, kas tiek nodrošināti **noklusējuma** un **fabrikam** vietnēm. Tomēr, ja nepieciešams, varat atvērt atbalsta biļeti, lai pieprasītu noklusējuma satura kopijas pievienošanu jaunai tukšai vietnei. Papildinformāciju skatiet [E-tirdzniecības vietnes izveide](create-ecommerce-site.md).

Pēc jaunas vietnes inicializēšanas tiek parādīta Commerce Site Builder **Sākumlapa**. Šajā lapā ir iekļautas saites uz kopējām darbībām un virzības saturu, kā parādīts piemērā sekojošajā ilustrācijā.

![Saites Commerce Site Builder sākumlapu](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Modificēt tiešsaistes veikala kanālus vai pievienot tiešsaistes veikala kanālus e-tirdzniecības vietnei

Kad e-tirdzniecības vietne ir izveidota, varat mainīt kanālu, ar kuru tas ir saistīts, izpildot darbības, kas saistītas ar [e-tirdzniecības vietnes saistīšana ar tiešsaistes kanālu](associate-site-online-store.md). Piemērā nākamajā attēlā ir parādīts, kā kanālu pārvaldības struktūrvienības numuru (OUN) var mainīt lapā **Kanāli** (**Vietnes iestatījumi \> Kanāli**). Pēc tam, kad esat beidzis izmaiņu veikšanu, noteikti atlasiet **Saglabāt un publicēt**. Šādā veidā tiek nodrošināts, ka izmaiņas tiek publicētas.

![Kanālu lapa Commerce Site Builder](media/e-commerce-site-04.png)

Varat pievienot jaunus kanālus, atlasot **Pievienot kanālu**. Lai kanālam pievienotu jaunas valodas, atlasiet kanālu un pēc tam atlasiet opciju **Pievienot lokalizāciju** kanāla dialoglodziņā, kas parādās. Pirms lokalizācijas ir redzamas dialoglodziņā, tās ir jākonfigurē tiešsaistes veikala kanālam Commerce Headquarters.

![Kanāla dialoglodziņš Commerce Site Builder](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Iestatīt Azure B2C nomnieku

Dynamics 365 Commerce izmanto Azure Active Directory (Azure AD) kompercpraksi pret patērētājiem stratēģiju (B2C), lai atbalstītu lietotāja akreditācijas datus un autentifikācijas plūsmas. Lai iegūtu informāciju par to, kā iestatīt jūsu Azure B2C nomnieku, skatiet sadaļu [B2C nomnieka iestatīšana Commerce](set-up-b2c-tenant.md), [Iestatīt pielāgotas lapas lietotāja pierakstīšanās](custom-pages-user-logins.md) un [Konfigurēt vairākus B2C nomniekus Commerce vidē](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Noklusējuma vietnes lapu apskats

**Noklusējuma** un **fabrikam** vietnes ietver iepriekš konfigurētas veidnes, fragmentus un lapas, lai palīdzētu uzsākt darbu. Papildinformāciju skatiet tālāk norādītajās tēmās.

- [Sākumlapas pārskats](quick-tour-home-page.md)
- [Preču papildinformācijas lapas pārskats](quick-tour-pdp.md)
- [Groza un norēķināšanās lapu pārskats](quick-tour-cart-checkout.md)
- [Konta pārvaldības lapu pārskats](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Vietnes iestatījumu pārvaldība

Informāciju par to, kā pārvaldīt jūsu vietnes iestatījumus, skatiet tālāk norādītajās tēmās.

- [Lietotāju un lomu pārvaldība e-tirdzniecībā](manage-ecommerce-users-roles.md)
- [Meklētājprogrammas optimizēšanas (SEO) apsvērumi jūsu vietnei](/search-engine-optimization-considerations.md)
- [Satura drošības politikas (CSP) pārvaldība](manage-csp.md)
- [Vietnes dizaina atlase](select-site-theme.md)

## <a name="manage-site-content"></a>Vietnes satura pārvaldība

Informāciju par to, kā pārvaldīt vietnes saturu, skatiet tālāk norādītajās tēmās.

- [Lapas modeļa glosārijs](page-elements-overview.md)
- [Dokumenta stāvokļi un dzīves cikls](document-states-overview.md)
- [Veidnes un izkārtojums](templates-layouts-overview.md)
- [Darbs ar fragmentiem](work-with-fragments.md)
- [Darbs ar moduļiem](work-with-modules.md)
- [Pārskats par digitālo līdzekļu pārvaldību](dam-overview.md)
- [Moduļu bibliotēkas pārskats](starter-kit-overview.md)

## <a name="additional-resources"></a>Papildu resursi

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Jaunas e-tirdzniecības vietnes izvietošana](deploy-ecommerce-site.md)

[Tiešsaistes vietnes saistīšana ar kanālu](associate-site-online-store.md)

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]