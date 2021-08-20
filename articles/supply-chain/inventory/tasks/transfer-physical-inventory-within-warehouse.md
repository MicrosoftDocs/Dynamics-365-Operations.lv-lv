---
title: Fizisko krājumu pārsūtīšana noliktavā
description: Šajā procedūrā parādīts krājumu pārsūtīšanas žurnāla izveides un grāmatošanas process, lai reģistrētu krājuma kustību no viena novietojuma noliktavā uz citu novietojumu.
author: MarkusFogelberg
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9557187d0c9f322729bbdd707525e18b54df34cd27aeed09adf4820e3c3d0f3d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754015"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Fizisko krājumu pārsūtīšana noliktavā

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts krājumu pārsūtīšanas žurnāla izveides un grāmatošanas process, lai reģistrētu krājuma kustību no viena novietojuma noliktavā uz citu novietojumu. Pirms procesa sākšanas ir jābūt izveidotam krājumu žurnāla nosaukumam krājumu pārsūtīšanām. Šo procedūru var izmēģināt demonstrācijas datu uzņēmumā USMF, izmantojot parādītās piemēra vērtības vai izmantojot savus datus, ja jums ir izveidoti produkti un novietojumi. Šos uzdevumus parasti veic noliktavas darbinieks.


## <a name="create-an-inventory-transfer-journal"></a>Krājumu pārsūtīšanas žurnāla izveide
1. **Navigācijas rūtī** pārejiet uz **Krājuma pārvaldība > Žurnāla ieraksti > Krājumi > Pārsūtīšana**.
2. Klikšķiniet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Nosaukums**.
4. Noklikšķiniet uz **Labi**. Pastāv opcija norādīt dimensijas No un Uz katrai žurnāla rindai. Tās ir būtiskas šim žurnāla tipam. Krājumus var pārsūtīt uz novietojumiem, izmantojot dažādas kārtulas. Šajā piemērā krājums tiks pārsūtīts tajā pašā noliktavā no novietojuma, kas ir atkarīgs no numura zīmes, uz novietojumu, kas nav atkarīgs no numura zīmes.   

## <a name="create-journal-lines"></a>Izveidot žurnāla rindas
1. Kopsavilkuma rūtī **Žurnāla rindas** noklikšķiniet uz **Jauns**.
2. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat izvēlēties "A0001".  
3. Laukā **No atrašanās vietas** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat izvēlēties "2".  
4. Laukā **Uz atrašanās vietu** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat izvēlēties "2".  
5. Laukā **No noliktavas** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat izvēlēties "24".  
6. Laukā **Uz noliktavu** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat izvēlēties "24".  
7. Laukā **No novietojuma** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat izvēlēties "FL-001".  
8. Laukā **Uz novietojumu** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat izvēlēties "Lielapjoma-001".  
9. Laukā **Daudzums** ierakstiet kādu skaitli.
10. Kopsavilkuma cilnē **Rindas informācija** noklikšķiniet uz cilnes **Krājumu dimensijas**.
11. Laukos **No krājumu dimensijām** un **Numura zīme** ievadiet vai atlasiet vērtību. Ja izmantojat USMF, varat izvēlēties "24".  
12. Noklikšķiniet uz **Saglabāt**.

## <a name="post-the-inventory-transfer-journal"></a>Krājumu pārsūtīšanas žurnāla grāmatošana
1. **Darbību rūtī** noklikšķiniet uz **Publicēt**.
2. Noklikšķiniet uz **Labi**.

## <a name="view-inventory-transactions"></a>Skatiet krājumu darbības
1. Noklikšķiniet uz **Krājumi**.
2. Noklikšķiniet uz **Transakcijas**. Šeit varat redzēt darbības, kas tika izveidotas, grāmatojot žurnālu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]