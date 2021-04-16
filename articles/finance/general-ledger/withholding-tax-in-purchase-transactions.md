---
title: Ieturētais nodoklis pirkšanas darījumos
description: Piegādātājiem, uz kuriem attiecas ieturamais nodoklis, varat piešķirt noklusēto **Ieturētā nodokļa grupu** lapā **Visi piegādātāji**.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: faeaf0746532875d3517a208c9c338c112bf2c77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816887"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="f9d0b-103">Ieturētais nodoklis pirkšanas darījumos</span><span class="sxs-lookup"><span data-stu-id="f9d0b-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="f9d0b-104">Piegādātājiem, uz kuriem attiecas ieturamais nodoklis, varat piešķirt noklusēto **Ieturētā nodokļa grupu** lapā **Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="f9d0b-105">Dodieties uz **Navigācijas rūts > Moduļi > Kreditori > Piegādātāji > Visi piegādātāji**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="f9d0b-106">Noklikšķiniet uz attiecīgā piegādātāja konta, noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="f9d0b-107">Cilnē **Rēķins un piegāde** iestatiet lauku **Aprēķināt ieturēto nodokli** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f9d0b-108">Ieturētais nodoklis netiks aprēķināts, ja datos šim piegādātājam nav ieslēgts **Aprēķināt ieturēto nodokli**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="f9d0b-109">Atlasiet ieturētā nodokļa grupu **Ieturētā nodokļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="f9d0b-110">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-110">Click **Save**.</span></span>

<span data-ttu-id="f9d0b-111">Krājumiem/pakalpojumiem, kas ir apliekami ar ieturēto nodokli, varat piešķirt noklusējuma **Krājuma ieturētā nodokļa grupu** sadaļā **Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="f9d0b-112">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="f9d0b-113">Noklikšķiniet uz attiecīgā vienuma numura, noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="f9d0b-114">Cilnē **Pirkums** noklikšķiniet uz **Aprēķināt ieturēto nodokli**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f9d0b-115">Ieturētais nodoklis netiks aprēķināts, ja **Aprēķināt ieturēto nodokli** nav iestatīts uz **Jā** šim krājumam cilnē **Pirkt** lapā **Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="f9d0b-116">Atlasiet krājuma ieturētā nodokļa grupu sarakstā **Krājuma ieturētā nodokļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="f9d0b-117">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-117">Click **Save**.</span></span>

<span data-ttu-id="f9d0b-118">Ieturētā nodokļa grupas un krājuma ieturētā nodokļa grupas var piešķirt tālāk minētajās lapās.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="f9d0b-119">**Pirkšanas pasūtījums**</span><span class="sxs-lookup"><span data-stu-id="f9d0b-119">**Purchase order**</span></span>
- <span data-ttu-id="f9d0b-120">**Kreditora rēķins**</span><span class="sxs-lookup"><span data-stu-id="f9d0b-120">**Vendor invoice**</span></span>
- <span data-ttu-id="f9d0b-121">**Rēķinu žurnāls**</span><span class="sxs-lookup"><span data-stu-id="f9d0b-121">**Invoice journal**</span></span>

<span data-ttu-id="f9d0b-122">Noklusējuma ieturētā nodokļa grupa un vienuma ieturētā nodokļa grupa tiks iekļauta rindās, veidojot **Pirkšanas pasūtījumus** un/vai **Neapmaksātos piegādātāja rēķinus**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="f9d0b-123">**Piegādātāju rēķinu žurnālam** varat ieslēgt **Aprēķināt ieturēto nodokli** un atlasīt **Vienuma ieturētā nodokļa grupa** žurnāla cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="f9d0b-124">Ieturētā nodokļa pagaidu summa ir pieejama laukā **Koriģētais ieturētais nodoklis** cilnē **Kopsummas** lapā **Pirkšanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Ieturētais nodoklis ir iekļauts pirkšanas pasūtījumā](media/withholding-tax-adjusted.png)

<span data-ttu-id="f9d0b-126">Ieturētais nodoklis tiek aprēķināts **Piegādātāja maksājumu žurnālā**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="f9d0b-127">Varat manuāli koriģēt piemērojamos ieturētā nodokļa kodus, kā arī faktiskās ieturētā nodokļa summas cilnē **Ieturētais nodoklis** lapā **Transakciju kārtošana**.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Ieturēto summu var manuāli koriģēt lapā Transakciju izpilde](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="f9d0b-129">Atvasinātā ieturētā nodokļa summa tiks atskaitīta no piegādātāja maksājuma un grāmatota **Ieturētā nodokļa korespondējošais konts** saistītā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="f9d0b-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Ieturētā nodokļa konts, kas rāda saistīto dokumentu](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]