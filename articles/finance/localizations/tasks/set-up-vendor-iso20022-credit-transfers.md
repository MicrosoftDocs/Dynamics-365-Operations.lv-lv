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
ms.openlocfilehash: 4809a352f87cc3d88429461a06dfe36189ed5f31
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138973"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Kreditoru un kreditoru bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem

[!include [banner](../../includes/banner.md)]

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

