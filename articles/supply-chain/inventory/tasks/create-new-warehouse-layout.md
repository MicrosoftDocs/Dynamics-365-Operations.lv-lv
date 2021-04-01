---
title: Jauna noliktavas izkārtojuma izveide
description: Šajā tēmā ir aprakstīts, kā iestatīt informāciju par vietām noliktavā.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2f6f97bc13bc27ec88570992872a256926522c52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218709"
---
# <a name="create-a-new-warehouse-layout"></a>Jauna noliktavas izkārtojuma izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt informāciju par vietām noliktavā. Tā attiecas tikai uz noliktavām, kas izveidotas, izmantojot “pamata noliktavu” krājumu vadības modulī, nevis uz noliktavām, kas izveidotas noliktavas vadības modulī. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-the-default-location-capacity"></a>Iestatīt noklusējuma novietojuma noslodzi
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana > Krājumu un noliktavas pārvaldības parametri**.
2. Atlasiet cilni **Atrašanās vieta**.
3. Laukā **Standarta platums** ievadiet skaitli.
4. Laukā **Standarta dziļums** ievadiet skaitli.
5. Laukā **Standarta augstums** ievadiet skaitli.
6. Atlasiet **Saglabāt**.
7. Aizvērt lapu.

## <a name="define-the-location-name-format"></a>Definēt novietojuma nosaukuma formātu
1. Navigācijas rūtī ejiet uz- **Moduļi > Krājumu pārvaldība > Iestatīšana > Krājumu sadalījums > Noliktavas**.
2. Atlasiet **Jauns**.
3. Laukā **Noliktava** atlasiet vērtību.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Vieta** uzmeklēšanā atlasiet vēlamo ierakstu.
6. Pārslēdziet sadaļas **Atrašanās vietu nosaukumi** izvēršanu. Opcijas šajā sadaļā definē novietojumu nosaukumu noklusējuma formātu. Mūsu piemērā būs ietverts ailes numurs, statīva numurs un plaukta numurs.  
7. Opciju **Iekļaut aili** iestatiet kā **Jā**.
8. Opciju **Iekļaut statīvu** iestatiet kā **Jā**. 
9. Laukam **Formāts** ierakstiet statīvam vērtību.
10. Opciju **Iekļaut plauktu** iestatiet kā **Jā**.
11. Laukam **Formāts** ierakstiet plauktam vērtību.

## <a name="define-warehouse-locations"></a>Definēt noliktavas novietojumus
1. Darbību rūtī atlasiet **Noliktava**.
2. Atlasiet **Atrašanās vietas vednis**.
3. Atlasiet **Nākamais**.
4. Noņemiet atzīmi opcijai **Izejošie doki**
5. Noņemiet atzīmi opcijai **Lielapjoma atrašanās vietas**
6. Atlasiet **Tālāk**, līdz aizejat uz opciju, kur var atlasīt **Pabeigt**.
7. Aizvērt lapu.
8. Atsvaidziniet lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]