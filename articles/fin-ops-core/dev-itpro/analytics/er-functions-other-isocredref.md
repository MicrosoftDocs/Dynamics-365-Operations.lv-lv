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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041381"
---
# <span data-ttu-id="0a4c7-103"><a name="ISOCREDREF">ISOCREDREF ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="0a4c7-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a4c7-104">`ISOCREDREF` funkcija atgriež *Virknes* vērtību, kas apzīmē Starptautiskās Standartizācijas organizācijas (ISO) kreditora atsauci atbilstoši norādītā rēķina numura cipariem un burtiem.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4c7-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="0a4c7-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="0a4c7-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="0a4c7-106">Arguments</span></span>

<span data-ttu-id="0a4c7-107">`invoice number digits`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="0a4c7-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="0a4c7-108">Teksta vērtība, kas attēlo rēķina numura ciparus.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="0a4c7-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="0a4c7-109">Return values</span></span>

<span data-ttu-id="0a4c7-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="0a4c7-110">*String*</span></span>

<span data-ttu-id="0a4c7-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0a4c7-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="0a4c7-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="0a4c7-113">Lai izslēgtu alfabētu simbolus, kas nav saderīgi ar ISO, arguments `invoice number digits` pirms nodošanas šai funkcijai ir jātulko.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="0a4c7-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="0a4c7-114">Example</span></span>

<span data-ttu-id="0a4c7-115">`ISOCredRef ("VEND-200002")` atgriež **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a4c7-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0a4c7-116">Additional resources</span></span>

[<span data-ttu-id="0a4c7-117">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="0a4c7-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
