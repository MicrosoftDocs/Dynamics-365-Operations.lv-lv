---
title: Bieži uzdotie jautājumi par darbplūsmu
description: Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu programmā Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
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
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/01/2019
ms.locfileid: "773221"
---
# <a name="workflow-system"></a><span data-ttu-id="293f6-103">Darbplūsmas sistēma</span><span class="sxs-lookup"><span data-stu-id="293f6-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="293f6-104">Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="293f6-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="293f6-105">Paziņojumi</span><span class="sxs-lookup"><span data-stu-id="293f6-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="293f6-106">Kāpēc darba vienuma noraidīšanas gadījumā tiek saņemti vairāki paziņojumi?</span><span class="sxs-lookup"><span data-stu-id="293f6-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="293f6-107">Darba vienuma noraidīšanas gadījumā šis darba vienums tiek pabeigts ar statusu Noraidīts.</span><span class="sxs-lookup"><span data-stu-id="293f6-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="293f6-108">Tiek izveidots cits darba vienums, kas tiek piešķirts veidotājam.</span><span class="sxs-lookup"><span data-stu-id="293f6-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="293f6-109">Tas nozīmē, ka veidotājs saņem paziņojumu par noraidīto darba vienumu, bet lietotājs, kas ir piešķirts jaunajam izmaiņu pieprasījuma darba vienumam, saņem atsevišķu paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="293f6-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="293f6-110">Katrs paziņojums ir saistīts ar atšķirīgu darba vienumu, taču to līdzība var radīt apjukumu.</span><span class="sxs-lookup"><span data-stu-id="293f6-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="293f6-111">Mēs meklējam veidus, kā uzlabot šo situāciju nākamajā laidienā.</span><span class="sxs-lookup"><span data-stu-id="293f6-111">We are looking at ways to improve this in a future release.</span></span>
