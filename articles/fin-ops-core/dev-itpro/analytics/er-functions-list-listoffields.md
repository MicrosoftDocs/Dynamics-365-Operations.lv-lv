---
title: LISTOFFIELDS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LISTOFFIELDS elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 0d51b59c437bd216c6d229546136bb604239fa92
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042002"
---
# <a name="LISTOFFIELDS">LISTOFFIELDS ER funkcija</a>

[!include [banner](../includes/banner.md)]

`LISTOFFIELDS` funkcija atgriež *Ierakstu saraksta* vērtību, kas tiek izveidota, pamatojoties uz norādītā *Uzskaitījuma* vai *Konteinera (ieraksta)* veida argumenta struktūru.

## <a name="syntax-1"></a>Sintakse 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Argumenti

`path`: Datu avota atsauce

Derīgs datu avota atsauces ceļš vienam no šādiem datu tipiem:

- Modeļa uzskaitījums
- Formāta uzskaitījums
- Lietojumprogrammu uzskaitījums
- Konteiners (ieraksts)

`language`: *Virkne*

Teksts, kas apzīmē valodas kodu.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Izveidotajā sarakstā ietverti ieraksti ar tālāk norādītajiem laukiem.

- **Nosaukums** (datu veids *Virkne*)
- **Marķējums** (datu veids *Virkne*)
- **Apraksts** (datu veids *Virkne*)
- **Istranslated** (*Būla* datu tips)

Ja `path` arguments attiecas uz datu avotu *Konteinera (ieraksta)* tipam katram atsauces konteinera ieraksta laukam, izveidotam sarakstam tiek pievienots jauns ieraksts. Katram izveidotam ierakstam laukā  **Nosaukums** tiek atgriezts tā konteinera ieraksta lauka nosaukums, kuram tika izveidots pašreizējais ieraksts.

Ja `path` arguments attiecas uz datu avotu vienam no *Uzskaitījuma* tipiem katrai atsauces uzskaitījuma vērtībai, izveidotam sarakstam tiek pievienots jauns ieraksts. Katram izveidotam ierakstam lauka **Nosaukums** vērtība atgriež atsauces tā uzskaitījuma vērtību, kas tika izveidots pašreizējam ierakstam, lauks **Apraksts** atgriež šī uzskaitījuma aprakstu, un lauks **Etiķete** atgriež šī uzskaitījuma etiķeti.

Izpildlaikā, izmantojot 1. sintaksi, laukiem **Etiķete** un **Apraksts** ir jāatgriež vērtības, kas ir balstītas uz valodas iestatījumiem elektronisko pārskatu (ER) formātā, kas ticis palaists:

- Ja ir pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz šo valodu, un lauks **IsTranslated** atgriež **True**.
- Ja nav pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz noklusējuma **EN-US** valodu un lauks **IsTranslated** atgriež **False**.

Izpildlaikā, izmantojot 2. sintaksi, laukiem **Etiķete** un **Apraksts** ir jāatgriež vērtības, kas ir balstītas uz valodu, kas ir definēta kā izsauktās funkcijas otrais arguments:

- Ja ir pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz šo valodu, un lauks **IsTranslated** atgriež **True**.
- Ja nav pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz **EN-US** valodu un lauks **IsTranslated** atgriež **False**.

## <a name="example-1"></a>1. piemērs

Tālāk esošajā attēlā ir parādīts ER datu modelī ieviests uzskaitījums.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.

- Modeļu uzskaitījums ir ievietots pārskatā kā datu avots.
- ER izteiksme modeļu uzskaitījumu izmanto kā funkcijas `LISTOFFIELDS` parametru.
- *Ierakstu saraksta* tipa datu avots tiek ievietots pārskatā, izmantojot izveidoto ER izteiksmi.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Tālāk esošajā piemērā parādīti ER formāta elementi, kas ir piesaistīti datu avotam ar *Ierakstu saraksta* tipu, kas tika izveidots, izmantojot funkciju `LISTOFFIELDS`

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Atbilstoši formāta vecākelementu **FILE** un **FOLDER** valodas iestatījumiem etiķešu un aprakstu tulkotais teksts tiek ievadīts ER formāta izvadē.

## <a name="example-2"></a>2. piemērs

Jūs izmantojat datu avota tipu *Aprēķinātais*, lai konfigurētu datu modeļu uzskaitījuma **enumType** datu avotus **enumType\_de** un **enumType\_deCH**.

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

Šajā gadījumā varat izmantot tālāk norādīto izteiksmi, lai iegūtu uzskaitījuma vērtības etiķeti Šveices vācu valodā, ja šāds tulkojums ir pieejams. Ja Šveices vācu valodas tulkojums nav pieejams, etiķete ir Vācu.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)
