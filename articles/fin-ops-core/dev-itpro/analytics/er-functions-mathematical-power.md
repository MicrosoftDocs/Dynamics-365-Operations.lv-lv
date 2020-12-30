---
title: POWER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota POWER elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683333"
---
# <a name="power-er-function"></a><span data-ttu-id="6c6a4-103">POWER ER funkcija</span><span class="sxs-lookup"><span data-stu-id="6c6a4-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c6a4-104">`POWER` funkcija atgriež *Reālu* vērtību, kas atspoguļo rezultātu norādītā pozitīvā skaitļa palielināšanai līdz norādītajai jaudai.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6a4-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="6c6a4-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="6c6a4-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="6c6a4-106">Arguments</span></span>

<span data-ttu-id="6c6a4-107">`number`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="6c6a4-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="6c6a4-108">Skaitliska vērtība, kas ir jāpaaugstina līdz norādītajai jaudām.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="6c6a4-109">`power`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="6c6a4-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="6c6a4-110">Skaitliska vērtība, kas apzīmē konkrēto jaudu.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="6c6a4-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="6c6a4-111">Return values</span></span>

<span data-ttu-id="6c6a4-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="6c6a4-112">*Real*</span></span>

<span data-ttu-id="6c6a4-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="6c6a4-114">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="6c6a4-114">Example 1</span></span>

<span data-ttu-id="6c6a4-115">`POWER (10, 2)` atgriež **100**.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6c6a4-116">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="6c6a4-116">Example 2</span></span>

<span data-ttu-id="6c6a4-117">`POWER (4, 0.5)` atgriež **2**.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c6a4-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6c6a4-118">Additional resources</span></span>

[<span data-ttu-id="6c6a4-119">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="6c6a4-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
