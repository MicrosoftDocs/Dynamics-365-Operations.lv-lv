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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917630"
---
# <span data-ttu-id="e2220-103"><a name="VALUE">VALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="e2220-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2220-104">`VALUE` funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās virknes vērtības.</span><span class="sxs-lookup"><span data-stu-id="e2220-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2220-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="e2220-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="e2220-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="e2220-106">Arguments</span></span>

<span data-ttu-id="e2220-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="e2220-107">`text`: *String*</span></span>

<span data-ttu-id="e2220-108">Virknes vērtība, kas ir jāpārvērš par skaitlisku vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2220-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="e2220-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="e2220-109">Return values</span></span>

<span data-ttu-id="e2220-110">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="e2220-110">*Real*</span></span>

<span data-ttu-id="e2220-111">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="e2220-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e2220-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="e2220-112">Usage notes</span></span>

<span data-ttu-id="e2220-113">Komati un punkta rakstzīmes (.) tiek uzskatīti par decimāldaļu atdalītājiem, un sākuma defise (-) tiek lietota kā mīnusa zīme.</span><span class="sxs-lookup"><span data-stu-id="e2220-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="e2220-114">Izņēmums tiek parādīts izpildes laikā, ja norādītā virkne satur citas rakstzīmes, kas nav skaitļi.</span><span class="sxs-lookup"><span data-stu-id="e2220-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="e2220-115">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="e2220-115">Example 1</span></span>

<span data-ttu-id="e2220-116">`VALUE ("1 234,56")` palaiž izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="e2220-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="e2220-117">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="e2220-117">Example 2</span></span>

<span data-ttu-id="e2220-118">`VALUE ("1234,56")` atgriež **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="e2220-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2220-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e2220-119">Additional resources</span></span>

[<span data-ttu-id="e2220-120">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="e2220-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)