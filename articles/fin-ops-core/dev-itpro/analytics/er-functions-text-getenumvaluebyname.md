---
title: GETENUMVALUEBYNAME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota GETENUMVALUEBYNAME elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570594"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="e158d-103">GETENUMVALUEBYNAME ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e158d-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e158d-104">`GETENUMVALUEBYNAME` funkcija meklē konkrētu *Enum* vērtību norādītajā uzskaitījuma datu avotā, izmantojot uzskaitījuma nosaukumu, kas ir norādīts kā *Virknes* vērtība.</span><span class="sxs-lookup"><span data-stu-id="e158d-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="e158d-105">Ja tiek tiek atrasta *Enum* vērtība, funkcija to atgriež.</span><span class="sxs-lookup"><span data-stu-id="e158d-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="e158d-106">Pretējā gadījumā funkcija atgriež uzskaitījuma vērtību **null**.</span><span class="sxs-lookup"><span data-stu-id="e158d-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e158d-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="e158d-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="e158d-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="e158d-108">Arguments</span></span>

<span data-ttu-id="e158d-109">`enumeration data source path`: *Uzskaitījums*</span><span class="sxs-lookup"><span data-stu-id="e158d-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="e158d-110">Derīgs datu avota atsauces ceļš vienam no šādiem uzskaitījumu tipiem:</span><span class="sxs-lookup"><span data-stu-id="e158d-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="e158d-111">Elektronisko pārskatu (ER) modeļu uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="e158d-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="e158d-112">ER formāta uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="e158d-112">ER format enumeration</span></span>
- <span data-ttu-id="e158d-113">Microsoft Dynamics 365 Finance uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="e158d-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="e158d-114">`enumeration value text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="e158d-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="e158d-115">Virknes vērtība, kas apzīmē vienas uzskaitījuma vērtības nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e158d-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="e158d-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="e158d-116">Return values</span></span>

<span data-ttu-id="e158d-117">Nullējama *Enum*</span><span class="sxs-lookup"><span data-stu-id="e158d-117">Nullable *Enum*</span></span>

<span data-ttu-id="e158d-118">Iegūtā uzskaitījuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="e158d-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e158d-119">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="e158d-119">Usage notes</span></span>

<span data-ttu-id="e158d-120">Netiek rādīts izņēmums, ja *Enum* vērtība nav atrasta, izmantojot uzskaitījuma vērtības nosaukumu, kas ir norādīts kā *Virknes* vērtība.</span><span class="sxs-lookup"><span data-stu-id="e158d-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="e158d-121">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="e158d-121">Example 1</span></span>

<span data-ttu-id="e158d-122">Tālāk esošajā attēlā ir parādīts datu modelī ieviests uzskaitījums **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="e158d-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="e158d-123">Ņemiet vērā, ka etiķetes ir definētas uzskaitījumu vērtībām.</span><span class="sxs-lookup"><span data-stu-id="e158d-123">Notice that labels are defined for the enumeration values.</span></span>

![Pieejamās datu modeļu uzskaitījuma vērtības](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="e158d-125">Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.</span><span class="sxs-lookup"><span data-stu-id="e158d-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="e158d-126">**$Direction** datu avots ir konfigurēts ER pārskatā.</span><span class="sxs-lookup"><span data-stu-id="e158d-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="e158d-127">Šis datu avots ir konfigurēts, pamatojoties uz modeļa uzskaitījumu **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="e158d-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="e158d-128">Izteiksme `$IsArrivals` ir izveidota ar mērķi lietot modeļa uzskaitījumā bāzētu datu avotu **$Direction** kā šīs funkcijas parametru.</span><span class="sxs-lookup"><span data-stu-id="e158d-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="e158d-129">Šīs salīdzinājuma izteiksmes vērtība ir **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="e158d-129">The value of this comparison expression is **TRUE**.</span></span>

![Datu modeļu uzskaitījuma piemērs](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="e158d-131">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="e158d-131">Example 2</span></span>

<span data-ttu-id="e158d-132">`GETENUMVALUEBYNAME` un [`LISTOFFIELDS`](er-functions-list-listoffields.md) funkcijas sniedz iespēju ienest atbalstīto uzskaitījumu vērtības un etiķetes kā teksta vērtības.</span><span class="sxs-lookup"><span data-stu-id="e158d-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="e158d-133">(Atbalstītie uzskaitījumi ir programmu uzskaitījumi, datu modeļu uzskaitījumi un formātu uzskaitījumi.)</span><span class="sxs-lookup"><span data-stu-id="e158d-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="e158d-134">Tālāk esošajā attēlā ir parādīts modeļa kartējumā ieviests datu avots **TransType**.</span><span class="sxs-lookup"><span data-stu-id="e158d-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="e158d-135">Šis datu avots attiecas uz programmu uzskaitījumu **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="e158d-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Modeļa kartējuma datu avots, kas attiecas uz programmu uzskaitījumu](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="e158d-137">Tālāk esošajā attēlā ir parādīts modeļa kartējumā konfigurēts datu avots **TransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="e158d-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="e158d-138">Šis datu avots ir konfigurēts, pamatojoties uz programmu uzskaitījumu **TransType**.</span><span class="sxs-lookup"><span data-stu-id="e158d-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="e158d-139">Funkcija `LISTOFFIELDS` tiek izmantota, lai atgrieztu visas uzskaitījuma vērtības kā ierakstu sarakstu ar laukiem.</span><span class="sxs-lookup"><span data-stu-id="e158d-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="e158d-140">Šādā veidā tiek atklāta informācija par katra uzskaitījuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="e158d-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="e158d-141">Lauks **EnumValue** ir konfigurēts **TransTypeList** datu avotam, izmantojot `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="e158d-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="e158d-142">Šis lauks atgriež uzskaitījuma vērtību katram šī saraksta ierakstam.</span><span class="sxs-lookup"><span data-stu-id="e158d-142">This field returns an enumeration value for every record in this list.</span></span>

![Modeļa kartējuma datu avots, kas atgriež visas atlasītās uzskaitījuma vērtības kā ierakstu sarakstu](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="e158d-144">Tālāk esošajā attēlā ir parādīts modeļa kartējumā konfigurēts datu avots **VendTrans**.</span><span class="sxs-lookup"><span data-stu-id="e158d-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="e158d-145">Šis datu avots atgriež kreditora transakciju ierakstus no **VendTrans** programmas tabulas.</span><span class="sxs-lookup"><span data-stu-id="e158d-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="e158d-146">Katras transakcijas virsgrāmatas veids ir definēts, izmantojot lauka **TransType** vērtību.</span><span class="sxs-lookup"><span data-stu-id="e158d-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="e158d-147">Lauks **TransTypeTitle** ir konfigurēts **VendTrans** datu avotam, izmantojot `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="e158d-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="e158d-148">Šis lauks atgriež pašreizējās transakcijas uzskaitījuma vērtības etiķeti kā tekstu, ja šī uzskaitījuma vērtība ir pieejama.</span><span class="sxs-lookup"><span data-stu-id="e158d-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="e158d-149">Pretējā gadījumā šī izteiksme atgriež tukšu virknes vērtību.</span><span class="sxs-lookup"><span data-stu-id="e158d-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="e158d-150">Lauks **TransTypeTitle** ir saistīts ar datu modeļa lauku **LedgerType**, kas iespējo šīs informācijas izmantošanu katrā elektroniskā pārskata formātā, kas izmanto datu modeli kā datu avotu.</span><span class="sxs-lookup"><span data-stu-id="e158d-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Modeļa kartējuma datu avots, kas atgriež kreditoru transakcijas](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="e158d-152">Tālāk esošajā attēlā ir parādīts, kā varat izmantot [datu avota atkļūdotāju](er-debug-data-sources.md), lai pārbaudītu konfigurēto modeļa kartējumu.</span><span class="sxs-lookup"><span data-stu-id="e158d-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Datu avota atkļūdotāja izmantošana, lai pārbaudītu konfigurēto modeļa kartējumu](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="e158d-154">Datu modeļa lauks **LedgerType** parāda transakciju veida etiķetes kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="e158d-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="e158d-155">Ja plānojat izmantot šo pieeju lielam transakciju datu apjomam, ir jāapsver izpildes veiktspēja.</span><span class="sxs-lookup"><span data-stu-id="e158d-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="e158d-156">Papildinformāciju skatiet [Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="e158d-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e158d-157">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e158d-157">Additional resources</span></span>

[<span data-ttu-id="e158d-158">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="e158d-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="e158d-159">Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas</span><span class="sxs-lookup"><span data-stu-id="e158d-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="e158d-160">LISTOFFIELDS ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e158d-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="e158d-161">FIRSTORNULL ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e158d-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="e158d-162">WHERE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e158d-162">WHERE ER function</span></span>](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]