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
ms.openlocfilehash: 13346c4810d6c93d4ef47ce525831332562c7f51
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743403"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="ad666-103">NUMBERVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="ad666-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad666-104">`NUMBERVALUE` funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās *Virknes* vērtības.</span><span class="sxs-lookup"><span data-stu-id="ad666-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="ad666-105">Konvertēšanas laikā tiek uzskatīti norādītie decimālo un ciparu grupēšanas atdalītāji.</span><span class="sxs-lookup"><span data-stu-id="ad666-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad666-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="ad666-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="ad666-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="ad666-107">Arguments</span></span>

<span data-ttu-id="ad666-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="ad666-108">`text`: *String*</span></span>

<span data-ttu-id="ad666-109">Teksta vērtība, kas ir jāpārvērš par *Reālu* skaitli.</span><span class="sxs-lookup"><span data-stu-id="ad666-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="ad666-110">`decimal separator`: Virkne</span><span class="sxs-lookup"><span data-stu-id="ad666-110">`decimal separator`: String</span></span>

<span data-ttu-id="ad666-111">Decimāldaļu atdalītājs.</span><span class="sxs-lookup"><span data-stu-id="ad666-111">A decimal separator.</span></span> <span data-ttu-id="ad666-112">Tas tiek izmantots, lai atdalītu veselā skaitļa un daļskaitļa daļas no decimālskaitļa.</span><span class="sxs-lookup"><span data-stu-id="ad666-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="ad666-113">`digit grouping separator`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="ad666-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="ad666-114">Ciparu grupēšanas atdalītājs.</span><span class="sxs-lookup"><span data-stu-id="ad666-114">A digit grouping separator.</span></span> <span data-ttu-id="ad666-115">Tas tiek izmantots kā tūkstošu atdalītājs.</span><span class="sxs-lookup"><span data-stu-id="ad666-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="ad666-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="ad666-116">Return values</span></span>

<span data-ttu-id="ad666-117">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="ad666-117">*Real*</span></span>

<span data-ttu-id="ad666-118">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="ad666-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="ad666-119">Paraugs</span><span class="sxs-lookup"><span data-stu-id="ad666-119">Example</span></span>

<span data-ttu-id="ad666-120">`NUMBERVALUE( "1 234,56", ",", " ")` atgriež **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="ad666-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad666-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ad666-121">Additional resources</span></span>

[<span data-ttu-id="ad666-122">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="ad666-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
