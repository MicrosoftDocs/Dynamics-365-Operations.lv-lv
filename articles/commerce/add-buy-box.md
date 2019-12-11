---
title: Iegādes lodziņa modulis
description: Šajā tēmā tiek stāstīts par iegādes lodziņa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811145"
---
# <a name="buy-box-module"></a>Iegādes lodziņa modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par iegādes lodziņa moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Termins *iegādes lodziņš* tipiski tiek attiecināts uz preces informācijas lapas apgabalu, kas ir “virs ieloces” un kurā ir ietverta visa svarīgākā informācija, kas nepieciešama preces pirkuma veikšanai. (Apgabals, kas ir “virs ieloces”, ir redzams, kad lapa tiek ielādēta pirmo reizi, lai lietotājiem skatīšanai nebūtu jāritina uz leju.)

Iegādes lodziņa modulis ir īpašs konteiners, kas tiek izmantots, lai viesotu visus moduļus, kas parādīti preces informācijas lapas iegādes lodziņā.

Preces informācijas lapas vietrādī URL ir ietverta preces ID. Visa informācija, kas nepieciešama iegādes lodziņa moduļa atveidošanai, tiek atvasināta no šīs preces ID. Ja preces ID nav norādīts, iegādes lodziņa modulis netiks pareizi atveidots lapā. Tāpēc iegādes lodziņa moduli nevar izmantot jebkurā lapā, kurā nav preces konteksta (piemēram, sākumlapā vai mārketinga lapā).

## <a name="buy-box-module-properties-and-slots"></a>Iegādes lodziņa moduļa rekvizīti un sloti 

Kā konteiners, iegādes lodziņa modulis kontrolē dažus pamata rekvizītus, piemēram, platumu. Platuma iestatījums nosaka, vai konteinerā esošajiem moduļiem ir jāietilpst konteinerā, vai arī tie var piepildīt ekrānu.

Preces informācijas lapā iegādes lodziņš ir sadalīts divos reģionos: multivides reģions kreisajā pusē un satura reģions labajā pusē. Iegādes lodziņā šos divus reģionus attēlo sloti. Katrs slots ir iepriekš konfigurēts, lai pieņemtu tikai noteiktus slota atbalstītus moduļus. Piemēram, **Multivides** slots atbalsta tikai multivides galerijas moduli.

Pēc noklusējuma kolonnu platuma proporcija multivides reģionam un satura apgabalam ir 2:1. Tomēr dizains var pārrakstīt kolonnu platumu. Turklāt mobilajās ierīcēs abi reģioni ir grupēti. Tādējādi viens reģions tiek parādīts zem cita reģiona.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduļi, ko var izmantot iegādes lodziņa modulī

- **Multivides galerija** — šis modulis tiek izmantots, lai parādītu preču attēlus preču informācijas lapā. Tas var atbalstīt no viena līdz vairākiem attēliem. Tā atbalsta arī sīktēlu attēlus. Sīktēlu attēlus var sakārtot vai nu horizontāli (kā rindu zem attēla), vai vertikāli (kā kolonnu blakus attēlam). Multivides galerijas modulis var tikt pievienots **Multivides** slotam iegādes lodziņa modulī. Tas pašlaik atbalsta tikai attēlus un videoklipus.
- **Preces nosaukums** — šis modulis parāda preces nosaukumu preces informācijas lapā. Pēc noklusējuma tiek izmantots virsraksta tags **H1**, bet šo virsraksta tagu var mainīt pēc nepieciešamības.
- **Preces novērtējums** — šis modulis parāda zvaigžņu vērtējumus, pamatojoties uz preces klientu vērtējumiem. Iegādes lodziņa modulis no reitingu pakalpojuma izgūst preču novērtējumu katrai precei.
- **Preces cena** — šis modulis parāda preces cenu. Cenā ir iekļautas pārsvītrojuma cenas un atlaides.
- **Preces apraksts** — šis modulis parāda preces cenu.
- **Preces konfigurēšana** — šis modulis rāda preces izmēru, stilu un dimensijas. Dimensiju atlasītāji var tikt sagrupēti vertikāli vai arī tie var parādīties blakus. Ja ir atlasīts preces variants, tad tiek atjaunināti citi rekvizīti iegādes lodziņā (piemēram, produkta apraksts un attēli), lai atspoguļotu informāciju par variantu.
- **Preces daudzums** — šis modulis tiek izmantots preces daudzuma konfigurēšanai. Iestatījums ierobežo preces vai varianta daudzumu, ko var pievienot grozam.
- **Pievienošana grozam** — šis modulis tiek izmantots, lai veiktu darbību “Pievienot grozam”. Grozam var pievienot tikai preci vai variantu. Citiem vārdiem, šablona preci nevar pievienot grozam. Modulī ir rekvizīts **Pāriet uz grozu**, ko var iestatīt vietnes autors. Kad šis rekvizīts ir iestatīts kā **Patiess**, lietotājs tiek novirzīts uz groza lapu ik reizi, kad tiek aktivizēta darbība “pievienot grozam”. Kad tas ir iestatīts kā **Nepatiess**, klients var turpināt pārlūkot preces informācijas lapu pēc preču pievienošanas grozam.
- **Pievienošana vēlmju sarakstam** – šis modulis tiek lietots, lai pievienotu elementu klienta vēlmju sarakstam. Vēlmju sarakstam var pievienot tikai preci vai variantu. Turklāt klientam ir jābūt pierakstītam vietnē. Modulis ietver kļūdu apstrādes loģiku, lai pārliecinātos, ka abi šie nosacījumi ir izpildīti.
- **Atrast veikalā** — šis modulis aktivizē plūsmu “pirkt tiešsaistē, saņemt veikalā”.
- **Saņemt veikalā** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci. Pēc noklusējuma šis modulis rāda veikalus, kas atrodas 50 jūdžu rādiusā no klienta atrašanās vietas. Tomēr meklēšanas rādiusu var pielāgot modulī. Katram veikalam tiek veikta krājumu pārbaude, ja ir ieslēgta krājumu pārbaudes funkcionalitāte, un tiek parādīts atbilstošs ziņojums “ir pieejams noliktavā” vai “beidzies”.
- **Veikala meklēšana, izmantojot Bing kartes** – šo moduli var izmantot modulī Saņemt veikalā. Tas ļauj klientiem meklēt veikalus, ievadot atrašanās vietu. Bing karšu ģeokodēšanas lietojumprogrammas interfeiss (API) tiek lietots, lai konvertētu norādīto atrašanās vietu uz ģeogrāfisko platumu un garumu. Ja tiek izmantots šis modulis, tiek rādīti tikai tie veikali, kas ir klienta pašreizējās atrašanās vietas tuvumā, un klients nevar meklēt citu atrašanās vietu.
- **Bagātināta satura bloks** — šajā modulī var tikt parādīts ziņojums, ka vietnes autors vai mazumtirgotājs vēlas ievietot reklāmu iegādes lodziņā, piemēram, “Ja rodas problēmas ar pasūtījumu, sazinieties ar 1-800-FABRIKAM” vai “Brīva piegāde pasūtījumiem virs 100 $”. Ziņojumi tiek vadīti, izmantojot satura pārvaldības sistēmu (CMS).

## <a name="buy-box-module-settings"></a>Iegādes lodziņa moduļa iestatījumi

Iegādes lodziņa moduļiem ir trīs iestatījumi, kurus var konfigurēt.

- **Maksimālais daudzums** — katras preces maksimālais skaits, ko var pievienot grozam. Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.
- **Krājumu pārbaude** — ja vērtība ir iestatīta uz **Patiess**, prece tiek pievienota grozam tikai pēc tam, kad iegādes lodziņa modulis apstiprina, ka šī prece ir krājumos. Šī krājuma pārbaude tiek veikta gan gadījumam, kad prece tiks nosūtīta, gan gadījumam, kur prece tiks saņemta veikalā. Ja vērtība ir iestatīta uz **Nepatiess**, krājumu pārbaude netiek veikta pirms preces pievienošanas grozam un pasūtījuma veikšanas.
- **Krājumu buferis** — krājumi tiek uzturēti reālajā laikā, un situācijā, kad daudzi klienti veic pasūtījumus, var būt sarežģīti uzturēt precīzu krājumu uzskaiti. Tāpēc krājumam var definēt buferi. Kad ir veikta krājuma pārbaude, ja krājumi ir mazāki par buferā esošo daudzumu, tiek uzskatīts, ka prece vairs nav pieejama. Tāpēc, kad pārdošana notiek ātri, izmantojot vairākus kanālus, un krājumu uzskaite nav pilnībā sinhronizēta, pastāv mazāks risks, ka tiks pārdota prece, kas vairs nav pieejama.

## <a name="retail-server-interaction"></a>Mijiedarbība ar mazumtirdzniecības serveri

Iegādes lodziņa modulis izgūst preču informāciju, izmantojot Mazumtirdzniecības servera API. Preces ID no preces informācijas lapas tiek izmantots visas informācijas izgūšanai.

## <a name="add-a-buy-box-module-to-a-page"></a>Iegādes lodziņa moduļa pievienošana lapā

Lai pievienotu iegādes lodziņa moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet fragmentu ar nosaukumu **iegādes lodziņa fragments** un pievienojiet tam iegādes lodziņa moduli.
1. Iegādes lodziņā moduļa **Multivides** slotā pievienojiet multivides galerijas moduli.
1. Iegādes lodziņa moduļa **Satura** slotā pievienojiet šādus moduļus: preces nosaukums, preces vērtējums, preces cena, preces apraksts, preces konfigurācija, pievienot grozam, pievienot vēlmju sarakstam un atrast veikalā. Varat pārkārtot moduļus **Satura** slotā, lai sasniegtu vēlamo izkārtojumu.
1. Atlasiet moduli Atrast veikalā. Slotā, kas atrodas šī moduļa iekšpusē, pievienojiet moduli Saņemt veikalā.
1. Slotā, kas atrodas šajā modulī saņemt veikalā, pievienojiet veikala meklētāju, izmantojot Bing kartes moduli.
1. Pārbaudiet lapu un publicējiet to.
1. Izveidojiet veidni preces informācijas lapai un nosauciet to par **PDP veidni**.
1. Noklusējuma lapas pievienošana
1. Noklusējuma lapas **Galvenajā** slotā pievienojiet iegādes lodziņa fragmentu.
1. Saglabājiet veidni, pārbaudiet un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto veidni lapas ar nosaukumu **PDP lapa** izveidei.
1. Jaunās lapas **Galvenajā** slotā pievienojiet iegādes lodziņa fragmentu.
1. Saglabājiet un priekšskatiet lapu. Pievienojiet **?productid=&lt;product id&gt;** vaicājuma virknes parametru priekšskatījuma lapas vietrādim URL. Šādā veidā preces konteksts tiek izmantots priekšskatījuma lapas ielādei un rādīšanai.
1. Pārbaudiet lapu un publicējiet to. Preču informācijas lapā ir jābūt redzamam iegādes lodziņam.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Container modulis](add-container-module.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
