---
title: Bieži uzdotie jautājumi par darbplūsmu
description: Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu programmā Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509295"
---
# <a name="workflow-system"></a><span data-ttu-id="446a2-103">Darbplūsmas sistēma</span><span class="sxs-lookup"><span data-stu-id="446a2-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="446a2-104">Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="446a2-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="446a2-105">Paziņojumi</span><span class="sxs-lookup"><span data-stu-id="446a2-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="446a2-106">Kāpēc darba vienuma noraidīšanas gadījumā tiek saņemti vairāki paziņojumi?</span><span class="sxs-lookup"><span data-stu-id="446a2-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="446a2-107">Darba vienuma noraidīšanas gadījumā šis darba vienums tiek pabeigts ar statusu Noraidīts.</span><span class="sxs-lookup"><span data-stu-id="446a2-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="446a2-108">Tiek izveidots cits darba vienums, kas tiek piešķirts veidotājam.</span><span class="sxs-lookup"><span data-stu-id="446a2-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="446a2-109">Tas nozīmē, ka veidotājs saņem paziņojumu par noraidīto darba vienumu, bet lietotājs, kas ir piešķirts jaunajam izmaiņu pieprasījuma darba vienumam, saņem atsevišķu paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="446a2-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="446a2-110">Katrs paziņojums ir saistīts ar atšķirīgu darba vienumu, taču to līdzība var radīt apjukumu.</span><span class="sxs-lookup"><span data-stu-id="446a2-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="446a2-111">Mēs meklējam veidus, kā uzlabot šo situāciju nākamajā laidienā.</span><span class="sxs-lookup"><span data-stu-id="446a2-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="446a2-112">Kāpēc manas darbplūsmas tiek eksportētas neveiksmīgi?</span><span class="sxs-lookup"><span data-stu-id="446a2-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="446a2-113">Pašlaik darbplūsmas eksportēšanas līdzeklī ir noteikts ierobežojums, kas neļauj darbplūsmas nosaukumiem pārsniegt 48 rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="446a2-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="446a2-114">Izmantojot nosaukumu, kas ir garāks par 48 rakstzīmēm, var rasties kļūda “Serveris nevarēja autentificēt pieprasījumu” un/vai iespējamība, ka faila eksportēšana netiks ļauta bez faila tipa.</span><span class="sxs-lookup"><span data-stu-id="446a2-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="446a2-115">Detalizēta informācija ir pieejama šajā emuāra ziņā: [Darbplūsmas eksportēšanas problēmu risināšana](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="446a2-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
