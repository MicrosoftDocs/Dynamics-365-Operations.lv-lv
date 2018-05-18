--- 
title: "Atgādinājuma vēstuļu apstrāde"
description: "Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>Atgādinājuma vēstuļu apstrāde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot atgādinājuma vēstules. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Atgādinājuma vēstuļu secības iestatīšana grāmatošanas metodē
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes.
2. Noklikšķiniet uz Rediģēt.
    * Atlasiet no nolaižamā saraksta atgādinājuma vēstuļu secību. Ja atgādinājuma vēstules nevēlaties ģenerēt darbībām, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu.  
    * Tabulas ierobežojumu cilnē varat mainīt veidu, kā tiek apstrādātas atgādinājuma vēstules. Ja šajā laukā ir iestatīts Jā, atgādinājuma vēstules tiks izveidotas šai grāmatošanas metodei.  
3. Aizvērt lapu.

## <a name="create-collection-letters"></a>Izveidot atgādinājuma vēstules
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Atgādinājuma vēstule > Izveidot atgādinājuma vēstules.
    * Atlasiet darbību veidus, kam apkoposit vēstules. Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.  
2. Laukā Atgādinājuma vēstule, atlasiet opciju.
3. Ievadiet atgādinājuma vēstules datumu.
    * Pieejamas ir divas grāmatošanas metodes opcijas: Konts — izmantot grāmatošanas metodi, kas ir piešķirta debitora kontam attiecībā uz visiem procentu paziņojumiem.   Atlasīt — lietojiet grāmatošanas profilu, kas ir atlasīts laukā Grāmatošanas metode.  
    * Atlasiet grāmatošanas metodi, ja mainījāt “Izmantojiet grāmatošanas metodi no” uz “Atlasīt”.  
4. Izvērsiet sadaļu Iekļaujamie ieraksti.
5. Noklikšķiniet uz Filtrēt.
6. Laukā Kritēriji ievadiet Debitora ID. Piemēram, ievadiet US-001.
7. Noklikšķiniet uz OK.
8. Noklikšķiniet uz OK.

## <a name="print-collection-letters"></a>Atgādinājuma vēstuļu izdruka
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Atgādinājuma vēstule > Pārskatīt un apstrādāt atgādinājuma vēstules.
2. Laukā Statuss atlasiet Izveidots.
3. Laukā Drukāts atlasiet Nav drukāts.
4. Klikšķiniet Drukāt.
5. Noklikšķiniet uz atgādinājuma vēstules piezīmes.
6. Izvērsiet sadaļu Iekļaujamie ieraksti.
7. Grāmatošanas robeždatuma ievadīšana
8. Noklikšķiniet uz Labi, lai drukātu atgādinājuma vēstuli.

## <a name="post-the-collection-letter"></a>Atgādinājuma vēstules grāmatošana
1. Noklikšķiniet uz Grāmatot.
2. Ievadiet atgādinājuma vēstules grāmatošanas datumu.
3. Izvērsiet sadaļu Iekļaujamie ieraksti.
4. Noklikšķiniet uz OK.
5. Laukā Statuss atlasiet Iegrāmatots.
6. Laukā Drukāts atlasiet opciju.


