---
title: NUMBERVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMBERVALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916526"
---
# <span data-ttu-id="bbfbf-103"><a name="NUMBERVALUE">NUMBERVALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="bbfbf-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbfbf-104">`NUMBERVALUE` funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās *Virknes* vērtības.</span><span class="sxs-lookup"><span data-stu-id="bbfbf-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="bbfbf-105">Konvertēšanas laikā tiek uzskatīti norādītie decimālo un ciparu grupēšanas atdalītāji.</span><span class="sxs-lookup"><span data-stu-id="bbfbf-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbfbf-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="bbfbf-106">Syntax</span></span>

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="bbfbf-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="bbfbf-107">Arguments</span></span>

<span data-ttu-id="bbfbf-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="bbfbf-108">`text`: *String*</span></span>

<span data-ttu-id="bbfbf-109">Teksta vērtība, kas ir jāpārvērš par *Reālu* skaitli.</span><span class="sxs-lookup"><span data-stu-id="bbfbf-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="bbfbf-110">`decimal separator`: Virkne</span><span class="sxs-lookup"><span data-stu-id="bbfbf-110">`decimal separator`: String</span></span>

<span data-ttu-id="bbfbf-111">Decimāldaļu atdalītājs.</span><span class="sxs-lookup"><span data-stu-id="bbfbf-111">A decimal separator.</span></span> <span data-ttu-id="bbfbf-112">Tas tiek izmantots, lai atdalītu veselā skaitļa un daļskaitļa daļas no decimālskaitļa.</span><span class="sxs-lookup"><span data-stu-id="bbfbf-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="bbfbf-113">`digit grouping separator`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="bbfbf-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="bbfbf-114">Ciparu grupēšanas atdalītājs.</span><span class="sxs-lookup"><span data-stu-id="bbfbf-114">A digit grouping separator.</span></span> <span data-ttu-id="bbfbf-115">Tas tiek izmantots kā tūkstošu atdalītājs.</span><span class="sxs-lookup"><span data-stu-id="bbfbf-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="bbfbf-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="bbfbf-116">Return values</span></span>

<span data-ttu-id="bbfbf-117">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="bbfbf-117">*Real*</span></span>

<span data-ttu-id="bbfbf-118">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="bbfbf-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="bbfbf-119">Paraugs</span><span class="sxs-lookup"><span data-stu-id="bbfbf-119">Example</span></span>

<span data-ttu-id="bbfbf-120">`NUMBERVALUE( "1 234,56", ",", " ")` atgriež **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="bbfbf-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbfbf-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bbfbf-121">Additional resources</span></span>

[<span data-ttu-id="bbfbf-122">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="bbfbf-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
