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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a93a9171456fb69e16c8104b0afb9ad485311b1a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683799"
---
# <a name="today-er-function"></a><span data-ttu-id="53503-103">TODAY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="53503-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53503-104">`TODAY` funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu.</span><span class="sxs-lookup"><span data-stu-id="53503-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="53503-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="53503-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="53503-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="53503-106">Return values</span></span>

<span data-ttu-id="53503-107">*Datums*</span><span class="sxs-lookup"><span data-stu-id="53503-107">*Date*</span></span>

<span data-ttu-id="53503-108">Iegūtā datuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="53503-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="53503-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="53503-109">Example</span></span>

<span data-ttu-id="53503-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā virkni **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.</span><span class="sxs-lookup"><span data-stu-id="53503-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53503-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="53503-111">Additional resources</span></span>

[<span data-ttu-id="53503-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="53503-112">Date and time functions</span></span>](er-functions-category-datetime.md)
