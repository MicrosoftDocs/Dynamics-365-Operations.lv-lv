---
title: Uzņēmuma bankas kontu iestatīšana ISO20022 tiešajiem debetiem
description: Šajā uzdevumā parādīts, kā iestatīt informāciju par uzņēmuma bankas kontu, kas nepieciešama debitora maksājumu failu ģenerēšanai.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 290d0eeb383dc3808935809e21b1bf6c99a8550a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552398"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Uzņēmuma bankas kontu iestatīšana ISO20022 tiešajiem debetiem

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevumā parādīts, kā iestatīt informāciju par uzņēmuma bankas kontu, kas nepieciešama debitora maksājumu failu ģenerēšanai. Šī procedūra izmanto ISO 20022 tiešā debeta formātu kā piemēru. Citos formātos, iespējams, ir nepieciešamu papildu iestatījumu informācija, piemēram, uzņēmuma ID un kārtošanas kods.



Šis uzdevums tika izveidots, izmantojot demonstrācijas datu uzņēmumu DEMF.



Šī ir otrā no piecām procedūrām, kas demonstrē debitora maksājuma procesu, izmantojot elektronisko atskaišu konfigurācijas.


## <a name="set-up-the-iban-and-swift-codes"></a>IBAN un SWIFT kodu iestatīšana
1. Pārejiet uz sadaļu Skaidras naudas un banku pārvaldība > Banku konti.
2. Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības DEMF OPER.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Piemēram, noklikšķiniet uz DEMF OPER, lai atvērtu informāciju par bankas kontu.  
4. Noklikšķiniet uz Rediģēt.
5. Izvērsiet vai sakļaujiet sadaļu Papildu identifikācija.
6. Ievadiet vērtību laukā IBAN.
    * Piemēram, ievadiet 'DE89370400440532013000'.  
7. Ierakstiet vērtību laukā SWIFT kods.
    * Piemēram, ievadiet DEUTDEFF.    Lūdzu, ņemiet vērā, ka SWIFT\BIC nav nepieciešami daudziem maksājumu formātiem, tomēr ir ieteicams reģistrēt to bankas kontam.  
8. Noklikšķiniet uz Saglabāt.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Juridiskas personas bankas konta iestatīšana
1. Pārejiet uz sadaļu Organizācijas administrēšana > Organizācijas > Juridiskās personas.
2. Noklikšķiniet uz Rediģēt.
3. Izvērsiet vai sakļaujiet sadaļu Bankas konta informācija.
4. Laukā Bankas konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Piemēram, atlasiet "DEMF OPER" bankas kontu.  
6. Noklikšķiniet uz Saglabāt.

