---
title: JSONVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota JSONVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746367"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="59261-103">JSONVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="59261-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59261-104">`JSONVALUE` funkcija parsē datus formātā JavaScript Object Notation (JSON), kuriem piekļūst pa norādīto ceļu un izgūst skalāru vērtību, kas ir balstīta uz norādīto ID.</span><span class="sxs-lookup"><span data-stu-id="59261-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="59261-105">Pēc tam tā atgriež izvērsto skalāro vērtību kā *Virknes* vērtību.</span><span class="sxs-lookup"><span data-stu-id="59261-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="59261-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="59261-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="59261-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="59261-107">Arguments</span></span>

<span data-ttu-id="59261-108">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="59261-108">`input`: *String*</span></span>

<span data-ttu-id="59261-109">*Virknes* tipa datu avota derīgs ceļš, kas satur JSON datus.</span><span class="sxs-lookup"><span data-stu-id="59261-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="59261-110">`path`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="59261-110">`path`: *String*</span></span>

<span data-ttu-id="59261-111">Skalārās JSON datu vērtības identifikators.</span><span class="sxs-lookup"><span data-stu-id="59261-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="59261-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="59261-112">Return values</span></span>

<span data-ttu-id="59261-113">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="59261-113">*String*</span></span>

<span data-ttu-id="59261-114">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="59261-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="59261-115">Paraugs</span><span class="sxs-lookup"><span data-stu-id="59261-115">Example</span></span>

<span data-ttu-id="59261-116">Datu avotā **JsonField** ir ietverti tālāk norādītie dati JSON formātā: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="59261-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="59261-117">Šādā gadījumā izteiksme `JSONVALUE (JsonField, "BuildNumber")` atgriež šādu vērtību *Virknes* datu tipam: **"7.3.1234.1".**</span><span class="sxs-lookup"><span data-stu-id="59261-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59261-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="59261-118">Additional resources</span></span>

[<span data-ttu-id="59261-119">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="59261-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]