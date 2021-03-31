---
title: Zvanu centra pārdošanas funkcionalitāte
description: Šajā tēmā ir sniegts apskats par zvanu centra pārdošanas funkcionalitāti programmā Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d3bdba4ac29f5e5b49af02110eb976f154327a43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213214"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="3977a-103">Zvanu centra pārdošanas funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="3977a-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="3977a-104">Programmā Dynamics 365 Commerce zvanu centrs ir Commerce kanāla veids, ko var definēt lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="3977a-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="3977a-105">Norādot noteiktu kanālu savām zvanu centra struktūrvienībām, sistēma var saistīt noteiktus datu noklusējumus un pasūtījumu apstrādes noklusējumus ar pārdošanas pasūtījumiem, ko izveidojis zvanu centra kanāla lietotājs.</span><span class="sxs-lookup"><span data-stu-id="3977a-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="3977a-106">Zvanu centra funkcijas ietver īpašas cenas, piedāvājumus, katalogus, dāvanu kartes, lojalitātes programmas un kuponus.</span><span class="sxs-lookup"><span data-stu-id="3977a-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="3977a-107">Zvanu centra pasūtījumus papildina pārdošanas punkta programma, lai atbalstītu šķērskanālu pasūtījuma izpildes scenārijus.</span><span class="sxs-lookup"><span data-stu-id="3977a-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="3977a-108">Ir svarīgi ņemt vērā, ka, lai arī zvanu centra moduli var izmantot arī citās nozarēs, ne tikai Commerce, pašreizējais zvanu centra lietojumprogrammas laidiens nav optimizēts izmantošanai starpuzņēmumu (B2B) pasūtījumu apstrādes scenārijiem vai scenārijiem, kuros pasūtījumiem ir liels pārdošanas rindu skaits.</span><span class="sxs-lookup"><span data-stu-id="3977a-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large number of sales lines.</span></span> <span data-ttu-id="3977a-109">Iesakām lietotājiem, kas vēlas izmantot zvanu centra funkcijas pasūtījumu apstrādei ārpus tipiskas tiešo darījumu ar patērētājiem apstrādes, pietiekami ilgi pārbaudīt un pārliecināties, ka zvanu centra funkcionalitātes iespējošana atbilst funkcionālajām un veiktspējas vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="3977a-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="3977a-110">Papildus atbalstam pasūtījumu izveidei zvanu centra modulis nodrošina arī lietotājam draudzīgu klientu pakalpojumu programmu, kas ļauj lietotājiem vieglāk atrast klientu kontus un pārskatīt visus saistītos klienta pasūtījumu datus un atribūtus.</span><span class="sxs-lookup"><span data-stu-id="3977a-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="3977a-111">Klientu apkalpošanas ekrāns ir izstrādāts, lai ļautu lietotājam ātri piekļūtu ar pasūtījumu saistītajiem datiem, kas ļaus atbildēt uz visbiežākajiem ar pasūtījumiem saistītiem jautājumiem, kas saņemti no klientiem.</span><span class="sxs-lookup"><span data-stu-id="3977a-111">The customer service screen is designed to enable a user to quickly access order-related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="3977a-112">Šajā lapā ir sniegtas saites uz atbilstošo dokumentāciju, kas ir saistīta ar zvanu centra līdzekļu iestatīšanu, konfigurēšanu un funkcionālo lietošanu.</span><span class="sxs-lookup"><span data-stu-id="3977a-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="3977a-113">Zvanu centra konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3977a-113">Configure the call center</span></span>

[<span data-ttu-id="3977a-114">Zvanu centra kanālu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3977a-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="3977a-115">Pasūtījumu apstrādes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3977a-115">Configure order processing</span></span>

[<span data-ttu-id="3977a-116">Zvanu centra pārkāpumu brīdinājumu iestatīšana un darbs ar tiem</span><span class="sxs-lookup"><span data-stu-id="3977a-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="3977a-117">Zvanu centra pasūtījumu aizturēšanas konfigurēšana un darbs ar to</span><span class="sxs-lookup"><span data-stu-id="3977a-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="3977a-118">Maksājumu apstrādes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3977a-118">Configure payment processing</span></span>

[<span data-ttu-id="3977a-119">Maksāšanas metodes zvanu centros</span><span class="sxs-lookup"><span data-stu-id="3977a-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="3977a-120">Piegādes režīmu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3977a-120">Configure delivery modes</span></span>

[<span data-ttu-id="3977a-121">Zvanu centra piegādes veidu un maksu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3977a-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="3977a-122">Tiešā mārketinga konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3977a-122">Configure direct marketing</span></span>

[<span data-ttu-id="3977a-123">Zvanu centra katalogi</span><span class="sxs-lookup"><span data-stu-id="3977a-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="3977a-124">Nesenības, biežuma un monetārās (RFM) analīzes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3977a-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="3977a-125">Nepārtrauktības programmu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3977a-125">Configure continuity programs</span></span>

[<span data-ttu-id="3977a-126">Nepārtrauktības programmu iestatīšana zvanu centriem</span><span class="sxs-lookup"><span data-stu-id="3977a-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]