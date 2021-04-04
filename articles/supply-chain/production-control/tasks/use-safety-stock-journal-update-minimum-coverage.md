---
title: Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo segumu
description: Šajā procedūrā ir parādīts, kā aprēķināt minimālā seguma priekšlikumus, pamatojoties uz vēsturiskām transakcijām, un pēc tam atjaunināt krājumu segumu, izmantojot priekšlikumus.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95dec1dba97923e58cfb603434a01cab6f66a3de
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252802"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo segumu

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā aprēķināt minimālā seguma priekšlikumus, pamatojoties uz vēsturiskām transakcijām, un pēc tam atjaunināt krājumu segumu, izmantojot priekšlikumus. Tas tiek darīts, izmantojot drošības krājumu žurnālu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF. Šis uzdevums ir paredzēts ražošanas plānotājam, lai palīdzētu uzturēt minimālo segumu.


## <a name="create-a-new-safety-stock-journal-name"></a>Izveidot jaunu drošības krājumu žurnāla nosaukumu
1. **Navigācijas rūtī** pārejiet uz **Vispārējā plānošana > Iestatīšana > Drošības krājumu žurnāla nosaukums**.
2. Klikšķiniet **Jauns**.
3. Laukā **Nosaukums** ierakstiet “Materiāls”.
4. Laukā **Apraksts** ierakstiet “Materiāls”.
5. Aizvērt lapu.

## <a name="create-a-safety-stock-journal"></a>Izveidot drošības krājumu žurnālu
1. **Navigācijas rūtī** pārejiet uz **Vispārējā plānošana > Vispārējā plānošana > Palaist > Drošības krājumu aprēķins**.
2. Klikšķiniet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Nosaukums**. Atlasiet drošības krājumu žurnāla nosaukumu, kurus jūs izveidojāt, piemēram, Materiāls.  
4. Noklikšķiniet uz **Izveidot rindas**.
5. Ievadiet datumu laukā **No datuma**.  
6. Ievadiet datumu laukā **Līdz datumam**.
7. Noklikšķiniet uz **Labi**. Šādi tiks izveidotas rindas tām dimensijām, kurām ir krājumu transakcijas.  

## <a name="calculate-proposal"></a>Aprēķināt priekšlikumu
1. Noklikšķiniet uz **Aprēķināt priekšlikumu**.
2. Atlasiet opciju **Izmantot vidējo izejas plūsmu izpildes laikā**.
3. Vienumu **Reizināšanas koeficients iestatiet** uz “10”. Reizināšanas koeficients tiek lietots, lai koriģētu priekšlikumu. Tā kā demonstrācijas datiem tikai dažas transakcijas, jums ir jāiestata šis koeficients, lai iegūtu reālistisku priekšlikumu.  
4. Noklikšķiniet uz **Labi**. Ritiniet uz leju, lai atrastu M0002 un M0003. Skatiet kolonnu **Aprēķinātais minimālais** daudzums.   

## <a name="update-minimum-quantity"></a>Atjaunināt minimālo daudzumu
1. Laukā **Jaunais minimālais daudzums** ievadiet kādu skaitli. Atjauniniet vērtību Jaunais minimālais daudzums, lai tā atbilstu vienuma Aprēķinātais minimālais daudzums vērtībai. Ja Aprēķinātais minimums ir nulle, varat ievadīt vēlamo nākotnes vērtību. Piemēram, šajā laukā varat ievadīt vērtību Aprēķinātais minimālais daudzums tādam M0002, kam ir noliktava 12.  
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Piemēram, varat atlasīt M0002, kam ir noliktava 12.  
3. Laukā **Jaunais minimālais daudzums** ievadiet kādu skaitli. Atjauniniet vērtību Jaunais minimālais daudzums, lai tā atbilstu vienuma Aprēķinātais minimālais daudzums vērtībai. Ja Aprēķinātais minimums ir nulle, varat ievadīt vēlamo nākotnes vērtību.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Grāmatot jauno minimālo daudzumu un validēt rezultātu
1. Noklikšķiniet uz **Grāmatot**.
2. Noklikšķiniet uz **Labi**.
3. Noklikšķiniet, lai sekotu saitei laukā **Krājuma numurs**.
4. Noklikšķiniet, lai sekotu saitei laukā **Krājuma numurs**.
5. **Darbību rūtī** noklikšķiniet uz Plāns.
6. Noklikšķiniet uz **Krājumu vajadzība**. Ņemiet vērā, ka **Minimālais daudzums** ir atjaunināts ar jaunu minimālo daudzumu no drošības krājumu žurnāla.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]