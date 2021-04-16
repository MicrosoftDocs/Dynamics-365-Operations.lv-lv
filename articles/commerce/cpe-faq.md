---
title: Bieži uzdotie jautājumi par Dynamics 365 Commerce novērtējuma vidi
description: Šajā tēmā sniegtas atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Commerce novērtēšanas vidi.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e42618a522f5ad551f608605300c30b5ffb8e299
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795935"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="8313f-103">Dynamics 365 Commerce novērtēšanas vides BUJ</span><span class="sxs-lookup"><span data-stu-id="8313f-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8313f-104">Šajā tēmā sniegtas atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Commerce novērtēšanas vidi.</span><span class="sxs-lookup"><span data-stu-id="8313f-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="8313f-105">**Vai mēs varam izmantot Commerce novērtējuma vidi kā e-komercijas vitrīnu klientiem, kas pašlaik ievieš mazumtirdzniecību?**</span><span class="sxs-lookup"><span data-stu-id="8313f-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="8313f-106">Nr.p.k.</span><span class="sxs-lookup"><span data-stu-id="8313f-106">No.</span></span> <span data-ttu-id="8313f-107">Commerce novērtējuma vide ir paredzēta tikai novērtēšanai.</span><span class="sxs-lookup"><span data-stu-id="8313f-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="8313f-108">Ja jums ir nepieciešama vide, kurā tiek ieviesta mazumtirdzniecība, sazinieties ar Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8313f-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="8313f-109">**Vai Commerce novērtējuma vidi var izmantot, lai nodrošinātu e-komercijas funkcijas papildu esošajam pieteikumam/videi, kas ievieš mazumtirdzniecību?**</span><span class="sxs-lookup"><span data-stu-id="8313f-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="8313f-110">Nē (galvenokārt).</span><span class="sxs-lookup"><span data-stu-id="8313f-110">No (mostly).</span></span> <span data-ttu-id="8313f-111">Commerce novērtēšanas komponenti ir pieejami tikai vidēm, kas atbilst konfigurācijām, kas norādītas priekšnosacījumos un nodrošināšanas ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="8313f-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="8313f-112">Turklāt nepieciešamie bāzes demonstrācijas dati nebūs pieejami vidēs, kas tika izvietotas ar sākotnējo laidienu, kas ir agrāks par 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="8313f-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="8313f-113">**Kādas izmaksas ir saistītas ar Commerce novērtējuma vides izvietošanu pakalpojumā Microsoft Azure, izmantojot Microsoft Dynamics Lifecycle Services (LCS)?**</span><span class="sxs-lookup"><span data-stu-id="8313f-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="8313f-114">Tradicionālā Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce Headquarters demonstrācijas vide (virtuālā mašīna \[VM\]) tiks viesota jūsu Azure abonementā.</span><span class="sxs-lookup"><span data-stu-id="8313f-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="8313f-115">Lai novērtētu šīs izmaksas, varat izmantot [Azure cenu kalkulatoru](https://azure.microsoft.com/pricing/calculator/).</span><span class="sxs-lookup"><span data-stu-id="8313f-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="8313f-116">Citi komponenti, piemēram, Commerce Scale Unit, Commerce vietņu veidotājs un jūsu e-komercijas vietne būs pieejama kā programmatūras pakalpojums (SaaS) un tiks viesoti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8313f-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="8313f-117">**Kuras Azure ģeogrāfiskās īpašības pašlaik tiek atbalstītas Commerce novērtējuma videi?**</span><span class="sxs-lookup"><span data-stu-id="8313f-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="8313f-118">Commerce novērtējuma vidi var izvietot tikai Ziemeļamerikā.</span><span class="sxs-lookup"><span data-stu-id="8313f-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="8313f-119">**Vai ir lejupielādējams virtuāls cietais disks (VHD), kurā ir pilnīga OneBox virtuālās mašīnas (VM) opcija?**</span><span class="sxs-lookup"><span data-stu-id="8313f-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="8313f-120">Dynamics 365 Commerce un Commerce Scale Unit ir pilnīgi programmatūras pakalpojumi (SaaS), un tiem ir jābūt viesotiem mākonī.</span><span class="sxs-lookup"><span data-stu-id="8313f-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="8313f-121">**Cik ilgi var izmantot Commerce novērtējuma vidi?**</span><span class="sxs-lookup"><span data-stu-id="8313f-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="8313f-122">Commerce novērtējuma videi ir 30 dienu laika ierobežojums no datuma, kad tiek nodrošināti SaaS komponenti, piemēram, Commerce Scale Unit, Commerce vietņu veidotājs un jūsu e-komercijas vietne.</span><span class="sxs-lookup"><span data-stu-id="8313f-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="8313f-123">**Vai es varu pagarināt laika ierobežojumu savai Commerce novērtējuma videi?**</span><span class="sxs-lookup"><span data-stu-id="8313f-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="8313f-124">Laika ierobežojuma pagarināšana ir normas izņēmums un tiek apsvērti katrā gadījumā atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="8313f-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="8313f-125">Lai saņemtu palīdzību, sazinieties ar Microsoft partnera kontaktpersonu.</span><span class="sxs-lookup"><span data-stu-id="8313f-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8313f-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8313f-126">Additional resources</span></span>

[<span data-ttu-id="8313f-127">Dynamics 365 Commerce novērtējuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="8313f-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="8313f-128">Nodrošināt Dynamics 365 Commerce novērtējuma vidi</span><span class="sxs-lookup"><span data-stu-id="8313f-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="8313f-129">Konfigurēt Dynamics 365 Commerce novērtējuma vidi</span><span class="sxs-lookup"><span data-stu-id="8313f-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="8313f-130">BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="8313f-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="8313f-131">Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="8313f-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]