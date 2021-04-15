---
title: TODAY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TODAY elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746751"
---
# <a name="today-er-function"></a><span data-ttu-id="066f9-103">TODAY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="066f9-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="066f9-104">`TODAY` funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu.</span><span class="sxs-lookup"><span data-stu-id="066f9-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="066f9-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="066f9-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="066f9-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="066f9-106">Return values</span></span>

<span data-ttu-id="066f9-107">*Datums*</span><span class="sxs-lookup"><span data-stu-id="066f9-107">*Date*</span></span>

<span data-ttu-id="066f9-108">Iegūtā datuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="066f9-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="066f9-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="066f9-109">Example</span></span>

<span data-ttu-id="066f9-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā virkni **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.</span><span class="sxs-lookup"><span data-stu-id="066f9-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="066f9-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="066f9-111">Additional resources</span></span>

[<span data-ttu-id="066f9-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="066f9-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]