---
title: Abonementu uzkrāšana
description: Ar pakalpojumu abonementu, periodos, kas seko maksājuma darbības rēķina izrakstīšanas datumam, jūs manuāli uzkrājat ieņēmumus.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27908e2852f3f28264f83e0118eb4be79c9e03bc
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742290"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="4724a-103">Abonementu uzkrāšana</span><span class="sxs-lookup"><span data-stu-id="4724a-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4724a-104">Ar pakalpojumu abonementu, periodos, kas seko maksājuma darbības rēķina izrakstīšanas datumam, jūs manuāli uzkrājat ieņēmumus.</span><span class="sxs-lookup"><span data-stu-id="4724a-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="4724a-105">Uzkrājumu periodi tiek izveidoti rēķina periodam, ko jūs iestatāt abonementa maksājumam, uzkrājumu periodi ir balstīti uz abonementa perioda kodu.</span><span class="sxs-lookup"><span data-stu-id="4724a-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="4724a-106">Jūs varat uzkrāt un atcelt uzkrāto ieņēmumu.</span><span class="sxs-lookup"><span data-stu-id="4724a-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="4724a-107">Kredīta summu uzkrājumu reversēšana</span><span class="sxs-lookup"><span data-stu-id="4724a-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="4724a-108">Ja kreditējat rēķinos ierakstītos abonementu apjomus, jūs varat izmantot divas metodes uzkrāto apjomu reversēšanai.</span><span class="sxs-lookup"><span data-stu-id="4724a-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="4724a-109">Varat reversēt katru uzkrāto ienākumu darījumu individuāli, pirms izveidojat kredīta notas piedāvājumu darījumam.</span><span class="sxs-lookup"><span data-stu-id="4724a-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="4724a-110">Šī ir manuālā metode.</span><span class="sxs-lookup"><span data-stu-id="4724a-110">This is the manual method.</span></span> <span data-ttu-id="4724a-111">(manuāli)</span><span class="sxs-lookup"><span data-stu-id="4724a-111">(manual)</span></span>

  - <span data-ttu-id="4724a-112">Jūs varat reversēt visus uzkrātos apjomus kredīta notas iegrāmatošanas datumā vai uzkrājuma iegrāmatošanas datumā.</span><span class="sxs-lookup"><span data-stu-id="4724a-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="4724a-113">Vairāk informācijas var atrast [Abonēšanas parametri (veidlapa)](https://technet.microsoft.com/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="4724a-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="4724a-114">Uzstādīšanas prasības</span><span class="sxs-lookup"><span data-stu-id="4724a-114">Setup requirements</span></span>

<span data-ttu-id="4724a-115">Lai uzkrātu ieņēmumus, pārliecinieties, vai šīs datu prasības ir ievērotas.</span><span class="sxs-lookup"><span data-stu-id="4724a-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="4724a-116">Konta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4724a-116">Account setup</span></span>

<span data-ttu-id="4724a-117">**NP - abonements** un **Uzkrātie ieņēmumi - abonements** kontiem ir jābūt iestatītiem modulī **Projekts**.</span><span class="sxs-lookup"><span data-stu-id="4724a-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="4724a-118">Iegrāmatojot uzkrāto ieņēmumu, konts **NP - abonements** tiek debitēts ar uzkrāto apjomu, bet konts **Uzkrātie ieņēmumi - abonements** tiek kreditēts ar uzkrāto apjomu.</span><span class="sxs-lookup"><span data-stu-id="4724a-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="4724a-119">Iestatīt kontus abonementa ieņēmumu uzkrāšanai</span><span class="sxs-lookup"><span data-stu-id="4724a-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="4724a-120">Noklikšķiniet uz **Projektu vadība un uzskaite** \> **Iestatījumi** \> **Grāmatošana** \> **Virsgrāmatas grāmatojumu iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="4724a-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="4724a-121">Noklikšķiniet uz cilnes **Ieņēmumu konti** cilnes un atlasiet **NP - abonements** vai **Uzkrātie ieņēmumi - abonements**, lai iestatītu kontus.</span><span class="sxs-lookup"><span data-stu-id="4724a-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="4724a-122">Abonementa grupas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4724a-122">Subscription group setup</span></span>

<span data-ttu-id="4724a-123">Lai varētu uzkrāt ieņēmumus abonementiem, jābūt atzīmētai izvēles rūtiņai **Uzkrāt ieņēmumus**.</span><span class="sxs-lookup"><span data-stu-id="4724a-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="4724a-124">Tā ir atrodama veidlapā **Abonementu grupas** grupai, kas piesaistīta abonementam.</span><span class="sxs-lookup"><span data-stu-id="4724a-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="4724a-125">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu abonementi** \> **Abonementu grupas**.</span><span class="sxs-lookup"><span data-stu-id="4724a-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="4724a-126">Iespējot ieņēmumu uzkrāšanu abonementa grupai</span><span class="sxs-lookup"><span data-stu-id="4724a-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="4724a-127">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatīšana** \> **Pakalpojumu abonementi** \> **Abonementu grupas**.</span><span class="sxs-lookup"><span data-stu-id="4724a-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="4724a-128">Periodi</span><span class="sxs-lookup"><span data-stu-id="4724a-128">Periods</span></span>

<span data-ttu-id="4724a-129">Jums ir jāiestata rēķina izrakstīšanas perioda kods.</span><span class="sxs-lookup"><span data-stu-id="4724a-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="4724a-130">Ja vien nevēlaties uzkrāt ieņēmumus ar tiem pašiem laika intervāliem, kas tiek izmantoti rēķinu izrakstīšanā, jums ir jāiestata arī uzkrāšanas periods.</span><span class="sxs-lookup"><span data-stu-id="4724a-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="4724a-131">Šajā tabulā ir pārskats par uzkrāšanas periodiem, ko varat iestatīt katram rēķinu izrakstīšanas periodam.</span><span class="sxs-lookup"><span data-stu-id="4724a-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4724a-132">Maksāšanas termiņš</span><span class="sxs-lookup"><span data-stu-id="4724a-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="4724a-133">Uzkrāšanas periods</span><span class="sxs-lookup"><span data-stu-id="4724a-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4724a-134"><strong>Gadi</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4724a-135"><strong>Gadi</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="4724a-136"><strong>Ceturksnis</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="4724a-137"><strong>mēnesis;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="4724a-138"><strong>diena;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4724a-139"><strong>Ceturksnis</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4724a-140"><strong>Ceturksnis</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="4724a-141"><strong>mēnesis;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="4724a-142"><strong>diena;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4724a-143"><strong>mēnesis;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4724a-144"><strong>mēnesis;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="4724a-145"><strong>diena;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4724a-146"><strong>Nedēļa</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4724a-147"><strong>diena;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4724a-148"><strong>diena;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="4724a-149"><strong>diena;</strong></span><span class="sxs-lookup"><span data-stu-id="4724a-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4724a-150">Rēķina perioda iestatīšana ir obligāta daļa no abonementu grupas vispārīgajiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="4724a-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="4724a-151">Varat izlemt, vai arī iestatīt uzkrāšanas periodu abonementu grupai.</span><span class="sxs-lookup"><span data-stu-id="4724a-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="4724a-152">Ja iestatāt uzkrāšanas periodu abonementu grupai, šis periods tiks norādīts laukā **Perioda kods**.</span><span class="sxs-lookup"><span data-stu-id="4724a-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="4724a-153">Šis lauks ir veidlapā **Uzkrāt abonementu ieņēmumus**, ja jūs uzkrājat abonementu ieņēmumus.</span><span class="sxs-lookup"><span data-stu-id="4724a-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="4724a-154">Tomēr uzkrāšanas periods ir papildu informācija par abonementa grupu.</span><span class="sxs-lookup"><span data-stu-id="4724a-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4724a-155">Izmantojiet šādu ceļu, lai atvērtu veidlapu <STRONG>Uzkrāt abonementu ieņēmumus</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="4724a-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="4724a-156">Noklikšķiniet uz <STRONG>Pakalpojumu pārvaldība</STRONG> &gt; <STRONG>Periodiski</STRONG> &gt; <STRONG>Pakalpojumu abonementi</STRONG> &gt; <STRONG>Uzkrāt abonementu ieņēmumus</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="4724a-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="4724a-157">Darbības</span><span class="sxs-lookup"><span data-stu-id="4724a-157">Transactions</span></span>

<span data-ttu-id="4724a-158">Jūs varat kontrolēt virsgrāmatas darījumu skaitu, kas tiek izveidoti, grāmatojot uzkrāto ieņēmumu.</span><span class="sxs-lookup"><span data-stu-id="4724a-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="4724a-159">Abonementiem nosakiet, vai virsgrāmatas darījumi jāveido kā kopums vai pa rindām.</span><span class="sxs-lookup"><span data-stu-id="4724a-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="4724a-160">Norādiet grāmatošanas detaļu līmeni, ko rādīt uzkrātajām darbībām</span><span class="sxs-lookup"><span data-stu-id="4724a-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="4724a-161">Noklikšķiniet uz **Projektu vadība un uzskaite** \> **Iestatīšana** \> **Projektu vadības un uzskaites parametri**.</span><span class="sxs-lookup"><span data-stu-id="4724a-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="4724a-162">Cilnē **Finanses** laukā **Rēķins** atlasiet **Kopā** vai **Rinda**.</span><span class="sxs-lookup"><span data-stu-id="4724a-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="4724a-163">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="4724a-163">See also</span></span>

[<span data-ttu-id="4724a-164">Uzkrāt abonementa ieņēmumus</span><span class="sxs-lookup"><span data-stu-id="4724a-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


