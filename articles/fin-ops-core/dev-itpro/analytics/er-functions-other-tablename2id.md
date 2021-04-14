---
title: TABLENAME2ID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TABLENAME2ID elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 0f94d00d9d40830d895e906ffbaa2a236f1efc43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746559"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]