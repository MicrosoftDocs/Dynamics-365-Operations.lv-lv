---
title: Dynamics 365 Commerce priekšskatījuma vides pārskats
description: Šajā tēmā ir sniegts pārskats par programmas Microsoft Dynamics 365 Commerce priekšskatījuma vidi.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024687"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a><span data-ttu-id="9b1fa-103">Dynamics 365 Commerce priekšskatījuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="9b1fa-103">Dynamics 365 Commerce preview environment overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9b1fa-104">Šajā tēmā ir sniegts pārskats par programmas Microsoft Dynamics 365 Commerce priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="9b1fa-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="9b1fa-105">Overview</span></span>

<span data-ttu-id="9b1fa-106">Commerce priekšskatījuma vide ir vispārīga Dynamics 365 Commerce vide pēc izvēles, kas ļauj potenciālajiem klientiem izmēģināt Commerce preci pirms tās vispārējās laišanas publiskā tirdzniecībā.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="9b1fa-107">Neņemot vērā dažus nelielus ierobežojumus, kas neietekmē līdzekļus vai funkcionalitāti, Commerce priekšskatījuma vide nodrošina pilnīgu Commerce pieredzi, un to var izmantot klienti un ieviešanas partneri, lai novērtētu preci, sniegtu atsauksmes un veiktu atbilstību analīzi.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="9b1fa-108">Commerce priekšskatījuma vides ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="9b1fa-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="9b1fa-109">Lai gan Commerce priekšskatījuma vide nodrošina pilnu Commerce līdzekļu un funkcionalitātes komplektu, ir daži nelieli ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="9b1fa-110">Lai gan pašai Commerce priekšskatījuma videi nav ģeogrāfisku ierobežojumu, vides komponenti, piemēram, Retail Cloud Scale Unit (RSCU) un e-Commerce lietojumprogrammas, var tikt nodrošināti tikai Amerikas Savienotajās valstīs.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="9b1fa-111">Commerce priekšskatījuma vides izmantošana ir ierobežota līdz 30 dienām no dienas, kad tiek nodrošināta e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="9b1fa-112">Commerce priekšskatījuma vidi var veiksmīgi izvietot un inicializēt tikai vidē, kas izmanto izmēģinājuma topoloģiju, kur visi vides komponenti tiek izvietoti vienā virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="9b1fa-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="9b1fa-113">Galvenais ierobežojums šajā OneBox VM topoloģijā ir to vienlaicīgo lietotāju skaits, kuru priekšskatījuma vide var atbalstīt.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="9b1fa-114">Commerce priekšskatījuma vidi var novērtēt tikai līdz Commerce preces vispārējai pieejamībai (GA).</span><span class="sxs-lookup"><span data-stu-id="9b1fa-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="9b1fa-115">Jaunas izmēģinājuma vides būs pieejamas pēc GA.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="9b1fa-116">Sākt darbu</span><span class="sxs-lookup"><span data-stu-id="9b1fa-116">Get started</span></span>

<span data-ttu-id="9b1fa-117">Lai varētu nodrošināt Commerce priekšskatījuma vidi, skatiet sadaļu [Commerce priekšskatījuma vides nodrošināšana ](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="9b1fa-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b1fa-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9b1fa-118">Additional resources</span></span>

[<span data-ttu-id="9b1fa-119">Dynamics 365 Commerce priekšskatījuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="9b1fa-119">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="9b1fa-120">Dynamics 365 Commerce priekšskatījuma vides konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9b1fa-120">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="9b1fa-121">Izvēles funkciju konfigurēšana Dynamics 365 Commerce priekšskatījuma videi</span><span class="sxs-lookup"><span data-stu-id="9b1fa-121">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="9b1fa-122">Dynamics 365 Commerce priekšskatījuma vides BUJ</span><span class="sxs-lookup"><span data-stu-id="9b1fa-122">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)
