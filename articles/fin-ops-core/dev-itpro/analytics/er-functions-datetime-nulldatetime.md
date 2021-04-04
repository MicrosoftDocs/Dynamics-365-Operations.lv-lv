---
title: NULLDATETIME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NULLDATETIME elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 159abe09f158565fa9c38da530498329ff183fba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563442"
---
# <a name="nulldatetime-er-function"></a><span data-ttu-id="0feac-103">NULLDATETIME ER funkcija</span><span class="sxs-lookup"><span data-stu-id="0feac-103">NULLDATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0feac-104">`NULLDATETIME` funkcija atgriež *DateTime* vērtību, kas apzīmē **nulles** datuma/laika vērtību (1900. gada 1. janvāris) universālajā koordinētajā laikā (Griničas laikā \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="0feac-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="0feac-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="0feac-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="0feac-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="0feac-106">Return values</span></span>

<span data-ttu-id="0feac-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="0feac-107">*DateTime*</span></span>

<span data-ttu-id="0feac-108">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="0feac-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="0feac-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="0feac-109">Example</span></span>

<span data-ttu-id="0feac-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` atgriež virknes vērtību **1900-01-01T00:00:00.0000000+00:00**, kad tā tiek saukta procesa laikā, ko iniciēja lietojumprogrammas lietotājs, kuram ir laika joslas vērtība **(GMT) universālais koordinētais laiks** sadaļā **Valodas un valsts/reģiona preferences**.</span><span class="sxs-lookup"><span data-stu-id="0feac-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0feac-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0feac-111">Additional resources</span></span>

[<span data-ttu-id="0feac-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="0feac-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]