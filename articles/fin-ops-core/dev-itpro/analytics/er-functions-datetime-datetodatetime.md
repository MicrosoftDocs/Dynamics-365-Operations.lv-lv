---
title: DATETODATETIME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATETODATETIME elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: bb90c58544eeba804cd39542cc70fab3b840af80
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746967"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="a04cf-103">DATETODATETIME ER funkcija</span><span class="sxs-lookup"><span data-stu-id="a04cf-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a04cf-104">`DATETODATETIME` funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no konkrētā datuma vērtības uz datuma/laika vērtību pēc universālā koordinētā laika (Griničas laika \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="a04cf-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="a04cf-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="a04cf-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="a04cf-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="a04cf-106">Arguments</span></span>

<span data-ttu-id="a04cf-107">`date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="a04cf-107">`date`: *Date*</span></span>

<span data-ttu-id="a04cf-108">Datuma/laika vērtība, kas apzīmē konvertējamo datumu.</span><span class="sxs-lookup"><span data-stu-id="a04cf-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="a04cf-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="a04cf-109">Return values</span></span>

<span data-ttu-id="a04cf-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="a04cf-110">*DateTime*</span></span>

<span data-ttu-id="a04cf-111">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="a04cf-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a04cf-112">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="a04cf-112">Example 1</span></span>

<span data-ttu-id="a04cf-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` atgriež pašreizējās Microsoft Dynamics 365 Finance sesijas datumu, 2015. gada 24. decembri, kā **12/24/2015 12:00:00 AM.**</span><span class="sxs-lookup"><span data-stu-id="a04cf-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="a04cf-114">Šajā piemērā **CompInfo** ir elektronisko pārskatu (ER) datu avots ar veidu **Finance and Operations/Table**, un tas atsaucas uz tabulu CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="a04cf-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="a04cf-115">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="a04cf-115">Example 2</span></span>

<span data-ttu-id="a04cf-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` atgriež datuma/laika vērtību **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="a04cf-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a04cf-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a04cf-117">Additional resources</span></span>

[<span data-ttu-id="a04cf-118">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="a04cf-118">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]