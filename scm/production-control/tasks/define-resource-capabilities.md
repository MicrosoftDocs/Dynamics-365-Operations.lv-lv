--- 
title: "Resursu iespēju definēšana"
description: "Resursu iespējas apraksta, kādas operācijas šie resursi var paveikt."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4a7d342eeb16fd76f2dde58151bfc7973de76e2d
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="define-resource-capabilities"></a>Resursu iespēju definēšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Resursu iespējas apraksta, kādas operācijas šie resursi var paveikt. Plānošanas laikā katra darba un operācijas prasības ir jāsaskaņo ar pieejamo resursu iespējām. Šis uzdevuma ceļvedis jums palīdzēs izveidot resursa iespēju un piešķirt to kādam resursam. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.


## <a name="create-a-resource-capability"></a>Resursa iespējas veidošana
1. Dodieties uz Resursu iespējas.
2. Klikšķiniet Jauns.
3. Laukā Iespēja ierakstiet resursa iespējas ID.
    * Katrai operācijai varat izmantot iespējas ID, lai norādītu, ka resursiem ir nepieciešama šī iespēja, lai varētu izpildīt operāciju.  
4. Laukā Apraksts ievadiet iespējas aprakstu.

## <a name="assign-capability-to-a-resource"></a>Piešķirt iespēju resursam
1. Noklikšķiniet uz Pievienot.
2. Laukā Resurss ierakstiet resursa ID.
    * Resursa iespēju var piešķirt vienam vai vairākiem resursiem.  
3. Laukā Termiņa beigas ievadiet kādu datumu.
    * Šo lauku varat izmantot, lai norādītu, ka resursam iespēja ir tikai ierobežotu laiku.  
4. Laukā Prioritāte ievadiet kādu skaitli.
    * Kad plānojat darbus un operācijas, varat norādīt, vai resursi ir jāatlasa pēc prioritātes. Ja izvēlaties to darīt un līdz pieprasītajam datumam attiecīgo darbu vai operāciju var izpildīt vairāki resursi, tad tiek atlasīts resurss, kuram ir viszemākā prioritāte attiecībā uz nepieciešamo iespēju.  
5. Laukā Līmenis ievadiet kādu skaitli.
    * Ja norādāt, ka darbam vai operācijai ir nepieciešama īpaša iespēja, varat arī norādīt minimālo nepieciešamo līmeni. Izmantojiet iespēju līmeni, lai atšķirtu resursus, kas var izpildīt to pašu darbu, bet ar atšķirīgu ātrumu, jaudu, izmēriem un citiem faktoriem.  


