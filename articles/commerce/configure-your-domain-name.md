---
title: Domēna nosaukuma konfigurēšana
description: Šajā tēmā paskaidrots, kā konfigurēt domēna nosaukumu Microsoft Dynamics 365 e-komercijas vietnei.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8b7bc322b1a42190d5eec99f89a34025c34ba09f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220490"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="bf3fe-103">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="bf3fe-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bf3fe-104">Šajā tēmā paskaidrots, kā konfigurēt domēna nosaukumu Microsoft Dynamics 365 e-komercijas vietnei.</span><span class="sxs-lookup"><span data-stu-id="bf3fe-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="bf3fe-105">Domēnu pievienošana e-komercijas inicializēšanas laikā</span><span class="sxs-lookup"><span data-stu-id="bf3fe-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="bf3fe-106">Lai saistītu domēnus ar savu Dynamics 365 Commerce e-komercijas vidi, inicializējiet e-komerciju, kā aprakstīts tēmā [Jaunas e-komercijas nomnieka izvietošana](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="bf3fe-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="bf3fe-107">Inicializēšanas laikā jums tiek lūgts sniegt informāciju, kas tiks izmantota jūsu e-komercijas vides nodrošināšanai.</span><span class="sxs-lookup"><span data-stu-id="bf3fe-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="bf3fe-108">Laukā **Atbalstītie resursdatora nosaukumi** pievienojiet visus domēnus, kurus plānojat izmantot šajā vidē.</span><span class="sxs-lookup"><span data-stu-id="bf3fe-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="bf3fe-109">Vairāki domēni jāatdala ar semikolu.</span><span class="sxs-lookup"><span data-stu-id="bf3fe-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="bf3fe-110">Šādā veidā domēni tiek konfigurēti visos nepieciešamajos komercijas komponentos, un tie ir gatavi izmantošanai, kad pārslēdzat datplūsmu no sava satura piegādes tīkla (CDN) vai tīmekļa servera un novirziet to uz e-komercijas priekšgalu.</span><span class="sxs-lookup"><span data-stu-id="bf3fe-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="bf3fe-111">Domēnu pievienošana pēc e-komercijas inicializēšanas</span><span class="sxs-lookup"><span data-stu-id="bf3fe-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="bf3fe-112">Lai saistītu jaunus domēnus ar savu e-komercijas vidi pēc e-komercijas inicializēšanas, ir jāiesniedz pakalpojuma pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="bf3fe-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bf3fe-113">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bf3fe-113">Additional resources</span></span>

[<span data-ttu-id="bf3fe-114">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="bf3fe-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="bf3fe-115">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="bf3fe-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="bf3fe-116">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="bf3fe-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="bf3fe-117">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="bf3fe-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="bf3fe-118">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="bf3fe-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="bf3fe-119">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="bf3fe-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="bf3fe-120">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="bf3fe-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="bf3fe-121">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="bf3fe-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="bf3fe-122">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="bf3fe-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="bf3fe-123">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="bf3fe-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]