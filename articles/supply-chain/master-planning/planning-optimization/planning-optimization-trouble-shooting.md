---
title: Plānošanas optimizācijas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar plānošanas optimizāciju.
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2100235fadabe6af87849aab7d9ec55d85ea66fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812887"
---
# <a name="troubleshoot-planning-optimization"></a>Plānošanas optimizācijas problēmu novēršana 

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot tipiskas problēmas, kas var rasties, strādājot ar plānošanas optimizāciju.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Plānošanas optimizācijas pievienojumprogrammas instalēšana nav pabeigta

Plānošanas optimizācijas prasība ir Lifecycle Services (LCS) iespējota, augstas pieejamības vide, 2. līmeņa vai augstāka, (ne OneBox vide) ar Dynamics 365 Supply Chain Management versiju 10.0.7 vai jaunāku. Mēģinot instalēt pievienojumprogrammu OneBox vidē, instalēšana netiks pabeigta.

**Labojums**: atceliet instalēšanu un izmantojiet augstas pieejamības vidi, 2. vai augstāku līmeni (ne OneBox vidi).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Neizdodas pakešuzdevumu plānošana, ja ir iespējota plānošanas optimizācija

Iespējojot plānošanas optimizāciju, iebūvētā vispārējās plānošanas programma tiek automātiski atspējota. Vispārējās plānošanas pakešuzdevumi, kas tika izveidoti iebūvētajam Supply Chain Management plānošanas dzinējam, neizdosies, ja tie tiks aktivizēti plānošanas optimizācijas iespējošanas laikā. Var tikt parādīts kļūdas ziņojums, piemēram, *Šī operācija izraisīja vispārējo plānošanu, kas netiek atbalstīta, ja ir iespējota plānošanas optimizācija*.

**Labojums**: atceliet visus vispārējās plānošanas pakešuzdevumus, kas tika izveidoti iebūvētajam Supply Chain Management plānošanas dzinējam.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Plānošanas optimizācijas rezultāti atšķiras no iepriekšējiem rezultātiem

Plānošanas optimizācija dažās jomās atšķiras no iebūvētā vispārējās plānošanas projekta. To var izraisīt arī vēl nepabeigtas funkcijas.

**Labojums**: palaist plānošanas optimizācijas saderības analīzi un pēc tam analizēt rezultātus, vienlaikus atsaucoties uz saistīto dokumentāciju, lai izprastu ietekmi. Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Nevar iespējot plānošanas optimizāciju

**Savienojuma statusam** ir jābūt **Savienots** pirms varat iestatīt **Izmantot plānošanas optimizāciju** uz **Jā**. Papildinformāciju skatiet [Sākt darbu ar Plānošanas optimizāciju ](get-started.md).

**Labojums**: pārliecinieties, ka plānošanas optimizācijas pievienojumprogramma ir veiksmīgi instalēta.

## <a name="error-message-is-shown-during-ctp"></a>CTP laikā tiek rādīts kļūdas ziņojums

Ja ir iespējota plānošanas optimizācija, mēģinot palaist pieejams iegādei (CTP) no pārdošanas pasūtījuma, tiks parādīts šāds kļūdas ziņojums: *Šī operācija izraisīja vispārējo plānošanu, kas netiek atbalstīta, ja ir iespējota plānošanas optimizācija*.

Tas ir saistīts ar nepabeigtu funkciju, kas tiek plānota kā daļa no ražošanas pasūtījumu atbalsta.

**Labojums:** izvairieties no CTP aprēķiniem, kad ir iespējota plānošanas optimizācija, līdz ir pieejams CTP atbalsts.

## <a name="additional-resources"></a>Papildu resursi

[Darba sākšana ar plānošanas optimizāciju](get-started.md)

[Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]