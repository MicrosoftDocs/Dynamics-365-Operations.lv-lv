---
title: ALLITEMS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ALLITEMS elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/04/2019
ms.topic: article
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
ms.openlocfilehash: 5ddcf989bdfd1d1f5d0a412a2ffefe0e3037ca79
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746727"
---
# <a name="allitems-er-function"></a>ALLITEMS ER funkcija

[!include [banner](../includes/banner.md)]

`ALLITEMS` funkcija darbojas kā atmiņas izvēle un atgriež jaunu izplātu *Ierakstu saraksta* vērtību kā ierakstu sarakstu, kas attēlo visus vienumus, kuri atbilst norādītajam ceļam.

## <a name="syntax"></a>Sintakse

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Argumenti

`path`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šis ceļš ir jādefinē kā derīgs datu avota ceļš datu avota elementam ar *Ierakstu saraksta* datu tipu. Tādiem datu elementiem kā ceļa virkne un datums elektronisko pārskatu (ER) izteiksmju veidotājā veidošanas laikā ir jāizraisa kļūda.

Nav ieteicams izmantot šo funkciju transakciju datu avotiem, kas var saturēt lielu datu apjomu. Tā vietā apsveriet iespēju izmantot funkciju [ALLTEMSQUERY](er-functions-list-allitemsquery.md).

## <a name="example-1"></a>1. piemērs

Ja `SPLIT("abcdef" , 2)` ievadāt kā datu avotu **DS**, izteiksme `COUNT( ALLITEMS (DS))` atgriež **3.**

## <a name="example-2"></a>2. piemērs

Ja ievadāt **Vend** kā datu avotu *Ierakstu saraksta* datu tipam, kas attiecas uz lietojumprogrammas tabulu VendTable, izteiksme `ALLITEMS (Vend.'<Relations'.ContactPerson)` atgriež saplātu ierakstu sarakstu, kam ir tabulas **ContactPerson** struktūra, un tajā ir visas kontaktpersonas, kurām var piekļūt, izmantojot **ContactPerson. contactforparty = = VendTable. Party** relāciju, un kuras ir pieejamas visiem kreditoriem no kreditoru atsauces tabulas.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]