---
title: Izdevumu kvīšu apstrāde
description: Šajā tēmā ir sniegta informācija par kvīšu optiskās rakstzīmju atpazīšanas (OCR) apstrādi. Šis līdzeklis ir paredzēts lietotāja pieredzes uzlabošanai, veidojot izdevumu pārskatus programmā Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: efba2faf9428d9b556d74273bc7daadba7211c48
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248967"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="0d6d6-104">Izdevumu ieejas apstrāde</span><span class="sxs-lookup"><span data-stu-id="0d6d6-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d6d6-105">Izdevumu ieraksts ir uzlabots, ieviešot kvīšu optiskās rakstzīmju pazīšanas (OCR) apstrādi.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="0d6d6-106">Šis līdzeklis ir paredzēts lietotāja pieredzes uzlabošanai, veidojot izdevumu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="0d6d6-107">Galvenie līdzekļi</span><span class="sxs-lookup"><span data-stu-id="0d6d6-107">Key features</span></span>

- <span data-ttu-id="0d6d6-108">No kvītīm tiek izgūts tirgotāja nosaukums, datums un kopējā summa.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="0d6d6-109">Šis līdzeklis mēģina saskaņot nepievienotās kvītis ar nepievienotām izdevumu darbībām.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="0d6d6-110">Lietotāji var no kvītīm izveidot manuāli ievadītas izdevumu darbības.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="0d6d6-111">Lietojuma piemēri</span><span class="sxs-lookup"><span data-stu-id="0d6d6-111">Usage examples</span></span>

- <span data-ttu-id="0d6d6-112">**Automātiski pievienojiet kvītis, kas, veidojot izdevumu pārskatu, ietver kredītkartes darbības.**</span><span class="sxs-lookup"><span data-stu-id="0d6d6-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="0d6d6-113">Atveriet darbvietu **Izdevumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="0d6d6-114">Cilnē **Kvītis** pārbaudiet, vai pastāv nepievienotas kvītis.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="0d6d6-115">Kvītis varat augšupielādēt arī cilnē **Kvītis**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="0d6d6-116">Cilnē **Izdevumi** pārbaudiet, vai pastāv nepievienoti izdevumi.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="0d6d6-117">Parasti izdevumu administrators importē šos izdevumus no kredītkartes nodrošinātāja.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="0d6d6-118">Atlasiet **Jauns izdevumu pārskats**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-118">Select **New expense report**.</span></span> <span data-ttu-id="0d6d6-119">Ievērojiet, ka tagad, veidojot izdevumu pārskatu, var iekļaut arī izdevumus un kvītis.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="0d6d6-120">Ja pievienojat gan izdevumus, gan kvīti,, automātiski tiek aktivizēta kvīšu salīdzināšana ar izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="0d6d6-121">**Izveidojiet izdevumus vai saskaņojiet kvītī norādītos izdevumus.**</span><span class="sxs-lookup"><span data-stu-id="0d6d6-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="0d6d6-122">Pievienojiet kvīti izdevumu pārskata cilnē **Kvītis**, atlasot **Pievienot kvītis**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="0d6d6-123">Zem augšupielādētā kvīts attēla ievērojiet opcijas **Izveidot** un **Saskaņot**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="0d6d6-124">Atlasiet **Izveidot**, lai izveidotu manuāli ievadītu izdevumu darbību, un ievadiet vērtības, kas izgūtas no kvīts.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="0d6d6-125">Ja atlasāt **Saskaņot**, sistēma mēģina saskaņot esošus izdevumus ar kvīti.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="0d6d6-126">Instalēšana</span><span class="sxs-lookup"><span data-stu-id="0d6d6-126">Installation</span></span>

<span data-ttu-id="0d6d6-127">Šis līdzeklis darbojas kombinācijā ar līdzekli **Izdevumu pārskati jaunā izskatā**, tādējādi vienkāršojot izdevumu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="0d6d6-128">Lai izmantotu šīs uzlabotās izdevumu iespējas, instalējiet Microsoft Dynamics 365 Finance izdevumu pārvaldības pakalpojuma pievienojumprogrammu un ieslēdziet līdzekļus savā instancē.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="0d6d6-129">Jūs variet piekļūt pievienojumprogrammai no sava projekta pakalpojumā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0d6d6-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="0d6d6-130">Piesakieties LCS un atveriet vēlamo vidi.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="0d6d6-131">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="0d6d6-132">Atlasiet **Uzturēt**vai ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="0d6d6-133">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="0d6d6-134">Atlasiet **Izdevumu pārvaldības pakalpojumi**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="0d6d6-135">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="0d6d6-136">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-136">Select **Install**.</span></span>

<span data-ttu-id="0d6d6-137">Darbvietā **Līdzekļu pārvaldība** aktivizējiet tālāk norādītos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="0d6d6-138">Izdevumu pārskati atkārtoti attēloti</span><span class="sxs-lookup"><span data-stu-id="0d6d6-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="0d6d6-139">Automātiski saskaņot un izveidot izdevumus no kvīts</span><span class="sxs-lookup"><span data-stu-id="0d6d6-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="0d6d6-140">Ieslēdzot šos līdzekļus, notiek tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="0d6d6-141">Esošā darbvieta **Izdevumu pārvaldība** tiek aizstāta ar jauno darbvietu.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="0d6d6-142">Tiek pievienots jauns izvēlnes elements izdevumu lauku redzamībai.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="0d6d6-143">Jūs joprojām varat atvērt bijušo lapu **Izdevumu pārskati**, pārejot uz **Izdevumu pārvaldība > Mani izdevumi > Izdevumu pārskati**.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="0d6d6-144">Darbplūsmas un visi apstiprinājumi vēl aizvien novirza uz esošo izdevumu pārskatu lapu.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="0d6d6-145">Kvītis tiks apstrādātas, izmantojot Microsoft Azure Cognitive Services, un tiks izgūti un pievienoti metadati.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="0d6d6-146">Tiek pievienota opcija, kas ļauj izveidot izdevumu pārskatu, kurā iekļautas saskaņotās nepievienotās kvītis.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="0d6d6-147">Izdevumu pārskatiem pievienotā opcija ļauj izveidot izdevumu rindu no kvīts vai mēģina saskaņot esošu kvīti ar esošu izdevumu rindu.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="0d6d6-148">Papildu informāciju par līdzekli izdevumu pārskati jaunā izskatā skatiet sadaļā [Izdevumu pārskati jaunā izskatā](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="0d6d6-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="0d6d6-149">Bieži uzdotie jautājumi</span><span class="sxs-lookup"><span data-stu-id="0d6d6-149">Frequently asked questions</span></span>

<span data-ttu-id="0d6d6-150">**Vai Microsoft izmanto manus datus saviem modeļiem?**</span><span class="sxs-lookup"><span data-stu-id="0d6d6-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="0d6d6-151">Nē, Microsoft ir izveidojusi vispārīgu algoritmiskās mācīšanās modeli savam kvīšu apstrādes pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="0d6d6-152">Šis modelis nav balstīts jūsu augšupielādētajam kvītīm.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="0d6d6-153">**Kur šis līdzeklis ir pieejams un apstrādāts?**</span><span class="sxs-lookup"><span data-stu-id="0d6d6-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="0d6d6-154">Šobrīd tiek atbalstītas Amerikas Savienotās Valstis.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="0d6d6-155">**Kur nonāk manas kvītis?**</span><span class="sxs-lookup"><span data-stu-id="0d6d6-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="0d6d6-156">Finance sazināsies ar Cognitive Services, lai izgūtu lauka datus.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="0d6d6-157">Cognitive Services saglabās kvīts kopiju līdz pat 24 stundām, kamēr tiek veikta apstrāde.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="0d6d6-158">Pēc apstrādes pabeigšanas Cognitive Services kvīti noņems.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="0d6d6-159">Kvīts joprojām tiek uzglabāta programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="0d6d6-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="0d6d6-160">Papildinformāciju skatiet sadaļā [Izpratnes par kvītīm aktivizēšana, izmantojot veidlapu atpazinēja jaunās iespējas](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="0d6d6-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
