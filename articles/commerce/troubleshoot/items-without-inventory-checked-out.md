---
title: Vienības bez krājumiem var izrakstīt
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad debitori var pievienot savam grozam krājumus, kas nav noliktavā, un turpināt apmaksu.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018462"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="c85e1-103">Vienības bez krājumiem var izrakstīt</span><span class="sxs-lookup"><span data-stu-id="c85e1-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c85e1-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad debitori var pievienot savam grozam krājumus, kas nav noliktavā, un turpināt apmaksu.</span><span class="sxs-lookup"><span data-stu-id="c85e1-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="c85e1-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c85e1-105">Description</span></span>

<span data-ttu-id="c85e1-106">Lietotāji var pievienot preci savam grozam, pat ja veikalā nav rīcībā esošu krājumu un tad pāriet uz apmaksas lapu.</span><span class="sxs-lookup"><span data-stu-id="c85e1-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="c85e1-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="c85e1-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="c85e1-108">Iespējot rekvizītu Rādīt Nav noliktavā kļūdas Commerce vietnes veidotājā</span><span class="sxs-lookup"><span data-stu-id="c85e1-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="c85e1-109">Lai iespējotu rekvizītu **Rādīt Nav noliktavā kļūdas** Commerce vietnes veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c85e1-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c85e1-110">Atlasiet vietni, pie kuras strādājat.</span><span class="sxs-lookup"><span data-stu-id="c85e1-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="c85e1-111">Kreisās puses navigācijā atlasiet **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="c85e1-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="c85e1-112">Atlasiet **CartPage**, lai to atvērtu.</span><span class="sxs-lookup"><span data-stu-id="c85e1-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="c85e1-113">Atlasiet slotu **1. grozs**, atlasiet **Rediģēt** un pēc tam rekvizītu rūtī atzīmējiet izvēles rūtiņu **Rādīt Nav noliktavā kļūdas**.</span><span class="sxs-lookup"><span data-stu-id="c85e1-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="c85e1-114">Saglabājiet un publicējiet lapu.</span><span class="sxs-lookup"><span data-stu-id="c85e1-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c85e1-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c85e1-115">Additional resources</span></span>

[<span data-ttu-id="c85e1-116">Krājumu iestatījumu lietošana</span><span class="sxs-lookup"><span data-stu-id="c85e1-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="c85e1-117">Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem</span><span class="sxs-lookup"><span data-stu-id="c85e1-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="c85e1-118">Krājumu buferu un krājumu līmeņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c85e1-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
