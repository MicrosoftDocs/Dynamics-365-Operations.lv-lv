---
title: Ienākošo dokumentu parsēšana JSON formātā
description: Šajā tēmā ir paskaidrots, kā iestatīt elektronisko pārskatu (ER) formātus, lai parsētu ienākošos dokumentus JavaScript Object Notation (JSON) formātā.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d39a697876641b4c9647dc1a55243ac2ca7cb9e7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564499"
---
# <a name="parse-incoming-documents-in-json-format"></a>Ienākošo dokumentu parsēšana JSON formātā

[!include[banner](../includes/banner.md)]

Varat izstrādāt elektronisko pārskatu (ER) formātus, lai parsētu ienākošos elektroniskos dokumentus, kuri attēlo datus teksta formātā, kas ir balstīts uz JavaScript (citiem vārdiem sakot, failus JavaScript Object Notation \[JSON\] formātā).

Lai uzzinātu vairāk par šo līdzekli, lejupielādējiet failus tālāk redzamajā tabulā un pēc tam atskaņojiet uzdevuma ceļvedi ER Izveidot formāta konfigurāciju, lai importētu datus no ārēja JSON faila. Šajā uzdevuma ceļvedī ir parādīts, kā ER formātu var izmantot, lai parsētu ienākošo JSON failu, lai atjauninātu programmas datus.

| Virsraksts                                  | Faila nosaukums |
|----------------------------------------|-----------|
| ER formāta konfigurācija                | [Formāts kreditoru trans_JSON.xml importēšanai](https://go.microsoft.com/fwlink/?linkid=874111) |
| Ienākošā faila .csv formātā paraugs | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Prasības

Pirms izpildāt uzdevuma ceļvedi ER Izveidot formāta konfigurāciju, lai importētu datus no ārēja JSON faila, ir jānodrošina šāda prasība:

- Pamatelementi JSON failā var būt tikai objekta elementi.
- Objekta ligzdotajiem elementiem ir jābūt rekvizītu elementiem, lai tiktu izveidota derīga JSON struktūra.
- JSON masīvi var būt tikai objekta rekvizītu elementu ligzdoti elementi.
- JSON masīvi var saturēt tikai JSON objektus. Tie nevar saturēt tiešas virknes/skaitliskas vērtības un ligzdotus masīvus. Elementi šajos masīvos tiks parsēti tādā secībā, kādā tie ir norādīti formātā. Tiek ņemti vērā katra JSON objekta daudzkārtīguma iestatījumi.

Turklāt jums ir jāizpilda uzdevuma ceļvedis [ER Izveidot nepieciešamās konfigurācijas datu importēšanai no ārējā faila elektronisko pārskatu veidošanai](tasks/er-required-configurations-import-data.md), ja vēl neesat to izpildījis. Lai izpildītu šo uzdevuma ceļvedi, lejupielādējiet tālāk norādīto failu.

| Virsraksts                  | Faila nosaukums |
|------------------------|-----------|
| ER modeļa konfigurācija | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]