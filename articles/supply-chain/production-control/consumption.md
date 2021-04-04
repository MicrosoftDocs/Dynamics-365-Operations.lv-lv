---
title: Aprēķināt materiālu patēriņu
description: Šajā rakstā ir sniegta informācija par dažādām opcijām, kas ir saistītas ar materiālu patēriņa aprēķināšanu.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc39df69a22b90a805aa9967d52dafea27c78c2b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246337"
---
# <a name="calculate-material-consumption"></a><span data-ttu-id="83e6a-103">Aprēķināt materiālu patēriņu</span><span class="sxs-lookup"><span data-stu-id="83e6a-103">Calculate material consumption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83e6a-104">Šajā rakstā ir sniegta informācija par dažādām opcijām, kas ir saistītas ar materiālu patēriņa aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="83e6a-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="83e6a-105">Tālāk ir norādītas ar materiālu patēriņa aprēķināšanu saistītās opcijas, kas ir pieejamas lapas **Materiālu komplekts** kopsavilkuma cilnes **Detalizēta informācija par rindu** cilnēs **Iestatīšana** un **Pakāpenisks patēriņš**.</span><span class="sxs-lookup"><span data-stu-id="83e6a-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="83e6a-106">Mainīgais un konstantais patēriņš</span><span class="sxs-lookup"><span data-stu-id="83e6a-106">Variable and constant consumption</span></span>
<span data-ttu-id="83e6a-107">Laukā **Patēriņš ir** varat atlasīt, vai patēriņš ir jāaprēķina kā konstants vai kā mainīgs daudzums.</span><span class="sxs-lookup"><span data-stu-id="83e6a-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="83e6a-108">Atlasiet vērtību **Konstante**, ja ražošanai ir nepieciešams fiksēts daudzums vai apjoms neatkarīgi no saražotā daudzuma.</span><span class="sxs-lookup"><span data-stu-id="83e6a-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="83e6a-109">Atlasiet opciju **Mainīgais**, kas ir noklusējuma iestatījums, ja saražotajām precēm nepieciešamais materiāla daudzums ir proporcionāls saražoto preču daudzumam.</span><span class="sxs-lookup"><span data-stu-id="83e6a-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="83e6a-110">Patēriņa aprēķināšana, izmantojot formulu</span><span class="sxs-lookup"><span data-stu-id="83e6a-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="83e6a-111">Laukā **Formula** varat iestatīt dažādas formulas materiālu patēriņa aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="83e6a-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="83e6a-112">Ja izmantojat noklusējuma vērtību **Standarta**, patēriņš netiek aprēķināts, izmantojot formulu.</span><span class="sxs-lookup"><span data-stu-id="83e6a-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="83e6a-113">Tālāk ir norādītas ar laukiem **Augstums**, **Platums**, **Dziļums**, **Blīvums** un **Konstante** izmantotās formulas.</span><span class="sxs-lookup"><span data-stu-id="83e6a-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="83e6a-114">Augstums \* Konstante</span><span class="sxs-lookup"><span data-stu-id="83e6a-114">Height \* Constant</span></span>
-   <span data-ttu-id="83e6a-115">Augstums \* Platums \* Konstante</span><span class="sxs-lookup"><span data-stu-id="83e6a-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="83e6a-116">Augstums \* Platums \* Dziļums \* Konstante</span><span class="sxs-lookup"><span data-stu-id="83e6a-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="83e6a-117">(Augstums \* Platums \* Dziļums / Blīvums) \* Konstante</span><span class="sxs-lookup"><span data-stu-id="83e6a-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="83e6a-118">Noapaļošana un dalītājs</span><span class="sxs-lookup"><span data-stu-id="83e6a-118">Rounding up and multiples</span></span>
<span data-ttu-id="83e6a-119">Kopā izmantojot laukus **Noapaļošana** un **Dalītājs**, varat noapaļot materiālu patēriņa vērtību.</span><span class="sxs-lookup"><span data-stu-id="83e6a-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="83e6a-120">Piemēram, varat noapaļot vērtību atbilstoši materiālu apstrādes vienībai, kur ražošanai tiek izdots izejmateriāls.</span><span class="sxs-lookup"><span data-stu-id="83e6a-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="83e6a-121">Ir pieejamas šādas lauka **Noapaļošana** opcijas: **Daudzums**, **Mērījums** un **Patēriņš**.</span><span class="sxs-lookup"><span data-stu-id="83e6a-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="83e6a-122">Daudzums</span><span class="sxs-lookup"><span data-stu-id="83e6a-122">Quantity</span></span>

<span data-ttu-id="83e6a-123">Ja atlasāt opciju **Daudzums** kā noapaļošanas mehānismu, daudzumam ir jābūt norādītā daudzuma dalītājam.</span><span class="sxs-lookup"><span data-stu-id="83e6a-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="83e6a-124">Piemēram, ja ir nepieciešams vesels skaitlis, laikā **Dalītājs** atlasiet vērtību **1**.</span><span class="sxs-lookup"><span data-stu-id="83e6a-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="83e6a-125">Pēc tam skaitļi tiek noapaļoti līdz daudzumam, kas dalās ar 1.</span><span class="sxs-lookup"><span data-stu-id="83e6a-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="83e6a-126">Mērījums</span><span class="sxs-lookup"><span data-stu-id="83e6a-126">Measurement</span></span>

<span data-ttu-id="83e6a-127">Noapaļošanas mehānisms **Mērījums** parasti tiek atlasīts, ja izejmateriālam ir konkrēti izmēri.</span><span class="sxs-lookup"><span data-stu-id="83e6a-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="83e6a-128">Piemēram, saražotajai precei ir nepieciešams 2 metrus garš metāla caurules posms un metāla caurule ir pieejama 4,5 metrus garos gabalos.</span><span class="sxs-lookup"><span data-stu-id="83e6a-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="83e6a-129">Šādā gadījumā var izmantot noapaļošanas mehānismu **Mērījums**, lai aprēķinātu, cik metāla cauruļu ir nepieciešams noteiktam saražoto preču skaitam.</span><span class="sxs-lookup"><span data-stu-id="83e6a-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="83e6a-130">Šajā piemērā laukam **Formula** ir iestatīta vērtība **Augstums \* Konstante**.</span><span class="sxs-lookup"><span data-stu-id="83e6a-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="83e6a-131">Laukam **Augstums** ir iestatīta vērtība **2**, lai norādītu pabeigtajai precei nepieciešamo caurules garumu.</span><span class="sxs-lookup"><span data-stu-id="83e6a-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="83e6a-132">Ir iestatīta lauka **Dalītājs** vērtība **4,5**, lai norādītu, ka caurule tiek izdota 4,5 metrus garos gabalos.</span><span class="sxs-lookup"><span data-stu-id="83e6a-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="83e6a-133">Tālāk ir norādīts aprēķins.</span><span class="sxs-lookup"><span data-stu-id="83e6a-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="83e6a-134">Dalītāju skaits, kas ir nepieciešams 10 saražotām precēm: 10 ÷ 2 = 5 gab</span><span class="sxs-lookup"><span data-stu-id="83e6a-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="83e6a-135">Kopējais patēriņš: 4,5 x 5 = 22,5 metri metāla caurules</span><span class="sxs-lookup"><span data-stu-id="83e6a-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="83e6a-136">Tiek pieņemts, ka uz katriem pieciem patērētajiem metāla caurules gabaliem tiek norakstīti 0,5 metri caurules.</span><span class="sxs-lookup"><span data-stu-id="83e6a-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="83e6a-137">Patēriņš</span><span class="sxs-lookup"><span data-stu-id="83e6a-137">Consumption</span></span>

<span data-ttu-id="83e6a-138">Noapaļošanas mehānisms **Patēriņš** parasti tiek atlasīts, ja izejmateriāls tiek izdots veselos noteiktas preces materiālu apstrādes vienības daudzumos.</span><span class="sxs-lookup"><span data-stu-id="83e6a-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="83e6a-139">Piemēram, saražotajai precei ir nepieciešamas 2 kvartas krāsas un krāsa tiek izdota 25 kvartu bundžās.</span><span class="sxs-lookup"><span data-stu-id="83e6a-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="83e6a-140">Šādā gadījumā var izmantot noapaļošanas mehānismu **Patēriņš**, lai noapaļotu patēriņu līdz veselam 25 kvartu bundžu skaitam.</span><span class="sxs-lookup"><span data-stu-id="83e6a-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="83e6a-141">Tālāk ir norādīts, kā tiek aprēķināts krāsas daudzums, kas ir nepieciešams 180 saražotajām precēm.</span><span class="sxs-lookup"><span data-stu-id="83e6a-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="83e6a-142">Nepieciešamā krāsa, neieskaitot brāķi: 180 × 2 = 360 kvartas</span><span class="sxs-lookup"><span data-stu-id="83e6a-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="83e6a-143">Bundžu skaits: 360 ÷ 25 = 14,4, kas tiek noapaļots līdz 15</span><span class="sxs-lookup"><span data-stu-id="83e6a-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="83e6a-144">Nepieciešamā krāsa, ieskaitot brāķi: 15 × 25 = 375 kvartas</span><span class="sxs-lookup"><span data-stu-id="83e6a-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="83e6a-145">Pakāpenisks patēriņš</span><span class="sxs-lookup"><span data-stu-id="83e6a-145">Step consumption</span></span>
<span data-ttu-id="83e6a-146">Pakāpenisks patēriņš tiek izmantots, lai aprēķinātu konstantu patēriņu daudzuma intervālos.</span><span class="sxs-lookup"><span data-stu-id="83e6a-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="83e6a-147">Ja cilnes **Iestatījumi** laukā **Formula** atlasāt **Pakāpenisks patēriņš**, tad varat pievienot informāciju par darbībām cilnē **Pakāpenisks patēriņš**. Fiksēto patērēto daudzumu var iestatīt saražotā daudzuma intervālos.</span><span class="sxs-lookup"><span data-stu-id="83e6a-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="83e6a-148">Piemēram, pakāpenisks patēriņš tiek iestatīts, kā tas ir redzams tālāk esošajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="83e6a-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="83e6a-149">No sērijas</span><span class="sxs-lookup"><span data-stu-id="83e6a-149">From series</span></span> | <span data-ttu-id="83e6a-150">Daudzums</span><span class="sxs-lookup"><span data-stu-id="83e6a-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="83e6a-151">0,00</span><span class="sxs-lookup"><span data-stu-id="83e6a-151">0.00</span></span>        | <span data-ttu-id="83e6a-152">10,0000</span><span class="sxs-lookup"><span data-stu-id="83e6a-152">10.0000</span></span>  |
| <span data-ttu-id="83e6a-153">100,00</span><span class="sxs-lookup"><span data-stu-id="83e6a-153">100.00</span></span>      | <span data-ttu-id="83e6a-154">20,0000</span><span class="sxs-lookup"><span data-stu-id="83e6a-154">20.0000</span></span>  |
| <span data-ttu-id="83e6a-155">200,00</span><span class="sxs-lookup"><span data-stu-id="83e6a-155">200.00</span></span>      | <span data-ttu-id="83e6a-156">40,0000</span><span class="sxs-lookup"><span data-stu-id="83e6a-156">40.0000</span></span>  |

<span data-ttu-id="83e6a-157">Materiālu komplekta (MK) daudzums ir 1, un ražošanas daudzums ir 110</span><span class="sxs-lookup"><span data-stu-id="83e6a-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="83e6a-158">Patēriņa aprēķināšanas formula ir No sērijas (daudzums) = Patēriņš.</span><span class="sxs-lookup"><span data-stu-id="83e6a-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="83e6a-159">Tā kā ražošanas daudzums ir 110, tas ietilpst grupā Sērija no 100.</span><span class="sxs-lookup"><span data-stu-id="83e6a-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="83e6a-160">Tāpēc daudzums ir 20.</span><span class="sxs-lookup"><span data-stu-id="83e6a-160">Therefore, the quantity is 20.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]