--- 
title: "Debitora norakstīšanas žurnāla izveide"
description: "Šajā uzdevuma ceļvedī parādīts, kā iestatīt norakstīšanas parametrus un tad norakstīt transakcijas no iekasēšanas lapas, atvērto debitora rēķinu lapas un debitoru lapas."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 19a816f04283ce4f200de7396617313e45e057db
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-write-off-journal-for-a-customer"></a>Debitora norakstīšanas žurnāla izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevuma ceļvedī parādīts, kā iestatīt norakstīšanas parametrus un tad norakstīt transakcijas no iekasēšanas lapas, atvērto debitora rēķinu lapas un debitoru lapas. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.


## <a name="set-up-the-write-off-parameters"></a>Norakstīšanas parametru iestatīšana
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru parametri.
2. Noklikšķiniet uz cilnes Iekasēšana.
3. Izvērsiet vai sakļaujiet sadaļu Norakstīšana.
    * Norakstīšanas žurnāls ir Virsgrāmatas žurnāls, kurā ietvertas visas radītās norakstīšanas transakcijas.  
    * Katrai norakstīšanai varat pievienot iemesla kodu. Šo noklusēto vērtību norakstīšanas laikā varat ignorēt.  
    * Iestatiet vērtību Jā, ja norakstīšanas laikā no sākotnējās transakcijas vēlaties atdalīt PVN.  
4. Aizvērt lapu.
5. Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes.
    * Norakstīšanas konts tiks izmantots par izdevumu kontu vai rezervju korekciju Virsgrāmatas žurnālā   
6. Aizvērt lapu.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Debitora bilances norakstīšana veco bilanču lapā
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Iekasēšana > Vecas bilances.
2. Atzīmējiet tā debitora rindu, kuram vēlaties veikt norakstīšanu. Piemēram, atzīmējiet rindu ar Birch Company uzņēmumu.
3. Darbību rūtī noklikšķiniet uz Iekasēt.
4. Noklikšķiniet uz Norakstīt.
5. Noklikšķiniet uz OK.
6. Aizvērt lapu.
7. Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.
8. Atlasiet žurnālu partijas numuru tam žurnālam, kas satur jūsu norakstāmās transakcijas.
    * Lai atgrieztu debitora bilanci, tiek izveidota viena rinda. Lai norakstīšanu iegrāmatotu norakstīšanas kontā, tiek izveidota viena vai vairākas rindas.  
9. Aizvērt lapu.
10. Aizvērt lapu.

## <a name="write-off-transactions-from-the-collections-form"></a>Norakstiet transakcijas no iekasēšanas veidlapas.
1. Pārejiet uz sadaļu Kredīts un iekasēšana > Iekasēšana > Vecas bilances.
2. Atlasiet tā debitora nosaukumu, kuram atbilst transakcijas, kuras vēlaties norakstīt. Piemēram, atlasiet Cave Wholesales (US-004).
3. Atzīmējiet pirmās transakcijas rindu.
4. Atzīmējiet otrās transakcijas rindu.
5. Noklikšķiniet uz Norakstīt.
6. Laukā Komentārs par iemeslu ierakstiet "Sliktie parādi".
7. Noklikšķiniet uz OK.
8. Aizvērt lapu.
9. Aizvērt lapu.
10. Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.
11. Atlasiet žurnālu partijas numuru tam žurnālam, kas satur jūsu norakstāmās transakcijas.
    * Lai atgrieztu debitora bilanci, tiek izveidota viena rinda. Lai norakstīšanu iegrāmatotu norakstīšanas kontā, tiek izveidota viena vai vairākas rindas.  
12. Aizvērt lapu.
13. Aizvērt lapu.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Rēķina norakstīšana no atvērto debitoru rēķinu lapas
1. Pārejiet uz sadaļu Debitori > Rēķini > Atvērtie debitoru rēķini.
2. Atzīmējiet rēķina rindu. Piemēram, atzīmējiet CIV-000667 rindu.
3. Darbību rūtī noklikšķiniet uz Rēķins.
4. Noklikšķiniet uz Norakstīt.
5. Noklikšķiniet uz OK.
6. Aizvērt lapu.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Debitora bilances norakstīšana debitora lapā
1. Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.
2. Izvēlieties debitora kontu. Piemēram, atlasiet US-001 (Contoso Retail San Diego).
3. Darbību rūtī noklikšķiniet uz Iekasēt.
4. Noklikšķiniet uz Norakstīt.
5. Noklikšķiniet uz OK.
6. Aizvērt lapu.


