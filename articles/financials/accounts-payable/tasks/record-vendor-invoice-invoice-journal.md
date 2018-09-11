--- 
title: "Kreditora rēķina reģistrēšana rēķinu žurnālā"
description: "Šajā uzdevuma ceļvedī ir parādīts, kā reģistrēt kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumiem."
author: abruer
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42f93e6d8fcf62babc3e3244bc1fe76d1efd9d13
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Kreditora rēķina reģistrēšana rēķinu žurnālā

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevuma ceļvedī ir parādīts, kā reģistrēt kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumiem. Šī rēķina tipa piemēri ietver izdevumus par piegādēm vai pakalpojumiem.  Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.

1. Pārejiet uz sadaļu Kreditori > Darbvietas > Kreditora rēķina ieraksts.
2. Noklikšķiniet uz Jauns rēķinu žurnāls.
3. Noklikšķiniet uz Jauns.
4. Laukā Nosaukums ievadiet žurnāla nosaukumu vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Apraksta laukā ierakstiet vērtību.
6. Noklikšķiniet uz Rindas.
    * Laukā Datums ievadiet grāmatošanas datumu, kas atjauninās vienumu Virsgrāmata.  
7. Laukā Konts norādiet Kreditora konts.
8. Laukā Rēķins ievadiet rēķina numuru.
9. Laukā Apraksts ierakstiet kādu vērtību.
10. Laukā Kredīts ievadiet kādu skaitli.
11. Laukā Korespondējošais konts ievadiet konta numuru vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * PVN grupa pēc noklusējuma tiek ņemta no kreditora konta datiem.  
    * Krājumu PVN grupa pēc noklusējuma tiek ņemta no galvenā konta, kurš norādīts laukā Korespondējošais konts.  
    * Izpildes datums tiek aprēķināts, ņemot vērā vienumu Apmaksas nosacījumi.  
    * Vērtība Termiņatlaide pēc noklusējuma tiek ņemta no datiem Kreditora konts.  
12. Noklikšķiniet uz Grāmatot.
13. Aizvērt lapu.


