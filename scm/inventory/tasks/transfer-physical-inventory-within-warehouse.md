--- 
title: "Fizisko krājumu pārsūtīšana noliktavā"
description: "Šajā procedūrā parādīts krājumu pārsūtīšanas žurnāla izveides un grāmatošanas process, lai reģistrētu krājuma kustību no viena novietojuma noliktavā uz citu novietojumu."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedb209ab111ed1fb6281fda2f4dea345e0905ef
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Fizisko krājumu pārsūtīšana noliktavā

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts krājumu pārsūtīšanas žurnāla izveides un grāmatošanas process, lai reģistrētu krājuma kustību no viena novietojuma noliktavā uz citu novietojumu. Pirms procesa sākšanas ir jābūt izveidotam krājumu žurnāla nosaukumam krājumu pārsūtīšanām. Šo procedūru var izmēģināt demonstrācijas datu uzņēmumā USMF, izmantojot parādītās piemēra vērtības vai izmantojot savus datus, ja jums ir izveidoti produkti un novietojumi. Šos uzdevumus parasti veic noliktavas darbinieks.


## <a name="create-an-inventory-transfer-journal"></a>Krājumu pārsūtīšanas žurnāla izveide
1. Dodieties uz sadaļu Pārsūtīšana.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
4. Noklikšķiniet uz OK.
    * Pastāv opcija norādīt dimensijas No un Uz katrai žurnāla rindai. Tās ir būtiskas šim žurnāla tipam. Krājumus var pārsūtīt uz novietojumiem, izmantojot dažādas kārtulas. Šajā piemērā krājums tiks pārsūtīts tajā pašā noliktavā no novietojuma, kas ir atkarīgs no numura zīmes, uz novietojumu, kas nav atkarīgs no numura zīmes.   

## <a name="create-journal-lines"></a>Žurnāla rindu izveide
1. Noklikšķiniet uz Jauns.
2. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat izvēlēties "A0001".  
3. Laukā No atrašanās vietas ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat izvēlēties "2".  
4. Laukā Uz atrašanās vietu ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat izvēlēties "2".  
5. Laukā No noliktavas ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat izvēlēties "24".  
6. Laukā Uz noliktavu ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat izvēlēties "24".  
7. Laukā No novietojuma ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat izvēlēties "FL-001".  
8. Laukā Uz novietojumu ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat izvēlēties "Lielapjoma-001".  
9. Laukā Daudzums ievadiet skaitli.
10. Noklikšķiniet uz cilnes Krājumu dimensijas.
11. Laukā Numura zīme ievadiet vai atlasiet kādu vērtību.
    * Ja izmantojat USMF, varat izvēlēties "24".  
12. Noklikšķiniet uz Saglabāt.

## <a name="post-the-inventory-transfer-journal"></a>Krājumu pārsūtīšanas žurnāla grāmatošana
1. Noklikšķiniet uz Grāmatot.
2. Noklikšķiniet uz OK.

## <a name="view-inventory-transactions"></a>Skatiet krājumu darbības
1. Noklikšķiniet uz Krājumi.
2. Noklikšķiniet uz Transakcijas.
    * Šeit varat redzēt darbības, kas tika izveidotas, grāmatojot žurnālu.  

