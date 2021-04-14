---
title: FIRST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FIRST elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: d30c8481866ccf3f7080197b37586a0460a4ad2c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746583"
---
# <a name="first-er-function"></a><span data-ttu-id="150c0-103">FIRST ER funkcija</span><span class="sxs-lookup"><span data-stu-id="150c0-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="150c0-104">`FIRST` funkcija atgriež norādītā saraksta pirmo ierakstu kā vērtību *Konteiners (ieraksts)*, ja šis saraksts nav tukšs.</span><span class="sxs-lookup"><span data-stu-id="150c0-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="150c0-105">Ja saraksts ir tukšs, šī funkcija rādīs izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="150c0-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="150c0-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="150c0-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="150c0-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="150c0-107">Arguments</span></span>

<span data-ttu-id="150c0-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="150c0-108">`list`: *Record list*</span></span>

<span data-ttu-id="150c0-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="150c0-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="150c0-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="150c0-110">Return values</span></span>

<span data-ttu-id="150c0-111">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="150c0-111">*Container (record)*</span></span>

<span data-ttu-id="150c0-112">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="150c0-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="150c0-113">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="150c0-113">Example 1</span></span>

<span data-ttu-id="150c0-114">Izteiksme `FIRST(SPLIT("ABC",1)).Value` atgriež teksta vērtību **"A".**</span><span class="sxs-lookup"><span data-stu-id="150c0-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="150c0-115">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="150c0-115">Example 2</span></span>

<span data-ttu-id="150c0-116">Izteiksme `FIRST(SPLIT("",1)).Value` izpildlaikā rāda izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="150c0-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="150c0-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="150c0-117">Additional resources</span></span>

[<span data-ttu-id="150c0-118">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="150c0-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]