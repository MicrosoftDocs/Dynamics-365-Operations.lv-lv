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
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c396060017db6d7ce830b350f242d3097876e50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012317"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="7ac80-103">Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas</span><span class="sxs-lookup"><span data-stu-id="7ac80-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="7ac80-104">Šajā tēmā izskaidrots, kā varat ļaut klientiem atteikties no tīmekļa aktivitāšu notikumu kolekcijas Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7ac80-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7ac80-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="7ac80-105">Overview</span></span>

<span data-ttu-id="7ac80-106">Dynamics 365 Commerce ļauj vietņu administratoriem analizēt lietotāju tīmekļa aktivitātes viņu e-komercijas vietnēs.</span><span class="sxs-lookup"><span data-stu-id="7ac80-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="7ac80-107">Tādā veidā viņi var labāk izprast, kā tiek izmantotas viņu vietnes, un viņi var optimizēt vietnes, lai nodrošinātu labāku lietotāja pieredzi un atbilstību biznesa mērķiem.</span><span class="sxs-lookup"><span data-stu-id="7ac80-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="7ac80-108">Veidi, kā administratoriem ieviest atteikšanās iespēju</span><span class="sxs-lookup"><span data-stu-id="7ac80-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="7ac80-109">Administratoriem ir trīs veidi, kādos ieviest atteikšanās iespēju.</span><span class="sxs-lookup"><span data-stu-id="7ac80-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="7ac80-110">Atteikšanās lietotāju vārdā</span><span class="sxs-lookup"><span data-stu-id="7ac80-110">Opt out on behalf of users</span></span>

<span data-ttu-id="7ac80-111">Kontu pārvaldībā Commerce Headquarters (HQ) administratori var atteikties lietotāju vārdā.</span><span class="sxs-lookup"><span data-stu-id="7ac80-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="7ac80-112">HQ klientā, lapā **Visi debitori** meklējiet un atlasiet debitoru.</span><span class="sxs-lookup"><span data-stu-id="7ac80-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="7ac80-113">Lapā Informācija par klientu, kopsavilkuma cilnes **Retail** sadaļā **Privātums** iestatiet opciju **Neizsekot tīmekļa aktivitātes** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7ac80-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Konfidencialitātes iestatījumi](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="7ac80-115">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="7ac80-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="7ac80-116">Modulī balstīta atteikšanās iespēja</span><span class="sxs-lookup"><span data-stu-id="7ac80-116">Module-based opt-out experience</span></span>

<span data-ttu-id="7ac80-117">Administratori var ļaut autentificētajiem lietotājiem pašiem atteikties no tīmekļa aktivitāšu notikumu apkopošanas.</span><span class="sxs-lookup"><span data-stu-id="7ac80-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="7ac80-118">Lai nodrošinātu šo atteikšanās iespēju, pievienojiet lietotāja atteikšanās moduli klienta konta profila lapām.</span><span class="sxs-lookup"><span data-stu-id="7ac80-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="7ac80-119">Pielāgoti paplašinājumi</span><span class="sxs-lookup"><span data-stu-id="7ac80-119">Custom extensions</span></span>

<span data-ttu-id="7ac80-120">Administratori var izveidot savus paplašinājumus, lai pārvaldītu lietotāju atteikšanās pieredzi.</span><span class="sxs-lookup"><span data-stu-id="7ac80-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="7ac80-121">Papildinformāciju skatiet šeit [Retail Server API izsaukšana](e-commerce-extensibility/call-retail-server-apis.md) un [Tiešsaistes kanāla paplašināšana](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="7ac80-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
