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
ms.openlocfilehash: 696cb96c6e934eaa44bfe6f51347df4541e5648f75f1ce07139787a1b235d69d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715775"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Materiālu komplekta izveide uz dimensiju balstītas preces šablonam

[!include [banner](../../includes/banner.md)]

Lai izpildītu šo procedūru, jums ir jāizpilda iepriekšējie 4 ceļveži šajā astoņu ierakstu procedūrā. Ar pirmajiem 4 ierakstiem tiek iestatīti dati, kas ir nepieciešami šīs procedūras izpildīšanai. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šo uzdevumu parasti veic preču noformētājs.

## <a name="select-the-product"></a>Atlasīt preci

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Sarakstā atzīmējiet atlasīto rindu.
    * Atrodiet izlaisto preces šablonu ar dimensijām atbilstošas konfigurācijas tehnoloģiju, kuru izveidojāt šīs procedūras pirmajā uzdevumu ceļvedī.  
1. Darbību rūtī atlasiet **Inženieris**.
1. Atlasīt **MK versijas**.

## <a name="create-new-bom-and-bom-version"></a>Izveidot jaunu MK un MK versiju

1. Atlasiet **Jauns**.
1. Atlasiet **MK un MK versiju**.
1. Laukā **Nosaukums** ierakstiet kādu vērtību.
    * Vietas iestatīšana  
    * Šajā procedūrā mēs šim MK neiestatām noteiktu vietu.  
1. Atlasiet **Labi**.
1. Atlasiet **Jauns**.
    * Šajā procedūrā mēs MK pievienosim četras rindas. Divas rindas apzīmē opcijas Cable, un divas rindas apzīmē opcijas Cabinet.  
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
    * Atlasiet krājumu kodu A0001, HDMI 6' Cables.  
1. Laukā **Konfigurācijas grupa** ievadiet vai atlasiet kādu vērtību.
    * Atlasiet kabeļa konfigurācijas grupu, kas tika izveidota šīs procedūras 4. ceļvedī.  
1. Atlasiet **Jauns**.
    * Atlasiet krājumu kodu A0002, HDMI 12' Cables.  
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
1. Laukā **Konfigurācijas grupa** ievadiet vai atlasiet kādu vērtību.
    * Vēlreiz atlasiet kabeļa konfigurācijas grupu.  
1. Atlasiet **Jauns**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
    * Atlasiet krājumu kodu D0002 Cable.  
1. Laukā **Konfigurācijas grupa** ievadiet vai atlasiet kādu vērtību.
    * Šai MK rindai atlasiet kabineta konfigurācijas grupu.  
1. Atlasiet **Jauns**.
1. Sarakstā atzīmējiet atlasīto rindu.
1. Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.
    * Kā pēdējo MK rindu atlasiet krājumu kodu M0007 StandardCabinet.  
1. Laukā **Konfigurācijas grupa** ievadiet vai atlasiet kādu vērtību.
    * Pēdējai MK rindai atlasiet kabineta konfigurācijas grupu.  

## <a name="approve-and-activate"></a>Apstiprināt un aktivizēt

1. Aizvērt lapu.
1. Atlasiet **Apstiprināt**.
1. Laukā **Apstiprināt pēc** ievadiet vai atlasiet kādu vērtību.
1. Laukā **Vai vēlaties arī apstiprināt materiālu komplektu?** atlasiet *Jā*.
1. Atlasiet **Labi**.
1. Atlasiet **Aktivizēt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]