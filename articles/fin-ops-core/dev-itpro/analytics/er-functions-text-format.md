---
title: FORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09efeb6b5d8bd2ea452dbf7a9ddaeec2ab75c92
ms.sourcegitcommit: 0455a024185f79ecb82df61e6d994bd71dee5c10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/20/2020
ms.locfileid: "2974296"
---
# <a name="FORMAT">FORMAT ER funkcija</a>

[!include [banner](../includes/banner.md)]

`FORMAT` funkcija atgriež norādīto virkni kā *Virknes* vērtību, kas ir formatēta, aizstājot argumentu **%N** ar argumentu *N*.

## <a name="syntax"></a>Sintakse

```
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Argumenti

`string`: *Virkne*

Atsauce uz datu avotu *Virknes* datu tipam, kas ir jāformatē. Šis arguments ir obligāts.

`argument 1`: *Virkne*

Pirmais arguments, kas tiek izmantots, lai aizstātu gadījumus **%1**. Šis arguments ir obligāts.

`argument N`: *Virkne*

*N*-tais arguments, kas tiek izmantots, lai aizstātu gadījumus **%2**, **%3** un tā tālāk. Šie papildu argumenti nav obligāti.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Ja arguments parametram nav norādīts, šis parametrs virknē tiek atgriezts kā **"%N"**. Vērtībām ar tipu *Reāls* noklusējuma virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.

## <a name="example"></a>Paraugs

Tālāk esošajā attēlā ir redzams, ka **PaymentModel** datu avots atgriež klientu ierakstu sarakstu, izmantojot **Debitora** komponentu. Tas atgriež vērtību apstrādes datums, izmantojot lauku **ProcessingDate**.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

Elektronisko pārskatu (ER) formātā, kas ir izveidots tā, lai ģenerētu elektronisku failu noteiktiem debitoriem, vienums **PaymentModel** ir atlasīts kā datu avots, un tas kontrolē procesa plūsmu. Lietotājiem tiek parādīts izņēmums, lai viņus informētu, ja atlasītais debitors tiek apturēts datumam, kad atskaite tiek apstrādāta. Šāda tipa apstrādes kontrolei izveidotā formulā var izmantot šādus resursus:

- Etiķete SYS70894, kurā ir šāds teksts:

    - **Valodai EN-US:** "Nothing to print"
    - **Valodai DE:** "Nichts zu drucken"

- Etiķete SYS18389, kurā ir šāds teksts:

    - **EN-US valodai:** "Customer %1 is stopped for %2."
    - **DE valodai:** "Debitor '%1' wird für %2 gesperrt."

Lūk, kādu izteiksmi varat izveidot.

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Ja pārskats debitoram **Litware Retail** tiek apstrādāts 2015. gada 17. decembrī kultūrā **EN-US** un valodā **EN-US**, šī formula atgriež tālāk norādīto tekstu, kurš lietotājam var tikt rādīts kā izņēmuma ziņojums.

*Nothing to print.. Customer Litware Retail is stopped for 12/17/2015."*

Ja tas pats pārskats debitoram **Litware Retail** tiek apstrādāts 2015. gada 17. decembrī kultūrā **DE** un valodā **DE**, šī formula atgriež tālāk norādīto tekstu, kurā tiek izmantots cits datuma formāts.

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> ER formulās etiķetēm tiek lietota tālāk norādītā sintakse.
>
> - **Etiķetēm no Microsoft Dynamics 365 Finance programmas resursiem:** **\@X**, kur **X** ir etiķetes ID lietojumprogrammas objektu kokā (AOT)
> - **Etiķetēm, kas ir ietvertas ER konfigurācijās:** **@"GER_LABEL:X"**, kur **X** ir etiķetes ID ER konfigurācijā

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)
