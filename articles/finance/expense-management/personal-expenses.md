---
title: Personiskie izdevumi un izdevumu pārskats
description: Šajā tēmā ir paskaidrotas divas nodarbinātā personisko izdevumu apstrādes metodes programmā Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178839"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="7ed58-103">Personiskie izdevumi attiecīgā izdevumu pārskatā</span><span class="sxs-lookup"><span data-stu-id="7ed58-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ed58-104">Komandējumu laikā var būt reizes, kad darbinieks izmanto uzņēmuma kredītkarti savu personīgo tēriņu segšanai.</span><span class="sxs-lookup"><span data-stu-id="7ed58-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="7ed58-105">Ja uzņēmumā nav noteikta kārtība saistībā ar personīgajiem tēriņiem, tad izdevumu pārskatu apstiprināšanas process var aizkavēties pēc darbinieka detalizētas izdevumu atskaites iesniegšanas.</span><span class="sxs-lookup"><span data-stu-id="7ed58-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="7ed58-106">Ir pieejamas divas nodarbinātā personisko izdevumu apstrādes metodes.</span><span class="sxs-lookup"><span data-stu-id="7ed58-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="7ed58-107">**Apmaksā darbinieks** — jūsu organizācijai nav jāapmaksā personīgie izdevumi, kas tiek parādīti korporatīvās kredītkartes konta izrakstā.</span><span class="sxs-lookup"><span data-stu-id="7ed58-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="7ed58-108">Tā vietā, tiek izveidots pārskats, kas parāda personīgos izdevumus kopā ar lietišķajiem izdevumiem, kas veikti ar uzņēmuma kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="7ed58-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="7ed58-109">**Apmaksā uzņēmums** — organizācija apmaksā visus izdevumus, kas veikti ar uzņēmuma kredītkarti un tad atvelk no darbinieka konta summu personīgo tēriņu apjomā.</span><span class="sxs-lookup"><span data-stu-id="7ed58-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="7ed58-110">Var izvēlēties organizācijas izmantojamo metodi lapā **Izmaksu pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="7ed58-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
