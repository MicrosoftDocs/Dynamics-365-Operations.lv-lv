---
title: NUMSEQVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMSEQVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: b513d04bfeb3a37aa0b1703d0fdde040885a5159
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680594"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="8d757-103">NUMSEQVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="8d757-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d757-104">`NUMSEQVALUE` funkcija atgriež *Virknes* vērtību, kas apzīmē jauno numuru sērijas ģenerēto vērtību, pamatojoties uz norādīto numuru sēriju, tvērumu un tvēruma ID.</span><span class="sxs-lookup"><span data-stu-id="8d757-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="8d757-105">Tvēruma ID ir vienāds ar uzņēmuma kodu, ko nodrošina konteksts, kurā tiek palaists elektroniskā pārskata (ER) formāts.</span><span class="sxs-lookup"><span data-stu-id="8d757-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="8d757-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="8d757-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="8d757-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="8d757-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="8d757-108">Sintakse 3</span><span class="sxs-lookup"><span data-stu-id="8d757-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="8d757-109">Argumenti</span><span class="sxs-lookup"><span data-stu-id="8d757-109">Arguments</span></span>

<span data-ttu-id="8d757-110">`number sequence code`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="8d757-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="8d757-111">Teksta vērtība, kas apzīmē kodu numuru sērijai, kurai ir nepieciešama jauna vērtība.</span><span class="sxs-lookup"><span data-stu-id="8d757-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="8d757-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="8d757-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="8d757-113">*Int64* vērtība, kas attēlo ieraksta ID ierakstu tabulā NumberSequenceTable, kas ietver numuru sērijas definīciju, kurai ir nepieciešama jauna vērtība.</span><span class="sxs-lookup"><span data-stu-id="8d757-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="8d757-114">`scope type`: *Uzskaitījuma vērtība*</span><span class="sxs-lookup"><span data-stu-id="8d757-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="8d757-115">Uzskaitījuma vērtība **ERExpressionNumberSequenceScopeType**, kas definē tās numuru sērijas tvērumu, kurai ir nepieciešama jauna vērtība.</span><span class="sxs-lookup"><span data-stu-id="8d757-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="8d757-116">Pieejamie tvērumu tipi ir **Kopīgots**, **Juridiska persona** un **Uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="8d757-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="8d757-117">`scope ID`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="8d757-117">`scope ID`: *String*</span></span>

<span data-ttu-id="8d757-118">*Virknes* vērtība, kas identificē tvērumu, pamatojoties uz norādīto tvēruma tipu.</span><span class="sxs-lookup"><span data-stu-id="8d757-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d757-119">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="8d757-119">Return values</span></span>

<span data-ttu-id="8d757-120">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="8d757-120">*String*</span></span>

<span data-ttu-id="8d757-121">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="8d757-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8d757-122">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="8d757-122">Usage notes</span></span>

<span data-ttu-id="8d757-123">Tvēruma tipam **Koplietots** kā tvēruma ID ir jānorāda tukša virkne.</span><span class="sxs-lookup"><span data-stu-id="8d757-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="8d757-124">Tvēruma tipiem **Uzņēmums** un **Juridiskā persona** kā tvēruma ID ir jānorāda uzņēmuma kods.</span><span class="sxs-lookup"><span data-stu-id="8d757-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="8d757-125">Ja šiem tvērumu tipiem ka tvēruma ID norādāt tukšu virkni, tiek izmantots pašreizējais uzņēmuma kods.</span><span class="sxs-lookup"><span data-stu-id="8d757-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="8d757-126">Lietojot 1. sintaksi, numuru sērija tiek pieprasīta **Uzņēmuma** tvēruma tipam, un uzņēmuma kodu nodrošina konteksts, kurā tiek palaists ER formāts.</span><span class="sxs-lookup"><span data-stu-id="8d757-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="8d757-127">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="8d757-127">Example 1</span></span>

<span data-ttu-id="8d757-128">Savā ER formātā jūs definējat tipa *Lietotāja ievades parametrs* datu avotu **AskNumSeq**.</span><span class="sxs-lookup"><span data-stu-id="8d757-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="8d757-129">Šis datu avots attiecas uz paplašināto datu tipu (EDT) **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="8d757-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="8d757-130">Pēc tam definējat tipa **Aprēķinātais lauks** datu avotu *NumSeq*.</span><span class="sxs-lookup"><span data-stu-id="8d757-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="8d757-131">Šajā datu avotā ir izteiksme `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="8d757-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="8d757-132">Kad tiek izsaukts datu avots **NumSeq**, tas atgriež jaunu ģenerēto numuru sērijas vērtību, kas tika norādīta izpildlaikā, ievadot tās kodu dialoglodziņā.</span><span class="sxs-lookup"><span data-stu-id="8d757-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="8d757-133">Numuru sērija tiek pieprasīta **Uzņēmuma** tvēruma tipam.</span><span class="sxs-lookup"><span data-stu-id="8d757-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="8d757-134">Uzņēmuma kodu nodrošina konteksts, kurā tiek palaists ER formāts.</span><span class="sxs-lookup"><span data-stu-id="8d757-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="8d757-135">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="8d757-135">Example 2</span></span>

<span data-ttu-id="8d757-136">Savā modeļa kartēšanā jūs tiek definēti šādi datu avoti:</span><span class="sxs-lookup"><span data-stu-id="8d757-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="8d757-137">**Tabulas** veida datu avots *LedgerParms*.</span><span class="sxs-lookup"><span data-stu-id="8d757-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="8d757-138">Šis datu avots attiecas uz LedgerParameters tabulu.</span><span class="sxs-lookup"><span data-stu-id="8d757-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="8d757-139">**Aprēķinātā lauka** veida datu avots *NumSeq*.</span><span class="sxs-lookup"><span data-stu-id="8d757-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="8d757-140">Šajā datu avotā ir izteiksme `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="8d757-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="8d757-141">Kad tiek izsaukts datu avots **NumSeq**, tas atgriež jauno vērtību, kas ir ģenerēta ar numuru sēriju, kura ir konfigurēta virsgrāmatas parametros tam uzņēmumam, kas nodrošina kontekstu, kurā tiek darbināts ER formāts.</span><span class="sxs-lookup"><span data-stu-id="8d757-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="8d757-142">Šī numuru sērija unikāli identificē žurnālus un darbojas kā partijas numurs, kas sasaista transakcijas.</span><span class="sxs-lookup"><span data-stu-id="8d757-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="8d757-143">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="8d757-143">Example 3</span></span>

<span data-ttu-id="8d757-144">Savā modeļa kartēšanā jūs tiek definēti šādi datu avoti:</span><span class="sxs-lookup"><span data-stu-id="8d757-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="8d757-145">**enumScope** datu avots Microsoft Dynamics 365 Finance *uzskaitījuma* tipam.</span><span class="sxs-lookup"><span data-stu-id="8d757-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="8d757-146">Šis datu avots attiecas uz uzskaitījumu **ERExpressionNumberSequenceScopeType**.</span><span class="sxs-lookup"><span data-stu-id="8d757-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="8d757-147">**Aprēķinātā lauka** veida datu avots *NumSeq*.</span><span class="sxs-lookup"><span data-stu-id="8d757-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="8d757-148">Šajā datu avotā ir izteiksme `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="8d757-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="8d757-149">Kad tiek izsaukts datu avots **NumSeq**, tas atgriež jauno vērtību, kas ir ģenerēta ar numuru sēriju **Gene\_1**, kura ir konfigurēta uzņēmumam, kas nodrošina kontekstu, kurā tiek darbināts ER formāts.</span><span class="sxs-lookup"><span data-stu-id="8d757-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d757-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8d757-150">Additional resources</span></span>

[<span data-ttu-id="8d757-151">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="8d757-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
