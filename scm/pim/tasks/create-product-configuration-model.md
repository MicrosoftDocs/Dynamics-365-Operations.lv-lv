--- 
title: "Preces konfigurācijas modeļa izveide"
description: "Šajā procedūrā ir parādīts, kā izveidot preces konfigurācijas modeli un ievadīt pamatinformāciju, piemēram, atribūtus un apakškomponentus."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: da8dd3bbc350c29ce1f7dc22ab3914dfee4b967c
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-configuration-model"></a>Preces konfigurācijas modeļa izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot preces konfigurācijas modeli un ievadīt pamatinformāciju, piemēram, atribūtus un apakškomponentus. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-a-product-model"></a>Preču modeļa izveide
1. Noklikšķiniet uz Preces varianta modeļa definīcija.
2. Noklikšķiniet uz Preču konfigurācijas modeļi.
3. Klikšķiniet Jauns.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Apraksta laukā ierakstiet vērtību.
6. Laukā Risinātāja stratēģija atlasiet opciju.
    * Risinātāja stratēģija nosaka, kā ierobežojumi tiek apstrādāti ierobežojumam atbilstošā preces konfigurācijas modelī. Šī atlase var ietekmēt preces konfigurācijas modeļa veiktspēju.  
7. Laukā Nosaukums ierakstiet kādu vērtību.
    * Saknes komponents norāda preces konfigurācijas modeli, bet to var izmantot arī citos preču modeļos.  
8. Noklikšķiniet uz OK.
9. Laukā Atkārtoti izmantot konfigurācijas atlasiet opciju.
    * Ja parametram Atkārtoti izmantot konfigurācijas ir iestatīta opcija Jā, sistēma meklēs identiskas konfigurācijas pēc katras konfigurācijas sesijas un atkārtoti tās izmantos, ja tiks atrasta precīza atbilstība.  

## <a name="add-attributes"></a>Pievienot atribūtus
1. Izvērsiet sadaļu Atribūti.
2. Noklikšķiniet uz Pievienot.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Risinātāja nosaukums ierakstiet vērtību.
    * Risinātāja nosaukumu izmanto preču konfiguratora ierobežojumu risinātājs. Tajā nedrīkst būt atstarpes vai īpašas rakstzīmes, izņemot _ (pasvītrojums).  
6. Apraksta laukā ierakstiet vērtību.
    * Apraksta teksts tiek rādīts konfigurācijas lietotājam un tādējādi var palīdzēt, izvēloties atbilstošo atribūta vērtību.  
7. Laukā Atribūta tips ievadiet vai atlasiet kādu vērtību.
    * Atribūta tips nosaka, kādas vērtības ir pieejamas atribūtam.  
8. Atzīmējiet izvēles rūtiņu Iekļaut atkārtotā izmantošanā.
    * Šī iespēja pieejama tikai tad, ja ir atlasīta opcija Atkārtoti izmantot konfigurācijas. Atribūta iekļaušana atkārtotas izmantošanas izvēles rūtiņā nozīmē, ka šis atribūts tiks ņemts vērā, kad sistēma meklē precīzu atbilstību.  

## <a name="add-subcomponents"></a>Apakškomponentu pievienošna
1. Izvērsiet sadaļu Apakškomponenti.
2. Noklikšķiniet uz Pievienot.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Risinātāja nosaukums ierakstiet vērtību.
6. Apraksta laukā ierakstiet vērtību.
7. Laukā Komponents ievadiet vai atlasiet kādu vērtību.
    * Katram apakškomponentam jābūt atsaucei uz komponenta definīciju. Šāds noformējums atbalsta atkārtoti izmantojamus komponentus un nodrošina, ka pēc komponenta definēšanas to var izmantot daudzos preču modeļos.  
8. Noklikšķiniet uz Saglabāt.
9. Noklikšķiniet uz Detalizēta informācija par MK rindu.
    * Veidlapa Detalizēta informācija par MK rindu ļauj lietotājam izvēlēties obligātos rekvizītus apakškomponentam. Katram rekvizītam var piešķirt fiksētu vērtību, vai to var kartēt uz atribūtu. Kartēšanas uz atribūtu rezultātā MK rindas rekvizītam būs atšķirīgas vērtības atkarībā no konfigurācijas atlases.  
10. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Katrs apakškomponents pārstāv konfigurējamu preces šablonu ar konfigurācijas atbilstoši ierobežojumam tehnoloģiju. Atsaucei tiek izmantots krājuma kods.  
11. Atzīmējiet izvēles rūtiņu Iestatīt.
12. Laukā Aprēķins atlasiet Jā.
    * Aprēķina opcijas iestatīšana nodrošina, ka prece tiks iekļauta, veicot preces izmaksu aprēķinu.  
13. Noklikšķiniet uz cilnes Iestatījumi.
14. Atzīmējiet izvēles rūtiņu Iestatīt.
15. Laukā Daudzums ievadiet skaitli.
    * Daudzuma lauks nosaka, kāds šīs preces dadzums tiks patērēts konfigurētajai precei.  
16. Atzīmējiet izvēles rūtiņu Iestatīt.
17. Ievadiet skaitli laukā Pa sērijām.
18. Noklikšķiniet uz OK.

