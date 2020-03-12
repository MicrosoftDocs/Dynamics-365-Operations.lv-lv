---
title: GUIDVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota GUIDVALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: a7b8c782aff488a433c40a49ab7f4fe2d0e944e4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041182"
---
# <span data-ttu-id="24ea2-103"><a name="GUIDVALUE">GUIDVALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="24ea2-103"><a name="GUIDVALUE">GUIDVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24ea2-104">`GUIDVALUE` funkcija konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *GUID*.</span><span class="sxs-lookup"><span data-stu-id="24ea2-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ea2-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="24ea2-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="24ea2-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="24ea2-106">Arguments</span></span>

<span data-ttu-id="24ea2-107">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="24ea2-107">`input`: *String*</span></span>

<span data-ttu-id="24ea2-108">*Virknes* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="24ea2-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="24ea2-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="24ea2-109">Return values</span></span>

<span data-ttu-id="24ea2-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="24ea2-110">*GUID*</span></span>

<span data-ttu-id="24ea2-111">Iegūtā globāli unikālā identifikatora (GUID) vērtība.</span><span class="sxs-lookup"><span data-stu-id="24ea2-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="24ea2-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="24ea2-112">Usage notes</span></span>

<span data-ttu-id="24ea2-113">Lai veiktu konvertēšanu pretējā virzienā (tas ir, lai norādīto ievadi ar datu tipu *GUID* konvertētu uz datu elementu ar datu tipu *Virkne* ), varat izmantot funkciju [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="24ea2-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="24ea2-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="24ea2-114">Example</span></span>

<span data-ttu-id="24ea2-115">Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.</span><span class="sxs-lookup"><span data-stu-id="24ea2-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="24ea2-116">Datu avots **myID** no veida *Aprēķinātais lauks*, kas satur izteiksmi `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="24ea2-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="24ea2-117">**Users** datu avots no veida *Tabulas ieraksti*, kas atsaucas uz tabulu UserInfo</span><span class="sxs-lookup"><span data-stu-id="24ea2-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="24ea2-118">Pēc tam varat izmantot izteiksmi, piemēram, `FILTER (Users, Users.objectId = myID)`, lai filtrētu tabulu UserInfo pēc lauka **objectId** ar datu tipu *GUID.*</span><span class="sxs-lookup"><span data-stu-id="24ea2-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24ea2-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="24ea2-119">Additional resources</span></span>

[<span data-ttu-id="24ea2-120">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="24ea2-120">Text functions</span></span>](er-functions-category-text.md)
