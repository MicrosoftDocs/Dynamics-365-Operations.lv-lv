---
title: Vērtējumu un atsauksmju apskats
description: Šajā tēmā apskatīti vērtējumi un apskati programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0788091755fb784621e972a0573f7004952e8e11
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792103"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="5b868-103">Vērtējumu un atsauksmju apskats</span><span class="sxs-lookup"><span data-stu-id="5b868-103">Ratings and reviews overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5b868-104">Šajā tēmā apskatīti vērtējumi un apskati programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5b868-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5b868-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="5b868-105">Overview</span></span>

<span data-ttu-id="5b868-106">Vērtējumi un apskati ir izšķiroši e-tirdzniecības klientiem, kuri vēlas uzzināt, kā citi klienti uztver preci.</span><span class="sxs-lookup"><span data-stu-id="5b868-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="5b868-107">Tie var arī palīdzēt patērētājiem pieņemt lēmumu veikt pirkumu.</span><span class="sxs-lookup"><span data-stu-id="5b868-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="5b868-108">Dynamics 365 Commerce vērtējumu un apskatu risinājums ļauj mazumtirgotājiem iegūt no klientiem preču vērtējumus un apskatus.</span><span class="sxs-lookup"><span data-stu-id="5b868-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="5b868-109">Pēc tam mazumtirgotāji savā e-tirdzniecības tīmekļa vietnē var parādīt vidējo vērtējumu un apskatu informāciju.</span><span class="sxs-lookup"><span data-stu-id="5b868-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="5b868-110">Vidējā vērtējuma informācija tiek parādīta pārdošanas punktā (POS) un zvanu centra kanālos.</span><span class="sxs-lookup"><span data-stu-id="5b868-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="5b868-111">Tāpēc pārdošanas partneri to var izmantot, lai palīdzētu lietotājiem pieņemt lēmumus.</span><span class="sxs-lookup"><span data-stu-id="5b868-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="5b868-112">Vērtējumi un apskati var kalpot arī kā atgriezeniskās saites mehānisms, ko mazumtirgotāji var izmantot, lai uzlabotu preces kvalitāti un tādējādi palielinātu pārdošanas apjomu.</span><span class="sxs-lookup"><span data-stu-id="5b868-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="5b868-113">Vērtējumu un apskatu funkcionalitāte Dynamics 365 Commerce ir daudzkanālu risinājums, un tas ir dabiski pieejams kā platformas daļa.</span><span class="sxs-lookup"><span data-stu-id="5b868-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="5b868-114">Vērtējumu un apskatu risinājums ir izveidots pa virsu Microsoft Azure, kas nodrošina augstu mērogojamību un uzticamību.</span><span class="sxs-lookup"><span data-stu-id="5b868-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="5b868-115">Tālāk redzamajā attēlā ir parādīts, kā Dynamics 365 Commerce darbojas vērtējumu un apskatu risinājums.</span><span class="sxs-lookup"><span data-stu-id="5b868-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![Vērtējumi un atsauksmes Dynamics 365 for Commerce](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="5b868-117">Vērtējumu un apskatu risinājums Dynamics 365 Commerce izmanto Azure Cognitive Services, lai piedāvātu automātisku necenzētu vārdu moderēšanu 40 valodās.</span><span class="sxs-lookup"><span data-stu-id="5b868-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="5b868-118">Tā kā nav nepieciešams cilvēka apstiprinājums, tiek samazinātas moderēšanas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="5b868-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="5b868-119">Sistēma piedāvā arī moderatora rīkus, ko var izmantot, lai atbildētu uz klientu bažām, atsauksmēm un noņemšanas pieprasījumiem, kā arī apstrādātu datu pieprasījumus no klientiem.</span><span class="sxs-lookup"><span data-stu-id="5b868-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="5b868-120">Vērtējumu un apskatu risinājums nodrošina logrīkus, kas parāda vērtējumu kopsavilkumus preču sarakstos, meklēšanas rezultātos, lapā preces detalizētas informācijas lapā un citās vietās.</span><span class="sxs-lookup"><span data-stu-id="5b868-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="5b868-121">Logrīki parāda pabeigtus apskatu sarakstus, un tie sniedz arī kārtošanas un filtrēšanas opcijas.</span><span class="sxs-lookup"><span data-stu-id="5b868-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="5b868-122">Vērtējumu un apskatu risinājums nodrošina arī biznesa informācijas (BI) veidni, kas ietver rādītāju kopu, lai sniegtu ieskatu vērtējumos un apskatos.</span><span class="sxs-lookup"><span data-stu-id="5b868-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="5b868-123">Vērtējumu un apskatu datus var eksportēt tālākai analīzei.</span><span class="sxs-lookup"><span data-stu-id="5b868-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b868-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5b868-124">Additional resources</span></span>

[<span data-ttu-id="5b868-125">Piekrišana izmantot vērtējumus un atsauksmes</span><span class="sxs-lookup"><span data-stu-id="5b868-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="5b868-126">Vērtējumu un atsauksmju pārvaldība</span><span class="sxs-lookup"><span data-stu-id="5b868-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="5b868-127">Vērtējumu un atsauksmju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5b868-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="5b868-128">Preču vērtējumu sinhronizācija Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5b868-128">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]