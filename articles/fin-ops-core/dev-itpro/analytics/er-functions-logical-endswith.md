---
title: ENDSWITH ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ENDSWITH elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 1155bb5446f0370d9a5c4b035a767aaeb1d46ee1
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048898"
---
# <a name="endswith-er-function"></a><span data-ttu-id="ad41a-103">ENDSWITH ER funkcija</span><span class="sxs-lookup"><span data-stu-id="ad41a-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad41a-104">`ENDSWITH` funkcija nosaka, vai norādītā ievade beidzas ar norādīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="ad41a-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="ad41a-105">Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade beidzas ar norādīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="ad41a-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="ad41a-106">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ad41a-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad41a-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="ad41a-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="ad41a-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="ad41a-108">Arguments</span></span>

<span data-ttu-id="ad41a-109">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="ad41a-109">`input`: *String*</span></span>

<span data-ttu-id="ad41a-110">Veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var beigties ar otro argumentu.</span><span class="sxs-lookup"><span data-stu-id="ad41a-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="ad41a-111">`start text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="ad41a-111">`start text`: *String*</span></span>

<span data-ttu-id="ad41a-112">Datu veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var būt pirmā argumenta beigās.</span><span class="sxs-lookup"><span data-stu-id="ad41a-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="ad41a-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="ad41a-113">Return values</span></span>

<span data-ttu-id="ad41a-114">*Būla*</span><span class="sxs-lookup"><span data-stu-id="ad41a-114">*Boolean*</span></span>

<span data-ttu-id="ad41a-115">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="ad41a-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ad41a-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="ad41a-116">Usage notes</span></span>

<span data-ttu-id="ad41a-117">Šo funkciju var izmantot funkcijas [FILTER](er-functions-list-filter.md) nosacījuma izteiksmes norādīšanai tikai tad, ja atbilstošā kartēšana ir konfigurēta [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md), lai piekļūtu [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="ad41a-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="ad41a-118">Pretējā gadījumā izstrādes laikā tiek izmests izņēmums.</span><span class="sxs-lookup"><span data-stu-id="ad41a-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="ad41a-119">Saņemtais ziņojums iesaka izmantot funkciju [WHERE](er-functions-list-where.md), nevis funkciju `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="ad41a-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="ad41a-120">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="ad41a-120">Example 1</span></span>

<span data-ttu-id="ad41a-121">Izteiksme `ENDSWITH ("abc", "d")` atgriež **APLAMS**, savukārt izteiksme `ENDSWITH ("abc", "C")` atgriež **PATIESS**.</span><span class="sxs-lookup"><span data-stu-id="ad41a-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ad41a-122">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="ad41a-122">Example 2</span></span>

<span data-ttu-id="ad41a-123">Izteiksme `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` atgriež **PATIESS**, ja datu avota **modelis** lauka **Adrese** vērtība beidzas ar virkni **USA**.</span><span class="sxs-lookup"><span data-stu-id="ad41a-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="ad41a-124">Pretējā gadījumā tā atgriež vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ad41a-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad41a-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ad41a-125">Additional resources</span></span>

[<span data-ttu-id="ad41a-126">Loģiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="ad41a-126">Logical functions</span></span>](er-functions-category-logical.md)
