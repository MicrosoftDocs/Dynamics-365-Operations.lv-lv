---
title: Dynamics 365 Commerce novērtēšanas vides pārskats
description: Šajā tēmā sniegts Microsoft Dynamics 365 Commerce novērtējuma vides pārskats.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cc6bffba6ee402c6b48d6a3c8f8356eb32b5423b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478024"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="e7e5a-103">Dynamics 365 Commerce novērtēšanas vides pārskats</span><span class="sxs-lookup"><span data-stu-id="e7e5a-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7e5a-104">Šajā tēmā sniegts Microsoft Dynamics 365 Commerce novērtējuma vides pārskats.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="e7e5a-105">Commerce novērtējuma vides nav vispārpieejamas, un tās tiek piešķirtas partneriem un klientiem pēc pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="e7e5a-106">Lai iegūtu plašāku informāciju, sazinieties ar sava Microsoft partnera kontaktpersonu.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="e7e5a-107">Commerce novērtējuma vide ir vispārīga Dynamics 365 Commerce vide pēc izvēles, kas ļauj partneriem un potenciālajiem klientiem izmēģināt Commerce preci.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="e7e5a-108">Novērtējuma vides ir daļēji iepriekš konfigurētas, lai samazinātu nepieciešamās pēc nodrošināšanas darbības.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="e7e5a-109">Neņemot vērā dažus nelielus ierobežojumus, kas neietekmē līdzekļus vai funkcionalitāti, Commerce novērtējuma vide nodrošina pilnīgu Commerce pieredzi, un to var izmantot klienti un ieviešanas partneri, lai novērtētu preci, sniegtu atsauksmes un veiktu atbilstību analīzi.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="e7e5a-110">Commerce novērtējuma vides ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="e7e5a-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="e7e5a-111">Lai gan Commerce novērtējuma vide nodrošina pilnu Commerce līdzekļu un funkcionalitātes komplektu, ir daži nelieli ierobežojumi:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="e7e5a-112">Lai gan pašai Commerce novērtējuma videi nav ģeogrāfisku ierobežojumu, vides komponenti, piemēram, Retail Cloud Scale Unit (RSCU) un e-komercijas lietojumprogrammas, ir nodrošināmas tikai Amerikas Savienotajās valstīs.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="e7e5a-113">Commerce novērtējuma vides izmantošana ir ierobežota līdz 30 dienām no datuma, kad tiek nodrošināta e-komercija.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="e7e5a-114">Commerce novērtējuma vidi var veiksmīgi izvietot un inicializēt tikai vidē, kas izmanto izmēģinājuma topoloģiju, kur visi vides komponenti tiek izvietoti vienā mākonī viesotā virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="e7e5a-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="e7e5a-115">Galvenais ierobežojums šajā topoloģijā ir to vienlaicīgo lietotāju skaits, kuru novērtējuma vide var atbalstīt.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="e7e5a-116">Sākt darbu</span><span class="sxs-lookup"><span data-stu-id="e7e5a-116">Get started</span></span>

<span data-ttu-id="e7e5a-117">Lai varētu nodrošināt Commerce novērtējuma vidi, skatiet sadaļu [Commerce novērtējuma vides nodrošināšana](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="e7e5a-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7e5a-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e7e5a-118">Additional resources</span></span>

[<span data-ttu-id="e7e5a-119">Nodrošināt Dynamics 365 Commerce novērtējuma vidi</span><span class="sxs-lookup"><span data-stu-id="e7e5a-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="e7e5a-120">Konfigurēt Dynamics 365 Commerce novērtējuma vidi</span><span class="sxs-lookup"><span data-stu-id="e7e5a-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="e7e5a-121">BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="e7e5a-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="e7e5a-122">Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="e7e5a-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="e7e5a-123">Dynamics 365 Commerce novērtējuma vide - bieži uzdotie jautājumi</span><span class="sxs-lookup"><span data-stu-id="e7e5a-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
