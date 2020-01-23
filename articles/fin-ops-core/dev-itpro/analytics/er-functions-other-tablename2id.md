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
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915813"
---
# <span data-ttu-id="94b8f-103"><a name="TABLENAME2ID">TABLENAME2ID ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="94b8f-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94b8f-104">`TABLENAME2ID` funkcija atgriež tabulas ID skaitlisko attēlojumu norādītajam tabulas nosaukumam kā *Vesela skaitļa* vērtību.</span><span class="sxs-lookup"><span data-stu-id="94b8f-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b8f-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="94b8f-105">Syntax</span></span>

```
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="94b8f-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="94b8f-106">Arguments</span></span>

<span data-ttu-id="94b8f-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="94b8f-107">`text`: *String*</span></span>

<span data-ttu-id="94b8f-108">Teksta vērtība, kas apzīmē derīgu tabulas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="94b8f-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="94b8f-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="94b8f-109">Return values</span></span>

<span data-ttu-id="94b8f-110">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="94b8f-110">*Integer*</span></span>

<span data-ttu-id="94b8f-111">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="94b8f-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="94b8f-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="94b8f-112">Usage notes</span></span>

<span data-ttu-id="94b8f-113">Šīs funkcijas izpildei var būt atšķirīgi rezultāti dažādās Microsoft Dynamics 365 Finance instancēs, pat ja tiek izmantots viens un tas pats uzņēmuma nosaukums.</span><span class="sxs-lookup"><span data-stu-id="94b8f-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="94b8f-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="94b8f-114">Example</span></span>

<span data-ttu-id="94b8f-115">`TABLENAME2ID ("Intrastat")` atgriež **1510**.</span><span class="sxs-lookup"><span data-stu-id="94b8f-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94b8f-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="94b8f-116">Additional resources</span></span>

[<span data-ttu-id="94b8f-117">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="94b8f-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
