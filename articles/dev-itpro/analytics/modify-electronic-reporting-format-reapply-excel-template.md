---
title: "Elektronisko pārskatu veidošanas formātu modificēšana, atkārtoti lietojot Excel veidnes"
description: "Šajā tēmā ir sniegta informācija par to, kā var izmainīt biznesa dokumentu ģenerēšanai izmantoto elektronisko pārskatu veidošanas (ER) formātu, atkārtoti lietojot izmainītu Excel veidni."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8707f7b184bb66648edd0e48672c5514a0a5caf1
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Elektronisko pārskatu veidošanas formātu modificēšana, atkārtoti lietojot Excel veidnes

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu veidošanas (ER) rīks tiek izmantots elektroniska formāta biznesa dokumentu ģenerēšanai. Ja vēlaties ģenerēt biznesa dokumentu, jums ir jāizveido ER formāta un pēc tam jāizmanto ER noformētājs, lai definētu biznesa dokumenta izkārtojumu un norādītu tajā ietveramos datus. Pēc tam varat izpildīt ER formātu, lai ģenerētu biznesa dokumentu.

ER rīku var izmantot, lai ģenerētu biznesa dokumentus Microsoft Excel failu formātā. Kā šo dokumentu veidnes varat izmantot Excel dokumentus. Lai ER noformētājā definētu dokumenta izkārtojumu, varat definētajā ER formātā importēt tā Excel dokumenta saturu, ko vēlaties izmantot kā veidni. Lai saņemtu papildinformāciju un izmēģinātu šo scenāriju, atskaņojiet uzdevuma ceļvedi **Konfigurācijas noformēšana pārskatu ģenerēšanai OPENXML formātā (ER)** (daļa no 7.5.4.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)).

Ja rediģējat Excel dokumentu, kas tiek izmantots kā biznesa dokumenta veidne, jauna ER funkcionalitāte sniedz iespēju ER formātam atkārtoti lietot atjaunināto veidni. Pēc tam ER formāts tiek atjaunināts atbilstoši atjauninātajai veidnei. Lai saņemtu papildinformāciju par šo funkcionalitāti, atskaņojiet uzdevuma ceļvedi **Formāta izmainīšana, atkārtoti lietojot Excel veidni (ER)** (daļa no 7.5.5.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10683)). Veicot uzdevuma ceļveža darbību, kuras ietvaros importējat atjauninātu veidni, izmantojiet maksājumu pārskata Excel faila SampleVendPaymWsReport2 izmainīto veidni.

