---
title: STARTSWITH ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota STARTSWITH elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 22e99d9e131410820abd12536b8d4f3e868c6863
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557537"
---
# <a name="startswith-er-function"></a><span data-ttu-id="3514c-103">STARTSWITH ER funkcija</span><span class="sxs-lookup"><span data-stu-id="3514c-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3514c-104">`STARTSWITH` funkcija nosaka, vai norādītā ievade sākas ar norādīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="3514c-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="3514c-105">Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade sākas ar norādīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="3514c-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="3514c-106">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="3514c-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3514c-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="3514c-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="3514c-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="3514c-108">Arguments</span></span>

<span data-ttu-id="3514c-109">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="3514c-109">`input`: *String*</span></span>

<span data-ttu-id="3514c-110">Veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var sākties ar otro argumentu.</span><span class="sxs-lookup"><span data-stu-id="3514c-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="3514c-111">`start text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="3514c-111">`start text`: *String*</span></span>

<span data-ttu-id="3514c-112">Datu veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var būt pirmā argumenta sākumā.</span><span class="sxs-lookup"><span data-stu-id="3514c-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="3514c-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="3514c-113">Return values</span></span>

<span data-ttu-id="3514c-114">*Būla*</span><span class="sxs-lookup"><span data-stu-id="3514c-114">*Boolean*</span></span>

<span data-ttu-id="3514c-115">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="3514c-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3514c-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="3514c-116">Usage notes</span></span>

<span data-ttu-id="3514c-117">Šo funkciju var izmantot funkcijas [FILTER](er-functions-list-filter.md) nosacījuma izteiksmes norādīšanai tikai tad, ja atbilstošā kartēšana ir konfigurēta [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md), lai piekļūtu [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="3514c-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="3514c-118">Pretējā gadījumā izstrādes laikā tiek izmests izņēmums.</span><span class="sxs-lookup"><span data-stu-id="3514c-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="3514c-119">Saņemtais ziņojums iesaka izmantot funkciju [WHERE](er-functions-list-where.md), nevis funkciju `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="3514c-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="3514c-120">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="3514c-120">Example 1</span></span>

<span data-ttu-id="3514c-121">Izteiksme `STARTSWITH ("abc", "d")` atgriež **APLAMS**, savukārt izteiksme `STARTSWITH ("abc", "A")` atgriež **PATIESS**.</span><span class="sxs-lookup"><span data-stu-id="3514c-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3514c-122">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="3514c-122">Example 2</span></span>

<span data-ttu-id="3514c-123">Izteiksme `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` atgriež **PATIESS**, ja datu avota **modelis** lauka **Adrese** vērtība sākas ar virkni **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="3514c-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="3514c-124">Pretējā gadījumā tā atgriež vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="3514c-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3514c-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3514c-125">Additional resources</span></span>

[<span data-ttu-id="3514c-126">Loģiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="3514c-126">Logical functions</span></span>](er-functions-category-logical.md)
