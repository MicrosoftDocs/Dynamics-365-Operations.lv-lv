---
title: QRCODE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota QRCODE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 8a52dbce29140591baf4be97baef237dce1f2511
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040852"
---
# <a name="QRCODE">QRCODE ER funkcija</a>

[!include [banner](../includes/banner.md)]

`QRCODE` funkcija atgriež *Konteinera* vērtību, kas parāda ātrās atbildes kodu (QR koda) attēlu norādītajai virknei binārā formātā.

## <a name="syntax"></a>Sintakse

```vb
QRCODE (text)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

*Virknes* vērtība, kas apzīmē oriģinālo tekstu.

## <a name="return-values"></a>Atgrieztās vērtības

*Konteiners*

Iegūtā binārā plūsma.

## <a name="example"></a>Paraugs

Varat konfigurēt elektronisko pārskatu (ER) formātu, lai ģenerētu izejošo dokumentu Microsoft Office formātā (Excel darbgrāmatas vai Word dokumenti), izmantojot iepriekš definētu veidni. Šī veidne var saturēt objektu **Attēls** (Excel darbgrāmata) vai **Attēla satura vadīklu** (Word dokuments) kā QR koda attēla vietturi. Jums jāpievieno konfigurētajam ER formātam **Šūnas** elements, kas tiks izmantots šī viettura aizpildīšanai. Lai norādītu, kāda informācija tiks glabāta QR kodā, jums ir jādefinē saistījums šim **Šūnas** elementam. Piemēram, varat konfigurēt šādu saistījumu, kā tādu, kas satur šādu izteiksmi:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Palaižot konfigurēto ER formātu, datu avota **model.ListOfShelfLabels** lauka **LabelText** teksta vērtība tiks izmantota, lai ģenerētu QR koda attēlu. Šis attēls aizstās QR koda attēla vietturi dokumenta veidnē, izmantojot, lai ģenerētu izejošo dokumentu. Ja šis ģenerētā dokumenta attēls tiek skenēts, tas atgriež tekstu, kas tika ņemts no datu avota **model.ListOfShelfLabels** lauka **LabelText**. Vairāk informācijas skatiet rakstā [Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](electronic-reporting-embed-images-shapes.md)

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)
