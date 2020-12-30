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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66398e624e4b9d69d4dc3ccf3ee8f97758f4f861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682345"
---
# <a name="days-er-function"></a><span data-ttu-id="eb1c7-103">DAYS ER funkcija</span><span class="sxs-lookup"><span data-stu-id="eb1c7-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb1c7-104">`DAYS` funkcija atgriež *Vesela skaitļa* vērtību, kas reprezentē dienu skaitu no viena norādītā datuma līdz otram norādītajam datumam.</span><span class="sxs-lookup"><span data-stu-id="eb1c7-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1c7-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="eb1c7-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="eb1c7-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="eb1c7-106">Arguments</span></span>

<span data-ttu-id="eb1c7-107">`date 1`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="eb1c7-107">`date 1`: *Date*</span></span>

<span data-ttu-id="eb1c7-108">Datuma vērtība, kas apzīmē sākuma datumu, kas jāizmanto, aprēķinot dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="eb1c7-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="eb1c7-109">`date 2`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="eb1c7-109">`date 2`: *Date*</span></span>

<span data-ttu-id="eb1c7-110">Datuma vērtība, kas apzīmē beigu datumu, kas jāizmanto, aprēķinot dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="eb1c7-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb1c7-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="eb1c7-111">Return values</span></span>

<span data-ttu-id="eb1c7-112">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="eb1c7-112">*Integer*</span></span>

<span data-ttu-id="eb1c7-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="eb1c7-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="eb1c7-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="eb1c7-114">Usage notes</span></span>

<span data-ttu-id="eb1c7-115">`DAYS` funkcija atgriež pozitīvu vērtību, ja pirmais datums ir vēlāks par otro datumu; tiek atgriezta **0** (nulle), ja pirmais datums ir vienāds ar otro; vai tiek atgriezta negatīva vērtība, ja pirmais datums ir agrāks par otro datumu.</span><span class="sxs-lookup"><span data-stu-id="eb1c7-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="eb1c7-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="eb1c7-116">Example</span></span>

<span data-ttu-id="eb1c7-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` atgriež **-1**.</span><span class="sxs-lookup"><span data-stu-id="eb1c7-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb1c7-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="eb1c7-118">Additional resources</span></span>

[<span data-ttu-id="eb1c7-119">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="eb1c7-119">Date and time functions</span></span>](er-functions-category-datetime.md)
