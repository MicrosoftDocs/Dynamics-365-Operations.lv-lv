---
title: Zvanu centra kanāla iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot jaunu zvanu centra kanālu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 14cee020cc8aead627180343c82bf23534ae83c4
ms.sourcegitcommit: 0681a00d60c9f8cc8f7b9888b8c5ddf07279fc04
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2020
ms.locfileid: "3131735"
---
# <a name="set-up-a-call-center-channel"></a>Zvanu centra kanāla iestatīšana


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot jaunu zvanu centra kanālu programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats


Programmā Dynamics 365 Commerce zvanu centrs ir mazumtirdzniecības kanāla veids, ko var definēt lietojumprogrammā. Lai noteiktu kanālu jūsu zvanu centra entītijām, sistēma ļauj saistīt specifiskus datus un pasūtījumu apstrādes noklusējumus pārdošanas pasūtījumos. Lai gan uzņēmums var pakalpojumā Commerce noteikt vairākus zvanu centra kanālus, ir svarīgi atzīmēt, ka atsevišķu lietotāju var saistīt tikai ar vienu zvanu centra kanālu. 

Pirms jauna zvanu centra kanāla izveidošanas pārliecinieties, ka esat pabeiguši [Kanāla iestatīšanas priekšnosacījumus](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Jauna zvanu centra kanāla izveide un konfigurācija

Lai izveidotu un konfigurētu jaunu zvanu centra kanālu, veiciet tālāk norādītās darbības.

1. Navigācijas panelī dodieties uz **Retail un Commerce \> Kanāli \> Zvanu centri \> Visi zvanu centri**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.
1. Atlasiet atbilstošo **Juridisko personu** no nolaižamā saraksta.
1. Atlasiet atbilstošo atrašanās vietu **Noliktava** no nolaižamā saraksta. Šī atrašanās vieta tiks izmantota kā noklusējuma vērtība pārdošanas pasūtījumiem, kas izveidoti šim zvanu centra kanālam, ja vien klienta vai krājuma līmenī nav definēti citi noklusējumi.
1. Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru. Šie dati tiek izmantoti, lai palīdzētu automātiskās aizpildīšanas noklusējumos, kad tiek veidoti jauni klientu ieraksti. Veidojot zvanu centra pasūtījumus, nav ieteicams izveidot pasūtījumus noklusējuma klientam.
1. Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu. Kad zvanu centra pasūtījumi ir izveidoti un apstrādāti, tiek izmantots e-pasta paziņojumu profils, lai aktivizētu automatizētos e-pasta brīdinājumus klientiem ar informāciju par viņu pasūtījuma statusu.
1. Nodrošiniet informācijas kodu **Cenas ignorēšana**. Jums, iespējams, vispirms būs jāizveido informācijas kods. Šis informācijas kods sniedz pamatojuma kodu kopu, no kuras lietotājam piedāvās izvēlēties, izmantojot cenu ignorēšanas funkcionalitāti zvanu centra pasūtījumā.
1. Norādiet informācijas kodu **Aizturēšanas kods**. Jums, iespējams, vispirms būs jāizveido informācijas kods. Šis informācijas kods sniedz neobligātu pamatojuma kodu kopu, no kuras lietotājam piedāvās izvēlēties, veicot aizturētu pasūtījumu.
1. Norādiet informācijas kodu **Kredīts**. Jums, iespējams, vispirms būs jāizveido informācijas kods. Šis informācijas kods sniedz pamatojuma kodu kopu, ko lietotājs var izvēlēties, izmantojot pasūtījuma kredīta funkcionalitāti zvanu centrā, lai sniegtu klientam dažās veida atmaksas klientu apkalpošanas nolūkos.
1. Neobligāti: Kopsavilkuma cilnē **Finanšu dimensijas** iestatiet finanšu dimensijas. Šeit ievadītās dimensijas pēc noklusējuma tiek rādītas šajā zvanu centra kanālā izveidotajā pārdošanas pasūtījumā.
1. Noklikšķiniet uz **Saglabāt**.

Tālāk redzamajā attēlā parādīta jauna zvanu centra kanāla izveide.

![Jauns zvanu centra kanāls](media/channel-setup-callcenter-1.png)

Tālāk redzamajā attēlā ir parādīts zvanu centra kanāla piemērs.

![Zvanu centra kanāla piemērs](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Papildu kanāla iestatīšana

Papildu uzdevumi, kas nepieciešami zvanu centra kanāla iestatīšanai, ietver maksājuma metožu un piegādes režīmu iestatīšanu.

Tālāk esošajā attēlā ir parādītas cilnes **Iestatīšana** iestatīšanas opcijas **Piegādes veidi** un **Maksāšanas metodes**.

![Papildu zvanu centra kanāla iestatīšanas darbības](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Iestatīt maksājuma metodes

Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības. Lietotājiem būs jāizvēlas no iepriekš definētajām maksājumu metodēm, lai piesaistītu tās zvanu centra kanālam. Pirms izveidojat zvanu centra maksājuma metodes, vispirms iestatiet savas galvenās maksājuma metodes sadaļā **Retail un Commerce\>Kanāla iestatīšana \>Maksājuma metodes \>Maksājuma metodēs**.

1. Darbības rūtī atlasiet cilni **Iestatīšana** un pēc tam atlasiet **Maksājumu metodes**.
1. Darbību rūtī atlasiet **Jauns**.
1. Navigācijas rūtī atlasiet maksājuma metodi no pieejamajiem iepriekš definētajiem maksājumiem.
1. Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam. Kredītkartēm, dāvanu kartēm vai lojalitātes programmas kartēm ir nepieciešams papildu iestatījums, atlasot funkciju **Kartes iestatīšana**. 
1. Konfigurējiet pareizus maksājuma tipa grāmatošanas kontus sadaļā **Grāmatošana**.
1. Darbību rūtī noklikšķiniet uz **Saglabāt**.

Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.

![Maksājumu metožu piemērs](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Iestatiet piegādes veidus

Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas **Darbību rūtī**.  

Lai mainītu vai pievienotu piegādes veidu, kas ir jāsaista ar zvanu centra kanālu, veiciet tālāk aprakstītās darbības.

1. Veidlapā Zvanu centra piegādes veidi atlasiet **Pārvaldīt piegādes veidus**
1. Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.
1. Sadaļā **Mazumtirdzniecības kanāli** noklikšķiniet uz **Pievienot rindu**, lai pievienotu zvanu centra kanālu. Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.
1. Pārliecinieties, ka piegādes veids ir konfigurēts ar datiem kopsavilkuma cilnē **Preces** un kopsavilkuma cilnē **Adreses**. Ja preces vai piegādes adreses nav derīgas piegādes veidam, izvēloties tās pasūtījuma izveides laikā, radīsies kļūdas.
1. Pēc tam, kad ir veiktas visas izmaiņas zvanu centra piegādes veida konfigurācijās, ir jāpalaiž darbs **Piegādes veidu apstrāde**, lai izvērstu izmaiņu matricu. Šo darbu var atrast, pārvietojoties uz sadaļu **Retail un Commerce \>Retail un Commerce IT \> Apstrādāt piegādes veidus**.

Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.

![Iestatiet piegādes veidus](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Kanāla lietotāju iestatīšana

Lai izveidotu pārdošanas pasūtījumu, kas ir saistīts ar zvanu centra kanālu no Commerce Headquarters, lietotājam, kas veido pārdošanas pasūtījumu, ir jābūt saistītam ar zvanu centra kanālu. Lietotājs nevar manuāli saistīt pārdošanas pasūtījumu, kas izveidots Commerce Headquarters, ar zvanu centra kanālu. Saite ir sistemātiska, un tā ir balstīta uz lietotāju un lietotāja attiecībām ar zvanu centra kanālu. Lietotājs var būt saistīts tikai ar vienu zvanu centra kanālu.

1. Darbības rūtī atlasiet cilni **Kanāls**, pēc tam atlasiet **Kanāla lietotāji**.
1. Darbību rūtī atlasiet **Jauns**.
1. Nolaižamajā atlases sarakstā izvēlieties esošu **Lietotāja ID**, lai saistītu šo lietotāju ar zvanu centra kanālu

Pēc kanāla lietotāja iestatīšanas un jauna pārdošanas pasūtījuma izveides programmā Commerce Headquarters, pārdošanas pasūtījumu saistīs ar saistīto zvanu centra kanālu. Visas konfigurācijas šim kanālam tiks sistemātiski piemērotas pārdošanas pasūtījumam. Lietotājs var apstiprināt, kurš zvanu centra kanāls ir saistīts ar pārdošanas pasūtījumu, skatot kanāla nosaukuma atsauci pārdošanas pasūtījuma galvenē.


### <a name="set-up-price-groups"></a>Cenu grupu iestatīšana

Cenu grupas ir obligātas, bet, ja tās tiek izmantotas, tās var kontrolēt, kuras pārdošanas cenas tiks piedāvātas klientiem, kuri veic pasūtījumus zvanu centra kanālā. Ja klientam nav konfigurēta cenu grupa vai ja kataloga cenu grupas netiek piemērotas pārdošanas pasūtījumam (izmantojot lauku **Avota koda ID** zvanu centra pasūtījuma galvenē), tad krājuma cenu atrašanai tiek izmantot kanāla cenu grupa. Ja zvanu centra kanālā nav atrasta cenu grupa, tiek izmantotas noklusētās krājuma pamata cenas. 

Lai iestatītu cenu grupu, rīkojieties šādi:

1. Darbības rūtī noklikšķiniet uz cilnes **Kanāls**, pēc tam atlasiet **Cenu grupas**.
1. Darbību rūtī noklikšķiniet uz **Jauns**.
1. Nolaižamajā atlases sarakstā atlasiet **Mazumtirdzniecības cenu grupa**.

## <a name="additional-resources"></a>Papildu resursi

[Kanāla iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Zvanu centra pārdošanas funkcionalitāte](call-center-functionality.md)

[Iestatīt zvanu centra pasūtījumu apstrādes opcijas](set-up-order-processing-options.md)

[Zvanu centra katalogi](call-center-catalogs.md)

[Pārkāpumu brīdinājumu iestatīšana un darbs ar tiem](set-up-fraud-alerts.md)

[Nepārtrauktības programmu iestatīšana zvanu centriem](set-up-continuity-program.md)
