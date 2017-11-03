---
title: "Autorizēt pielāgotu prognozi"
description: "Ne visi prognozes dati ir jāautorizē nekavējoties. Šajā tēmā ir izskaidrots, kā var norādīt periodu, kuram prognoze ir autorizēta. Tajā arī izskaidrots, kā var autorizēt noteiktu uzņēmumu prognozi un prognozes modeļus."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5ce38e94ae4c7b28b4e182018add7c046f685e46
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="fe5e5-105">Autorizēt pielāgotu prognozi</span><span class="sxs-lookup"><span data-stu-id="fe5e5-105">Authorize an adjusted forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fe5e5-106">Visi prognozes datu nav jāautorizē nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="fe5e5-107">Šajā tēmā ir izskaidrots, kā var norādīt periodu, kuram prognoze ir autorizēta.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="fe5e5-108">Tajā arī izskaidrots, kā var autorizēt noteiktu uzņēmumu prognozi un prognozes modeļus.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="fe5e5-109">Visi prognozes datu nav jāautorizē nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="fe5e5-110">Var norādīt prognozes autorizētā perioda sākuma un beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="fe5e5-111">Šī funkcija ļauj iesaldēt noteiktus intervālus.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="fe5e5-112">Norādītajam sākuma un beigu datumam ir jāatbilst tā intervāla sākuma un beigu datumam, kurā šī prognoze ir ģenerēta.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="fe5e5-113">Šis ierobežojums ir noteikts sistēmā, un, ja ir jāveic korekcijas, datumi tiek automātiski pielāgoti.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="fe5e5-114">Lapas **Autorizācija** cilnē **Detalizēta informācija** var skatīt detalizētu informāciju par pēdējo ģenerēto prognozi.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="fe5e5-115">Var atlasīt uzņēmumus un prognožu modeļus, ko izmantot prognozes autorizēšanai.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="fe5e5-116">Pēc noklusējuma režģī ir iekļauti visi uzņēmumi, kam ir izveidots prognozes pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="fe5e5-117">Katram uzņēmumam iepriekš tiek ievadīts prognozes modelis, kas atbilst pašreizējam vispārējās plānošanas parametros iestatītajam prognozes plānam.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="fe5e5-118">Taču šo prognozes modeli var mainīt, izmantojot jebkuru šim uzņēmumam atbilstošo prognozes modeli.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="fe5e5-119">Ja atlasītajam uzņēmumam nav ģenerēti prognozes pieprasījuma dati, importēšanas laikā tiek parādīts brīdinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="fe5e5-120">Ir ļoti svarīgi saprast izvēles rūtiņas **Saglabāt bāzlīnijas pieprasījuma apjoma prognozē manuāli veiktās korekcijas** darbības principus.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="fe5e5-121">Ja statistiskās bāzlīnijas prognoze ir manuāli koriģēta, tad koriģētās vērtības tiek autorizētas lietošanai pat tad, ja šīs izvēles rūtiņas atzīme ir noņemta.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="fe5e5-122">Tomēr pēc autorizācijas izmaiņas tiek atmestas.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="fe5e5-123">Nākamajā prognozes ģenerēšanas reizē šai prognozei ir tikai statiska nozīme, un tajā netiek manuāli pārrakstīti dati arī tad, ja izvēles rūtiņa **Pārsūtīt manuālās korekcijas uz pieprasījuma apjoma prognozi** ir atzīmēta.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="fe5e5-124">Tāpēc ir jāņem vēra izvēles rūtiņas **Saglabāt bāzlīnijas pieprasījuma apjoma prognozē manuāli veiktās korekcijas** darbības mehānisms, kas ļauj saglabāt vai atmest visas manuāli veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="see-also"></a><span data-ttu-id="fe5e5-125">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="fe5e5-125">See also</span></span>
--------

[<span data-ttu-id="fe5e5-126">Manuālu bāzlīnijas prognozes korekciju veikšana</span><span class="sxs-lookup"><span data-stu-id="fe5e5-126">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="fe5e5-127">Prognozes precizitātes pārraudzība</span><span class="sxs-lookup"><span data-stu-id="fe5e5-127">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




