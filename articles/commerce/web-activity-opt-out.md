---
title: Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas
description: Šajā tēmā skaidrots, kā varat ļaut vietnes apmeklētājiem atteikties no tīmekļa aktivitāšu notikumu kolekcijas programmā Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791561"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="917c9-103">Atteikšanās no tīmekļa aktivitāšu notikumu apkopošanas</span><span class="sxs-lookup"><span data-stu-id="917c9-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="917c9-104">Šajā tēmā izskaidrots, kā varat ļaut klientiem atteikties no tīmekļa aktivitāšu notikumu kolekcijas programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="917c9-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="917c9-105">Dynamics 365 Commerce ļauj vietņu administratoriem analizēt lietotāju tīmekļa aktivitātes viņu e-komercijas vietnēs.</span><span class="sxs-lookup"><span data-stu-id="917c9-105">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="917c9-106">Tādā veidā viņi var labāk izprast, kā tiek izmantotas viņu vietnes, un viņi var optimizēt vietnes, lai nodrošinātu labāku lietotāja pieredzi un atbilstību biznesa mērķiem.</span><span class="sxs-lookup"><span data-stu-id="917c9-106">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="917c9-107">Veidi, kā administratoriem ieviest atteikšanās iespēju</span><span class="sxs-lookup"><span data-stu-id="917c9-107">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="917c9-108">Administratoriem ir trīs veidi, kādos ieviest atteikšanās iespēju.</span><span class="sxs-lookup"><span data-stu-id="917c9-108">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="917c9-109">Atteikšanās lietotāju vārdā</span><span class="sxs-lookup"><span data-stu-id="917c9-109">Opt out on behalf of users</span></span>

<span data-ttu-id="917c9-110">Kontu pārvaldībā Commerce Headquarters (HQ) administratori var atteikties lietotāju vārdā.</span><span class="sxs-lookup"><span data-stu-id="917c9-110">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="917c9-111">HQ klientā, lapā **Visi debitori** meklējiet un atlasiet debitoru.</span><span class="sxs-lookup"><span data-stu-id="917c9-111">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="917c9-112">Lapā Informācija par klientu, kopsavilkuma cilnes **Retail** sadaļā **Privātums** iestatiet opciju **Neizsekot tīmekļa aktivitātes** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="917c9-112">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Konfidencialitātes iestatījumi](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="917c9-114">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="917c9-114">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="917c9-115">Modulī balstīta atteikšanās iespēja</span><span class="sxs-lookup"><span data-stu-id="917c9-115">Module-based opt-out experience</span></span>

<span data-ttu-id="917c9-116">Administratori var ļaut autentificētajiem lietotājiem pašiem atteikties no tīmekļa aktivitāšu notikumu apkopošanas.</span><span class="sxs-lookup"><span data-stu-id="917c9-116">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="917c9-117">Lai nodrošinātu šo atteikšanās iespēju, pievienojiet lietotāja atteikšanās moduli klienta konta profila lapām.</span><span class="sxs-lookup"><span data-stu-id="917c9-117">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="917c9-118">Pielāgoti paplašinājumi</span><span class="sxs-lookup"><span data-stu-id="917c9-118">Custom extensions</span></span>

<span data-ttu-id="917c9-119">Administratori var izveidot savus paplašinājumus, lai pārvaldītu lietotāju atteikšanās pieredzi.</span><span class="sxs-lookup"><span data-stu-id="917c9-119">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="917c9-120">Papildinformāciju skatiet šeit [Retail Server API izsaukšana](e-commerce-extensibility/call-retail-server-apis.md) un [Tiešsaistes kanāla paplašināšana](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="917c9-120">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
