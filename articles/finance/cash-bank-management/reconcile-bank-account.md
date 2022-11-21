---
title: Bankas konta saskaņošana
description: Šajā rakstā ir aprakstīts, kā saskaņot bankas kontu.
author: angelad116
ms.date: 11/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 576dcd320600f4741a43bfeee53198637bffce15
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779532"
---
# <a name="reconcile-a-bank-account"></a>Bankas konta saskaņošana

[!include[banner](../includes/banner.md)]

Saņemot bankas izrakstu, periodiski ir jāsaskaņo juridiskās personas bankas transakcijas ar bankas izrakstā norādītajām transakcijām.

Jūs nevarat saskaņot bankas konta pārskatu ar bankas kontu, ja jebkuriem pārskatā uzskaitītiem čekiem vai depozīta kvīts maksājumiem pašreiz ir statuss **Gaida atcelšanu**. Kad čeka anulēšana vai depozīta kvīts maksājuma atcelšana ir iegrāmatota vai apvērsta, status vairs netiks rādīts kā **Gaida atcelšanu**, un jūs varēsiet saskaņot bankas kontu.

1. Atveriet sadaļu **Kases un bankas vadība** \> **Banku konti** \> **Banku konti**. Atlasiet bankas kontu, kas jāsaskaņo ar bankas izrakstu, un atlasiet **Saskaņot** > **Kontu saskaņošana**.

2. Ievadiet informāciju laukos **Bankas izraksta datums** un **Bankas izraksts**. Laukā **Beigu bilance** varat ievadīt bankas konta bilanci saskaņā ar bankas konta pārskata datiem.

3. Atlasiet **Transakcijas**, lai atvērtu lapu **Kontu saskaņošana**.

4. Katrai transakcijai, kas ir iekļauta bankas izrakstā, atzīmējiet izvēles rūtiņu Notīrīt **,** ja summa programmā Dynamics 365 Finance atbilst summai bankas izrakstā. Varat arī ievadīt vai mainīt vērtību laukā **Bankas transakcijas veids**. Šī lauka vērtība ir svarīga jūsu bankas konta statistikai un dažiem pārskatiem.
    

>[!NOTE]
>Neatlasiet izvēles rūtiņu **Dzēsts** tām transakcijām, kuras nav iekļautas bankas konta pārskatā. Šīs transakcijas tiks rādītas šajā lapā līdz brīdim, kamēr tās netiks saskaņotas nākamajā bankas konta pārskatā.
>Izvēles rūtiņa **Dzēsts** nav pieejama, ja transakcijas statuss ir **Gaida atcelšanu**. Transakcijām var būt šis statuss, ja Finance ir iestatīta tā, lai pirms grāmatošanas visas apgriešanas vai atcelšanas tiktu nosūtītas apstiprināšanai. Kad čeka anulēšana vai depozīta kvīts maksājuma atcelšana ir iegrāmatota vai apvērsta, status vairs netiks rādīts kā **Gaida anulēšanu**, un jūs varēsiet saskaņot bankas kontu ar bankas izrakstu.


Lai atzīmētu izvēles rūtiņu **Dzēsts** čeku intervālam, kas visi ir redzami bankas izrakstā, atlasiet **Atzīmēt čeku intervālu** un pēc tam norādiet intervālu.

5.  Ja bankas konta transakciju summa neatbilst bankas izrakstā norādītajai transakciju summai, laukā **Labojuma summa** ievadiet labojuma summu.
    

> [!NOTE]
> Ja labojamas transakcijas fiskālais periods ir noslēgs, tad lauku **Labojuma summa** nevarēs lietot. Lai veiktu labojumus, varat izveidot rindu ar transakcijas datumu, kas ir atvērtajā fiskālajā periodā. Šādā gadījumā ir jāpievieno finanšu dimensijas, kas tika izmantotas sākotnējā transakcijā, kā arī korespondējošais galvenais konts.



6.  Izveidojiet darbības ierakstiem (piemēram, komisijas un procenti), kas ir iekļauti bankas izrakstā, bet nav ierakstīti programmā Finance. Ievadiet **Bankas transakcijas veidu** un atbilstīgās finanšu dimensijas.

7.  Kad bankas konta pārskatā esošas darbības ir atzīmētas kā **Dzēsts**, summa laukā **Nesaskaņots** kas tiek pastāvīgi pārrēķināta, kamēr ievadāt izmaiņas, tuvojas nullei. Kad summa sasniedz nulles vērtību, atlasiet **Saskaņot kontu**, lai iegrāmatotu jūsu veidotās saskaņošanas, transakcijas un labojumus.
    
    Kad saskaņošana ir iegrāmatota, transakcijas, kuras tika iekļautas grāmatošanā, vairs nevarēsmodificēt vai labot, un turpmāk tās vairs netiks rādītas konta saskaņošanas procedūras laikā.

8.  Lai skatītu bankas transakcijas, kas vēl nav saskaņotas, izmantojiet **Nesaskaņoto bankas transakciju** pārskatu. Lai skatītu bankas konta izrakstu, izmantojiet pārskatu **Bankas pārskats**.

## <a name="cancel-bank-statement-reconciliation"></a>Atcelt bankas izrakstu saskaņošanu 

Funkcionalitāte Atcelt bankas izraksta saskaņošanu ļauj atcelt bankas izraksta saskaņošanu. Lai izmantotu šo funkciju, iespējojiet funkciju **Atcelt bankas izraksta saskaņošanu** darbvietā **Funkciju pārvaldība** . Ir arī jāiespējo parametrs **Atļaut bankas izraksta rediģēšanu** . Lai to paveiktu, pārejiet uz **Kases un bankas vadība > Iestatīšana > Kases un bankas vadības parametri > Bankas saskaņošana**.
 
Bankas izrakstu saskaņošanu var atcelt tikai tādā hronoloģiskā secībā, kādā tie ievadīti. Kad bankas izraksta saskaņošana ir atcelta, jaunas transakcijas un labojumi tiks atsaukti, un visas pārējās transakcijas tiks atzīmētas kā nesaskaņotas.
 
Lai atceltu bankas izraksta saskaņošanu, atlasiet bankas izrakstu un atlasiet **Bankas izraksts > Atcelt bankas saskaņošanu**. Lapā **Atcelt bankas saskaņošanu** norādiet **Pamatojuma kodu**, **Pamatojuma komentāru** un **Atcelšanas datumu**. Atlasiet **Labi**, lai sāktu atcelšanu. Ņemiet vērā, ka bankas izraksta atcelšanas datumam jābūt bankas izraksta datumā vai pēc tā. Kad bankas izraksta saskaņošana ir atcelta, bankas izraksta lauks **Atcelšanas datums** tiks atjaunināts ar norādīto **Atcelšanas datumu**. Atlasiet pogu **Transakcijas**, lai skatītu transakcijas, kurām saskaņošana tika atcelta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
