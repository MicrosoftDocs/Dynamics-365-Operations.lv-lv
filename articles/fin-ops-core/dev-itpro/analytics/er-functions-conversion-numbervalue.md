---
title: NUMBERVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMBERVALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755352"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="fbb9b-103">NUMBERVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="fbb9b-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbb9b-104">`NUMBERVALUE` funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās *Virknes* vērtības.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="fbb9b-105">Konvertēšanas laikā tiek uzskatīti norādītie decimālo un ciparu grupēšanas atdalītāji.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb9b-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="fbb9b-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="fbb9b-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="fbb9b-107">Arguments</span></span>

<span data-ttu-id="fbb9b-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="fbb9b-108">`text`: *String*</span></span>

<span data-ttu-id="fbb9b-109">Teksta vērtība, kas ir jāpārvērš par *Reālu* skaitli.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="fbb9b-110">`decimal separator`: Virkne</span><span class="sxs-lookup"><span data-stu-id="fbb9b-110">`decimal separator`: String</span></span>

<span data-ttu-id="fbb9b-111">Decimāldaļu atdalītājs.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-111">A decimal separator.</span></span> <span data-ttu-id="fbb9b-112">Tas tiek izmantots, lai atdalītu veselā skaitļa un daļskaitļa daļas no decimālskaitļa.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="fbb9b-113">`digit grouping separator`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="fbb9b-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="fbb9b-114">Ciparu grupēšanas atdalītājs.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-114">A digit grouping separator.</span></span> <span data-ttu-id="fbb9b-115">Tas tiek izmantots kā tūkstošu atdalītājs.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="fbb9b-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="fbb9b-116">Return values</span></span>

<span data-ttu-id="fbb9b-117">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="fbb9b-117">*Real*</span></span>

<span data-ttu-id="fbb9b-118">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="fbb9b-119">Paraugs</span><span class="sxs-lookup"><span data-stu-id="fbb9b-119">Example</span></span>

<span data-ttu-id="fbb9b-120">`NUMBERVALUE( "1 234,56", ",", " ")` atgriež **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fbb9b-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fbb9b-121">Additional resources</span></span>

[<span data-ttu-id="fbb9b-122">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="fbb9b-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]