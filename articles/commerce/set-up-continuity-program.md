---
title: Nepārtrauktības programmu iestatīšana zvanu centram
description: Šajā rakstā ir aprakstīts, kā zvanu centrā iestatīt nepārtrauktības programmu.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 39c3e6d740bff2af27a2fba2ac4c406c01b43a87218fdc1dcfe094c147cd3de3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716154"
---
# <a name="set-up-continuity-programs-for-call-centers"></a>Nepārtrauktības programmu iestatīšana zvanu centram

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā zvanu centrā iestatīt nepārtrauktības programmu.

Nepārtrauktības programmā, kas ir pazīstama arī kā periodisku pasūtījumu programma, klienti saņem regulārus preču sūtījumus saskaņā ar iepriekš noteiktu grafiku. Katrā sūtījumā var būt atšķirīgas preces, kā tas ir ar klubu, kas katru mēnesi saņem jaunu grāmatu, vai arī vienu preci var sūtīt atkārtoti. Lai iestatītu nepārtrauktības programmu, ir jāizpilda tālāk minētie uzdevumi.

1. Iestatiet nepārtrauktības parametrus lapā **Zvanu centra parametri**.
2. Izveidojiet nepārtrauktības programmu, kas norāda detalizētu informāciju, piemēram, maksājumu grafiku, sūtījumu laiku un vai maksājums tiek veikts uzreiz. Jums jāpievieno arī to preču saraksts, kas ir iekļautas nepārtrauktības programmā. Katra prece saņem notikuma ID numuru, kas tiek piešķirts secīgi, sākot ar 1. Notikuma ID nosaka secību, kādā preces tiek nosūtītas.

    - Ja katrā sūtījumā debitori saņem atšķirīgu preci, tās tiek nosūtītas secīgi saskaņā ar to notikuma ID, sākot no pašreizējā notikuma.
    - Ja debitori katrā sūtījumā saņem vienu un to pašu preci, sarakstā ir tikai viena prece, kam ir viens notikuma ID. Viens un tas pats notikums notiek atkārtoti. Varat norādīt, cik reizes atkārtot katru notikumu.

3. Izveidojiet pamata preci, kas apzīmē nepārtrauktības programmu, kuru izveidojāt 2. uzdevuma izpildes laikā. Ja šo preci pievienojat pārdošanas pasūtījumam, tiek atvērta lapa **Nepārtrauktība**. Pēc tam šo lapu varat izmantot, lai izveidotu faktisko nepārtrauktības pasūtījumu. Pamata prece nenorāda atsevišķas preces, ko debitors saņem katrā sūtījumā.

Kad esat iestatījis nepārtrauktības programmu, kā aprakstīts iepriekš, varat debitoram izveidot nepārtrauktības pasūtījumu. Iespējams, būs jāizpilda arī tālāk minētie papildu uzturēšanas uzdevumi.

- **Pašreizējā notikuma perioda nepārtrauktības atjaunināšana** — iestatiet pakešuzdevumu, kas sistēmai paziņo, kāds ir pašreizējais notikuma periods.
- **Izveidot nepārtrauktos apakšpasūtījumus** — izveidojiet apakšpasūtījumus no pamata nepārtrauktības pasūtījuma.
- **Nepārtrauktības maksājumu apstrāde** — apstrādājiet to maksājumu norēķinus un paziņojumus, kas ir saistīti ar nepārtrauktības pārdošanas pasūtījumiem.
- **Nepārtrauktības rindu paplašināšana** (ja nepieciešams) — palieliniet reižu skaitu, cik nepārtrauktības notikumu var atkārtot. Sūtījumu atkārtošana var pārsniegt ierobežojumus, kas ir iestatīti zvanu centra parametru laukā **Nepārtrauktības atkārtošanas robežvērtība**.
- **Nepārtrauktības atjauninājuma veikšana** (ja nepieciešams) — sinhronizējiet izmaiņas starp nepārtrauktības programmu un nepārtrauktība pamata pārdošanas pasūtījumiem.
- **Galveno nepārtrauktības rindu un pasūtījumu aizvēršana** — aizveriet nepārtrauktības pasūtījumus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]