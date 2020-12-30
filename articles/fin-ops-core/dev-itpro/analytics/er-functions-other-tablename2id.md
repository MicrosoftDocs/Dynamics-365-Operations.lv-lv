---
title: TABLENAME2ID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TABLENAME2ID elektroniskā pārskata (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a68a8e1f4afa378ab446eae12bc90cdb3aba8b19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681162"
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

Šīs funkcijas izpildei var būt atšķirīgi rezultāti dažādās Microsoft Dynamics 365 Finance instancēs, pat ja tiek izmantots viens un tas pats uzņēmuma nosaukums.

## <a name="example"></a>Paraugs

`TABLENAME2ID ("Intrastat")` atgriež **1510**.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)
