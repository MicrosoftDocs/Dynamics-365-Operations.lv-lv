---
title: Base64StringToContainer ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota Base64StringToContainer elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 01f7f032915a5e4170cae5e28a445081aef075fa
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355374"
---
# <a name="base64stringtocontainer-er-function"></a>Base64StringToContainer ER funkcija

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [funkcija](er-formula-language.md#functions) konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *[Konteiners](er-functions-category-container.md)*.

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