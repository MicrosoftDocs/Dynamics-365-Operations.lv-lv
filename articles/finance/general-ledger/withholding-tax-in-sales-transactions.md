---
title: Ieturētais nodoklis pārdošanas darījumos
description: Šajā tēmā ir uzskaitītas darbības, lai izvairītos no ieturētā nodokļa aprēķināšanas atlasītajiem debitoriem. Debitoriem, kuri savos maksājumos norāda ieturamo nodokli, varat piešķirt noklusēto ieturētā nodokļa grupu.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060766"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="29a0d-104">Ieturētais nodoklis pārdošanas darījumos</span><span class="sxs-lookup"><span data-stu-id="29a0d-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="29a0d-105">Šajā tēmā ir uzskaitītas darbības, lai izvairītos no ieturētā nodokļa aprēķināšanas atlasītajiem debitoriem.</span><span class="sxs-lookup"><span data-stu-id="29a0d-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="29a0d-106">Klientiem, kuri savos maksājumos norāda ieturamo nodokli, varat piešķirt noklusēto **Ieturētā nodokļa grupu** lapā **Klienti**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="29a0d-107">Dodieties uz sadaļu **Navigācijas rūts > Moduļi > Debitori > Klienti > Visi klienti**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="29a0d-108">Noklikšķiniet uz attiecīgā klienta konta, noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="29a0d-109">Cilnē **Rēķins un piegāde** iestatiet lauku **Aprēķināt ieturēto nodokli** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="29a0d-110">Ieturētais nodoklis netiks aprēķināts, ja pamatdatos šim klientam nav ieslēgts **Aprēķināt ieturēto nodokli**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="29a0d-111">Atlasiet ieturētā nodokļa grupu **Ieturētā nodokļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="29a0d-112">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-112">Click **Save**.</span></span>

<span data-ttu-id="29a0d-113">Krājumiem/pakalpojumiem, kas ir apliekami ar ieturēto nodokli, varat piešķirt noklusējuma **Krājuma ieturētā nodokļa grupu** sadaļā **Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="29a0d-114">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="29a0d-115">Noklikšķiniet uz attiecīgā vienuma numura, noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="29a0d-116">Cilnē **Pārdošana** noklikšķiniet uz **Aprēķināt ieturēto nodokli**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="29a0d-117">Ieturētais nodoklis netiks aprēķināts, ja **Aprēķināt ieturēto nodokli** nav iestatīts uz **Jā** šim krājumam cilnē **Pārdot** lapā **Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="29a0d-118">Atlasiet krājuma ieturētā nodokļa grupu sarakstā **Krājuma ieturētā nodokļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="29a0d-119">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-119">Click **Save**.</span></span>

<span data-ttu-id="29a0d-120">Ieturētā nodokļa grupas un krājuma ieturētā nodokļa grupas var piešķirt, izmantojot lapu **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="29a0d-121">Noklusējuma ieturētā nodokļa grupa un krājuma ieturētā nodokļa grupa tiks izmantota kā noklusējuma ieraksti pārdošanas pasūtījuma rindās, veidojot jaunu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="29a0d-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="29a0d-122">Ieturētais nodoklis tiek aprēķināts un grāmatots **Klientu maksājumu žurnālā**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="29a0d-123">Varat manuāli koriģēt piemērojamo ieturētā nodokļa kodu, kā arī faktisko ieturētā nodokļa summu cilnē **Ieturētais nodoklis** lapā **Transakciju kārtošana**.</span><span class="sxs-lookup"><span data-stu-id="29a0d-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="29a0d-124">Aprēķinātā ieturētā nodokļa summa tiks atskaitīta no klienta maksājuma un grāmatota kontā **Ieturētā nodokļa korespondējošais konts** saistītā dokumentā.</span><span class="sxs-lookup"><span data-stu-id="29a0d-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>
