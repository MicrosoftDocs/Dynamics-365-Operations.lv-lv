---
title: MID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota MID elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744723"
---
# <a name="mid-er-function"></a><span data-ttu-id="0c1b4-103">MID ER funkcija</span><span class="sxs-lookup"><span data-stu-id="0c1b4-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c1b4-104">`MID` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes, sākot no norādītas pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="0c1b4-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1b4-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="0c1b4-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="0c1b4-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="0c1b4-106">Arguments</span></span>

<span data-ttu-id="0c1b4-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="0c1b4-107">`text`: *String*</span></span>

<span data-ttu-id="0c1b4-108">*Virknes* vērtība, kas norāda tekstu, no kura jāatgriež rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="0c1b4-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="0c1b4-109">`starting position`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="0c1b4-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="0c1b4-110">*Vesela skaitļa* vērtība, kas norāda pirmās rakstzīmes novietojumu, kura ir jāatgriež no norādītā teksta.</span><span class="sxs-lookup"><span data-stu-id="0c1b4-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="0c1b4-111">`number of characters`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="0c1b4-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="0c1b4-112">*Vesela skaitļa* vērtība, kas norāda skaitu rakstzīmēm, kuras ir jāatgriež, sākot no norādītās sākuma pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="0c1b4-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c1b4-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="0c1b4-113">Return values</span></span>

<span data-ttu-id="0c1b4-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="0c1b4-114">*String*</span></span>

<span data-ttu-id="0c1b4-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0c1b4-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0c1b4-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="0c1b4-116">Usage notes</span></span>

<span data-ttu-id="0c1b4-117">Ja `starting position` argumenta vērtība ir mazāka par 0 (nulli), atgrieztās rakstzīmes tiek skaitītas no norādītās virknes pirmās pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="0c1b4-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="0c1b4-118">Ja `starting position` argumenta vērtība pārsniedz norādītās virknes garumu, tiek atgriezta tukša virkne.</span><span class="sxs-lookup"><span data-stu-id="0c1b4-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="0c1b4-119">Paraugs</span><span class="sxs-lookup"><span data-stu-id="0c1b4-119">Example</span></span>

<span data-ttu-id="0c1b4-120">`MID ("Sample", 2, 3)` atgriež **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="0c1b4-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c1b4-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0c1b4-121">Additional resources</span></span>

[<span data-ttu-id="0c1b4-122">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="0c1b4-122">Text functions</span></span>](er-functions-category-text.md)
