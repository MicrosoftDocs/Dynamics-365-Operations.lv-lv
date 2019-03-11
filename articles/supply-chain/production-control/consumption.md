---
title: Aprēķināt materiālu patēriņu
description: Šajā rakstā ir sniegta informācija par dažādām opcijām, kas ir saistītas ar materiālu patēriņa aprēķināšanu.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e4010b5abb6b5a871d098422f1489cb2db3a071
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "316192"
---
# <a name="calculate-material-consumption"></a>Aprēķināt materiālu patēriņu

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par dažādām opcijām, kas ir saistītas ar materiālu patēriņa aprēķināšanu. 

Tālāk ir norādītas ar materiālu patēriņa aprēķināšanu saistītās opcijas, kas ir pieejamas lapas **Materiālu komplekts** kopsavilkuma cilnes **Detalizēta informācija par rindu** cilnēs **Iestatīšana** un **Pakāpenisks patēriņš**.

## <a name="variable-and-constant-consumption"></a>Mainīgais un konstantais patēriņš
Laukā **Patēriņš ir** varat atlasīt, vai patēriņš ir jāaprēķina kā konstants vai kā mainīgs daudzums. Atlasiet vērtību **Konstante**, ja ražošanai ir nepieciešams fiksēts daudzums vai apjoms neatkarīgi no saražotā daudzuma. Atlasiet opciju **Mainīgais**, kas ir noklusējuma iestatījums, ja saražotajām precēm nepieciešamais materiāla daudzums ir proporcionāls saražoto preču daudzumam.

## <a name="calculating-consumption-from-a-formula"></a>Patēriņa aprēķināšana, izmantojot formulu
Laukā **Formula** varat iestatīt dažādas formulas materiālu patēriņa aprēķināšanai. Ja izmantojat noklusējuma vērtību **Standarta**, patēriņš netiek aprēķināts, izmantojot formulu. Tālāk ir norādītas ar laukiem **Augstums**, **Platums**, **Dziļums**, **Blīvums** un **Konstante** izmantotās formulas.

-   Augstums \* Konstante
-   Augstums \* Platums \* Konstante
-   Augstums \* Platums \* Dziļums \* Konstante
-   (Augstums \* Platums \* Dziļums / Blīvums) \* Konstante

## <a name="rounding-up-and-multiples"></a>Noapaļošana un dalītājs
Kopā izmantojot laukus **Noapaļošana** un **Dalītājs**, varat noapaļot materiālu patēriņa vērtību. Piemēram, varat noapaļot vērtību atbilstoši materiālu apstrādes vienībai, kur ražošanai tiek izdots izejmateriāls. Ir pieejamas šādas lauka **Noapaļošana** opcijas: **Daudzums**, **Mērījums** un **Patēriņš**.

### <a name="quantity"></a>Daudzums

Ja atlasāt opciju **Daudzums** kā noapaļošanas mehānismu, daudzumam ir jābūt norādītā daudzuma dalītājam. Piemēram, ja ir nepieciešams vesels skaitlis, laikā **Dalītājs** atlasiet vērtību **1**. Pēc tam skaitļi tiek noapaļoti līdz daudzumam, kas dalās ar 1.

### <a name="measurement"></a>Mērījums

Noapaļošanas mehānisms **Mērījums** parasti tiek atlasīts, ja izejmateriālam ir konkrēti izmēri. Piemēram, saražotajai precei ir nepieciešams 2 metrus garš metāla caurules posms un metāla caurule ir pieejama 4,5 metrus garos gabalos. Šādā gadījumā var izmantot noapaļošanas mehānismu **Mērījums**, lai aprēķinātu, cik metāla cauruļu ir nepieciešams noteiktam saražoto preču skaitam. Šajā piemērā laukam **Formula** ir iestatīta vērtība **Augstums \* Konstante**. Laukam **Augstums** ir iestatīta vērtība **2**, lai norādītu pabeigtajai precei nepieciešamo caurules garumu. Ir iestatīta lauka **Dalītājs** vērtība **4,5**, lai norādītu, ka caurule tiek izdota 4,5 metrus garos gabalos. Tālāk ir norādīts aprēķins.

1.  Dalītāju skaits, kas ir nepieciešams 10 saražotām precēm: 10 ÷ 2 = 5 gab
2.  Kopējais patēriņš: 4,5 x 5 = 22,5 metri metāla caurules

Tiek pieņemts, ka uz katriem pieciem patērētajiem metāla caurules gabaliem tiek norakstīti 0,5 metri caurules.

### <a name="consumption"></a>Patēriņš

Noapaļošanas mehānisms **Patēriņš** parasti tiek atlasīts, ja izejmateriāls tiek izdots veselos noteiktas preces materiālu apstrādes vienības daudzumos. Piemēram, saražotajai precei ir nepieciešamas 2 kvartas krāsas un krāsa tiek izdota 25 kvartu bundžās. Šādā gadījumā var izmantot noapaļošanas mehānismu **Patēriņš**, lai noapaļotu patēriņu līdz veselam 25 kvartu bundžu skaitam. Tālāk ir norādīts, kā tiek aprēķināts krāsas daudzums, kas ir nepieciešams 180 saražotajām precēm.

1.  Nepieciešamā krāsa, neieskaitot brāķi: 180 × 2 = 360 kvartas
2.  Bundžu skaits: 360 ÷ 25 = 14,4, kas tiek noapaļots līdz 15
3.  Nepieciešamā krāsa, ieskaitot brāķi: 15 × 25 = 375 kvartas

## <a name="step-consumption"></a>Pakāpenisks patēriņš
Pakāpenisks patēriņš tiek izmantots, lai aprēķinātu konstantu patēriņu daudzuma intervālos. Ja cilnes **Iestatījumi** laukā **Formula** atlasāt **Pakāpenisks patēriņš**, tad varat pievienot informāciju par darbībām cilnē **Pakāpenisks patēriņš**. Fiksēto patērēto daudzumu var iestatīt saražotā daudzuma intervālos. Piemēram, pakāpenisks patēriņš tiek iestatīts, kā tas ir redzams tālāk esošajā tabulā.

| No sērijas | Daudzums |
|-------------|----------|
| 0,00        | 10,0000  |
| 100,00      | 20,0000  |
| 200,00      | 40,0000  |

Materiālu komplekta (MK) daudzums ir 1, un ražošanas daudzums ir 110 Patēriņa aprēķināšanas formula ir No sērijas (daudzums) = Patēriņš. Tā kā ražošanas daudzums ir 110, tas ietilpst grupā Sērija no 100. Tāpēc daudzums ir 20.



