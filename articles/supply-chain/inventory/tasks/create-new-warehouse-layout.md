---
title: Jauna noliktavas izkārtojuma izveide
description: Šajā procedūrā ir parādīts, kā iestatīt informāciju par novietojumiem noliktavā.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26314f9015feded41f105814b85069fff0c62964
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572769"
---
# <a name="create-a-new-warehouse-layout"></a>Jauna noliktavas izkārtojuma izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā iestatīt informāciju par novietojumiem noliktavā. Tā attiecas tikai uz noliktavām, kas izveidotas, izmantojot “pamata noliktavu” krājumu vadības modulī, nevis uz noliktavām, kas izveidotas noliktavas vadības modulī. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-the-default-location-capacity"></a>Iestatīt noklusējuma novietojuma noslodzi
1. Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Krājumu un noliktavas pārvaldības parametri.
2. Noklikšķiniet uz cilnes Novietojumi.
3. Laukā Standarta platums ievadiet kādu skaitli.
4. Laukā Standarta dziļums ievadiet kādu skaitli.
5. Laukā Standarta augstums ievadiet kādu skaitli.
6. Noklikšķiniet uz Saglabāt.
7. Aizvērt lapu.

## <a name="define-the-location-name-format"></a>Definēt novietojuma nosaukuma formātu
1. Doties uz Krājumu vadība > Iestatījumi > Noliktavu sadalījums > Noliktavas.
2. Noklikšķiniet uz Jauns.
3. Laukā Noliktava ierakstiet kādu vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Pārslēdziet sadaļas Novietojumu nosaukumi izvēršanu.
    * Opcijas šajā sadaļā definē novietojumu nosaukumu noklusējuma formātu. Mūsu piemērā būs ietverts ailes numurs, statīva numurs un plaukta numurs.  
8. Opcijas Iekļaut aili vērtību iestatiet uz Jā.
9. Opcijas Iekļaut statīvu vērtību iestatiet uz Jā. 
10. Statīva laukā Formāts ierakstiet kādu vērtību.
    * Piemēram: -##  
11. Opcijas Iekļaut plauktu vērtību iestatiet uz Jā.
12. Plaukta laukā Formāts ierakstiet kādu vērtību.
    * Piemēram: -##  

## <a name="define-warehouse-locations"></a>Definēt noliktavas novietojumus
1. Darbību rūtī noklikšķiniet uz Noliktava.
2. Noklikšķiniet uz vienuma Novietojumu ceļvedis.
3. Noklikšķiniet uz Tālāk.
4. Noņemiet atzīmi opcijai Nosūtīšanas doki
5. Notīriet atzīmi opcijai Uzkrāšanas vietas
6. Noklikšķiniet uz Tālāk.
7. Noklikšķiniet uz Tālāk.
8. Noklikšķiniet uz Tālāk.
9. Noklikšķiniet uz Tālāk.
10. Noklikšķiniet uz Tālāk.
11. Noklikšķiniet uz Tālāk.
12. Noklikšķiniet uz Tālāk.
    * Ņemiet vērā, ka šajā lapā rādītie fiziskie izmēri ir tie paši, ko iestatāt šīs procedūras sākumā.  
13. Noklikšķiniet uz Tālāk.
14. Noklikšķiniet uz Pabeigt.
15. Aizvērt lapu.
16. Atsvaidziniet lapu.

