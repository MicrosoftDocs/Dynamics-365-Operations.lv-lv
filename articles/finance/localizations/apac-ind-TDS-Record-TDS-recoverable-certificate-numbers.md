---
title: Ierakstīt atjaunojamos TDS sertifikātu numurus
description: Šajā tēmā skaidrots, kā izmantot atjaunojamo sertifikātu lapu, lai ierakstītu sertifikātu numurus un datumus No kopējo ienākumu summas atskaitītā nodokļa (TDS) sertifikātiem, kas tiek saņemti noteiktam kreditoram, debitoram vai virsgrāmatai.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023404"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="917af-103">Ierakstīt atjaunojamos TDS sertifikātu numurus</span><span class="sxs-lookup"><span data-stu-id="917af-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="917af-104">Šajā tēmā skaidrots, kā izmantot **Atjaunojamo sertifikātu** lapu, lai ierakstītu sertifikātu numurus un datumus No kopējo ienākumu summas atskaitītā nodokļa (TDS) sertifikātiem, kas tiek saņemti noteiktam kreditoram, debitoram vai virsgrāmatai.</span><span class="sxs-lookup"><span data-stu-id="917af-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="917af-105">Lai atjauninātu TDS sertifikātu numurus un datumus, kas ierakstīti TDS darījumiem šajā lapā, izmantojiet **Atjaunināt sertifikātu** lapu (**Virsgrāmata \> Periodiski \> Ieturētais nodoklis \> Atjaunināt sertifikātu**).</span><span class="sxs-lookup"><span data-stu-id="917af-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="917af-106">Kad TDS sertifikātu numuru atjaunināšana ir pabeigta, aizveriet tos.</span><span class="sxs-lookup"><span data-stu-id="917af-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="917af-107">Izpildiet šīs darbības, lai ierakstītu TDS sertifikātu numurus un datumus.</span><span class="sxs-lookup"><span data-stu-id="917af-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="917af-108">Pārejiet uz sadaļu **Nodokļi \> Netiešais nodoklis \> Ieturētais nodoklis \> Atjaunojamie sertifikāti**.</span><span class="sxs-lookup"><span data-stu-id="917af-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="917af-109">[![Atjaunojamo sertifikātu lapa](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="917af-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="917af-110">Lapā **Atjaunojamie sertifikāti** laukā **Nodokļa tips** atlasiet **TDS**.</span><span class="sxs-lookup"><span data-stu-id="917af-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="917af-111">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="917af-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="917af-112">Laukā **Sertifikātu numurs** ievadiet TDS sertifikāta numuru.</span><span class="sxs-lookup"><span data-stu-id="917af-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="917af-113">Laukā **Konta tips** atlasiet konta tipu, kam TDS sertifikāts tiek saņemts: **Kreditoram**, **Debitoram** vai **Virsgrāmatai**.</span><span class="sxs-lookup"><span data-stu-id="917af-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="917af-114">Laukā **Konts** atlasiet kreditora, debitora vai virsgrāmatas konta numuru, atkarībā no atlasītā konta tipa.</span><span class="sxs-lookup"><span data-stu-id="917af-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="917af-115">Laukā **Nosaukums** ir norādīts kreditora, debitora vai virsgrāmatas konta nosaukums.</span><span class="sxs-lookup"><span data-stu-id="917af-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="917af-116">Laukā **Sertifikāta summa** ievadiet TDS sertifikāta summu.</span><span class="sxs-lookup"><span data-stu-id="917af-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="917af-117">Laukā **Datums** ievadiet sertifikāta numura datums.</span><span class="sxs-lookup"><span data-stu-id="917af-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="917af-118">Atlasiet **Uzziņas**, lai atvērtu lapu **Sertifikātu darījumi**, kur varat apskatīt TDS darījumus, kam TDS sertifikāta numurs un datums ir atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="917af-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="917af-119">Šo informāciju var atjaunināt laukā **Atjaunināt sertifikātu** (**Nodokļi \> Deklarācijas \> Ieturētais nodoklis \> Atjaunināt sertifikātu**).</span><span class="sxs-lookup"><span data-stu-id="917af-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="917af-120">Lapa **Atjaunināt sertifikātu** parāda šādu informāciju par katru TDS darījumu:</span><span class="sxs-lookup"><span data-stu-id="917af-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="917af-121">**Datums** – TDS darījumu grāmatošanas datums.</span><span class="sxs-lookup"><span data-stu-id="917af-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="917af-122">**Dokuments** – TDS darījuma dokumenta numurs.</span><span class="sxs-lookup"><span data-stu-id="917af-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="917af-123">**Avots** - modulis, kurā TDS darījums tika izveidots.</span><span class="sxs-lookup"><span data-stu-id="917af-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="917af-124">**Konts** – kreditora, debitora vai virsgrāmatas konta numurs, kuram TDS darījums tika izveidots.</span><span class="sxs-lookup"><span data-stu-id="917af-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="917af-125">**Nosaukums** – kreditora, debitora vai virsgrāmatas konta nosaukums, kuram TDS darījums tika izveidots.</span><span class="sxs-lookup"><span data-stu-id="917af-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="917af-126">**Summa** – rēķina summa, pēc kuras tika aprēķināta TDS.</span><span class="sxs-lookup"><span data-stu-id="917af-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="917af-127">**Nodokļu summa** – TDS nodokļa summa, kas tika aprēķināta darījumam.</span><span class="sxs-lookup"><span data-stu-id="917af-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="917af-128">**Sertifikāta datums** – TDS sertifikāta datums, kas tika atjaunināts TDS darījumam.</span><span class="sxs-lookup"><span data-stu-id="917af-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="917af-129">**Sertifikāta numurs** – TDS sertifikāta numurs, kas tika atjaunināts TDS darījumam.</span><span class="sxs-lookup"><span data-stu-id="917af-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="917af-130">Laukā **Atjaunojamie sertifikāti** atlasiet izvēles rūtiņu **Slēgts**, lai aizvērtu TDS sertifikāta numuru pēc tam, kad esat beidzis tā atjaunināšanu TDS darījumiem lapā **Atjaunināt sertifikātu**.</span><span class="sxs-lookup"><span data-stu-id="917af-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="917af-131">Lai atlasītu izvēles rūtiņu **Slēgts** visiem lapas ierakstiem, atlasiet **Atzīmēt visu**.</span><span class="sxs-lookup"><span data-stu-id="917af-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="917af-132">TDS sertifikātu numuri, kuriem atzīmēta izvēles rūtiņa **Slēgts**, nav pieejami lapā **Atjaunināt sertifikātu**.</span><span class="sxs-lookup"><span data-stu-id="917af-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
