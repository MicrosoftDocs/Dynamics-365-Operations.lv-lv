---
title: Preces šablona izveide
description: Izveidojiet preces šablonu iepriekš definētiem variantiem.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2290cf8da4387155de7790dd3db88b34eb6e96
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150083"
---
# <a name="create-a-product-master"></a>Preces šablona izveide

[!include [banner](../../includes/banner.md)]

Izveidojiet preces šablonu iepriekš definētiem variantiem. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta preču noformētājam.


## <a name="create-a-new-product-master"></a>Izveidot jaunu preces šablonu
1. Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Preces šabloni**.
2. Klikšķiniet **Jauns**.
3. Laukā **Preces numurs** ierakstiet vērtību. Numuram jābūt unikālam. Laukam **Preces numurs** var iestatīt numuru secību. Šajā gadījumā lietotājam nav jāievada vērtība.
4. Laukā **Preces nosaukums** ierakstiet vērtību. Ievadiet aprakstošo preces nosaukumu. Pēc noklusējuma vērtība ir meklēšanas nosaukums, bet lietotājs var to mainīt.
5. Laukā **Preces dimensijas grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu. Preces dimensiju grupa nosaka, kuru no 4 preču dimensijām var izmantot, lai izveidotu preces variantus. Šajā piemērā tiek izmantota grupa ar krāsu un izmēru.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā. Noklusējuma **Konfigurēšanas tehnoloģija** ir 'Iepriekš definēts variants'. Tas tiks izmantots šajā piemērā.
8. Noklikšķiniet uz **Labi**.

## <a name="select-product-dimension-groups"></a>Preču dimensiju grupu atlasīšana
1. Laukā **Krāsu grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Laukā **Izmēru grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="add-dimension-groups"></a>Pievienot dimensiju grupas
1. **Darbību rūtī** noklikšķiniet uz**Prece**.
2. Noklikšķiniet uz **Dimensiju grupas**, lai atvērtu nolaižamo dialoglodziņu.
3. Laukā **Noliktavas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu. Noliktavas dimensijas palīdz kontrolēt krājumu uzglabāšanu un izņemšanu no krājumiem. Piemēram, noliktavas dimensija var iekļaut vietu un noliktavu.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā **Izsekošanas dimensiju grupa** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu. Izsekošanas dimensiju grupa nosaka izsekošanas dimensijas, kuras var pievienot precei. Piemēram, partijas numuru un sērijas numuru izmanto krājuma vienību izsekošanai.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Noklikšķiniet uz **Labi**.
10. Noklikšķiniet uz **Saglabāt**.
11. Aizvērt lapu.

