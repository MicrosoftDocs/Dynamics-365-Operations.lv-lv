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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91e4658043278b9b8d73766cc0deac5d50d51a59
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916158"
---
# <span data-ttu-id="9301a-103"><a name="LISTOFFIELDS">LISTOFFIELDS ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="9301a-103"><a name="LISTOFFIELDS">LISTOFFIELDS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9301a-104">`LISTOFFIELDS` funkcija atgriež *Ierakstu saraksta* vērtību, kas tiek izveidota, pamatojoties uz norādītā *Uzskaitījuma* vai *Konteinera (ieraksta)* veida argumenta struktūru.</span><span class="sxs-lookup"><span data-stu-id="9301a-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="9301a-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="9301a-105">Syntax 1</span></span>

```
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="9301a-106">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="9301a-106">Syntax 2</span></span>

```
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="9301a-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="9301a-107">Arguments</span></span>

<span data-ttu-id="9301a-108">`path`: Datu avota atsauce</span><span class="sxs-lookup"><span data-stu-id="9301a-108">`path`: Data source reference</span></span>

<span data-ttu-id="9301a-109">Derīgs datu avota atsauces ceļš vienam no šādiem datu tipiem:</span><span class="sxs-lookup"><span data-stu-id="9301a-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="9301a-110">Modeļa uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="9301a-110">Model enumeration</span></span>
- <span data-ttu-id="9301a-111">Formāta uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="9301a-111">Format enumeration</span></span>
- <span data-ttu-id="9301a-112">Lietojumprogrammu uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="9301a-112">Application enumeration</span></span>
- <span data-ttu-id="9301a-113">Konteiners (ieraksts)</span><span class="sxs-lookup"><span data-stu-id="9301a-113">Container (record)</span></span>

<span data-ttu-id="9301a-114">`language`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="9301a-114">`language`: *String*</span></span>

<span data-ttu-id="9301a-115">Teksts, kas apzīmē valodas kodu.</span><span class="sxs-lookup"><span data-stu-id="9301a-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="9301a-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="9301a-116">Return values</span></span>

<span data-ttu-id="9301a-117">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="9301a-117">*Record list*</span></span>

<span data-ttu-id="9301a-118">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="9301a-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9301a-119">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="9301a-119">Usage notes</span></span>

<span data-ttu-id="9301a-120">Izveidotajā sarakstā ietverti ieraksti ar tālāk norādītajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="9301a-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="9301a-121">**Nosaukums** (datu veids *Virkne*)</span><span class="sxs-lookup"><span data-stu-id="9301a-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="9301a-122">**Marķējums** (datu veids *Virkne*)</span><span class="sxs-lookup"><span data-stu-id="9301a-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="9301a-123">**Apraksts** (datu veids *Virkne*)</span><span class="sxs-lookup"><span data-stu-id="9301a-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="9301a-124">**Istranslated** (*Būla* datu tips)</span><span class="sxs-lookup"><span data-stu-id="9301a-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="9301a-125">Ja `path` arguments attiecas uz datu avotu *Konteinera (ieraksta)* tipam katram atsauces konteinera ieraksta laukam, izveidotam sarakstam tiek pievienots jauns ieraksts.</span><span class="sxs-lookup"><span data-stu-id="9301a-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="9301a-126">Katram izveidotam ierakstam laukā  **Nosaukums** tiek atgriezts tā konteinera ieraksta lauka nosaukums, kuram tika izveidots pašreizējais ieraksts.</span><span class="sxs-lookup"><span data-stu-id="9301a-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="9301a-127">Ja `path` arguments attiecas uz datu avotu vienam no *Uzskaitījuma* tipiem katrai atsauces uzskaitījuma vērtībai, izveidotam sarakstam tiek pievienots jauns ieraksts.</span><span class="sxs-lookup"><span data-stu-id="9301a-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="9301a-128">Katram izveidotam ierakstam lauka **Nosaukums** vērtība atgriež atsauces tā uzskaitījuma vērtību, kas tika izveidots pašreizējam ierakstam, lauks **Apraksts** atgriež šī uzskaitījuma aprakstu, un lauks **Etiķete** atgriež šī uzskaitījuma etiķeti.</span><span class="sxs-lookup"><span data-stu-id="9301a-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="9301a-129">Izpildlaikā, izmantojot 1. sintaksi, laukiem **Etiķete** un **Apraksts** ir jāatgriež vērtības, kas ir balstītas uz valodas iestatījumiem elektronisko pārskatu (ER) formātā, kas ticis palaists:</span><span class="sxs-lookup"><span data-stu-id="9301a-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="9301a-130">Ja ir pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz šo valodu, un lauks **IsTranslated** atgriež **True**.</span><span class="sxs-lookup"><span data-stu-id="9301a-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="9301a-131">Ja nav pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz noklusējuma **EN-US** valodu un lauks **IsTranslated** atgriež **False**.</span><span class="sxs-lookup"><span data-stu-id="9301a-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="9301a-132">Izpildlaikā, izmantojot 2. sintaksi, laukiem **Etiķete** un **Apraksts** ir jāatgriež vērtības, kas ir balstītas uz valodu, kas ir definēta kā izsauktās funkcijas otrais arguments:</span><span class="sxs-lookup"><span data-stu-id="9301a-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="9301a-133">Ja ir pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz šo valodu, un lauks **IsTranslated** atgriež **True**.</span><span class="sxs-lookup"><span data-stu-id="9301a-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="9301a-134">Ja nav pieejamas etiķetes un apraksti par pieprasīto valodu, lauki **Etiķete** un **Apraksts** atgriež vērtības, kas ir balstītas uz **EN-US** valodu un lauks **IsTranslated** atgriež **False**.</span><span class="sxs-lookup"><span data-stu-id="9301a-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="9301a-135">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="9301a-135">Example 1</span></span>

<span data-ttu-id="9301a-136">Tālāk esošajā attēlā ir parādīts ER datu modelī ieviests uzskaitījums.</span><span class="sxs-lookup"><span data-stu-id="9301a-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="9301a-137">Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.</span><span class="sxs-lookup"><span data-stu-id="9301a-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="9301a-138">Modeļu uzskaitījums ir ievietots pārskatā kā datu avots.</span><span class="sxs-lookup"><span data-stu-id="9301a-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="9301a-139">ER izteiksme modeļu uzskaitījumu izmanto kā funkcijas `LISTOFFIELDS` parametru.</span><span class="sxs-lookup"><span data-stu-id="9301a-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="9301a-140">*Ierakstu saraksta* tipa datu avots tiek ievietots pārskatā, izmantojot izveidoto ER izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="9301a-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="9301a-141">Tālāk esošajā piemērā parādīti ER formāta elementi, kas ir piesaistīti datu avotam ar *Ierakstu saraksta* tipu, kas tika izveidots, izmantojot funkciju `LISTOFFIELDS`</span><span class="sxs-lookup"><span data-stu-id="9301a-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="9301a-142">Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</span><span class="sxs-lookup"><span data-stu-id="9301a-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="9301a-143">Atbilstoši formāta vecākelementu **FILE** un **FOLDER** valodas iestatījumiem etiķešu un aprakstu tulkotais teksts tiek ievadīts ER formāta izvadē.</span><span class="sxs-lookup"><span data-stu-id="9301a-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="9301a-144">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="9301a-144">Example 2</span></span>

<span data-ttu-id="9301a-145">Jūs izmantojat datu avota tipu *Aprēķinātais*, lai konfigurētu datu modeļu uzskaitījuma **enumType** datu avotus **enumType\_de** un **enumType\_deCH**.</span><span class="sxs-lookup"><span data-stu-id="9301a-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="9301a-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="9301a-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="9301a-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="9301a-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="9301a-148">Šajā gadījumā varat izmantot tālāk norādīto izteiksmi, lai iegūtu uzskaitījuma vērtības etiķeti Šveices vācu valodā, ja šāds tulkojums ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="9301a-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="9301a-149">Ja Šveices vācu valodas tulkojums nav pieejams, etiķete ir Vācu.</span><span class="sxs-lookup"><span data-stu-id="9301a-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="9301a-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9301a-150">Additional resources</span></span>

[<span data-ttu-id="9301a-151">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="9301a-151">List functions</span></span>](er-functions-category-list.md)
