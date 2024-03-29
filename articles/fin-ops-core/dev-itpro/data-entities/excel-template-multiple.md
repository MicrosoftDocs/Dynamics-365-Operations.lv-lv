---
title: Datu veidnes ar vairākām darblapām
description: Šajā rakstā ir aprakstīts, kā finansēs un operācijās importēt datus, izmantojot Excel datu elementu veidnes.
author: peakerbl
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: f0845b111afb18205677b885c91fe1585b24ab14
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108812"
---
# <a name="data-templates-with-multiple-worksheets"></a>Datu veidnes ar vairākām darblapām

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Datu pārvaldība programmā atbalsta Microsoft Excel-datu elementu veidnes. Šajās veidnēs var būt viena vai vairākas darblapas. Veidnes ar vairākām darblapām bieži tiek izmantotas, kad ir vēlams datus pārvaldīt vienā failā un to importēt vairākos datu elementos. Kā piemēru varētu minēt vietas un noliktavas.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Faila augšupielādēšana vienu reizi un kartēšana uz visiem elementiem
Apskatīsim piemēru, kur vienā Excel failā ir darblapas ar nosaukumu **Vietas** un **Noliktavas**. Lai iestatītu datu importēšanas projektu, jūs pievienotu pirmo datu elementu, **Vietas**, un pēc tam augšupielādētu šo failu. Kā šim elementam izmantojamo darblapu varat atlasīt **Vietas**.

Ja pievienojat otro elementu, **Noliktavas**, neaizverot formu **Pievienot failu**, darblapas uzmeklēšana jums ļauj atlasīt darblapu **Noliktavas** bez nepieciešamības šo failu augšupielādēt vēlreiz. Vienīgais iemesls augšupielādēt jaunu failu būtu tad, ja dati **Noliktavas** atrastos citā failā.

![Vairākas darblapas.](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Darblapas norādīšana elementa kartēšanai

Darblapas kartēšanu uz kādu datu elementu importēšanas darbā var norādīt no režģa. Režģa kolonnā **Darblapa** tiek rādītas darblapas no faila, kurš tika kartēts. Nolaižamajā izvēlnē varat izvēlēties citu darblapu. Ja izvēlētā darblapa jau tiek kartēta uz kādu elementu datu projektā, sistēma jums lūdz apstiprināt šīs izmaiņas. Ieteicams norādīt visus kartējumus režģī.

![Darblapas kartējuma atjaunināšana.](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Pārkartēšana uz jaunu failu

Gadījumos, kad kādā datu projektā esošiem elementiem ir nepieciešams augšupielādēt tā paša faila jaunu versiju vai pilnīgi jaunu failu, jums ir jālieto funkcionalitāte **Pievienot failu** un jāpievieno šie elementi vēlreiz, it kā tie tiktu pievienoti pirmo reizi. Pirms turpināšanas sistēma pārliecināsies, vai vēlaties pārrakstīt esošos elementus datu projektā. Elementi, kas netiek pievienoti vēlreiz (vai pārrakstīti), turpina izmantot iepriekšējos kartējumus no iepriekšējā faila.

## <a name="upload-a-file-using-run-project"></a>Faila augšupielādēšana, izmantojot opciju Palaist projektu

Varat augšupielādēt Excel failu, kamēr izmantojat opciju **Palaist projektu**, lai izpildītu importēšanas projektu. Uzmanieties, lai augšupielādētu tikai failus, kuros ir tādas pašas darblapas kā esošajiem kartējumiem uz datu elementiem datu projektā. Ja no jauna augšupielādētajā failā kāda darblapa netiek atrasta, sistēma parāda kļūdas ziņojumu un pārtrauc importēšanu. Ja kādam elementam ir jāmaina kartēšana uz darblapu, tad kartējumi datu projektā vispirms ir jāatjaunina no datu projekta, un tikai pēc tam šo failu var izmantot funkcionalitātē **Palaist projektu**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

