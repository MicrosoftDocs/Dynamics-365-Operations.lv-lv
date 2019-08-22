---
title: Pamatlīdzekļu nolietojuma konvencijas
description: Šajā tēmā ir sniegts pārskats par pamatlīdzekļu nolietojuma konvencijām.
author: saraschi2
manager: AnnBe
ms.date: 03/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad44282de9d999aa211548601eb416f4bdba2047
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840773"
---
# <a name="fixed-asset-depreciation-conventions"></a>Pamatlīdzekļu nolietojuma konvencijas

[!include [banner](../includes/banner.md)]

Nolietojuma konvencijas tiek izmantotas, lai noteiktu, kad un kā tiek aprēķināts nolietojums gan par gadu, kad pamatlīdzeklis ir iegādāts, gan par gadu, kad pamatlīdzeklis tiek izslēgts.

Nolietojuma konvencijas var piešķirt pamatlīdzekļu grupas grāmatas iestatīšanai. Lai skatītu vai piešķirtu nolietojuma aprēķināšanas metodi, pamatlīdzekļu iestatīšanas apgabalā atlasiet **Pamatlīdzekļu** grupas. Atlasiet pogu **Grāmatas**. Šajā gadījumā piešķirtās nolietojuma konvencijas tiek izmantotas kā noklusējuma vērtības, veidojot pamatlīdzekļu grāmatas. Nolietojuma konvencijas var iestatīt arī atsevišķā pamatlīdzekļu grāmatā. Lai to izdarītu, atlasiet vienumu **Grāmatas** pamatlīdzekļu iestatīšanas apgabalā un pēc tam atlasiet pogu **Pamatlīdzekļu grupas**.


|  Nolietojuma aprēķināšanas metode  |   Apraksts  |
|---------------------------|-----------------|
|           Nav            |  Pamatlīdzekļiem sāk aprēķināt nolietojumu datumā <strong>Nodots lietošanā</strong>.|
|         Pusgads         |  Atskaitiet pusgada nolietojumu gan pirmajā, gan pēdējā gadā, kurā tiek rēķināts īpašuma nolietojums. Atskaitiet gada nolietojumu katrā otrajā gadā atkopšanas perioda laikā. |
|        Pilns mēnesis         | Pamatlīdzekļiem, kuriem datums <strong>Nodots lietošanā</strong> ir mēneša ietvaros, sāk rēķināt nolietojumu attiecīgā mēneša pirmajā datumā. Pamatlīdzekļi, kas ir norakstīti mēneša ietvaros, uzskatāmi par norakstītiem nolietojuma vajadzībām iepriekšējā mēneša pēdējā dienā.  |
|        Puse ceturkšņa        | Lai aprēķinātu nolietojuma atskaitījumus par gadu, kad īpašums nodots ekspluatācijā, reiziniet visa gada nolietojumu ar tāda ceturkšņa procentuālo vērtību, kad īpašums nodots ekspluatācijā, kā norādīts tabulā.<table><thead><tr><th>Ceturksnis</th><th>Procenti</th></tr></thead><tbody><tr><td>Pirmais</td><td>87,5</td></tr><tr><td>Otrā</td><td>62,5</td></tr><tr><td>Trešā</td><td>37,5</td></tr><tr><td>Ceturtā</td><td>12,5</td></tr></tbody></table>Izslēgšanas ceturksnī (vai pilnīga nolietojuma ceturksnī) tiek ņemts vērā pusceturkšņa nolietojums. |
| Puse mēneša (mēneša 1. datums)  | Pamatlīdzekļiem, kuriem datums <strong>Nodots lietošanā</strong> ir pirmajā mēneša pusē (no 1. līdz 15. datumam), sāk aprēķināt nolietojumu tāda mēneša pirmajā datumā, kurā ir datums <strong>Nodots lietošanā</strong>. Pamatlīdzekļiem, kuriem datums <strong>Nodots lietošanā</strong> ir otrajā mēneša pusē (no 16. datuma līdz mēneša beigām), sāk aprēķināt nolietojumu tāda mēneša pirmajā datumā, kurš ir pēc datuma <strong>Nodots lietošanā</strong>. Pamatlīdzekļi, kas ir norakstīti mēneša pirmajā pusē (no 1. līdz 15. datumam), uzskatāmi par norakstītiem nolietojuma vajadzībām iepriekšējā mēneša pēdējā dienā. Pamatlīdzekļi, kas ir norakstīti mēneša otrajā pusē (no 16. datuma līdz mēneša beigām), uzskatāmi par norakstītiem nolietojuma vajadzībām norakstīšanas mēneša pēdējā dienā. |
| Puse mēneša (mēneša 15. datums) |  Lai aprēķinātu nolietojuma atskaitījumus par gadu, kad īpašums nodots ekspluatācijā, reiziniet visa gada nolietojumu ar daļskaitli. Minētā daļskaitļa skaitītājs (augšējais skaitlis) ir pilno mēnešu skaits gadā, kurā īpašums ir lietošanā, pieskaitot 1/2 jeb (0,5). Saucējs (apakšējais skaitlis) ir 12. Ja īpašums tiek izslēgts pirms atkopšanas perioda beigām, izmantojiet tādu pašu metodi, lai aprēķinātu nolietojuma atskaitījumus par gadu, kurā veikta izslēgšana.   |
| Pusgads (gada sākums) | Pamatlīdzekļiem, kuriem datums <strong>Nodots lietošanā</strong> ir gada pirmajā pusē, sāk aprēķināt nolietojumu gada (pilnā gada) pirmajā dienā. Pamatlīdzekļiem, kuriem datums <strong>Nodots lietošanā</strong> ir gada otrajā pusē, sāk aprēķināt nolietojumu gada (pilnā gada) viduspunktā.|
|   Puse gada (nākamais gads)   |   Pamatlīdzekļiem, kuriem datums <strong>Nodots lietošanā</strong> ir gada pirmajā pusē, sāk aprēķināt nolietojumu gada (pilnā gada) pirmajā dienā. Pamatlīdzekļiem, kuriem datums <strong>Nodots lietošanā</strong> ir gada otrajā pusē, sāk aprēķināt nolietojumu nākamā gada pirmajā dienā. Pamatlīdzekļi, kas ir norakstīti gada pirmajā pusē, uzskatāmi par norakstītiem nolietojuma vajadzībām iepriekšējā gada pēdējā dienā. Nolietojums, kas grāmatots pašreizējā gadā, ir jāstornē vai jākoriģē. Pamatlīdzekļi, kas ir norakstīti otrajā gada pusē, uzskatāmi par norakstītiem nolietojuma vajadzībām norakstīšanas gada pēdējā dienā.|

