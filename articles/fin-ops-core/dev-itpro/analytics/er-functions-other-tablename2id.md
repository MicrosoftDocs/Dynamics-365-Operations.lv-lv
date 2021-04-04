---
title: TABLENAME2ID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TABLENAME2ID elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563274"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="b41d6-103">TABLENAME2ID ER funkcija</span><span class="sxs-lookup"><span data-stu-id="b41d6-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b41d6-104">`TABLENAME2ID` funkcija atgriež tabulas ID skaitlisko attēlojumu norādītajam tabulas nosaukumam kā *Vesela skaitļa* vērtību.</span><span class="sxs-lookup"><span data-stu-id="b41d6-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b41d6-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="b41d6-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="b41d6-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="b41d6-106">Arguments</span></span>

<span data-ttu-id="b41d6-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="b41d6-107">`text`: *String*</span></span>

<span data-ttu-id="b41d6-108">Teksta vērtība, kas apzīmē derīgu tabulas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b41d6-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="b41d6-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="b41d6-109">Return values</span></span>

<span data-ttu-id="b41d6-110">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="b41d6-110">*Integer*</span></span>

<span data-ttu-id="b41d6-111">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="b41d6-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b41d6-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="b41d6-112">Usage notes</span></span>

<span data-ttu-id="b41d6-113">Šīs funkcijas izpildei var būt atšķirīgi rezultāti dažādās Microsoft Dynamics 365 Finance instancēs, pat ja tiek izmantots viens un tas pats uzņēmuma nosaukums.</span><span class="sxs-lookup"><span data-stu-id="b41d6-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="b41d6-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="b41d6-114">Example</span></span>

<span data-ttu-id="b41d6-115">`TABLENAME2ID ("Intrastat")` atgriež **1510**.</span><span class="sxs-lookup"><span data-stu-id="b41d6-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b41d6-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b41d6-116">Additional resources</span></span>

[<span data-ttu-id="b41d6-117">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="b41d6-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]