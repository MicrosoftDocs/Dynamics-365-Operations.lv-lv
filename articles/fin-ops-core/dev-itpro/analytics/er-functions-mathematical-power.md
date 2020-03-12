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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c57222d7fcc133faa679bab43431272c984c9d8b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041634"
---
# <span data-ttu-id="be138-103"><a name="POWER">POWER ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="be138-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be138-104">`POWER` funkcija atgriež *Reālu* vērtību, kas atspoguļo rezultātu norādītā pozitīvā skaitļa palielināšanai līdz norādītajai jaudai.</span><span class="sxs-lookup"><span data-stu-id="be138-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="be138-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="be138-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="be138-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="be138-106">Arguments</span></span>

<span data-ttu-id="be138-107">`number`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="be138-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="be138-108">Skaitliska vērtība, kas ir jāpaaugstina līdz norādītajai jaudām.</span><span class="sxs-lookup"><span data-stu-id="be138-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="be138-109">`power`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="be138-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="be138-110">Skaitliska vērtība, kas apzīmē konkrēto jaudu.</span><span class="sxs-lookup"><span data-stu-id="be138-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="be138-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="be138-111">Return values</span></span>

<span data-ttu-id="be138-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="be138-112">*Real*</span></span>

<span data-ttu-id="be138-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="be138-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="be138-114">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="be138-114">Example 1</span></span>

<span data-ttu-id="be138-115">`POWER (10, 2)` atgriež **100**.</span><span class="sxs-lookup"><span data-stu-id="be138-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="be138-116">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="be138-116">Example 2</span></span>

<span data-ttu-id="be138-117">`POWER (4, 0.5)` atgriež **2**.</span><span class="sxs-lookup"><span data-stu-id="be138-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be138-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="be138-118">Additional resources</span></span>

[<span data-ttu-id="be138-119">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="be138-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
