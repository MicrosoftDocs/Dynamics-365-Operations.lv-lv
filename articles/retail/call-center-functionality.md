---
title: "Zvanu centra pārdošanas funkcionalitāte"
description: "Šajā tēmā ir sniegts pārskats par zvanu centra pārdošanas funkcionalitāti programmā Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 8b78762ce70b318e1f77e1e49ffaa7b72f01667f
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="call-center-sales-functionality"></a><span data-ttu-id="2a63b-103">Zvanu centra pārdošanas funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="2a63b-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a63b-104">Pakalpojumā Dynamics 365 for Retail zvanu centrs ir Retail kanāla veids, ko var norādīt programmā.</span><span class="sxs-lookup"><span data-stu-id="2a63b-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="2a63b-105">Norādot noteiktu kanālu savām zvanu centra struktūrvienībām, sistēma var saistīt noteiktus datu noklusējumus un pasūtījumu apstrādes noklusējumus ar pārdošanas pasūtījumiem, ko izveidojis zvanu centra kanāla lietotājs.</span><span class="sxs-lookup"><span data-stu-id="2a63b-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="2a63b-106">Zvanu centra funkcijas ietver īpašas mazumtirdzniecības cenas, piedāvājumus, katalogus, dāvanu kartes, lojalitātes programmas un kuponus.</span><span class="sxs-lookup"><span data-stu-id="2a63b-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="2a63b-107">Zvanu centra pasūtījumus papildina pārdošanas punkta programma, lai atbalstītu šķērskanālu pasūtījuma izpildes scenārijus.</span><span class="sxs-lookup"><span data-stu-id="2a63b-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="2a63b-108">Jāņem vērā, ka, lai arī zvanu centra modulis var tikt izmantots arī citās nozarēs ārpus mazumtirdzniecības, pašreizējais Dynamics 365 for Retail zvanu centra programmas laidiens nav optimizēts izmantošanai starpuzņēmumu (B2B) pasūtījumu apstrādes scenārijiem vai scenārijiem, kur pasūtījumiem ir liels pārdošanas rindu skaits.</span><span class="sxs-lookup"><span data-stu-id="2a63b-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="2a63b-109">Iesakām lietotājiem, kas vēlas izmantot zvanu centra funkcijas pasūtījumu apstrādei ārpus tipiskas tiešo darījumu ar patērētājiem apstrādes, pietiekami ilgi pārbaudīt un pārliecināties, ka zvanu centra funkcionalitātes iespējošana atbilst funkcionālajām un veiktspējas vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="2a63b-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="2a63b-110">Papildus atbalstam pasūtījumu izveidei zvanu centra modulis nodrošina arī lietotājam draudzīgu klientu pakalpojumu programmu, kas ļauj lietotājiem vieglāk atrast klientu kontus un pārskatīt visus saistītos klienta pasūtījumu datus un atribūtus.</span><span class="sxs-lookup"><span data-stu-id="2a63b-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="2a63b-111">Klientu apkalpošanas ekrāns ir izstrādāts, lai ļautu lietotājam ātri piekļūtu ar pasūtījumu saistītajiem datiem, kas ļaus atbildēt uz visbiežākajiem ar pasūtījumiem saistītiem jautājumiem, kas saņemti no klientiem.</span><span class="sxs-lookup"><span data-stu-id="2a63b-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="2a63b-112">Šī lapa sniedz saites uz atbilstošo dokumentāciju, kas saistīti ar zvanu centra līdzekļu iestatīšanu, konfigurēšanu un lietošanu pakalpojumā Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="2a63b-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="2a63b-113">Zvanu centra konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-113">Configure the call center</span></span>

[<span data-ttu-id="2a63b-114">Iestatīt pasūtījumu apstrādes opcijas</span><span class="sxs-lookup"><span data-stu-id="2a63b-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="2a63b-115">Pasūtījumu apstrādes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-115">Configure order processing</span></span>

[<span data-ttu-id="2a63b-116">Pārkāpumu brīdinājumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-116">Set up fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="2a63b-117">Manuāla pasūtījumu aizturēšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-117">Manual Order Holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="2a63b-118">Maksājumu apstrādes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-118">Configure payment processing</span></span>

[<span data-ttu-id="2a63b-119">Maksāšanas metodes zvanu centrā</span><span class="sxs-lookup"><span data-stu-id="2a63b-119">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="2a63b-120">Piegādes režīmu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-120">Configure delivery modes</span></span>

[<span data-ttu-id="2a63b-121">Zvanu centra piegādes veidu un maksu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="2a63b-122">Tiešā mārketinga konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-122">Configure direct marketing</span></span>

[<span data-ttu-id="2a63b-123">Zvanu centra katalogi</span><span class="sxs-lookup"><span data-stu-id="2a63b-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="2a63b-124">RFM analīzes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-124">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="2a63b-125">Nepārtrauktības programmu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="2a63b-125">Configure continuity programs</span></span>

[<span data-ttu-id="2a63b-126">Nepārtrauktības programmas iestatīšana zvanu centram</span><span class="sxs-lookup"><span data-stu-id="2a63b-126">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)

