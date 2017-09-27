--- 
title: "No atribūtiem atkarīgas cenu noteikšanas iestatīšana konfigurējamām precēm"
description: "Šajā procedūrā parādīts kā iestatīt atribūtam atbilstošu cenu noteikšanu."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 473d01ecddfd58aa72a972ee901673534c9d7c9c
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>No atribūtiem atkarīgas cenu noteikšanas iestatīšana konfigurējamām precēm

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts kā iestatīt atribūtam atbilstošu cenu noteikšanu. Kā priekšnosacījumam, jums jābūt preces konfigurācijas modelim, kam ir viens vai vairāki komponenti un atribūti. Šajā piemērā tiek izmantots augstas kvalitātes skaļruņa preces modelis demonstrācijas datu uzņēmumā USMF. Parasti produktu menedžeris izmanto šo procedūru.


## <a name="create-a-new-price-model"></a>Izveidot jaunu cenas modeli
1. Noklikšķiniet uz Preces varianta modeļa definīcija.
2. Noklikšķiniet uz Preču konfigurācijas modeļi.
3. Sarakstā atlasiet augstas kvalitātes skaļruņa rindu, bet nenoklikšķiniet uz nosaukuma saites.
4. Darbību rūtī noklikšķiniet uz Modelis.
5. Noklikšķiniet uz Cenu modeļi.
6. Noklikšķiniet uz Jauns.
7. Laukā Cenas modeļa nosaukums ierakstiet vērtību.
    * Izmantojiet nosaukumu, kas ļauj viegli identificēt modeli.  
8. Apraksta laukā ierakstiet vērtību.
9. Noklikšķiniet uz Saglabāt.

## <a name="add-price-elements"></a>Pievienot cenas elementus
1. Noklikšķiniet uz Rediģēt.
    * Katrs komponents preces modelī var saturēt pamatcenas elementu un jebkādu cenas izteiksmes kārtulu skaitu. Jūs varat arī pievienot cenas dažādās valūtās.  
2. Laukā Pamatcenas izteiksme ievadiet laukā vērtību.
    * Piemēram, ievadiet 100.   Pamatcenas izteiksme var būt skaitliska vērtība, vai tā var sastāvēt no aritmētiska aprēķina, kas ietver vienu vai vairākus atribūtus.  
3. Noklikšķiniet uz Pievienot.
4. Laukā Nosaukums ierakstiet 'Rosewood'.
    * Cenas izteiksmes nosaukums palīdz noteikt, ko atspoguļo cenas elements. Šajā piemērā tiek izveidots cenas elements Rosewood skaļruņa korpusa apdares opcijai.  
5. Noklikšķiniet uz Rediģēt nosacījumu.
    * Cenas nosacījumu palīdz nodrošināt to, ka cenas izteiksmes elements tiek iekļauts pārdošanas cenā tikai tad, ja ir noteiktu atribūtu kombinācija.  
6. Laukā ConstraintBody ievadiet 'CabinetFinish=="Rosewood"'.
7. Noklikšķiniet uz OK.
8. Laukā Izteiksme ierakstiet kādu vērtību.
    * Piemēram, ievadiet 50.  
9. Aizvērt lapu.
10. Aizvērt lapu.

