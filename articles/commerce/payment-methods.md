---
title: Maksāšanas metodes
description: Kad sistēma tiek iestatīta, ir jākonfigurē katrs maksājuma tips, kuru mazumtirgotājs pieņem. Šajā rakstā ir aprakstīti maksājumu tipi, kurus varat iestatīt, un aprakstīts to iestatīšanas process.
author: BrianShook
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: d16cdf237042471d367adb7081bf34e9c8a9460f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272827"
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

## <a name="handle-change-tendering-for-payment-methods"></a>Apstrādāt norēķinu izmaiņas maksāšanas metodēm

Dažas maksāšanas metodes neatbalsta tiešo izmaiņu norēķinus, ja pārdošanas punkta transakciju laikā līdzekļi ir atgriežami debitoriem. Norēķinu maiņai **var** **izmantot** tikai skaidras naudas un valūtas maksājuma metodes. 

Lai apstrādātu gadījumus, kad darbības laikā ir nepieciešama norēķinu maiņa, bet maksājuma metode to neatbalsta, **varat definēt maksājumu maiņas** metodi. Kad veikalam iestatāt veikala maksāšanas metodes, atlasiet maksāšanas metodi, kuru vēlaties izmantot. Pēc tam sadaļas **Mainīt** laukā **Mainīt norēķinus** ievadiet norēķinu maiņas maksājuma opciju. Piemēram, varat ievadīt 1, **lai** norādītu, ka skaidra nauda var tikt izmantota kā norēķinu maiņas maksāšanas opcija.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
