---
title: Projekta grupas izveide
description: Šajā sadaļā ir sniegta informācija par to, kā izveidot un pārvaldīt projekta grupas.
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
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760604"
---
# <a name="create-a-project-team"></a>Projekta grupas izveide

[!include [banner](../includes/banner.md)]

Lai lietotu lomas, kas iepriekš tika iestatītas projektā, projektu vadītājam šīs lomas ir jāsaista ar projektu. Projektam var piešķirt vairākas lomas. Lai nerastos pārpratumi, rezervēšanas laikā šīm lomām etiķetes tiek piešķirtas automātiski. Piemēram, ja projektu vadītājam ir nepieciešami trīs programmatūras inženieri, tiek automātiski ģenerētas trīs lomas Programmatūras inženieris, kuru etiķetes ir **1. programmatūras inženieris**, **2. programmatūras inženieris** un **3. programmatūras inženieris**. Ja lomai iepriekš tika iestatītas lomas īpašības, tās tiek pielietotas kā filtrs resursu meklēšanas laikā. Lai precizētu meklēšanu, nepieciešamības gadījumā var pievienot papildu īpašības.

Skata iestatījumus arī var pielāgot, lai nodrošinātu labāku pārskatu par resursu pieejamību. Ir pieejamas iespējas stundu, dienu, nedēļu, ceturkšņu un gada pieejamības attēlošanai. Pastāv arī iespēja rādīt pieejamo un atlikušo resursu noslodzi. Šī opcija ir noderīga laika pārvaldībai, kad novērtējat darbībām pieejamo laiku vai resursu pieejamību.

Projektu vadītājs var lapā atlasīt lomu un pēc tam, ja ir pieejams resurss, kas atbilst vajadzībai, viņš var rezervēt resursu šai lomai. Ņemiet vērā, ka šajā plānošanas posmā resursi nav jārezervē. Veidojot WBS, lomas var aizstāt ar projekta personāla resursiem. Ja WBS ietvaros lomas tiek aizstātas ar personāla resursiem, resursu iestatījumos tiek automātiski atjaunināts projekta grupas saraksts un plānošana.

[![Projekta grupas saraksts, kurā ir ietvertas gan lomas, gan faktiskie resursi](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektu vadītājam ir dažādas iespējas projekta resursu rezervācijai, piemēram, **Atlikusī noslodze**, **Pilna noslodze**, **Noslodzes procentuālā daļa** un **Norādiet stundas**. Šīs rezervēšanas iespējas var atcelt jebkurā laikā, ja mainās resursu piešķires. Tiek atbalstīti divi rezervāciju tipi:

- **Stingrā rezervācija** – resursa rezervācija ir apstiprināta darbam attiecīgajā iesaistē uz norādīto laiku.
- **Vieglā rezervēšana** – resursu rezervācijas ir uz laiku iestatītas darbam attiecīgajā iesaistē uz norādīto laiku.

Tālāk esošajā procedūrā izskaidrots, kā izveidot projekta grupu.

## <a name="create-a-project-team"></a>Projekta grupas izveide

1. Saraksta lapā **Visi projekti** atlasiet kādu projektu un pēc tam atlasiet **Rediģēt**.
2. Cilnes **Projekta grupa un plānošana** laukā **Grafika beigu datums** ievadiet grafika sākuma datumu, kam ir pieskaitīts viens mēnesis. Piemēram, ja grafika sākuma datums ir 2017. gada 24. jūnijs (24/06/2017), ievadiet **24/07/2017**.
3. Atlasiet **Pievienot**.
4. Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Vecākais projektu vadītājs**.
5. Atlasiet **Nepieciešamās kompetences**.
6. Lapā **Īpašību izvēle** īpašības, ko iepriekš iestatījāt lomai Vecākais projektu vadītājs, tiek atlasītas pēc noklusējuma. Atlasiet **Labi**.
7. Lapas **Pievienot projekta lomas** laukā **Resursu skaits** ievadiet **1**.
8. Laukā **Resursi** uzmeklēšana parāda visus resursus, kuriem ir nepieciešamās kompetences. Atlasiet **Rihards Taurenis** un pēc tam atlasiet **Izveidot**.
9. Lapā **Projekts** atlasiet **Pievienot**.
10. Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Grupas dalībnieks**. Laukā **Resursu skaits** ievadiet **5**.
11. Atlasiet **Izveidot**.
12. Lapā **Projekti** atlasiet **Izpildīt resursu**.

## <a name="monitor-project-teams"></a>Projektu grupu pārraudzība
1. Lapā **Visi projekti** atlasiet saiti **Projekta ID** projektam **XYZ jaunināšanas fāze 2**.
2. Kopsavilkuma cilnē **Projekta grupa un plānošana** pārbaudiet, vai minētie projekta resursi ir pareizi.
