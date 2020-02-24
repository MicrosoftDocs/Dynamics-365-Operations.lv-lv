---
title: Kanālu iestatīšanas priekšnosacījumi
description: Šajā tēmā sniegts pārskats par kanālu iestatīšanas priekšnosacījumiem programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002293"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="30164-103">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="30164-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="30164-104">Šajā tēmā sniegts pārskats par kanāla iestatīšanas priekšnosacījumiem programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="30164-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="30164-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="30164-105">Overview</span></span>

<span data-ttu-id="30164-106">Lai varētu programmā Dynamics 365 Commerce izveidot kanālu, ir jāizpilda vairāki priekšnosacījumu uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="30164-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="30164-107">Šādi priekšnosacījumu uzdevumu saraksti ir organizēti pēc kanāla veida.</span><span class="sxs-lookup"><span data-stu-id="30164-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="30164-108">Daži dokumenti joprojām tiek ierakstīti, un saites tiks atjauninātas, kad tiek publicēts jauns saturs.</span><span class="sxs-lookup"><span data-stu-id="30164-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="30164-109">Inicializēšana</span><span class="sxs-lookup"><span data-stu-id="30164-109">Initialization</span></span>

- [<span data-ttu-id="30164-110">Inicializēt sākumdatus</span><span class="sxs-lookup"><span data-stu-id="30164-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="30164-111">Visi kanālu veidiem nepieciešami globālie priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="30164-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="30164-112">Definēt un konfigurēt juridisko personu struktūru</span><span class="sxs-lookup"><span data-stu-id="30164-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="30164-113">Konfigurēt savas organizāciju hierarhijas</span><span class="sxs-lookup"><span data-stu-id="30164-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="30164-114">Noliktavas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="30164-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="30164-115">Konfigurēt PVN</span><span class="sxs-lookup"><span data-stu-id="30164-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="30164-116">E-pasta paziņojumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="30164-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="30164-117">Numuru sēriju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="30164-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="30164-118">Noklusējuma debitora un adrešu grāmatas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="30164-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="30164-119">Mazumtirdzniecības kanāla priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="30164-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="30164-120">Informācijas kodi un informācijas kodu grupas</span><span class="sxs-lookup"><span data-stu-id="30164-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="30164-121">Iestatīt mazumtirdzniecības funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="30164-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="30164-122">Darbinieku adrešu grāmatas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="30164-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="30164-123">Iestatīt ekrāna izkārtojumu</span><span class="sxs-lookup"><span data-stu-id="30164-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="30164-124">Iestatīt aparatūras staciju</span><span class="sxs-lookup"><span data-stu-id="30164-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="30164-125">Zvanu centra kanāla priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="30164-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="30164-126">Zvanu centra parametri</span><span class="sxs-lookup"><span data-stu-id="30164-126">Call center parameters</span></span>
- <span data-ttu-id="30164-127">Zvanu centra atmaksas metodes</span><span class="sxs-lookup"><span data-stu-id="30164-127">Call center refund methods</span></span>
- <span data-ttu-id="30164-128">Nomas tipi</span><span class="sxs-lookup"><span data-stu-id="30164-128">Rental types</span></span>
- <span data-ttu-id="30164-129">Maksājumu pakalpojumi</span><span class="sxs-lookup"><span data-stu-id="30164-129">Payment services</span></span>
- <span data-ttu-id="30164-130">Pasūtījumu aizturēšanas kodi</span><span class="sxs-lookup"><span data-stu-id="30164-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="30164-131">Tiešsaistes kanāla priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="30164-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="30164-132">Izveidot tiešsaistes funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="30164-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="30164-133">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="30164-133">Additional resources</span></span>

[<span data-ttu-id="30164-134">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="30164-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="30164-135">Organizācijas un organizāciju hierarhiju pārskats</span><span class="sxs-lookup"><span data-stu-id="30164-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="30164-136">Iestatīt organizāciju hierarhijas</span><span class="sxs-lookup"><span data-stu-id="30164-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="30164-137">Izveidot juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="30164-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="30164-138">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="30164-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="30164-139">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="30164-139">Set up an online channel</span></span>](channel-setup-online.md)
