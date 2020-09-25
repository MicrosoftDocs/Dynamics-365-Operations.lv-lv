---
title: VALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota VALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: ecbffb7e39d7f2f2bccdfe32d593512a65da163c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745517"
---
# <a name="value-er-function"></a><span data-ttu-id="77ba2-103">VALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="77ba2-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77ba2-104">`VALUE` funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās virknes vērtības.</span><span class="sxs-lookup"><span data-stu-id="77ba2-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ba2-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="77ba2-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="77ba2-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="77ba2-106">Arguments</span></span>

<span data-ttu-id="77ba2-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="77ba2-107">`text`: *String*</span></span>

<span data-ttu-id="77ba2-108">Virknes vērtība, kas ir jāpārvērš par skaitlisku vērtību.</span><span class="sxs-lookup"><span data-stu-id="77ba2-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="77ba2-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="77ba2-109">Return values</span></span>

<span data-ttu-id="77ba2-110">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="77ba2-110">*Real*</span></span>

<span data-ttu-id="77ba2-111">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="77ba2-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="77ba2-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="77ba2-112">Usage notes</span></span>

<span data-ttu-id="77ba2-113">Komati un punkta rakstzīmes (.) tiek uzskatīti par decimāldaļu atdalītājiem, un sākuma defise (-) tiek lietota kā mīnusa zīme.</span><span class="sxs-lookup"><span data-stu-id="77ba2-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="77ba2-114">Izņēmums tiek parādīts izpildes laikā, ja norādītā virkne satur citas rakstzīmes, kas nav skaitļi.</span><span class="sxs-lookup"><span data-stu-id="77ba2-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="77ba2-115">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="77ba2-115">Example 1</span></span>

<span data-ttu-id="77ba2-116">`VALUE ("1 234,56")` palaiž izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="77ba2-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="77ba2-117">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="77ba2-117">Example 2</span></span>

<span data-ttu-id="77ba2-118">`VALUE ("1234,56")` atgriež **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="77ba2-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77ba2-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="77ba2-119">Additional resources</span></span>

[<span data-ttu-id="77ba2-120">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="77ba2-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
