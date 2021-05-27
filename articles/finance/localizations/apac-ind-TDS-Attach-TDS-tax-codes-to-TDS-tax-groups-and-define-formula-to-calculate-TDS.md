---
title: Pievienojiet TDS nodokļu kodus TDS nodokļu grupām un definējiet TDS aprēķināšanas formulu
description: Šajā tēmā ir paskaidrots, kā iestatīt No kopējo ienākumu summas atskaitītā (TDS) nodokļu grupas un pievienot TDS nodokļu kodus TDS nodokļu grupām. Lai aprēķinātu TDS nodokļu grupai, jums ir jādefinē formula TDS nodokļu kodiem, kas tam piesaistīti.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023427"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="d4fbb-104">Pievienojiet TDS nodokļu kodus TDS nodokļu grupām un definējiet TDS aprēķināšanas formulu</span><span class="sxs-lookup"><span data-stu-id="d4fbb-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4fbb-105">Šajā tēmā ir paskaidrots, kā iestatīt No kopējo ienākumu summas atskaitītā (TDS) nodokļu grupas un pievienot TDS nodokļu kodus TDS nodokļu grupām.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="d4fbb-106">Lai aprēķinātu TDS nodokļu grupai, jums ir jādefinē formula TDS nodokļu kodiem, kas tam piesaistīti.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="d4fbb-107">Sekojiet šiem soļiem, lai iestatītu TDS nodokļu grupu, tai pievienotus TDS nodokļu kodus un definētu formulu TDS aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="d4fbb-108">Pārejiet uz sadaļu **Nodokļi \> Netiešie nodokļi \> Ieturētais nodoklis \> Ieturētā nodokļa grupas**.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="d4fbb-109">[![Ieturēto nodokļu grupas lapa](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="d4fbb-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="d4fbb-110">Darbību rūtī atlasiet **Jauns**, lai izveidotu ieturētā nodokļa grupu TDS, un ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="d4fbb-111">Laukā **Nodokļa veids** atlasiet **TDS**.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="d4fbb-112">Kopsavilkuma cilnē **Iestatīšana** atlasiet **Pievienot**, lai izveidotu rindu.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="d4fbb-113">Laukā **Ieturētā nodokļa kods** atlasiet ieturētā TDS nodokļa kodu TDS nodokļu grupai.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="d4fbb-114">Laukā **Ieturētā nodokļa nosaukums** tiek rādīts TDS nodokļa koda nosaukums, un lauks **Vērtība** rāda vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="d4fbb-115">Lai ignorētu TDS nodokļu komponentam definēto sliekšņa ierobežojumu un izņēmuma sliekšņa ierobežojumu TDS nodokļu kodam TDS darījumos, atzīmējiet izvēles rūtiņu **Neievērot slieksni**.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="d4fbb-116">Atlasiet **Atbrīvot** izvēles rūtiņu, lai novērstu nodokļu grupas aprēķināšanu darījumos.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="d4fbb-117">Darbību rūtī atlasiet **Veidotājs**, lai atvērtu formulas noformētāju, tādējādi varat definēt formulu TDS aprēķināšanai TDS nodokļu grupai.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="d4fbb-118">Lapā **Veidotājs** cilne **Nodokļi** rāda TDS nodokļu kodus, kas ir atlasīti TDS nodokļu grupai.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="d4fbb-119">[![Veidotāja lapa](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="d4fbb-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="d4fbb-120">Cilnē **Aprēķins** atlasiet **Alt+N**, lai izveidotu rindu.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="d4fbb-121">**ID** lauks parāda automātiski ģenerēto prioritātes ID TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="d4fbb-122">Laukā **Nodokļa kods** atlasiet ieturētā TDS nodokļa kodu, kam definēt formulu.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="d4fbb-123">Visi TDS nodokļu kodi, kas atlasīti TDS nodokļu grupai, ir pieejami atlasei šajā laukā.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="d4fbb-124">Laukā **Apliekamās bāzes** izvēlieties pamatu TDS aprēķināšanai:</span><span class="sxs-lookup"><span data-stu-id="d4fbb-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="d4fbb-125">**Bruto summa** – aprēķina TDS, pamatojoties uz bruto darbību summu (t.i., rēķina summu), izmantojot aprēķina izteiksmi, kas definēta nodokļa kodam.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="d4fbb-126">**Bez bruto summas** – aprēķiniet TDS, pamatojoties uz nodokļu kodam definēto aprēķina izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4fbb-127">Lauku **Apliekamās bāzes** nevar iestatīt uz **Bez bruto summas** TDS nodokļa kodam, kam ir prioritātes ID **1**.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="d4fbb-128">TDS aprēķina pamatā ir formula, kas laukā **Aprēķina izteiksme** noteikta katram nodokļu kodam, kas ir piesaistīts TDS nodokļu grupai.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="d4fbb-129">Atlasiet plus zīmes (**+**), mīnus zīmes (**-**), reizināšanai zīmes (**\**_) vai dalījuma zīmes (_*/**) pogu, lai ievadītu aprēķina izteiksmi atlasītam TDS nodokļa kodam laukā **Aprēķina izteiksme**.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4fbb-130">TDS nodokļa kodam, kura prioritātes ID ir **1**, nevar definēt aprēķina izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="d4fbb-131">Lai definētu aprēķina izteiksmi TDS nodokļu kodam **Aprēķina izteiksmes** laukā, pievienojiet TDS nodokļu kodus, kas ir pieejami cilnē **Nodokļi**. Lai pievienotu TDS nodokļu kodus laukā **Aprēķina izteiksme**, varat izmantot jebkuru no šīm metodēm:</span><span class="sxs-lookup"><span data-stu-id="d4fbb-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="d4fbb-132">Velciet nepieciešamo nodokļa kodu no cilnes **Nodokļi** uz lauku **Aprēķina izteiksme**.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="d4fbb-133">Veiciet dubultklikšķi uz nepieciešamā nodokļu koda cilnē **Nodokļi**.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="d4fbb-134">Atlasiet un turiet (vai veiciet labo klikšķi) pieprasīto nodokļu kodu cilnē **Nodokļi** un pēc tam atlasiet **Pievienot nodokļa kodu**.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4fbb-135">Pirms katra TDS nodokļa koda ievietojiet aprēķina izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="d4fbb-136">Aprēķina izteiksmei pievienotie TDS nodokļu kodi ir redzami iekavās (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="d4fbb-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="d4fbb-137">Lai notīrītu aprēķina izteiksmi, kas noteikta nodokļu kodam laukā **Aprēķina izteiksme**, atlasiet **C** pogu.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="d4fbb-138">Lai dzēstu ierakstu cilnē **Aprēķins**, atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="d4fbb-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d4fbb-139">Close the page.</span></span>
