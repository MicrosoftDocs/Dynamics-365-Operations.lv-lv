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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915997"
---
# <span data-ttu-id="42445-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="42445-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42445-104"> `GETCURRENTCOMPANY` funkcija atgriež *Virknes* vērtību, kas apzīmē juridiskās personas (uzņēmuma) kodu, kurā lietotājs šobrīd ir pieteicies.</span><span class="sxs-lookup"><span data-stu-id="42445-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="42445-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="42445-105">Syntax</span></span>

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="42445-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="42445-106">Return values</span></span>

<span data-ttu-id="42445-107">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="42445-107">*String*</span></span>

<span data-ttu-id="42445-108">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="42445-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="42445-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="42445-109">Example</span></span>

<span data-ttu-id="42445-110">`GETCURRENTCOMPANY ()` atgriež **USMF** lietotājam, kurš ir pierakstījies uzņēmumā **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="42445-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42445-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="42445-111">Additional resources</span></span>

[<span data-ttu-id="42445-112">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="42445-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
