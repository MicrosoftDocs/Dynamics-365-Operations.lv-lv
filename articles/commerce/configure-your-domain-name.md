---
title: Domēna nosaukuma konfigurēšana
description: Šajā tēmā paskaidrots, kā konfigurēt domēna nosaukumu Microsoft Dynamics365 e-komercijas vietnei.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f73c034563fb1cc6b05091b4c47e2a788d1a8b6
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945540"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="f5cda-103">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="f5cda-103">Configure your domain name</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f5cda-104">Šajā tēmā paskaidrots, kā konfigurēt domēna nosaukumu Microsoft Dynamics365 e-komercijas vietnei.</span><span class="sxs-lookup"><span data-stu-id="f5cda-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="f5cda-105">Domēnu pievienošana E-komercijas inicializēšanas laikā</span><span class="sxs-lookup"><span data-stu-id="f5cda-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="f5cda-106">Lai saistītu domēnus ar savu e-komercijas vidi, inicializējiet E-komerciju, kā aprakstīts tēmā [Jaunas E-komercijas vietnes izvietošana](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="f5cda-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="f5cda-107">Inicializēšanas laikā jums tiek lūgts sniegt informāciju, kas tiks izmantota jūsu E-komercijas vides nodrošināšanai.</span><span class="sxs-lookup"><span data-stu-id="f5cda-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="f5cda-108">Laukā **Atbalstītie resursdatora nosaukumi** pievienojiet visus domēnus, kurus plānojat izmantot šajā vidē.</span><span class="sxs-lookup"><span data-stu-id="f5cda-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="f5cda-109">Vairāki domēni jāatdala ar semikolu.</span><span class="sxs-lookup"><span data-stu-id="f5cda-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="f5cda-110">Šādā veidā domēni tiek konfigurēti visos nepieciešamajos E-komercijas komponentos, un tie ir gatavi izmantošanai, kad pārslēdzat datplūsmu no sava satura piegādes tīkla (CDN) vai tīmekļa servera un novirziet to uz E-komercijas priekšgalu.</span><span class="sxs-lookup"><span data-stu-id="f5cda-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="f5cda-111">Domēnu pievienošana pēc E-komercijas inicializēšanas</span><span class="sxs-lookup"><span data-stu-id="f5cda-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="f5cda-112">Lai saistītu jaunus domēnus ar savu E-komercijas vidi pēc E-komercijas inicializēšanas, ir jāiesniedz pakalpojuma pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="f5cda-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5cda-113">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f5cda-113">Additional resources</span></span>

[<span data-ttu-id="f5cda-114">Jaunas e-komercijas vietnes izvietošana</span><span class="sxs-lookup"><span data-stu-id="f5cda-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f5cda-115">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="f5cda-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f5cda-116">Tiešsaistes vietnes saistīšana ar kanālu</span><span class="sxs-lookup"><span data-stu-id="f5cda-116">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f5cda-117">robots.txt failu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="f5cda-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="f5cda-118">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="f5cda-118">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f5cda-119">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="f5cda-119">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="f5cda-120">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="f5cda-120">Enable location-based store detection</span></span>](enable-store-detection.md)
