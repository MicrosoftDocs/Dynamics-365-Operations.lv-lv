---
title: Debitora vecumstruktūru momentuzņēmumi
description: Šajā rakstā ir sniegta informācija par debitora vecumstruktūras momentuzņēmumiem. Vecumstruktūras momentuzņēmums aprēķina vecas klientu grupas bilances par noteiktu laika periodu.
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c1a83f2648b52e436d19a11862e58dc33313f341
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902578"
---
# <a name="customer-aging-snapshots"></a>Debitora vecumstruktūru momentuzņēmumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par debitora vecumstruktūras momentuzņēmumiem. Vecumstruktūras momentuzņēmums aprēķina vecas klientu grupas bilances par noteiktu laika periodu. Varat izveidot vecumstruktūras momentuzņēmumu ierakstus vai nu visiem debitoriem, vai debitoru kopai.

Vecumstruktūras momentuzņēmuma informācija tiek rādīta saraksta lapā **Vecas bilances** un lapā **Iekasēšana**. Vispirms ir jāizveido vecumstruktūras momentuzņēmums, un tikai tad varat izmantot **Vecas bilances** saraksta lapu. Saraksta lapa uzskaita tikai tos debitorus, kuriem ir izveidots vecumstruktūras momentuzņēmums.

**Debitora kredīta un iekasēšanas** darbvieta rāda arī debitoru vecumstruktūras. Papildinformāciju skatiet [Kredīta un iekasēšanas pārvaldības Power BI saturā](credit-collections-power-bi.md).

> [!NOTE]
> Lai palīdzētu samazināt laiku, kas nepieciešams vecumstruktūras momentuzņēmuma izveidošanai, ieslēdziet **Debitoru vecumstruktūras veiktspējas uzlabojumu** līdzekli **Līdzekļu pārvaldības** darbvietā. Tomēr neizmantojiet debitoru kopas, ja šī funkcija ir ieslēgta. Ja ir atlasīta debitoru kopa, funkcija nedarbosies, bet joprojām varat izveidot vecumstruktūras momentuzņēmumu.

Veidojot debitora vecumstruktūras momentuzņēmumu, izmantojiet šādus laukus, lai ievadītu informāciju par to:

- **Vecumstruktūras perioda definīcija** - atlasiet vecumstruktūras perioda definīciju vecumstruktūras momentuzņēmumam. Katrai vecumstruktūras perioda definīcijai jums var būt viens vecumstruktūras momentuzņēmums. Vecumstruktūras momentuzņēmums un vecumstruktūras perioda definīcija jāizveido atsevišķi.
- **Kopas ID** – šis lauks ir izvēles. Varat izmantot kopu, lai definētu debitoru kopu, kas jāapstrādā vecumstruktūras momentuzņēmumā. Ja šajā laukā atlasāt debitoru kopu, tad vecumstruktūras momentuzņēmums tiek izveidota tikai tiem debitoru kontiem, kas ir daļa no attiecīgās debitoru kopas. Atlasītās debitoru kopas tipam ir jābūt **Vecumstruktūras momentuzņēmums**. Ja šo lauku atstājat tukšu, vecumstruktūras momentuzņēmums tiek izveidots visiem debitora kontiem.

    > [!NOTE]
    > Ja **Debitora vecumstruktūras veiktspējas uzlabojumu** līdzeklis ir ieslēgts, neatlasiet debitoru kopu.

- **Kritēriji** – vecumstruktūras momentuzņēmums novecos, pamatojoties uz jūsu izvēlēto datumu:

    - **Transakcijas datums** - katra transakcija tiek novecota, pamatojoties uz tās datumu.
    - **Izpildes datums** - katra transakcija tiek novecota, pamatojoties uz tās izpildes datumu.
    - **Dokumenta datums** - katra transakcija tiek novecota, pamatojoties uz tās dokumentēšanas datumu.

- **Novecot no** - atlasiet datumu, ko izmantot laukā **Pašreizējais datums** vecumstruktūras momentuzņēmuma. Vecumstruktūras periodi tad tiek aprēķināti, pamatojoties uz šo datumu. 

    - **Šodienas datums** - izmanto sistēmas datumu. Atlasiet šo opciju, ja apstrāde ir iestatīta palaišanai periodiskā pakešuzdevumā. Pēc tam katru reizi, kad partija tiek palaista, tiek izmantots šīs palaišanas sistēmas datums.
    - **Atlasītais datums** - izmanto jūsu norādīto datumu. Ja atlasāt šo opciju, ir jāievada arī vecumstruktūras datums.

    Piemēram, pašreizējais vecumstruktūras periods ir 30 dienas. Ja šajā laukā atlasāt **Šodienas datumu**, pašreizējais vecumstruktūras periods sākas šodienas datumā un pēc tam ietver iepriekšējās 29 dienas. Ja šajā laukā atlasāt **Atlasīto datumu** un ievadāt datumu, pašreizējais vecumstruktūras periods sākas norādītajā datumā un pēc tam ietver iepriekšējās 29 dienas.

- **Atjaunināt iekasēšanas statusu** – iestatiet šo opciju uz **Jā**, lai atjauninātu iekasēšanas statusu transakciju **Iekasēšanas** lapā no **Samaksas solījums** uz **Neizpildītās samaksas solījums**, ja vecumstruktūras datums ir vēlāks par datumu laukā **Samaksas solījuma datums**. Iestatiet šo opciju uz **Nē**, lai atstātu iekasēšanas statusu nemainītu **Iekasēšanas** lapā.
- **Iekļaut debitorus ar nulles bilanci** – iestatiet šo opciju uz **Jā**, lai iekļautu visus debitorus, neatkarīgi no to bilances. Ja iekļauti visi debitori, ieteicams ieslēgt **Debitoru vecumstruktūras veiktspējas uzlabojumu** līdzekli, un šādi debitoru kopas netiek lietotas. Iestatiet šo opciju uz **Nē**, lai iekļautu tikai debitorus, kuriem ir bilance. Šis iestatījums palīdz paātrināt veiktspēju, jo debitori, kuriem nav bilances, tiek izlaisti.
- **Uzņēmumu diapazons** – cilnē **Uzņēmumu diapazons** atlasiet juridiskās personas (uzņēmumus), kas jāietver vecumstruktūras momentuzņēmumā. Atlasei ir pieejamas tikai juridiskās personas, kas ir iestatītas centralizētajiem maksājumiem. Tad darījumi no atlasītajām juridiskajām personām tiek iekļauti debitoru vecumstruktūras periodos, kuriem ir vienāds puses ID visās šajās juridiskajās personās. Valūtu summas tiek konvertētas uz to juridisko personu valūtu, kura kontā pieteicāties, kad izveidojāt vecumstruktūras momentuzņēmumu.

Mēs iesakām jums plānot šo procesu, lai palaistu to partijā.

> [!NOTE]
> Lai palīdzētu uzlabot pakešuzdevumu veiktspēju vecumstruktūras momentuzņēmumu izveides laikā, ievadiet skaitli laukā **Maksimālais pakešuzdevumu skaits**, kopsavilkuma cilnē **Iekasēšanas noklusējumi**, cilnē **Iekasēšana**, lapā **Debitoru parādu parametri**. Laukā **Debitora vecuma bilances** ieteicams sākt ar noklusēto vērtību **100** un pēc tam koriģēt vērtību, lai optimizētu jūsu situācijas apstrādi.

