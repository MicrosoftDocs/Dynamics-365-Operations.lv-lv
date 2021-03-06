---
title: Krājumu līmeņu inicializēšana noliktavā
description: Šajā procedūrā parādīts, kā manuāli atjaunot rīcībā esošo krājumu, izmantojot krājumu kustības žurnālu.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0746b799c701c569f0ae5c657ac3302ab6626287
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823485"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Krājumu līmeņu inicializēšana noliktavā

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā manuāli atjaunot rīcībā esošo krājumu, izmantojot krājumu kustības žurnālu. (Ir iespējams atjaunināt rīcībā esošos krājumus, importējot transakcijas datu elementos.) Šo ceļvedi var palaist demonstrācijas datu uzņēmumā USMF, kur ir pieejami visi nepieciešamie priekšnosacījumi, piemēram, žurnāla nosaukums, krājuma iestatījumi, grāmatošanas metodes un konti. Šajā ceļvedī ir ieteiktas noteiktas vērtības krājumam un izmantotās dimensijas. Ja jūs izvēlēsieties citu krājumu, jums var būt nepieciešams ievadīt vērtības citām dimensijām.

1. Dodieties uz Krājumu vadība > Žurnāla ieraksti > Krājumi > Kustība.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Atlasiet IMov.
    * Dažādiem uzņēmējdarbības nolūkiem ieteicams izmantot atšķirīgas žurnāla nosaukuma veidnes.  
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā Korespondējošais konts norādiet vērtības "140200".
    * Tas ir korespondējošais konts, kas būs noklusējuma korespondējošais konts žurnāla rindās. Ir iespējams ignorēt noklusējumu, piešķirot dažādus korespondējošos kontus katrai rindai.  
7. Noklikšķiniet uz OK.
8. Noklikšķiniet uz Jauns.
9. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
10. Atlasiet krājumu A0001.
11. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
12. Noklikšķiniet uz cilnes Krājumu dimensijas.
13. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
14. Atlasiet vietu 1.
15. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
16. Atlasiet noliktavu 13.
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
19. Atlasiet novietojumu 13.
20. Laukā Daudzums ievadiet skaitli.
21. Noklikšķiniet uz Saglabāt.
22. Noklikšķiniet uz Grāmatot.
23. Atzīmējiet vai notīriet izvēles rūtiņu Visas grāmatošanas kļūdas pārsūtīt uz jaunu žurnālu.
    * Ja iespējosiet šo opciju, jebkuras neiegrāmatotas rindas tiks kopētas uz jaunu žurnālu. Žurnāla informāciju var izmantot, lai labotu problēmas un pēc tam vēlreiz grāmatot rindas.  
24. Noklikšķiniet uz OK.
25. Aizvērt lapu.
26. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]