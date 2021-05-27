---
title: ieturētā nodokļa kodu iestatīšana TDS nodokļu tipam
description: Šajā tēmā skaidrots, kā iestatīt No kopējās ienākumu summas atskaitītā nodokļa (TDS) nodokļa kodus.
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023430"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="8743b-103">ieturētā nodokļa kodu iestatīšana TDS nodokļu tipam</span><span class="sxs-lookup"><span data-stu-id="8743b-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8743b-104">Šajā tēmā skaidrots, kā iestatīt No kopējās ienākumu summas atskaitītā nodokļa (TDS) nodokļa kodus.</span><span class="sxs-lookup"><span data-stu-id="8743b-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="8743b-105">Pārejiet uz sadaļu **Nodokļi \> Netiešie nodokļi \> Ieturētais nodoklis \> ieturētā nodokļa kodi**.</span><span class="sxs-lookup"><span data-stu-id="8743b-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="8743b-106">[![Ieturēto nodokļu kodi lapa](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="8743b-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="8743b-107">Darbību rūtī atlasiet **Jauns**, lai izveidotu ieturētā nodokļa kodu TDS, un ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="8743b-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="8743b-108">Kopsavilkuma cilnes **Vispārīgi** laukā **Nodokļu tips** atlasiet **TDS**, lai nodokļu kodu kategorizētu kā TDS nodokļa kodu.</span><span class="sxs-lookup"><span data-stu-id="8743b-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="8743b-109">Laukā **Norēķinu periods** atlasiet TDS norēķinu periodu TDS nodokļa kodam.</span><span class="sxs-lookup"><span data-stu-id="8743b-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="8743b-110">Laukā **Galvenais konts** atlasiet virsgrāmatas kontu, kurā jāgrāmato TDS summa.</span><span class="sxs-lookup"><span data-stu-id="8743b-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="8743b-111">Laukā **Debitoru konts** atlasiet debitoru kontu, kurā jāgrāmato TDS summa, kas ir ieturēta pārdošanas darījumos.</span><span class="sxs-lookup"><span data-stu-id="8743b-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="8743b-112">Lauks **Izcelsme** automātiski tiek iestatīts kā **Procenti no bruto summas**, un vērtību nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="8743b-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8743b-113">TDS nodokļu tipa nodokļu kodiem nevar iestatīt izcelsmi **Procenti no neto summas**.</span><span class="sxs-lookup"><span data-stu-id="8743b-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="8743b-114">Laukā **ieturētā nodokļa komponents** atlasiet ieturētā TDS nodokļa komponentu TDS nodokļu kodam.</span><span class="sxs-lookup"><span data-stu-id="8743b-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="8743b-115">Darbību rūtī atlasiet **Vērtības**, lai atvērtu lapu **ieturētā nodokļa vērtības**.</span><span class="sxs-lookup"><span data-stu-id="8743b-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="8743b-116">Laukā **Sākuma datums** ievadiet TDS vērtības sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="8743b-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="8743b-117">Laukā **Beigu datums** ievadiet beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="8743b-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8743b-118">Lauki **Minimālais limits**, **Augšējais limits** un **Izņemot %** nav pieejami TDS nodokļu tipa nodokļu kodiem.</span><span class="sxs-lookup"><span data-stu-id="8743b-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="8743b-119">Laukā **Vērtība** ievadiet TDS nodokļa kodam izmantojamo TDS procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="8743b-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="8743b-120">Aizveriet lapu **ieturētā nodokļa vērtības**, lai atgrieztos **ieturētā nodokļa kodu** lapā.</span><span class="sxs-lookup"><span data-stu-id="8743b-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8743b-121">Poga **Limiti** lapā **ieturētā nodokļa kodi** nav pieejama TDS nodokļa tipa nodokļa kodiem.</span><span class="sxs-lookup"><span data-stu-id="8743b-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="8743b-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8743b-122">Close the page.</span></span>
