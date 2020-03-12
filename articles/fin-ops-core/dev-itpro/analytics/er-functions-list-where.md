---
title: WHERE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota WHERE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 392cf7acebd7ad95bcc0f5d4b7a67500a412a795
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041838"
---
# <span data-ttu-id="d66a4-103"><a name="WHERE">WHERE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="d66a4-103"><a name="WHERE">WHERE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d66a4-104">`WHERE` funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību pēc tam, kad tas ir filtrēts atbilstoši norādītajiem nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="d66a4-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="d66a4-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="d66a4-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="d66a4-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d66a4-106">Arguments</span></span>

<span data-ttu-id="d66a4-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="d66a4-107">`list`: *Record list*</span></span>

<span data-ttu-id="d66a4-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="d66a4-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d66a4-109">`condition`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="d66a4-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="d66a4-110">Derīga nosacījuma izteiksme, ko izmanto, lai filtrētu norādītā saraksta ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d66a4-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="d66a4-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d66a4-111">Return values</span></span>

<span data-ttu-id="d66a4-112">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="d66a4-112">*Record list*</span></span>

<span data-ttu-id="d66a4-113">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="d66a4-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d66a4-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="d66a4-114">Usage notes</span></span>

<span data-ttu-id="d66a4-115">Šī funkcija atšķiras no funkcijas [FILTER](er-functions-list-filter.md), jo norādītais nosacījums tiek lietots datu bāzes līmenī visiem elektronisko pārskatu (ER) datu avotiem ar tipu *Ierakstu saraksts*, kas atrodas atmiņā.</span><span class="sxs-lookup"><span data-stu-id="d66a4-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="d66a4-116">Ja argumenti, kas ir konfigurēts šai funkcijai (`list` un `condition`) neļauj šo pieprasījumu tulkot uz tiešo SQL zvanu, noformēšanas laikā tiek rādīts brīdinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="d66a4-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="d66a4-117">Šis ziņojums informē lietotāju, ka tas var uzlabot veiktspēju, ja `WHERE` vietā tiek izmantota funkcija [FILTER](er-functions-list-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d66a4-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="d66a4-118">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="d66a4-118">Example 1</span></span>

<span data-ttu-id="d66a4-119">Ja parametrs **Kreditors** ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, izteiksme `WHERE (Vendors, Vendors.VendGroup = "40")` atgriež tikai kreditoru grupā 40 ietverto kreditoru sarakstu.</span><span class="sxs-lookup"><span data-stu-id="d66a4-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="d66a4-120">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="d66a4-120">Example 2</span></span>

<span data-ttu-id="d66a4-121">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `WHERE( DS, DS.Value = "B")` atgriež sarakstu tikai ar vienu ierakstu kas laukā **Vērtība** satur tekstu **"B"**.</span><span class="sxs-lookup"><span data-stu-id="d66a4-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d66a4-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d66a4-122">Additional resources</span></span>

[<span data-ttu-id="d66a4-123">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="d66a4-123">List functions</span></span>](er-functions-category-list.md)
