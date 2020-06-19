---
title: TODAY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TODAY elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 94ef15d1971287e8bf13944bc8f693b567950031
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411441"
---
# <a name=""></a><span data-ttu-id="1304c-103"><a name="TODAY">TODAY ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="1304c-103"><a name="TODAY">TODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1304c-104">`TODAY` funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu.</span><span class="sxs-lookup"><span data-stu-id="1304c-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="1304c-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="1304c-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="1304c-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="1304c-106">Return values</span></span>

<span data-ttu-id="1304c-107">*Datums*</span><span class="sxs-lookup"><span data-stu-id="1304c-107">*Date*</span></span>

<span data-ttu-id="1304c-108">Iegūtā datuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="1304c-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="1304c-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="1304c-109">Example</span></span>

<span data-ttu-id="1304c-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā virkni **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.</span><span class="sxs-lookup"><span data-stu-id="1304c-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1304c-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1304c-111">Additional resources</span></span>

[<span data-ttu-id="1304c-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="1304c-112">Date and time functions</span></span>](er-functions-category-datetime.md)
