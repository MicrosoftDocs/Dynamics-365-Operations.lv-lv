---
title: Maksāšanas metodes
description: Kad sistēma tiek iestatīta, ir jākonfigurē katrs maksājuma tips, kuru mazumtirgotājs pieņem. Šajā rakstā ir aprakstīti maksājumu tipi, kurus varat iestatīt, un aprakstīts to iestatīšanas process.
author: rubencdelgado
ms.date: 06/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 414b49d1099575f1626c29e8f3b07f522e3ab370
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804507"
---
# <a name="payment-methods"></a>Maksāšanas metodes

[!include [banner](includes/banner.md)]

Kad sistēma tiek iestatīta, ir jākonfigurē katrs maksājuma tips, kuru mazumtirgotājs pieņem. Šajā rakstā ir aprakstīti maksājumu tipi, kurus varat iestatīt, un aprakstīts to iestatīšanas process.

Mazumtirgotāji var pieņemt dažāda veida maksājumus apmaiņā pret pārdotajām precēm un pakalpojumiem. Kaut gan skaidra nauda ir visizplatītākais maksājumu veids, mazumtirgotāji var arī saņemt maksājumus čeku, karšu vai dokumentu u.c. formā. Sistēmas iestatīšanas laikā programmā Dynamics 365 Commerce ir jākonfigurē katrs maksājuma veids, ko pieņem mazumtirgotājs. Tālāk esošajā sarakstā ir aprakstīts katrs maksājuma veids, ko var iestatīt.

- **Skaidra nauda** – nauda fiziskā valūtas formā, piemēram, banknotes un monētas. Šī valūta var būt uzņēmuma valūta vai veikala vietējā valūta.
- **Čeks** – maksāšanas līdzeklis noteiktas summas maksājuma noteiktā valūtā izrakstīšanai noteiktā bankā. Čeks parasti ir derīgs nenoteiktu laiku vai sešus mēnešus pēc izsniegšanas datuma, ja vien nav norādīts cits derīguma periods. Šis periods atšķiras atkarībā no bankas, kurā ir izrakstīts čeks. Ir pieejami dažādi čeku veidi, piemēram, pasūtījuma čeki, skaitītāja čeki, uzrādītāja čeki un saņēmēja čeki. Varat iestatīt čekus kā maksājuma metodi katram veikalam. Čekus var pieņemt valūtā, kas ir noteikta uzņēmuma līmenī vai veikala līmenī. Jums ir jāiestata čekus kā maksājuma metodi, pirms jūs varat pieņemt čeku kā maksājumu veikalā.
- **Valūta** – galvenais maksāšanas līdzeklis papildus uzņēmuma noklusējuma valūtai. Valūta ietver gan monētas, gan banknotes. Valūtas maksājuma metode atspoguļo visas valūtas, kas tiek izmantotas. Lai varētu izmantot šo norēķinu veidu, ir jāiestata valūtas un ir jānorāda to maiņas kurss.
- **Karte** – visa veida kartes, kas tiek izmantotas, piemēram, debetkartes un kredītkartes. Ir ieteicams iestatīt vienu kartes maksājuma metodi uzņēmuma līmenī, lai pārstāvētu visa veida kartes. Katrā veikalā varat iestatīt maksājuma metodi katrai kartei vai karšu kopai, kas ir jāapstrādā, izmantojot vienādus iestatījumus. Nepieciešams iestatīt apritē pieejamās ražotāju kartes, piemēram, debetkartes un kredītkartes, pirms jūs varat pieņemt tās veikalā kā maksājuma veidu.
- **Kredītrēķins** – kredītrēķini, kas ir izsniegti vai izpirkti pārdošanas punktā. Kredītrēķins var kredīta vai atgriešanas kredīta rēķins, kas tiek izsniegts atgriešanas pārdošanas brīdī. Ja kredītrēķini tiek izpirkti tikai daļēji, programma automātiski izsniedz jaunu kredītrēķinu par jauno bilances summu. Jaunajam kredītrēķinam ir jauns numurs. Kredītrēķinu var izmantot tikai vienu reizi, un sistēmā tiek veikta visu izmantoto numuru uzskaite. Ierakstu, var skatīt lapā **Kredītrēķina tabula**. Debitors nevar izpirkt summu, kas pārsniedz kredītrēķina vērtību.
- **Dāvanu karte** – attiecas uz dāvanu kartēm, kas izsniegtas un izpirktas pārdošanas punktā. Dāvanu kartēm nav atļauta pārmaksa. Visām dāvanu kartēm ir jābūt karšu numuru kartējumiem. 
- **Debitora konts** – sniedz iespēju pārdošanas laikā atskaitīt maksājuma summu no debitora konta, izmantojot kases sistēmu. Šo maksājuma metodi var izmantot arī, lai apkopotu pārdošanas informāciju vai debitora individuālās atlaides, kad debitors veic maksājumu, izmantojot citu maksājuma metodi. Šajā gadījumā ir jāiestata debitoram raksturīgā informācija.
- **Lojalitātes programmas punkti** – punkti, ko debitori saņem lojalitātes programmu ietvaros. Ja izveidojat lojalitātes programmas, debitori var saņemt punktus un pēc tam izpirkt tos dažādos veidos. Piemēram, dažās lojalitātes programmās debitori var izpirkt lojalitātes programmas punktus atlaide formā vai pat izmantot tos kā maksājuma veidu.

Lai iestatītu maksāšanas metodes, ir jāizpilda tālāk aprakstītie uzdevumi.

1. Iestatīt organizācijas maksājumu metodes. Izveidot maksājuma metodes, kas tiek pieņemtas visā organizācijā.
2. Izveidojiet uzņēmuma līmeņa karšu veidus un karšu numurus. Ja tiek pieņemtas kredītkartes vai debetkartes, ir jāizveido viena maksājumu metode maksājumiem ar kartēm un pēc tam ir jāizveido organizācijas līmeņa karšu veidi un karšu numuri.
3. Iestatiet veikala maksājuma metodes. Saistiet maksājuma metodes ar katru veikalu un pēc tam ievadiet veikalam raksturīgos maksājuma metodes iestatījumus.
4. Iestatiet veikalu kartes maksājuma metodes. Veiciet kartes iestatījumus visām kartes maksājuma metodēm, kas tiek pieņemtas veikalā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]