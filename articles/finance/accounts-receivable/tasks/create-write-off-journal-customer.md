---
title: Debitora norakstīšanas žurnāla izveide
description: Šajā uzdevuma ceļvedī parādīts, kā iestatīt norakstīšanas parametrus un tad norakstīt transakcijas no iekasēšanas lapas, atvērto debitora rēķinu lapas un debitoru lapas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6526e57cf2ed84161eb7a92c031127bb6c6536a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003308"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Debitora norakstīšanas žurnāla izveide

[!include [banner](../../includes/banner.md)]

Šajā uzdevuma ceļvedī parādīts, kā iestatīt norakstīšanas parametrus un tad norakstīt transakcijas no iekasēšanas lapas, atvērto debitora rēķinu lapas un debitoru lapas. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.


## <a name="set-up-the-write-off-parameters"></a>Norakstīšanas parametru iestatīšana
1. Ejiet uz **Navigācijas rūti > Moduļi > Kredīts un atgūšana > Iestatīšana > Kreditoru parametri.**
2. Noklikšķiniet uz cilnes **Atgūšana**.
3. Izvērsiet vai sakļaujiet sadaļu **Norakstīšana**.
    - **Norakstīšanas žurnāls** ir vispārīgais žurnāls, kas satur jūsu izveidotos norakstīšanas darījumus.  
    - Katrai norakstīšanai varat pievienot iemesla kodu. Šo noklusēto vērtību norakstīšanas laikā varat ignorēt.  
    - Iestatiet **Atsevišķs pārdošanas nodoklis** kā „Jā”, ja vēlaties nošķirt pārdošanas nodokli no sākotnējā darījuma norakstīšanā.  
4. Aizvērt lapu.
5. Pārejiet uz sadaļu **Kredīts un iekasēšana > Iestatījumi > Debitoru grāmatošanas metodes**. Norakstīšanas konts tiks izmantots kā izdevumu konts vai rezerves regulēšana vispārējā žurnālā.
6. Aizvērt lapu.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Debitora bilances norakstīšana veco bilanču lapā
1. Pārejiet uz sadaļu **Kredīts un iekasēšana > Iekasēšana > Vecas bilances**.
2. Atzīmējiet tā debitora rindu, kuram vēlaties veikt norakstīšanu. Piemēram, atzīmējiet rindu ar Birch Company uzņēmumu.
3. **Darbību rūtī** noklikšķiniet uz **Ievākt**.
4. Noklikšķiniet uz **Norakstīt**.
5. Noklikšķiniet uz **Labi**.
6. Aizvērt lapu.
7. Ejiet uz **Navigācijas rūts > Moduļi > Virsgrāmata > Žurnāla ieraksti > Vispārējie žurnāli**.
8. Atlasiet žurnālu partijas numuru tam žurnālam, kas satur jūsu norakstāmās transakcijas. Lai atgrieztu debitora bilanci, tiek izveidota viena rinda. Lai norakstīšanu iegrāmatotu norakstīšanas kontā, tiek izveidota viena vai vairākas rindas.  
9. Aizvērt lapu.
10. Aizvērt lapu.

## <a name="write-off-transactions-from-the-collections-form"></a>Norakstiet transakcijas no iekasēšanas veidlapas.
1. Pārejiet uz sadaļu **Kredīts un iekasēšana > Iekasēšana > Vecas bilances**.
2. Atlasiet tā debitora nosaukumu, kuram atbilst transakcijas, kuras vēlaties norakstīt. Piemēram, atlasiet Cave Wholesales (US-004).
3. Atzīmējiet pirmās transakcijas rindu.
4. Atzīmējiet otrās transakcijas rindu.
5. Noklikšķiniet uz **Norakstīt**.
6. Ievadiet laukā **Iemesla komentārs** „Sliktie parādi”.
7. Noklikšķiniet uz **Labi**.
8. Aizvērt lapu.
9. Aizvērt lapu.
10. Ejiet uz **Virsgrāmata > Žurnāla ieraksti > Vispārējie žurnāli**.
11. Atlasiet žurnālu partijas numuru tam žurnālam, kas satur jūsu norakstāmās transakcijas. Lai atgrieztu debitora bilanci, tiek izveidota viena rinda. Lai norakstīšanu iegrāmatotu norakstīšanas kontā, tiek izveidota viena vai vairākas rindas.  
12. Aizvērt lapu.
13. Aizvērt lapu.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Rēķina norakstīšana no atvērto debitoru rēķinu lapas
1. Ejiet uz **Navigācijas rūts > Moduļi > Debitori > Rēķini > Atvērtie klientu rēķini**.
2. Atzīmējiet rēķina rindu. Piemēram, atzīmējiet CIV-000667 rindu.
3. **Darbību rūtī** noklikšķiniet uz **Rēķins**.
4. Noklikšķiniet uz **Norakstīt**.
5. Noklikšķiniet uz **Labi**.
6. Aizvērt lapu.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Debitora bilances norakstīšana debitora lapā
1. Ejiet uz sadaļu **Debitori > Klienti > Visi klienti**.
2. Izvēlieties debitora kontu. Piemēram, atlasiet US-001 (Contoso Retail San Diego).
3. **Darbību rūtī** noklikšķiniet uz **Ievākt**.
4. Noklikšķiniet uz **Norakstīt**.
5. Noklikšķiniet uz **Labi**.
6. Aizvērt lapu.

