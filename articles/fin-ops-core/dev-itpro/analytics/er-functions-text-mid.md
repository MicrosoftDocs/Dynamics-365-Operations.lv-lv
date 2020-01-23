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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915606"
---
# <span data-ttu-id="95cbb-103"><a name="MID">MID ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="95cbb-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95cbb-104">`MID` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes, sākot no norādītas pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="95cbb-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="95cbb-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="95cbb-105">Syntax</span></span>

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="95cbb-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="95cbb-106">Arguments</span></span>

<span data-ttu-id="95cbb-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="95cbb-107">`text`: *String*</span></span>

<span data-ttu-id="95cbb-108">*Virknes* vērtība, kas norāda tekstu, no kura jāatgriež rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="95cbb-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="95cbb-109">`starting position`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="95cbb-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="95cbb-110">*Vesela skaitļa* vērtība, kas norāda pirmās rakstzīmes novietojumu, kura ir jāatgriež no norādītā teksta.</span><span class="sxs-lookup"><span data-stu-id="95cbb-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="95cbb-111">`number of characters`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="95cbb-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="95cbb-112">*Vesela skaitļa* vērtība, kas norāda skaitu rakstzīmēm, kuras ir jāatgriež, sākot no norādītās sākuma pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="95cbb-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="95cbb-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="95cbb-113">Return values</span></span>

<span data-ttu-id="95cbb-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="95cbb-114">*String*</span></span>

<span data-ttu-id="95cbb-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="95cbb-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="95cbb-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="95cbb-116">Usage notes</span></span>

<span data-ttu-id="95cbb-117">Ja `starting position` argumenta vērtība ir mazāka par 0 (nulli), atgrieztās rakstzīmes tiek skaitītas no norādītās virknes pirmās pozīcijas.</span><span class="sxs-lookup"><span data-stu-id="95cbb-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="95cbb-118">Ja `starting position` argumenta vērtība pārsniedz norādītās virknes garumu, tiek atgriezta tukša virkne.</span><span class="sxs-lookup"><span data-stu-id="95cbb-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="95cbb-119">Paraugs</span><span class="sxs-lookup"><span data-stu-id="95cbb-119">Example</span></span>

<span data-ttu-id="95cbb-120">`MID ("Sample", 2, 3)`atgriež **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="95cbb-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95cbb-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="95cbb-121">Additional resources</span></span>

[<span data-ttu-id="95cbb-122">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="95cbb-122">Text functions</span></span>](er-functions-category-text.md)
