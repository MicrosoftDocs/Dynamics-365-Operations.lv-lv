---
title: TDS sertifikātu numurus un datumus atjaunināšana TDS darījumiem
description: Šajā tēmā skaidrots, kā atjaunināt atjaunojamo sertifikātu numurus un datumus, kas tiek saņemti noteiktiem kreditoru, debitoru vai virsgrāmatas kontiem No kopējo ienākumu summas atskaitītajam nodoklim (TDS).
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023414"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="10e6c-103">TDS sertifikātu numurus un datumus atjaunināšana TDS darījumiem</span><span class="sxs-lookup"><span data-stu-id="10e6c-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10e6c-104">Šajā tēmā skaidrots, kā atjaunināt atjaunojamo sertifikātu numurus un datumus, kas tiek saņemti noteiktiem kreditoru, debitoru vai virsgrāmatas kontiem No kopējo ienākumu summas atskaitītajam nodoklim (TDS).</span><span class="sxs-lookup"><span data-stu-id="10e6c-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="10e6c-105">Varat apskatīt sertifikātus TDS darījumiem lapā **Atjaunojamie sertifikāti**.</span><span class="sxs-lookup"><span data-stu-id="10e6c-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="10e6c-106">Sertifikātus var atjaunināt, izmantojot lapu **Atjaunināt sertifikātus**.</span><span class="sxs-lookup"><span data-stu-id="10e6c-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="10e6c-107">Izpildiet šīs darbības, lai atjauninātu TDS darījumu sertifikātu numurus un datumus.</span><span class="sxs-lookup"><span data-stu-id="10e6c-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="10e6c-108">Atveriet **Nodoklis \> Deklarācijas \> Ieturētais nodoklis \> Atjaunināt sertifikātu**.</span><span class="sxs-lookup"><span data-stu-id="10e6c-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="10e6c-109">[![Atjaunināt sertifikāta lapa](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="10e6c-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="10e6c-110">Lapā **Atjaunināt sertifikātu**, sadaļā **Atlasīt**, laukā **Nodokļu tips** atlasiet **TDS**.</span><span class="sxs-lookup"><span data-stu-id="10e6c-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="10e6c-111">Laukā **Sertifikāta numurs** atlasiet debitora vai kreditora TDS sertifikāta numuru.</span><span class="sxs-lookup"><span data-stu-id="10e6c-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10e6c-112">**Sertifikātu numuru** laukā tiek uzskaitīti tikai TDS sertifikātu numuri, kuriem lapā **Atgūstamie sertifikāti** tiek notīrīta izvēles rūtiņa **Aizvērts**.</span><span class="sxs-lookup"><span data-stu-id="10e6c-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="10e6c-113">Laukā **Sertifikāta datums** tiek parādīts sertifikāta datums.</span><span class="sxs-lookup"><span data-stu-id="10e6c-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="10e6c-114">Lauks **Konta tips** parāda konta tipu, kam TDS sertifikāta numurs ir saņemts, un laukā **Nosaukums** tiek parādīts konta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="10e6c-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="10e6c-115">Laukos **Datums no** un **Datums līdz** atlasiet perioda sākuma un beigu datumus, lai parādītu TDS darījumus.</span><span class="sxs-lookup"><span data-stu-id="10e6c-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="10e6c-116">Atlasiet **Rādīt datus**, lai skatītu TDS darījumus, kas grāmatoti atlasītajā periodā.</span><span class="sxs-lookup"><span data-stu-id="10e6c-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="10e6c-117">Cilnes **Pārskats** režģis augšējā rūtī rāda šādu informāciju par katru TDS darījumu, kas tika grāmatots kreditoram vai debitoram atlasītajā periodā:</span><span class="sxs-lookup"><span data-stu-id="10e6c-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="10e6c-118">**Dokuments** – TDS darījuma dokumenta numurs.</span><span class="sxs-lookup"><span data-stu-id="10e6c-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="10e6c-119">**Datums** – TDS darījuma datums.</span><span class="sxs-lookup"><span data-stu-id="10e6c-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="10e6c-120">**Summa** – rēķina summa, pēc kuras tika aprēķināta TDS.</span><span class="sxs-lookup"><span data-stu-id="10e6c-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="10e6c-121">**Nodokļu summa** – TDS nodokļa summa, kas tika aprēķināta darījumam.</span><span class="sxs-lookup"><span data-stu-id="10e6c-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="10e6c-122">Lai pārvietotu noteiktus TDS darījumus no augšējā režģa uz apakšējo režģi, atlasiet darījumus un pēc tam atlasiet **Iekļaut**.</span><span class="sxs-lookup"><span data-stu-id="10e6c-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="10e6c-123">Pēc izvēles atlasiet opciju **Iekļaut visu**, lai pārvietotu visus TDS darījumus no augšējās režģa uz apakšējo režģi.</span><span class="sxs-lookup"><span data-stu-id="10e6c-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="10e6c-124">Lai pārvietotu noteiktus TDS darījumus vai visus TDS darījumus no apakšējā režģa uz augšējo režģi, izmantojiet pogu **Izslēgt** vai **Izslēgt visu**.</span><span class="sxs-lookup"><span data-stu-id="10e6c-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="10e6c-125">Atlasiet **Atjaunināt**, lai apakšējā režģī atjauninātu **Sertifikāta numura** un **Sertifikāta datuma** laukus TDS darījumiem.</span><span class="sxs-lookup"><span data-stu-id="10e6c-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="10e6c-126">Dodieties uz **Nodoklis \> Netiešie nodokļi \> Ieturētais nodoklis \> Atjaunojamais sertifikāts** un atlasiet **Vaicājums** lai skatītu atjauninātās darījumu rindas, kurām **Sertifikātu darījumu** lapā ir jauni sertifikātu numuri.</span><span class="sxs-lookup"><span data-stu-id="10e6c-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="10e6c-127">[![Sertifikāta darījumi lapa](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="10e6c-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
