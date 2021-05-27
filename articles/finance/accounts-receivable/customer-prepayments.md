---
title: Debitora priekšapmaksas
description: Šajā tēmā skaidrots, kā iestatīt un apstrādāt debitoru priekšapmaksas (ko sauc arī par debitoru depozītiem).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019424"
---
# <a name="customer-prepayments"></a><span data-ttu-id="25228-103">Debitora priekšapmaksas</span><span class="sxs-lookup"><span data-stu-id="25228-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25228-104">Debitoru priekšapmaksas tiek izmantotas, kad saņemat maksājumu no debitora, bet nav rēķina, ar kuru maksājumu var nosegt.</span><span class="sxs-lookup"><span data-stu-id="25228-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="25228-105">Šie maksājumu veidi tiek saukti arī par debitoru depozītiem.</span><span class="sxs-lookup"><span data-stu-id="25228-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="25228-106">Debitoru priekšapmaksu iestatīšanas un darba process sastāv no šādiem pamata soļiem.</span><span class="sxs-lookup"><span data-stu-id="25228-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="25228-107">Izveidojiet debitoru grāmatošanas metodi priekšapmaksām.</span><span class="sxs-lookup"><span data-stu-id="25228-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="25228-108">Iestatiet parametru **Grāmatošanas profils priekšapmaksas žurnāla dokumenta summā**.</span><span class="sxs-lookup"><span data-stu-id="25228-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="25228-109">Izveidojiet debitoru maksājumu žurnālu un atzīmējiet izvēles rūtiņu **Priekšapmaksas žurnāla dokuments** katrā rindā.</span><span class="sxs-lookup"><span data-stu-id="25228-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="25228-110">Grāmatojiet debitoru maksājumu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="25228-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="25228-111">Pēc rēķina ģenerēšanas nosedziet priekšapmaksu ar to, izmantojot lapu **Nosegt atvērtos darījumus**.</span><span class="sxs-lookup"><span data-stu-id="25228-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="25228-112">Izveidojiet debitoru grāmatošanas metodi priekšapmaksām</span><span class="sxs-lookup"><span data-stu-id="25228-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="25228-113">Parasti, kad pieņemat priekšapmaksas vai depozītus no saviem debitoriem pirms preču vai pakalpojumu piegādes, vai pirms rēķins eksistē jūsu sistēmā, jūs vēlaties reģistrēt skaidru naudu kā saistības nevis kā līdzekļus jūsu kontu plānā.</span><span class="sxs-lookup"><span data-stu-id="25228-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="25228-114">Tomēr šo summu ierakstīšanas prasības jūsu virsgrāmatā var atšķirties atkarībā no valsts vai reģiona.</span><span class="sxs-lookup"><span data-stu-id="25228-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="25228-115">Tāpēc noteikti konsultējieties ar saviem grāmatvežiem par visiem spēkā esošajiem vietējiem likumiem.</span><span class="sxs-lookup"><span data-stu-id="25228-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="25228-116">Parasti grāmatošanas metodes izveides process, ko var izmantot priekšapmaksām, ir tāds pats process kā citu grāmatošanas metožu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="25228-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="25228-117">Galvenā starpība ir galvenais konts, kas atlasīts laukā **Summu konts**.</span><span class="sxs-lookup"><span data-stu-id="25228-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="25228-118">Plašāku informāciju skatiet šeit: [Debitoru grāmatošanas profili](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="25228-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="25228-119">Definēt debitoru priekšapmaksu parametrus</span><span class="sxs-lookup"><span data-stu-id="25228-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="25228-120">Pastāv divi galvenie debitoru parādu parametri, kas jāņem vērā, konfigurējot sistēmu debitoru priekšapmaksām.</span><span class="sxs-lookup"><span data-stu-id="25228-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="25228-121">Veiciet tālāk norādītās darbības, lai konfigurētu parametrus.</span><span class="sxs-lookup"><span data-stu-id="25228-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="25228-122">Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="25228-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="25228-123">Nav obligāti: cilnē **Virsgrāmata un PVN**, kopsavilkuma cilnē **Maksājums** iestatiet **Priekšapmaksas žurnāla dokumenta summas PVN** opciju uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="25228-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="25228-124">Laukā **Grāmatošanas metode ar priekšapmaksas žurnāla dokumentu** atlasiet debitora grāmatošanas metodi, ko izmantot, grāmatojot debitoru priekšapmaksas.</span><span class="sxs-lookup"><span data-stu-id="25228-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="25228-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="25228-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="25228-126">Izveidot debitoru priekšapmaksas dokumentus</span><span class="sxs-lookup"><span data-stu-id="25228-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="25228-127">Veidojot debitoru maksājumu žurnālu, katrai priekšapmaksai jums jāiestata **Priekšapmaksas žurnāla dokumenta** opcija uz **Jā** lapā **Debitoru maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="25228-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="25228-128">Izpildiet tālāk aprakstītās darbības, lai izveidotu debitoru priekšapmaksu.</span><span class="sxs-lookup"><span data-stu-id="25228-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="25228-129">Dodieties uz **Debitori \> Maksājumi \> Debitora maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="25228-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="25228-130">Atlasiet **Jauns**, lai izveidotu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="25228-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="25228-131">Laukā **Nosaukums** atlasiet izmantojamo žurnāla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="25228-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="25228-132">Ja iepriekšējās procedūras ietvaros iestatāt **Priekšapmaksas žurnāla dokumenta summas PVN** opciju uz **Jā**, ir jāatlasa žurnāla nosaukums, kurā ir atlasīts parametrs **Summa iekļauj PVN**.</span><span class="sxs-lookup"><span data-stu-id="25228-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="25228-133">pēc izvēles: Laukā **Apraksts** ievadiet detalizētu aprakstu.</span><span class="sxs-lookup"><span data-stu-id="25228-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="25228-134">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="25228-134">Select **Lines**.</span></span>
6. <span data-ttu-id="25228-135">Ja tukša rinda nepastāv, atlasiet **Jauns**, lai izveidotu rindu.</span><span class="sxs-lookup"><span data-stu-id="25228-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="25228-136">Laukā **Datums** ievadiet datumu, kad ir jāgrāmato priekšapmaksa.</span><span class="sxs-lookup"><span data-stu-id="25228-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="25228-137">Laukā **Uzņēmums** atlasiet klientu priekšapmaksai.</span><span class="sxs-lookup"><span data-stu-id="25228-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="25228-138">Pēc izvēles: laukā **Apraksts** ievadiet detalizētu darījuma aprakstu.</span><span class="sxs-lookup"><span data-stu-id="25228-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="25228-139">Laukā **Kredīts** ievadiet priekšapmaksas summu.</span><span class="sxs-lookup"><span data-stu-id="25228-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="25228-140">Laukā **Korespondējošā konts** atlasiet kontu, uz kuru veikt priekšapmaksu.</span><span class="sxs-lookup"><span data-stu-id="25228-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="25228-141">Piemēram, atlasiet banku vai galveno kontu, kurā grāmatot maksājumu.</span><span class="sxs-lookup"><span data-stu-id="25228-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="25228-142">Laukā **Maksāšanas veids** atlasiet debitora maksāšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="25228-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="25228-143">Cilnē **Maksājums** iestatiet **Priekšapmaksas žurnāla dokumenta** opciju uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="25228-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="25228-144">Atkārtojiet no 7. līdz 13. solim katrai papildu priekšapmaksai, kas ir jāiegrāmato.</span><span class="sxs-lookup"><span data-stu-id="25228-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="25228-145">Atlasiet **Grāmatot**, lai pabeigtu žurnāla gatavošanu.</span><span class="sxs-lookup"><span data-stu-id="25228-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="25228-146">Priekšapmaksas nosedziet ar rēķiniem</span><span class="sxs-lookup"><span data-stu-id="25228-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="25228-147">Varat izmantot **Debitoru maksājumu** darbvietu, lai viegli atrastu un apmaksātu maksājumus, kas nav pilnībā nosegti.</span><span class="sxs-lookup"><span data-stu-id="25228-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="25228-148">**Sākuma** informācijas panelī atlasiet elementu **Debitoru maksājumi**.</span><span class="sxs-lookup"><span data-stu-id="25228-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="25228-149">Sadaļas **Debitora darījumi** cilnē **Nenosegtie maksājumi** meklējiet un atlasiet sedzamo maksājumu.</span><span class="sxs-lookup"><span data-stu-id="25228-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="25228-150">Atlasiet **Segt darījumus**.</span><span class="sxs-lookup"><span data-stu-id="25228-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="25228-151">Atlasiet izvēles rūtiņu **Atzīmēt** rēķinam un maksājumam, kas tiks segts.</span><span class="sxs-lookup"><span data-stu-id="25228-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="25228-152">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="25228-152">Select **Post**.</span></span>

<span data-ttu-id="25228-153">Papildinformāciju par to, kā nosegt atvērtos darījumus, skatiet sadaļā [Norēķinu pārskats](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="25228-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
