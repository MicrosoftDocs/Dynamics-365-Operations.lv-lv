---
title: ISOCREDREF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ISOCREDREF elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748321"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="ca296-103">ISOCREDREF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="ca296-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca296-104">`ISOCREDREF` funkcija atgriež *Virknes* vērtību, kas apzīmē Starptautiskās Standartizācijas organizācijas (ISO) kreditora atsauci atbilstoši norādītā rēķina numura cipariem un burtiem.</span><span class="sxs-lookup"><span data-stu-id="ca296-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca296-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="ca296-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="ca296-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="ca296-106">Arguments</span></span>

<span data-ttu-id="ca296-107">`invoice number digits`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="ca296-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="ca296-108">Teksta vērtība, kas attēlo rēķina numura ciparus.</span><span class="sxs-lookup"><span data-stu-id="ca296-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="ca296-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="ca296-109">Return values</span></span>

<span data-ttu-id="ca296-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="ca296-110">*String*</span></span>

<span data-ttu-id="ca296-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="ca296-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ca296-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="ca296-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="ca296-113">Lai izslēgtu alfabētu simbolus, kas nav saderīgi ar ISO, arguments `invoice number digits` pirms nodošanas šai funkcijai ir jātulko.</span><span class="sxs-lookup"><span data-stu-id="ca296-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="ca296-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="ca296-114">Example</span></span>

<span data-ttu-id="ca296-115">`ISOCredRef ("VEND-200002")` atgriež **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="ca296-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca296-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ca296-116">Additional resources</span></span>

[<span data-ttu-id="ca296-117">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="ca296-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]