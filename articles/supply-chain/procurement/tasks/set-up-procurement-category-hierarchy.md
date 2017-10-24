--- 
title: "Sagādes kategoriju hierarhijas iestatīšana"
description: "Šajā procedūrā parādīts, kā izveidot jaunus zarus sagādes kategoriju hierarhijā un kā konfigurēt sagādes kategoriju izmantošanai sagādes procesā."
author: mkirknel
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9897b1184e8159b20a45d4cedbba56baef31a3c
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a>Sagādes kategoriju hierarhijas iestatīšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā izveidot jaunus zarus sagādes kategoriju hierarhijā un kā konfigurēt sagādes kategoriju izmantošanai sagādes procesā. Šos uzdevumus parasti veic pirkšanas vadītājs. Pirms var sākt šo procedūru, ir jābūt Sagādes tipa kategoriju hierarhijai. Ja izmantojat demonstrācijas datu uzņēmumu, šo procedūru varat veikt USMF uzņēmumā.


## <a name="add-a-new-procurement-category"></a>Jaunas sagādes kategorijas pievienošana
1. Pārejiet uz sadaļu Sagāde un avoti > .. > Sagādes kategorijas.
2. Noklikšķiniet uz Rediģēt kategoriju hierarhiju.
    * Pašreizējā sagādes kategoriju hierarhija tiek parādīta lapas kreisajā pusē. Jūs gatavojaties modificēt hierarhiju.  
3. Noklikšķiniet uz Jauns kategorijas zars.
    * Sistēma atlasa augšējo zaru pēc noklusējuma. Ja veicāt šo procedūru kā uzdevumu ceļvedi, varat noklikšķināt uz pogas Atbloķēt un atlasīt citu pamatzaru, kura jāievieto jūsu jaunais zars. Kad tas tiks izdarīts, atkal bloķējiet uzdevumu ceļvedi un pēc tam noklikšķiniet uz Jauns kategorijas zars.  
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Apraksta laukā ierakstiet vērtību.
6. Laukā Draudzīgais nosaukums ierakstiet vērtību.
    * Draudzīgais nosaukums nav obligāts. Tas tiks parādīts kategorijas uzmeklēšanās kopā ar kategorijas nosaukumu.  
7. Noklikšķiniet uz Saglabāt.

## <a name="add-products-to-your-new-procurement-category"></a>Preču pievienošana jaunajai sagādes kategorijai
1. Pārejiet uz sadaļu Sagāde un avoti > .. > Sagādes kategorijas.
    * Atlasiet zaru, ko tikko pievienojāt. Ja veicāt šo procedūru kā uzdevuma ceļvedi, lai atlasītu zaru, iespējams, būs jāatbloķē šis uzdevuma ceļvedis.  
2. Pārslēdziet sadaļas Preces paplašinājumu.
3. Noklikšķiniet uz Pievienot, lai saistītu preces ar sagādes kategoriju.
4. Atlasiet preci, ko vēlaties pievienot sagādes kategorijai.
5. Noklikšķiniet uz bultiņas, lai atlasītu preci.
6. Atlasiet citu preci, ko vēlaties pievienot sagādes kategorijai.
7. Noklikšķiniet uz bultiņas, lai atlasītu preci.
8. Noklikšķiniet uz OK.

## <a name="add-approved-and-preferred-vendors"></a>Apstiprināto vai vēlamo kreditoru pievienošana
1. Pārslēdziet sadaļas Kreditori paplašinājumu.
2. Noklikšķiniet uz Pievienot.
    * Var pievienot kreditoru sagādes kategorijai un norādīt, vai kreditors ir vēlams vai apstiprināts šai kategorijai. Dzēšot kreditoru no kategorijas, vēsturiskās transakcijas ar kreditoru kategorijā netiek dzēstas.   
3. Atrodiet kreditoru, ko vēlaties pievienot kategorijai.
4. Noklikšķiniet uz bultiņas, lai atlasītu kreditoru.
5. Noklikšķiniet uz Labi.
6. Izvēlieties kreditora rindu, ko vēlaties modificēt.
7. Laukā Kreditora statuss atlasiet kādu opciju.
    * Kreditora izvēles iestatījums Kategorijas ierobežojuma nosacījumos reglamentē, vai pirkšanas pieprasījumos pieejami vēlamie, apstiprinātie vai visi kreditori.   

## <a name="add-additional-information-to-the-category"></a>Papildinformācijas pievienošana kategorijai
1. Pārslēdziet sadaļas Kreditoru vērtēšanas kritēriju grupas sadaļas paplašinājumu.
    * Šī cilne ļauj definēt, pēc kuriem kritērijiem jāvērtē kreditori sagādes kategorijā. Lai to izdarītu, jānoklikšķina uz Pievienot un pēc tam jāatlasa kreditoru novērtēšanas grupa, kas satur vēlamos kritērijus.  
2. Pārslēdziet sadaļas Anketas paplašinājumu.
    * Šī cilne ļauj jums pievienot anketas, kas parādīsies uz pieprasījumā, ja Aktivitātes tips ir iestatīts uz "Pieprasījums". Pēc tam pieprasītājam jāaizpilda anketa pirms pieprasījuma iesniegšanas par noteiktu preci vai precēm sagādes kategorijā.  
3. Pārslēdziet sadaļas Krājumu PVN grupas paplašinājumu.
4. Laukā Krājumu PVN grupa: noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Atlasiet PVN grupu.
6. Pārslēdziet sadaļas Kategorijas lapa paplašinājumu.
    * Kategorijas lapas tiek izveidotas lapā Kategoriju hierarhija. Tās satur informāciju par sagādes kategoriju, piemēram, informāciju par preču tipu kategorijā, preču attēliem kategorijā un paziņojumiem, piemēram, atlaidēm, kas ir pieejamas kategorijā. Kategorijas lapas informācija tiek parādīta pirkšanas pieprasījumos.  
7. Aizvērt lapu.


