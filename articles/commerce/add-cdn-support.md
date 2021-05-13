---
title: Atbalsta pievienošana satura piegādes tīklam (CDN)
description: Šajā tēmā aprakstīts, kā pievienot satura piegādes tīklu savai Microsoft Dynamics 365 Commerce videi.
author: brianshook
ms.date: 03/17/2021
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
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936834"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Atbalsta pievienošana satura piegādes tīklam (CDN)

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā pievienot satura piegādes tīklu savai Microsoft Dynamics 365 Commerce videi.

Iestatot e-komercijas vidi programmā Dynamics 365 Commerce, varat konfigurēt to, lai varētu strādāt ar savu CDN pakalpojumu. 

Jūsu pielāgoto domēnu var iespējot jūsu e-komercijas vides nodrošināšanas procesā. Alternatīvi varat izmantot pakalpojuma pieprasījumu, lai to iestatītu pēc nodrošināšanas procesa pabeigšanas. E-komercijas vides nodrošināšanas process ģenerē resursdatora nosaukumu, kas ir saistīts ar vidi. Šim resursdatora nosaukumam ir šāds formāts, kur \<*e-commerce-tenant-name*\> ir jūsu vides nosaukums.

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

Resursdatora nosaukums vai galapunkts, kas tiek ģenerēts nodrošināšanas procesā, atbalsta drošligzdu slāņa (SSL) sertifikātu tikai \*. commerce.dynamics.com. Tas neatbalsta SSL pielāgotiem domēniem. Tāpēc jums ir jāpārtrauc SSL pielāgotiem domēniem savā CDN un jāpārsūta datplūsma no CDN uz resursdatora nosaukumu vai galapunktu, ko Komercija ir ģenerējusi. 

Turklāt *statika* (JavaScript vai kaskādes stila lapu \[CSS\] faili) no Komercijas tiek nodrošināti no Komercijas ģenerētā galapunkta (\*.commerce.dynamics.com). Statiku var saglabāt kešatmiņā tikai tad, ja resursdatora nosaukums vai galapunkts, ko ģenerējusi Komercija, tiek novietots pēc CDN.

## <a name="set-up-ssl"></a>SSL iestatīšana

Pēc tam, kad jūs sniedzat savu Commerce vidi kopā ar sniegto pielāgoto domēnu, vai pēc tam, kad jūs nodrošināt pielāgotu domēnu jūsu videi, izmantojot pakalpojuma pieprasījumu, norādiet savu pielāgoto domēnu resursdatora nosaukumam vai galapunktam, ko ģenerēja Commerce.

Kā iepriekš tika minēts, ģenerētais resursdatora nosaukums vai galapunkts atbalsta SSL sertifikātu tikai attiecībā uz \*. commerce.dynamics.com. Tas neatbalsta SSL pielāgotiem domēniem.

## <a name="cdn-services"></a>CDN pakalpojumi

Jebkuru CDN pakalpojumu var izmantot ar Komercijas vidi. Tālāk ir sniegti divi piemēri.

- **Microsoft Azure optimālās ieejas pakalpojums** — Azure CDN risinājums. Papildinformāciju par Azure optimālās ieejas pakalpojumu skatiet tēmā [Azure optimālās ieejas pakalpojuma dokumentācija](/azure/frontdoor/)
- **Akamai dinamisks vietnes paātrinātājs** – papildinformāciju skatiet tēmā [Dinamisks vietnes paātrinātājs](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN iestatīšana

CDN iestatīšanas process sastāv no šīm vispārīgajām darbībām.

1. Pievienojiet priekšgala resursdatoru.
1. Konfigurējiet aizmugursistēmas kopu.
1. Maršrutēšanas noteikumu iestatīšana.

### <a name="add-a-front-end-host"></a>Priekšgala resursdatora pievienošana

Jebkuru CDN pakalpojumu var izmantot, bet, piemēram, šajā tēmā tiek izmantots Azure optimālās ieejas pakalpojums. 

Lai iegūtu informāciju par to, kā iestatīt Azure optimālās ieejas pakalpojumu, skatiet tēmu [Īsa pamācība: izveidojiet optimālo ieeju augstas pieejamības globālai tīmekļa lietojumprogrammai](/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Aizmugursistēmas kopas konfigurēšana Azure optimālās ieejas pakalpojumā

Lai konfigurētu aizmugursistēmas kopu Azure optimālās ieejas pakalpojumā, veiciet tālāk norādītās darbības.

1. Pievienojiet **&lt;ecom-nomnieka nosaukumu&gt;.commerce.dynamics.com** servera kopai kā pielāgotu resursdatoru, kam ir servera resursdatora virsraksts, kas ir tāds pats kā **&lt;ecom-nomnieka nosaukums&gt;.commerce.dynamics.com**.
1. Zem **Slodzes līdzsvarošana** atstājiet noklusējuma vērtības.
1. Deaktivēt veselības pārbaudes aizmugursistēmas kopai.

Šajā attēlā redzams dialoglodziņš **Pievienot aizmugursistēmu** Azure optimālās ieejas pakalpojumā ar ievadīto aizmugursistēmas resursdatora virsrakstu.

![Pievienot aizmugursistēmas kopas dialoglodziņu](./media/CDN_BackendPool.png)

Šajā attēlā redzams dialoglodziņš **Pievienot aizmugursistēmas kopa** Azure optimālās ieejas pakalpojumā ar noklusējuma noslodzes balansēšanas vērtībām.

![Pievienot aizmugursistēmas kopas dialoglodziņa turpinājumu](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Noteikti atspējojiet **Veselības zondes**, iestatot savu Azure Front Door pakalpojumu pakalpojumam Commerce.


### <a name="set-up-rules-in-azure-front-door-service"></a>Kārtulu iestatīšāna Azure optimālās ieejas pakalpojumā

Lai uzstādītu maršrutēšanas kārtulu Azure optimālās ieejas pakalpojumā, veiciet šādas darbības.

1. Pievienojiet maršrutēšanas kārtulu.
1. Laukā **Nosaukums** ievadiet **noklusējuma**.
1. Laukā **Pieņemtais protokols** atlasiet **HTTP un HTTPS**.
1. Laukā **Priekšgala resursdatori** ievadiet **dynamics-ecom-tenant-name.azurefd.net**.
1. Zem **Modeļi saskaņošanai** augšējā laukā ievadiet **/\***.
1. Sadaļā **Maršruta dati** iestatiet opciju **Maršruta tips** uz **Pārsūtīt**.
1. Laukā **Aizmugursistēmas kopa** atlasiet **e-komercijas aizmugursistēma**.
1. **Pārsūtīšanas protokola** lauka grupā atlasiet opciju **Saskaņot pieprasījumu**. 
1. Iestatiet opciju **URL pārrakstīšana** uz **Atspējots**.
1. Iestatiet opciju **Saglabāšana kešatmiņā** uz **Atspējots**.


> [!WARNING]
> Ja domēns, ko izmantosiet, jau ir aktīvs un dzīvs, izveidojiet atbalsta biļeti no **Atbalsta** elementa, kas atrodas [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/), lai saņemtu palīdzību nākamajiem soļiem. Papildinformāciju skatiet sadaļā [Iegūt atbalstu Finance and Operations programmām vai Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Ja jūsu domēns ir jauns un nav jau esošs domēns, varat pievienot pielāgotu domēnu Azure optimālās ieejas pakalpojuma konfigurācijai. Tas ļaus tīmekļa datplūsmu vadīt tieši uz jūsu vietni, izmantojot Azure optimālās ieejas instanci. Lai pievienotu pielāgotu domēnu (piemēram, `www.fabrikam.com`), jums ir jākonfigurē Kanoniskais nosaukums (CNAME) domēnam.

Šajā attēlā redzams dialoglodziņš **CNAME konfigurācija** Azure optimālās ieejas pakalpojumā.

![CNAME konfigurācijas dialoglodziņš](./media/CNAME_Configuration.png)

Varat izmantot Azure optimālās ieejas pakalpojumu, lai pārvaldītu sertifikātu, vai arī varat izmantot savu sertifikātu pielāgotajam domēnam.

Šajā attēlā redzams dialoglodziņš **Pielāgota domēna HTTPS** Azure optimālās ieejas pakalpojumā.

![Pielāgota domēna HTTPS dialoglodziņš](./media/Custom_Domain_HTTPS.png)

Lai iegūtu detalizētas instrukcijas par pielāgota domēna pievienošanu Azure optimālās ieejas pakalpojumu, skatiet sadaļu [Pievienot pielāgotu domēnu jūsu optimālās ieejas pakalpojumam](/azure/frontdoor/front-door-custom-domain).

Tagad jūsu CDN ir jābūt pareizi konfigurētam, lai to varētu izmantot kopā ar jūsu Komercijas vietni.

## <a name="additional-resources"></a>Papildu resursi

[Satura piegādes tīkla ieviešanas opcijas](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]