---
title: SPLIT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SPLIT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 4a42b0c7cfa2a8d3dcb7448224c9e88a48276f7d8cdbcce484383a778b8275a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757325"
---
# <a name="split-er-function"></a>SPLIT ER funkcija

[!include [banner](../includes/banner.md)]

`SPLIT` funkcija sadala norādīto ievades virkni apakšvirknēs un atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību.

## <a name="syntax-1"></a>Sintakse 1

```vb
SPLIT (input, length)
```

Šo sintaksi izmanto, lai norādīto ievades virkni sadalītu apakšvirknēs, katrai no kurām ir norādīts garums.

## <a name="syntax-2"></a>Sintakse 2

```vb
SPLIT (input, delimiter)
```

Šo sintaksi izmanto, lai norādīto ievades virkni sadalītu apakšvirknēs, pamatojoties uz norādīto norobežotāju.

## <a name="arguments"></a>Argumenti

`input`: *Virkne*

Sadalāmais teksts.

`length`: *Vesels skaitlis*

Vienas apakšvirknes maksimālais garums.

`delimiter`: *Virkne*

Norobežotājs, ko izmanto, lai atdalītu apakšvirknes.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Atgrieztā saraksta ieraksta struktūra sastāv no **Virknes** tipa *Vērtības* lauka. Katrā atgrieztā saraksta ierakstā ir šajā laukā ģenerētās apakšvirknes.

Ja `delimiter` arguments ir tukšs, tiek atgriezts jauns saraksts, kas sastāv no viena ieraksta, kurā ir **Virknes** veida lauks *Vērtība*. Šis lauks satur ievades tekstu.

Ja `input` arguments ir tukšs, tiek atgriezts jauns tukšs saraksts. Ja `input` vai `delimiter` arguments nav norādīts (ir tukšs), tiek parādīts programmas izņēmums.

## <a name="example-1"></a>1. piemērs

`SPLIT ("abcd", 3)` atgriež jaunu sarakstu, kas sastāv no diviem ierakstiem ar **Virknes** veida lauku *Vērtība*. Pirmā ieraksta lauks **Vērtība** ietver tekstu **"abc"**, un otrā ieraksta lauks **Vērtība** satur tekstu **"d"**.

## <a name="example-2"></a>2. piemērs

`SPLIT ("XAb aBy", "aB")` atgriež jaunu sarakstu, kas sastāv no trim ierakstiem ar **Virknes** veida lauku *Vērtība*. Laukam **Vērtība** pirmajā ierakstā ir teksts **"X"**, laukam **Vērtība** otrajā ierakstā ir teksts **"&nbsp;"**, un laukam **Vērtība** trešajā ierakstā ir teksts **"y"**. 

## <a name="example-3"></a>3. piemērs

Varat izmantot funkciju [INDEKSS](er-functions-list-index.md), lai piekļūtu atsevišķiem norādītās ievades virknes elementiem. Ja ievadāt datu avotu **MansSaraksts** tipam **Aprēķinātais lauks** un konfigurējiet tam izteiksmi `SPLIT("abc", 1)`, izteiksme `INDEX(MyList,2).Value` atgriež tekstu **b**.

## <a name="example-4"></a>4. piemērs

Funkcija [UZSKAITĪT](er-functions-list-enumerate.md) arī var palīdzēt piekļūt atsevišķiem norādītās ievades virknes elementiem. Ja vispirms ievadāt **Aprēķinātā lauka** tipa **MansSaraksts** datu avotu un konfigurējat tai izteiksmi `SPLIT("abc", 1)`, pēc tam ievadiet **Aprēķinātā lauka** tipa **UzskaitījumaSaraksts** datu avotu un konfigurējat to izteiksmei `ENUMERATE(MyList)`, izteiksme `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` atgriež tekstu **"b"**.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
