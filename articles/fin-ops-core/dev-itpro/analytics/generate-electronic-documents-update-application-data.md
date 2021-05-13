---
title: Elektronisko dokumentu ģenerēšana un programmas datu atjaunināšana, izmantojot ER
description: Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus, ko var izmantot izejošo elektronisko dokumentu ģenerēšanai.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f66a173c7d66f915a7802e42caf1a36f661eea1
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944321"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Elektronisko dokumentu ģenerēšana un programmas datu atjaunināšana, izmantojot ER

[!include [banner](../includes/banner.md)]

Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus, ko var izmantot izejošo elektronisko dokumentu ģenerēšanai. Varat arī izstrādāt ER formātus, kas parsē ienākošos elektroniskos dokumentus un izmanto šajos dokumentos ietverto saturu, lai atjauninātu programmas datus.

Ar šo funkcionalitāti viens ER formāts var tikt izmantots, gan lai ģenerētu izejošos elektroniskos dokumentus, gan lai pēc tam atjauninātu programmas datus. Šo līdzekli var lietot tālāk aprakstītajos scenārijos.

- Lai novērstu iespēju, ka programmas dati tiek atkārtoti izmantoti turpmākajos procesos, programmas datus varat atzīmēt uzreiz pēc to lietošanas elektronisko dokumentu ģenerēšanai. Varat, piemēram, maksājumu transakcijas atzīmēt kā jau apstrādāts uzreiz pēc tam, kad tās ir iekļautas ģenerētā maksājumu ziņojumā.
- Lai saglabātu apstrādes informāciju elektroniskajiem dokumentiem, kas ir ģenerēti, izmantojot ER loģiku. Piemēram, unikālu identifikāciju maksājuma ziņojumam, kas tiek ģenerēts, izmantojot ER izteiksmi. Šī izteiksme ir balstīta uz ER dialoglodziņā ievadīto informāciju, kad ER formāts tiek palaists dokumentu ģenerēšanai.

Lai uzzinātu vairāk par šo līdzekli, atskaņojiet ER uzdevumu ceļvežu kopu Dokumentu ģenerēšana, saglabājot izmaiņas programmas datos (daļa no 7.5.4.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)), kur ir sniegti detalizēti norādījumi par Intrastat pārskatu izveidi un arhivēšanu. Lai izpildītu noteiktas šajos uzdevumu ceļvežos iekļautās darbības, ir nepieciešami tālāk norādītie faili. Lejupielādējiet un saglabājiet šos failus lokālajā datorā.

- [ER datu modeļa konfigurācija: Intrastat (modelis)](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [ER modeļa kartējuma konfigurācija: Intrastat (kartēšana)](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [ER formāta konfigurācija: Intrastat (formāts)](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
