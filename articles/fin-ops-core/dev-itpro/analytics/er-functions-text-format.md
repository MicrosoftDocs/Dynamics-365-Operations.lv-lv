---
title: FORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dbde3ebfd2670639a2fff19d83ea9bd8d15c22b09b43ab49ae1b9e35562625a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720884"
---
# <a name="format-er-function"></a>FORMAT ER funkcija

[!include [banner](../includes/banner.md)]

`FORMAT` funkcija atgriež norādīto virkni kā *Virknes* vērtību, kas ir formatēta, aizstājot argumentu **%N** ar argumentu *N*.

## <a name="syntax"></a>Sintakse

```vb
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

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]