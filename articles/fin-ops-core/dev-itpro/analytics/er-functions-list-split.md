---
title: SPLIT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SPLIT elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 5c99ee5e8129ed45253893dc83acdef99b4ce2c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745597"
---
# <a name="split-er-function"></a><span data-ttu-id="d8445-103">SPLIT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="d8445-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8445-104">`SPLIT` funkcija sadala norādīto ievades virkni apakšvirknēs un atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību.</span><span class="sxs-lookup"><span data-stu-id="d8445-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d8445-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="d8445-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="d8445-106">Šo sintaksi izmanto, lai norādīto ievades virkni sadalītu apakšvirknēs, katrai no kurām ir norādīts garums.</span><span class="sxs-lookup"><span data-stu-id="d8445-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="d8445-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="d8445-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="d8445-108">Šo sintaksi izmanto, lai norādīto ievades virkni sadalītu apakšvirknēs, pamatojoties uz norādīto norobežotāju.</span><span class="sxs-lookup"><span data-stu-id="d8445-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="d8445-109">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d8445-109">Arguments</span></span>

<span data-ttu-id="d8445-110">`input`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d8445-110">`input`: *String*</span></span>

<span data-ttu-id="d8445-111">Sadalāmais teksts.</span><span class="sxs-lookup"><span data-stu-id="d8445-111">The text to split.</span></span>

<span data-ttu-id="d8445-112">`length`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="d8445-112">`length`: *Integer*</span></span>

<span data-ttu-id="d8445-113">Vienas apakšvirknes maksimālais garums.</span><span class="sxs-lookup"><span data-stu-id="d8445-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="d8445-114">`delimiter`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d8445-114">`delimiter`: *String*</span></span>

<span data-ttu-id="d8445-115">Norobežotājs, ko izmanto, lai atdalītu apakšvirknes.</span><span class="sxs-lookup"><span data-stu-id="d8445-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="d8445-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d8445-116">Return values</span></span>

<span data-ttu-id="d8445-117">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="d8445-117">*Record list*</span></span>

<span data-ttu-id="d8445-118">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="d8445-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d8445-119">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="d8445-119">Usage notes</span></span>

<span data-ttu-id="d8445-120">Atgrieztā saraksta ieraksta struktūra sastāv no **Virknes** tipa *Vērtības* lauka.</span><span class="sxs-lookup"><span data-stu-id="d8445-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="d8445-121">Katrā atgrieztā saraksta ierakstā ir šajā laukā ģenerētās apakšvirknes.</span><span class="sxs-lookup"><span data-stu-id="d8445-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="d8445-122">Ja `delimiter` arguments ir tukšs, tiek atgriezts jauns saraksts, kas sastāv no viena ieraksta, kurā ir **Virknes** veida lauks *Vērtība*.</span><span class="sxs-lookup"><span data-stu-id="d8445-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="d8445-123">Šis lauks satur ievades tekstu.</span><span class="sxs-lookup"><span data-stu-id="d8445-123">This field contains the input text.</span></span>

<span data-ttu-id="d8445-124">Ja `input` arguments ir tukšs, tiek atgriezts jauns tukšs saraksts.</span><span class="sxs-lookup"><span data-stu-id="d8445-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="d8445-125">Ja `input` vai `delimiter` arguments nav norādīts (ir tukšs), tiek parādīts programmas izņēmums.</span><span class="sxs-lookup"><span data-stu-id="d8445-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="d8445-126">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="d8445-126">Example 1</span></span>

<span data-ttu-id="d8445-127">`SPLIT ("abcd", 3)` atgriež jaunu sarakstu, kas sastāv no diviem ierakstiem ar **Virknes** veida lauku *Vērtība*.</span><span class="sxs-lookup"><span data-stu-id="d8445-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="d8445-128">Pirmā ieraksta lauks **Vērtība** ietver tekstu **"abc"**, un otrā ieraksta lauks **Vērtība** satur tekstu **"d"**.</span><span class="sxs-lookup"><span data-stu-id="d8445-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d8445-129">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="d8445-129">Example 2</span></span>

<span data-ttu-id="d8445-130">`SPLIT ("XAb aBy", "aB")` atgriež jaunu sarakstu, kas sastāv no trim ierakstiem ar **Virknes** veida lauku *Vērtība*.</span><span class="sxs-lookup"><span data-stu-id="d8445-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="d8445-131">Laukam **Vērtība** pirmajā ierakstā ir teksts **"X"**, laukam **Vērtība** otrajā ierakstā ir teksts **"&nbsp;"**, un laukam **Vērtība** trešajā ierakstā ir teksts **"y"**.</span><span class="sxs-lookup"><span data-stu-id="d8445-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d8445-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d8445-132">Additional resources</span></span>

[<span data-ttu-id="d8445-133">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="d8445-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]