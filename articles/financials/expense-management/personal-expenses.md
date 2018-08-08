---
title: "Personiskie izdevumi un izdevumu pārskats"
description: "Šajā tēmā izskaidrotas divas darbinieka personisko izdevumu apstrādes metodes risinājumā Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: a6b6c505e7dc5e6544658b00d9f59e6062353608
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="bacf3-103">Personiskie izdevumi un izdevumu pārskats</span><span class="sxs-lookup"><span data-stu-id="bacf3-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bacf3-104">Komandējumu laikā var būt reizes, kad darbinieks izmanto uzņēmuma kredītkarti savu personīgo tēriņu segšanai.</span><span class="sxs-lookup"><span data-stu-id="bacf3-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="bacf3-105">Ja uzņēmumā nav noteikta kārtība saistībā ar personīgajiem tēriņiem, tad izdevumu pārskatu apstiprināšanas process var aizkavēties pēc darbinieka detalizētas izdevumu atskaites iesniegšanas.</span><span class="sxs-lookup"><span data-stu-id="bacf3-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="bacf3-106">Risinājumā Microsoft Dynamics 365 for Finance and Operations ir pieejamas divas darbinieka personisko izdevumu apstrādes metodes.</span><span class="sxs-lookup"><span data-stu-id="bacf3-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="bacf3-107">**Apmaksā darbinieks** — jūsu organizācijai nav jāapmaksā personīgie izdevumi, kas tiek parādīti korporatīvās kredītkartes konta izrakstā.</span><span class="sxs-lookup"><span data-stu-id="bacf3-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="bacf3-108">Tā vietā, tiek izveidots pārskats, kas parāda personīgos izdevumus kopā ar lietišķajiem izdevumiem, kas veikti ar uzņēmuma kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="bacf3-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="bacf3-109">**Apmaksā uzņēmums** — organizācija apmaksā visus izdevumus, kas veikti ar uzņēmuma kredītkarti un tad atvelk no darbinieka konta summu personīgo tēriņu apjomā.</span><span class="sxs-lookup"><span data-stu-id="bacf3-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="bacf3-110">Var izvēlēties organizācijas izmantojamo metodi lapā **Izmaksu pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="bacf3-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>

