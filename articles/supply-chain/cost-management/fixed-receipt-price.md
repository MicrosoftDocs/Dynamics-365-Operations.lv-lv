---
title: Fiksēta saņemtā krājuma cena
description: Šajā rakstā skaidrots, kā var konfigurēt un izmantot fiksētās kvīšu cenas programmā Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: d58e8dcc580bf9327cd89427530f59340e27f4aa
ms.sourcegitcommit: 78576abe5c7cbab1bb69d26c999b038e8c24873a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/13/2022
ms.locfileid: "8954697"
---
# <a name="fixed-receipt-price"></a>Fiksēta saņemtā krājuma cena

[!include [banner](../includes/banner.md)]

**Fiksētā saņemtā** krājuma cena ir opcija *, kuru var atlasīt krājumu modeļu grupā, ja lietojat krājumu modeli, kas nav Standarta izmaksas vai Pārvietots* *novērtētais vidējais*. Agrākās versijās šīs Microsoft Dynamics AX opcijas nosaukums bija Standarta **izmaksas**. Tā tika pārdēvēta par **fiksēto ieejas** plūsmas cenu, kad sistēmā Dynamics AX 2012 tika ieviests jauns standarta izmaksu krājumu modelis. Šajā rakstā skaidrots, kā var konfigurēt un izmantot fiksētās ieejas plūsmas cenas Dynamics 365 Supply Chain Management.

## <a name="about-fixed-receipt-prices"></a>Par fiksētas saņemtā krājuma cenām

Atlasot krājuma **izvēles** **rūtiņu** Fiksētas saņemšanas cena krājumu modeļu grupas lapā, sistēma krājumu ieejas plūsmai izmanto saņemšanas cenu kā standarta izmaksu. Ja pirkšanas cena un noklusējuma krājuma izmaksu cena, kas ir konfigurēta precei, atšķiras, **·** **·** **·** **starpība** tiek grāmatota fiksētās saņemšanas cenas peļņas vai Fiksētas saņemšanas cenas zaudējumu kontā un korespondējošā kontā Fiksētas saņemtā krājuma cenas korespondējošais konts, kuru norādāt lapā Krājumu grāmatošanas metode.

**Tā** kā fiksētas saņemtā krājuma cenas opcija tiek izmantota kopā ar dažādiem krājumu modeļiem (piemēram, pirmais in, pirmais ārā (FIFO); pēdējais ieejiet, pirmais ārā (LIFO); un novērtētais vidējais), *Krājumu* slēgšana un koriģēšanas process vēl joprojām izveidos segšanas **un korekcijas atbilstoši krājumu principam, ko atlasāt krājumu modeļu grupas** lapā. Tomēr korekcijas tiek veiktas tikai krājumu izejas plūsmas darbībām.

Piemēram, esat konfigurējis **preci** *ar krājumu modeļu grupu, kur krājumu modeļa lauks ir iestatīts uz FIFO* **un ir atlasīta opcija Fiksētas** saņemtā krājuma cena. Kad saņemat krājumu, izmantojot pirkšanas pasūtījumu, krājumu vērtība tiek iestatīta uz krājuma noklusējuma izmaksu cenas vērtību produktu ieejas plūsmas laikā. Kad pirkšanas pasūtījums tiek iekļauts rēķinā, ja rēķina cena atšķiras, sistēma krājumu kontā grāmato izlaistās preces noklusēto izmaksu cenu. Tas iegrāmato starpību fiksētās saņemtā krājuma cenas peļņas vai zaudējumu kontā. Vēlāk, kad prece tiek pārdota vai patērēta, sistēma izmanto krājuma vidējo rādītāju pārdošanas pasūtījuma rēķina grāmatošanas laikā (ja vien netiek lietota atzīmēšana).

Palaižot krājumu slēgšanas *un koriģēšanas* procesu, sistēma izveido segšanu ar pirmo izdošanas darbību attiecībā pret pirmo ieejas plūsmu. Atšķirība starp ieejas plūsmas cenu, kas tika izmantota saņemšanai, un ieejas plūsmas vidējo rādītāju, kas tika izmantots izdošanai, tiek grāmatota jaunā dokumentā.

## <a name="enable-fixed-receipt-prices"></a>Iespējot fiksētas ieejas plūsmas cenas

Lai iespējotu krājuma fiksētās ieejas plūsmas cenas, veiciet šādus soļus.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Krājumi \> Krājumu modeļu grupas**.
2. Izveidojiet jaunu krājumu modeļu grupu vai atlasiet esošu modeļu grupu.
3. Kopsavilkuma cilnē **Izmaksu metode > Izmaksu** grāmatošana atzīmējiet izvēles rūtiņu **Fiksēta saņemtā** krājuma cena.

    > [!NOTE]
    > Izvēles rūtiņu Fiksētas saņemtā krājuma **cena nevar atzīmēt**, ja **lauks Krājumu modelis** ir iestatīts uz Standarta *izmaksas vai* Pārvietojams *vidējais*.

4. Aizvērt lapu.

Pēc opcijas Fiksētas **saņemšanas cenas iespējošanas** ir jāatjaunina noliktavas grāmatošanas metode, veicot šādus soļus.

1. Doties uz **Krājumu vadība \> Iestatīšana \> Grāmatojums \> Grāmatošana**.
1. Cilnes Pirkšanas **pasūtījums** kolonnā Atlasīt **atlasiet** Fiksētas saņemtā **krājuma cenas peļņa**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**.
1. Iestatiet jaunu rindu tā, lai tā attiecas uz krājumu modeļu grupu, kam iespējota fiksēta saņemtā krājuma cena, un norādiet galveno kontu, kas tiek lietots fiksētas saņemtā krājuma cenas peļņas reģistrēšanai pirkšanas pasūtījumos. Konfigurējiet citus iestatījumus pēc jūsu pieprasītā.
1. Kolonnā Atlasīt **atlasiet** Fiksētas saņemtā **krājuma cenas zaudējumus**. Pievienojiet jaunu rindu, kas attiecas uz krājumu modeļu grupu, kurā iespējota fiksēta saņemtā krājuma cena, un norādiet galveno kontu, kas tiek lietots, lai ierakstītu fiksētus ieejas plūsmas cenas zaudējumus pirkšanas pasūtījumiem. Konfigurējiet citus iestatījumus pēc jūsu pieprasītā.
1. Kolonnā Atlasīt atlasiet **Fiksētas** saņemtā krājuma **cenas korespondējošo kontu**. Pievienojiet jaunu rindu, kas attiecas uz krājumu modeļu grupu, kam iespējota fiksēta saņemtā krājuma cena, un norādiet galveno kontu, kas tiek lietots, lai ierakstītu fiksētās saņemtā krājuma cenas korespondējošās vērtības pirkšanas pasūtījumiem. Konfigurējiet citus iestatījumus pēc jūsu pieprasītā.
1. Cilnes Krājumi **kolonnā** Atlasīt atlasiet **Fiksētas** saņemtā **krājuma cenas peļņa**. Pievienojiet jaunu rindu, kas attiecas uz krājumu modeļu grupu, kam iespējota fiksēta saņemtā krājuma cena, un norādiet galveno kontu, kas tiek izmantots, lai ierakstītu fiksētās saņemtā krājuma cenas peļņu. Konfigurējiet citus iestatījumus pēc jūsu pieprasītā.
1. Kolonnā Atlasīt **atlasiet** Fiksētas saņemtā **krājuma cenas zaudējumus**. Pievienojiet jaunu rindu, kas attiecas uz krājumu modeļu grupu, kurā iespējota fiksēta saņemtā krājuma cena, un norādiet galveno kontu, kas tiek lietots, lai ierakstītu krājuma fiksētas saņemtā krājuma cenas zaudējumus. Konfigurējiet citus iestatījumus pēc jūsu pieprasītā.

> [!NOTE]
> Parasti ieteicams, lai lauki Fiksētas **saņemšanas cenas peļņa un** Fiksētas **saņemtā** krājuma cenas zaudējumi lietotu to pašu galveno kontu gan pirkšanas pasūtījumiem, gan krājumiem.

> [!IMPORTANT]
> Ja maināt **lapas** **·** **Izlaistās** preces kopsavilkuma cilnes Pārvaldīt izmaksas laukā Cena, sistēma automātiski pārvērtē rīcībā esošos krājumus. Kā manuālu risinājumu atveriet lapu **Slēgšana un pielāgošana** un **\>** darbību rūtī atlasiet Rīcībā rūts korekcija. Pēc tam atlasiet rīcībā esošos krājumus un pielāgojiet tos pašreizējai cenai. Viena skaidra priekšrocība, izmantojot standarta izmaksu krājumu modeli, ir tā, ka sistēma automātiski pārvērtē rīcībā esošos krājumus.
