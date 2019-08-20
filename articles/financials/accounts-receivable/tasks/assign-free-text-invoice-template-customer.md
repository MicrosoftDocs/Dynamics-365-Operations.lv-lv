---
title: Brīva teksta rēķina veidnes piešķiršana debitoram
description: Šajā uzdevumā parādīts, kā debitoram piešķirt brīvā teksta rēķina veidni.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53bff33083a78c0bb1c7d243fe9965fb264d209e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843053"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a>Brīva teksta rēķina veidnes piešķiršana debitoram

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevumā parādīts, kā debitoram piešķirt brīvā teksta rēķina veidni. Šajā uzdevumā izmantots demonstrācijas uzņēmums USMF, un šis uzdevums ir paredzēts lietotājam, kurš ir atbildīgs par debitoru parādu rēķinu pārvaldīšanu un apstrādi.

1. Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Darbību rūtī noklikšķiniet uz Rēķins.
4. Noklikšķiniet uz Periodiskie rēķini.
    * Izmantojiet šo lapu, lai piešķirtu brīva teksta rēķinu veidnes debitoriem un norādītu, cik bieži rēķini tiks nosūtīti debitoram.  
5. Lai debitoram piešķirtu jaunu veidni, noklikšķiniet uz Jauns.
6. Atlasiet brīvā teksta rēķina veidni, kuru vēlaties piešķirt debitoram.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Ievadiet datumu, kad tiks ģenerēts pirmais rēķins.
    * Ievadiet periodiskuma beigu datumu.  
    * Atlasiet kādu no šīm vērtībām: Bez beigu datuma — rēķini tiek ģenerēts uz nenoteiktu laiku, līdz veidne tiek noņemta no debitora konta.  Norēķinu beigu datums — atlasiet šo opciju un ievadiet pēdējo datumu, kad var ģenerēt rēķinu.  
    * Maksimālā kopējā summa, pēc kuras sasniegšanas rēķinu ģenerēšana tiks pārtraukta.  
    * Ievadiet maksimālo kopējo summu, kuru atļauts sasniegt, izmantojot atlasīto veidni. Piemēram, ja ievadāt 1000,00 un ģenerējat ikmēneša rēķinus, katru 100,00 vērtībā, rēķinu ģenerēšana tiks pārtraukta pēc desmitā rēķina izveides.  
    * Ģenerējiet periodiskos rēķinus, izmantojot noklusējuma vērtības no brīvā teksta rēķina veidnes vai debitora konta.  
    * Atlasiet, vai izmantot brīvā teksta rēķina veidni vai debitora kontu, lai noteiktu noklusējuma vērtības valodai, grāmatošanas profilam, PVN grupai, krājumu PVN grupai, saraksta kodam, piegādes valstij/reģionam, valūtai, maksāšanas termiņiem, maksāšanas metodei, maksājuma specifikācijai, maksājumu grafikam, termiņatlaidei, finanšu dimensijām un žiro naudas pārskaitīšanas sarakstam, kad tiek izveidoti rēķini.  
10. Atlasiet atkārtošanās shēmu.
    * Dienas — atlasiet šo opciju un ievadiet dienu skaitu laukā Uz. Piemēram, ja ievadāt 15, tad rēķins šim debitoram tiks ģenerēts ik pēc 15 dienām.  Nedēļas — atlasiet šo opciju un ievadiet nedēļu skaitu laukā Uz. Piemēram, ja ievadāt 2, tad rēķins šim debitoram tiks ģenerēts ik pēc divām nedēļām.  Mēneša — atlasiet šo opciju un ievadiet mēnešu skaitu laukā Uz. Piemēram, ja ievadāt 6, tad rēķins šim debitoram tiks ģenerēts ik pēc sešiem mēnešiem.  Gada — atlasiet šo opciju un ievadiet gadu skaitu laukā Uz. Piemēram, ja ievadāt 2, tad rēķins šim debitoram tiks ģenerēts ik pēc diviem gadiem.  
11. Ievadiet skaitli laukā Uz.

