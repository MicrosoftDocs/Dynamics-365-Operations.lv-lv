--- 
title: "Procentu apstrāde"
description: "Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot procentu paziņojumus."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="process-interest"></a>Procentu apstrāde

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izveidot, izdrukāt un grāmatot procentu paziņojumus. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Iestatiet grāmatošanas metodes procentus.
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes.
2. Noklikšķiniet uz Rediģēt.
    * Nolaižamajā sarakstā atlasiet procentu kodu. Ja nevēlaties veikt procentu aprēķinu transakcijām, izmantojot šo grāmatošanas metodi, atstājiet šo lauku tukšu.  
    * Cilnē Tabulas ierobežojums varat mainīt veidu, kā tiek apstrādāti procenti. Ja šajā laukā ir iestatīts Jā, procenti šai grāmatošanas metodei tiks aprēķināti.  

## <a name="calculate-interest"></a>Aprēķināt procentus
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Procenti > Izveidot procentu paziņojumus.
    * Atlasiet transakciju veidus, kuriem aprēķināsit procentus. Aprēķinā tiks iekļautas visas šiem tipiem atbilstošās atvērtās transakcijas.  
    * Ja atlasāt Procenti, aprēķināsit procentus par procentiem. Pirms šo transakciju pievienošanas, iespējams, vēlēsities pārbaudīt likumus, kas regulē procentu aprēķināšanu procentiem.  
    * Procenti tiks aprēķināti no šī datuma līdz datumam, kas norādīts laukā Datums līdz. Ja jums nav specifiskas vērtības laukā Datums no, tad visi neiegrāmatotie procentu paziņojumi tiks atcelti un procenti tiks pārrēķināti no transakcijas datuma.  
2. Ievadiet procentu paziņojuma datumu.
    * Pieejamas ir trīs grāmatošanas metodes opcijas: Konts — izmantot grāmatošanas metodi, kas ir piešķirta debitora kontam attiecībā uz visiem procentu paziņojumiem.   Atlasīt — lietojiet grāmatošanas profilu, kas ir atlasīts laukā Grāmatošanas metode.   Transakcija — izmantot katram procentu paziņojumam atsevišķu grāmatošanas metodi transakcijām, par kurām tiek aprēķināti procenti. Transakcijām, kurām nav piešķirta grāmatošanas metode, tiek izmantota grāmatošanas metode, kura ir norādīta veidlapas Debitoru parametri apgabalā Virsgrāmata un PVN formā.  
    * Ja mainījāt Izmantot grāmatošanas metodi no lauka vērtību uz Atlasīt, atlasiet šeit grāmatošanas metodi.  
3. Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.
4. Noklikšķiniet uz Filtrēt.
5. Laukā Kritērijs ievadiet klienta ID. Piemēram, ievadiet US-001.
6. Noklikšķiniet uz OK.
7. Noklikšķiniet uz OK.

## <a name="print-interest-notes"></a>Drukāt procentu paziņojumus
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Procenti > Pārskatīt un apstrādāt procentu paziņojumus.
2. Laukā Statuss atlasiet Izveidots.
3. Laukā Drukāts atlasiet Nav drukāts.
4. Klikšķiniet Drukāt.
5. Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.
6. Noklikšķiniet uz OK.
7. Aizvērt lapu.

## <a name="post-the-interest-note"></a>Procentu paziņojuma grāmatošana
1. Atlasiet procentu paziņojumu, kas ir gatavs grāmatošanai (statuss ir Izveidots).
2. Noklikšķiniet uz Grāmatot.
3. Ievadiet procentu paziņojuma grāmatošanas datumu.
    * Lai katram procentu paziņojumam izveidotu Virsgrāmatas transakciju, atlasiet Jā.     Ja neatlasāt vērtību Jā, visi debitora procentu paziņojumu procenti tiek uzkrāti un grāmatoti Virsgrāmatā vienā transakcijā.  
4. Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.
5. Noklikšķiniet uz OK.
6. Laukā Statuss atlasiet Iegrāmatots.


