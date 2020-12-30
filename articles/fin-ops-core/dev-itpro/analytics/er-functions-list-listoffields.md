---
title: LISTOFFIELDS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LISTOFFIELDS elektroniskā pārskata (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d8d9f41d6ee5256f560c83486c95ecd47f5b081
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686516"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="60be5-103">LISTOFFIELDS ER funkcija</span><span class="sxs-lookup"><span data-stu-id="60be5-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60be5-104">`LISTOFFIELDS` funkcija atgriež *Ierakstu saraksta* vērtību, kas tiek izveidota, pamatojoties uz norādītā *Uzskaitījuma* vai *Konteinera (ieraksta)* veida argumenta struktūru.</span><span class="sxs-lookup"><span data-stu-id="60be5-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="60be5-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="60be5-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="60be5-106">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="60be5-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="60be5-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="60be5-107">Arguments</span></span>

<span data-ttu-id="60be5-108">`path`: Datu avota atsauce</span><span class="sxs-lookup"><span data-stu-id="60be5-108">`path`: Data source reference</span></span>

<span data-ttu-id="60be5-109">Derīgs datu avota atsauces ceļš vienam no šādiem datu tipiem:</span><span class="sxs-lookup"><span data-stu-id="60be5-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="60be5-110">Modeļa uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="60be5-110">Model enumeration</span></span>
- <span data-ttu-id="60be5-111">Formāta uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="60be5-111">Format enumeration</span></span>
- <span data-ttu-id="60be5-112">Lietojumprogrammu uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="60be5-112">Application enumeration</span></span>
- <span data-ttu-id="60be5-113">Konteiners (ieraksts)</span><span class="sxs-lookup"><span data-stu-id="60be5-113">Container (record)</span></span>

<span data-ttu-id="60be5-114">`language`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="60be5-114">`language`: *String*</span></span>

<span data-ttu-id="60be5-115">Teksts, kas apzīmē valodas kodu.</span><span class="sxs-lookup"><span data-stu-id="60be5-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="60be5-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="60be5-116">Return values</span></span>

<span data-ttu-id="60be5-117">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="60be5-117">*Record list*</span></span>

<span data-ttu-id="60be5-118">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="60be5-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="60be5-119">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="60be5-119">Usage notes</span></span>

<span data-ttu-id="60be5-120">Izveidotajā sarakstā ietverti ieraksti ar tālāk norādītajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="60be5-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="60be5-121">**Nosaukums** (*Virkne* datu veids)</span><span class="sxs-lookup"><span data-stu-id="60be5-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="60be5-122">**Marķējums** (*Virkne* datu veids)</span><span class="sxs-lookup"><span data-stu-id="60be5-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="60be5-123">**Apraksts** (*Virkne* datu veids)</span><span class="sxs-lookup"><span data-stu-id="60be5-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="60be5-124">**Istranslated** (*Būla* datu tips)</span><span class="sxs-lookup"><span data-stu-id="60be5-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="60be5-125">Ja `path` arguments attiecas uz datu avotu *Konteinera (ieraksta)* tipam katram atsauces konteinera ieraksta laukam, izveidotam sarakstam tiek pievienots jauns ieraksts.</span><span class="sxs-lookup"><span data-stu-id="60be5-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="60be5-126">Katram izveidotam ierakstam laukā **Nosaukums** tiek atgriezts tā konteinera ieraksta lauka nosaukums, kuram tika izveidots pašreizējais ieraksts.</span><span class="sxs-lookup"><span data-stu-id="60be5-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="60be5-127">Ja `path` arguments attiecas uz datu avotu vienam no *Uzskaitījuma* tipiem katrai atsauces uzskaitījuma vērtībai, izveidotam sarakstam tiek pievienots jauns ieraksts.</span><span class="sxs-lookup"><span data-stu-id="60be5-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="60be5-128">Katram izveidotam ierakstam lauka **Nosaukums** vērtība atgriež atsauces tā uzskaitījuma vērtību, kas tika izveidots pašreizējam ierakstam, lauks **Apraksts** atgriež šī uzskaitījuma aprakstu, un lauks **Etiķete** atgriež šī uzskaitījuma etiķeti.</span><span class="sxs-lookup"><span data-stu-id="60be5-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="60be5-129">Izpildlaikā, izmantojot 1. sintaksi, laukiem **Etiķete** un **Apraksts** ir jāatgriež vērtības, kas ir balstītas uz valodas iestatījumiem elektronisko pārskatu (ER) formātā, kas ticis palaists:</span><span class="sxs-lookup"><span data-stu-id="60be5-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="60be5-130">Ja ir pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz šo valodu, un lauks **IsTranslated** atgriež **True**.</span><span class="sxs-lookup"><span data-stu-id="60be5-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="60be5-131">Ja nav pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz noklusējuma **EN-US** valodu un lauks **IsTranslated** atgriež **False**.</span><span class="sxs-lookup"><span data-stu-id="60be5-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="60be5-132">Izpildlaikā, izmantojot 2. sintaksi, laukiem **Etiķete** un **Apraksts** ir jāatgriež vērtības, kas ir balstītas uz valodu, kas ir definēta kā izsauktās funkcijas otrais arguments:</span><span class="sxs-lookup"><span data-stu-id="60be5-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="60be5-133">Ja ir pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz šo valodu, un lauks **IsTranslated** atgriež **True**.</span><span class="sxs-lookup"><span data-stu-id="60be5-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="60be5-134">Ja nav pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz **EN-US** valodu un lauks **IsTranslated** atgriež **False**.</span><span class="sxs-lookup"><span data-stu-id="60be5-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="60be5-135">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="60be5-135">Example 1</span></span>

<span data-ttu-id="60be5-136">Tālāk esošajā attēlā ir parādīts ER datu modelī ieviests uzskaitījums.</span><span class="sxs-lookup"><span data-stu-id="60be5-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="60be5-137">Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.</span><span class="sxs-lookup"><span data-stu-id="60be5-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="60be5-138">Modeļu uzskaitījums ir ievietots pārskatā kā datu avots.</span><span class="sxs-lookup"><span data-stu-id="60be5-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="60be5-139">ER izteiksme modeļu uzskaitījumu izmanto kā funkcijas `LISTOFFIELDS` parametru.</span><span class="sxs-lookup"><span data-stu-id="60be5-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="60be5-140">*Ierakstu saraksta* tipa datu avots tiek ievietots pārskatā, izmantojot izveidoto ER izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="60be5-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="60be5-141">Tālāk esošajā piemērā parādīti ER formāta elementi, kas ir piesaistīti datu avotam ar *Ierakstu saraksta* tipu, kas tika izveidots, izmantojot funkciju `LISTOFFIELDS`</span><span class="sxs-lookup"><span data-stu-id="60be5-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="60be5-142">Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</span><span class="sxs-lookup"><span data-stu-id="60be5-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="60be5-143">Atbilstoši formāta vecākelementu **FILE** un **FOLDER** valodas iestatījumiem etiķešu un aprakstu tulkotais teksts tiek ievadīts ER formāta izvadē.</span><span class="sxs-lookup"><span data-stu-id="60be5-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="60be5-144">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="60be5-144">Example 2</span></span>

<span data-ttu-id="60be5-145">Jūs izmantojat datu avota tipu *Aprēķinātais*, lai konfigurētu datu modeļu uzskaitījuma **enumType** datu avotus **enumType\_de** un **enumType\_deCH**.</span><span class="sxs-lookup"><span data-stu-id="60be5-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="60be5-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="60be5-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="60be5-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="60be5-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="60be5-148">Šajā gadījumā varat izmantot tālāk norādīto izteiksmi, lai iegūtu uzskaitījuma vērtības etiķeti Šveices vācu valodā, ja šāds tulkojums ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="60be5-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="60be5-149">Ja Šveices vācu valodas tulkojums nav pieejams, etiķete ir Vācu.</span><span class="sxs-lookup"><span data-stu-id="60be5-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="60be5-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="60be5-150">Additional resources</span></span>

[<span data-ttu-id="60be5-151">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="60be5-151">List functions</span></span>](er-functions-category-list.md)
