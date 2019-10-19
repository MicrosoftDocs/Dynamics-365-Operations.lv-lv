---
title: Project Service Automation integrācijas parametri
description: Šajā tēmā ir paskaidrots, kā konfigurēt noklusējuma datu ievades viedu, integrējot Microsoft Dynamics 365 for Project Service Automation programmā Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: f7cef5384812e0dcb7d5e084ddd7668a7687a259
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174948"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation integrācijas parametri

[!include[banner](../includes/banner.md)]

Lapā **Project Service Automation integrācijas parametri** varat konfigurēt noklusējuma datu ievades veidu, integrējot Dynamics 365 Project Service Automation programmā Dynamics 365 Finance. Lai projektus no Project Service Automation sekmīgi sinhronizētu uz Finance, ir jāiestata tālāk noradītie lauki.

> [!NOTE]
> - Versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.
> - Faktisko vērtību integrācija ir pieejama versijā 8.0.1 vai jaunākās versijās.


| Cilne                    | Lauks                | Apraksts |
|------------------------|----------------------|-------------|
| Vispārējs                | Noklusējuma projekta tips | Atlasiet noklusējuma projekta tipu. Kad projekti tiek sinhronizēti no Project Service Automation un integrācijas veidnē neesat norādījis noklusējuma vērtību, tiek izmantota šī vērtība. Sinhronizēšanas laikā jauno projektu lauks **Projekta tips** tiek iestatīts uz šo vērtību. Taču šī vērtība var tikt atjaunināta, kad projekta līguma rindas tiek sinhronizēts no Project Service Automation. |
|                        | Laika kategorija        | Atlasiet noklusējuma laika kategoriju. Šī vērtība tiek izmantota, kad stundu novērtējumi tiek sinhronizēti no Project Service Automation. Kad stundu novērtējumi un stundu faktiskās vērtības tiek sinhronizētas no Project Service Automation, jauna projekta stundu novērtējumu lauks **Kategorija** programmā Finance tiek iestatīts uz šo vērtību. |
|                        | Papildmaksas kategorija         | Atlasiet noklusējuma maksas kategoriju. Šī vērtība tiek izmantota, kad maksu faktiskās vērtības tiek sinhronizētas no Project Service Automation. Kad maksu faktiskās vērtības tiek sinhronizētas no Project Service Automation, jaunu maksu transakciju lauks **Kategorija** programmā Finance tiek iestatīts uz šo vērtību. |
| Projektu grupas noklusējuma vērtības | Projekta tips         | Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kurā var izvēlēties projekta tipu, kuram iestatīt noklusējuma projektu grupu. Noteiktu projekta tipu konfigurācijā var atlasīt tikai vienu reizi. |
|                        | Projektu grupa        | Atlasītajam projekta tipam atlasiet noklusējuma projektu grupu. Kad jaunie projekti tiek sinhronizēti no Project Service Automation un integrācijas veidnē neesat norādījis noklusējuma vērtību, lauks **Projektu grupa** tiek iestatīts uz noklusējuma vērtību attiecīgajam projekta tipam. |
| Norēķinu veida noklusējuma vērtības  | Norēķinu veids         | Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kur varat atlasīt norēķinu tipu, kuram iestatīt noklusējuma rindas rekvizītu. Noteiktu norēķinu tipu konfigurācijā var atlasīt tikai vienu reizi. |
|                        | Rindas rekvizīts        | Atlasītajam norēķinu tipam atlasiet noklusējuma rindas rekvizītu. Kad jauni stundu novērtējumi, jauni izdevumu novērtējumi vai jaunas faktiskās vērtības tiek sinhronizētas no Project Service Automation, lauks **Rindas rekvizīts** tiek iestatīts uz attiecīgā norēķinu tipa noklusējuma vērtību. |
| Funkcionalitātes bloķēšana  | Nav attiecināms       | Atlasiet funkcionalitāti, kas tiks atspējota programmā Finance projektiem un līgumiem, kuru izcelsme ir Project Service Automation. Piemēram, varat izslēgt iespēju rediģēt līgumus un projektus, veidot darba sadalījuma struktūras un ievadīt darba laika uzskaites tabulas programmā Finance. Ar uzskaiti saistītie lauki joprojām būs iespējoti pat tad, ja tie ir atzīmēti kā nepieejami parametru iestatījumos. Pēc noklusējuma visa funkcionalitāte ir iespējota. |
