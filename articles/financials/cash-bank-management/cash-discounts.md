---
title: Termiņatlaides
description: Termiņatlaides tiek iestatītas un koplietotas moduļiem Parādi kreditoriem un Debitoru parādi.  Pieejamo termiņatlaidi var definēt debitora rēķinā vai kreditora rēķinā, un tā tiek izmantota, ja rēķins tiek apmaksāts termiņatlaides datumu diapazonā.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd15a021244e55ea988a95184a758a321ebeafb3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561619"
---
# <a name="cash-discounts"></a><span data-ttu-id="53528-104">Termiņatlaides</span><span class="sxs-lookup"><span data-stu-id="53528-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53528-105">Termiņatlaides tiek iestatītas un koplietotas moduļiem Parādi kreditoriem un Debitoru parādi.</span><span class="sxs-lookup"><span data-stu-id="53528-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="53528-106">Pieejamo termiņatlaidi var definēt debitora rēķinā vai kreditora rēķinā, un tā tiek izmantota, ja rēķins tiek apmaksāts termiņatlaides datumu diapazonā.</span><span class="sxs-lookup"><span data-stu-id="53528-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="53528-107">Termiņatlaides</span><span class="sxs-lookup"><span data-stu-id="53528-107">Cash discounts</span></span>

<span data-ttu-id="53528-108">Gan debitoriem, gan kreditoriem termiņatlaides var izveidot lapā Termiņatlaides.</span><span class="sxs-lookup"><span data-stu-id="53528-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="53528-109">Izmantojot lauku Nākamais atlaižu kods, varat arī norādīt sēriju ar termiņatlaidēm, kas seko viena otrai, beidzoties iepriekšējās termiņatlaides datumiem.</span><span class="sxs-lookup"><span data-stu-id="53528-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="53528-110">Plašāku informāciju skatiet tālāk šajā tēmā, sadaļā “Piemērs. Termiņatlaižu sērijas”.</span><span class="sxs-lookup"><span data-stu-id="53528-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="53528-111">Ja rēķins, kredīta transakcija (maksājums vai kredīta nota) vai tie abi tiek ievadīti valūtā, kas nav juridiskās personas uzskaites valūta, tad termiņatlaide tiek aprēķināta, izmantojot valūtas maiņas kursu, kurš ir balstīts uz maksājuma vai kredīta notas datumu.</span><span class="sxs-lookup"><span data-stu-id="53528-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="53528-112">Ja rēķins un kredīta dokuments tiek ievadīti dažādās juridiskajās personās un ja uzskaites valūtas šīm juridiskajām personām atšķiras, tad valūtas maiņas kurss tiek ņemts no rēķina juridiskās personas attiecīgā kredīta dokumenta datumā.</span><span class="sxs-lookup"><span data-stu-id="53528-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="53528-113">Plašāku informāciju skatiet tālāk šajā tēmā, sadaļā “Piemērs. Valūtas maiņas kursi termiņatlaidēm”.</span><span class="sxs-lookup"><span data-stu-id="53528-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="53528-114">Termiņatlaides galvenā konta pasūtījuma noklusējuma secība</span><span class="sxs-lookup"><span data-stu-id="53528-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="53528-115">Ja rēķins ir segts laikā, lai saņemtu termiņatlaidi, šī termiņatlaide tiek automātiski grāmatota uz termiņatlaides galveno kontu atbilstoši šādai noklusējuma prioritātei:</span><span class="sxs-lookup"><span data-stu-id="53528-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="53528-116">Galvenais konts, kas norādīts laukā Alternatīvais termiņatlaides konts debitora lapā Nosegt atvērtās transakcijas vai kreditora lapā Nosegt atvērtās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="53528-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="53528-117">Galvenais konts, kas ir norādīts laukā Debitora termiņatlaide vai laukā Kreditora termiņatlaide tajā virsgrāmatas grāmatošanas grupā, kas ir piešķirta rēķina pārdošanas nodokļa kodam.</span><span class="sxs-lookup"><span data-stu-id="53528-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="53528-118">Iestatiet virsgrāmatas grāmatošanas grupas lapā Virsgrāmatas grāmatošanas grupas un piešķiriet tās pārdošanas nodokļa kodiem lapā Pārdošanas nodokļa kodi.</span><span class="sxs-lookup"><span data-stu-id="53528-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="53528-119">Galvenais grāmatošanas konts lapā Termiņatlaides laukā Galvenais konts debitoru atlaidēm vai lapā Galvenais konts kreditoru atlaidēm attiecībā uz termiņatlaides kodu, kas ir norādīts nosegtajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="53528-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="53528-120">Galvenais konts termiņatlaidēm, kā definēts lapā Automātisko transakciju konti.</span><span class="sxs-lookup"><span data-stu-id="53528-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="53528-121">Piemērs. Termiņatlaižu sērijas</span><span class="sxs-lookup"><span data-stu-id="53528-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="53528-122">Iestatiet trīs termiņatlaižu kodus šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="53528-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="53528-123">Kods 5D10% – 10% termiņatlaide, ja summa tiek samaksāta 5 dienu laikā.</span><span class="sxs-lookup"><span data-stu-id="53528-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="53528-124">Kods 10D5% – 5% termiņatlaide, ja summa tiek samaksāta 10 dienu laikā.</span><span class="sxs-lookup"><span data-stu-id="53528-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="53528-125">Kods 14D2% – 2% termiņatlaide, ja summa tiek samaksāta 14 dienu laikā.</span><span class="sxs-lookup"><span data-stu-id="53528-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="53528-126">Laukā Nākamais atlaižu kods:</span><span class="sxs-lookup"><span data-stu-id="53528-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="53528-127">Kodam 5D10% atlasiet 10D5%</span><span class="sxs-lookup"><span data-stu-id="53528-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="53528-128">Kodam 10D5% atlasiet 14D2%.</span><span class="sxs-lookup"><span data-stu-id="53528-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="53528-129">Kodam 14D2% lauku Nākamais atlaižu kods atstājiet tukšu.</span><span class="sxs-lookup"><span data-stu-id="53528-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="53528-130">Maksājuma datumam pārsniedzot iepriekšējo rēķinā norādītās termiņatlaides datumu, šīs trīs termiņatlaides seko cita citai.</span><span class="sxs-lookup"><span data-stu-id="53528-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="53528-131">Apmaksājot rēķinu, tiek piešķirta tikai viena termiņatlaide, pamatojoties uz to, kurš termiņatlaides datums šajā termiņatlaižu secībā tiek ievērots.</span><span class="sxs-lookup"><span data-stu-id="53528-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="53528-132">Piemērs. Valūtas maiņas kursi termiņatlaidēm</span><span class="sxs-lookup"><span data-stu-id="53528-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="53528-133">Jūsu juridiskās personas uzskaites valūta ir EUR, un šāds valūtas maiņas kurss ir norādīts attiecībā uz USD:</span><span class="sxs-lookup"><span data-stu-id="53528-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="53528-134">1. februāris = 110</span><span class="sxs-lookup"><span data-stu-id="53528-134">February 1 = 110</span></span>
-   <span data-ttu-id="53528-135">1. marts = 80</span><span class="sxs-lookup"><span data-stu-id="53528-135">March 1 = 80</span></span>

<span data-ttu-id="53528-136">Rēķins par 1000 USD ar termiņatlaides nosacījumiem 20D2% tiek grāmatots 15. februārī.</span><span class="sxs-lookup"><span data-stu-id="53528-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="53528-137">Rēķina summa uzskaites valūtā ir 1100 EUR.</span><span class="sxs-lookup"><span data-stu-id="53528-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="53528-138">Maksājums par 980 USD šim rēķinam tiek nosegts 1. martā.</span><span class="sxs-lookup"><span data-stu-id="53528-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="53528-139">Termiņatlaides summa ir 20 USD.</span><span class="sxs-lookup"><span data-stu-id="53528-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="53528-140">Maksājuma summa uzskaites valūtā ir 784 EUR.</span><span class="sxs-lookup"><span data-stu-id="53528-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="53528-141">Termiņatlaides uzskaites valūtas summa tiek aprēķināta, izmantojot valūtas maiņas kursu no 1. marta: 20 \* 80 / 100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="53528-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="53528-142">Ja lapā Debitoru moduļa parametri vai Kreditoru moduļa parametri ir atlasīta opcija Aprēķināt termiņatlaides daļējiem maksājumiem, tiek izmantots valūtas maiņas kurss, kas ir spēkā katra daļējā maksājuma datumā.</span><span class="sxs-lookup"><span data-stu-id="53528-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 

