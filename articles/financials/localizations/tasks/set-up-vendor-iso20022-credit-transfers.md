---
title: Kreditoru un kreditoru bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem
description: Šajā procedūrā parādīts, kā iestatīt kreditoru un informāciju par kreditora bankas kontu, kas nepieciešama ISO20022 kredīta pārskaitījumam, vai jebkura cita kreditora maksājumu faila izveidošanai.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c52b9b457505c2cf2bfca46cb938e73c0142e
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848677"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Kreditoru un kreditoru bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

