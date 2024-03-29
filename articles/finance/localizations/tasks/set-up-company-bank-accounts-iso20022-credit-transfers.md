---
title: Uzņēmuma bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem
description: Šajā procedūrā parādīts, kā iestatīt uzņēmumam specifiskus bankas konta informāciju, kas ir nepieciešama maksājuma faila izveidošanai.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3b3b5ce9d7e24b2b7d3f76e4d770968df897b546df507ba9e3bde5aeac91715
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780774"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Uzņēmuma bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā iestatīt uzņēmumam specifiskus bankas konta informāciju, kas ir nepieciešama maksājuma faila izveidošanai. Iestatiet informāciju, kas nepieciešama, lai izveidotu ISO 20022 kredīta pārskaitījuma formātu, taču atkarībā no formāta var būt nepieciešama cita informācija, piemēram, uzņēmuma ID un kārtošanas kods. 

Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.

Šī ir otrā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="set-up-iban-and-swift-code"></a>IBAN un SWIFT koda iestatīšana
1. Pārejiet uz sadaļu Skaidras naudas un banku pārvaldība > Banku konti.
2. Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības DEMF OPER.
3. Noklikšķiniet uz DEMF OPER, lai apskatītu informāciju par bankas kontu.
4. Noklikšķiniet uz Rediģēt.
5. Izvērsiet sadaļu Papildu identifikācija.
6. Laukā IBAN ierakstiet DE89370400440532013000.
7. Laukā SWIFT kods ierakstiet vērtību DEUTDEFF.
    * Ņemiet vērā, ka SWIFT\BIC nav nepieciešami daudziem maksājumu formātiem, tomēr ir ieteicams reģistrēt to bankas kontam.  
8. Noklikšķiniet uz Saglabāt.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Juridiskas personas bankas konta iestatīšana
1. Pārejiet uz sadaļu Organizācijas administrēšana > Organizācijas > Juridiskās personas.
2. Noklikšķiniet uz Rediģēt.
3. Izvērsiet sadaļu Bankas konta informācija.
4. Ievadiet vai atlasiet vērtību laukā Bankas konts.
5. Noklikšķiniet uz Saglabāt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]