---
title: QRCODE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota QRCODE elektronisko pārskatu (ER) funkcija.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: e1bcb053297b05f38a1185b54bde25c09411dd9e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905146"
---
# <a name="qrcode-er-function"></a>QRCODE ER funkcija

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]