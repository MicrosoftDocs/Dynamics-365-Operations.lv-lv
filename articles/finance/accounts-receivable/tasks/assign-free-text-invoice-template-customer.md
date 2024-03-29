---
title: Brīva teksta rēķina veidnes piešķiršana debitoram
description: Šajā uzdevumā parādīts, kā debitoram piešķirt brīvā teksta rēķina veidni.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49074c11659ae30fd2decdb93b4721441edff2c5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780262"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Brīva teksta rēķina veidnes piešķiršana debitoram

[!include [banner](../../includes/banner.md)]

Šajā uzdevumā parādīts, kā debitoram piešķirt brīvā teksta rēķina veidni. Šajā uzdevumā izmantots demonstrācijas uzņēmums USMF, un šis uzdevums ir paredzēts lietotājam, kurš ir atbildīgs par debitoru parādu rēķinu pārvaldīšanu un apstrādi.

1. **Navigācijas rūtī** ejiet uz sadaļu **Moduļi > Debitori > Klienti > Visi klienti**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. **Darbību rūtī** noklikšķiniet uz **Rēķins**.
4. Klikšķiniet uz **Periodiskie rēķini**. Izmantojiet šo lapu, lai piešķirtu brīva teksta rēķinu veidnes debitoriem un norādītu, cik bieži rēķini tiks nosūtīti debitoram.  
5. Lai klientam piešķirtu jaunu veidni, noklikšķiniet uz **Jauna**.
6. Laukā **Veidne** atlasiet brīva teksta rēķina veidni, ko vēlaties piešķirt klientam.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Laukā **Rēķinu izrakstīšanas sākuma datums** ievadiet datumu, kad tiks izveidots pirmais rēķins.
10. Sadaļā **Periodiskuma beigas** ievadiet perioda beigu datumu.  
    Atlasiet vienu no norādītajiem saraksta elementiem: 
    - **Nav beigu datuma** – rēķini tiks ģenerēti uz nenoteiktu laiku, līdz veidne tiks noņemta no klienta konta.
    - **Norēķinu beigu datums** — atlasiet šo opciju un ievadiet pēdējo datumu, kad rēķinu var ģenerēt.  
11. Laukā **Maksimālā uzkrātā summa** ievadiet maksimālo uzkrāto summu, pēc kuras beigsies rēķinu veidošana. Ievadiet maksimālo kopējo summu, kuru atļauts sasniegt, izmantojot atlasīto veidni. Piemēram, ja ievadāt 1000,00 un ģenerējat ikmēneša rēķinus, katru 100,00 vērtībā, rēķinu ģenerēšana tiks pārtraukta pēc desmitā rēķina izveides.  
12. Sadaļā **Veidot periodiskus rēķinus, izmantojot noklusējuma vērtības no** izvēlieties brīva teksta ievades veidni vai klienta kontu. Atlasiet, vai izmantot brīvā teksta rēķina veidni vai debitora kontu, lai noteiktu noklusējuma vērtības valodai, grāmatošanas profilam, PVN grupai, krājumu PVN grupai, saraksta kodam, piegādes valstij/reģionam, valūtai, maksāšanas termiņiem, maksāšanas metodei, maksājuma specifikācijai, maksājumu grafikam, termiņatlaidei, finanšu dimensijām un žiro naudas pārskaitīšanas sarakstam, kad tiek izveidoti rēķini.  
13. Laukā **Atkārtošanās shēma** atlasiet atkārtošanās shēmu.
    - **Katru dienu — atlasiet šo opciju un laukā Per ievadiet dienu** skaitu. Piemēram, ja ievadāt 15, tad rēķins šim debitoram tiks ģenerēts ik pēc 15 dienām.
    - **Katru nedēļu — atlasiet šo opciju un laukā Per ievadiet nedēļu** skaitu. Piemēram, ja ievadāt 2, tad rēķins šim debitoram tiks ģenerēts ik pēc divām nedēļām.
    - **Monthly** — atlasiet šo opciju un laukā Per ievadiet mēnešu skaitu. Piemēram, ja ievadāt 6, tad rēķins šim debitoram tiks ģenerēts ik pēc sešiem mēnešiem.
    - **Gads** — atlasiet šo opciju un laukā Per ievadiet gadu skaitu. Piemēram, ja ievadāt 2, tad rēķins šim debitoram tiks ģenerēts ik pēc diviem gadiem.  
14. Laukā **Par** ievadiet skaitli.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
