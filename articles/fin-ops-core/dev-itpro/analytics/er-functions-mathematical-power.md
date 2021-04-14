---
title: POWER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota POWER elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750160"
---
# <a name="power-er-function"></a><span data-ttu-id="adbf0-103">POWER ER funkcija</span><span class="sxs-lookup"><span data-stu-id="adbf0-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adbf0-104">`POWER` funkcija atgriež *Reālu* vērtību, kas atspoguļo rezultātu norādītā pozitīvā skaitļa palielināšanai līdz norādītajai jaudai.</span><span class="sxs-lookup"><span data-stu-id="adbf0-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="adbf0-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="adbf0-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="adbf0-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="adbf0-106">Arguments</span></span>

<span data-ttu-id="adbf0-107">`number`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="adbf0-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="adbf0-108">Skaitliska vērtība, kas ir jāpaaugstina līdz norādītajai jaudām.</span><span class="sxs-lookup"><span data-stu-id="adbf0-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="adbf0-109">`power`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="adbf0-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="adbf0-110">Skaitliska vērtība, kas apzīmē konkrēto jaudu.</span><span class="sxs-lookup"><span data-stu-id="adbf0-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="adbf0-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="adbf0-111">Return values</span></span>

<span data-ttu-id="adbf0-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="adbf0-112">*Real*</span></span>

<span data-ttu-id="adbf0-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="adbf0-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="adbf0-114">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="adbf0-114">Example 1</span></span>

<span data-ttu-id="adbf0-115">`POWER (10, 2)` atgriež **100**.</span><span class="sxs-lookup"><span data-stu-id="adbf0-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="adbf0-116">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="adbf0-116">Example 2</span></span>

<span data-ttu-id="adbf0-117">`POWER (4, 0.5)` atgriež **2**.</span><span class="sxs-lookup"><span data-stu-id="adbf0-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adbf0-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="adbf0-118">Additional resources</span></span>

[<span data-ttu-id="adbf0-119">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="adbf0-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]