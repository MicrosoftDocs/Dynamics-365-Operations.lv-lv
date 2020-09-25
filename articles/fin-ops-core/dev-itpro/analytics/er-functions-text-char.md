---
title: CHAR ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CHAR elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 63df7b1ac847e12cf429467dd444450552a59162
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744965"
---
# <a name="char-er-function"></a><span data-ttu-id="22249-103">CHAR ER funkcija</span><span class="sxs-lookup"><span data-stu-id="22249-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22249-104">`CHAR` funkcija atgriež *Virknes* vērtību, kas parāda vienu rakstzīmi, uz kuru atsaucas norādītais unikoda numurs.</span><span class="sxs-lookup"><span data-stu-id="22249-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="22249-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="22249-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="22249-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="22249-106">Arguments</span></span>

<span data-ttu-id="22249-107">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="22249-107">`number`: *Integer*</span></span>

<span data-ttu-id="22249-108">Skaitlis, kas atbilst paredzētai vienai rakstzīmei.</span><span class="sxs-lookup"><span data-stu-id="22249-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="22249-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="22249-109">Return values</span></span>

<span data-ttu-id="22249-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="22249-110">*String*</span></span>

<span data-ttu-id="22249-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="22249-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="22249-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="22249-112">Usage notes</span></span>

<span data-ttu-id="22249-113">Šīs funkcijas atgrieztā virkne ir atkarīga kodējuma, kas ir atlasīts vecākelementa formāta elementā **FILE**.</span><span class="sxs-lookup"><span data-stu-id="22249-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="22249-114">Atbalstīto kodējumu sarakstu skatiet tēmā [Kodējuma klase](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="22249-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="22249-115">Paraugs</span><span class="sxs-lookup"><span data-stu-id="22249-115">Example</span></span>

<span data-ttu-id="22249-116">`CHAR (255)` atgriež **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="22249-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22249-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="22249-117">Additional resources</span></span>

[<span data-ttu-id="22249-118">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="22249-118">Text functions</span></span>](er-functions-category-text.md)
