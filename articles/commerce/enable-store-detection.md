---
title: Veikala noteikšanas iespējošana pēc atrašanās vietas
description: Šajā tēmā ir aprakstīts, kā ieslēgt uz atrašanās vietu balstītu veikala atrašanu jūsu Dynamics 365 Commerce vietnē.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a542d6987280451910b4ff3bcfb3a109a0e028c6
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697616"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="59e2c-103">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="59e2c-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="59e2c-104">Šajā tēmā ir aprakstīts, kā ieslēgt uz atrašanās vietu balstītu veikala atrašanu jūsu Dynamics 365 Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="59e2c-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="59e2c-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="59e2c-105">Overview</span></span>

<span data-ttu-id="59e2c-106">Uz atrašanās vietu balstīta veikala atrašana Commerce ļauj nodrošināt klientiem būtisku vietnes saturu, pamatojoties uz to atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="59e2c-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="59e2c-107">Ja ir ieslēgta uz atrašanās vietu balstīta veikala atrašana, Commerce atveidošanas pakalpojums izmanto informāciju par valsti / reģionu no klienta tīmekļa pārlūkprogrammas IP adreses, lai novirzītu klientu uz visatbilstošāko pieejamo ģeogrāfiskās vietas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="59e2c-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="59e2c-108">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="59e2c-108">Privacy notice</span></span>

<span data-ttu-id="59e2c-109">Ja ieslēdzat uz atrašanās vietu balstītu veikala atrašanas līdzekli, informācija no klienta pārlūkprogrammas tiek nosūtīta Microsoft vietas pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="59e2c-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="59e2c-110">Šī informācija pēc tam tiek izmantota, lai nodrošinātu klientam saturu, kas ir būtisks viņa atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="59e2c-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="59e2c-111">Gan informācija, kas tiek sūtīta no klienta pārlūka, gan uz atrašanās vietu balstītā informācija, kas tiek nosūtīta atpakaļ klientam, ir pakļauta privātuma un sīkfailu atbilstības politikām.</span><span class="sxs-lookup"><span data-stu-id="59e2c-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="59e2c-112">Uz atrašanās vietu balstītas veikala atrašanas ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="59e2c-112">Turn on location-based store detection</span></span>

<span data-ttu-id="59e2c-113">Lai ieslēgtu uz atrašanās vietu balstītu veikala atrašanu Commerce, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="59e2c-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="59e2c-114">Autorēšanas rīkā dodieties uz savu vietni.</span><span class="sxs-lookup"><span data-stu-id="59e2c-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="59e2c-115">Navigācijas rūtī kreisajā pusē atlasiet **Lapas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="59e2c-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="59e2c-116">Atlasiet **Lapas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="59e2c-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="59e2c-117">Iestatiet opciju **Iespējot uz atrašanās vietu balstītu veikala atrašanu** uz **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="59e2c-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59e2c-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="59e2c-118">Additional resources</span></span>

[<span data-ttu-id="59e2c-119">Tiešsaistes veikala apskats</span><span class="sxs-lookup"><span data-stu-id="59e2c-119">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="59e2c-120">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="59e2c-120">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="59e2c-121">Jaunas e-komercijas vietnes izvietošana</span><span class="sxs-lookup"><span data-stu-id="59e2c-121">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="59e2c-122">Tiešsaistes vietnes saistīšana ar kanālu</span><span class="sxs-lookup"><span data-stu-id="59e2c-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="59e2c-123">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="59e2c-123">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="59e2c-124">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="59e2c-124">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="59e2c-125">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="59e2c-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
