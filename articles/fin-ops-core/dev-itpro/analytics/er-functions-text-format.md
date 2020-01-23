---
title: FORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FORMAT elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: df158e80bd1c11832376678a631a9e0e162534ad
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915721"
---
# <span data-ttu-id="61aa5-103"><a name="FORMAT">FORMAT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="61aa5-103"><a name="FORMAT">FORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61aa5-104">`FORMAT` funkcija atgriež norādīto virkni kā *Virknes* vērtību, kas ir formatēta, aizstājot argumentu **%N** ar argumentu *N*.</span><span class="sxs-lookup"><span data-stu-id="61aa5-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="61aa5-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="61aa5-105">Syntax</span></span>

```
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="61aa5-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="61aa5-106">Arguments</span></span>

<span data-ttu-id="61aa5-107">`string`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="61aa5-107">`string`: *String*</span></span>

<span data-ttu-id="61aa5-108">Atsauce uz datu avotu *Virknes* datu tipam, kas ir jāformatē.</span><span class="sxs-lookup"><span data-stu-id="61aa5-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="61aa5-109">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="61aa5-109">This argument is required.</span></span>

<span data-ttu-id="61aa5-110">`argument 1`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="61aa5-110">`argument 1`: *String*</span></span>

<span data-ttu-id="61aa5-111">Pirmais arguments, kas tiek izmantots, lai aizstātu gadījumus **%1**.</span><span class="sxs-lookup"><span data-stu-id="61aa5-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="61aa5-112">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="61aa5-112">This argument is required.</span></span>

<span data-ttu-id="61aa5-113">`argument N`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="61aa5-113">`argument N`: *String*</span></span>

<span data-ttu-id="61aa5-114">*N*-tais arguments, kas tiek izmantots, lai aizstātu gadījumus **%2**, **%3** un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="61aa5-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="61aa5-115">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="61aa5-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="61aa5-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="61aa5-116">Return values</span></span>

<span data-ttu-id="61aa5-117">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="61aa5-117">*String*</span></span>

<span data-ttu-id="61aa5-118">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="61aa5-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="61aa5-119">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="61aa5-119">Usage notes</span></span>

<span data-ttu-id="61aa5-120">Ja arguments parametram nav norādīts, šis parametrs virknē tiek atgriezts kā **"%N"**.</span><span class="sxs-lookup"><span data-stu-id="61aa5-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="61aa5-121">Vērtībām ar tipu *Reāls* noklusējuma virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.</span><span class="sxs-lookup"><span data-stu-id="61aa5-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="61aa5-122">Paraugs</span><span class="sxs-lookup"><span data-stu-id="61aa5-122">Example</span></span>

<span data-ttu-id="61aa5-123">Tālāk esošajā attēlā ir redzams, ka **PaymentModel** datu avots atgriež klientu ierakstu sarakstu, izmantojot **Debitora** komponentu.</span><span class="sxs-lookup"><span data-stu-id="61aa5-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="61aa5-124">Tas atgriež vērtību apstrādes datums, izmantojot lauku **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="61aa5-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="61aa5-125">Elektronisko pārskatu (ER) formātā, kas ir izveidots tā, lai ģenerētu elektronisku failu noteiktiem debitoriem, vienums **PaymentModel** ir atlasīts kā datu avots, un tas kontrolē procesa plūsmu.</span><span class="sxs-lookup"><span data-stu-id="61aa5-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="61aa5-126">Lietotājiem tiek parādīts izņēmums, lai viņus informētu, ja atlasītais debitors tiek apturēts datumam, kad atskaite tiek apstrādāta.</span><span class="sxs-lookup"><span data-stu-id="61aa5-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="61aa5-127">Šāda tipa apstrādes kontrolei izveidotā formulā var izmantot šādus resursus:</span><span class="sxs-lookup"><span data-stu-id="61aa5-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="61aa5-128">Etiķete SYS70894, kurā ir šāds teksts:</span><span class="sxs-lookup"><span data-stu-id="61aa5-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="61aa5-129">**Valodai EN-US:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="61aa5-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="61aa5-130">**Valodai DE:** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="61aa5-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="61aa5-131">Etiķete SYS18389, kurā ir šāds teksts:</span><span class="sxs-lookup"><span data-stu-id="61aa5-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="61aa5-132">**EN-US valodai:** "Customer %1 is stopped for %2."</span><span class="sxs-lookup"><span data-stu-id="61aa5-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="61aa5-133">**DE valodai:** "Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="61aa5-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="61aa5-134">Lūk, kādu izteiksmi varat izveidot.</span><span class="sxs-lookup"><span data-stu-id="61aa5-134">Here is the expression that can be designed.</span></span>

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="61aa5-135">Ja pārskats debitoram **Litware Retail** tiek apstrādāts 2015. gada 17. decembrī kultūrā **EN-US** un valodā **EN-US**, šī formula atgriež tālāk norādīto tekstu, kurš lietotājam var tikt rādīts kā izņēmuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="61aa5-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="61aa5-136">*Nothing to print.. Customer Litware Retail is stopped for 12/17/2015."*</span><span class="sxs-lookup"><span data-stu-id="61aa5-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="61aa5-137">Ja tas pats pārskats debitoram **Litware Retail** tiek apstrādāts 2015. gada 17. decembrī kultūrā **DE** un valodā **DE**, šī formula atgriež tālāk norādīto tekstu, kurā tiek izmantots cits datuma formāts.</span><span class="sxs-lookup"><span data-stu-id="61aa5-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="61aa5-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="61aa5-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="61aa5-139">ER formulās etiķetēm tiek lietota tālāk norādītā sintakse.</span><span class="sxs-lookup"><span data-stu-id="61aa5-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="61aa5-140">**Etiķetēm no Microsoft Dynamics 365 Finance programmas resursiem:** **@X**, kur **X** ir etiķetes ID programmas objektu kokā (AOT)</span><span class="sxs-lookup"><span data-stu-id="61aa5-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="61aa5-141">**Etiķetēm, kas ir ietvertas ER konfigurācijās:** **@"GER_LABEL:X"**, kur **X** ir etiķetes ID ER konfigurācijā</span><span class="sxs-lookup"><span data-stu-id="61aa5-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61aa5-142">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="61aa5-142">Additional resources</span></span>

[<span data-ttu-id="61aa5-143">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="61aa5-143">Text functions</span></span>](er-functions-category-text.md)
