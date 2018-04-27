---
title: "Virsgrāmatas sadalījuma kārtulas"
description: "Šajā rakstā ir sniegta informācija par virsgrāmatas sadalījuma kārtulām. Tajā ir aprakstīti dažādi šo sadalījuma kārtulu un tiem izmantojamo sadalīšanas metožu komponenti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 63562cde3f2813fdcfc9df7ccbfc623aa2fbe9b1
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="ledger-allocation-rules"></a>Virsgrāmatas sadalījuma kārtulas

[!INCLUDE [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par virsgrāmatas sadalījuma kārtulām. Tajā ir aprakstīti dažādi šo sadalījuma kārtulu un tiem izmantojamo sadalīšanas metožu komponenti.

Virsgrāmatas sadalījuma kārtulas izmanto, lai automātiski aprēķinātu un ģenerētu sadalījuma žurnālus un virsgrāmatas bilances vai fiksētu summu sadales kontu ierakstus. Sadalījuma metodes var būt mainīgas vai fiksētas. Virsgrāmatas sadalījuma kārtulām var izmantot šādas sadalījuma metodes.

-   **Pamata** — šī mainīgā metode tiek lietota, ja sadalījums ir atkarīgs no faktiskās virsgrāmatas bilances, pamatojoties uz filtra kritērijiem. Piemēram, var tikt piešķirti reklāmas izdevumi, pamatojoties uz katras nodaļas pārdošanas apjomu proporcionāli kopīgajam nodaļas pārdošanas apjomam.
-   **Fiksēta procentuālā vērtība** un **Fiksēts svars** — šīm metodēm sadalījuma procenti vai svars tiek noteikts tieši šai kārtulai. Piemēram: reklāmas izdevumus var piešķirt tā, lai A nodaļa saņemtu 70 procentus reklāmas izdevumu, bet B nodaļa — 30 procentus.
-   **Vienādi** — šī metode sadala summu vienādās daļās katram definētajam galamērķim. Piemēram: ja A un B nodaļai tiek definēti galamērķi, reklāmas izdevumus var piešķirt tā, lai A un B nodaļa saņem 50 procentus no reklāmas izdevumiem.

Ja sadalījuma kārtulai izmanto sadalījuma metodi Pamata, jādefinē arī atsevišķas virsgrāmatas sadalījuma pamata kārtulas. Darbība “Apstrādāt piešķiršanas pieprasījumu” ļauj lietotājiem apstrādāt virsgrāmatas sadalījuma kārtulu un priekšskatīt rezultātā iegūtos sadalījuma žurnāla ierakstus pirms aprēķināto sadalījumu grāmatošanas vai dzēšanas.

## <a name="components-of-ledger-allocation-rules"></a>Virsgrāmatas sadalījuma kārtulu komponenti
Katrai sadales kārtulai ir četri komponenti: vispārīgais, avota, galamērķa un korespondējošais. Papildu komponents, virsgrāmatas sadalījuma pamatu kārtulas ir nepieciešamas tad, ja pamata metode tiek izmantota kā sadalījuma metode. Katrs komponents nodrošina nozīmīgu informācijas daļu, kas nepieciešama sadalījumu apstrādei.

-   **Vispārīgais** — šis komponents ļauj lietotājam noteikt opcijas, piemēram, sadalījuma metodi, starpuzņēmuma kārtulas iestatījumus un to, vai kārtula ir aktīva.
-   **Avots** — šis komponents ļauj lietotājam noteikt avota datus sadalījumam. Sadalījumu var veidot, pamatojoties uz Virsgrāmatas bilancēm (**Datu avots** = **Virsgrāmata**) vai fiksētām summām (**Datu avots** = **Fiksēta vērtība**). Ja opcija **Datu avots** ir iestatīta uz **Virsgrāmata**, virsgrāmatas sadalījuma kārtulai jānosaka avota filtra kritēriji (piemēram, par reklāmas izdevumiem).
-   **Galamērķis** — šis komponents definē, kā sadales aprēķina rezultāts jāsadala un jāiekļauj norēķinos. Piemēram, katrai nodaļai var būt viena galamērķa rinda.
-   **Korespondējošais konts** — šis komponents definē, kā jānosaka galvenie konti un dimensijas korespondējošiem ierakstiem, kas līdzsvaro galamērķa ierakstus. Lietotāja definētus ierakstus parasti izmanto to kontu un dimensiju vietā, kuru pamatā ir avots. Kad opcija **Datu avots** ir iestatīta uz **Fiksēta vērtība**, opciju **Avots** nevar izmantot kā opciju.
-   **Virsgrāmatas sadalījuma pamata kārtulas** — šīs kārtulas izmanto savus avota filtra kritērijus, lai noteiktu, kuru virsgrāmatas bilanci lietot sadalījumam (piemēram, ieņēmumu departamenta). Katra sadalījuma pamata kārtulu var izmantot ar vairākām sadalījuma kārtulām.





