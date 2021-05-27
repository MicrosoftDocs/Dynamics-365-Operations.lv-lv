---
title: Nodokļu komponentu iestatīšana TDS nodokļu veidam
description: Šajā tēmā skaidrots, kā iestatīt ieturētā nodokļa komponentus No kopējās ienākumu summas atskaitītā nodokļa (TDS) veidam. Dokumentā ir arī izskaidrots, kā definēt sliekšņa ierobežojumu, kas tiek izmantots katra TDS komponenta TDS aprēķinam.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023413"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="6c686-104">Nodokļu komponentu iestatīšana TDS nodokļu veidam</span><span class="sxs-lookup"><span data-stu-id="6c686-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c686-105">Šajā tēmā skaidrots, kā iestatīt ieturētā nodokļa komponentus No kopējās ienākumu summas atskaitītā nodokļa (TDS) veidam.</span><span class="sxs-lookup"><span data-stu-id="6c686-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="6c686-106">TDS komponenti ir TDS, piemaksas, PE-Cess un SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="6c686-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="6c686-107">Šajā tēmā ir arī izskaidrots, kā definēt slieksni, kas tiek izmantots katra TDS komponenta TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="6c686-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="6c686-108">Papildus var definēt izņēmumu slieksni, kas tiek izmantots, lai aprēķinātu TDS katram TDS komponentam.</span><span class="sxs-lookup"><span data-stu-id="6c686-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="6c686-109">Lai iestatītu TDS komponentus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="6c686-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="6c686-110">Atveriet **Nodoklis \> Iestatīšana \> Ieturētais nodoklis \> Ieturētā nodokļa komponenti**.</span><span class="sxs-lookup"><span data-stu-id="6c686-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="6c686-111">[![Ieturētā nodokļa komponentu lapa](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="6c686-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="6c686-112">Laukā **Nodokļu tips** atlasiet **TDS**, lai iestatītu ieturētā nodokļa komponentus TDS nodokļa tipam.</span><span class="sxs-lookup"><span data-stu-id="6c686-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="6c686-113">Lai izveidotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="6c686-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="6c686-114">Laukā **Ieturētā nodokļa komponents** ievadiet TDS komponenta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6c686-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="6c686-115">Laukā **Ieturētā nodokļa komponentu grupa** atlasiet TDS ieturētā nodokļa komponentu grupu, lai pievienotu TDS komponentu.</span><span class="sxs-lookup"><span data-stu-id="6c686-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="6c686-116">Kopsavilkuma cilnē **Vispārīgi** laukā **Apraksts** ievadiet TDS komponenta aprakstu.</span><span class="sxs-lookup"><span data-stu-id="6c686-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="6c686-117">Darbību rūtī atlasiet **Slieksnis**, lai atvērtu lapu **Slieksnis**, tādējādi varat definēt slieksni, kas tiek izmantots TDS komponenta TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="6c686-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="6c686-118">Lai definētu periodu, uz kuru attiecas slieksnis, lietojiet laukus **sākuma datums** un **Beigu datums**.</span><span class="sxs-lookup"><span data-stu-id="6c686-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="6c686-119">Kopsavilkuma cilnē **Vispārīgi**, laukā **Slieksnis** ievadiet sliekšņa summu, kas tiek izmantota TDS komponenta TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="6c686-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="6c686-120">Nodokli atskaita no kopējās ienākumu summas tikai tad, ja kopējā rēķina summa pārsniedz slieksni.</span><span class="sxs-lookup"><span data-stu-id="6c686-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="6c686-121">Piemēram, ja sliekšņa summa ir 10 000, TDS tiek aprēķināts pēc tam, kad kopējā rēķina summa pārsniedz 10 000 (citiem vārdiem, ja tā ir 10 001 vai lielāka).</span><span class="sxs-lookup"><span data-stu-id="6c686-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="6c686-122">Laukā **Izņēmuma slieksnis** ievadiet izņēmuma sliekšņa summu, kas tiek izmantota TDS komponenta TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="6c686-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="6c686-123">Nodokli rēķina rindā atskaita no kopējās ienākumu summas tikai tad, ja summa pārsniedz izņēmuma slieksni.</span><span class="sxs-lookup"><span data-stu-id="6c686-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="6c686-124">Piemēram, ja izņēmuma sliekšņa summa ir 5000, TDS tiek aprēķināts uz noteiktu rēķina rindu, ja rēķina rindas summa pārsniedz 5000 (citiem vārdiem, ja tas ir 5001 vai vairāk).</span><span class="sxs-lookup"><span data-stu-id="6c686-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="6c686-125">[![Sliekšņa lapa](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="6c686-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c686-126">Izņēmuma sliekšņa summai ir jābūt mazākai par sliekšņa summu vai vienādai ar to.</span><span class="sxs-lookup"><span data-stu-id="6c686-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="6c686-127">Nodoklis tiek atskaitīts darījumam, ja darījuma summa pārsniedz izņēmuma slieksni, pat ja kopējā rēķina summa nešķērso sliekšņa robežas, kas ir norādītas laukā **Slieksnis**.</span><span class="sxs-lookup"><span data-stu-id="6c686-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="6c686-128">Aizveriet lapu **Slieksnis**, lai atgrieztos uz lapu **Ieturētā nodokļa komponenti**.</span><span class="sxs-lookup"><span data-stu-id="6c686-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="6c686-129">Darbību rūtī atlasiet **Kopēt**, lai atvērtu dialoglodziņu **Kopēt ieturētā nodokļa komponentus** tādējādi varat kopēt TDS komponentus, kas tika iestatīti vienam TDS komponentu grupai citā TDS komponentu grupā.</span><span class="sxs-lookup"><span data-stu-id="6c686-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="6c686-130">Laukā **No** atlasiet TDS komponentu grupu, no kā kopēt TDS komponentus.</span><span class="sxs-lookup"><span data-stu-id="6c686-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="6c686-131">Laukā **Uz** atlasiet ieturētā nodokļa komponentu grupu, uz kuru kopēt TDS komponentus.</span><span class="sxs-lookup"><span data-stu-id="6c686-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c686-132">Kopējie TDS komponenti, kas ir pievienoti abām TDS komponentu grupām, netiek nokopēti.</span><span class="sxs-lookup"><span data-stu-id="6c686-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="6c686-133">Atlasiet **Labi**, lai kopētu un izveidotu TDS komponentus citai TDS komponentu grupai **Ieturētā nodokļa komponentu** lapā.</span><span class="sxs-lookup"><span data-stu-id="6c686-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="6c686-134">[![Kopēt ieturētā nodokļa komponentu dialoglodziņu](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="6c686-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="6c686-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6c686-135">Close the page.</span></span>
