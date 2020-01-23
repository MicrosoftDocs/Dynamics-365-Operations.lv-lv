---
title: SPLIT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SPLIT elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 31caf7c728a92d31428f47320c074fa9fc35bda6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916112"
---
# <span data-ttu-id="d8a73-103"><a name="SPLIT">SPLIT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="d8a73-103"><a name="SPLIT">SPLIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8a73-104">`SPLIT` funkcija sadala norādīto ievades virkni apakšvirknēs un atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību.</span><span class="sxs-lookup"><span data-stu-id="d8a73-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d8a73-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="d8a73-105">Syntax 1</span></span>

```
SPLIT (input, length)
```

<span data-ttu-id="d8a73-106">Šo sintaksi izmanto, lai norādīto ievades virkni sadalītu apakšvirknēs, katrai no kurām ir norādīts garums.</span><span class="sxs-lookup"><span data-stu-id="d8a73-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="d8a73-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="d8a73-107">Syntax 2</span></span>

```
SPLIT (input, delimiter)
```

<span data-ttu-id="d8a73-108">Šo sintaksi izmanto, lai norādīto ievades virkni sadalītu apakšvirknēs, pamatojoties uz norādīto norobežotāju.</span><span class="sxs-lookup"><span data-stu-id="d8a73-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="d8a73-109">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d8a73-109">Arguments</span></span>

<span data-ttu-id="d8a73-110">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d8a73-110">`input`: *String*</span></span>

<span data-ttu-id="d8a73-111">Sadalāmais teksts.</span><span class="sxs-lookup"><span data-stu-id="d8a73-111">The text to split.</span></span>

<span data-ttu-id="d8a73-112">`length`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="d8a73-112">`length`: *Integer*</span></span>

<span data-ttu-id="d8a73-113">Vienas apakšvirknes maksimālais garums.</span><span class="sxs-lookup"><span data-stu-id="d8a73-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="d8a73-114">`delimiter`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d8a73-114">`delimiter`: *String*</span></span>

<span data-ttu-id="d8a73-115">Norobežotājs, ko izmanto, lai atdalītu apakšvirknes.</span><span class="sxs-lookup"><span data-stu-id="d8a73-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="d8a73-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d8a73-116">Return values</span></span>

<span data-ttu-id="d8a73-117">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="d8a73-117">*Record list*</span></span>

<span data-ttu-id="d8a73-118">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="d8a73-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d8a73-119">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="d8a73-119">Usage notes</span></span>

<span data-ttu-id="d8a73-120">Atgrieztā saraksta ieraksta struktūra sastāv no **Virknes** tipa *Vērtības* lauka.</span><span class="sxs-lookup"><span data-stu-id="d8a73-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="d8a73-121">Katrā atgrieztā saraksta ierakstā ir šajā laukā ģenerētās apakšvirknes.</span><span class="sxs-lookup"><span data-stu-id="d8a73-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="d8a73-122">Ja  `delimiter` arguments ir tukšs, tiek atgriezts jauns saraksts, kas sastāv no viena ieraksta, kurā ir **Virknes** veida lauks *Vērtība*.</span><span class="sxs-lookup"><span data-stu-id="d8a73-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="d8a73-123">Šis lauks satur ievades tekstu.</span><span class="sxs-lookup"><span data-stu-id="d8a73-123">This field contains the input text.</span></span>

<span data-ttu-id="d8a73-124">Ja `input` arguments ir tukšs, tiek atgriezts jauns tukšs saraksts.</span><span class="sxs-lookup"><span data-stu-id="d8a73-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="d8a73-125">Ja `input` vai `delimiter` arguments nav norādīts (ir tukšs), tiek parādīts programmas izņēmums.</span><span class="sxs-lookup"><span data-stu-id="d8a73-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="d8a73-126">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="d8a73-126">Example 1</span></span>

<span data-ttu-id="d8a73-127">`SPLIT ("abcd", 3)` atgriež jaunu sarakstu, kas sastāv no diviem ierakstiem ar **Virknes** veida lauku *Vērtība*.</span><span class="sxs-lookup"><span data-stu-id="d8a73-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="d8a73-128">Pirmā ieraksta lauks **Vērtība** ietver tekstu **"abc"**, un otrā ieraksta lauks **Vērtība** satur tekstu **"d"**.</span><span class="sxs-lookup"><span data-stu-id="d8a73-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d8a73-129">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="d8a73-129">Example 2</span></span>

<span data-ttu-id="d8a73-130">`SPLIT ("XAb aBy", "aB")` atgriež jaunu sarakstu, kas sastāv no trim ierakstiem ar **Virknes** veida lauku *Vērtība*.</span><span class="sxs-lookup"><span data-stu-id="d8a73-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="d8a73-131">Laukam **Vērtība** pirmajā ierakstā ir teksts **"X"**, laukam **Vērtība** otrajā ierakstā ir teksts **"&nbsp;"**, un laukam **Vērtība** trešajā ierakstā ir teksts **"y"**.</span><span class="sxs-lookup"><span data-stu-id="d8a73-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d8a73-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d8a73-132">Additional resources</span></span>

[<span data-ttu-id="d8a73-133">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="d8a73-133">List functions</span></span>](er-functions-category-list.md)
