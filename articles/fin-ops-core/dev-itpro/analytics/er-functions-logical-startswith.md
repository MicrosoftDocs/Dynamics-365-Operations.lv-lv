---
title: STARTSWITH ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota STARTSWITH elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: ef7e9c88abff2b4b58ecb8abf1e69f7853f9b3fa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751684"
---
# <a name="startswith-er-function"></a><span data-ttu-id="aff64-103">STARTSWITH ER funkcija</span><span class="sxs-lookup"><span data-stu-id="aff64-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aff64-104">`STARTSWITH` funkcija nosaka, vai norādītā ievade sākas ar norādīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="aff64-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="aff64-105">Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade sākas ar norādīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="aff64-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="aff64-106">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="aff64-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff64-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="aff64-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="aff64-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="aff64-108">Arguments</span></span>

<span data-ttu-id="aff64-109">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="aff64-109">`input`: *String*</span></span>

<span data-ttu-id="aff64-110">Veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var sākties ar otro argumentu.</span><span class="sxs-lookup"><span data-stu-id="aff64-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="aff64-111">`start text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="aff64-111">`start text`: *String*</span></span>

<span data-ttu-id="aff64-112">Datu veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var būt pirmā argumenta sākumā.</span><span class="sxs-lookup"><span data-stu-id="aff64-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="aff64-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="aff64-113">Return values</span></span>

<span data-ttu-id="aff64-114">*Būla*</span><span class="sxs-lookup"><span data-stu-id="aff64-114">*Boolean*</span></span>

<span data-ttu-id="aff64-115">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="aff64-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="aff64-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="aff64-116">Usage notes</span></span>

<span data-ttu-id="aff64-117">Šo funkciju var izmantot funkcijas [FILTER](er-functions-list-filter.md) nosacījuma izteiksmes norādīšanai tikai tad, ja atbilstošā kartēšana ir konfigurēta [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md), lai piekļūtu [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="aff64-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="aff64-118">Pretējā gadījumā izstrādes laikā tiek izmests izņēmums.</span><span class="sxs-lookup"><span data-stu-id="aff64-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="aff64-119">Saņemtais ziņojums iesaka izmantot funkciju [WHERE](er-functions-list-where.md), nevis funkciju `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="aff64-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="aff64-120">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="aff64-120">Example 1</span></span>

<span data-ttu-id="aff64-121">Izteiksme `STARTSWITH ("abc", "d")` atgriež **APLAMS**, savukārt izteiksme `STARTSWITH ("abc", "A")` atgriež **PATIESS**.</span><span class="sxs-lookup"><span data-stu-id="aff64-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="aff64-122">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="aff64-122">Example 2</span></span>

<span data-ttu-id="aff64-123">Izteiksme `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` atgriež **PATIESS**, ja datu avota **modelis** lauka **Adrese** vērtība sākas ar virkni **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="aff64-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="aff64-124">Pretējā gadījumā tā atgriež vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="aff64-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aff64-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="aff64-125">Additional resources</span></span>

[<span data-ttu-id="aff64-126">Loģiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="aff64-126">Logical functions</span></span>](er-functions-category-logical.md)
