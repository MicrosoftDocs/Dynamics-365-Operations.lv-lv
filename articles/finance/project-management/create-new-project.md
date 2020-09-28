---
title: Izveidot jaunu projektu
description: Šajā sadaļā ir sniegta informācija par to, kā izveidot jaunu projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760603"
---
# <a name="create-a-new-project"></a>Izveidot jaunu projektu

[!include [banner](../includes/banner.md)]

Lai izveidotu jaunu projektu, veiciet tālāk norādītās transakcijas.

1. Lapā **Projektu vadība** atlasiet **Jauns projekts** un ievadiet tālāk norādītās vērtības.

    - **Projekta veids:** Laiks un materiāls
    - **Projekta nosaukums:** XYZ jaunināšanas fāze 2
    - **Projektu grupa:** TM\_WIP
    - **Projekta līguma ID:** 00000002

2. Atlasiet **Izveidot projektu**.

## <a name="assign-a-resource-to-a-project"></a>Resursa piešķiršana projektam

1. Lapa **Nodarbinātie**, sarakstā **Nodarbinātie** atlasiet tāda nodarbinātā ierakstu, kuram iepriekš veicāt kompetenču iestatīšanu, un atveriet šī nodarbinātā ierakstu.
2. Darbību rūts cilnē **Projekts**, grupā **Iestatījumi** atlasiet **Piešķirt projektus**.
3. Lapā **Resursa apstiprināšanas projektu piešķires**, cilnē **Projekti**, laukā **Pievienot projektu atlasītajiem projektiem** filtrējiet pēc projekta **XYZ jaunināšanas fāze 2**.
4. Rūtī **Atlikušie projekti** atlasiet kādu projektu un pēc tam atlasiet bultiņas pogu, lai to pievienotu rūtī **Atlasītie projekti**.

Ja nepieciešams, resursam varat piešķirt arī kategorijas. Kategorijas tips ir **Izmaksas** vai **Ieņēmumi**. Kategorijas tipu nosaka jūsu organizācija. Ja resursam nav piešķirta neviena kategorija, tad programmā Finance tiek uzmeklēta noklusējuma kategorija izmaksu un ieņēmumu stundu likmēm.

## <a name="set-up-project-resource-and-role-characteristics"></a>Projekta resursu un lomu īpašību iestatīšana

Projekta vadītājs var izmantot projekta resursu sadalījuma funkcionalitāti, lai izveidotu lomas, kas nepieciešamas projektam. Lomas var izmantot, ja resursu rezervēšanas laikā apstiprinātie resursi joprojām nav zināmi. Lomas var uz laiku rezervēt kā ieplānotos resursus, lai varētu turpināt projekta plānošanas posmus.

[![Lomas piemērs](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenārijs:** Contoso tika nolīgts, lai pabeigtu laika un materiālu projektu, kuram ir apstiprināta projekta privilēģijas. Jaunākais projektu vadītājs joprojām strādā pie projekta darba apjoma pabeigšanas. Resursu pārvaldnieks pašlaik norāda konkrētus resursus, kas tiks rezervēti darbam ar jauno projektu. Tā kā attiecīgais projekts ir ļoti svarīgs, projekta sponsors kā vienu no lomām pieprasīja lomu Vecākais projektu vadītājs. Resursu pārvaldniekam ir jāiegūst jaunais resurss un sistēmā jādefinē loma, lai tā būtu pieejama gadījumā, ja jaunākajam projektu vadītājam projekta plānošanas laikā ir nepieciešama resursa informācija.

Tālāk sniegtajos darbību aprakstos ir norādīts, kā resursu pārvaldnieks var iestatīt lomu Vecākais projektu vadītājs un piesaistīt tai resursa īpašības. Pēc tam šo lomu var izmantot, lai meklētu pieejamos resursus, kas atbilst nepieciešamajām resursu kompetencēm.

1. Lapā **Lomu iestatīšana** atlasiet **Jauns** un ievadiet tālāk norādītās vērtības.

    - **Lomas ID:** Vecākais projektu vadītājs
    - **Apraksts:** Vecākais projektu vadītājs

2. Atlasiet **Izveidot**.
3. Atlasiet lomu **Vecākais projektu vadītājs** un pēc tam atlasiet **Konfigurēt īpašības**.
4. Laukā **Īpašību veids** atlasiet **Prasme**.
5. Laukā **Pieejamās īpašības** ievadiet meklējamo prasmi.
6. Laukā **Īpašību veids** atlasiet **Sertifikāts**.
7. Laukā **Pieejamās īpašības** ievadiet meklējamo sertifikātu.

## <a name="assign-a-project-resource-to-a-project"></a>Projekta resursa piešķiršana projektam

1. Lapā **Visi projekti** atlasiet projektu **XYZ jaunināšanas fāze 2**.
2. Cilnē **Projekta grupa un plānošana** atlasiet **Pievienot**.
3. Laukā **Loma** atlasiet **Grupas dalībnieks**.
4. Atlasiet **Rezervēt no kalendāra**.
5. Lapā **Resursu pieejamība** atlasiet **Skata iestatījumi**.
6. Lapā **Pielāgojiet skata iestatījumus** ievadiet šādas vērtības:

    - **Datumu diapazona skata formāts:** Diena
    - **Parādīt pieejamības aprakstus:** Jā
    - **Rādīt atlikušo noslodzi:** Jā

7. Resursu sarakstā atlasiet resursu.
8. Atlasiet **Stingrā rezervēšana** un **Visa noslodze**.

## <a name="assign-a-resource-to-a-default-role"></a>Resursa piešķiršana noklusējuma lomai

Lai palīdzētu projektu vadītājiem vai resursu pārvaldniekiem, varat detalizētāk rādīt resursus, ko var rezervēt projektam. Noklusējuma lomu var saistīt ar esošu resursu vai jauniegūtu resursu. Piemēram, kad Rihards tika pieņemts darbā, viņa pieredze un prasmes bija piemērotas lomai Biznesa analītiķis. Resursu pārvaldnieks piešķīra šo lomu kā Rihards noklusējuma lomu. Tādējādi resursu pārvaldnieks pievienoja Danielu to biznesa analītiķu kopai, kuri ir pieejami darbam projektā.

Resursu rezervēšanas laikā projektu vadītāji var filtrēt lomu resursus, kas ir pieejami darbam projektos. Viņi var izmantot šo informāciju kā vienu kritēriju, veicot vairāku kritēriju lēmumu analīzi resursu izpildes laikā. Viņi var pievienot arī citas resursa īpašības filtram, lai meklētu resursus, kuriem ir īpašas prasmes, izglītība un pieredze attiecīgajam projektam.

**Scenārijs:** ir uzsākts apstiprināts projekts, un loma Vecākais projektu vadītājs ir rezervēta kā ieplānots resurss projekta plānošanas posma laikā. Resursu pārvaldnieks ir ieguvis resursu, lai aizpildītu lomu Vecākais projektu vadītājs.

1. Lapā **Resursu saraksts** atlasiet **Rihards Taurenis**.
2. Lapā **Resursa loma** atlasiet **Jauns** un ievadiet tālāk norādītās vērtības.

    - **Ir spēkā:** ievadiet pašreizējo datumu.
    - **Termiņa beigas:** ievadiet **Nekad**.
    - **Loma:** ievadiet **Vecākais projektu vadītājs**.

3. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
4. Cilnē **Kompetences** pievienojiet prasmi **ProjectMgmt** un sertifikātu **PMP**.
