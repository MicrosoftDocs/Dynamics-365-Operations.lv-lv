---
title: SESSIONTODAY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SESSIONTODAY elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 87e8d5498c82d7c9ca6ee0a855f139dde77d75ab
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683823"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="e387a-103">SESSIONTODAY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e387a-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e387a-104">`SESSIONTODAY` funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu.</span><span class="sxs-lookup"><span data-stu-id="e387a-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e387a-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="e387a-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e387a-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="e387a-106">Return values</span></span>

<span data-ttu-id="e387a-107">*Datums*</span><span class="sxs-lookup"><span data-stu-id="e387a-107">*Date*</span></span>

<span data-ttu-id="e387a-108">Iegūtā datuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="e387a-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e387a-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="e387a-109">Example</span></span>

<span data-ttu-id="e387a-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datumu, 2015. gada 24. decembri, kā virkni **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.</span><span class="sxs-lookup"><span data-stu-id="e387a-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e387a-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e387a-111">Additional resources</span></span>

[<span data-ttu-id="e387a-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="e387a-112">Date and time functions</span></span>](er-functions-category-datetime.md)
