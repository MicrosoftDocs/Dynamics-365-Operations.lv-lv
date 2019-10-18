---
title: Ļaut lietotājiem saņemt ar darbplūsmu saistītus e-pasta ziņojumus
description: Sistēmu varat konfigurēt tā, lai lietotājiem sūtītu e-pasta ziņojumus, kad notiek ar darbplūsmu saistīti notikumi.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189848"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="06c45-103">Ļaut lietotājiem saņemt ar darbplūsmu saistītus e-pasta ziņojumus</span><span class="sxs-lookup"><span data-stu-id="06c45-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06c45-104">Sistēmu varat konfigurēt tā, lai lietotājiem sūtītu e-pasta ziņojumus, kad notiek ar darbplūsmu saistīti notikumi.</span><span class="sxs-lookup"><span data-stu-id="06c45-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="06c45-105">Piemēram, e-pasta ziņojumus var nosūtīt lietotājiem, ja to apstiprināšanai ir piešķirti dokumenti.</span><span class="sxs-lookup"><span data-stu-id="06c45-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="06c45-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="06c45-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="06c45-107">Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Lietotāji > Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="06c45-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="06c45-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="06c45-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="06c45-109">**Darbību rūtī** noklikšķiniet uz **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="06c45-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="06c45-110">Noklikšķiniet uz cilnes **Darbplūsma**. Pārliecinieties, ka sadaļa **Paziņojumi** ir izvērsta.</span><span class="sxs-lookup"><span data-stu-id="06c45-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="06c45-111">Sadaļā **Paziņojumi** varat norādīt, kā paziņot lietotājam par notikumiem, kas ir saistīti ar darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="06c45-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="06c45-112">Laukā **Rindas vienuma darbplūsmas paziņojuma veids** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="06c45-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="06c45-113">Grupēti — paziņojumi par rindas krājumiem tiek grupēti vienā e-pasta ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="06c45-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="06c45-114">Atsevišķi — e-pasta ziņojums tiek nosūtīts katram rindas krājumam.</span><span class="sxs-lookup"><span data-stu-id="06c45-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="06c45-115">Ja vēlaties, lai lietotājs saņem paziņojumus klientā, tad atzīmējiet izvēles rūtiņu **Sūtīt paziņojumus ar e-pasta ziņojumu**.</span><span class="sxs-lookup"><span data-stu-id="06c45-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="06c45-116">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="06c45-116">Click **Save**.</span></span>
7. <span data-ttu-id="06c45-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="06c45-117">Close the page.</span></span>

