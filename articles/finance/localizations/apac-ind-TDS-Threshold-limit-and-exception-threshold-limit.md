---
title: Sliekšņa ierobežojums un izņēmuma sliekšņa ierobežojums
description: Šajā tēmā ir aprakstīts No kopējo ienākumu summas atskaitītā nodokļa (TDS) slieksnis un izņēmuma ierobežojumi.
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
ms.openlocfilehash: 1bf0d3a01ede559d288581d3b58b3777d0e608dc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023412"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a><span data-ttu-id="9352e-103">Sliekšņa ierobežojums un izņēmuma sliekšņa ierobežojums</span><span class="sxs-lookup"><span data-stu-id="9352e-103">Threshold limit and exception threshold limit</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9352e-104">Šajā tēmā ir aprakstīts No kopējo ienākumu summas atskaitītā nodokļa (TDS) slieksnis un izņēmuma ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="9352e-104">This topic describes the threshold and exception limits for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="9352e-105">TDS rēķinos un maksājumos vienmēr tiek aprēķināts, ņemot vērā sliekšņa ierobežojumu un izņēmuma sliekšņa ierobežojumu, kas definēti TDS nodokļa komponentiem lapā **ieturētā nodokļa komponenti**.</span><span class="sxs-lookup"><span data-stu-id="9352e-105">The TDS on invoices and payments is always calculated considering the threshold limit and exception threshold limit defined for the TDS tax components on the **Withholding tax components** page.</span></span> <span data-ttu-id="9352e-106">TDS nodokļu komponenti ir pievienoti TDS nodokļu kodiem, kas ir iekļauti TDS nodokļu grupās.</span><span class="sxs-lookup"><span data-stu-id="9352e-106">The TDS tax components are attached to TDS tax codes, which are included in the TDS tax groups.</span></span> <span data-ttu-id="9352e-107">TDS nodokļu grupas ir pievienotas kreditoriem un debitoriem, lai aprēķinātu TDS rēķina līmenī vai maksājuma līmenī.</span><span class="sxs-lookup"><span data-stu-id="9352e-107">The TDS tax groups are attached to vendors and customers to calculate TDS at the invoice-level or payment-level.</span></span>

<span data-ttu-id="9352e-108">TDS tiek aprēķināts, ja summa darījumam vai kumulatīvajiem darījumiem, kas grāmatotas ar noteiktu TDS grupu kreditoram, pārsniedz sliekšņa ierobežojumu, kas norādīts lapā **ieturētā nodokļa komponenti**.</span><span class="sxs-lookup"><span data-stu-id="9352e-108">TDS is calculated if the amount for a transaction or the cumulative transactions posted with a specific TDS group for a vendor exceeds the threshold limit specified on the **Withholding tax components** page.</span></span> <span data-ttu-id="9352e-109">TDS netiks aprēķināts, kamēr kumulatīvā darījuma summa nepārsniedz norādīto sliekšņa ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="9352e-109">TDS will not be calculated until the cumulative transaction amount exceeds the specified threshold limit.</span></span>

<span data-ttu-id="9352e-110">Ja kopā ar TDS komponenta sliekšņa ierobežojumu tiek norādīts izņēmuma sliekšņa ierobežojums, TDS tiek aprēķināts, ja noteikta darījuma summa pārsniedz izņēmuma sliekšņa ierobežojumu pat tad, ja kopējā darījuma summa nepārsniedz norādīto sliekšņa ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="9352e-110">If an exception threshold limit is specified along with the threshold limit for a TDS component, TDS is calculated when a specific transaction amount exceeds the exception threshold limit even if the cumulative transaction amount does not exceed the specified threshold limit.</span></span>

### <a name="example"></a><span data-ttu-id="9352e-111">Paraugs</span><span class="sxs-lookup"><span data-stu-id="9352e-111">Example</span></span>
<span data-ttu-id="9352e-112">Nodokļu komponents ar nosaukumu TDS ir iestatīts un pievienots TDS nodokļu grupai ar nosaukumu Līgumdarbinieks.</span><span class="sxs-lookup"><span data-stu-id="9352e-112">A tax component called TDS is set up and attached to the TDS tax group called Contractor.</span></span> <span data-ttu-id="9352e-113">Slieksnis ir definēts kā 50 000, un TDS nodokļa komponentam izņēmuma slieksnis ir definēts kā 20 000.</span><span class="sxs-lookup"><span data-stu-id="9352e-113">The threshold has been defined as 50,000 and exception threshold has been defined as 20,000 for TDS tax component.</span></span> <span data-ttu-id="9352e-114">TDS grupas līgumdarbinieks ir definēts kā noklusējuma TDS grupa 1. kreditoram.</span><span class="sxs-lookup"><span data-stu-id="9352e-114">The TDS group contractor is defined as the default TDS group for vendor 1.</span></span>

<span data-ttu-id="9352e-115">Pirkšanas rēķins 001 ir grāmatots 1. kreditoram par 10 000.</span><span class="sxs-lookup"><span data-stu-id="9352e-115">A purchase invoice 001 is posted for vendor 1 for 10000.</span></span> <span data-ttu-id="9352e-116">TDS netiek aprēķināts rēķinam, jo rēķina summa nav pārsniegusi sliekšņa ierobežojumu vai izņēmumu sliekšņa ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="9352e-116">TDS is not calculated for the invoice because the invoice amount has not crossed the threshold limit or exception threshold limit.</span></span> <span data-ttu-id="9352e-117">Pirkšanas rēķins 002 ir grāmatots 1. kreditoram par 25 000.</span><span class="sxs-lookup"><span data-stu-id="9352e-117">A purchase invoice 002 is posted for vendor 1 for 25,000.</span></span> <span data-ttu-id="9352e-118">TDS tiek aprēķināts rēķinam, jo rēķina summa ir pārsniegusi izņēmumu sliekšņa ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="9352e-118">TDS is calculated for the invoice because the invoice amount has crossed the exception threshold limit.</span></span> <span data-ttu-id="9352e-119">Pirkšanas rēķins 003 ir grāmatots 1. kreditoram par 20 000.</span><span class="sxs-lookup"><span data-stu-id="9352e-119">A purchase invoice 003 is posted for Vendor 1 for 20,000.</span></span> <span data-ttu-id="9352e-120">TDS tiek aprēķināts rēķinam, jo trīs kreditoram izsniegto rēķinu kopējā rēķina summa ir pārsniegusi sliekšņa ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="9352e-120">TDS is calculated for the invoice because the total invoice amount of the three invoices that are issued for the vendor has crossed the threshold limit.</span></span> <span data-ttu-id="9352e-121">TDS tiek aprēķināts visiem rēķiniem, kas tiek izsniegti kreditoram, kuram TDS nav aprēķināts iepriekš.</span><span class="sxs-lookup"><span data-stu-id="9352e-121">TDS is calculated on all invoices that are issued for the vendor on which the TDS has not been calculated earlier.</span></span> <span data-ttu-id="9352e-122">Tādējādi TDS tiek aprēķināts summai 30 000, kas ir kopējā summa rēķiniem 001 un 003.</span><span class="sxs-lookup"><span data-stu-id="9352e-122">Therefore, TDS is calculated on 30,000, which is the total invoice amount of invoice 001 and 003.</span></span>

<span data-ttu-id="9352e-123">Sliekšņa ierobežojums un izņēmuma sliekšņa ierobežojums netiek pielietoti TDS aprēķinam, ja izvēles rūtiņa **Ignorēt slieksni** TDS nodokļu kodiem ir atzīmēta darījumam pievienotajā TDS grupā.</span><span class="sxs-lookup"><span data-stu-id="9352e-123">The threshold limit and exception threshold limit are not considered for the TDS calculation if the **Overlook threshold** check box is selected for TDS tax codes in the TDS group that is attached to the transaction.</span></span> <span data-ttu-id="9352e-124">Sliekšņa ierobežojums netiks izmantots TDS nodokļu kodiem TDS grupā, kurai paredzēta izvēles rūtiņa **Ignorēt slieksni**.</span><span class="sxs-lookup"><span data-stu-id="9352e-124">The threshold limit won't be used in the TDS tax codes in the TDS group that the **Overlook threshold** check box is for.</span></span>

<span data-ttu-id="9352e-125">Ja noteiktai TDS grupai dažiem rēķiniem ir atzīmēta izvēles rūtiņa **Ignorēt slieksni**, taču nav atlasīta citiem rēķiniem, kas tika izveidoti noteiktam kreditoram/debitoram, TDS aprēķins, neņemot vērā sliekšņa ierobežojumu dažiem rēķiniem, iespējams, tiks ņemta vērā visu to rēķinu kopējā summa, kuriem TDS nav aprēķināts iepriekš.</span><span class="sxs-lookup"><span data-stu-id="9352e-125">If the **Overlook threshold** check box is selected for a specific TDS group for some invoices, but not selected for other invoices that were created for a specific vendor/customer, the calculation of TDS without overlooking the threshold limit for few invoices may take place considering the cumulative amount on all invoices on which TDS hasn't been calculated earlier.</span></span>

<span data-ttu-id="9352e-126">Piemēram, sliekšņa ierobežojums ir 25 000.</span><span class="sxs-lookup"><span data-stu-id="9352e-126">For example, the threshold limit is 25000.</span></span> <span data-ttu-id="9352e-127">Kreditoram A tiek izveidoti šādi rēķini.</span><span class="sxs-lookup"><span data-stu-id="9352e-127">The following invoices are created for Vendor A.</span></span>

- <span data-ttu-id="9352e-128">1. rēķins – 20 000 – (izvēles rūtiņa **Ignorēt slieksni** nav atzīmēta): TDS netiek aprēķināts.</span><span class="sxs-lookup"><span data-stu-id="9352e-128">Invoice 1 – 2,0000 – (**Overlook threshold** check box is not selected): TDS is not calculated.</span></span>

- <span data-ttu-id="9352e-129">2. rēķins – 4000 – (izvēles rūtiņa **Ignorēt slieksni** ir atzīmēta): TDS tiek aprēķināts uz summu 4000.</span><span class="sxs-lookup"><span data-stu-id="9352e-129">Invoice 2 – 4,000 – (**Overlook threshold** check box is selected): TDS is calculated on 4,000.</span></span>

- <span data-ttu-id="9352e-130">2. rēķins – 3000 – (izvēles rūtiņa **Ignorēt slieksni** nav atzīmēta): TDS tiek aprēķināts kopējai rēķina summai, t.i., 27 000 (20000+4000+3000), kas pārsniedz sliekšņa ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="9352e-130">Invoice 2 – 3,000 – (**Overlook threshold** check box is not selected): TDS is calculated as the cumulative invoice amount, that is, 27,000 (20000+4000+3000) exceeded the threshold limit.</span></span> <span data-ttu-id="9352e-131">TDS tiek aprēķināts, pamatojoties uz to rēķinu kopējo summu, kuriem TDS nav aprēķināts iepriekš, t.i., 23 000 (20 000+3000).</span><span class="sxs-lookup"><span data-stu-id="9352e-131">TDS is calculated on the cumulative amount of invoices on which the TDS has not been calculated earlier, that is, 23,000 (20000+3000).</span></span>