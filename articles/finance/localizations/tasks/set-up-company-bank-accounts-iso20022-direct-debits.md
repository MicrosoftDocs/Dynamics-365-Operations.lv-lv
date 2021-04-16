---
title: Uzņēmuma bankas kontu iestatīšana ISO20022 tiešajiem debetiem
description: Šajā uzdevumā parādīts, kā iestatīt informāciju par uzņēmuma bankas kontu, kas nepieciešama debitora maksājumu failu ģenerēšanai.
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
ms.openlocfilehash: 319bf71982987296a8270f596f8d2bb518dd1790
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819460"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Uzņēmuma bankas kontu iestatīšana ISO20022 tiešajiem debetiem

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]