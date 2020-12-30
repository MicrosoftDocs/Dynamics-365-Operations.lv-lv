---
title: TEXT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TEXT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d489da24d0589549153913bbc6db699e3c217e72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682899"
---
# <a name="text-er-function"></a><span data-ttu-id="d7ed8-103">TEXT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="d7ed8-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7ed8-104">`TEXT` funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tā ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās programmas instances servera lokalizācijas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="d7ed8-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ed8-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="d7ed8-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="d7ed8-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d7ed8-106">Arguments</span></span>

<span data-ttu-id="d7ed8-107">`number`: *Vesels skaitlis* vai *Reāls*</span><span class="sxs-lookup"><span data-stu-id="d7ed8-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="d7ed8-108">Skaitlis, kas ir jāpārvērš par teksta virkni.</span><span class="sxs-lookup"><span data-stu-id="d7ed8-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7ed8-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d7ed8-109">Return values</span></span>

<span data-ttu-id="d7ed8-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="d7ed8-110">*String*</span></span>

<span data-ttu-id="d7ed8-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="d7ed8-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d7ed8-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="d7ed8-112">Usage notes</span></span>

<span data-ttu-id="d7ed8-113">Vērtībām ar tipu *Reāls* šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.</span><span class="sxs-lookup"><span data-stu-id="d7ed8-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="d7ed8-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="d7ed8-114">Example</span></span>

<span data-ttu-id="d7ed8-115">Ja Microsoft Dynamics 365 Finance instances servera lokalizācija ir definēta kā **EN-US**, `TEXT (NOW ())` pašreizējo Finance sesijas datumu, 2015. gada 17. decembri, atgriež kā teksta virkni **"12/17/2015 07:59:23 AM"**.</span><span class="sxs-lookup"><span data-stu-id="d7ed8-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="d7ed8-116">`TEXT (1/3)` atgriež **"0.33"**.</span><span class="sxs-lookup"><span data-stu-id="d7ed8-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7ed8-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d7ed8-117">Additional resources</span></span>

[<span data-ttu-id="d7ed8-118">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="d7ed8-118">Text functions</span></span>](er-functions-category-text.md)
