---
title: TABLENAME2ID ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota FUNKCIJA TABLENAME2ID Electronic Reporting (ER).
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
ms.openlocfilehash: b5deea69d5c43be599ccf02c0344ba8d662a6e0f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886854"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER funkcija

[!include [banner](../includes/banner.md)]

`TABLENAME2ID` funkcija atgriež tabulas ID skaitlisko attēlojumu norādītajam tabulas nosaukumam kā *Vesela skaitļa* vērtību.

## <a name="syntax"></a>Sintakse

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

Teksta vērtība, kas apzīmē derīgu tabulas nosaukumu.

## <a name="return-values"></a>Atgrieztās vērtības

*Vesels skaitlis*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šīs funkcijas izpildei var būt dažādi rezultāti dažādos Microsoft Dynamics 365 Finanšu gadījumos, pat ja tiek izmantots viens uzņēmuma nosaukums.

## <a name="example"></a>Paraugs

`TABLENAME2ID ("Intrastat")` atgriež **1510**.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]