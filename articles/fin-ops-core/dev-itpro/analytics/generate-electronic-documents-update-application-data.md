---
title: Elektronisko dokumentu ģenerēšana un programmas datu atjaunināšana, izmantojot ER
description: Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus, ko var izmantot izejošo elektronisko dokumentu ģenerēšanai. Varat arī izstrādāt ER formātus, kas parsē ienākošos elektroniskos dokumentus un izmanto šajos dokumentos ietverto saturu, lai atjauninātu programmas datus.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 333f91cef12b6564ca9bc668732b4cc038f0fa7e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181868"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Elektronisko dokumentu ģenerēšana un programmas datu atjaunināšana, izmantojot ER

[!include [banner](../includes/banner.md)]

Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus, ko var izmantot izejošo elektronisko dokumentu ģenerēšanai. Varat arī izstrādāt ER formātus, kas parsē ienākošos elektroniskos dokumentus un izmanto šajos dokumentos ietverto saturu, lai atjauninātu programmas datus.

Ar šo funkcionalitāti viens ER formāts var tikt izmantots, gan lai ģenerētu izejošos elektroniskos dokumentus, gan lai pēc tam atjauninātu programmas datus. Šo līdzekli var lietot tālāk aprakstītajos scenārijos.

- Lai novērstu iespēju, ka programmas dati tiek atkārtoti izmantoti turpmākajos procesos, programmas datus varat atzīmēt uzreiz pēc to lietošanas elektronisko dokumentu ģenerēšanai. Varat, piemēram, maksājumu transakcijas atzīmēt kā jau apstrādāts uzreiz pēc tam, kad tās ir iekļautas ģenerētā maksājumu ziņojumā.
- Lai saglabātu apstrādes informāciju elektroniskajiem dokumentiem, kas ir ģenerēti, izmantojot ER loģiku. Piemēram, unikālu identifikāciju maksājuma ziņojumam, kas tiek ģenerēts, izmantojot ER izteiksmi. Šī izteiksme ir balstīta uz ER dialoglodziņā ievadīto informāciju, kad ER formāts tiek palaists dokumentu ģenerēšanai.

Lai uzzinātu vairāk par šo līdzekli, atskaņojiet ER uzdevumu ceļvežu kopu Dokumentu ģenerēšana, saglabājot izmaiņas programmas datos (daļa no 7.5.4.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)), kur ir sniegti detalizēti norādījumi par Intrastat pārskatu izveidi un arhivēšanu. Lai izpildītu noteiktas šajos uzdevumu ceļvežos iekļautās darbības, ir nepieciešami tālāk norādītie faili. Lejupielādējiet un saglabājiet šos failus lokālajā datorā.

- [ER datu modeļa konfigurācija: Intrastat (modelis)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER modeļa kartējuma konfigurācija: Intrastat (kartēšana)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER formāta konfigurācija: Intrastat (formāts)](https://go.microsoft.com/fwlink/?linkid=849038)