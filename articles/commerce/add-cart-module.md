---
title: Groza modulis
description: Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696765"
---
# <a name="cart-module"></a>Groza modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šī tēma ietver groza moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Groza modulis ir konteiners, kas tiek izmantots visu moduļu viesošanai, kuri ir nepieciešami, lai parādītu grozā esošus elementus. Piemēram, tas ietver visus elementus, kas tika pievienoti grozam, pasūtījuma kopsavilkumam un reklāmas kodiem.

Groza modulis atveido datus, pamatojoties uz groza ID. Groza ID ir pārlūkprogrammas sīkfails, kas ir pieejams visā vietnē.

## <a name="cart-module-properties-and-slots"></a>Groza moduļa rekvizīti un sloti

Kā konteiners groza modulis kontrolē dažus pamata rekvizītus, piemēram, virsrakstu un platumu. Virsrakstā parasti ir šāds teksts, piemēram, **Iepirkumu soma**, **Jūsu grozs** vai **Preces jūsu grozā**. Platuma iestatījums nosaka, vai konteinerā esošajiem moduļiem ir jāietilpst konteinerā, vai arī tie var piepildīt ekrānu.

Groza lapa ir sadalīta vairākos reģionos: groza rindas elementi, pasūtījumu kopsavilkums un norēķini, un funkcionalitāte “Meklēt veikalā”. Katrs reģions tiek kartēts uz slotu groza modulī, un katrs slots pieņem iepriekš definētu moduļu kopu.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduļi, ko var izmantot groza modulī

- **Groza rindas elementi** — šis modulis parāda visu to elementu kopsavilkumu, kas tika pievienoti grozam. Informācija ietver preces nosaukumu, atlasītās dimensijas, cenu, daudzumu un atlaides. Šis modulis atbalsta arī tādas darbības kā “noņemt no groza” un “pievienot vēlmju sarakstam”. Attiecībā uz katru rindas elementu ir iespēja nosūtīt preci vai to saņemt veikalā. Šī opcija ir jākonfigurē atsevišķi modulī Saņemt veikalā.
- **Pasūtījuma kopsavilkums** — šis modulis parāda pasūtījuma kopsavilkumu. Informācija ietver apakšsummu, nosūtīšanu, nodokļus un ietaupījumus. Šim modulim var konfigurēt virsrakstu.
- **Promo kods** — šis modulis ļauj klientam izpirkt akcijas kodus. Akcijas kodu var lietot vai noņemt.
- **Norēķināšanās** — šis modulis uzsāk norēķināšanās darbību un novirza lietotāju uz norēķināšanās lapu. Šim modulim ir jākonfigurē trīs saites.

    - **Norēķināšanās** – šī saite liek klientiem pierakstīties, ja viņi vēl to nav izdarījuši.
    - **Viesu norēķināšanās** — šī saite ļauj anonīmiem klientiem veikt pasūtījumus. Tā tiek rādīta tikai tad, kad klienti nav pierakstījušies.
    - **Atgriezties pie iepirkšanās** — šī saite ļauj klientiem doties uz sākumlapu vai jebkuru citu lapu, lai varētu turpināt iepirkties.

- **Bagātinātā satura bloks** — šis modulis atbalsta pielāgotu ziņojumapmaiņu iepirkumu groza modulī. Ziņojumi tiek vadīti, izmantojot satura pārvaldības sistēmu (CMS). Var pievienot jebkuru ziņojumu, piemēram, “Ja rodas problēmas ar pasūtījumu, sazinieties ar 1-800-Fabrikam”.
- **Saņemt veikalā** — šis modulis rāda tuvumā esošo veikalu sarakstu, kur var saņemt preci. Pēc noklusējuma šis modulis rāda veikalus, kas atrodas 50 jūdžu rādiusā no klienta atrašanās vietas. Tomēr meklēšanas rādiusu var pielāgot modulī. Katram veikalam tiek veikta krājumu pārbaude, ja ir ieslēgta krājumu pārbaudes funkcionalitāte, un tiek parādīts atbilstošs ziņojums “ir pieejams noliktavā” vai “beidzies”.
- **Veikala meklēšana, izmantojot Bing kartes** – šo moduli var izmantot modulī Saņemt veikalā. Tas ļauj klientiem meklēt veikalus, ievadot atrašanās vietu. Bing karšu ģeokodēšanas lietojumprogrammas interfeiss (API) tiek lietots, lai konvertētu klienta norādīto atrašanās vietu uz ģeogrāfisko platumu un garumu. Neizmantojot šo moduli, tiek rādīti tikai tie veikali, kas ir klienta pašreizējās atrašanās vietas tuvumā, un klients nevar meklēt citu atrašanās vietu.

## <a name="cart-module-settings"></a>Groza moduļa iestatījumi

Groza moduļiem ir trīs iestatījumi, kurus var konfigurēt.

- **Maksimālais daudzums** — katras preces maksimālais skaits, ko var pievienot grozam. Piemēram, mazumtirgotājs var nolemt, ka vienā transakcijā var pārdot tikai 10 katras preces vienumus.
- **Krājumu pārbaude** — ja vērtība ir iestatīta uz **Patiess**, prece tiek pievienota grozam tikai pēc tam, kad iegādes lodziņa modulis apstiprina, ka šī prece ir krājumos. Šī krājuma pārbaude tiek veikta gan gadījumam, kad prece tiks nosūtīta, gan gadījumam, kur prece tiks saņemta veikalā. Ja vērtība ir iestatīta uz **Nepatiess**, krājumu pārbaude netiek veikta pirms preces pievienošanas grozam un pasūtījuma veikšanas.
- **Krājumu buferis** — krājumi tiek uzturēti reālajā laikā, un situācijā, kad daudzi klienti veic pasūtījumus, var būt sarežģīti uzturēt precīzu krājumu uzskaiti. Tāpēc krājumam var definēt buferi. Kad ir veikta krājuma pārbaude, ja krājumi ir mazāki par buferā esošo daudzumu, tiek uzskatīts, ka prece vairs nav pieejama. Tāpēc, kad pārdošana notiek ātri, izmantojot vairākus kanālus, un krājumu uzskaite nav pilnībā sinhronizēta, pastāv mazāks risks, ka tiks pārdota prece, kas vairs nav pieejama.

## <a name="retail-server-interaction"></a>Mijiedarbība ar mazumtirdzniecības serveri

Groza modulis izgūst preču informāciju, izmantojot Mazumtirdzniecības servera API. Groza ID no pārlūka sīkfaila tiek izmantots, lai izgūtu visu informāciju par preci no Mazumtirdzniecības servera.

## <a name="add-a-cart-module-to-a-page"></a>Groza moduļa pievienošana lapā

Lai pievienotu groza moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet fragmentu ar nosaukumu **groza fragments** un pievienojiet tam groza moduli.
1. Groza moduļa slotā **Groza rindas krājumi** pievienojiet groza rindas krājumu moduli.
1. Slotā **Pasūtījuma kopsavilkums** pievienojiet pasūtījuma kopsavilkuma moduli.
1. Slotā **Akcijas kods** pievienojiet akcijas koda moduli.
1. Slotā **Norēķināšanās** pievienojiet norēķināšanās moduli.
1. Slotā **Atrast veikalā** pievienojiet moduli Saņemt veikalā.
1. Modulī Saņemt veikalā, atlasiet **Veikala meklēšana** un pievienojiet veikala meklēšanu, izmantojot moduli Bing kartes.
1. Pārbaudiet fragmentu un publicējiet to.
1. Izveidojiet veidni ar nosaukumu **groza veidne** un pievienojiet groza fragmentu, ko tikko izveidojāt.
1. Saglabājiet veidni, pārbaudiet un publicējiet to.
1. Izveidojiet lapu, kas izmanto jauno veidni.
1. Saglabājiet un priekšskatiet lapu.
1. Pārbaudiet lapu un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Container modulis](add-container-module.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
