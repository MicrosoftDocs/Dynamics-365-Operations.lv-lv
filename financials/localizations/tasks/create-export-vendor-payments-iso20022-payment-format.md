--- 
title: "Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022"
description: "Šajā procedūrā ir parādīts, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 16c2af862a73047a2e6ebdc056275392fa8a0d93
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot maksājumu rindas kreditora maksājumu žurnālā un ģenerēt kreditora maksājuma failu, izmantojot ISO2022 kredīta pārskaitījuma piemēru. 

Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.

Šī ir piektā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="create-payment-lines"></a>Maksājuma rindu izveide
1. Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.
2. Noklikšķiniet uz Jauns.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
5. Noklikšķiniet uz Rindas.
6. Noklikšķiniet uz Maksājuma priekšlikums.
7. Noklikšķiniet uz Izveidot maksājuma priekšlikumu.
8. Izvērsiet sadaļu Iekļaujamie ieraksti.
9. Noklikšķiniet uz Filtrēt.
10. Sarakstā atlasiet rindu Kreditoru tabulai un Kreditora konta laukam.
11. Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.
    * Varat lietot visus kritērijus, atlasot kreditoru darījumus, kas jāapmaksā, šim piemēram izmantojiet DE-001 kā kreditora kontu.  
12. Noklikšķiniet uz OK.
13. Noklikšķiniet uz OK.
14. Noklikšķiniet uz Izveidot maksājumus.

## <a name="generate-an-iso20022-payment-file"></a>ISO20022 maksājuma faila ģenerēšana


