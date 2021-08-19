---
title: FIRST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FIRST elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: f108676c2ff8801fddc0a72be3f75d212582efe6b5d96f7515354739eb446532
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740994"
---
# <a name="first-er-function"></a>FIRST ER funkcija

[!include [banner](../includes/banner.md)]

`FIRST` funkcija atgriež norādītā saraksta pirmo ierakstu kā vērtību *Konteiners (ieraksts)*, ja šis saraksts nav tukšs. Ja saraksts ir tukšs, šī funkcija rādīs izņēmumu.

## <a name="syntax"></a>Sintakse

```vb
FIRST (list)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Konteiners (ieraksts)*

Iegūtā ieraksta vērtība.

## <a name="example-1"></a>1. piemērs

Izteiksme `FIRST(SPLIT("ABC",1)).Value` atgriež teksta vērtību **"A".**

## <a name="example-2"></a>2. piemērs

Izteiksme `FIRST(SPLIT("",1)).Value` izpildlaikā rāda izņēmumu.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]