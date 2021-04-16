---
title: DAYS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DAYS elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 310359a29a506d69d1f34aaa710a82b0f2ea528e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746895"
---
# <a name="days-er-function"></a><span data-ttu-id="e63cb-103">DAYS ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e63cb-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e63cb-104">`DAYS` funkcija atgriež *Vesela skaitļa* vērtību, kas reprezentē dienu skaitu no viena norādītā datuma līdz otram norādītajam datumam.</span><span class="sxs-lookup"><span data-stu-id="e63cb-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e63cb-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="e63cb-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="e63cb-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="e63cb-106">Arguments</span></span>

<span data-ttu-id="e63cb-107">`date 1`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="e63cb-107">`date 1`: *Date*</span></span>

<span data-ttu-id="e63cb-108">Datuma vērtība, kas apzīmē sākuma datumu, kas jāizmanto, aprēķinot dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="e63cb-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="e63cb-109">`date 2`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="e63cb-109">`date 2`: *Date*</span></span>

<span data-ttu-id="e63cb-110">Datuma vērtība, kas apzīmē beigu datumu, kas jāizmanto, aprēķinot dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="e63cb-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="e63cb-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="e63cb-111">Return values</span></span>

<span data-ttu-id="e63cb-112">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="e63cb-112">*Integer*</span></span>

<span data-ttu-id="e63cb-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="e63cb-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e63cb-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="e63cb-114">Usage notes</span></span>

<span data-ttu-id="e63cb-115">`DAYS` funkcija atgriež pozitīvu vērtību, ja pirmais datums ir vēlāks par otro datumu; tiek atgriezta **0** (nulle), ja pirmais datums ir vienāds ar otro; vai tiek atgriezta negatīva vērtība, ja pirmais datums ir agrāks par otro datumu.</span><span class="sxs-lookup"><span data-stu-id="e63cb-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="e63cb-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="e63cb-116">Example</span></span>

<span data-ttu-id="e63cb-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` atgriež **-1**.</span><span class="sxs-lookup"><span data-stu-id="e63cb-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e63cb-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e63cb-118">Additional resources</span></span>

[<span data-ttu-id="e63cb-119">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="e63cb-119">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]