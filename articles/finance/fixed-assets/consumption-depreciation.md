---
title: Patēriņa nolietojuma aprēķins
description: Šajā rakstā ir sniegts pārskats par nolietojuma patēriņa metodi.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a11389d1042eb62ed081d7615fea2f370de8255
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827006"
---
# <a name="consumption-depreciation"></a>Patēriņa nolietojuma aprēķins

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par nolietojuma patēriņa metodi.

Ja iestatāt nolietojuma tabulu pamatlīdzekļiem un atlasāt opciju **Patēriņš** laukā **Metode**, kurš atrodas lapā **Nolietojuma tabulas**, tad pamatlīdzekļi tiek piešķirti nolietojuma tabulai, pamatojoties uz to lietojumu. Jums nav jāiestata procentuālais daudzums un intervāli lapā **Nolietojuma tabulas**. Kad ir izveidota nolietojuma tabula, kas izmanto metodi Patēriņš, šo metodi varat iestatīt dažādos veidos.

## <a name="set-up-and-use-consumption-depreciation"></a>Patēriņa nolietojuma iestatīšana un lietošana
1.  Lapā **Nolietojuma tabulas** izveidojiet nolietojuma tabulu. Patēriņa aprēķināšanai nolietojuma tabulā ir jābūt iekļautam ID un nosaukumam, un ir jābūt atlasītam vienumam **Patēriņš** laukā **Metode**.
2.  Lapā **Patēriņa koeficienti** iestatiet patēriņa koeficientus. Katram patēriņa koeficientam ir nepieciešams ID un nosaukums, kā arī patēriņa koeficients, kas ir norādīts kā daudzums vai kā procenti.
3.  Lapā **Patēriņa vienības** iestatiet patēriņa vienības. Katrai patēriņa vienībai ir nepieciešams ID un nosaukums. Nolietojuma vienības tiek izmantotas, lai aprēķinātu patēriņa nolietojumu lapā **Patēriņa nolietojums**. Vienību piemēri ir kilometrs (km), kilograms (kg) un stunda.
4.  Lapā **Pamatlīdzekļi** iestatiet atsevišķus pamatlīdzekļus. Katram pamatlīdzeklim atlasiet vērtības modeļus un nolietojuma grāmatas, kurām ir nolietojuma tabulas. Patēriņa nolietojumam jums ir jāiestata vērtības modeļi vai nolietojuma grāmatas, ja kādam no jūsu pamatlīdzekļiem tiek lietotas tādas nolietojuma tabulas, kas ir balstītas uz metodi Patēriņš. Šis iestatījums tiek veikts vai nu cilnē **Nolietojums**, lapā **Vērtības modeļi**, vai kopsavilkuma cilnē **Vispārīgi**, lapā **Nolietojuma tabula**. Vairākiem pamatlīdzekļiem varat izvēlēties vienu un to pašu vērtības modeli. Nolietojuma tabulas ir katram pamatlīdzeklim atlasītā vērtības modeļa vai nolietojuma grāmatas daļa. Nolietojuma tabulas nevar pievienot vai modificēt tieši lapā **Pamatlīdzekļi**. Nolietojuma tabulas varat modificēt tikai lapā **Nolietojuma grāmatas**.
5.  Lapā **Vērtības modeļi** vai lapā **Nolietojuma grāmatas**, lauku grupā **Patēriņa nolietojums** ierakstiet informāciju tālāk uzskaitītajos laukos.
    -   Patēriņa koeficients
    -   Vienība
    -   Vienības nolietojums
    -   Aprēķinātais patēriņš

    Laukā **Grāmatotais patēriņš** tiek rādīts patēriņa nolietojums tādās vienībās, kas jau ir grāmatotas pamatlīdzekļa un vērtības modeļa kombinācijai vai nolietojuma grāmatai. Vērtību šajā laukā nevar manuāli atjaunināt.

## <a name="examples"></a>Piemēri
### <a name="example-1"></a>1. piemērs

Šāds patēriņa faktors ir iestatīts 31. janvārī:

-   Daudzums ir 1000.
-   Pamatlīdzeklim norādītā vienības nolietojuma cena ir 1,5.

Nolietojuma priekšlikums 31. janvārī ir šāds: Daudzums × Vienības nolietojums 1000 × 1,5 = 1500 Ja šim pamatlīdzeklim norādītais koeficients ir procentuāls koeficients, tad daudzums, kas tiek prognozēts laukā **Aprēķinātais patēriņš** attiecībā uz pamatlīdzekļa vērtības modeli, tiek reizināts ar procentiem, kuri ir iestatīti atlasītajam beigu datumam. Pēc tam iegūtais daudzums tiek piedāvāts kā nolietojuma daudzums attiecīgajam periodam.

### <a name="example-2"></a>2. piemērs

31 janvārim patēriņa nolietojumam tiek iestatīts tālāk norādītais patēriņa koeficients.

-   Procentuālais daudzums ir 10 procenti.
-   Pamatlīdzeklim norādītā vienības nolietojuma cena ir 1,5.
-   Pamatlīdzekļa novērtētais daudzums ir 2000.

Nolietojuma priekšlikums 31. janvārī ir šāds: Novērtētais daudzums × Procenti × Vienības nolietojums 2000 × 0,10 × 1,5 = 300





[!INCLUDE[footer-include](../../includes/footer-banner.md)]