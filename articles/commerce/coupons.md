---
title: Kuponi
description: Šajā rakstā ir sniegts apskats par iespējām, kas attiecas uz kuponiem Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 2594848948b141015adfaa4ec27e2c2b4cc4dcd2
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410473"
---
# <a name="coupons"></a>Kuponi

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šajā rakstā ir sniegts apskats par iespējām, kas attiecas uz kuponiem Microsoft Dynamics 365 Commerce.

Kuponi ir kodi un svītrkodi, kas tiek izmantoti, lai darījumiem pievienotu atlaides. Mazumtirgotāji izplatīt kuponus potenciālajiem vai esošajiem debitoriem, lai palīdzētu uzlabot viņu zīmola atpazīšanu, vadīt pārvēršanu, saglabāt debitoru bāzi, palielināt pārdošanu un visbeidzot palielināt ieņēmumus. Kuponi ir kļuvis par vienu no vissvarīgākajiem mārketinga rīkiem un ir jauns norma e-komercijas pārdošanā.

Kuponi Dynamics 365 Commerce ir saistīti ar atlaidēm un tiek uzskatīti par papildu apstiprināšanu papildus atlaidēm. Katrs kupons ir saistīts ar vienu atlaidi, un ar saistīto atlaidi tiek definēta preču kopa, kam kupons ir derīgs.

Cenu grupas, kas ir saistītas ar atlaidi, nosaka piemērotos nosacījumus, kuriem var izmantot kuponu. Šie nosacījumi ietver debitoru grupas un pārdošanas kanālus. Kuponi nodrošina arī lietojuma **ierobežojumu un debitora** **nepieciešamos rekvizītus**, ko var izmantot, lai konfigurētu neobligātos lietošanas ierobežojumus.

Katram kuponam var būt vairāki kuponu kodi un kupona svītrkodi, un katram kodam var būt savs derīguma datumu diapazons un statuss. Ja koda statuss ir iestatīts uz **Neaktīvs**, kodu nevar izmantot jebkurā kanālā.

## <a name="set-up-a-coupon"></a>Kupona iestatīšana

Lai iestatītu kuponu, ir jāiestata kupona svītrkods un divas kupona numuru sērijas.

Lai iestatītu kuponu programmā Commerce Headquarters, veiciet šādus soļus.

1. Pārejiet uz **sadaļu Mazumtirdzniecības un Commerce \> Krājumu pārvaldības \> svītrkodi un etiķetes Maskas \> rakstzīmes**.
1. Atlasiet **Pievienot**, lai izveidotu kupona koda veida **maskas** rakstzīmi. Laukā **Rakstzīme** varat atlasīt neizmantotās rakstzīmes.
1. Pārejiet uz **sadaļu Mazumtirdzniecības \> un Commerce Krājumu pārvaldības \> svītrkodi un etiķešu \> svītrkodu maskas iestatījumi**.
1. Atlasiet **Jauns**, lai izveidotu kupona veida svītrkoda **masku**.
1. Pārejiet uz **sadaļu Mazumtirdzniecības \> un Commerce Krājumu \> vadības svītrkodi un etiķešu \> svītrkodu iestatījumi**.
1. Atlasiet **Jauns**, lai izveidotu svītrkodu, kas izmanto izveidoto svītrkoda masku.
1. Dodieties uz **organizācijas administrēšanas \> numuru sēriju**.
1. Izveidojiet divas numuru sērijas:

    1. Viena sērija kupona **numura atsaucei**. Šajā secībā tiek definēts kupona unikālais identifikators.
    1. Viena sērija kupona koda **ID atsaucei**. Šajā secībā tiek definēts katra kupona koda unikālais identifikators.

    Abu numuru sēriju laukam **Sfēra** jāiestata vērtība **Uzņēmums**. Parasti automātiski jāģenerē abi sērijas numuri.

1. Dodieties uz **commerce parametru \> cenām un atlaižu \> kuponiem**.
1. Iestatiet agrāk **izveidoto svītrkoda** svītrkoda lauku Kupona svītrkoda maska.
1. Dodieties uz **Commerce parametru \> numuru sērijas**.
1. Atlasiet numuru sērijas, ko iepriekš izveidojāt kupona numuram **un kupona** koda **ID atsaucēm**.

Lai iestatītu kuponu, vispirms ir jāizveido atlaide un kupons atsevišķi, un pēc tam tie jāsaista, **atlasot atlaidi kupona** konfigurācijas laukā Atlaide. Kad kupons ir saistīts ar atlaidi, **saistītās** atlaides lauki Statuss, **·** **Spēkā** stāšanās datums un Beigu datums kļūst tikai lasāmi, jo vērtības tiek noteiktas pēc kupona statusa un derīguma perioda. Ja kupona statuss ir iestatīts uz **Aktīvs**, saistītās atlaides statuss automātiski tiek atjaunināts uz **Iespējots**. Tāpat, ja kupona statuss ir iestatīts uz **Neaktīvs**, saistītās atlaides statusa statuss tiek automātiski atjaunināts uz **Atspējots**.

## <a name="use-a-coupon"></a>Izmantot kuponu

Lai pārdošanas darījumam pievienotu kuponu commerce point of Sale (POS), varat izmantot kupona kodu vai kupona svītrkodu. Lai izmantotu kupona kodu, atlasiet operāciju **Pievienot kupona kodu** un pēc tam ievadiet kodu. Lai lietotu kupona svītrkodu, varat skenēt svītrkodu, izmantojot skenēšanas ierīci, vai ievadīt to, izmantojot darbības ekrānā redzamo ciparu **tastatūru**.

Dažreiz mazumtirgotāji vēlas, lai kasieri varētu piešķirt fiksētas summas atlaides debitoriem appeasement iemeslu dēļ vai preču defektu dēļ, taču tie nevēlas drukāt kuponu kodus un izplatīt tos kasierim. Šādā gadījumā kuponam opciju Lietot **bez kupona koda** var iestatīt uz **Jā**. Pēc tam POS kasieri var **izmantot** **operācijas Skatīt pieejamās atlaides funkciju, lai pievienotu kupona darbību bez manuālas** koda ievadīšanas. Ja kuponam ir vairāki kuponu kodi, sistēma automātiski atlasa pirmo aktīvo kodu un piemēro to darbībai.

Lai zvanu centra pārdošanas pasūtījumam pievienotu kuponu, **·** **zvanu** centra lietotājam pārdošanas pasūtījuma lapas darbību rūts cilnē Pārvaldīt jāatlasa kuponi.

Lai pievienotu kuponu e-komercijas pasūtījumam, **pircējs var ievadīt kupona kodu iepirkumu** groza laukā Peles kods.

Kad pārdošanas pasūtījumam ir pievienots kupons, cenu noteikšanas programma nekavējoties izraisa visu pasūtījumu pārrēķinu neatkarīgi no tā, vai ir iespējots aizkavētais aprēķins.

> [!NOTE]
> Commerce versijā 10.0.30 un agrāk pēc zvanu centra lietotāju pievienošanas zvanu centra pārdošanas pasūtījumam tiem ir jāatlasa Pārrēķins darbību rūts cilnes Pārdošana cilnē Aprēķināt, **·** **·** **lai** piemērotu ar šo kuponu saistīto atlaidi.

## <a name="coupon-usage-limit"></a>Kupona lietošanas ierobežojums

Kuponus var konfigurēt ierobežotai lietošanai. Lietošanas ierobežojumu var definēt katram debitoram, kanālam vai globāli. Izmantošanas ierobežojums tiek ieviests uz kupona. Piemēram, vienreizējas lietošanas kuponu, kam ir divi kuponu kodi, var izmantot divas reizes, vienu reizi katram kupona kodam.

Kuponus var izmantot pārdošanas kanālos. Tomēr zvanu centram ierobežotu lietošanas kuponus var lietot **tikai tad, ja zvanu centra** kanālam ir iespējots iestatījums Iespējot pasūtījuma pabeigšanu. Ja ir **atspējots iestatījums** Iespējot pasūtījuma pabeigšanu, var lietot tikai ierobežotus lietošanas kuponus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
