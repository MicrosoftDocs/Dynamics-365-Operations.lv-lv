---
title: GUIDVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota GUIDVALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 552c6a42dd0e189f2f8404ce5d7f7a68fec1b216
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564342"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="55046-103">GUIDVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="55046-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55046-104">`GUIDVALUE` funkcija konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *GUID*.</span><span class="sxs-lookup"><span data-stu-id="55046-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="55046-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="55046-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="55046-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="55046-106">Arguments</span></span>

<span data-ttu-id="55046-107">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="55046-107">`input`: *String*</span></span>

<span data-ttu-id="55046-108">*Virknes* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="55046-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="55046-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="55046-109">Return values</span></span>

<span data-ttu-id="55046-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="55046-110">*GUID*</span></span>

<span data-ttu-id="55046-111">Iegūtā globāli unikālā identifikatora (GUID) vērtība.</span><span class="sxs-lookup"><span data-stu-id="55046-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="55046-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="55046-112">Usage notes</span></span>

<span data-ttu-id="55046-113">Lai veiktu konvertēšanu pretējā virzienā (tas ir, lai norādīto ievadi ar datu tipu *GUID* konvertētu uz datu elementu ar datu tipu *Virkne* ), varat izmantot funkciju [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="55046-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="55046-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="55046-114">Example</span></span>

<span data-ttu-id="55046-115">Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.</span><span class="sxs-lookup"><span data-stu-id="55046-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="55046-116">Datu avots **myID** no veida *Aprēķinātais lauks*, kas satur izteiksmi `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="55046-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="55046-117">**Users** datu avots no veida *Tabulas ieraksti*, kas atsaucas uz tabulu UserInfo</span><span class="sxs-lookup"><span data-stu-id="55046-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="55046-118">Pēc tam varat izmantot izteiksmi, piemēram, `FILTER (Users, Users.objectId = myID)`, lai filtrētu tabulu UserInfo pēc lauka **objectId** ar datu tipu *GUID.*</span><span class="sxs-lookup"><span data-stu-id="55046-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55046-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="55046-119">Additional resources</span></span>

[<span data-ttu-id="55046-120">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="55046-120">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]