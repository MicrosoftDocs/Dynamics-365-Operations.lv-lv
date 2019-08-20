---
title: Debitora maksājumu deponējums
description: Debitora maksājumu depozīts.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afbf74d1cf3dc87e97dda0873115b5c7fa49ca3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834467"
---
# <a name="deposit-customer-payments"></a>Debitora maksājumu deponējums

[!include [task guide banner](../../includes/task-guide-banner.md)]

Debitora maksājumu depozīts. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu Debitori > Maksājumi > Maksājumu žurnāls.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Atlasiet maksājuma žurnālu. 
5. Noklikšķiniet uz Rindas.
6. Laukā Konts atlasiet debitoru, kuram vēlaties ierakstīt maksājumu.
7. Ievadiet maksājuma summu laukā Kredīts.
    * Ja vēlaties, varat atstāt summas lauku tukšu, tad sistēma to aprēķinās, atlasot apmaksātos rēķinus.  
8. Ierakstiet vērtību laukā Maksājuma atsauce.
    * Maksājuma atsauce varētu būt ievadāmā maksājuma čeka numurs. Maksājuma atsauce ir nepieciešama, lai iekļautu maksājumu depozīta kvītī.  
9. Atzīmējiet rūtiņu Izmantot depozīta kvīti.
    * Ja maksājums ir jāiekļauj depozītā, nomainiet šo iestatījumu uz Jā.  
10. Noklikšķiniet uz Jauns.
11. Laukā Konts atlasiet debitoru nākamajam maksājumam.
12. Ievadiet maksājuma summu laukā Kredīts.
13. Ierakstiet vērtību laukā Maksājuma atsauce.
14. Atzīmējiet rūtiņu Izmantot depozīta kvīti.
15. Noklikšķiniet uz Grāmatot.
    * Maksājumi ir jāiegrāmato pirms depozīta kvīts izveides. Tas ir nepieciešams, lai nodrošinātu, ka pēc depozīta kvīts izveides maksājumi netiek mainīti.  
16. Noklikšķiniet uz Funkcijas.
17. Noklikšķiniet uz Depozīta kvīts.
18. Noklikšķiniet uz OK.
    * Pirmā lapa tiek izmantota, lai izveidotu depozīta kvīti.  
19. Noklikšķiniet uz OK.
    * Otrais solis ir depozīta kvīts drukāšana, bet šis solis nav obligāts.  

