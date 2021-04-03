---
title: Veikala noteikšanas iespējošana pēc atrašanās vietas
description: Šajā tēmā ir aprakstīts, kā ieslēgt uz atrašanās vietu balstītu veikala atrašanu jūsu Dynamics 365 Commerce vietnē.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b34f156642b23f7b9754dac1ee81c7d0004872d8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478192"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="338e3-103">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="338e3-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="338e3-104">Šajā tēmā ir aprakstīts, kā ieslēgt uz atrašanās vietu balstītu veikala atrašanu jūsu Dynamics 365 Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="338e3-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="338e3-105">Uz atrašanās vietu balstīta veikala atrašana Commerce ļauj nodrošināt klientiem būtisku vietnes saturu, pamatojoties uz to atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="338e3-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="338e3-106">Ja ir ieslēgta uz atrašanās vietu balstīta veikala atrašana, Commerce atveidošanas pakalpojums izmanto informāciju par valsti / reģionu no klienta tīmekļa pārlūkprogrammas IP adreses, lai novirzītu klientu uz visatbilstošāko pieejamo ģeogrāfiskās vietas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="338e3-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="338e3-107">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="338e3-107">Privacy notice</span></span>

<span data-ttu-id="338e3-108">Ja ieslēdzat uz atrašanās vietu balstītu veikala atrašanas līdzekli, informācija no klienta pārlūkprogrammas tiek nosūtīta Microsoft vietas pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="338e3-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="338e3-109">Šī informācija pēc tam tiek izmantota, lai nodrošinātu klientam saturu, kas ir būtisks viņa atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="338e3-109">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="338e3-110">Gan informācija, kas tiek sūtīta no klienta pārlūka, gan uz atrašanās vietu balstītā informācija, kas tiek nosūtīta atpakaļ klientam, ir pakļauta privātuma un sīkfailu atbilstības politikām.</span><span class="sxs-lookup"><span data-stu-id="338e3-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="338e3-111">Uz atrašanās vietu balstītas veikala atrašanas ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="338e3-111">Turn on location-based store detection</span></span>

<span data-ttu-id="338e3-112">Lai ieslēgtu uz atrašanās vietu balstītu veikala atrašanu Commerce, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="338e3-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="338e3-113">Autorēšanas rīkā dodieties uz savu vietni.</span><span class="sxs-lookup"><span data-stu-id="338e3-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="338e3-114">Navigācijas rūtī kreisajā pusē atlasiet **Lapas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="338e3-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="338e3-115">Atlasiet **Lapas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="338e3-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="338e3-116">Iestatiet opciju **Iespējot uz atrašanās vietu balstītu veikala atrašanu** uz **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="338e3-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="338e3-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="338e3-117">Additional resources</span></span>

[<span data-ttu-id="338e3-118">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="338e3-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="338e3-119">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="338e3-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="338e3-120">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="338e3-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="338e3-121">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="338e3-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="338e3-122">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="338e3-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="338e3-123">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="338e3-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="338e3-124">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="338e3-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="338e3-125">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="338e3-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="338e3-126">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="338e3-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="338e3-127">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="338e3-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
