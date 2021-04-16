---
title: Pārvaldīt folio
description: Šajā tēmā ir aprakstīts, kā strādāt ar folio. Parasti folio veido viena kreditora preces vienai entītijai vai uzņēmumam vienā sūtījumā. Folio preces var būt vienā konteinerā vai izplatītas starp vairākiem konteineriem.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 99159d2197648b8f17a719b74c8cd6ea4bffe550
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833837"
---
# <a name="manage-folios"></a>Pārvaldīt folio

[!include [banner](../../includes/banner.md)]

Folio bieži nosaka muitas noteikumi. Tas var ietvert viena kreditora preces vienam elementam vai uzņēmumam vienā sūtījumā. Folio preces var būt vienā konteinerā vai izplatītas starp vairākiem konteineriem.

Lai atvērtu lapu **Visi folio**, dodieties uz sadaļu **Kopējās izmaksas \> Folio \> Visi folio**. Šajā lapā ir parādīts visu pašreizējo folio saraksts. Jūs varat izmantot pogas Darbību rūtī, lai izveidotu, dzēstu un darbotos ar folio. Sarakstā atlasiet jebkuru folio, lai apskatītu tā detaļas lapā **Folio**.

## <a name="action-pane"></a>Darbības rūts

Darbību rūts lapā **Visi folio** un **Folio** nodrošina pogas, kas ļauj strādāt ar atlasīto folio. Katra poga veic vienu darbību. Darbību rūtī ir ietvertas arī cilnes, katra no tām savukārt sniedz saistītu pogu kopu. Izņemot, ja atzīmēts, visas pogas un cilnes, kas ir aprakstītas tālākminošajos apakšsadaļās, ir pieejamas gan saraksta skatījumā (t.i., lapā **Visi folio**), gan detalizētajā skatā (t.i., lapā **Folio**).

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Pogas, kas parādās tieši darbību rūtī

Šajā tabulā ir aprakstītas pogas, kas ir pieejamas tieši darbību rūtī.

| Poga | Apraksts |
|---|---|
| Jauna | Folio izveide. |
| Delete | Dzēst atvērto vai atlasīto folio. |
| Reisa izmaksas | Atvērt lapu **Reisu izmaksas**, kurā var skatīt un pievienot folio līmeņa izmaksas visām reisa precēm. Kad folio izmaksas tiek manuāli pievienotas reisam, tās automātiski tiek pievienotas izmaksu pieprasījuma lapai un izmaksātas katrai labākās preces atbilstoši metodei, kas ir norādīta lapā **Reisu izmaksas**. |

### <a name="buttons-on-the-manage-tab"></a>Pogas cilnē Pārvaldīt

Šajā tabulā ir aprakstītas pogas, kas ir pieejamas darbību rūts cilnē **Pārvaldīt**.

| Poga | Apraksts |
|---|---|
| Grāmatot saņemšanas sarakstu | Grāmatojiet saņemšanas sarakstu visām pirkšanas pasūtījuma rindām folio. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns saņemšanas saraksta grāmatošanas dialoglodziņš. |
| Grāmatot produktu ieejas plūsmu | Grāmatojiet saņemto preču pavadzīmi visām pirkšanas pasūtījuma rindām folio. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns saņemto preču pavadzīmes grāmatošanas dialoglodziņš. |
| Grāmatot rēķinu | Grāmatojiet rēķinu visām pirkšanas pasūtījuma rindām folio. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns rēķina grāmatošanas dialoglodziņš. |
| Nosūtīšanas pārsūtīšanas pasūtījums | Grāmatot pārsūtīšanas pasūtījumu visām pārsūtīšanas pasūtījuma rindām, kas attiecas uz pašreizējo folio saistītajā sūtījumā. |
| Saņemt pārsūtīšanas pasūtījumu | Grāmatot pārsūtīšanas pasūtījuma pavadzīmi visām pārsūtīšanas pasūtījuma rindām, kas attiecas uz pašreizējo folio saistītajā sūtījumā. |
| Saņemtās tranzītpreces | Saņemt visas pasūtījuma rindas, kas ir tranzītā folio. |
| Saņemtie dokumenti | Atjauniniet opcijas **Saņemtie dokumenti** iestatījumus uz *Jā*. Šo pogu var izmantot, lai bloķētu krājumu un/vai pirkšanas rindu tā, ka to vairs nevar atjaunināt. |
| Atrast automātiskās izmaksas | Atrast atbilstošās reisa izmaksas. Ja šīs izmaksas jau ir atrastas vai atjauninātas, tiek saņemts šāds ziņojums: "Pastāv rēķinā neiekļautas izmaksu rindas. Vai vēlaties tos pārrakstīt?" Ievērojiet, ka reisu izmaksas, kas ir pievienotas folio un kurām izrakstīts rēķins, netiks pārrakstītas. |
| Izveidot saņemšanas žurnālu | Izveidojiet organizāciju saņemšanas žurnālu, izmantojot papildu noliktavas funkcijas. Varat atlasīt **Inicializēt daudzumu (ieteicams)**, **Izveidot no tranzīta precēm** un/vai **Izveidot no pirkšanas pasūtījumiem**. Pēdējā opcija ir atkarīga no tā, vai tiek lietota tranzīta preču apstrāde. |
| Uzkrāt izmaksas | Uzkrāt izmaksas, kur izmaksu tipam ir norādīts debeta Virsgrāmatas konts. Šī poga parasti tiek lietota, kad krājums ir tranzītā vai kad preces ir saņemtas un iekļautas rēķinā. |

### <a name="buttons-on-the-general-tab"></a>Pogas cilnē Vispārīgi

Šajā tabulā ir aprakstītas pogas, kas ir pieejamas darbību rūts cilnē **Vispārīgi**.

| Poga | Apraksts |
|---|---|
| Saņemšanas saraksts | Grāmatojiet saņemšanas sarakstu visām pirkšanas pasūtījuma rindām folio. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns saņemšanas saraksta grāmatošanas dialoglodziņš. |
| Produktu ieejas plūsma | Skatiet produktu ieejas plūsmas ierakstu, ja tas tiek izmantots. |
| Krājumu saņemšana | Skatiet krājumu saņemšanas žurnālu, ja tas tiek izmantots. |
| Izmaksu pieprasījums | Atveriet izmaksu pieprasījuma lapu, lai skatītu visas reisa izmaksas, tostarp pārvadāšanas konteineru, folio un pirkšanas pasūtījumu. Varat koriģēt precīzu lapas skatu, izmantojot darbību Skatīt. Izmaksu uzziņu lapā varat apskatīt jebkuru no apgabaliem, plus krājuma un izmaksu tipa kodu. Noņemot šos krājumus, var koriģēt lapu, grupējot izmaksas. Šī iespēja var būt noderīga, ja izmantojat izmērus un krāsas. Varat mainīt lapā parādītās dimensijas. Lapa **Izmaksas** rāda tikai tos izmaksu tipu kodus, kur cilnes **Grāmatošana** ieraksts **Dr** ir iestatīts uz *Krājums*. |

## <a name="header-view"></a>Virsraksta skatījums

Lai atvērtu **Galvenes** skatu, atveriet folio un pēc tam atlasiet cilni **Galvene** folio galvenes augšējā labajā stūrī.

### <a name="settings-on-the-general-fasttab"></a>Kopsavilkuma cilnes Vispārīgi iestatījumi

Šajā tabulā ir aprakstīti lauki, kas ir pieejami folio **Galvenes** skata kopsavilkuma cilnē **Vispārīgi**.

| Lauks | Apraksts |
|---|---|
| Folio | Folio nosaukums. Šis nosaukums tiek automātiski izveidots, kad tiek izveidots folio.|
| Reiss | Ceļojums, kas saistīts ar folio. |
| Muitas aģents | Izvēlieties folio muitas starpnieku. Muitas starpnieki tiek noteikti kreditoram. Tie ļauj automātiski noteikt izveidotās izmaksas. |
| Sākotnējā gaisa kravas pavadzīme/preču transporta pavadzīme | Norādiet mājas gaisa ceļa laiku vai preču transporta pavadzīmi, kas attiecas uz folio. |
| Uzņēmums | Juridiskā persona (uzņēmums), kas ir saistīts ar folio. |
| Kravas kontroles numurs | Šo lauku izmanto dažu valstu vai reģionu muitas nodaļas. |
| Mērījums | Šis lauks aktivizē mērījumu norādīšanu modulī **Kopējās izmaksas**. Bieži vien mērījumus izmanto organizācijas, kas nezina preču individuālo tilpumu vai svaru, bet pieprasa daudz precīzāku sadali nekā to sniedz daudzums vai skaits. Kravas ekspediators vai aģents nodrošina organizāciju ar svara vai kubikmetru krājumu līmenī vai pirkšanas pasūtījuma līmenī. Ja parametrs ir atlasīts vai ievadīts manuāli, to var atjaunināt automātiski. |
| Mērvienība | Vienība, kas attiecas uz norādīto mērījumu. |
| Kastu skaits | Kastu skaits folio. Atkarībā no parametru atlases šo lauku var atjaunināt automātiski. |
| Kreditora konts | Atlasiet kreditoru, kas ir saistīts ar folio. Šis lauks ir paredzēts tikai informatīviem nolūkiem. Tā neietekmē funkcionalitāti. |
| Vārds, uzvārds | Atlasītā kreditora konta nosaukums. |
| Atzīmes | Ievadiet papildu informāciju, kas saistīta ar folio. |
| Preču apraksts | Atlasīt preču aprakstu, lai palīdzētu noteikt folio. Papildinformāciju skatiet sadaļā [Preču apraksts](shipping-information-setup.md#description-of-goods). |
| Apstiprināšanas datums | Šis lauks ir saistīts ar nodokļa ievades lapu. **Kopējo izmaksu** modulis izmantos muitas valūtas maiņas kursu datumā, ko iestatīsit šeit. Noklusējuma vērtība ir datums nodokļa ievades lapā. |
| Muitas ID | Ievadiet muitas ID. Šo ID nodrošina valstu vai reģionu muitas nodaļas. |
| Tarifa kods | Ievadiet tarifa kodu, ko saistīt ar folio. Šo kodu parasti pieprasa (un definē) valsts vai reģions, uz kuru tiek veikts nosūtīšanu. |

### <a name="settings-on-the-delivery-fasttab"></a>Kopsavilkuma cilnes Dimensijas iestatījumi

Šajā tabulā ir aprakstīti lauki, kas ir pieejami folio **Galvenes** skata kopsavilkuma cilnē **Piegāde**.

| Lauks | Apraksts |
|---|---|
| Folio datums | Atlasiet datumu, ko saistīt ar folio. Noklusējuma vērtība ir reisa datuma izveide. |
| ETA nosūtīšanas ostā | Plānotais saņemšanas laiks (ETA) datumā galamērķa ostā ("uz" ostu). |
| Aprēķinātais piegādes datums | Parasti datums, kad precēm jāienāk noliktavā. Šis lauks netiek izmantots, kad tiek aprēķināts aprēķinātais piegādes datums. (Tā vietā tiek izmantots izsekotās kontroles plānotais piegādes datums.) Lai iestatītu šo lauku tā, lai vērtība atbilstu izsekošanas kontroles plānotjam piegādes datumam, izmantojiet [Izsekošanas kontroles centru](delivery-information-setup.md#tracking-control-center). |
| Oriģinālais dokuments saņemts | Sākotnējais dokumentu saņemšanas datums. |
| Brokeris ieteica | Muitas starpnieka ieteikšanas datums. |
| Sākotnējais piegādes rēķins nosūtīts | Datums, kad tika nosūtīta sākotnējā preču transporta pavadzīme. |
| Preces izpildītas | Datums, kad preces tika izlaistas. |
| Norunātā tikšanās ar klientu | Debitora tikšanās datums. |
| Sūtījums piegādāts noliktavā | Datums, kad preces tika piegādātas noliktavā. |
| Pārbaudes datums | Pārbaudes datums. |
| Piegādes instrukcijas | Piegādes instrukciju saņemšanas datums. |
| No ostas | Osta, no kuras nāk reiss. |
| Uz ostu | Reisa saņemšanas osta. Sūtījuma konteineram, iespējams, ir cita osta, jo kuģis var piestāt vairākās ostās. |

### <a name="settings-on-the-export-fasttab"></a>Kopsavilkuma cilnes Eksports iestatījumi

Šajā tabulā ir aprakstīti lauki, kas ir pieejami folio **Galvenes** skata kopsavilkuma cilnē **Eksports**.

| Lauks | Apraksts |
|---|---|
| Eksportētājs | Eksportētāju var uzglabāt folio. Starptautiskā tirdzniecībā pirkšanas pasūtījumu var nosūtīt vienam uzņēmumam, bet saņemt preces no cita uzņēmuma. Izsekošana un dokumentācija ir obligāta muitas iestādēm. Eksportētāja nosaukumu un adresi var glabāt šeit. |
| Vārds, uzvārds | Atlasītā eksportētāja nosaukums. |

## <a name="lines-view"></a>Rindu skats

Lai atvērtu **Rindu** skatu, atveriet folio un pēc tam atlasiet cilni **Rindas** folio galvenes augšējā labajā stūrī.

### <a name="information-on-the-folio-fasttab"></a>Kopsavilkuma cilne Informācija par folio

Kopsavilkuma cilne **Folio** **Rindu** skatā rāda informāciju par folio. Lielākā daļa šīs informācijas parādās arī **Galvenes** skatā, kā aprakstīts iepriekš šajā tēmā.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Kopsavilkuma cilnes Rindas informācija un pogas

Kopsavilkuma cilne **Rindas** skatā **Rindas** rāda detalizētu informāciju par katru pilnu vai daļēju pirkšanas pasūtījuma rindu, kas iekļauta pašreizējā folio.

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Rindu** kopsavilkuma cilnes **Rindu** skatā.

| Poga | Apraksts |
|---|---|
| Aizvākt | Noņemt atlasīto pirkšanas pasūtījuma rindu no reisa. |
| Krājumi \> Darbības | Skatiet krājumu darbības atlasītajai pirkšanas pasūtījuma rindai. Ievērojiet, ka, ja izmantojat tranzīta preces, tiek parādīts arī oriģinālais pasūtījums un tranzīta preču pasūtījumi. |
| Krājums \> Dimensiju rādīšana | Atveriet dialoglodziņu, kur var atlasīt krājumu dimensijas, kas parādītas izmaksu darbībām, kuras skatāt. |
| Atsvaidzināt | Atjauniniet informāciju, kas saistīta ar atlasītās pirkšanas pasūtījuma rindas rindas summu, svaru vai tilpumu. |

### <a name="information-on-the-lines-details-fasttab"></a>Kopsavilkuma cilnes Rindas informācija

Kopsavilkuma cilne **Detalizēta informācija par rindām** **Rindu** skatā rāda detalizētu informāciju par pirkšanas pasūtījuma rindu, kas pašlaik ir atlasīta kopsavilkuma cilnē **Rindas**.
