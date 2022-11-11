---
title: Debitora sadalīšana norēķinu grafikiem
description: Šajā rakstā ir aprakstīts, kā sadalīt debitoru, kad tiek izmantoti abonementa rēķini.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746333"
---
# <a name="customer-split-on-billing-schedules"></a>Debitora sadalīšana norēķinu grafikiem

Rēķinu grafikā rēķina konts ir *debitors*, kurš saņem pārdošanas pasūtījuma rēķinu, lai varētu apmaksāt rēķinu. Dažos scenārijos rēķinu var maksāt vairāk nekā viens debitors. Debitora **sadalīšanas funkcionalitāte** ļauj pievienot vairākus debitorus, kuriem var izrakstīt rēķinus par to pašu norēķinu grafiku. Lai iespējotu šo funkcionalitāti, pārejiet uz sadaļu **\>\>\>** **Abonementa norēķini Periodiskie līguma norēķinu iestatījumi periodiskie līguma norēķinu parametri un iestatiet debitora sadalīšanas** opciju uz **Jā.**

## <a name="customer-split-on-the-billing-schedule-header"></a>Debitora sadalīšana norēķinu grafika virsrakstā

Kad ir izveidots norēķinu grafiks, norēķinu grafika galvenei var pievienot papildu debitorus.

Lai pievienotu debitoru, sekojiet šiem soļiem.

1. **Cilnē Norēķinu grafiks** atlasiet Debitora **sadalīšana**. Debitora **konta un** debitora **konta nosaukuma lauki augšējā** līmenī norāda debitoru, kurš ir piešķirts kā Rēķina grafika **debitors**.

    > [!NOTE]
    > Debitora konts, ko pievienojat, nevar būt vienāds ar rēķina kontu.

2. Cilnē Debitora **sadalīšanas** rindas atlasiet **Pievienot rindu**.
3. Atlasiet debitoru un pēc tam ievadiet katra rēķina procentu likmi šim debitoram.
4. Pēc noklusējuma norēķinu grafika sākuma un beigu datumi tiek izmantoti kā sākuma un beigu datumi. Ievadiet dažādus sākuma un beigu datumus, ja jaunais debitors maksās norādīto procentuālo vērtību tikai daļai no norēķinu grafika. Piemēram, ja rēķinu grafika sākuma datums ir 1. janvāris un beigu datums ir 31. decembris, un jaunajam debitoram ir izrakstīts rēķins 40 procenti par pirmajiem deviņiem mēnešiem, kā sākuma datumu norādiet 1. janvāri un kā beigu datumu 30 **. septembri ievadiet 40,00** kā procentus.

Debitora sadalītajām rindām var pievienot vairākus debitorus. Šajā gadījumā ievadītie kopējie procenti nedrīkst pārsniegt 100 procentus. Ievadiet debitora atsauci un debitora pieprasījumu kā informācijas laukus, kas tiks rādīti pārdošanas pasūtījuma rindā rēķina ģenerēšanas **procesa** laikā.

Rindas detaļas rādīs kontaktinformāciju, piegādes adresi, rēķina adresi un pievienoto debitoru maksājuma informāciju. Šī informācija tiks rādīta arī debitoru pārdošanas pasūtījumā.

Kad norēķinu grafika virsrakstam pievienojat debitora sadalītu informāciju, ja norēķinu grafikā ir nenosūtāmas norēķinu grafika rindas, saņemsit šādu ziņojumu, kurā būs redzama uzvedne ar aicinājumu noņemt izmaiņas: "Vai vēlaties noņemt izmaiņas no virsraksta rindās? Izmaiņas atjauninās tikai tās norēķinu grafika rindas, kurām nav izrakstīts rēķins. Atlasiet **Jā**, lai atjauninātu debitora sadalīšanas informāciju norēķinu grafika rindā. Izmaiņas netiks atjauninātas, ja norēķinu grafika rindai jau ir izrakstīts rēķins.

Ja norēķinu grafiks tiek izveidots, izmantojot opciju Kopēt **grafiku**, noklusējuma informācija tiks ievadīta debitora sadalītā virsraksta rindās. Tā nevar būt vienāda ar debitora kontu.

Kad Rēķinu **ģenerēšanas** process ir pabeigts, tiks izveidoti vairāki pārdošanas pasūtījumi. (Ja tiek izmantota automātiskā grāmatošana, tiks izveidoti arī vairāki pārdošanas rēķini.) Šos pārdošanas pasūtījumus un pārdošanas **rēķinus** **var** skatīt cilnes Rēķins kopsavilkuma cilnes Detalizēta informācija par **rindu lapā Skatīt norēķinu** informāciju. **Vairāki** ir parādīti norēķinu informācijas rindā, lai norādītu, ka ir izveidoti vairāki pārdošanas pasūtījumi un pārdošanas rēķini.

## <a name="customer-split-on-billing-schedule-lines"></a>Debitora sadalīšana norēķinu grafika rindās

Debitora sadalījumu var pievienot atsevišķām norēķinu grafika rindām, ja vēlaties sadalīt tikai noteiktas norēķinu grafika rindas. Atzīmējiet **rindas izvēles** rūtiņu Debitora sadalīšana un pēc tam norēķinu grafika rindas izvēlnē atlasiet Debitora sadalīšana, **lai** atjauninātu, vai ievadiet debitora sadalīšanas informāciju.

Audita informācija tiek atjaunināta, ja norēķinu grafikam jau ir izrakstīts rēķins, bet norēķinu grafika rindā tika mainīti procenti. Visas rindas, par kurām pēc šīs izmaiņas tiek izrakstīti rēķini, izmantos jaunos procentus.

> [!NOTE]
> - Debitora sadalīšanas opciju nevar izmantot ar uzkrātām precēm.
> - Ja ir **atzīmēta izvēles rūtiņa** Nenosūtāmie ieņēmumi, **nevar** atzīmēt izvēles rūtiņu Debitora sadalīšana.
> - Ja izmantojat tikai **opciju Ieņēmumu sadalīšana**, pamata rindai ir **opcija** Debitora sadalīšana, bet pakārtotās rindas krājumiem tā nav.
