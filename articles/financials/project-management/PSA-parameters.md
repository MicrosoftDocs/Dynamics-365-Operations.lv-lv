---
title: "Project Service Automation integrācijas parametri"
description: "Varat konfigurēt datu noklusējuma iestatījumus, veicot programmas Project Service Automation integrēšanu ar programmu Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: lv-lv
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Project Service Automation integrācijas parametri

Lapā **Project Service Automation integrācijas parametri** varat konfigurēt datu noklusējuma iestatījumu, veicot programmas Project Service Automation integrēšanu ar programmu Finance and Operations. Lai sekmīgi sinhronizētu programmā Project Service Automation ietvertos projektus ar programmu Finance and Operations, ir jāiestata šādi elementi.

> [!NOTE]
> Projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana ir pieejama programmas Dynamics 365 for Finance and Operations versijā 8.0.




| **Cilne**                      | **Lauks**                          | **Apraksts**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Vispārīgie iestatījumi**                  | **Noklusējuma projekta veids**               | Atlasiet noklusējuma vērtību vienumam **Projekta veids** gadījumos, kad tiek sinhronizēti programmā Project Service Automation ietvertie projekti, ja neesat norādījis noklusējuma vērtību integrācijas veidnē. Sinhronizēšanas laikā jauniem projektiem vienumam **Projekta veids** tiks iestatīta šī vērtība, un to var atjaunināt, veicot programmā Project Service Automation ietverto projekta līguma rindu sinhronizēšanu.               |
| **Vispārīgie iestatījumi**                  | **Laika kategorija**                      | Atlasiet noklusējuma vērtību vienumam **Laika kategorija** gadījumos, kad tiek sinhronizēti programmā Project Service Automation ietvertie stundu novērtējumi. Sinhronizēšanas laikā jaunām projekta stundu prognozēm programmā Finance and Operations vienumam **Kategorija** tiks iestatīta šī vērtība, veicot programmā Project Service Automation ietverto stundu novērtējumu un stundu faktisko vērtību sinhronizēšanu.   |
| **Vispārīgie iestatījumi**                  | **Maksas kategorija**                       | Atlasiet noklusējuma vērtību vienumam **Maksas kategorija** gadījumos, kad tiek sinhronizētas programmā Project Service Automation ietvertās maksas faktiskās vērtības. Sinhronizēšanas laikā jaunām maksas transakcijām programmā Finance and Operations vienumam **Kategorija** tiks iestatīta šī vērtība, veicot programmā Project Service Automation ietverto maksas faktisko vērtību sinhronizēšanu.          |
| **Projektu grupas noklusējuma vērtības**   | **Projekta veids** | Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kurā var izvēlēties projekta veidu, kuram iestatīt noklusējuma projekta grupu. Noteiktu projekta veidu var atlasīt tikai vienu reizi konfigurācijā.              
|                              | **Projektu grupa**          | Atlasiet norādītajam projekta veidam noklusējuma projekta grupu. Kad tiek sinhronizēti programmā Project Service Automation ietvertie projekti, **Projekta grupa** būs noklusējuma iestatījums, kas balstīts uz projekta veidu, ja neesat norādījis noklusējuma vērtību integrācijas veidnē.  |
| **Norēķinu veida noklusējuma vērtības**    | **Norēķinu veids** | Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kurā var izvēlēties norēķinu veidu, kuram iestatīt noklusējuma rindas rekvizītu. Noteiktu norēķinu veidu var atlasīt tikai vienu reizi konfigurācijā.          |
|                              | **Rindas statuss**| Atlasiet norādītajam norēķinu veidam noklusējuma rindas rekvizītu. Sinhronizējot programmā Project Service Automation ietvertos jaunos stundu novērtējumus, jaunos izdevumu novērtējumus vai jaunas faktiskās vērtības, vienums **Rindas rekvizīts** būs noklusējuma iestatījums, kas balstīts uz norēķinu veidu.          |
| **Funkcionalitātes bloķēšana**    |                   | Atlasiet funkcionalitāti, kas tiks atspējota programmā Finance and Operations projektiem un līgumiem, kuru izcelsme ir Project Service Automation. Piemēram, varat izvēlēties izslēgt iespēju rediģēt līgumus un projektus, veidot darba sadalījuma struktūras un ievadīt darba laiku grafikus programmā Finance and Operations. Ar uzskaiti saistītie lauki joprojām būs iespējoti pat tad, ja tie ir atzīmēti kā nepieejami parametru iestatījumos. Pēc noklusējuma tiks iespējotas visas funkcijas.           |

