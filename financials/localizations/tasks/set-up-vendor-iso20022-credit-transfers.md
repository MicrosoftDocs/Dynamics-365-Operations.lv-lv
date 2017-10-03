--- 
title: "Kreditoru un kreditoru bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem"
description: "Šajā procedūrā parādīts, kā iestatīt kreditoru un informāciju par kreditora bankas kontu, kas nepieciešama ISO20022 kredīta pārskaitījumam, vai jebkura cita kreditora maksājumu faila izveidošanai."
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
ms.openlocfilehash: 147d8fa82bf15c984ad263cada42789038fa7371
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Kreditoru un kreditoru bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā iestatīt kreditoru un informāciju par kreditora bankas kontu, kas nepieciešama ISO20022 kredīta pārskaitījumam, vai jebkura cita kreditora maksājumu faila izveidošanai. 

Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.
Šī ir trešā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="set-up-bank-details"></a>Bankas informācijas iestatīšana
1. Pārejiet uz sadaļu Kreditori > Kreditori > Visi kreditori.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Kreditora konts, izmantojot vērtību DE-001.
3. Noklikšķiniet uz DE-001, lai apskatītu detalizētu informāciju par kreditoru.
4. Darbību rūtī noklikšķiniet uz Kreditors.
5. Noklikšķiniet uz Banku konti.
6. Noklikšķiniet uz Rediģēt.
    * Ja bankas konts nav pieejams, nepieciešams izveidot jaunu.  
7. Laukā SWIFT kods ierakstiet vērtību COBADEFFXXX.
8. Laukā IBAN ierakstiet DE36200400000628808808.
9. Aizvērt lapu.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Kreditora maksāšanas metodes iestatīšana
1. Noklikšķiniet uz Rediģēt.
2. Izvērsiet vai sakļaujiet sadaļu Maksājums.
3. Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā noklikšķiniet uz saites SEPA CT rindā.
5. Noklikšķiniet uz Saglabāt.


