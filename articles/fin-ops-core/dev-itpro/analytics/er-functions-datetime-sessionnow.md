---
title: SESSIONNOW ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SESSIONNOW elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: 47b88a1ca0ea9fd09c2a82963901d9ace78891bb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746799"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="b3d8c-103">SESSIONNOW ER funkcija</span><span class="sxs-lookup"><span data-stu-id="b3d8c-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3d8c-104">`SESSIONNOW` funkcija atgriež *DateTime* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="b3d8c-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d8c-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="b3d8c-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="b3d8c-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="b3d8c-106">Return values</span></span>

<span data-ttu-id="b3d8c-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="b3d8c-107">*DateTime*</span></span>

<span data-ttu-id="b3d8c-108">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="b3d8c-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="b3d8c-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="b3d8c-109">Example</span></span>

<span data-ttu-id="b3d8c-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datuma/laika vērtību, 2015. gada 24. decembri, kā **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.</span><span class="sxs-lookup"><span data-stu-id="b3d8c-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3d8c-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b3d8c-111">Additional resources</span></span>

[<span data-ttu-id="b3d8c-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="b3d8c-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]