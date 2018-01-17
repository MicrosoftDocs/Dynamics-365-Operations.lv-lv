---
title: "Izveidot mazumtirdzniecības pārdošanas kuponus"
description: "Šajā tēmā sniegts pārskats par mazumtirdzniecības kuponiem un izskaidrots, kā tos iestatīt."
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCoupon
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e05361bf865e44ba6073198fba94d7102b1ed19
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="create-coupons-for-retail-sales"></a>Izveidot mazumtirdzniecības pārdošanas kuponus

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a>Pārskats par kuponiem

Kuponi ir kodi un svītrkodi, kas tiek izmantoti, lai darījumiem pievienotu mazumtirdzniecības atlaides. Katram kuponam var būt vairāki kodi, un katram kodam var būt savs derīguma datumus. 

Katrs kupons ir saistīts ar vienu mazumtirdzniecības atlaidi. Cenu grupas, kas ir saistītas ar atlaidi, definē klientus, kas var izmantot kuponu vai kanālus, kur kupons ir derīgs. 

Pamatā kuponi ir papildu apstiprināšana papildus mazumtirdzniecības atlaidēm. Kupons sniedz kupona kodus un svītrkodus, kas nepieciešami kopā ar šo kodu datumu diapazoniem. Kupons nodrošina arī papildu lietošanas ierobežojumus un klientiem nepieciešamos rekvizītus. Atlaide nodrošina preču kopu, kam kupons ir derīgs. Atlaides cenu grupas sniedz klientu, kanālu vai katalogu kopu, kam kupons ir derīgs.

Lai izveidotu kuponu, atlaide un kupons ir jāizveido atsevišķi. Pēc tam tie jāsaista, atlasot atlaidi programmatūras Microsoft Dynamics 365 for Retail kupona lapā. 

> [!NOTE]
> Pēc tam, kad kupons ir saistīts ar atlaidi, vairāki Microsoft Dynamics 365 for Retail atlaides lapas lauki kļūst tikai lasāmi, jo tos pārvalda kupona iestatījumi. Šie lauki ietver statusa un standarta datumu diapazona laukus.

### <a name="limited-use-coupons"></a>Kuponi ar izmantošanas ierobežojumiem

Kuponiem var konfigurēt izmantošanas ierobežojumus. Lietojuma ierobežojumu var noteikt katram debitoram vai kanālam, vai arī kā globālu ierobežojumu. Šis ierobežojums tiek izmantots, kad kods vai svītrkods tiek ievadīts vai skenēts POS sistēmā vai kad tiek izveidots pārdošanas pasūtījums. Kupons tiek reģistrēts kā izmantots, kad tiek pabeigts pasūtījums, ar kuru kupons ir saistīts.

Kupona ierobežojums tiek īstenots pēc kupona koda. Piemēram, vienreizēju kuponu, kam ir divi kupona kodi, var izmantot divas reizes: vienu reiz katram kupona kodam. Katru kupona kodu var neatkarīgi iestatīt kā aktīvu.

## <a name="managing-coupons"></a>Kuponu pārvaldība

Atlaide un kupons ir jāizveido atsevišķi. Pēc tam tie jāsaista, atlasot atlaidi kupona lapā. Pēc tam, kad kupons ir saistīts ar atlaidi, vairāki atlaides lapas lauki kļūst tikai lasāmi, jo tos pārvalda kupona iestatījumi. Šie lauki ietver statusa un standarta datumu diapazona laukus.  

Pamatā kuponi ir papildu apstiprināšana papildus mazumtirdzniecības atlaidēm. Kupons sniedz kupona kodus un svītrkodus, kas nepieciešami kopā ar šo kodu datumu diapazoniem, lietošanas ierobežojumiem un debitoram nepieciešamo rekvizītu. Atlaide nodrošina preču kopu, kam kupons ir derīgs. Atlaides cenu grupas sniedz klientu, kanālu vai katalogu kopu, kam kupons ir derīgs.

## <a name="system-setup-for-coupons"></a>Kuponu sistēmas iestatīšana 

Lai iestatītu kuponu, ir jāiestata kupona svītrkods un divas kupona numuru sērijas. 

1.  Lapā **Maskas rakstzīmes** izveidojiet jaunu maskas rakstzīmi kupona kodam. Iespējams atlasīt jebkuru neizmantotu rakstzīmi.
2.  Lapā **Svītrkodu masku iestatīšana** izveidojiet jaunu svītrkoda masku. Laukam **Veids** iestatiet vērtību **Kupons**.
3.  Lapā **Svītrkodu iestatīšana** izveidojiet jaunu svītrkodu, kas izmanto svītrkoda masku, ko tikko izveidojāt.
4.  Lapā **Numuru sērijas** izveidojiet divas jaunas numuru sērijas. Viena sērija ir paredzēta kupona koda identifikatoram un otra — kupona numuram. Kupona koda ID ir unikāls katra kupona koda identifikators. Kupona numurs ir unikālais kupona identifikators. Katram kuponam var būt vairāki kodi un svītrkodi, kas aktivizē kuponu.

    > [!NOTE]
    > Abu numuru sēriju laukam **Sfēra** jāiestata vērtība **Uzņēmums**. Vairumā gadījumu jums automātiski jāģenerē abi sērijas numuri.

5.  Lapas **Mazumtirdzniecības koplietojamie parametri** cilnē **Svītrkodi** izvēlieties iepriekš izveidoto svītrkodu.
6.  Lapas **Mazumtirdzniecības parametri** cilnē **Numuru sērijas** atlasiet numuru sērijas, ko izveidojāt kupona numuram un kupona koda identifikatoram.
7.  Tagad varat atvērt lapu **Kuponi** un izveidot jaunus kuponus.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Daļēju atjauninājumu ietekme uz kuponiem

Programmatūrā Dynamics 365 for Retail kupona funkcionalitāte ietver vairākus atšķirīgus līdzekļus. Microsoft Dynamics 365 for Retail headquarters (HQ) un kanālu var daļēji atjaunināt starp komponentiem. Tāpēc ir svarīgi saprast, kā daļēji atjauninājumi ietekmēt kupona funkcionalitāti kopumā.

- **HQ tiek daļēji atjaunināts, bet Retail serveris un POS — netiek atjaunināti.** HQ atjauninājumā tiek atjaunināts kupons un atlaižu lapas, un mazumtirdzniecības cenu noteikšanas programma arī tiek atjaunināta. Ja tiek atjaunināts tikai viens no šiem diviem komponentiem, dažas Retail lapas neatbildīs cenu aprēķina datiem. Tāpēc atlaižu aprēķinu laikā var rasties neparedzēti atlaižu aprēķini var kļūdas.
- **HQ tiek atjaunināts, bet Retail serveris un POS — netiek atjaunināti (N-1).** Ne visus mazumtirdzniecības veikalus var atjaunināt vienlaicīgi, tādēļ HQ ieteicams atjaunināt pirms mazumtirdzniecības veikalu atjaunināšanas. N-1 scenārijā jaunā funkcionalitāte, kas ir saistīts ar kuponiem, nebūs pieejama veikalos, kas vēl nav atjaunināti. Piemēram, kupona funkcionalitāte ievieš rindas “Izslēgt”. Ja atlaidei izmantojat rindu izslēgšanu, tās netiks piemērotas mazumtirdzniecības veikalā, kurā darbojas vecāka versija.
- **HQ netiek atjaunināts, bet Retail serveris un POS — tiek atjaunināti (N+1).** Atjauninātā Retail servera cenu noteikšanas programma var apstrādāt mantojuma atlaižu kodus cenu aprēķinu laikā, tādēļ šajā scenārijā atjauninājumam nevajadzētu ietekmēt darbību.

