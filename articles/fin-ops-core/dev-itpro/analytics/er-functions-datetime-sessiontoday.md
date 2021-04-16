---
title: SESSIONTODAY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SESSIONTODAY elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746775"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="a9b73-103">SESSIONTODAY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="a9b73-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9b73-104">`SESSIONTODAY` funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu.</span><span class="sxs-lookup"><span data-stu-id="a9b73-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b73-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="a9b73-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="a9b73-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="a9b73-106">Return values</span></span>

<span data-ttu-id="a9b73-107">*Datums*</span><span class="sxs-lookup"><span data-stu-id="a9b73-107">*Date*</span></span>

<span data-ttu-id="a9b73-108">Iegūtā datuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="a9b73-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="a9b73-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="a9b73-109">Example</span></span>

<span data-ttu-id="a9b73-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datumu, 2015. gada 24. decembri, kā virkni **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.</span><span class="sxs-lookup"><span data-stu-id="a9b73-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9b73-111">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a9b73-111">Additional resources</span></span>

[<span data-ttu-id="a9b73-112">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="a9b73-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]