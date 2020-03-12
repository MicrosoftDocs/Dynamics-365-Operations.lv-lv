---
title: TABLENAME2ID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TABLENAME2ID elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 951de1d1505508ebb6abeff5b80ecef10573e117
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041272"
---
# <span data-ttu-id="c4c02-103"><a name="TABLENAME2ID">TABLENAME2ID ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="c4c02-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4c02-104">`TABLENAME2ID` funkcija atgriež tabulas ID skaitlisko attēlojumu norādītajam tabulas nosaukumam kā *Vesela skaitļa* vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4c02-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c02-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="c4c02-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="c4c02-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="c4c02-106">Arguments</span></span>

<span data-ttu-id="c4c02-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="c4c02-107">`text`: *String*</span></span>

<span data-ttu-id="c4c02-108">Teksta vērtība, kas apzīmē derīgu tabulas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c4c02-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="c4c02-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="c4c02-109">Return values</span></span>

<span data-ttu-id="c4c02-110">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="c4c02-110">*Integer*</span></span>

<span data-ttu-id="c4c02-111">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="c4c02-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c4c02-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="c4c02-112">Usage notes</span></span>

<span data-ttu-id="c4c02-113">Šīs funkcijas izpildei var būt atšķirīgi rezultāti dažādās Microsoft Dynamics 365 Finance instancēs, pat ja tiek izmantots viens un tas pats uzņēmuma nosaukums.</span><span class="sxs-lookup"><span data-stu-id="c4c02-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="c4c02-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="c4c02-114">Example</span></span>

<span data-ttu-id="c4c02-115">`TABLENAME2ID ("Intrastat")` atgriež **1510**.</span><span class="sxs-lookup"><span data-stu-id="c4c02-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4c02-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c4c02-116">Additional resources</span></span>

[<span data-ttu-id="c4c02-117">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="c4c02-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
