---
title: Abonementa darbplūsmas apskats
description: Šajā tēmā ir sniegts apskats par abonementa darbplūsmu.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f023ddd8d6f9350702f687763b53b057baa9aed8
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985819"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="fe4d7-103">Abonementa darbplūsmas apskats</span><span class="sxs-lookup"><span data-stu-id="fe4d7-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fe4d7-104">Jūs esat abonementa administrators apgaismojuma uzņēmumā, kurš piedāvā abonementu apgaismojuma ierīču apkopei.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="fe4d7-105">Klients sazinās ar jūsu uzņēmumu, lai iegādātos gada abonementu apgaismojuma ierīču apkopei.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="fe4d7-106">Abonementu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="fe4d7-106">Setting up subscriptions</span></span>

<span data-ttu-id="fe4d7-107">Lai iestatītu abonementu, vispirms jums ir jāizveido abonementu grupa jaunajam pakalpojumu līgumam vai ir jāapstiprina, ka šāda abonementu grupa jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="fe4d7-108">Ja abonementu grupa jau pastāv, jums tā ir jāiestata, lai klientam reizi gadā tiktu izrakstīts rēķins un lai pārdošanas ieņēmumus uzkrātu par katru gada mēnesi.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="fe4d7-109">Plašāku informāciju par to, kā iestatīt abonementus, skatiet tēmā [Abonementu grupu iestatīšana](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="fe4d7-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="fe4d7-110">Kad abonementu grupa ir izveidota, varat izveidot abonementu.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="fe4d7-111">Plašāku informāciju par to, kā izveidot pakalpojumu abonementus, skatiet tēmā [Pakalpojumu abonementu izveidošana no abonementu grupas](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="fe4d7-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="fe4d7-112">Abonementu transakciju izveidošana un modificēšana</span><span class="sxs-lookup"><span data-stu-id="fe4d7-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="fe4d7-113">Pēc abonementa iestatīšanas varat izveidot abonēšanas maksas transakciju pirmajam rēķina periodam, kas ir viens gads.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="fe4d7-114">Transakciju veids ir **Regulārs**.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="fe4d7-115">Tādēļ varat izveidot tikai tādas abonementu transakcijas, kur datums No un datums Līdz atbilst periodiem, kurus iepriekš izveidojāt formā **Periodu veidi**.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="fe4d7-116">Plašāku informāciju par maksas transakcijām skatiet tēmā [Abonēšanas maksas transakciju izveidošana](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="fe4d7-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="fe4d7-117">Kad savam klientam esat iestatījis abonementu, jūs atceraties, ka esat vienojies par 10 procentu atlaidi visām pakalpojumu piedāvājumu cenu sistēmā iestatītajām cenām.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="fe4d7-118">Tādēļ jums ir jāsamazina izveidotās transakcijas maksas cena.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="fe4d7-119">Vēlāk tajā pašā dienā jūsu klienta kontaktpersona jums zvana, lai pastāstītu, ka, lai gan viņi joprojām vēlas noslēgt līgumu par apgaismojuma ierīču apkopi, tajā pašā gadā viņi vēlāk plāno ieviest jaunas apgaismojuma ierīces.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="fe4d7-120">Tādēļ apkopes segums viņiem ir nepieciešams tikai līdz 2013. gada oktobrim.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="fe4d7-121">Lai samazinātu klienta abonementa mēnešu skaitu, jūs izveidojat jaunu abonēšanas maksas transakciju ar veidu **Dienu skaita samazināšana**.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="fe4d7-122">Plašāku informāciju par dienu skaita samazināšanu skatiet tēmā [Abonēšanas maksu dienu skaita samazināšana](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="fe4d7-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="fe4d7-123">Rēķinu izrakstīšana un uzkrāšana saistība ar abonementu transakcijām</span><span class="sxs-lookup"><span data-stu-id="fe4d7-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="fe4d7-124">Tagad jūs esat pabeidzis abonementa iestatīšanu un varat klientam par to izrakstīt rēķinu.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="fe4d7-125">Plašāku informāciju par to, kā izrakstīt rēķinu par abonementiem, skatiet tēmā [Abonementu transakciju rēķinu izrakstīšana](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="fe4d7-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="fe4d7-126">Pēc divām dienām klients zvana, lai paziņotu, ka rēķins par abonementu ir jāizraksta ASV dolāros, nevis eiro.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="fe4d7-127">Tādēļ jūs izveidojat kredīta notu, un jūs izveidojat arī jaunu abonementa transakciju ar pareizo valūtu.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="fe4d7-128">Plašāku informāciju par to, kā kreditēt abonementu transakcijas, skatiet tēmā [Abonementu transakciju kreditēšana](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="fe4d7-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="fe4d7-129">Katra mēneša beigās viena mēneša ienākumus no debitora abonementa var uzkrāt uz peļņas un zaudējumu kontu un NP kontiem.</span><span class="sxs-lookup"><span data-stu-id="fe4d7-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="fe4d7-130">Plašāku informāciju par to, kā uzkrāt ieņēmumus abonementiem, skatiet tēmā [Abonementu ieņēmumu uzkrāšana](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="fe4d7-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  


