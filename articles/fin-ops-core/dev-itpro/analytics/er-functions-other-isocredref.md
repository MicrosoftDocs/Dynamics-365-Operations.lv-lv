---
title: ISOCREDREF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ISOCREDREF elektroniskā pārskata (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9a75cedcf543b318df2850df3e4a60bac2dc6b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680690"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="97cf8-103">ISOCREDREF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="97cf8-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97cf8-104">`ISOCREDREF` funkcija atgriež *Virknes* vērtību, kas apzīmē Starptautiskās Standartizācijas organizācijas (ISO) kreditora atsauci atbilstoši norādītā rēķina numura cipariem un burtiem.</span><span class="sxs-lookup"><span data-stu-id="97cf8-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="97cf8-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="97cf8-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="97cf8-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="97cf8-106">Arguments</span></span>

<span data-ttu-id="97cf8-107">`invoice number digits`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="97cf8-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="97cf8-108">Teksta vērtība, kas attēlo rēķina numura ciparus.</span><span class="sxs-lookup"><span data-stu-id="97cf8-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="97cf8-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="97cf8-109">Return values</span></span>

<span data-ttu-id="97cf8-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="97cf8-110">*String*</span></span>

<span data-ttu-id="97cf8-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="97cf8-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="97cf8-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="97cf8-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="97cf8-113">Lai izslēgtu alfabētu simbolus, kas nav saderīgi ar ISO, arguments `invoice number digits` pirms nodošanas šai funkcijai ir jātulko.</span><span class="sxs-lookup"><span data-stu-id="97cf8-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="97cf8-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="97cf8-114">Example</span></span>

<span data-ttu-id="97cf8-115">`ISOCredRef ("VEND-200002")` atgriež **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="97cf8-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97cf8-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="97cf8-116">Additional resources</span></span>

[<span data-ttu-id="97cf8-117">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="97cf8-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
