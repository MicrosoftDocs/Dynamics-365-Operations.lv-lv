---
title: Materiālu komplekta izveide uz dimensiju balstītas preces šablonam
description: Lai izpildītu šo procedūru, jums ir jāizpilda iepriekšējie 4 ceļveži šajā astoņu ierakstu procedūrā.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0db1c35779a468d9a86d18eb6c849d40bc8c03a3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820086"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Materiālu komplekta izveide uz dimensiju balstītas preces šablonam

[!include [banner](../../includes/banner.md)]

Lai izpildītu šo procedūru, jums ir jāizpilda iepriekšējie 4 ceļveži šajā astoņu ierakstu procedūrā. Ar pirmajiem 4 ierakstiem tiek iestatīti dati, kas ir nepieciešami šīs procedūras izpildīšanai. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šo uzdevumu parasti veic preču noformētājs.


## <a name="select-the-product"></a>Atlasīt preci
1. Noklikšķiniet uz Izlaisto preču uzturēšana.
2. Noklikšķiniet uz Izlaistās preces.
3. Sarakstā atzīmējiet atlasīto rindu.
    * Atrodiet izlaisto preces šablonu ar dimensijām atbilstošas konfigurācijas tehnoloģiju, kuru izveidojāt šīs procedūras pirmajā uzdevumu ceļvedī.  
4. Darbību rūtī noklikšķiniet uz Inženieris.
5. Noklikšķiniet uz MK versijas.

## <a name="create-new-bom-and-bom-version"></a>Izveidot jaunu MK un MK versiju
1. Noklikšķiniet uz Jauns.
2. Noklikšķiniet uz MK un MK versija.
3. Laukā Nosaukums ierakstiet kādu vērtību.
    * Vietas iestatīšana  
    * Šajā procedūrā mēs šim MK neiestatām noteiktu vietu.  
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Jauns.
    * Šajā procedūrā mēs MK pievienosim četras rindas. Divas rindas apzīmē opcijas Cable, un divas rindas apzīmē opcijas Cabinet.  
6. Sarakstā atzīmējiet atlasīto rindu.
7. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Atlasiet krājumu kodu A0001, HDMI 6' Cables.  
8. Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.
    * Atlasiet konfigurācijas grupu Cable, kas tika izveidota šīs procedūras 4. ceļvedī.  
9. Noklikšķiniet uz Jauns.
    * Atlasiet krājumu kodu A0002, HDMI 12' Cables.  
10. Sarakstā atzīmējiet atlasīto rindu.
11. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
12. Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.
    * Vēlreiz atlasiet konfigurācijas grupu Cable.  
13. Noklikšķiniet uz Jauns.
14. Sarakstā atzīmējiet atlasīto rindu.
15. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Atlasiet krājumu kodu D0002 Cable.  
16. Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.
    * Šai MK rindai atlasiet konfigurācijas grupu Cabinet.  
17. Noklikšķiniet uz Jauns.
18. Sarakstā atzīmējiet atlasīto rindu.
19. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Kā pēdējo MK rindu atlasiet krājumu kodu M0007 StandardCabinet.  
20. Laukā Konfigurācijas grupa ievadiet vai atlasiet kādu vērtību.
    * Pēdējai MK rindai atlasiet konfigurācijas grupu Cabinet.  

## <a name="approve-and-activate"></a>Apstiprināt un aktivizēt
1. Aizvērt lapu.
2. Noklikšķiniet uz Apstiprināt.
3. Laukā Apstiprināja ievadiet vai atlasiet kādu vērtību.
4. Laukā Vai vēlaties arī apstiprināt materiālu komplektu? atlasiet Jā.
5. Noklikšķiniet uz OK.
6. Noklikšķiniet uz Aktivizēt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]