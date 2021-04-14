---
title: IF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota IF elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: 3674618acae79170daf94413895d17d86a491996
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753172"
---
# <a name="if-er-function"></a><span data-ttu-id="b586f-103">IF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="b586f-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b586f-104">`IF` funkcija atgriež pirmo norādīto vērtību, ja tiek izpildīts norādītais nosacījums.</span><span class="sxs-lookup"><span data-stu-id="b586f-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="b586f-105">Pretējā gadījumā tiek atgriezta otrā norādītā vērtība.</span><span class="sxs-lookup"><span data-stu-id="b586f-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="b586f-106">Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība.</span><span class="sxs-lookup"><span data-stu-id="b586f-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="b586f-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="b586f-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="b586f-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="b586f-108">Arguments</span></span>

<span data-ttu-id="b586f-109">`condition`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="b586f-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="b586f-110">Derīga nosacījuma izteiksme, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="b586f-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="b586f-111">`first value`: *Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="b586f-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="b586f-112">Rezultāts, kas tiek atgriezts, ja nosacījums ir izpildīts.</span><span class="sxs-lookup"><span data-stu-id="b586f-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="b586f-113">`second value`: *Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="b586f-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="b586f-114">Rezultāts, kas tiek atgriezts, ja nosacījums nav izpildīts.</span><span class="sxs-lookup"><span data-stu-id="b586f-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="b586f-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="b586f-115">Return values</span></span>

<span data-ttu-id="b586f-116">*Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="b586f-116">*Any of the supported data types*</span></span>

<span data-ttu-id="b586f-117">Jebkura atbalstītā datu tipa iegūtā vērtība.</span><span class="sxs-lookup"><span data-stu-id="b586f-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b586f-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="b586f-118">Usage notes</span></span>

<span data-ttu-id="b586f-119">Argumenti `first value` un `second value` ir jānorāda, izmantojot vienu datu tipu.</span><span class="sxs-lookup"><span data-stu-id="b586f-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="b586f-120">Noformēšanas laikā tiek parādīts izņēmums, ja konfigurētās vērtības nesakrīt.</span><span class="sxs-lookup"><span data-stu-id="b586f-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="b586f-121">Ja pirmā rezultāta vērtība un otrā rezultāta vērtība ir *Konteinera (ieraksta)* vai *Ierakstu saraksta* datu tipa vērtības, rezultātam ir tikai tie lauki, kas ir abās vērtībās.</span><span class="sxs-lookup"><span data-stu-id="b586f-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="b586f-122">Paraugs</span><span class="sxs-lookup"><span data-stu-id="b586f-122">Example</span></span>

<span data-ttu-id="b586f-123">`IF (1=2, "condition is met", "condition is not met")` atgriež virkni **"nosacījums nav izpildīts"**.</span><span class="sxs-lookup"><span data-stu-id="b586f-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b586f-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b586f-124">Additional resources</span></span>

[<span data-ttu-id="b586f-125">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="b586f-125">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]