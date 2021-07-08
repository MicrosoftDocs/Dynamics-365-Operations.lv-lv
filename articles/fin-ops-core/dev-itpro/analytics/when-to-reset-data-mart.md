---
title: Data mart atiestatīšanas BUJ
description: Šī tēma sniedz atbildes uz dažiem bieži uzdotiem jautājumiem par data mart atiestatīšanu.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266613"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="e4c5c-103">Data mart atiestatīšanas BUJ</span><span class="sxs-lookup"><span data-stu-id="e4c5c-103">Data mart resets FAQ</span></span>

<span data-ttu-id="e4c5c-104">Šī tēma sniedz atbildes uz dažiem bieži uzdotiem jautājumiem par data mart atiestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="e4c5c-105">Data mart atiestatīšana var būt laikietilpīgs process un atkarībā no apstākļiem var nebūt nepieciešamais risinājums.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="e4c5c-106">Tāpēc šī tēma ietver informāciju par apstākļiem, kuros data mart atiestatīšana var palīdzēt, kā arī gadījumos, kad tas, visticamāk, nepalīdzēs.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="e4c5c-107">Kas ir data mart atiestatīšana?</span><span class="sxs-lookup"><span data-stu-id="e4c5c-107">What is a data mart reset?</span></span>

<span data-ttu-id="e4c5c-108">Data marta atiestatīšana atspējos integrācijas uzdevumus, izdzēsis visus data mart datus un tad atkārtoti aktivizēs integrāciju.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="e4c5c-109">Lai nodrošinātu, ka vecie dati netiek ievietoti, data mart atiestatīšanu var sākt tikai pēc esošo uzdevumu pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="e4c5c-110">Ja mēģināsit atiestatīt data mart pirms visu uzdevumu pabeigšanas, iespējams, saņemsit ziņojumu, tādu kā "Data mart atiestatīšanu nevarēja apstrādāt aktīva uzdevuma dēļ.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="e4c5c-111">Lūdzu, vēlāk mēģiniet vēlreiz.”</span><span class="sxs-lookup"><span data-stu-id="e4c5c-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="e4c5c-112">Kad jāveic data mart atiestatīšana?</span><span class="sxs-lookup"><span data-stu-id="e4c5c-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="e4c5c-113">Ja uz jūsu situāciju attiecas viens vai vairāki no šiem priekšrakstiem, jūsu organizācija var gūt labumu no data mart atiestatīšanas:</span><span class="sxs-lookup"><span data-stu-id="e4c5c-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="e4c5c-114">Programmu datu bāze ir atjaunota.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-114">The application database was restored.</span></span>
- <span data-ttu-id="e4c5c-115">Jūs esat atvēris atbalsta biļeti, un atbalsta inženieris ir norādījis, ka jūs atiestatīt data mart kā daļu no problēmu novēršanas soļa.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="e4c5c-116">Kad data mart atiestatīšana nav piemērota?</span><span class="sxs-lookup"><span data-stu-id="e4c5c-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="e4c5c-117">Tālāk ir norādīti daži apstākļi, kad nav ieteicams atiestatīt data mart:</span><span class="sxs-lookup"><span data-stu-id="e4c5c-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="e4c5c-118">Jūs saskaraties ar datu sinhronizāciju saistītās veiktspējas problēmām.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="e4c5c-119">Jums ir periodiska atiestatīšanas shēma šādu iemeslu dēļ:</span><span class="sxs-lookup"><span data-stu-id="e4c5c-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="e4c5c-120">**Trūkst datu** – ja ievērojat, ka trūkst datu, atveriet atbalsta biļeti ar Microsoft, lai pārskatītu savu pārskata formātu un iespējamās datu sinhronizācijas problēmas.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="e4c5c-121">**Iesprūdis integrācijas stāvoklis**</span><span class="sxs-lookup"><span data-stu-id="e4c5c-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="e4c5c-122">**Novecojuši ieraksti** – novecojuši ieraksti paši par sevi neattaisno data mart atiestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="e4c5c-123">Ja ir iestatīta liela datu kopa, atiestatīšanas process var ilgt kādu laiku, bet maz ticams, ka tas novedīs pie kaut kādiem uzlabojumiem.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="e4c5c-124">Ja atiestatīšu datu mart, vai zaudēšu pārskatus, ko es jau esmu izveidojis?</span><span class="sxs-lookup"><span data-stu-id="e4c5c-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="e4c5c-125">Nē.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-125">No.</span></span> <span data-ttu-id="e4c5c-126">Jūsu pārskati tiek glabāti SQL tabulās, kuras neietekmē data mart atiestatīšana.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="e4c5c-127">Ja jums ir bažas par savu izstrādāto ziņojumu zaudēšanu, varat dublēt noformējumus, kurus nevēlaties zaudēt.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="e4c5c-128">Lai tos dublētu veidotājus, atveriet Pārskatu veidotāju un dodieties uz **Uzņēmums \> Uzņēmumi \> Veidošanas bloki \> Eksports**.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="e4c5c-129">Vai visiem lietotājiem ir jāiziet no sistēmas, pirms var atiestatīt data mart?</span><span class="sxs-lookup"><span data-stu-id="e4c5c-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="e4c5c-130">Nē.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-130">No.</span></span> <span data-ttu-id="e4c5c-131">Lietotāji var turpināt darbu sistēmā data mart atiestatīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="e4c5c-132">Tomēr, kamēr atiestatīšana nav pabeigta, lietotāji nevarēs piekļūt nevienam pārskatam, kas tika izveidoti, izmantojot finanšu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="e4c5c-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
