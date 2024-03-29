---
title: Ģenerēto XML failu sadalīšana, pamatojoties uz faila lielumu un satura daudzumu
description: Šajā rakstā ir sniegta informācija par to, kā sadalīt ģenerētos failus, pamatojoties uz faila lielumu un satura krājuma daudzumu.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 5347d4e85198893dd94f14508176db93ccd47c22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280101"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Ģenerēto XML failu sadalīšana, pamatojoties uz faila lielumu un satura daudzumu

[!include[banner](../includes/banner.md)]

Varat noformēt elektronisko pārskatu (Electronic Reporting — ER) formātus, lai izejošos dokumentus ģenerētu XML formātā. Reizēm šos dokumentus var pieņemt tikai tad, ja tie atbilst noteiktiem kritērijiem, piemēram, maksimālajam faila lielumam vai maksimālajam noteiktu XML zaru skaitam. Varat noformēt ER formātus tā, lai ģenerētu elektroniskos dokumentus, kas atbilst šo dokumentu saņēmēju norādītajām prasībām.

- FILE formāta elementam varat definēt faila lieluma ierobežojumu kā ER izteiksmi. Ja ER pārskata ģenerēšanas laikā definētais ierobežojums tiek pārsniegts, ER beidz veidot pašreizējo failu un pēc tam pāriet pie nākamā faila veidošanas.
- Ikvienam XML ELEMENT formātam elementu skaita ierobežojumu varat definēt kā ER izteiksmi. Ja ģenerētajā failā XML zaru skaits pārsniedz definēto ierobežojumu, kad tiek palaists ER pārskats, ER beidz veidot pašreizējo failu un pēc tam pāriet pie nākamā faila veidošanas.
- Ikvienam XML SEQUENCE formāta elementam bērnelementu skaita ierobežojumu varat definēt kā ER izteiksmi. Ja ģenerētajā failā formāta elementa ligzdoto XML zaru skaits pārsniedz definēto ierobežojumu, kad tiek palaists ER pārskats, ER beidz veidot pašreizējo failu un pēc tam pāriet pie nākamā faila veidošanas.
- Jebkuru XML ELEMENT formāta elementu varat atzīmēt kā nedalāmu. Tādējādi formāta elementā ģenerētos XML zaru ligzdotos elementus varat paturēt vienā ģenerētajā failā.

Lai ģenerētajam failam pievienotu XML zarus, papildus XML ELEMENT un XML SEQUENCE formāta elementu lietošanai varat izmantot RAW XML formāta elementu. Taču zari, ko pievienojat, izmantojot RAW XML formāta elementu, netiek ņemti vērā, kad tiek aprēķināts zaru skaits, lai novērtētu elementu skaita ierobežojumus.

Ja konfigurējat failu galamērķus FILE formāta elementam, kas ir konfigurēts ģenerētās izvades sadalīšanai katru reizi, kad tiek pārsniegti noteikti ierobežojumi, katra ģenerētās izvades daļa tiek nosūtīta uz konfigurētā faila galamērķi kā atsevišķs fails. Lai piešķirtu unikālu nosaukumu failiem, kas tiek izveidoti, sadalot izvadi, jums ir jākonfigurē ER izteiksme FILE formāta elementam. Ja ietverat ER datu avotu ar tipu NUMBER SEQUENCE, numuru sērija pieaug katrai sadalītās izvades daļai.

Lai par šo līdzekli uzzinātu vairāk, noskatieties uzdevuma ceļvedi **ER XML failu sadalīšana, pamatojoties uz faila lielumu vai satura vienumu daudzumu**, kas veido daļu no biznesa procesa **7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)** un ko var lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684). Šajā uzdevumu ceļvedī ir izklāstīts ER formāta konfigurēšanas process, lai sadalītu ģenerētos failus, pamatojoties uz faila lieluma un satura vienumu daudzuma ierobežojumiem. Lai izpildītu šo uzdevuma ceļvedi, jums ir nepieciešams lejupielādēt tālāk norādītos failus.

- [ER modeļa konfigurācija — XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [ER formāta konfigurācija — XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>Papildu resursi
[Elektronisko pārskatu (ER) galamērķi](electronic-reporting-destinations.md)

[Formulas veidotājs elektronisko pārskatu veidošanā (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
