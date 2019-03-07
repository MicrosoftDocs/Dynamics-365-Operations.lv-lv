---
title: Personiskie izdevumi un izdevumu pārskats
description: Šajā tēmā ir paskaidrotas divas nodarbinātā personisko izdevumu apstrādes metodes programmā Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6b6c505e7dc5e6544658b00d9f59e6062353608
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "344896"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="04109-103">Personiskie izdevumi attiecīgā izdevumu pārskatā</span><span class="sxs-lookup"><span data-stu-id="04109-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04109-104">Komandējumu laikā var būt reizes, kad darbinieks izmanto uzņēmuma kredītkarti savu personīgo tēriņu segšanai.</span><span class="sxs-lookup"><span data-stu-id="04109-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="04109-105">Ja uzņēmumā nav noteikta kārtība saistībā ar personīgajiem tēriņiem, tad izdevumu pārskatu apstiprināšanas process var aizkavēties pēc darbinieka detalizētas izdevumu atskaites iesniegšanas.</span><span class="sxs-lookup"><span data-stu-id="04109-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="04109-106">Programmā Microsoft Dynamics 365 for Finance and Operations ir pieejamas divas nodarbinātā personisko izdevumu apstrādes metodes.</span><span class="sxs-lookup"><span data-stu-id="04109-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="04109-107">**Apmaksā darbinieks** — jūsu organizācijai nav jāapmaksā personīgie izdevumi, kas tiek parādīti korporatīvās kredītkartes konta izrakstā.</span><span class="sxs-lookup"><span data-stu-id="04109-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="04109-108">Tā vietā, tiek izveidots pārskats, kas parāda personīgos izdevumus kopā ar lietišķajiem izdevumiem, kas veikti ar uzņēmuma kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="04109-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="04109-109">**Apmaksā uzņēmums** — organizācija apmaksā visus izdevumus, kas veikti ar uzņēmuma kredītkarti un tad atvelk no darbinieka konta summu personīgo tēriņu apjomā.</span><span class="sxs-lookup"><span data-stu-id="04109-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="04109-110">Var izvēlēties organizācijas izmantojamo metodi lapā **Izmaksu pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="04109-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
