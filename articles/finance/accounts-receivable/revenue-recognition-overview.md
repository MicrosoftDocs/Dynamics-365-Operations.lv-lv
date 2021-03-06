---
title: Ieņēmumu atzīšanas pārskats
description: Šajā tēmā ir sniegta informācija par ieņēmumu atzīšanas līdzekli. Šis līdzeklis nodrošina elastīgu platformu, kas ļauj jums noteikt uzņēmuma specifiskos noteikumus, lai varētu atpazīt gan ieņēmumu cenu, gan ieņēmumu grafiku vairāku elementu pasūtījumiem.
author: kweekley
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: edc0bab7287e271f1d1197d87a95709599e12b5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820549"
---
# <a name="revenue-recognition-overview"></a>Ieņēmumu atzīšanas pārskats

[!include [banner](../includes/banner.md)]

Uzņēmumiem nozarēs, kas pārdod vairākus elementus, piemēram, preces, pakalpojumus, abonementus un tā tālāk, ir jābūt iespējai noņemt vairāku elementu pasūtījumus, lai ieņēmumus varētu atpazīt, pamatojoties uz uzņēmumam un nozarei raksturīgu vadlīniju kopu.

> [!NOTE]
> Ieņēmumu atzīšanas līdzekli nav iespējams ieslēgt, izmantojot līdzekļu pārvaldību. Pašlaik jāizmanto konfigurācijas atslēgas, lai to ieslēgtu.

> Ieņēmumu atzīšana, tostarp komplektu funkcionalitāte, netiek atbalstīta izmantošanai Commerce kanālos (e-komercija, POS, zvanu centrs). Krājumus, kas ir konfigurēti ar ieņēmumu atzīšanu, nedrīkst pievienot pasūtījumiem vai transakcijām, kas izveidotas Commerce kanālos.

Parasti ieņēmumu atzīšanas procesu var izmantot, lai veiktu šos uzdevumus:

* Sadalīt ieņēmumus, lai palīdzētu nodrošināt, ka tiek atzīta atbilstoša ieņēmumu cena, pamatojoties uz vairāku elementu pasūtījumos esošo komponentu vērtību.
* Atlikt ieņēmumus, pamatojoties uz ieņēmumu grafiku, kas atspoguļo līguma termiņu un procentus ieņēmumu atpazīšanai laika gaitā.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Video [Kā izmantot ieņēmumu atzīšanu programmā Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (parādīts iepriekš) ir iekļauts [Finance and Operations atskaņošanas sarakstā](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kas ir pieejams vietnē YouTube.

Ieņēmumu atzīšanas līdzeklis nodrošina elastīgu platformu, kas ļauj jums noteikt uzņēmuma specifiskos noteikumus, lai varētu atpazīt gan ieņēmumu cenu, gan ieņēmumu grafiku.

Izlaistie produkti tiek izmantoti, lai atbalstītu ieņēmumu atzīšanu pārdošanas pasūtījuma dokumentos. Izlaistās preces ietver iestatījumus, kas nepieciešami, lai noteiktu ieņēmumu cenu un ieņēmumu grafiku. Pārdošanas pasūtījumu var izveidot no laika un materiālu projekta.

Uzņēmumi var izmantot ieņēmumu grafika funkcionalitāti, neizmantojot ieņēmumu cenas funkcionalitāti. Tāpēc pārdošanas pasūtījuma rindu cena tiks izmantota kā ieņēmumi vai atliktie ieņēmumi. Ja pārdošanas pasūtījuma rindā pastāv ieņēmumu grafiks, pārdošanas pasūtījuma rindā norādītā cena tiks atlikta. Ja pārdošanas pasūtījuma rindā nav ieņēmumu grafika, pārdošanas pasūtījuma rindā norādītā cena tiks grāmatota ieņēmumu kontā, kad tiek izrakstīts rēķins.

Ieņēmumu cena tiek aprēķināta vai nu pēc pārdošanas pasūtījuma apstiprināšanas, vai tad, kad rēķins ir iegrāmatots. Lai priekšskatītu ieņēmumu cenu pirms rēķina grāmatošanas, ir jāapstiprina pārdošanas pasūtījums.

Kad pārdošanas pasūtījums tiek apstiprināts, tiek izveidots arī prognozētais ieņēmumu grafiks, ja pārdošanas pasūtījuma rindai ir ieņēmumu grafiks. Kad pārdošanas pasūtījums ir iekļauts rēķinā, paredzamais ieņēmumu grafiks tiek dzēsts un paredzamais ieņēmumu grafiks tiek aizstāts ar faktisko ieņēmumu atzīšanas grafiku.

Detalizēta informācija par ieņēmumu atzīšanas grafiku tiek uzturēta katrai pārdošanas pasūtījuma rindai. Tāpēc ieņēmumu atzīšanas vadītājs var skatīt detalizētu informāciju un var nodot rindas ieņēmumiem, kad līgumsaistības ir pabeigtas. Katra perioda beigās ieņēmumu atzīšanas vadītājs var izveidot ieņēmumu žurnālu, lai izlaistu visas grafika rindas, kas maksājamas tieši tajā datumā vai pirms datuma, kas tiek definēts. Šis ieņēmumu žurnāls netiek grāmatots nekavējoties. Tāpēc ieņēmumu atzīšanas vadītājs var pārbaudīt, vai pareizās summas tiek atbrīvotas no atliktajiem ieņēmumiem uz faktiskajiem ieņēmumiem.

Ja līguma izmaiņa rada jaunu pārdošanas pasūtījuma rindu, kas jāpievieno esošajam pārdošanas pasūtījumam vai jaunam pārdošanas pasūtījumam, var tikt palaists pārdales process, lai labotu ieņēmumu cenu visās rindās pārdošanas pasūtījumos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]