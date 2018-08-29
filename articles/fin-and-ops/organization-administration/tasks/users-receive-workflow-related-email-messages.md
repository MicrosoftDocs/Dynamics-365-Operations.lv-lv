--- 
title: "Sistēmas konfigurēšana, lai lietotājiem sūtītu ar darbplūsmu saistītus e-pasta ziņojumus"
description: "Sistēmu varat konfigurēt tā, lai lietotājiem sūtītu e-pasta ziņojumus, kad notiek ar darbplūsmu saistīti notikumi."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a><span data-ttu-id="3b703-103">Sistēmas konfigurēšana, lai lietotājiem sūtītu ar darbplūsmu saistītus e-pasta ziņojumus</span><span class="sxs-lookup"><span data-stu-id="3b703-103">Configure the system to send workflow-related email to users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3b703-104">Sistēmu varat konfigurēt tā, lai lietotājiem sūtītu e-pasta ziņojumus, kad notiek ar darbplūsmu saistīti notikumi.</span><span class="sxs-lookup"><span data-stu-id="3b703-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="3b703-105">Piemēram, e-pasta ziņojumus var nosūtīt lietotājiem, ja to apstiprināšanai ir piešķirti dokumenti.</span><span class="sxs-lookup"><span data-stu-id="3b703-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="3b703-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="3b703-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3b703-107">Pārejiet uz sadaļu Sistēmas administrēšana > Lietotāji > Lietotāji.</span><span class="sxs-lookup"><span data-stu-id="3b703-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="3b703-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3b703-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3b703-109">Noklikšķiniet uz Lietotāja opcijas.</span><span class="sxs-lookup"><span data-stu-id="3b703-109">Click User options.</span></span>
4. <span data-ttu-id="3b703-110">Noklikšķiniet uz cilnes Darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="3b703-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="3b703-111">Pārliecinieties, ka sadaļa Paziņojumi ir izvērsta.</span><span class="sxs-lookup"><span data-stu-id="3b703-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="3b703-112">Sadaļā Paziņojumi varat norādīt, kā paziņot lietotājam par notikumiem, kas ir saistīti ar darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="3b703-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="3b703-113">Laukā Rindas vienuma darbplūsmas paziņojuma tips atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="3b703-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="3b703-114">Grupēti — paziņojumi par rindas krājumiem tiek grupēti vienā e-pasta ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="3b703-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="3b703-115">Atsevišķi — e-pasta ziņojums tiek nosūtīts katram rindas krājumam.</span><span class="sxs-lookup"><span data-stu-id="3b703-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="3b703-116">Ja vēlaties, lai lietotājs saņem paziņojumus klientā, tad atzīmējiet izvēles rūtiņu Sūtīt paziņojumus ar e-pasta ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="3b703-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="3b703-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3b703-117">Click Save.</span></span>
7. <span data-ttu-id="3b703-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3b703-118">Close the page.</span></span>


