---
title: Krājumu reģistrēšana pamata noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu
description: Šajā procedūrā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat "pamata noliktavas" iestatījumus krājumu vadības modulī.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1745642dd270e62557b8624cc9daf85d13da044e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982580"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Krājumu reģistrēšana pamata noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat "pamata noliktavas" iestatījumus krājumu vadības modulī. Tas parasti būtu jāveic saņemšanas darbiniekam. Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības.  Ja neizmantojat USMF, tad pirms šī ceļveža uzsākšanas pārliecinieties, ka jums ir apstiprināts pirkšanas pasūtījums ar atvērtu pirkšanas pasūtījuma rindu. Rindas vienībai ir jābūt esošā krājumā. Krājuma vienībai jābūt saistītai ar noliktavas dimensijas grupu, kurā ir aktīva vieta un noliktava.


## <a name="create-item-arrival-journal-header"></a>Krājumu saņemšanas žurnāla virsraksta izveide
1. Dodieties uz Krājumu vadība > Žurnāla ieraksti > Krājumu saņemšana > Krājumu saņemšana.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
    * Ja izmantojat USMF, varat ierakstīt WHS. Ja izmantojat citus datus, izvēlētajam žurnālam ir jābūt šādiem rekvizītiem: Pārbaudīt izdošanas vietu vērtībai ir jābūt Nē un Karantīnas pārraudzība vērtībai ir jābūt Nē.  
4. Ierakstiet vērtību laukā Pavadzīme.
    * Šis ir kreditora izsniegtajā pavadzīmē norādītais pavadzīmes ID. Pievienojiet unikālu numuru.  
5. Atlasiet pirkšanas pasūtījumu laukā Numurs...
6. Noklikšķiniet uz OK.

## <a name="add-lines-to-item-arrival-journal"></a>Rindu pievienošana krājumu saņemšanas žurnālam
1. Noklikšķiniet uz Funkcijas.
2. Noklikšķiniet uz Izveidot rindas.
    * Šajā žurnālā rindas var ievadīt manuāli vai izveidot automātiski. Šajā piemērā tiks parādīts, kā tās izveidot automātiski.  
3. Atzīmējiet izvēles rūtiņu Inicializēt skaitu vai noņemiet tās atzīmi.
    * Šajā piemērā žurnāla rindu skaits tiks inicializēts atbilstoši nereģistrētajam skaitam no pirkšanas pasūtījuma rindas.  
4. Noklikšķiniet uz OK.

## <a name="post-the-journal"></a>Grāmatot žurnālu
1. Noklikšķiniet uz Grāmatot.
2. Noklikšķiniet uz OK.

## <a name="generate-the-product-receipt"></a>Preču ieejas plūsmas ģenerēšana
1. Noklikšķiniet uz Funkcijas.
2. Noklikšķiniet uz Produktu ieejas plūsma.
3. Noklikšķiniet uz OK.

