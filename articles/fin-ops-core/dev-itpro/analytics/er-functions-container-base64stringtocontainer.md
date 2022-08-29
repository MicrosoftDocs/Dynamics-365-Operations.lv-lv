---
title: Base64StringToContainer ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota Base64StringToContainer Elektronisko pārskatu (ER) funkcija.
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 96dfffc3d899f1106c6c931efb08c941f5b3c1a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291240"
---
# <a name="base64stringtocontainer-er-function"></a>Base64StringToContainer ER funkcija

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [funkcija](er-formula-language.md#Functions) konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *[Konteiners](er-functions-category-container.md)*.

## <a name="syntax"></a>Sintakse

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Argumenti

`input`: *Virkne*

*Virknes* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*Konteiners*

Iegūtā binārā vērtība binārajā lielu objektu (BLOB) formātā.

## <a name="usage-notes"></a>Lietošanas piezīmes

"Parametrs nav derīgs" izņēmums tiek izmantots, ja ievades virkne nesniedz pareizu bināro-teksta kodēšanas shēmu grupu Base64.

## <a name="example"></a>Paraugs

Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.

- Saknes **DocuTypeGroupEnum** *Dynamics 365 for Operations datu avots/ uzskaitījuma tips*, kas attiecas uz **DocuTypeGroup** programmas uzskaitījumu
- Saknes **Debitors** *Dynamics 365 for Operations / Tabulas ieraksti* datu avots, kas atsaucas uz lietojuma tabulu **CustTable**
- **\#Media** datu avots no veida *Aprēķinātais lauks*, kas ir konfigurēts šādā veidā:

    - Tas ir pievienots kā debitora datu avota **Debitori** datu avots.
    - Tajā ir ietverta izteiksme `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- **\#MediaAsBase64String** datu avots no veida *Aprēķinātais lauks*, kas ir konfigurēts šādā veidā:

    - Tas ir pievienots kā atvasinātā datu avota **Debitori.'\#Media'** datu avots.
    - Tajā ir ietverta izteiksme `Customer.'#Media'.'getFileContentAsBase64String()'`.

- **\#lobFomBase64** datu avots no veida *Aprēķinātais lauks*, kas ir konfigurēts šādā veidā:

    - Tas ir pievienots kā atvasinātā datu avota **Debitori.'\#Media'** datu avots.
    - Tajā ir ietverta izteiksme `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

Šajā piemērā **\#MediaAsBase64String** datu avots kodē pašreizējā multivides pielikuma bināro saturu kā tekstu, kas apzīmē bināro-teksta kodēšanas shēmu Base64 grupu. **\#BLOBFomBase64** datu avots atšifrē Base64 virkni un atgriež bināro vērtību BLOB formātā.

![Parauga datu avoti ER Modeļu kartēšanas veidotāja lapā.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Papildu resursi

[Konteinera funkcijas](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
