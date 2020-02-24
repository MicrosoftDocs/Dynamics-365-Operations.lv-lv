---
title: Izlases ikonas pievienošana
description: Šajā tēmā ir paskaidrots, kā pievienot izlases ikonu jūsu vietnei.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001545"
---
# <a name="add-a-favicon"></a><span data-ttu-id="db975-103">Izlases ikonas pievienošana</span><span class="sxs-lookup"><span data-stu-id="db975-103">Add a favicon</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="db975-104">Šajā tēmā ir paskaidrots, kā pievienot izlases ikonu jūsu vietnei.</span><span class="sxs-lookup"><span data-stu-id="db975-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="db975-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="db975-105">Overview</span></span>

<span data-ttu-id="db975-106">Izlases ikona ir neliels grafiskais fails, kas tiek attēlots tīmekļa pārlūkprogrammas cilnē, adreses joslā, pārlūkošanas vēsturē un grāmatzīmēs vai izlasē, kā arī citās vietās.</span><span class="sxs-lookup"><span data-stu-id="db975-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="db975-107">Mēs iesakām jums pievienot izlases ikonu jūsu vietnei, jo tā pārstāv un nostiprina jūsu zīmolu, kā arī palīdz atšķirt jūsu vietni no citām jūsu klientu apmeklētajām vietnēm.</span><span class="sxs-lookup"><span data-stu-id="db975-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="db975-108">Lai gan jūs varat pievienot vairākas dažādu izmēru un failu tipu izlases ikonas jūsu vietnē, šajā tēmā ir aprakstīts, kā pievienot vienu izlases ikonu.</span><span class="sxs-lookup"><span data-stu-id="db975-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="db975-109">Tomēr tas pats process un atrašanās vieta tiek izmantoti, lai pievienotu vairāk izlases ikonu.</span><span class="sxs-lookup"><span data-stu-id="db975-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="db975-110">Izlases ikonas augšupielāde jūsu vietnes līdzekļu kolekcijā</span><span class="sxs-lookup"><span data-stu-id="db975-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="db975-111">Lai pievienotu izlases ikonu jūsu vietnes līdzekļu kolekcijā, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="db975-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="db975-112">Dodieties uz **Līdzekļi \> Augšupielādēt \> Augšupielādēt līdzekļus**.</span><span class="sxs-lookup"><span data-stu-id="db975-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="db975-113">Atrodiet un izvēlēties izlases ikonu jūsu vietējā failu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="db975-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="db975-114">Ievadiet nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="db975-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="db975-115">Rekvizītu rūtī labajā pusē nokopējiet izlases ikonas publisko vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="db975-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="db975-116">Ja neizvēlaties opciju **Publicēt līdzekļus pēc augšupielādes**, atgriezieties pie lapas **Līdzekļi** un manuāli publicējiet izlases ikonu vēlāk.</span><span class="sxs-lookup"><span data-stu-id="db975-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="db975-117">HTML izveide izlases ikonai</span><span class="sxs-lookup"><span data-stu-id="db975-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="db975-118">Lai izveidotu HTML izlases ikonai, izmantojiet šādu HTML fragmentu.</span><span class="sxs-lookup"><span data-stu-id="db975-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="db975-119">**href** atribūtam aizvietojiet **“Public\_URL\_for\_your\_favicon”** ar publisku vietrādi URL, ko kopējāt agrāk.</span><span class="sxs-lookup"><span data-stu-id="db975-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="db975-120">HTML pievienošana izlases ikonai jūsu lapas \<galvenajā\> elementā</span><span class="sxs-lookup"><span data-stu-id="db975-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="db975-121">Lai pievienotu izlases ikonu jūsu vietnei, izmantojiet to pašu procedūru, kas tiek izmantota, lai pievienotu jebkāda veida HTML vai skriptu **\<galvenajam\>** elementam jūsu vietnes lapās.</span><span class="sxs-lookup"><span data-stu-id="db975-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db975-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="db975-122">Additional resources</span></span>

[<span data-ttu-id="db975-123">Logotipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="db975-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="db975-124">Vietnes dizaina atlase</span><span class="sxs-lookup"><span data-stu-id="db975-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="db975-125">Darbs ar CSS ignorēšanas failiem</span><span class="sxs-lookup"><span data-stu-id="db975-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="db975-126">Sveiciena ziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="db975-126">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="db975-127">Autortiesību paziņojuma pievienošana</span><span class="sxs-lookup"><span data-stu-id="db975-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="db975-128">Valodu pievienošana vietnei</span><span class="sxs-lookup"><span data-stu-id="db975-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="db975-129">Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju</span><span class="sxs-lookup"><span data-stu-id="db975-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

