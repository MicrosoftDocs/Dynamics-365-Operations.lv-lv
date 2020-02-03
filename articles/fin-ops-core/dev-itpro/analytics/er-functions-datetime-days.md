---
title: DAYS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DAYS elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4f8c12a22f7654285d5598064473bf86689ed207
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916296"
---
# <span data-ttu-id="780c7-103"><a name="DAYS">DAYS ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="780c7-103"><a name="DAYS">DAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="780c7-104">`DAYS` funkcija atgriež *Vesela skaitļa* vērtību, kas reprezentē dienu skaitu no viena norādītā datuma līdz otram norādītajam datumam.</span><span class="sxs-lookup"><span data-stu-id="780c7-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="780c7-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="780c7-105">Syntax</span></span>

```
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="780c7-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="780c7-106">Arguments</span></span>

<span data-ttu-id="780c7-107">`date 1`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="780c7-107">`date 1`: *Date*</span></span>

<span data-ttu-id="780c7-108">Datuma vērtība, kas apzīmē sākuma datumu, kas jāizmanto, aprēķinot dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="780c7-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="780c7-109">`date 2`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="780c7-109">`date 2`: *Date*</span></span>

<span data-ttu-id="780c7-110">Datuma vērtība, kas apzīmē beigu datumu, kas jāizmanto, aprēķinot dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="780c7-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="780c7-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="780c7-111">Return values</span></span>

<span data-ttu-id="780c7-112">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="780c7-112">*Integer*</span></span>

<span data-ttu-id="780c7-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="780c7-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="780c7-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="780c7-114">Usage notes</span></span>

<span data-ttu-id="780c7-115">`DAYS` funkcija atgriež pozitīvu vērtību, ja pirmais datums ir vēlāks par otro datumu; tiek atgriezta **0** (nulle), ja pirmais datums ir vienāds ar otro; vai tiek atgriezta negatīva vērtība, ja pirmais datums ir agrāks par otro datumu.</span><span class="sxs-lookup"><span data-stu-id="780c7-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="780c7-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="780c7-116">Example</span></span>

<span data-ttu-id="780c7-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` atgriež **-1**.</span><span class="sxs-lookup"><span data-stu-id="780c7-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="780c7-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="780c7-118">Additional resources</span></span>

[<span data-ttu-id="780c7-119">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="780c7-119">Date and time functions</span></span>](er-functions-category-datetime.md)