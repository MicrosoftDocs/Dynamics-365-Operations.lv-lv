---
title: Debitora maksājumu deponējums
description: Debitora maksājumu depozīts.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9221101581a6a130889b7c941ca228070a000c56
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003160"
---
# <a name="deposit-customer-payments"></a>Debitora maksājumu deponējums

[!include [banner](../../includes/banner.md)]

Debitora maksājumu depozīts. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Debitori > Maksājumi > Maksājumu žurnāls**.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums** nolaižamajā izvēlnē atlasiet **CustPay**.
4. Atlasiet **Rindas**.
5. Laukā **Uzņēmums** atlasiet klientu, par kuru ierakstāt maksājumu.
6. Laukā **Kredīts** ievadiet maksājuma summu. Ja vēlaties, varat atstāt summas lauku tukšu, tad sistēma to aprēķinās, atlasot apmaksātos rēķinus.  
7. Ievadiet vērtību laukā **Maksājuma atsauce**. Maksājuma atsauce varētu būt ievadāmā maksājuma čeka numurs. Maksājuma atsauce ir nepieciešama, lai iekļautu maksājumu depozīta kvītī.  
8. Atzīmējiet rūtiņu Izmantot depozīta kvīti. Ja maksājums ir jāiekļauj depozītā, nomainiet šo iestatījumu uz Jā.  
9. Atlasiet **Jauns**.
10. Laukā **Uzņēmums** atlasiet klientu nākamajam maksājumam.
11. Laukā **Kredīts** ievadiet maksājuma summu.
12. Ievadiet vērtību laukā **Maksājuma atsauce**.
13. Atzīmējiet rūtiņu **Izmantot depozīta kvīti**.
14. Atlasiet **Grāmatot**. Maksājumi ir jāiegrāmato pirms depozīta kvīts izveides. Tas ir nepieciešams, lai nodrošinātu, ka pēc depozīta kvīts izveides maksājumi netiek mainīti.  
15. Atlasiet **Funkcijas**.
16. Atlasiet **Depozīta kvīts**.
17. Atlasiet **Labi**. Pirmā lapa tiek izmantota, lai izveidotu depozīta kvīti.  
18. Atlasiet **Labi**. Otrais solis ir depozīta kvīts drukāšana, bet šis solis nav obligāts.  

