---
title: Pārdošanas pasūtījuma rēķinu izveidošana
description: Šajā uzdevuma ceļvedī ir aprakstīta pārdošanas pasūtījuma rēķina izrakstīšana, tostarp rēķinu sapludināšana un pakešapstrāde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba8e0f02f2d1eb12cecc2c434fbca1e198cddbe9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842957"
---
# <a name="create-sales-order-invoices"></a>Pārdošanas pasūtījuma rēķinu izveidošana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevuma ceļvedī ir aprakstīta pārdošanas pasūtījuma rēķina izrakstīšana, tostarp rēķinu sapludināšana un pakešapstrāde. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="create-an-invoice-from-a-sales-order"></a>Izveidot rēķinu no pārdošanas pasūtījuma
1. Dodieties uz Debitoru parādi > Pasūtījumi > Nosūtītie pārdošanas pasūtījumi, kas vēl nav iekļauti rēķinā.
2. Sarakstā atlasiet kādu pārdošanas pasūtījumu. 
3. Darbību rūtī noklikšķiniet uz Rēķins.
4. Noklikšķiniet uz Rēķins.
    * Ievērojiet, ka ar šo pārdošanas pasūtījumu ir saistītas vairākas pavadzīmes. Pavadzīmes numura vietā tajā tiek rādīts tikai vārds <multiple>.  
5. Izvērsiet sadaļu Parametri.
    * Lai grāmatotu rēķinu, grāmatošana ir jāiestata uz Jā. Varat arī grāmatošanu izslēgt un rēķinu tikai drukāt. Taču to pašu rezultātu varat panākt, rēķina vietā izveidojot pro forma rēķinu.  
    * Šī opcija tiek izmantota pakešuzdevumiem. Vaicājums tiek izpildīts, kad tiek veikts pakešuzdevums.    
6. Laukā Drukāt atlasiet “Pēc”.
7. Vienumam Drukāt rēķinu atlasiet vērtību Jā.
    * Drukas pārvaldība var drukāt vairākas rēķina kopijas, kā arī nosūtīt rēķinu pa e-pastu kā PDF failu.  
8. Laukā Drukāt maksas atlasiet vērtību “Apkopot”.
9. Laukā Pārbaudīt kredīta limitu atlasiet vienumu “Bilance”.
10. Noklikšķiniet uz Atcelt.

## <a name="combine-orders-into-a-single-invoice"></a>Kombinēt pasūtījumus vienā rēķinā
1. Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.
2. Atrodiet debitoru, kam ir atvērti vairāki rēķini.
3. Atlasiet atvērtu pārdošanas pasūtījumu.
4. Atlasiet citu atvērtu pārdošanas pasūtījumu tam pašam debitoram.
5. Darbību rūtī noklikšķiniet uz Rēķins.
6. Noklikšķiniet uz Rēķins.
7. Izvērsiet sadaļu Parametri.
8. Laukā Daudzums atlasiet vērtību Visi.
    * Ņemiet vērā, ka pārskata sadaļā ir uzskaitīti divi rēķini. Tagad tos abus sapludināsim vienā rēķinā.  
9. Laukā Kopgrāmatojums atlasiet vērtību “Rēķina konts”.
10. Noklikšķiniet uz Sakārtot, lai pārdošanas pasūtījumus sapludinātu vienā rēķinā.
    * Abi pārdošanas pasūtījumi tagad ir sapludināti vienā rēķinā.   
11. Noklikšķiniet uz Atcelt.
12. Noklikšķiniet uz Jā.

## <a name="post-invoices-in-a-batch"></a>Veikt rēķinu pakešveida grāmatošanu
1. Doties uz Debitoru parādi > Rēķini > Partijas rēķinu izrakstīšana > Rēķins.
2. Noklikšķiniet uz Atlasīt.
3. Noklikšķiniet uz OK.
4. Noklikšķiniet uz Partija.
5. Noklikšķiniet uz Jā, lai ieslēgtu pakešapstrādi.
6. Noklikšķiniet uz Periodiskums.
7. Atlasiet vienumu Dienas
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz Atcelt.
11. Noklikšķiniet uz Jā.

