---
title: Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas
description: Šajā tēmā skaidrots, kā varat ļaut vietnes apmeklētājiem atteikties no tīmekļa aktivitāšu notikumu kolekcijas programmā Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 8058db089b8768076ff1250be77d42a6e2b3f570
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378996"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="954bb-103">Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas</span><span class="sxs-lookup"><span data-stu-id="954bb-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="954bb-104">Šajā tēmā izskaidrots, kā varat ļaut klientiem atteikties no tīmekļa aktivitāšu notikumu kolekcijas Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="954bb-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="954bb-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="954bb-105">Overview</span></span>

<span data-ttu-id="954bb-106">Dynamics 365 Commerce ļauj vietņu administratoriem analizēt lietotāju tīmekļa aktivitātes viņu e-komercijas vietnēs.</span><span class="sxs-lookup"><span data-stu-id="954bb-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="954bb-107">Tādā veidā viņi var labāk izprast, kā tiek izmantotas viņu vietnes, un viņi var optimizēt vietnes, lai nodrošinātu labāku lietotāja pieredzi un atbilstību biznesa mērķiem.</span><span class="sxs-lookup"><span data-stu-id="954bb-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="954bb-108">Veidi, kā administratoriem ieviest atteikšanās iespēju</span><span class="sxs-lookup"><span data-stu-id="954bb-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="954bb-109">Administratoriem ir trīs veidi, kādos ieviest atteikšanās iespēju.</span><span class="sxs-lookup"><span data-stu-id="954bb-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="954bb-110">Atteikšanās lietotāju vārdā</span><span class="sxs-lookup"><span data-stu-id="954bb-110">Opt out on behalf of users</span></span>

<span data-ttu-id="954bb-111">Kontu pārvaldībā Commerce Headquarters (HQ) administratori var atteikties lietotāju vārdā.</span><span class="sxs-lookup"><span data-stu-id="954bb-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="954bb-112">HQ klientā, lapā **Visi debitori** meklējiet un atlasiet debitoru.</span><span class="sxs-lookup"><span data-stu-id="954bb-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="954bb-113">Lapā Informācija par klientu, kopsavilkuma cilnes **Retail** sadaļā **Privātums** iestatiet opciju **Neizsekot tīmekļa aktivitātes** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="954bb-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Konfidencialitātes iestatījumi](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="954bb-115">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="954bb-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="954bb-116">Modulī balstīta atteikšanās iespēja</span><span class="sxs-lookup"><span data-stu-id="954bb-116">Module-based opt-out experience</span></span>

<span data-ttu-id="954bb-117">Administratori var ļaut autentificētajiem lietotājiem pašiem atteikties no tīmekļa aktivitāšu notikumu apkopošanas.</span><span class="sxs-lookup"><span data-stu-id="954bb-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="954bb-118">Lai nodrošinātu šo atteikšanās iespēju, pievienojiet lietotāja atteikšanās moduli klienta konta profila lapām.</span><span class="sxs-lookup"><span data-stu-id="954bb-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="954bb-119">Pielāgoti paplašinājumi</span><span class="sxs-lookup"><span data-stu-id="954bb-119">Custom extensions</span></span>

<span data-ttu-id="954bb-120">Administratori var izveidot savus paplašinājumus, lai pārvaldītu lietotāju atteikšanās pieredzi.</span><span class="sxs-lookup"><span data-stu-id="954bb-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="954bb-121">Papildinformāciju skatiet šeit [Retail Server API izsaukšana](e-commerce-extensibility/call-retail-server-apis.md) un [Tiešsaistes kanāla paplašināšana](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="954bb-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
