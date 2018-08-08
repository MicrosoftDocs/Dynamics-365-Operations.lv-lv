--- 
title: "Preču saņemšanas reģistrēšana pirkšanas pasūtījumā"
description: "Šajā procedūrā ir parādīts, kā reģistrēt preču saņemšanu tieši pirkšanas pasūtījumā."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Preču saņemšanas reģistrēšana pirkšanas pasūtījumā

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā reģistrēt preču saņemšanu tieši pirkšanas pasūtījumā. Produktu ieejas plūsmu var reģistrēt arī noliktavā, un pēc tam to reģistrēt pirkšanas pasūtījumā. Šo uzdevumu parasti izpilda pirkšanas aģents vai kreditoru koordinators. Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF. Piemērā ir iekļautas darbības vienkārša pirkšanas pasūtījuma izveidošanai, lai jūs varētu izspēlēt šo procedūru kā uzdevuma ceļvedi. Ja šo procedūru izmantojāt pats saviem datiem, jums būtu jāsāk ar apakšuzdevumu Reģistrēt preču saņemšanu.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Sagatavot jaunu pirkšanas pasūtījumu preču saņemšanai
1. Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Kreditora konts ievadiet US-101.
4. Noklikšķiniet uz OK.
5. Laukā Krājuma kods ievadiet M0001.
6. Laukā Daudzums ievadiet 5.
7. Darbību rūtī noklikšķiniet uz Pirkt.
8. Noklikšķiniet uz Apstiprināt.

## <a name="record-receipt-of-goods"></a>Preču saņemšanas reģistrēšana
1. Darbību rūtī noklikšķiniet uz Saņemt.
2. Noklikšķiniet uz Produktu ieejas plūsma.
    * Laukā Daudzums varat atlasīt dažādas opcijas tam daudzumam, ko vēlaties saņemt. Piemēram, ja daudzums ir iepriekš reģistrēts noliktavā, varat atlasīt Reģistrētais daudzums.  Šim piemēram lietojiet vērtību Pasūtītais daudzums.   
3. Laukā Produktu ieejas plūsma ierakstiet jebkādu vērtību.
    * Šis lauks tiek lietots, lai ievadītu atsauci, kas tiks izmantota kā dokuments produktu ieejas plūsmas žurnālam.  
4. Izvērsiet sadaļu Rindas.
5. Daudzuma laukā iestatiet vērtību 4.
    * Šeit jūs varat manuāli norādīt daudzumu, kas tiek saņemts katrai pasūtījuma rindai.  
6. Sakļaujiet sadaļu Rindas.
7. Noklikšķiniet uz OK.
    * Tagad preces ir reģistrētas kā saņemtas pirkšanas pasūtījumā, un produktu ieejas plūsmas žurnāls ir izveidots kā dokuments, kas to atspoguļo. Produktu ieejas plūsmas darbību var izmantot, lai pārskatītu ar pirkšanas pasūtījumu izveidotos žurnālus un redzētu, kas un kad tika saņemts.  


