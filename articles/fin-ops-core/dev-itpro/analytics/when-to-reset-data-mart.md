---
title: Kad atiestatīt data mart
description: Šajā tēmā uzskaitīti apstākļi, kas, iespējams, var tikt uzlaboti, no jauna atiestatot data mart, kas, maz ticams, ka palīdzēs.
author: jinniew
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c88994a336528650bf8ab6e239c873fa6cd36c46
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754148"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="dff29-103">Kad atiestatīt data mart</span><span class="sxs-lookup"><span data-stu-id="dff29-103">When to reset a data mart</span></span>

<span data-ttu-id="dff29-104">Data mart atiestatīšana var būt laikietilpīga.</span><span class="sxs-lookup"><span data-stu-id="dff29-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="dff29-105">Atkarībā no apstākļiem šī darbība var nebūt nepieciešamais risinājums.</span><span class="sxs-lookup"><span data-stu-id="dff29-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="dff29-106">Šajā tēmā uzskaitīti apstākļi, kas, iespējams, var tikt uzlaboti, no jauna atiestatot data mart, kas, maz ticams, ka palīdzēs.</span><span class="sxs-lookup"><span data-stu-id="dff29-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="dff29-107">Kad nepieciešams veikt data mart atiestatīšanu?</span><span class="sxs-lookup"><span data-stu-id="dff29-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="dff29-108">Pirms data mart atiestatīšanas aplūkosim šādus jautājumus.</span><span class="sxs-lookup"><span data-stu-id="dff29-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="dff29-109">Atbildot "jā" uz vienu vai vairākiem jautājumiem, var norādīt, ka jūsu organizācija var gūt labumu, atiestata data mart.</span><span class="sxs-lookup"><span data-stu-id="dff29-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="dff29-110">Programmas datu bāze tika atjaunota, bet data mart netika atjaunota.</span><span class="sxs-lookup"><span data-stu-id="dff29-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="dff29-111">Jūs redzat nepareizus datus uzskaites periodam, kas nav pārskata dizaina problēmas rezultāts.</span><span class="sxs-lookup"><span data-stu-id="dff29-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="dff29-112">Jūs redzat nepareizus datus uzskaites periodam, un ieraksti tiek uzskaitīti integrācijas mēģinājumu sarakstā pārskatu veidotāja lapā **Integrācijas statuss** (startējiet pārskatu veidotāju un atlasiet **Rīki > Integrācijas statuss**).</span><span class="sxs-lookup"><span data-stu-id="dff29-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="dff29-113">Jūs esat atvēris atbalsta incidentu, un atbalsta inženieris ir norādījis, ka jūs atiestatīt data mart kā daļu no problēmu novēršanas soļa.</span><span class="sxs-lookup"><span data-stu-id="dff29-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="dff29-114">Kad nav atbilstoši atiestatīt data mart?</span><span class="sxs-lookup"><span data-stu-id="dff29-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="dff29-115">Ir daži apstākļi, kad nav ieteicams atiestatīt data mart.</span><span class="sxs-lookup"><span data-stu-id="dff29-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="dff29-116">Tie ietver.</span><span class="sxs-lookup"><span data-stu-id="dff29-116">These include the following.</span></span> 

- <span data-ttu-id="dff29-117">Jebkurā laikā šajā tēmā nav uzskaitīts iemesls.</span><span class="sxs-lookup"><span data-stu-id="dff29-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="dff29-118">Jūs saskaraties ar datu sinhronizāciju saistītās veiktspējas problēmas. Šajā iestatījumā, iespējams, data mart atiestatīšana nelīdzēsies.</span><span class="sxs-lookup"><span data-stu-id="dff29-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="dff29-119">Ja periodisks atiestatīšanas modelis ir nepieciešams kāda no šo iemeslu dēļ:</span><span class="sxs-lookup"><span data-stu-id="dff29-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="dff29-120">**Trūkst dati** - vispirms likvidējiet pārskata dizaina problēmas un datu sinhronizēšanas hronometrāžas problēmas, piemēram, jūs ievērojat, ka fakta karte nav palaista, jo trūkstošie dati tika grāmatoti.</span><span class="sxs-lookup"><span data-stu-id="dff29-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="dff29-121">**Kavēts integrācijas stāvoklis** - Ja integrācija ir lēna vai šķiet, ka pielīmē, datu izejas plūsma tiek atiestatīta, maz ticams, lai atrisinātu problēmu.</span><span class="sxs-lookup"><span data-stu-id="dff29-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="dff29-122">**Mēģinājumi atiestatīt ir bijuši neveiksmīgi** - Ja ir veikts mēģinājumu skaits pabeigt atiestatīšanu, un to nav bijis neveiksmīgs, tāpēc ieteicams atvērt atbalsta atgadījumu un strādāt ar atbalsta inženieri, lai analizētu jūsu situāciju pirms datu neveiksmīgas atiestatīšanas mēģinājuma vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="dff29-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="dff29-123">**Novecojuši ieraksti** - novecojuši ieraksti paši par sevi neattaisno data mart atiestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="dff29-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="dff29-124">Ja ir iestatīta liela datu kopa, atiestatīšanas process var ilgt kādu laiku, bet maz ticams, ka tā rezultāts būs uzlabojums.</span><span class="sxs-lookup"><span data-stu-id="dff29-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="dff29-125">Ko data mart atiestatīšana nedara</span><span class="sxs-lookup"><span data-stu-id="dff29-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="dff29-126">Atiestatīšana sāksies tikai tad, kad esošie uzdevumi būs pabeigti.</span><span class="sxs-lookup"><span data-stu-id="dff29-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="dff29-127">Tas nodrošina, ka vecie dati netiek ievietoti.</span><span class="sxs-lookup"><span data-stu-id="dff29-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="dff29-128">Šajā brīdī varat redzēt ziņojumu, piemēram, "Data mart atiestatīšanu nevarēja apstrādāt aktīva uzdevuma dēļ.</span><span class="sxs-lookup"><span data-stu-id="dff29-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="dff29-129">Lūdzu, vēlāk mēģiniet vēlreiz."</span><span class="sxs-lookup"><span data-stu-id="dff29-129">Please try again later.”</span></span>
- <span data-ttu-id="dff29-130">Atiestatīšana atspējos integrācijas uzdevumus un izdzēsīs visus data mart datus.</span><span class="sxs-lookup"><span data-stu-id="dff29-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="dff29-131">Integrācijas atkārtota iespējošana.</span><span class="sxs-lookup"><span data-stu-id="dff29-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="dff29-132">Tālāk norādītajiem punktiem ir divas lietas, kas *neatiestata* data mart.</span><span class="sxs-lookup"><span data-stu-id="dff29-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="dff29-133">Atiestatīšana nenoņem pārskata dizainus.</span><span class="sxs-lookup"><span data-stu-id="dff29-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="dff29-134">Atiestatīšana, ja nav atlasīta, nenoņem uzņēmuma datus vai lietotāja datus.</span><span class="sxs-lookup"><span data-stu-id="dff29-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]