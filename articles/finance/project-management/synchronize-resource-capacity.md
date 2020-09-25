---
title: Sinhronizēt resursu noslodzi
description: Šī tēma sniedz informāciju par to, kā sinhronizēt resursa noslodzi kalendāros un projektos.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760602"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="8fc17-103">Sinhronizēt resursu noslodzi</span><span class="sxs-lookup"><span data-stu-id="8fc17-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fc17-104">Resursu sinhronizēšanas process palīdz nodrošināt to, ka informācija kalendāram un pamatkalendāram nokļūst projekta resursu plānošanā.</span><span class="sxs-lookup"><span data-stu-id="8fc17-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="8fc17-105">Ja kalendārs tiek mainīts, procesi veic nepieciešamos atjauninājumus projekta resursu plānošanai.</span><span class="sxs-lookup"><span data-stu-id="8fc17-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="8fc17-106">Šie procesi arī palīdz uzlabot veiktspēju, jo kalendāra resursu informācija tiek sinhronizēta jau iepriekš.</span><span class="sxs-lookup"><span data-stu-id="8fc17-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="8fc17-107">Tāpēc resursu plānošanas informācijas atjauninājumi notiek ātrāk.</span><span class="sxs-lookup"><span data-stu-id="8fc17-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="8fc17-108">Procesu plānošanu ieteicams veikt kā pakešuzdevumu, nevis atsevišķi katram procesam.</span><span class="sxs-lookup"><span data-stu-id="8fc17-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="8fc17-109">Pretējā gadījumā pastāv risks, ka kāds aizmirsīs ietvertos datumus, kad pēdējo reizi tika sinhronizēta informācija.</span><span class="sxs-lookup"><span data-stu-id="8fc17-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="8fc17-110">Ja netiek izmantoti ietvertie datumi, datu sinhronizācijas laikā var rasties pārrāvumi.</span><span class="sxs-lookup"><span data-stu-id="8fc17-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendāra sinhronizācija](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="8fc17-112">Sinhronizēt resursu noslodzes apkopojumus</span><span class="sxs-lookup"><span data-stu-id="8fc17-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="8fc17-113">Sinhronizācijas process ir paredzēts, lai sinhronizētu visu resursu kalendāra informāciju.</span><span class="sxs-lookup"><span data-stu-id="8fc17-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="8fc17-114">Šajā informācijā ir ietverta pamatkalendāra informācija par visām izmaiņām projekta resursu kalendāra noslodzes tabulā.</span><span class="sxs-lookup"><span data-stu-id="8fc17-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="8fc17-115">Ja projektā tiek pievienoti jauni resursi, sinhronizācija palīdz garantēt to, ka ir pieejama atjaunināta kalendāra informācija.</span><span class="sxs-lookup"><span data-stu-id="8fc17-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="8fc17-116">Šo sinhronizāciju var veikt jebkurā laikā.</span><span class="sxs-lookup"><span data-stu-id="8fc17-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="8fc17-117">Ieteicams izmantot partijas.</span><span class="sxs-lookup"><span data-stu-id="8fc17-117">We recommend that you use a batch.</span></span> <span data-ttu-id="8fc17-118">Opcijas ir pieejamas noslodzes rezervāciju sinhronizēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="8fc17-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="8fc17-119">Atlasiet **Projektu vadība un uzskaite** &gt; **Periodisks** &gt; **Noslodzes sinhronizācija** &gt; **Sinhronizēt resursu noslodzes apkopojumus**.</span><span class="sxs-lookup"><span data-stu-id="8fc17-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="8fc17-120">Iestatiet opcijas nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="8fc17-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="8fc17-121">Opcija</span><span class="sxs-lookup"><span data-stu-id="8fc17-121">Option</span></span>      | <span data-ttu-id="8fc17-122">Apraksts</span><span class="sxs-lookup"><span data-stu-id="8fc17-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="8fc17-123">Perioda kods</span><span class="sxs-lookup"><span data-stu-id="8fc17-123">Period code</span></span> | <span data-ttu-id="8fc17-124">Ja vēlaties, atlasiet virsgrāmatas datumu intervāla kodu, lai resursu noslodzes apkopojumu sinhronizācijas procesam iestatītu sākuma un beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="8fc17-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="8fc17-125">Sākuma datums</span><span class="sxs-lookup"><span data-stu-id="8fc17-125">Start date</span></span>  | <span data-ttu-id="8fc17-126">Ievadiet resursu noslodzes apkopojumu sinhronizācijas procesa sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="8fc17-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="8fc17-127">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="8fc17-127">End date</span></span>    | <span data-ttu-id="8fc17-128">Ievadiet resursu noslodzes apkopojumu sinhronizācijas procesa beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="8fc17-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="8fc17-129">[![Sinhronizācijas process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="8fc17-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
