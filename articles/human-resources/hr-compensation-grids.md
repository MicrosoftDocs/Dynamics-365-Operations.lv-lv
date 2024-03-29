---
title: Atlīdzību režģu iestatīšana
description: Atlīdzības režģi tiek izmantoti, lai definētu un uzturētu algu struktūras fiksētās atlīdzības plāniem.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9119c15cf80b9ebb9bed83ac438f24249aa4aa2f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691678"
---
# <a name="set-up-compensation-grids"></a>Atlīdzību režģu iestatīšana


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Atlīdzības režģi tiek izmantoti, lai definētu un uzturētu algu struktūras fiksētās atlīdzības plāniem. Atlīdzības režģus var koplietot vairākiem plāniem vai kopēt, veidojot jaunu atlīdzības plānu.  Pirms atlīdzības režģa izveidošanas ir jāiestata Līmeņi un Atsauces punkti. Šajā piemērā tiks izveidots jauns atlīdzības režģa pakāpes tips, izmantojot demonstrācijas datus līmeņiem un atskaites punktiem. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Informāciju par atlīdzības režģi iestatīšana
1. Pārejiet uz sadaļu **Personāla vadība**  >  **Atlīdzība**  >  **Fiksēta atlīdzība**  > **Atlīdzības režģi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Režģis** ierakstiet vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Atlasiet opciju laukā **Tips**.
6. Ievadiet vai atlasiet vērtību iestatīšanas laukā **Atsauce**.
7. Laukā **Valūta** ievadiet vai atlasiet vērtību.
8. Laukā **Spēkā stāšanās datums** ievadiet datumu.

## <a name="add-levels-to-the-compensation-structure"></a>Līmeņu pievienošana kompensācijas struktūrai
1. Noklikšķiniet uz **Atlīdzības struktūra**.
2. Sarakstā atzīmējiet atlasīto rindu.
3. Laukā **Līmenis** ievadiet vai atlasiet kādu vērtību.
4. Klikšķiniet **Jauns**.
5. Sarakstā atzīmējiet atlasīto rindu.
6. Laukā **Līmenis** ievadiet vai atlasiet kādu vērtību.
7. Klikšķiniet **Jauns**.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Laukā **Līmenis** ievadiet vai atlasiet kādu vērtību.
10. Klikšķiniet **Jauns**.
11. Sarakstā atzīmējiet atlasīto rindu.
12. Laukā **Līmenis** ievadiet vai atlasiet kādu vērtību.
13. Klikšķiniet **Jauns**.
14. Sarakstā atzīmējiet atlasīto rindu.
15. Laukā **Līmenis** ievadiet vai atlasiet kādu vērtību.

## <a name="fill-in-the-compensation-structure-with-values"></a>Kompensācijas struktūras aizpildīšana ar vērtībām
1. Sarakstā atzīmējiet atlasīto rindu.
    * Šajā posmā katrā tabulas laukā var manuāli ievadīt atlīdzības vērtības vai arī var izmantot funkciju Masveida izmaiņas, lai vienkārši aizpildītu vairākus laukus un veiktu pamata aprēķinus.  
2. Noklikšķiniet **Masveida izmaiņas**.
    * Šim režģim vispirms tiks lietota pirmā līmeņa viduspunkta vērtība visiem tabulas laukiem. Tas būs pamats atlīdzības matricai.  
3. Laukā **Korekcijas veids** atlasiet opciju.
4. Laukā **Korekcijas summa** ievadiet kādu skaitli.
5. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.
6. Noklikšķiniet uz **Piemērot režģim**.
    * Tagad izmantosim masveida izmaiņu funkciju, lai palielinātu summas katrā nākamajā līmenī par noteiktu procentuālo vērtību vai summu. Šajā piemērā katrai pakāpei būs 12,5 % izplatība starp to viduspunktiem.  
7. Laukā **Korekcijas veids** atlasiet opciju.
8. Laukā **Korekcijas summa** ievadiet kādu skaitli.
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Noklikšķiniet uz **Piemērot režģim**.
    * Tagad izmantosim masveida izmaiņu funkciju, lai koriģētu minimālo un maksimālo atsauces punktu katram līmenim. Šajā piemērā tiks izmantota 50 % izplatība, tādējādi minimālais atsauces punkts tiks koriģēts par –20 % un maksimālais atsauces punkts tiks koriģēts pa +20 %.  
11. Laukā **Korekcijas summa** ievadiet kādu skaitli.
12. Ievadiet vai atlasiet vērtību laukā **Atsauces punkts**.
13. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.
14. Noklikšķiniet uz **Piemērot režģim**.
15. Laukā **Korekcijas summa** ievadiet kādu skaitli.
16. Ievadiet vai atlasiet vērtību laukā **Atsauces punkts**.
17. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.
18. Noklikšķiniet uz **Piemērot režģim**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
