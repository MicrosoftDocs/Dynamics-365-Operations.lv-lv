---
title: Atbalsta pievienošana satura piegādes tīklam (CDN)
description: Šajā tēmā ir aprakstīts, kā pievienot satura piegādes tīklu (CDN) jūsu Microsoft Dynamics 365 Commerce videi.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0e888fca4a5401f1df6e61b10358489846ad4b0e
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517212"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Atbalsta pievienošana satura piegādes tīklam (CDN)


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pievienot satura piegādes tīklu (CDN) jūsu Microsoft Dynamics 365 Commerce videi.

## <a name="overview"></a>Pārskats

Iestatot e-komercijas vidi programmā Dynamics 365 Commerce, varat konfigurēt to, lai varētu strādāt ar savu CDN pakalpojumu. 

Jūsu pielāgoto domēnu var iespējot jūsu e-komercijas vides nodrošināšanas procesā. Alternatīvi varat izmantot pakalpojuma pieprasījumu, lai to iestatītu pēc nodrošināšanas procesa pabeigšanas. E-komercijas vides nodrošināšanas process ģenerē resursdatora nosaukumu, kas ir saistīts ar vidi. Šim resursdatora nosaukumam ir šāds formāts, kur \<*e-commerce-tenant-name*\> ir jūsu vides nosaukums.

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

Resursdatora nosaukums vai galapunkts, kas tiek ģenerēts nodrošināšanas procesā, atbalsta drošligzdu slāņa (SSL) sertifikātu tikai \*. commerce.dynamics.com. Tas neatbalsta SSL pielāgotiem domēniem. Tāpēc jums ir jāpārtrauc SSL pielāgotiem domēniem savā CDN un jāpārsūta datplūsma no CDN uz resursdatora nosaukumu vai galapunktu, ko Komercija ir ģenerējusi. 

Turklāt *statika* (JavaScript vai kaskādes stila lapu \[CSS\] faili) no Komercijas tiek nodrošināti no Komercijas ģenerētā galapunkta (\*.commerce.dynamics.com). Statiku var saglabāt kešatmiņā tikai tad, ja resursdatora nosaukums vai galapunkts, ko ģenerējusi Komercija, tiek novietots pēc CDN.

## <a name="set-up-ssl"></a>SSL iestatīšana

Lai palīdzētu nodrošināt, ka SSL ir iestatīts un ka statika saglabāta kešatmiņā, jums ir jākonfigurē savs CDN, lai tas būtu saistīts ar resursdatora nosaukumu, ko ģenerēja Komercija jūsu videi. Sekojošais modelis ir arī jāsaglabā kešatmiņā tikai statikai. 

/\_msdyn365/\_scnr/\*

Pēc tam, kad jūs sniedzat savu Komercijas vidi kopā ar sniegto pielāgoto domēnu, vai pēc tam, kad jūs nodrošināt pielāgotu domēnu jūsu videi, izmantojot pakalpojuma pieprasījumu, norādiet savu pielāgoto domēnu resursdatora nosaukumam vai galapunktam, ko ģenerējusi Komercija.

Kā iepriekš tika minēts, ģenerētais resursdatora nosaukums vai galapunkts atbalsta SSL sertifikātu tikai attiecībā uz \*. commerce.dynamics.com. Tas neatbalsta SSL pielāgotiem domēniem.

## <a name="cdn-services"></a>CDN pakalpojumi

Jebkuru CDN pakalpojumu var izmantot ar Komercijas vidi. Tālāk ir sniegti divi piemēri.

- **Microsoft Azure optimālās ieejas pakalpojums** — Azure CDN risinājums. Papildinformāciju par Azure optimālās ieejas pakalpojumu skatiet tēmā [Azure optimālās ieejas pakalpojuma dokumentācija](https://docs.microsoft.com/azure/frontdoor/)
- **Akamai dinamisks vietnes paātrinātājs** – papildinformāciju skatiet tēmā [Dinamisks vietnes paātrinātājs](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN iestatīšana

CDN iestatīšanas process sastāv no šīm vispārīgajām darbībām.

1. Pievienojiet priekšgala resursdatoru.
1. Konfigurējiet aizmugursistēmas kopu.
1. Iestatiet kārtulas maršrutēšanai un saglabāšanai kešatmiņā.

### <a name="add-a-front-end-host"></a>Priekšgala resursdatora pievienošana

Jebkuru CDN pakalpojumu var izmantot, bet, piemēram, šajā tēmā tiek izmantots Azure optimālās ieejas pakalpojums. 

Lai iegūtu informāciju par to, kā iestatīt Azure optimālās ieejas pakalpojumu, skatiet tēmu [Īsa pamācība: izveidojiet optimālo ieeju augstas pieejamības globālai tīmekļa lietojumprogrammai](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Aizmugursistēmas kopas konfigurēšana Azure optimālās ieejas pakalpojumā

Lai konfigurētu aizmugursistēmas kopu Azure optimālās ieejas pakalpojumā, veiciet tālāk norādītās darbības.

1. Pievienojiet **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** aizmugursistēmas kopai kā pielāgotu resursdatoru, kam ir tukšs aizmugursistēmas resursdatora virsraksts.
1. Zem **Slodzes līdzsvarošana** atstājiet noklusējuma vērtības.

Šajā attēlā redzams dialoglodziņš **Pievienot aizmugursistēmu** Azure optimālās ieejas pakalpojumā ar ievadīto aizmugursistēmas resursdatora virsrakstu.

![Pievienot aizmugursistēmas kopas dialoglodziņu](./media/CDN_BackendPool.png)

Šajā attēlā redzams dialoglodziņš **Pievienot aizmugursistēmas kopa** Azure optimālās ieejas pakalpojumā ar noklusējuma noslodzes balansēšanas vērtībām.

![c](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Kārtulu iestatīšāna Azure optimālās ieejas pakalpojumā

Lai uzstādītu maršrutēšanas kārtulu Azure optimālās ieejas pakalpojumā, veiciet šādas darbības.

1. Pievienojiet maršrutēšanas kārtulu.
1. Laukā **Nosaukums** ievadiet **noklusējuma**.
1. Laukā **Pieņemtais protokols** atlasiet **HTTP un HTTPS**.
1. Laukā **Priekšgala resursdatori** ievadiet **dynamics-ecom-tenant-name.azurefd.net**.
1. Zem **Modeļi saskaņošanai** augšējā laukā ievadiet **/\** _.
1. Sadaļā **Maršruta dati** iestatiet opciju **Maršruta tips** uz **Pārsūtīt**.
1. Laukā **Aizmugursistēmas kopa** atlasiet **e-komercijas aizmugursistēma**.
1. **Pārsūtīšanas protokola** lauka grupā atlasiet opciju **Saskaņot pieprasījumu**. 
1. Iestatiet opciju **URL pārrakstīšana** uz **Atspējots**.
1. Iestatiet opciju **Saglabāšana kešatmiņā** uz **Atspējots**.

Lai iestatītu kešošanas kārtulu Azure optimālās ieejas pakalpojumā, veiciet šādas darbības.

1. Pievienojiet kešošanas kārtulu.
1. Laukā **Nosaukums** ievadiet **statika**.
1. Laukā **Pieņemtais protokols** atlasiet **HTTP un HTTPS**.
1. Laukā **Priekšgala resursdatori** ievadiet **dynamics-ecom-tenant-name.azurefd.net**.
1. Zem **Modeļi saskaņošanai**, augšējā laukā, **/\_msdyn365/\_scnr/\** _.
1. Sadaļā **Maršruta dati** iestatiet opciju **Maršruta tips** uz **Pārsūtīt**.
1. Laukā **Aizmugursistēmas kopa** atlasiet **e-komercijas aizmugursistēma**.
1. **Pārsūtīšanas protokola** lauka grupā atlasiet opciju **Saskaņot pieprasījumu**.
1. Iestatiet opciju **URL pārrakstīšana** uz **Atspējots**.
1. Iestatiet opciju **Saglabāšana kešatmiņā** uz **Atspējots**.
1. Laukā **Vaicājuma virknes kešošanas uzvedība** atlasiet **Saglabāt kešatmiņā katru unikālo vietrādi URL**.
1. **Dinamiskās saspiešanas** lauka grupā atlasiet opciju **Iespējots**.

Šajā attēlā redzams dialoglodziņš **Pievienot kārtulu** Azure optimālās ieejas pakalpojumā.

![Dialoglodziņš Kārtulas pievienošana](./media/CDN_CachingRule.png)

> [!WARNING]
> Ja domēns, ko izmantosiet, jau ir aktīvs un dzīvs, izveidojiet atbalsta biļeti no **Atbalsta** elementa, kas atrodas [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/), lai saņemtu palīdzību nākamajiem soļiem. Papildinformāciju skatiet sadaļā [Iegūt atbalstu Finance and Operations programmām vai Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Ja jūsu domēns ir jauns un nav jau esošs domēns, varat pievienot pielāgotu domēnu Azure optimālās ieejas pakalpojuma konfigurācijai. Tas ļaus tīmekļa datplūsmu vadīt tieši uz jūsu vietni, izmantojot Azure optimālās ieejas instanci. Lai pievienotu pielāgotu domēnu (piemēram, `www.fabrikam.com`), jums ir jākonfigurē Kanoniskais nosaukums (CNAME) domēnam.

Šajā attēlā redzams dialoglodziņš **CNAME konfigurācija** Azure optimālās ieejas pakalpojumā.

![CNAME konfigurācijas dialoglodziņš](./media/CNAME_Configuration.png)

Varat izmantot Azure optimālās ieejas pakalpojumu, lai pārvaldītu sertifikātu, vai arī varat izmantot savu sertifikātu pielāgotajam domēnam.

Šajā attēlā redzams dialoglodziņš **Pielāgota domēna HTTPS** Azure optimālās ieejas pakalpojumā.

![Pielāgota domēna HTTPS dialoglodziņš](./media/Custom_Domain_HTTPS.png)

Lai iegūtu detalizētas instrukcijas par pielāgota domēna pievienošanu Azure optimālās ieejas pakalpojumu, skatiet sadaļu [Pievienot pielāgotu domēnu jūsu optimālās ieejas pakalpojumam](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).

Tagad jūsu CDN ir jābūt pareizi konfigurētam, lai to varētu izmantot kopā ar jūsu Komercijas vietni.

## <a name="additional-resources"></a>Papildu resursi

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Jauna e-tirdzniecības nomnieka izvietošana](deploy-ecommerce-site.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

[Failu robots.txt pārvaldība](manage-robots-txt-files.md)

[Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

[B2C nomnieka iestatīšana programmā Commerce](set-up-B2C-tenant.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

[Vairāku B2C nomnieku konfigurēšana Commerce vidē](configure-multi-B2C-tenants.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]