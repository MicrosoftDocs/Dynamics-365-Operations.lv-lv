---
title: Jauna noliktavas izkārtojuma izveide
description: Šajā rakstā ir aprakstīts, kā iestatīt informāciju par atrašanās vietām noliktavā.
author: yufeihuang
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143648e5317e6dce1b1a76a96d6069abe5d0e351
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859319"
---
# <a name="create-a-new-warehouse-layout"></a>Jauna noliktavas izkārtojuma izveide

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iestatīt informāciju par atrašanās vietām noliktavā. Tā attiecas tikai uz noliktavām, kas izveidotas, izmantojot “pamata noliktavu” krājumu vadības modulī, nevis uz noliktavām, kas izveidotas noliktavas vadības modulī. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


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