---
title: GETCURRENTCOMPANY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota GETCURRENTCOMPANY elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744129"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="0b641-103">GETCURRENTCOMPANY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="0b641-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b641-104">Funkcija `GETCURRENTCOMPANY` atgriež *Virknes* vērtību, kas apzīmē juridiskās personas (uzņēmuma) kodu, kurā lietotājs šobrīd ir pieteicies.</span><span class="sxs-lookup"><span data-stu-id="0b641-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b641-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="0b641-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="0b641-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="0b641-106">Return values</span></span>

<span data-ttu-id="0b641-107">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="0b641-107">*String*</span></span>

<span data-ttu-id="0b641-108">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0b641-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0b641-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="0b641-109">Example</span></span>

<span data-ttu-id="0b641-110">`GETCURRENTCOMPANY ()` atgriež **USMF** lietotājam, kurš ir pierakstījies uzņēmumā **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="0b641-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b641-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0b641-111">Additional resources</span></span>

[<span data-ttu-id="0b641-112">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="0b641-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
