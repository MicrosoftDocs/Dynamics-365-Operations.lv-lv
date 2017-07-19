---
title: "Uzkrājumu pārskats"
description: "Šajā rakstā ir aprakstīti uzkrājumi un sniegta informācija par to, kā tos iestatīt un izveidot transakcijas."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5ad5030da963ca961d49e645b1d9ad19453376b8
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="accruals-overview"></a>Uzkrājumu pārskats

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīti uzkrājumi un sniegta informācija par to, kā tos iestatīt un izveidot transakcijas.

Uzkrājumi tiek izmantoti uzkrājumu principa uzskaitē, lai izsekotu ieņēmumus, kas tiek atzīti par iegūtiem noteiktā periodā, nevis tad, kad tiek saņemts maksājums, un izsekotu izdevumus (izmaksas), kas tiek atzītas tad, kad tie rodas, nevis tad, kad tiek veikts maksājums.

## <a name="accrual-schemes"></a>Uzkrāšanas shēmas
Uzkrājumu shēmas tiek izmantotas, lai iestatītu atliktos ieņēmumus un izmaksas, un to pašu uzkrājumu shēmu var izmantot gan ieņēmumiem, gan izdevumiem. Virsgrāmatas uzkrājumi pārdala žurnāla rindas izmaksas vai ieņēmumus tā, lai tos atpazītu atbilstošajos periodos. Lapā **Uzkrājumu shēma** norādiet debeta un kredīta kontu, kas tiks izmantots, lietojot uzkrājumu shēmu.

-   **Debets** — definētais galvenais konts aizstās debeta galveno kontu žurnāla dokumenta rindā. Šis konts tiks izmantots arī atliktā maksājuma anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.
-   **Kredīts** — definētais galvenais konts aizstās kredīta galveno kontu žurnāla dokumenta rindā. Šis konts tiks izmantots arī atliktā maksājuma anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.

Pēc tam, kad definēsiet, kurus kontus izmantot, var norādīt, kā dokumenta numurs tiek izveidots uzkrājumu transakciju izveides laikā. Varat arī norādīt, cik bieži transakcijas notiek, to izveides reižu skaitu un grāmatošanas brīdi. Kad uzkrājumu shēma ir izveidota, to var izmantot dažos no žurnāliem, lieotojot funkciju Virsgrāmatas uzkrājumi.

## <a name="ledger-accruals"></a>Virsgrāmatas uzkrājumi
Atverot žurnālu, izvēlnē **Funkcijas** varat noklikšķināt uz **Virsgrāmatas uzkrājumi**. Atlasot uzkrājumu shēmu, redzēsit pamatsummu no žurnāla, kas tiks sadalīts laika posmā, kā noteikts uzkrājmu shēmā. Piemēram, ja janvārī apmaksājat darbinieka apdrošināšanu par visu gadu, un summa ir 12 000, šie izdevumi ir jāapstiprina katru mēnesi. Varat atlasīt sākuma datumu. Var arī norādīt, vai summa, kas tiek uzkrāta, tiek apstiprināta kontā vai korespondējošajā kontā. Pēc atlases veikšanas noklikšķiniet uz **Transakcijas**, lai skatītu visas transakcijas, kas tika izveidotas atbilstoši uzkrājumu shēmai. Piemēram, ja izdevumus par apdrošināšanu 12 000 apmērā sadalāt uz visu gadu, tad katru mēnesi redzēsiet 1000. Pēc žurnāla grāmatošanas transakcijas varat apskatīt, izmantojot uzziņu lapu **Dokumentu transakcijas**. Ja uzkrājumu shēmu nevar lietot (piemēram, ja ir iesaistīts pārdošanas pasūtījuma rēķins vai pirkšanas pasūtījuma rēķins), varat kreditēt priekšapmaksas summu un debitēt izdevumu summu. Kad tiek lietota uzkrājumu shēma, varat atlasīt **Korespondējošais**.




