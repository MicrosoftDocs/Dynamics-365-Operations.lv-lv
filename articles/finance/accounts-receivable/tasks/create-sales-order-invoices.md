---
title: Pārdošanas pasūtījumu rēķinu izveide
description: Šajā tēmā ir aprakstīta pārdošanas pasūtījuma rēķina izrakstīšana, tostarp rēķinu sapludināšana un pakešapstrāde.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6712779ca64f5934edd37730597541679b86e43
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394614"
---
# <a name="create-sales-order-invoices"></a>Pārdošanas pasūtījumu rēķinu izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīta pārdošanas pasūtījuma rēķina izrakstīšana, tostarp rēķinu sapludināšana un pakešapstrāde. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="create-an-invoice-from-a-sales-order"></a>Izveidot rēķinu no pārdošanas pasūtījuma
1. Dodieties uz **Navigācijas rūts > Moduļi > Debitoru parādi > Pasūtījumi > Nosūtītie pārdošanas pasūtījumi, kas vēl nav iekļauti rēķinā**.
2. Sarakstā atlasiet kādu pārdošanas pasūtījumu. 
3. **Darbību rūtī** noklikšķiniet uz **Rēķins > Ģenerēt > Rēķins**. Ievērojiet, ka ar šo pārdošanas pasūtījumu ir saistītas vairākas pavadzīmes. Pavadzīmes numura vietā tajā tiek rādīts tikai vārds *vairāki*.  
4. Izvērsiet sadaļu **Parametri**.
    - Lai grāmatotu rēķinu, grāmatošana ir jāiestata uz Jā. Varat arī grāmatošanu izslēgt un rēķinu tikai drukāt. Taču to pašu rezultātu varat panākt, rēķina vietā izveidojot pro forma rēķinu.  
    - Šī opcija tiek izmantota pakešuzdevumiem. Vaicājums tiek izpildīts, kad tiek veikts pakešuzdevums.
5. Laukā **Drukāt** atlasiet “Pēc”.
6. Vienumam **Drukāt rēķinu** atlasiet vērtību **Drukāt rēķinu**. Drukas pārvaldība var drukāt vairākas rēķina kopijas, kā arī nosūtīt rēķinu pa e-pastu kā PDF failu.  
7. Laukā **Drukāt maksas** atlasiet vērtību “Apkopot”.
8. Laukā **Pārbaudīt kredīta limitu** atlasiet vienumu “Bilance”.
9. Noklikšķiniet uz **Atcelt**.

## <a name="combine-orders-into-a-single-invoice"></a>Kombinēt pasūtījumus vienā rēķinā
1. Dodieties uz **Navigācijas rūts > Moduļi > Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Atrodiet debitoru, kam ir atvērti vairāki rēķini.
3. Atlasiet vairākus atvērtos pārdošanas pasūtījumus no tā paša debitora.
4. **Darbību rūtī** noklikšķiniet uz **Rēķins > Ģenerēt > Rēķins**.
5. Izvērsiet sadaļu **Parametri**.
6. Laukā **Daudzums** atlasiet vērtību “Visi”. Ņemiet vērā, ka pārskata sadaļā ir uzskaitīti divi rēķini. Tagad tos abus sapludināsim vienā rēķinā.  
7. Laukā **Kopgrāmatojums** atlasiet vērtību “Rēķina konts”.
8. Noklikšķiniet uz **Sakārtot**, lai pārdošanas pasūtījumus sapludinātu vienā rēķinā. Abi pārdošanas pasūtījumi tagad ir sapludināti vienā rēķinā.   
9. Noklikšķiniet uz **Atcelt**.
10. Noklikšķiniet uz pogas **Jā**.

## <a name="post-invoices-in-a-batch"></a>Veikt rēķinu pakešveida grāmatošanu
1. Dodieties uz **Navigācijas rūts > Moduļi > Debitori > Rēķini > Partijas rēķinu izrakstīšana > Rēķins**.
2. Noklikšķiniet uz **Atlasīt**.
3. Noklikšķiniet uz **Labi**.
4. Noklikšķiniet uz **Partija**.
5. Vienumam **Pakešapstrāde** atlasiet **Jā**.
6. Noklikšķiniet uz **Periodiskums**.
7. Atlasiet vienumu **Dienas**.
8. Noklikšķiniet uz **Labi**.
9. Noklikšķiniet uz **Labi**.
10. Noklikšķiniet uz **Atcelt**.
11. Noklikšķiniet uz pogas **Jā**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
