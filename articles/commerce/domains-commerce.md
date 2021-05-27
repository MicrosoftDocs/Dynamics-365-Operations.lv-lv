---
title: Domēni programmā Dynamics 365 Commerce
description: Šajā tēmā aprakstīts, kā domēni tiek apstrādāti pakalpojumā Microsoft Dynamics 365 Commerce.
author: BrShoo
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 0a494a36d1d8fa55521c416efd4262d860e1a708
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022840"
---
# <a name="domains-in-dynamics-365-commerce"></a>Domēni programmā Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā domēni tiek apstrādāti pakalpojumā Microsoft Dynamics 365 Commerce.

Domēni ir tīmekļa adreses, ko izmanto, lai naviģētu uz Dynamics 365 Commerce vietnēm tīmekļa pārlūkā. Jūs kontrolējat sava domēna pārvaldību ar izvēlēto domēna nosaukuma servera (Domain Name Server - DNS) nodrošinātāju. Domēniem ir atsauces visā Dynamics 365 Commerce vietnes veidotājā, lai koordinētu, kā vietnei varēs piekļūt pēc publicēšanas. Šajā tēmā ir aplūkots, kā tiek apstrādāti domēni un kā uz tiem tiek sniegtas atsauces visā Commerce vietnes izstrādes un palaišanas cikla laikā.

## <a name="provisioning-and-supported-host-names"></a>Nodrošināšana un atbalstītie resursdatoru nosaukumi

Nodrošinot e-komercijas vidi [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), tiek izmantots lodziņš **Atbalstītie resursdatora nosaukumi** e-komercijas nodrošināšanas ekrānā, lai ievadītu domēnus, kas tiks saistīti ar izvietoto Commerce vidi. Šie domēni būs uz klientu vērsti domēna nosaukuma servera (DNS) nosaukumi, kuros tiks viesotas e-komercijas vietnes. Ievadot domēnu šajā posmā, netiek sākta domēna trafika pāradresācija uz Dynamics 365 Commerce. Trafiks domēnam tiks maršrutēts uz Commerce galapunktu, kad DNS CNAME ieraksts tiek atjaunināts, lai izmantotu Commerce galapunktu ar šo domēnu.

> [!NOTE]
> Vairākus domēnus var ievadīt lodziņā **Atbalstītie resursdatora nosaukumi** , atdalot tos ar semikolu.

Sekojošajā attēlā redzams LCS e-komercijas nodrošināšanas ekrāns ar iezīmētu lodziņu **Atbalstītie resursdatora nosaukumi**. 

![LCS e-komercijas nodrošināšanas ekrāns ar izceltu lodziņu **Atbalstītie resursdatora nosaukumi**](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Varat izveidot pakalpojuma pieprasījumu, lai videi pievienotu papildu domēnus, ja nodrošināšana jau ir notikusi. Lai izveidotu pakalpojuma pieprasījumu LCS, jūsu vidē atveriet **Atbalsts \> Atbalsta jautājumi** un atlasiet **Iesniegt incidentu**.

## <a name="commerce-generated-urls"></a>Commerce ģenerētie vietrāži URL

Kad tiek nodrošināta Dynamics 365 Commerce e-komercijas vide, Commerce ģenerēs vietrādi URL, kas būs vides darba adrese. Šim vietrādim URL ir atsauce uz e-komercijas vietnes saiti, kas norādīta LCS pēc vides nodrošināšanas. Commerce ģenerētie vietrāži URL ir `https://<e-commerce tenant name>.commerce.dynamics.com`formātā , kur e-komercijas nomnieka nosaukums ir nosaukums, kas ievadīts LCS Commerce videi.

Ražošanas vietnes resursdatoru nosaukumus var izmantot arī smilškastes vidē. Šī opcija ir ideāli piemērota, ja kopēsit vietni no smilškastes vides uz ražošanu.

## <a name="site-setup"></a>Vietnes iestatījumi

Pēc e-komercijas vides nodrošināšanas ir jāiestata vietnes Commerce vietņu veidotājā, lai saistītu savu vietni ar darba URL.

Pirmoreiz iestatot vietni vietnes veidotājā, tiks atvērts dialoglodziņš **Vietnes iestatīšana** .

Sekojošajā attēlā ir parādīts dialoglodziņš **Vietnes iestatīšana** vietnei ar nosaukumu "noklusējums", kad piekļūstat vietnei pirmo reizi vietnes veidotājā.

![Dialoglodziņš **Vietnes iestatīšana**](./media/Domains_SetupyoursiteScreen.png)

Lodziņš **Atlasīt domēnu** ļauj saistīt vienu no atbalstītajiem resursdatora nosaukumiem, kas tiek nodrošināti jūsu vietnei LCS, jūsu vietnei vietnes veidotājā.

Lodziņu **Ceļš** var atstāt tukšu, vai var pievienot papildu ceļu virkni, kas tiks parādīta darba vietrādī URL. Atstājot lodziņu **Ceļš** tukšu, pamata Commerce ģenerēts vietrādis URL tiek saistīts ar vietni, kas tiek iestatīta vietnes veidotājā. Ceļiem ir jābūt unikāliem katram vietņu/domēnu pārim. Izvēlētās vietnes un domēna ietvaros tikai viena vietne vidē var izmantot tukšu ceļu vai būt saistītai ar unikālu ceļu virkni. Jebkura virkne, kas pievienota laukam **Ceļš** vietnes iestatīšanas laikā, kļūs par pamata Commerce ģenerēta vietrāža URL apakšceļu, kas tiek izmantots, lai piekļūtu vietnei tīmekļa pārlūkprogrammā.

> [!NOTE]
> Ceļš tiek saukts arī par **Atbilstības ceļš**, kad tiek pievienots kanāls vietnes veidotāja konfigurācijas sadaļā **Vietnes iestatījumi \> Kanāli** .

Piemēram, ja vietnes veidotājā ir vietne, kas saukta "fabrikam", kas atrodas e-komercijas nomniekā ar nosaukumu "xyz", un, ja iestatāt vietni ar tukšu ceļu, piekļūsiet publicētajam vietnes saturam tīmekļa pārlūkā, dodoties tieši uz pamata Commerce ģenerēto vietrādi URL:

`https://xyz.commerce.dynamics.com`

Pārmaiņus, ja šīs vietnes uzstādīšanas laikā esat pievienojis ceļu “fabrikam”, publicētajam vietnes saturam var piekļūt tīmekļa pārlūkprogrammā, izmantojot šādu vietrādi URL:

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a>Lapas un vietrāži URL

Pēc tam, kad jūsu vietne ir iestatīta ar ceļu, visi vietrāži URL, kas saistīti ar lapām vietnes veidotājā, vietnei tiks balstīti uz darba vietrādi URL (Commerce ģenerēto vietrādi URL vai Commerce ģenerēto vietrādi URL un ceļu). Jauna vietrāža URL izveide vietnes veidotājā (**URL /> +Jauns**), atlasot lapu no saraksta, dialoglodziņā **Jauns vietrādis URL** un ievadot URL ceļu šai lapai, šis vietrādis URL tiks saistīts ar atlasīto lapu. URL ceļa vērtība pēc tam, lai piekļūtu lapai, tiek pievienota vietnes darba vietrādim URL un ir apzīmēta kā `./<URL path>` URL sarakstā lapā **Vietrāži URL** vietnes veidotājā.

Sekojošajā attēlā redzams dialoglodziņš **Jauns vietrādis URL** vietnes veidotājā ar URL ceļa piemēru. 

![Dialoglodziņš **Jauns vietrādis URL** vietnes veidotājā](./media/Domains_PageSetup2a.png)

Sekojošajā attēlā redzama lapa **Vietrāži URL** vietnes veidotājā ar URL piemēru, kas ir izcelts sarakstā.

![Izpildīt lietotāja plūsmas opciju politikas plūsmā](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Domēni vietnes veidotājā

Atbalstīto resursdatoru nosaukumu vērtības ir pieejamas, lai, iestatot vietni, tās būtu saistītas kā domēns. Atlasot atbalstītā resursdatora nosaukuma vērtību kā domēnu, tiks parādīts izvēlētais domēns, uz kuru ir atsauce vietņu veidotājā. Šis domēns ir tikai atsauce Commerce vidē, dzīvā datplūsma šim domēnam vēl netiks pārsūtīta uz Dynamics 365 Commerce.

Ja strādājat ar vietnēm vietnes veidotājā, ja jums ir divas vietnes, kas iestatītas ar diviem dažādiem domēniem, varat pievienot atribūtu **?domēns=** jūsu darba vietrādim URL, lai piekļūtu publicētajai vietnes informācijai pārlūkprogrammā.

Piemēram, vide "xyz" ir nodrošināta, un divas vietnes ir izveidotas un saistītas ar vietnes veidotāju: viens ar domēnu `www.fabrikam.com` un otrs ar domēnu `www.constoso.com`. Katra vietne tika iestatīta, izmantojot tukšu ceļu. Šīm divām vietnem pēc tam var piekļūt tīmekļa pārlūkprogrammā, lietojot atribūtu **?domēns=** :
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

Ja domēna vaicājuma virkne netiek norādīta vidē ar vairākiem domēniem, Commerce izmanto pirmo norādīto domēnu. Piemēram, ja ceļš "fabrikam" vietas iestatīšanas laikā tika nodrošināts pirmais, vietrādi URL `https://xyz.commerce.dynamics.com` var izmantot, lai piekļūtu publicētajai vietnes satura vietnei `www.fabrikam.com`.

## <a name="traffic-forwarding-in-production"></a>Satiksmes pārsūtīšana ražošanā

Varat simulēt vairākus domēnus, izmantojot domēna vaicājuma virknes parametrus pašā commerce.dynamics.com galapunktā. Bet, ja jums ir jābūt tiešraidē ražošanā, jums ir jānosūta trafiks jūsu pielāgotajam domēnam uz `<e-commerce tenant name>.commerce.dynamics.com` galapunktu.

Galapunkts `<e-commerce tenant name>.commerce.dynamics.com` neatbalsta pielāgotus domēna drošligzdu slāņus (Secure Sockets Layers - SSLs), tāpēc ir jāiestata pielāgoti domēni, izmantojot front door pakalpojumu vai satura piegādes tīklu (content delivery network - CDN). 

Lai iestatītu pielāgotus domēnus, izmantojot front door pakalpojumu vai CDN, ir divas opcijas:

- Iestatiet front door pakalpojumu, piemēram, Azure Front Door, lai apstrādātu priekšgala trafiku un pievienotos jūsu Commerce videi. Tas nodrošina lielāku kontroli pār domēnu un sertifikātu pārvaldību, kā arī detalizētākas drošības politikas.
- Izmantot Commerce nodrošināto Azure Front Door instanci. Tas prasa koordinēt darbību ar Dynamics 365 Commerce grupu domēna verifikācijai un iegūt SSL sertifikātus jūsu ražošanas domēnam.

Informāciju par to, kā tieši iestatīt CDN pakalpojumu, skatiet [Pievienot atbalstu satura piegādes tīklam (CDN)](add-cdn-support.md).

Lai izmantotu Commerce nodrošināto Azure Front Door instanci, jums ir jāizveido pakalpojuma pieprasījums pēc palīdzības CDN iestatīšanā no Commerce ievadapmācības grupas. 

- Jums būs jānorāda uzņēmuma nosaukums, ražošanas domēns, vides ID un ražošanas e-komercijas nomnieka nosaukums. 
- Jums būs jāapstiprina, ja šis ir esošs domēns (tiek izmantots pašreiz aktīvajai vietnei) vai jauns domēns. 
- Jaunam domēnam domēna verifikāciju un SSL sertifikātu var iegūt vienā solī. 
- Domēnam, kas apkalpo esošu vietni, ir jāveic daudzpakāpju process, lai izveidotu domēna verifikāciju un SSL sertifikātu. Šim procesam ir 7 darba dienu pakalpojuma līmeņa vienošanās (service level agreement - SLA) domēnam, lai nokļūtu tiešraidē, jo tas ietver vairākus secīgus soļus.

Lai izveidotu pakalpojuma pieprasījumu LCS, jūsu vidē atveriet **Atbalsts \> Atbalsta jautājumi** un atlasiet **Iesniegt incidentu**.

> [!NOTE]
> Pielāgoti domēni ar SSL tiek atbalstīti tikai ražošanas vidēs. Neražošanas vidēm, piemēram, smilškastes un lietotāja akceptēšanas pārbaudes (user acceptance testing - UAT) vidēm, izmantojiet Commerce ģenerēto vietrādi URL, lai piekļūtu publicētajam saturam tīmekļa pārlūkprogrammā.

## <a name="ssl-certificate-process"></a>SSL sertifikāta process

Kad pakalpojuma pieprasījums ir iesniegts, Commerce grupa ar jums koordinēs tālāk minētās darbības.

Jauniem domēniem:
- Commerce grupa iestatīs Azure Front Door instanci (Commerce viesota).
- Pēc tam Commerce grupa nodrošinās CNAME ierakstu, lai norādītu jūsu pielāgoto domēnu.
- Pēc CNAME ieraksta atjaunināšanas Commerce viesota Azure Front Door instance varēs pārbaudīt domēna īpašumtiesības un iegūt SSL sertifikātu.

Esošajiem/aktīvajiem domēniem:
- Commerce grupa dos norādījumus pievienot `afdverify.<custom-domain>` CNAME ierakstu, lai to sniegtu jūsu domēna DNS nodrošinātājam.
- Pēc pabeigšanas, Commerce grupa pievienos domēnu Azure Front Door instancei un nodrošinās papildu DNS TXT ierakstus, kas jāpievieno domēna DNS.
- Kad TXT ieraksti ir pabeigti, Commerce grupa pabeigs Azure Front Door atjauninājumus domēnam, kas iestatīs SSL sertifikātu.

## <a name="apex-domains"></a>Apeksa domēni

Commerce nodrošinātā Azure Front Door instance neatbalsta apeksa domēnus (saknes domēnus, kas nesatur apakšdomēnus). Lai atrisinātu apeksa domēnus, ir nepieciešama IP adrese, un Commerce Azure Front Door instance pastāv tikai ar virtuāliem galapunktiem. Lai izmantotu apeksa domēnu, ir divas opcijas:

- **1. opcija** - Izmantojiet DNS nodrošinātāju, lai novirzītu apeksa domēnu uz "www" domēnu. Piemēram, fabrikam.com pārvirza uz `www.fabrikam.com` , kur `www.fabrikam.com` ir CNAME ieraksts, kas norāda uz Commerce viesotu Azure Front Door instanci.

- **2. opcija** - Iestatiet CDN/front door instanci uz savu instanci, lai viesotu apeksa domēnu.

> [!NOTE]
> Ja izmantojat Azure Front Door, jums ir arī jāiestata Azure DNS tajā pašā abonementā. Apeksa domēns, kas viesots Azure DNS, var norādīt uz jūsu Azure Front Door kā uz aizstājvārda ierakstu. Šis ir vienīgais risinājums, tā kā apeksa domēniem vienmēr ir jānorāda IP adrese.

  ## <a name="additional-resources"></a>Papildu resursi

  [Jauna e-tirdzniecības nomnieka izvietošana](deploy-ecommerce-site.md)

  [Tiešsaistes veikala kanāla iestatīšana](./channel-setup-online.md)

  [E-komercijas vietnes izveide](create-ecommerce-site.md)

  [Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

  [Failu robots.txt pārvaldība](manage-robots-txt-files.md)

  [Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

  [B2C nomnieka iestatīšana programmā Commerce](set-up-B2C-tenant.md)

  [Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

  [Vairāku B2C nomnieku konfigurēšana Commerce vidē](configure-multi-B2C-tenants.md)

  [Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

  [Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]