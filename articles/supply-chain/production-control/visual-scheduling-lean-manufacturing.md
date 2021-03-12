---
title: Vizuāla plānošana ražošanai lean manufacturing
description: Šajā tēmā ir sniegta informācija par Kanban plānošanas paneli, kuru ražošanas plānotājs var izmantot, lai kontrolētu un optimizētu ražošanas plānu Kanban darbiem.
author: johanhoffmann
manager: tfehr
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization, KanbanBoardUnplannedJobs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76a72e09f72c396f457283bfd18c41cac2607d1f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998607"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a>Vizuāla plānošana ražošanai lean manufacturing

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par Kanban plānošanas paneli, kuru ražošanas plānotājs var izmantot, lai kontrolētu un optimizētu ražošanas plānu Kanban darbiem.

Šajā tēmā ir sniegta informācija par Kanban plānošanas paneli, kuru ražošanas plānotājs var izmantot, lai kontrolētu un optimizētu ražošanas plānu Kanban darbiem.

Izmantojot Kanban plānošanas paneli, ražošanas plānotājs var kontrolēt un optimizēt ražošanas plānu Kanban darbiem. Tas padara Kanban darbu plūsmu pārredzamu un ražošanas plānotājam nodrošina rīku, kas ražošanas plānu optimizē un pielāgo lean manufacturing darba šūnai.

## <a name="visual-scheduling-of-kanban-jobs"></a>Vizuāla Kanban darbu plānošana
Kanban darbs var ietvert vienu vai daudzus Kanban darbus. Ir divu tipu Kanban darbi.

-   Apstrādāt
-   Pārsūtījums

Ieplānot var tikai tipa **Apstrādāt** darbus. Kanban darbs un tā rekvizīti, piemēram, darbības laiks, ir definēti ražošanas Kanban plūsmā. Ražošanas Kanban plūsmā Kanban darbs tiek arī piešķirts darba šūnai. Darba šūnas ikdienas noslodze tiek aprēķināta, pamatojoties uz resursu grupā iestatīto darba šūnas noslodzi. Tā tiek pielāgota atbilstoši ikdienas darba laikam saistītajā kalendārā. Kad Kanban darbs tiek plānots, šis darbs ielādē darba šūnas noslodzi. Kanban plānošanas panelis nodrošina tālāk norādītās galvenās funkcijas.

-   Grafisks pārskats par ražošanas plānu racionālā darba šūnā. Šajā pārskatā tiek rādīti plānotie Kanban apstrādes darbi definētajos periodos.
-   Rīks, kas ļauj plānot neieplānotos Kanban darbus un pārplānot iepriekš plānotos darbus.

## <a name="kanban-schedule-board"></a>Kanban grafika dēlis
Lapā **Kanban plānošanas panelis** ir septiņi galvenie elementi, kā parādīts tālāk esošajā attēlā. 

![Kanban grafika dēlis](./media/kanban-schedule-board-1024x554.png)
1.  Darbības rūts
2.  Lauku filtrēšana
3.  Poga neplānotajiem darbiem
4.  Perioda mezgls
5.  Kanban darbs
6.  Noslodzes josla
7.  Laika skala

### <a name="view-the-time-scale"></a>Laika skalas skatīšana

Panelis ir sadalīts periodos, un katrs no tiem ir attēlots kā mezgls (4). Perioda mezgli tiek uzskaitīti uz vertikālās ass, un uz horizontālās ass attēlota laika skala (7), kurā parādīts perioda garums. Perioda garums ir viena diena vai viena nedēļa. Perioda garumu nosaka Kanban plānošanas panelim (2) atlasītā darba šūnas konfigurācija. Katram perioda mezglam Kanban plānošanas panelis norāda, cik daudz plānoto Kanban darbu noslogo periodu. Sniegta arī norāde par maksimālo perioda caurlaidi. Ja plānotā caurlaide pārsniedz maksimālo caurlaidi, periods tiek uzskatīts par pārslogotu, un tiek parādīts sarkans brīdinājuma simbols. Plānotais Kanban darbs tiek rādīts periodā, kam ir ieplānoti sākuma un beigu laiki (5). Darba garums ir vienāds ar darbības laiku. Kanban darbi periodā ir redzami pārklājušies, ja darbības laiks pārsniedz darba šūnas uzdevuma laiku.

### <a name="view-job-status"></a>Darba statusa skatīšana

Papildinformācija par Kanban darbu ir pieejama rīka padomā, kas parādās, peles rādītāju novietojot virs darba. Simbols sniedz informāciju par darba statusu. Piemēram, pulksteņa simbols norāda, ka Kanban darbs ir nokavēts.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Krāsu izmantošana Kanban plānošanas paneļa skatīšanai

Lai uzlabotu Kanban plānošanas paneļa sniegto pārskatu, varat izmantot krāsas Kanban darbu atšķiršanai. Kanban darba krāsa tiek konfigurēta racionālās plānošanas grupā, kurā varat apkopot preces, kas jāražo vienā secībā. Izmantojot pogu **Lietot dizaina krāsas** darbību rūts cilnē **Panelis**, varat pārslēgt programmas dizaina krāsas, kā arī racionālās plānošanas grupā konfigurētās krāsas. Katram periodam noslodzes josla (6) norāda, cik daudz no periodam pieejamajām stundām ir noslogotas ar Kanban darbiem. Ja periods ir pārslogots, noslodzes josla tiek parādīta biezāka un sarkanā krāsā. Visas šīs funkcijas ir pieejamas darbību rūts (1) cilnē **Panelis** lapas **Kanban plānošanas panelis** augšdaļā.

## <a name="plan-unplanned-jobs"></a>Plānot neplānotus darbus
Neplānotos Kanban darbus varat plānot dialoglodziņā **Plānot neplānotos darbus**. Lai atvērtu šo dialoglodziņu, noklikšķiniet uz pogas **Neplānotie darbi**, kas parāda pašreizējo neplānoto darbu skaitu. Vai arī noklikšķiniet uz **Plānot neplānotos darbus** darbību rūts cilnē **Panelis**. Dialoglodziņā tiek rādīts saraksts ar darba šūnas neplānotajiem Kanban darbiem. Varat izmantot lauku **Filtrēt**, lai filtrētu visus laukus režģī. Piemēram, varat filtrēt Kanban darbus pēc noteiktas preces. Kad esat izfiltrējis sarakstu ar darbiem, ko vēlaties ieplānot, atlasiet tos sarakstā un pēc tam noklikšķiniet uz **Labi**. Lai darbu plānošanai lietotu automātisko plānošanu, opciju **Automātiskā plānošana** iestatiet uz **Jā**. Šajā gadījumā darbi tiek ieplānoti periodā saskaņā ar to izpildes datumu. Darbus varat plānot arī pēc perioda. Atlasiet kādu periodu laukā **Periods**. Tālāk esošajā attēlā parādīts dialoglodziņa **Plānot neplānotos darbus** piemērs. 

![Dialoglodziņš Plānot neplānotos darbus](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Kanban darbu kārtošana vienā periodā
Varat mainīt viena vai vairāku atlasīto darbu secību periodā. Šī iespēja var būt noderīga, ja noteiktiem darbiem periodā vēlaties piešķirt prioritāti. Iespējams, vēlaties kārtot darbus, kuriem ir vienādas preču īpašības, lai optimizētu darbu izpildi. Secību var mainīt, veicot vilkšanas un nomešanas darbību vai izmantojot izvēlnes vienumus **Atpakaļ** un **Uz priekšu** darbību rūts cilnē **Panelis**.

## <a name="reassign-kanban-jobs-across-periods"></a>Kanban darbu atkārtota piešķire periodos
Darbus var atkārtoti piešķirt no viena perioda uz citu. Šī iespēja var būt noderīga, ja periods ir pārslogots un vēlaties izlīdzināt noslodzi, pārceļot to uz brīvākiem periodiem. Darbus var atkārtoti piešķirt, veicot vilkšanas un nomešanas darbību vai izmantojot izvēlnes vienumus **Nākamais periods** un **Iepriekšējais periods** darbību rūts cilnē **Panelis**.

## <a name="open-the-kanban-schedule-board"></a>Kanban plānošanas paneļa atvēršana
Kanban plānošanas paneli var atvērt, izmantojot izvēlnes vienumu tālāk norādītajās lapās.

-   Lapa **Ražošanas vieta**
-   Lapa **Kanban darbu plānošana**
-   Lapa **Ražošanas plūsmas vizualizēšana**


<a name="additional-resources"></a>Papildu resursi
--------

[Kanban darbu plānošana ražošanai lean manufacturing](lean-manufacturing-kanban-job-scheduling.md)

