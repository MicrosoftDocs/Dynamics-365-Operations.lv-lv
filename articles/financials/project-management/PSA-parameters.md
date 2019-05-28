---
title: Project Service Automation integrācijas parametri
description: Šajā tēmā ir paskaidrots, kā konfigurēt noklusējuma datu ievades viedu, integrējot Microsoft Dynamics 365 for Project Service Automation programmā Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 33960a97f69d6bcc70a3035d4d68095ca6993a10
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557287"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation integrācijas parametri

[!include[banner](../includes/banner.md)]

Lapā **Project Service Automation integrācijas parametri** varat konfigurēt noklusējuma datu ievades veidu, integrējot Microsoft Dynamics 365 for Project Service Automation programmā Microsoft Dynamics 365 for Finance and Operations. Lai projektus no Project Service Automation sekmīgi sinhronizētu uz Finance and Operations, ir jāiestata tālāk noradītie lauki.

> [!NOTE]
> - Microsoft Dynamics 365 for Finance and Operations versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.
> - Faktisko vērtību integrācija ir pieejama Microsoft Dynamics 365 for Finance and Operations versijā 8.0.1 vai jaunākās versijās.
> - Ja lietojat Microsoft Dynamics 365 for Finance and Operations Enterprise Edition versiju 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu. Ja ir nepieciešams atiestatīt uzskaites sadali, mēs ieteicām instalēt arī KB 4131710.

| Cilne                    | Lauks                | apraksts |
|------------------------|----------------------|-------------|
| Vispārēji                | Noklusējuma projekta veids | Atlasiet noklusējuma projekta tipu. Kad projekti tiek sinhronizēti no Project Service Automation un integrācijas veidnē neesat norādījis noklusējuma vērtību, tiek izmantota šī vērtība. Sinhronizēšanas laikā jauno projektu lauks **Projekta tips** tiek iestatīts uz šo vērtību. Taču šī vērtība var tikt atjaunināta, kad projekta līguma rindas tiek sinhronizēts no Project Service Automation. |
|                        | Laika kategorija        | Atlasiet noklusējuma laika kategoriju. Šī vērtība tiek izmantota, kad stundu novērtējumi tiek sinhronizēti no Project Service Automation. Kad stundu novērtējumi un stundu faktiskās vērtības tiek sinhronizētas no Project Service Automation, jauna projekta stundu novērtējumu lauks **Kategorija** programmā Finance and Operations tiek iestatīts uz šo vērtību. |
|                        | Maksas kategorija         | Atlasiet noklusējuma maksas kategoriju. Šī vērtība tiek izmantota, kad maksu faktiskās vērtības tiek sinhronizētas no Project Service Automation. Kad maksu faktiskās vērtības tiek sinhronizētas no Project Service Automation, jaunu maksu transakciju lauks **Kategorija** programmā Finance and Operations tiek iestatīts uz šo vērtību. |
| Projektu grupas noklusējuma vērtības | Projekta veids         | Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kurā var izvēlēties projekta tipu, kuram iestatīt noklusējuma projektu grupu. Noteiktu projekta tipu konfigurācijā var atlasīt tikai vienu reizi. |
|                        | Projektu grupa        | Atlasītajam projekta tipam atlasiet noklusējuma projektu grupu. Kad jaunie projekti tiek sinhronizēti no Project Service Automation un integrācijas veidnē neesat norādījis noklusējuma vērtību, lauks **Projektu grupa** tiek iestatīts uz noklusējuma vērtību attiecīgajam projekta tipam. |
| Norēķinu veida noklusējuma vērtības  | Norēķinu veids         | Noklikšķiniet uz **Jauns**, lai pievienotu rindu, kur varat atlasīt norēķinu tipu, kuram iestatīt noklusējuma rindas rekvizītu. Noteiktu norēķinu tipu konfigurācijā var atlasīt tikai vienu reizi. |
|                        | Rindas rekvizīts        | Atlasītajam norēķinu tipam atlasiet noklusējuma rindas rekvizītu. Kad jauni stundu novērtējumi, jauni izdevumu novērtējumi vai jaunas faktiskās vērtības tiek sinhronizētas no Project Service Automation, lauks **Rindas rekvizīts** tiek iestatīts uz attiecīgā norēķinu tipa noklusējuma vērtību. |
| Funkcionalitātes bloķēšana  | Nav attiecināms       | Atlasiet funkcionalitāti, kas tiks atspējota programmā Finance and Operations projektiem un līgumiem, kuru izcelsme ir Project Service Automation. Piemēram, varat izslēgt iespēju rediģēt līgumus un projektus, veidot darba sadalījuma struktūras un ievadīt darba laika uzskaites tabulas programmā Finance and Operations. Ar uzskaiti saistītie lauki joprojām būs iespējoti pat tad, ja tie ir atzīmēti kā nepieejami parametru iestatījumos. Pēc noklusējuma visa funkcionalitāte ir iespējota. |
