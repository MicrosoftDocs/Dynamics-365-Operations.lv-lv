---
title: Kreditora rēķina reģistrēšana rēķinu žurnālā
description: Šajā uzdevuma ceļvedī ir parādīts, kā reģistrēt kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumiem.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140379"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Kreditora rēķina reģistrēšana rēķinu žurnālā

[!include [banner](../../includes/banner.md)]

Šajā uzdevuma ceļvedī ir parādīts, kā reģistrēt kreditoru rēķinus, kas nav saistīti ar pirkšanas pasūtījumiem. Šī rēķina tipa piemēri ietver izdevumus par piegādēm vai pakalpojumiem.  Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.

1. Pārejiet uz **Navigācijas rūts > Moduļi > Kreditori > Darbvietas > Kreditora rēķina ieraksts**.
2. Sadaļā **Darbību rūts** noklikšķiniet uz **Jauns rēķinu žurnāls**.
3. Klikšķiniet **Jauns**.
4. Laukā **Nosaukums** ievadiet žurnāla nosaukumu vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Laukā **Apraksts** ierakstiet kādu vērtību.
6. **Darbību rūtī** noklikšķiniet uz **Rindas**. Laukā **Datums** ievadiet grāmatošanas datumu, kas atjauninās vienumu Virsgrāmata.  
7. Laukā **Konts** norādiet **Kreditora konts**.
8. Laukā **Rēķins** ievadiet rēķina numuru
9. Laukā **Apraksts** ierakstiet kādu vērtību.
10. Laukā **Kredīts** ievadiet kādu skaitli.
11. Laukā **Korespondējošais konts** ievadiet konta numuru vai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * **PVN grupa** pēc noklusējuma tiek ņemta no kreditora konta datiem.  
    * **Krājumu PVN grupa** pēc noklusējuma tiek ņemta no galvenā konta, kurš norādīts laukā **Korespondējošais konts**.  
    * **Izpildes datums** tiek aprēķināts, ņemot vērā vienumu Apmaksas nosacījumi.  
    * Vērtība **Termiņatlaide** pēc noklusējuma tiek ņemta no datiem Kreditora konts.  
12. Noklikšķiniet uz **Grāmatot**.
13. Aizvērt lapu.

