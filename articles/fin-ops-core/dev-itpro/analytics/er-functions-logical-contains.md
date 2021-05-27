---
title: CONTAINS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CONTAINS elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: a31d89f036a6e821bea2b6733c0c646145d2a47c
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048874"
---
# <a name="contains-er-function"></a><span data-ttu-id="6e359-103">CONTAINS ER funkcija</span><span class="sxs-lookup"><span data-stu-id="6e359-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e359-104">`CONTAINS` funkcija nosaka, vai norādītā ievade satur norādīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="6e359-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="6e359-105">Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade satur norādīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="6e359-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="6e359-106">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6e359-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e359-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="6e359-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="6e359-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="6e359-108">Arguments</span></span>

<span data-ttu-id="6e359-109">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="6e359-109">`input`: *String*</span></span>

<span data-ttu-id="6e359-110">Veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var saturēt otro argumentu.</span><span class="sxs-lookup"><span data-stu-id="6e359-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="6e359-111">`search text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="6e359-111">`search text`: *String*</span></span>

<span data-ttu-id="6e359-112">Datu veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var būt ietverta pirmajā argumentā.</span><span class="sxs-lookup"><span data-stu-id="6e359-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="6e359-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="6e359-113">Return values</span></span>

<span data-ttu-id="6e359-114">*Būla*</span><span class="sxs-lookup"><span data-stu-id="6e359-114">*Boolean*</span></span>

<span data-ttu-id="6e359-115">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="6e359-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6e359-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="6e359-116">Usage notes</span></span>

<span data-ttu-id="6e359-117">Šo funkciju var izmantot funkcijas [FILTER](er-functions-list-filter.md) nosacījuma izteiksmes norādīšanai tikai tad, ja atbilstošā kartēšana ir konfigurēta [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md), lai piekļūtu [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="6e359-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="6e359-118">Pretējā gadījumā izstrādes laikā tiek izmests izņēmums.</span><span class="sxs-lookup"><span data-stu-id="6e359-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="6e359-119">Saņemtais ziņojums iesaka izmantot funkciju [WHERE](er-functions-list-where.md), nevis funkciju `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="6e359-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="6e359-120">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="6e359-120">Example 1</span></span>

<span data-ttu-id="6e359-121">Izteiksme `CONTAINS ("abc", "d")` atgriež **APLAMS**, savukārt izteiksme `CONTAINS ("abc", "C")` atgriež **PATIESS**.</span><span class="sxs-lookup"><span data-stu-id="6e359-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6e359-122">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="6e359-122">Example 2</span></span>

<span data-ttu-id="6e359-123">Izteiksme `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` atgriež **PATIESS**, ja datu avota **modelis** lauka **Adrese** vērtība ietver virkni **DEU**.</span><span class="sxs-lookup"><span data-stu-id="6e359-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="6e359-124">Pretējā gadījumā tā atgriež vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6e359-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e359-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6e359-125">Additional resources</span></span>

[<span data-ttu-id="6e359-126">Loģiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="6e359-126">Logical functions</span></span>](er-functions-category-logical.md)
