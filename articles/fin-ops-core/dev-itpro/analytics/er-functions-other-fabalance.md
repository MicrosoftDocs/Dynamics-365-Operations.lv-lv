---
title: FA_BALANCE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FA_BALANCE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 37c440a5c626016ebdb75703a2be63c9a1a2b560
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567596"
---
# <a name="fa_balance-er-function"></a><span data-ttu-id="47bd7-103">FA_BALANCE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="47bd7-103">FA_BALANCE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47bd7-104">`FA_BALANCE` funkcija atgriež *Konteinera (ieraksta)* vērtību, kas sastāv no pamatlīdzekļa bilances datiem par norādīto pamatlīdzekļa krājumu, vērtības modeļa kodu, pārskata gadu un pārskata datumu.</span><span class="sxs-lookup"><span data-stu-id="47bd7-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="47bd7-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="47bd7-105">Syntax</span></span>

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="47bd7-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="47bd7-106">Arguments</span></span>

<span data-ttu-id="47bd7-107">`fixed asset code`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="47bd7-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="47bd7-108">*Virknes* vērtība, kas apzīmē pamatlīdzekļu krājuma kodu, kuram tiek aprēķināta bilance.</span><span class="sxs-lookup"><span data-stu-id="47bd7-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="47bd7-109">`value model code`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="47bd7-109">`value model code`: *String*</span></span>

<span data-ttu-id="47bd7-110">*Virknes* vērtība, kas apzīmē vērtības modeļa kodu, kuram tiek aprēķināta bilance.</span><span class="sxs-lookup"><span data-stu-id="47bd7-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="47bd7-111">`reporting year`: *Uzskaitījuma vērtība*</span><span class="sxs-lookup"><span data-stu-id="47bd7-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="47bd7-112">Uzskaitījuma vērtība **AssetYear** lietojumprogrammu uzskaitījumam, kas nosaka periodu bilances aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="47bd7-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="47bd7-113">`reporting date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="47bd7-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="47bd7-114">*Datuma* vērtība, kas definē bilances aprēķināšanas datumu.</span><span class="sxs-lookup"><span data-stu-id="47bd7-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="47bd7-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="47bd7-115">Return values</span></span>

<span data-ttu-id="47bd7-116">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="47bd7-116">*Container (record)*</span></span>

<span data-ttu-id="47bd7-117">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="47bd7-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="47bd7-118">Paraugs</span><span class="sxs-lookup"><span data-stu-id="47bd7-118">Example</span></span>

<span data-ttu-id="47bd7-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` atgriež sagatavoto datu konteineru no bilancēm pamatlīdzeklim **COMP-000001** ar vērtības modeli **Pašreizējais** pašreizējā programmas sesijas datumā.</span><span class="sxs-lookup"><span data-stu-id="47bd7-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47bd7-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="47bd7-120">Additional resources</span></span>

[<span data-ttu-id="47bd7-121">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="47bd7-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]