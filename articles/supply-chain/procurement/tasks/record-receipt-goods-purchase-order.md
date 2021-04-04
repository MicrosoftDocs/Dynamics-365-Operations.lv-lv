---
title: Preču saņemšanas reģistrēšana pirkšanas pasūtījumā
description: Šajā tēmā ir paskaidrots, kā reģistrēt preču saņemšanu tieši pirkšanas pasūtījumā.
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cdf2b8624bf0319cd421ec11417695cfd4c78db
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244091"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Preču saņemšanas reģistrēšana pirkšanas pasūtījumā

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā reģistrēt preču saņemšanu tieši pirkšanas pasūtījumā. Produktu ieejas plūsmu var reģistrēt arī noliktavā, un pēc tam to reģistrēt pirkšanas pasūtījumā. Šo uzdevumu parasti izpilda pirkšanas aģents vai kreditoru koordinators. Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF. Piemērā ir iekļautas darbības vienkārša pirkšanas pasūtījuma izveidošanai, lai jūs varētu izspēlēt šo procedūru kā uzdevuma ceļvedi. Ja šo procedūru izmantojāt pats saviem datiem, jums būtu jāsāk ar apakšuzdevumu **Reģistrēt preču saņemšanu**.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Sagatavot jaunu pirkšanas pasūtījumu preču saņemšanai
1. Pārejiet uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**.
2. Atlasiet **Jauns**.
3. Laukā **Kreditora konts** ievadiet `US-101`.
4. Atlasiet **Labi**.
5. Laukā **Krājuma kods** ievadiet `M0001`.
6. Laukā **Daudzums** ievadiet `5`.
7. Darbību rūtī atlasiet **Pirkšana**.
8. Atlasiet **Apstiprināt**.

## <a name="record-receipt-of-goods"></a>Preču saņemšanas reģistrēšana
1. Darbību rūtī atlasiet **Saņemt**.
2. Atlasiet **Preču ieejas plūsma**. Laukā **Daudzums** varat atlasīt dažādas opcijas tam daudzumam, ko vēlaties saņemt. Piemēram, ja daudzums ir iepriekš reģistrēts noliktavā, varat atlasīt **Reģistrētais daudzums**. Šim piemēram lietojiet vērtību **Pasūtītais daudzums**.
3. Izvērsiet sadaļu **Pārskats**.
4. Laukā **Preču ieejas plūsma** ierakstiet jebkādu vērtību. Šis lauks tiek lietots, lai ievadītu atsauci, kas tiks izmantota kā dokuments produktu ieejas plūsmas žurnālam.  
5. Izvērsiet sadaļu **Rindas**.
6. Iestatiet **Daudzums** uz '4'. Šeit jūs varat manuāli norādīt daudzumu, kas tiek saņemts katrai pasūtījuma rindai.  
7. Atlasiet **Labi**. Tagad preces ir reģistrētas kā saņemtas pirkšanas pasūtījumā, un produktu ieejas plūsmas žurnāls ir izveidots kā dokuments, kas to atspoguļo. Produktu ieejas plūsmas darbību var izmantot, lai pārskatītu ar pirkšanas pasūtījumu izveidotos žurnālus un redzētu, kas un kad tika saņemts.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]