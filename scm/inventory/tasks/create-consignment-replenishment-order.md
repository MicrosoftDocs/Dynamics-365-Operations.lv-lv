--- 
title: "Sūtījuma papildināšanas pasūtījuma izveide"
description: "Šajā procedūrā parādīts kā izveidot jaunu sūtījuma papildināšanas pasūtījumu, lai jūs varētu izsekot paredzēto piegādi no kreditora jūsu sūtījumu krājumā."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 5e268f640be11b0905457ff6b7697c90411f53e5
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-consignment-replenishment-order"></a>Sūtījuma papildināšanas pasūtījuma izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts kā izveidot jaunu sūtījuma papildināšanas pasūtījumu, lai jūs varētu izsekot paredzēto piegādi no kreditora jūsu sūtījumu krājumā. Tajā ir arī parādīts kā reģistrēt preču saņemšanu, lai sūtījumu krājums ir reģistrēts kā rīcībā esošos krājums, kas pieder kreditoram. Šo procedūru parasti veic sagādes speciālists. Šo ceļvedi var izmantot demonstrācijas datu uzņēmumā USMF. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.




## <a name="create-a-consignment-replenishment-order"></a>Sūtījuma papildināšanas pasūtījuma izveide
1. Dodieties uz Sagāde un avoti > Sūtījums > Sūtījuma papildināšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Kreditora konts atlasiet kreditoru US-104.
    * Nepieciešams atlasīt kreditoru, kas ir reģistrēts kā īpašnieks lapā Krājumu īpašnieki.  
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Pievienot rindu.
6. Laukā Krājuma kods ierakstiet M9211CI.
    * Atlasiet vienumu, kas ir iestatīts sūtījuma krājumam.  
7. Laukā Daudzums ievadiet skaitli.
8. Laukā Pieprasītais piegādes datums ievadiet datumu.
    * Pieprasītos un apstiprinātos datumus izmanto MRP programma preču saņemšanas paredzēšanai.  
9. Laukā Apstiprinātais piegādes datums ievadiet datumu.
10. Izvērsiet sadaļu Detalizēta informācija par rindu.
11. Noklikšķiniet uz cilnes Krājumu dimensijas.
12. Atsvaidziniet lapu, lai parādītu īpašnieku laukā Krājuma dimensijas īpašnieks.
    * Kreditors US-104 tagad ir norādīts kā īpašnieks.  

## <a name="check-the-inventory-transaction-status"></a>Pārbaudiet krājumu darbības statusu
1. Noklikšķiniet uz Krājumi.
2. Noklikšķiniet uz Transakcijas.
3. Sarakstā atzīmējiet atlasīto rindu.
    * Ievērojiet, ka saņemšanas lauks ir iestatīts uz Pasūtīts.  
4. Aizvērt lapu.

## <a name="receive-items"></a>Saņemt krājumus
1. Noklikšķiniet uz Produktu ieejas plūsma.
2. Laukā Ārējā produktu ieejas plūsma ierakstiet kādu vērtību.
3. Laukā Daudzums ievadiet skaitli, kas ir mazāks par skaitli, kas ir norādīts šeit. 
4. Noklikšķiniet uz OK.

## <a name="check-the-on-hand-inventory"></a>Pārbaudiet rīcībā esošo krājumu
1. Noklikšķiniet uz Krājumi.
2. Noklikšķiniet uz Rīcībā esošie krājumi.
3. Noklikšķiniet uz Pārskats.
    * Krājumus, kas tika saņemti kā sūtījumu krājumi, kas pieder kreditoram, ir pieejami rīcībā esoši. Sūtījuma papildināšanas pasūtījuma Atlikušais daudzums tiek parādīts laukā Pasūtīts kopā.  
4. Aizvērt lapu.
5. Noklikšķiniet uz Aizvērt.


