---
title: Elektronisko pārskatu veidošanas formātu modificēšana, atkārtoti lietojot Excel veidnes
description: Šajā rakstā ir aprakstīts, kā modificēt elektronisko pārskatu (ER) formātu, kas tiek izmantots biznesa dokumentu ģenerēšanai, atkārtoti izmantojot modificētu Excel veidni.
author: NickSelin
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50b115448bc89bba7e9abeb8062d03d31a163b64
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906736"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Elektronisko pārskatu veidošanas formātu modificēšana, atkārtoti lietojot Excel veidnes

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu veidošanas (ER) rīks tiek izmantots elektroniska formāta biznesa dokumentu ģenerēšanai. Ja vēlaties ģenerēt biznesa dokumentu, jums ir jāizveido ER formāta un pēc tam jāizmanto ER noformētājs, lai definētu biznesa dokumenta izkārtojumu un norādītu tajā ietveramos datus. Pēc tam varat izpildīt ER formātu, lai ģenerētu biznesa dokumentu.

ER rīku var izmantot biznesa dokumentu ģenerēšanai Microsoft Excel failu formātā. Kā šo dokumentu veidnes varat izmantot Excel dokumentus. Lai ER noformētājā definētu dokumenta izkārtojumu, varat definētajā ER formātā importēt tā Excel dokumenta saturu, ko vēlaties izmantot kā veidni. Lai saņemtu papildinformāciju un izmēģinātu šo scenāriju, atskaņojiet uzdevuma ceļvedi **Konfigurācijas noformēšana pārskatu ģenerēšanai OPENXML formātā (ER)** (daļa no 7.5.4.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)). Uzdevumu ceļveža darbībā, kur importējat Excel veidni, izmantojiet maksājuma pārskata Excel [faila SampleVendPaymWsReport sākotnējo veidni](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx).

Ja rediģējat Excel dokumentu, kas tiek izmantots kā biznesa dokumenta veidne, jauna ER funkcionalitāte sniedz iespēju ER formātam atkārtoti lietot atjaunināto veidni. Pēc tam ER formāts tiek atjaunināts atbilstoši atjauninātajai veidnei. Lai saņemtu papildinformāciju par šo funkcionalitāti, atskaņojiet uzdevuma ceļvedi **Formāta izmainīšana, atkārtoti lietojot Excel veidni (ER)** (daļa no 7.5.5.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10683)). Uzdevumu ceļveža darbībā, kur importējat atjauninātu veidni, izmantojiet modificēto veidni Maksājumu pārskata Excel [failam SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx).

## <a name="additional-resources"></a>Papildu resursi

[Veidnes atjaunināšana](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
