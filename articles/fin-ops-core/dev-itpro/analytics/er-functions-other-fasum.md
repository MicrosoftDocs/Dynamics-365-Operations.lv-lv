---
title: FA_SUM ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FA_SUM elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: fccd318a8ab67528f0ce048fc770a2037f625d7a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744146"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="7c7c9-103">FA_SUM ER funkcija</span><span class="sxs-lookup"><span data-stu-id="7c7c9-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c7c9-104">`FA_SUM` funkcija atgriež *Konteinera (ieraksta)* vērtību, kas sastāv no pamatlīdzekļa summu datiem par norādīto pamatlīdzekļa krājumu, vērtības modeļa kodu, pārskata gadu un datumu periodu.</span><span class="sxs-lookup"><span data-stu-id="7c7c9-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7c9-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="7c7c9-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="7c7c9-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="7c7c9-106">Arguments</span></span>

<span data-ttu-id="7c7c9-107">`fixed asset code`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="7c7c9-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="7c7c9-108">*Virknes* vērtība, kas apzīmē pamatlīdzekļu krājuma kodu, kuram tiek aprēķināta bilance.</span><span class="sxs-lookup"><span data-stu-id="7c7c9-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="7c7c9-109">`value model code`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="7c7c9-109">`value model code`: *String*</span></span>

<span data-ttu-id="7c7c9-110">*Virknes* vērtība, kas apzīmē vērtības modeļa kodu, kuram tiek aprēķināta bilance.</span><span class="sxs-lookup"><span data-stu-id="7c7c9-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="7c7c9-111">`start date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="7c7c9-111">`start date`: *Date*</span></span>

<span data-ttu-id="7c7c9-112">*Datuma* vērtība, kas apzīmē sākuma datumu periodam, kuram tiek aprēķinātas pamatlīdzekļu summas.</span><span class="sxs-lookup"><span data-stu-id="7c7c9-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="7c7c9-113">`end date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="7c7c9-113">`end date`: *Date*</span></span>

<span data-ttu-id="7c7c9-114">*Datuma* vērtība, kas apzīmē beigu datumu periodam, kuram tiek aprēķinātas pamatlīdzekļu summas.</span><span class="sxs-lookup"><span data-stu-id="7c7c9-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="7c7c9-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="7c7c9-115">Return values</span></span>

<span data-ttu-id="7c7c9-116">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="7c7c9-116">*Container (record)*</span></span>

<span data-ttu-id="7c7c9-117">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="7c7c9-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="7c7c9-118">Paraugs</span><span class="sxs-lookup"><span data-stu-id="7c7c9-118">Example</span></span>

<span data-ttu-id="7c7c9-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` atgriež pamatlīdzekļa **COMP-000001** datu konteineru, kas ir sagatavots **Pašreizējam** vērtības modelim un periodam no **Date1** līdz **Date2**.</span><span class="sxs-lookup"><span data-stu-id="7c7c9-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c7c9-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7c7c9-120">Additional resources</span></span>

[<span data-ttu-id="7c7c9-121">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="7c7c9-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
