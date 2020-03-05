---
title: Mazumtirdzniecības cenu pārskati
description: Šajā tēmā ir sniegts apskats par cenu pārskatu līdzekli, ko var izmantot, lai skatītu sašķiroto preču gaidāmās cenu izmaiņas.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 91c0a96abdd7df9e85e63ca6b1b47a57f3f401eb
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023333"
---
# <a name="retail-price-reports"></a><span data-ttu-id="b7ad0-103">Mazumtirdzniecības cenu pārskati</span><span class="sxs-lookup"><span data-stu-id="b7ad0-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="b7ad0-104">Lai piedāvātu saviem debitoriem konkurētspējīgas cenas, mazumtirgotāji bieži maina preču cenas.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="b7ad0-105">Veikala vadītājiem ir vajadzīga iespēja viegli piekļuvi jaunākajām vai gaidāmajām cenu izmaiņām, lai viņi varētu plānot resursus, kas ir nepieciešami veikala plauktos redzamo preču etiķešu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="b7ad0-106">Retail laidienā 10.0 veikala vadītājs var atvērt pārskatu **Cena**, pārejot uz sadaļu **Visi veikali \> Veikals \> Cenas pārskats** un skatot ar veikalu saistīto preču atjauninātās cenas.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="b7ad0-107">Lai iespējotu cenu pārskatu, ir jāiespējo parametrs **Iespējot cenu pārskatu par veikalu**.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-107">To enable the price report, the **Enable price report for store** parameter must be turned on.</span></span> <span data-ttu-id="b7ad0-108">Šis parametrs atrodas cilnē **Commerce parametri \> Atlaides \> Dažādi**. Atverot lapu **Cenu pārskats**, tiek parādīts dialoglodziņš ar dažādām konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-108">This parameter is located on the **Commerce parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="b7ad0-109">Tālāk ir norādītas pieejamās konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="b7ad0-110">Konfigurācija</span><span class="sxs-lookup"><span data-stu-id="b7ad0-110">Configuration</span></span> | <span data-ttu-id="b7ad0-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="b7ad0-111">Description</span></span> |
|---|---|
| <span data-ttu-id="b7ad0-112">Sākuma datums/beigu datums</span><span class="sxs-lookup"><span data-stu-id="b7ad0-112">From date / To date</span></span>| <span data-ttu-id="b7ad0-113">Datumu diapazons, par kuru ir jāģenerē cenu pārskats.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="b7ad0-114">Pašlaik ilgums nedrīkst pārsniegt 7 dienas.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="b7ad0-115">Kanāls</span><span class="sxs-lookup"><span data-stu-id="b7ad0-115">Channel</span></span>| <span data-ttu-id="b7ad0-116">Veikals, par kuru ir jāģenerē cenu pārskats.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-116">The store for which the price report should be generated.</span></span> |
| <span data-ttu-id="b7ad0-117">Parādīt preces, kam pieejami krājumi</span><span class="sxs-lookup"><span data-stu-id="b7ad0-117">Display products with available inventory</span></span>| <span data-ttu-id="b7ad0-118">Ja tiek iestatīta vērtība **Jā**, tiek rādītas tikai to preču cenas, kas pašlaik ir pieejamas veikala fiziskajos krājumos.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="b7ad0-119">Parādīt variantu cenas</span><span class="sxs-lookup"><span data-stu-id="b7ad0-119">Display prices for variants</span></span> | <span data-ttu-id="b7ad0-120">Ja tiek iestatīta vērtība **Jā**, tiek parādītas variantu, kā arī preču šablonu cenas.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="b7ad0-121">Šo opciju drīkst**iespējot** tikai tad, ja izmantojat variantiem raksturīgas cenas, jo būtiski palielinās rindu skaits.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="b7ad0-122">Turpmākajos laidienos tiks iespējotas no dimensijas atkarīgas cenas, lai veikala vadītājs varētu izvēlēties dimensijas, kuru cenas ir jāparāda.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="b7ad0-123">Parādīt preces ar cenu izmaiņām</span><span class="sxs-lookup"><span data-stu-id="b7ad0-123">Display products with price changes</span></span> | <span data-ttu-id="b7ad0-124">Ja ir iestatīta vērtība **Jā**, tiek parādītas cenas tikai tajos datumos, kad ir mainīta cena.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="b7ad0-125">Vienmēr tiek rādīta cena *vienu dienu pirms* laukā **Sākuma datums** atlasītā datuma, lai veikala vadītājs varētu viegli noteikt preces, kuru cenas nav mainītas visā atlasītajā periodā, kā arī skatīt pašreizējo cenu.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="b7ad0-126">Pēc pārskata izveides var lejupielādēt Excel failu, lai veiktu jebkāda veida papildu filtrēšanu.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="b7ad0-127">Cenu pārskatu var arī izmantot, lai pārbaudītu preču vēsturiskās cenas iepriekšējos datumos.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-127">The price report can also be used to check the historical prices of products for past dates.</span></span>