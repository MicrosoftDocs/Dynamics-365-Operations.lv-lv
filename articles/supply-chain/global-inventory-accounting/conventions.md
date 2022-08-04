---
title: Konvencijas
description: Šajā rakstā ir aprakstīts, kā iestatīt konvencijas, lai noteiktu, kā izmaksas jāskaita globālajā krājumu uzskaitē.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f148d4c6ece543c8a11eee3e6dcdff47b3767936
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135511"
---
# <a name="conventions"></a>Konvencijas

[!include [banner](../includes/banner.md)]

Konvencija ir konteiners politiku kopai, kas ietekmē sistēmas darbību. Pamatojoties uz biznesa prasībām, ir jādefinē konvencijas, izmantojot dažādu politiku kombināciju, kas nosaka, kā izmaksas jāskaita Globālajā krājumu uzskaitē. Jūs varat saistīt katru konvenciju ar vienu vai vairākām Virsgrāmatām, lai nodrošinātu konsekvenci uzskaites politikā, kas tiek piemērota Virsgrāmatā.

Lai iestatītu konvencijas, dodieties uz **Globālā krājumu uzskaite \> Iestatīšana \> Konvencijas**. Katrai konvencijai iestatiet šādus laukus:

- **Nosaukums** — ievadiet konvencijas nosaukumu.
- **Apraksts** — ievadiet konvencijas aprakstu.
- **Izmaksu objekta politika** – atlasiet izmaksu objekta politiku. Šīs politikas nosaka precizitātes līmeni, ko sistēma izmanto, lai aprēķinātu un uzturētu krājumu vērtību. Pieejamas šādas iepriekš definētas opcijas:

    - Produkts
    - Prece – Vieta
    - Prece – Vieta — Noliktava

    Piemēram, atlasot *Prece – Vieta*, katrai krājumu kustībai (ieplūdei vai aizplūdei), sistēma aprēķina un uztur katras preces krājumu izmaksas vietas līmenī. Tādēļ krājumu kustības zemākos līmeņos, piemēram, noliktavas līmenī, neietekmē krājumu vērtību. (Noliktavas līmeņa pārsūtīšanas piemērs ir krājumu pārsūtīšana starp divām noliktavām vienā vietā.) Tāpat nevar skatīt krājumu izmaksas zemākā līmenī, piemēram, noliktavas līmenī.

- **Ievades mērījumu pamata politika** – atlasiet ievades mērījumu pamata politiku. Šīs politikas nosaka izmaksas, kas jāplūst krājumu kontā, un izmaksas, kas jāmaksā. Tirdzniecības uzņēmumiem ir svarīgas šādas opcijas:

    - **Parasts vēsturisks** – visas izmaksu sastāvdaļas ieplūst krājumu kontā.
    - **Standarta** – standarta izmaksas ieplūst krājumu kontos, un atšķirības starp piemērotajām izmaksām un faktiskajām izmaksām tiek ieskaitītas dispersijas kontos. Ja vēlaties izveidot *Standarta* ievades mērījumu pamata politiku, vispirms jāizveido cenu saraksts, kur politika var atrast krājuma standarta izmaksas.
    - **Cenu saraksti** - Globālā krājumu uzskaite atbalsta krājumu cenu nākšanu no vairākām juridiskām personām. Var definēt cenu sarakstu, ko izmantos ievades mērījumu bāzes politika. Šādā veidā sistēma zinās, kur meklēt krājuma cenu. Lai iestatītu cenrāžus, rīkojieties šādi:

        1. Laukā **Nosaukums** ievadiet nosaukumu.
        1. Ievadiet aprakstu laukā **Apraksts**.
        1. Laukā **Izmaksu aprēķināšanas veids** atlasiet izmaksu aprēķināšanas veidu (*Standarta izmaksas* vai *Plānotās izmaksas*).
        1. Laukā **Cenas veids** atlasiet cenas veidu (*Izmaksas*, *Pirkšana* vai *Pārdošanas cena*).
        1. Pievienot izmaksu aprēķināšanas versiju.
        1. Darbību rūtī atlasiet **Cena**, lai validētu krājuma cenas cenu sarakstā.

- **Izmaksu plūsmas pieņēmuma politika** – izvēlieties izmaksu plūsmas pieņēmuma politiku. Šīs politikas nosaka to, kā izmaksas tiek noņemtas no krājuma un ziņotas kā pārdoto preču pašizmaksa. Pieejamas šādas iepriekš definētas opcijas:

    - Vidēji
    - Specifisks — Partija

    > [!NOTE]
    > Globālā krājumu uzskaite ir beztermiņa krājumu sistēma. Tādēļ sistēma izseko krājuma vērtību katrai transakcijai atsevišķi.

- **Izmaksu elementu politika** – var definēt izmaksu elementu politikas un saistīt tās ar šo lauku. Šis *Izmaksu elements* ir notikuma patērētā resursa izmaksas. Izmaksu elementus var izmantot, lai izsekotu un kategorizētu izmaksas. Lai izveidotu izmaksu elementu politiku, ievadiet informāciju šādās vietās:

    - **Nosaukums** lauks
    - **Apraksts** lauks
    - **Izmaksu elements** saraksts
    - **Noteikumi** režģis

    Ja nevēlaties tālāk sadalīt krājumu vērtību, ir jāizveido izmaksu elementu saraksts, kurā ir viens izmaksu elements. Pēc tam ir jāizveido izmaksu elementu politika, lai kartētu visus atbilstošos mērījumu tipus (izmaksu sastāvdaļas) uz šo izmaksu elementu.
