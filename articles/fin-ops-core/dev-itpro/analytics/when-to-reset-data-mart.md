---
title: Kad atiestatīt data mart
description: Šajā tēmā uzskaitīti apstākļi, kas, iespējams, var tikt uzlaboti, no jauna atiestatot data mart, kas, maz ticams, ka palīdzēs.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988996"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="17ad1-103">Kad atiestatīt data mart</span><span class="sxs-lookup"><span data-stu-id="17ad1-103">When to reset a data mart</span></span>

<span data-ttu-id="17ad1-104">Data mart atiestatīšana var būt laikietilpīga.</span><span class="sxs-lookup"><span data-stu-id="17ad1-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="17ad1-105">Atkarībā no apstākļiem šī darbība var nebūt nepieciešamais risinājums.</span><span class="sxs-lookup"><span data-stu-id="17ad1-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="17ad1-106">Šajā tēmā uzskaitīti apstākļi, kas, iespējams, var tikt uzlaboti, no jauna atiestatot data mart, kas, maz ticams, ka palīdzēs.</span><span class="sxs-lookup"><span data-stu-id="17ad1-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="17ad1-107">Kad nepieciešams veikt data mart atiestatīšanu?</span><span class="sxs-lookup"><span data-stu-id="17ad1-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="17ad1-108">Pirms data mart atiestatīšanas aplūkosim šādus jautājumus.</span><span class="sxs-lookup"><span data-stu-id="17ad1-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="17ad1-109">Atbildot "jā" uz vienu vai vairākiem jautājumiem, var norādīt, ka jūsu organizācija var gūt labumu, atiestata data mart.</span><span class="sxs-lookup"><span data-stu-id="17ad1-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="17ad1-110">Vai programmu datu bāze ir atjaunota?</span><span class="sxs-lookup"><span data-stu-id="17ad1-110">Was the application database restored?</span></span>
- <span data-ttu-id="17ad1-111">Ja esat atvēris atbalsta incidentu, un atbalsta inženieris ir norādījis, ka jūs atiestatīt data mart kā daļu no problēmu novēršanas soļa.</span><span class="sxs-lookup"><span data-stu-id="17ad1-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="17ad1-112">Kad nav atbilstoši atiestatīt data mart?</span><span class="sxs-lookup"><span data-stu-id="17ad1-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="17ad1-113">Ir daži apstākļi, kad nav ieteicams atiestatīt data mart.</span><span class="sxs-lookup"><span data-stu-id="17ad1-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="17ad1-114">Tie ietver.</span><span class="sxs-lookup"><span data-stu-id="17ad1-114">These include the following.</span></span> 

- <span data-ttu-id="17ad1-115">Jūs saskaraties ar datu sinhronizāciju saistītās veiktspējas problēmām.</span><span class="sxs-lookup"><span data-stu-id="17ad1-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="17ad1-116">Ja periodisks atiestatīšanas modelis ir nepieciešams kāda no šo iemeslu dēļ:</span><span class="sxs-lookup"><span data-stu-id="17ad1-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="17ad1-117">**Trūkst datu**</span><span class="sxs-lookup"><span data-stu-id="17ad1-117">**Missing data**</span></span> 
  - <span data-ttu-id="17ad1-118">**Iesprūdis integrācijas stāvoklis**</span><span class="sxs-lookup"><span data-stu-id="17ad1-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="17ad1-119">**Novecojuši ieraksti** - novecojuši ieraksti paši par sevi neattaisno data mart atiestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="17ad1-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="17ad1-120">Ja ir iestatīta liela datu kopa, atiestatīšanas process var ilgt kādu laiku, bet maz ticams, ka tā rezultāts būs uzlabojums.</span><span class="sxs-lookup"><span data-stu-id="17ad1-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="17ad1-121">Kas ir data mart atiestatīšana?</span><span class="sxs-lookup"><span data-stu-id="17ad1-121">What is a data mart reset?</span></span>
- <span data-ttu-id="17ad1-122">Atiestatīšana sāksies tikai tad, kad esošie uzdevumi būs pabeigti.</span><span class="sxs-lookup"><span data-stu-id="17ad1-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="17ad1-123">Tas nodrošina, ka vecie dati netiek ievietoti.</span><span class="sxs-lookup"><span data-stu-id="17ad1-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="17ad1-124">Šajā brīdī varat redzēt ziņojumu, piemēram, "Data mart atiestatīšanu nevarēja apstrādāt aktīva uzdevuma dēļ.</span><span class="sxs-lookup"><span data-stu-id="17ad1-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="17ad1-125">Lūdzu, vēlāk mēģiniet vēlreiz."</span><span class="sxs-lookup"><span data-stu-id="17ad1-125">Please try again later.”</span></span>
- <span data-ttu-id="17ad1-126">Atiestatīšana atspējos integrācijas uzdevumus un izdzēsīs visus data mart datus.</span><span class="sxs-lookup"><span data-stu-id="17ad1-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="17ad1-127">Integrācijas atkārtota iespējošana.</span><span class="sxs-lookup"><span data-stu-id="17ad1-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="17ad1-128">Ja atiestatīšu datu mart, vai zaudēšu pārskatus, ko es jau esmu izveidojis?</span><span class="sxs-lookup"><span data-stu-id="17ad1-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="17ad1-129">Nē, jūsu pārskati tiek glabāti SQL tabulās, kuras neietekmē data mart atiestatīšana.</span><span class="sxs-lookup"><span data-stu-id="17ad1-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="17ad1-130">Ja jums ir bažas par savu izstrādāto ziņojumu zaudēšanu, varat dublēt noformējumus, kurus nevēlaties zaudēt.</span><span class="sxs-lookup"><span data-stu-id="17ad1-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="17ad1-131">Lai tos dublētu, atveriet Pārskatu veidotāju un dodieties uz **Uzņēmums > Uzņēmumi > Veidošanas bloki > Eksports**.</span><span class="sxs-lookup"><span data-stu-id="17ad1-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="17ad1-132">Vai visiem lietotājiem ir jāiziet no sistēmas, lai atiestatītu data mart?</span><span class="sxs-lookup"><span data-stu-id="17ad1-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="17ad1-133">Nē, lietotāji var turpināt darbu sistēmā data mart atiestatīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="17ad1-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="17ad1-134">Tomēr viņi nevarēs piekļūt nevienam pārskatam, kas tika izveidoti finanšu pārskatā līdz atiestatīšanas pabeigšanai.</span><span class="sxs-lookup"><span data-stu-id="17ad1-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
