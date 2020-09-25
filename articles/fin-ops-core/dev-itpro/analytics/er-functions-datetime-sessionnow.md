---
title: SESSIONNOW ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SESSIONNOW elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 00c41564b18eed477e1cefb0bc3bb2bca3fa6fdd
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745469"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="f4f46-103">SESSIONNOW ER funkcija</span><span class="sxs-lookup"><span data-stu-id="f4f46-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4f46-104">`SESSIONNOW` funkcija atgriež *DateTime* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="f4f46-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f46-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="f4f46-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="f4f46-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="f4f46-106">Return values</span></span>

<span data-ttu-id="f4f46-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="f4f46-107">*DateTime*</span></span>

<span data-ttu-id="f4f46-108">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="f4f46-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="f4f46-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="f4f46-109">Example</span></span>

<span data-ttu-id="f4f46-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datuma/laika vērtību, 2015. gada 24. decembri, kā **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.</span><span class="sxs-lookup"><span data-stu-id="f4f46-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4f46-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f4f46-111">Additional resources</span></span>

[<span data-ttu-id="f4f46-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="f4f46-112">Date and time functions</span></span>](er-functions-category-datetime.md)
