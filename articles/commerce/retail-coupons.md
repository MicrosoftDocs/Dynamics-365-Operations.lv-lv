---
title: Mazumtirdzniecības pārdošanas kuponu iestatīšana
description: Šajā tēmā sniegts pārskats par kuponiem un izskaidrots, kā tos iestatīt.
author: scott-tucker
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9d8b9977d733c87566249bcb9658b80c4350c17d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792029"
---
# <a name="set-up-coupons-for-retail-sales"></a>Mazumtirdzniecības pārdošanas kuponu iestatīšana

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Pārskats par kuponiem

Kuponi ir kodi un svītrkodi, kas tiek izmantoti, lai darījumiem pievienotu atlaides. Katram kuponam var būt vairāki kodi, un katram kodam var būt savs derīguma datumus.

Katrs kupons ir saistīts ar vienu atlaidi. Cenu grupas, kas ir saistītas ar atlaidi, definē klientus, kas var izmantot kuponu vai kanālus, kur kupons ir derīgs.

Pamatā kuponi ir papildu apstiprināšana papildus atlaidēm. Kupons sniedz kupona kodus un svītrkodus, kas nepieciešami kopā ar šo kodu datumu diapazoniem. Kupons nodrošina arī papildu lietošanas ierobežojumus un klientiem nepieciešamos rekvizītus. Atlaide nodrošina preču kopu, kam kupons ir derīgs. Atlaides cenu grupas sniedz klientu, kanālu vai katalogu kopu, kam kupons ir derīgs.

Lai izveidotu kuponu, atlaide un kupons ir jāizveido atsevišķi. Pēc tam tie ir jāsaista, atlasot atlaidi programmas Commerce kuponu lapā.

> [!NOTE]
> Pēc tam, kad kupons ir saistīts ar atlaidi, vairāki lauki programmas Commerce atlaižu lapā kļūst tikai lasāmi, jo to pārvaldībai tiek izmantoti kupona iestatījumi. Šie lauki ietver statusa un standarta datumu diapazona laukus.

### <a name="limited-use-coupons"></a>Kuponi ar izmantošanas ierobežojumiem

Kuponiem var konfigurēt izmantošanas ierobežojumus. Lietojuma ierobežojumu var noteikt katram debitoram vai kanālam, vai arī kā globālu ierobežojumu. Šis ierobežojums tiek izmantots, kad kods vai svītrkods tiek ievadīts vai skenēts POS sistēmā vai kad tiek izveidots pārdošanas pasūtījums.

Kupona ierobežojums tiek īstenots pēc kupona koda. Piemēram, vienreizēju kuponu, kam ir divi kupona kodi, var izmantot divas reizes: vienu reiz katram kupona kodam. Katru kupona kodu var neatkarīgi iestatīt kā aktīvu.

Kuponus var izmantot visos pārdošanas kanālos, tomēr zvanu centra pasūtījumiem ierobežotās lietošanas kuponus var izmantot tikai tiem zvanu centru pasūtījumiem, kam zvanu centrā ir aktivizēts iestatījums **Pasūtījuma pabeigšana**. Ja tas nav iespējots, zvanu centra pasūtījumos var izmantot tikai neierobežota lietošanas veida kuponus.

> [!NOTE]
> Kad kupona kods ir sasniedzis lietojuma ierobežojumu, sistēma šī kupona koda statusu automātiski *nemaina* uz “Izlietots”. Tomēr šis kupona kods ir sasniedzis savu lietojuma ierobežojumu un to nevar izmantot. Ja kupona koda statuss ir manuāli iestatīts uz kaut citu, kas nav **Aktīvs**, šo kupona kodu nevar izmantot nevienā kanālā.  

## <a name="managing-coupons"></a>Kuponu pārvaldība

Atlaide un kupons ir jāizveido atsevišķi. Pēc tam tie jāsaista, atlasot atlaidi kupona lapā. Pēc tam, kad kupons ir saistīts ar atlaidi, vairāki atlaides lapas lauki kļūst tikai lasāmi, jo tos pārvalda kupona iestatījumi. Šie lauki ietver statusa un standarta datumu diapazona laukus.

Pamatā kuponi ir papildu apstiprināšana papildus atlaidēm. Kupons sniedz kupona kodus un svītrkodus, kas nepieciešami kopā ar šo kodu datumu diapazoniem, lietošanas ierobežojumiem un debitoram nepieciešamo rekvizītu. Atlaide nodrošina preču kopu, kam kupons ir derīgs. Atlaides cenu grupas sniedz klientu, kanālu vai katalogu kopu, kam kupons ir derīgs.

## <a name="system-setup-for-coupons"></a>Kuponu sistēmas iestatīšana

Lai iestatītu kuponu, ir jāiestata kupona svītrkods un divas kupona numuru sērijas.

1. Lapā **Maskas rakstzīmes** izveidojiet jaunu maskas rakstzīmi kupona kodam. Iespējams atlasīt jebkuru neizmantotu rakstzīmi.
2. Lapā **Svītrkodu masku iestatīšana** izveidojiet jaunu svītrkoda masku. Laukam **Veids** iestatiet vērtību **Kupons**.
3. Lapā **Svītrkodu iestatīšana** izveidojiet jaunu svītrkodu, kas izmanto svītrkoda masku, ko tikko izveidojāt.
4. Lapā **Numuru sērijas** izveidojiet divas jaunas numuru sērijas. Viena sērija ir paredzēta kupona koda identifikatoram un otra — kupona numuram. Kupona koda ID ir unikāls katra kupona koda identifikators. Kupona numurs ir unikālais kupona identifikators. Katram kuponam var būt vairāki kodi un svītrkodi, kas aktivizē kuponu.

    > [!NOTE]
    > Abu numuru sēriju laukam **Sfēra** jāiestata vērtība **Uzņēmums**. Vairumā gadījumu jums automātiski jāģenerē abi sērijas numuri.

5. Lapas **Commerce parametri** cilnē **Svītrkodi** atlasiet iepriekš izveidoto svītrkodu.
6. Lapas **Commerce koplietojamie parametri** cilnē **Numuru sērijas** atlasiet numuru sērijas, ko izveidojāt kupona numuram un kupona koda identifikatoram.
7. Tagad varat atvērt lapu **Kuponi** un izveidot jaunus kuponus.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Daļēju atjauninājumu ietekme uz kuponiem

Kupona funkcionalitātē ir ietverti daudzi atšķirīgi līdzekļi. Commerce Headquarters (HQ) un kanāls var tikt daļēji atjaunināti vairākos komponentos. Tāpēc ir svarīgi saprast, kā daļēji atjauninājumi ietekmēt kupona funkcionalitāti kopumā.

- **HQ tiek daļēji atjaunināts, bet Commerce Scale Unit un POS — netiek atjaunināti.** HQ atjauninājumā tiek atjaunināts kupons un atlaižu lapas, un komercijas cenu noteikšanas programma arī tiek atjaunināta. Ja tiek atjaunināts tikai viens no šiem diviem komponentiem, dažas Commerce lapas neatbildīs cenu aprēķina datiem. Tāpēc atlaižu aprēķinu laikā var rasties neparedzēti atlaižu aprēķini var kļūdas.
- **HQ tiek atjaunināts, bet Commerce Scale Unit un POS — netiek atjaunināti (N-1).** Ne visus veikalus var atjaunināt vienlaicīgi, tādēļ HQ ieteicams atjaunināt pirms veikalu atjaunināšanas. N-1 scenārijā jaunā funkcionalitāte, kas ir saistīta ar kuponiem, nebūs pieejama veikalos, kas vēl nav atjaunināti. Piemēram, kupona funkcionalitāte ievieš rindas “Izslēgt”. Ja atlaidei izmantojat rindu izslēgšanu, tās netiks piemērotas veikalā, kurā darbojas vecāka versija.
- **HQ netiek atjaunināts, bet Commerce Scale Unit un POS — tiek atjaunināti (N+1).** Atjauninātā Commerce Scale Unit cenu noteikšanas programma var apstrādāt mantojuma atlaižu kodus cenu aprēķinu laikā, tādēļ šajā scenārijā atjauninājumam nevajadzētu ietekmēt darbību.


[!INCLUDE[footer-include](../includes/footer-banner.md)]