---
title: Debitora vecumstruktūru momentuzņēmumi
description: Šajā rakstā ir sniegta informācija par klientu novecošanas momentuzņēmumiem. Vecumstruktūras momentuzņēmums aprēķina vecas klientu grupas bilances par noteiktu laika periodu.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: e4ccc8ac9b5374ca0713167a17b8704727c687fd
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775246"
---
# <a name="customer-aging-snapshots"></a>Debitora vecumstruktūru momentuzņēmumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par klientu novecošanas momentuzņēmumiem. Vecumstruktūras momentuzņēmums aprēķina vecas klientu grupas bilances par noteiktu laika periodu. Varat izveidot vecumstruktūras momentuzņēmumu ierakstus vai nu visiem debitoriem, vai debitoru kopai.

Vecumstruktūras momentuzņēmuma informācija tiek rādīta saraksta lapā **Vecas bilances** un lapā **Iekasēšana**. Vispirms ir jāizveido vecumstruktūras momentuzņēmums, un tikai tad varat izmantot **Vecas bilances** saraksta lapu. Saraksta lapa uzskaita tikai tos debitorus, kuriem ir izveidots vecumstruktūras momentuzņēmums.

**Debitora kredīta un iekasēšanas** darbvieta rāda arī debitoru vecumstruktūras. Papildinformāciju skatiet [Kredīta un iekasēšanas pārvaldības Power BI saturā](credit-collections-power-bi.md).

> [!NOTE]
> Lai palīdzētu samazināt novecošanas momentuzņēmuma izveidei nepieciešamo laiku, darbvietā Līdzekļu **pārvaldība** ieslēdziet šādus līdzekļus: 
> - **Debitoru novecošanas veiktspējas uzlabošana** 
> - **Klientu novecošanas veiktspējas uzlabošana ar klientu pūliem**  
>Ja ir iespējotas abas funkcijas, klientu pūlus **var izmantot,** veidojot novecošanās momentuzņēmumu. 

Veidojot debitora vecumstruktūras momentuzņēmumu, izmantojiet šādus laukus, lai ievadītu informāciju par to:

- **Vecumstruktūras perioda definīcija** - atlasiet vecumstruktūras perioda definīciju vecumstruktūras momentuzņēmumam. Katrai vecumstruktūras perioda definīcijai jums var būt viens vecumstruktūras momentuzņēmums. Vecumstruktūras momentuzņēmums un vecumstruktūras perioda definīcija jāizveido atsevišķi.
- **Kopas ID** – šis lauks ir izvēles. Varat izmantot kopu, lai definētu debitoru kopu, kas jāapstrādā vecumstruktūras momentuzņēmumā. Ja šajā laukā atlasāt debitoru kopu, tad vecumstruktūras momentuzņēmums tiek izveidota tikai tiem debitoru kontiem, kas ir daļa no attiecīgās debitoru kopas. Atlasītās debitoru kopas tipam ir jābūt **Vecumstruktūras momentuzņēmums**. Ja šo lauku atstājat tukšu, vecumstruktūras momentuzņēmums tiek izveidots visiem debitora kontiem.


- **Kritēriji** – vecumstruktūras momentuzņēmums novecos, pamatojoties uz jūsu izvēlēto datumu:

    - **Transakcijas datums** - katra transakcija tiek novecota, pamatojoties uz tās datumu.
    - **Izpildes datums** - katra transakcija tiek novecota, pamatojoties uz tās izpildes datumu.
    - **Dokumenta datums** - katra transakcija tiek novecota, pamatojoties uz tās dokumentēšanas datumu.

- **Novecot no** - atlasiet datumu, ko izmantot laukā **Pašreizējais datums** vecumstruktūras momentuzņēmuma. Vecumstruktūras periodi tad tiek aprēķināti, pamatojoties uz šo datumu. 

    - **Šodienas datums** - izmanto sistēmas datumu. Atlasiet šo opciju, ja apstrāde ir iestatīta palaišanai periodiskā pakešuzdevumā. Pēc tam katru reizi, kad partija tiek palaista, tiek izmantots šīs palaišanas sistēmas datums.
    - **Atlasītais datums** - izmanto jūsu norādīto datumu. Ja atlasāt šo opciju, ir jāievada arī vecumstruktūras datums.

   Piemēram, pašreizējais vecumstruktūras periods ir 30 dienas. Ja šajā laukā atlasāt **Šodienas datumu**, pašreizējais vecumstruktūras periods sākas šodienas datumā un pēc tam ietver iepriekšējās 29 dienas. Ja šajā laukā atlasāt **Atlasīto datumu** un ievadāt datumu, pašreizējais vecumstruktūras periods sākas norādītajā datumā un pēc tam ietver iepriekšējās 29 dienas.

- **Atjaunināt iekasēšanas statusu** – iestatiet šo opciju uz **Jā**, lai atjauninātu iekasēšanas statusu transakciju **Iekasēšanas** lapā no **Samaksas solījums** uz **Neizpildītās samaksas solījums**, ja vecumstruktūras datums ir vēlāks par datumu laukā **Samaksas solījuma datums**. Iestatiet šo opciju uz **Nē**, lai atstātu iekasēšanas statusu nemainītu **Iekasēšanas** lapā.
- **Iekļaut debitorus ar nulles bilanci** – iestatiet šo opciju uz **Jā**, lai iekļautu visus debitorus, neatkarīgi no to bilances. Ja iekļaujat visus klientus, ieteicams ieslēgt gan klientu novecošanas veiktspējas uzlabošanu, gan **klientu** novecošanas veiktspējas uzlabošanu **, izmantojot klientu pūla** funkcijas. Iestatiet šo opciju uz **Nē**, lai iekļautu tikai debitorus, kuriem ir bilance. Šis iestatījums palīdzēs paātrināt veiktspēju, jo klienti, kuriem nav līdzsvara, tiek izlaisti.
- **Apejiet kredītlimita aprēķinus novecošanas laikā — ja šī opcija ir iestatīta uz** Jā, novecošanas **process nepārrēķinās** katram debitoram pieejamo **pavadzīmes starpsummas summu,** Atvērtā pasūtījuma starpsummas **summu** un **Kredītu**. Šie atlikumi tiek parādīti **lapas Vecuma bilances** sadaļā FactBox sadaļā **Kredītlimits**. Lai novecošanas procesā nodrošinātu ātrāku veiktspēju, iestatiet šai opcijai vērtību **Jā**. Iestatiet to uz **Nē**, lai pārrēķinātu atlikumus, veicot novecošanās procesu. 
- **Uzņēmumu diapazons** – cilnē **Uzņēmumu diapazons** atlasiet juridiskās personas (uzņēmumus), kas jāietver vecumstruktūras momentuzņēmumā. Atlasei ir pieejamas tikai juridiskās personas, kas ir iestatītas centralizētajiem maksājumiem. Tad darījumi no atlasītajām juridiskajām personām tiek iekļauti debitoru vecumstruktūras periodos, kuriem ir vienāds puses ID visās šajās juridiskajās personās. Valūtu summas tiek konvertētas uz to juridisko personu valūtu, kura kontā pieteicāties, kad izveidojāt vecumstruktūras momentuzņēmumu.

Mēs iesakām jums plānot šo procesu, lai palaistu to partijā.

> [!NOTE]
> Lai palīdzētu uzlabot pakešuzdevumu veiktspēju vecumstruktūras momentuzņēmumu izveides laikā, ievadiet skaitli laukā **Maksimālais pakešuzdevumu skaits**, kopsavilkuma cilnē **Iekasēšanas noklusējumi**, cilnē **Iekasēšana**, lapā **Debitoru parādu parametri**. **Laukā Klientu bilances vecums** ieteicams sākt ar vērtību no **12** līdz **20** un pēc tam pielāgot vērtību, lai optimizētu apstrādi atbilstoši jūsu situācijai. Mēs neiesakām iestatīt šo vērtību, kas ir lielāka par **30**, jo tas ietekmēs veiktspēju. 

