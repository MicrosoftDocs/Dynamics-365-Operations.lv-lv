---
title: NOW ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NOW elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 8e549634b3856777aff610fa0e61c19bcad71dd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563514"
---
# <a name="now-er-function"></a><span data-ttu-id="359ec-103">NOW ER funkcija</span><span class="sxs-lookup"><span data-stu-id="359ec-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="359ec-104">`NOW` funkcija atgriež *DateTime* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="359ec-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="359ec-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="359ec-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="359ec-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="359ec-106">Return values</span></span>

<span data-ttu-id="359ec-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="359ec-107">*DateTime*</span></span>

<span data-ttu-id="359ec-108">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="359ec-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="359ec-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="359ec-109">Example</span></span>

<span data-ttu-id="359ec-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.</span><span class="sxs-lookup"><span data-stu-id="359ec-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="359ec-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="359ec-111">Additional resources</span></span>

[<span data-ttu-id="359ec-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="359ec-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]