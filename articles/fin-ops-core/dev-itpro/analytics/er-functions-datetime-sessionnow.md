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
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916273"
---
# <span data-ttu-id="7ac77-103"><a name="">SESSIONNOW ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="7ac77-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ac77-104">`SESSIONNOW` funkcija atgriež *DateTime* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="7ac77-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac77-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="7ac77-105">Syntax</span></span>

```
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="7ac77-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="7ac77-106">Return values</span></span>

<span data-ttu-id="7ac77-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="7ac77-107">*DateTime*</span></span>

<span data-ttu-id="7ac77-108">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="7ac77-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="7ac77-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="7ac77-109">Example</span></span>

<span data-ttu-id="7ac77-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")`atgriež pašreizējās lietojumprogrammas sesijas datuma/laika vērtību, 2015. gada 24. decembri, kā **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.</span><span class="sxs-lookup"><span data-stu-id="7ac77-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ac77-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7ac77-111">Additional resources</span></span>

[<span data-ttu-id="7ac77-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="7ac77-112">Date and time functions</span></span>](er-functions-category-datetime.md)
