---
title: FIRST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FIRST elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917354"
---
# <span data-ttu-id="97f3b-103"><a name="FIRST">FIRST ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="97f3b-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97f3b-104">`FIRST` funkcija atgriež norādītā saraksta pirmo ierakstu kā vērtību *Konteiners (ieraksts)*, ja šis saraksts nav tukšs.</span><span class="sxs-lookup"><span data-stu-id="97f3b-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="97f3b-105">Ja saraksts ir tukšs, šī funkcija rādīs izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="97f3b-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f3b-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="97f3b-106">Syntax</span></span>

```
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="97f3b-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="97f3b-107">Arguments</span></span>

<span data-ttu-id="97f3b-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="97f3b-108">`list`: *Record list*</span></span>

<span data-ttu-id="97f3b-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="97f3b-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="97f3b-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="97f3b-110">Return values</span></span>

<span data-ttu-id="97f3b-111">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="97f3b-111">*Container (record)*</span></span>

<span data-ttu-id="97f3b-112">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="97f3b-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="97f3b-113">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="97f3b-113">Example 1</span></span>

<span data-ttu-id="97f3b-114">Izteiksme `FIRST(SPLIT("ABC",1)).Value` atgriež teksta vērtību **"A".**</span><span class="sxs-lookup"><span data-stu-id="97f3b-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="97f3b-115">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="97f3b-115">Example 2</span></span>

<span data-ttu-id="97f3b-116">Izteiksme `FIRST(SPLIT("",1)).Value` izpildlaikā rāda izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="97f3b-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97f3b-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="97f3b-117">Additional resources</span></span>

[<span data-ttu-id="97f3b-118">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="97f3b-118">List functions</span></span>](er-functions-category-list.md)