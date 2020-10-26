---
title: Skatīt kreditora rēķina automatizācijas rezultātus (priekšskatījums)
description: Šajā tēmā skaidrots, kā skatīt to kreditoru rēķinu statusu, kas ir iekļauti automatizētajā darbplūsmā iesniegšanas procesā.
author: abruer
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 65e7929e612c8465f26a2f3bc7df6f13620e5b4e
ms.sourcegitcommit: 3387595e41fb03e98bb437588f6de78794ae383f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930947"
---
# <a name="view-vendor-invoice-automation-results-preview"></a><span data-ttu-id="8317c-103">Skatīt kreditora rēķina automatizācijas rezultātus (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="8317c-103">View vendor invoice automation results (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8317c-104">Šajā tēmā skaidrots, kā skatīt to kreditoru rēķinu statusu, kas ir iekļauti automatizētajā darbplūsmā iesniegšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="8317c-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="8317c-105">Detalizēta informācija par automatizācijas vēsturi tiek uzturēta katram importētajam kreditora rēķinam.</span><span class="sxs-lookup"><span data-stu-id="8317c-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="8317c-106">Atkarībā no biznesa procesiem, ko esat automatizējuši, lapa **Gaidošie kreditoru rēķini** parāda vērtības **Automatizētās preču ieejas plūsmas atbilstības statuss** un **Automatizētās darbplūsmā iesniegšanas statuss**.</span><span class="sxs-lookup"><span data-stu-id="8317c-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="8317c-107">Varat apskatīt detalizētu informāciju un izveidot plānu, lai koncentrētos uz rēķiniem, kam automatizēta darbība bijusi nesekmīga.</span><span class="sxs-lookup"><span data-stu-id="8317c-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="8317c-108">Pēc tam, kad esat novērsis problēmu, varat atsākt importētā rēķina automatizēto procesu.</span><span class="sxs-lookup"><span data-stu-id="8317c-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="8317c-109">Pirms iesniegta rēķina rediģēšanas, ir jāpārtrauc automātiskā apstrāde.</span><span class="sxs-lookup"><span data-stu-id="8317c-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="8317c-110">Ja automatizētajā darbplūsmā iesniegšanas procesā ir jāpārtrauc rēķins, iestatiet lauku **Iekļaut automatizētajā apstrādē** uz **Nē** lapā **Kreditoru rēķini**.</span><span class="sxs-lookup"><span data-stu-id="8317c-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="8317c-111">Pēc tam automatizācija netiks palaista, kamēr lauks **Iekļaut automatizētajā apstrādē** netiks iestatīts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8317c-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="8317c-112">Var pārtraukt rēķina turpmāku automatizāciju, ja rēķins vēl nav darbplūsmas sistēmā un netiek izmantots automatizētajā procesā.</span><span class="sxs-lookup"><span data-stu-id="8317c-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="8317c-113">Ja importētais rēķins ir pakļauts darbplūsmā iesniegšanas procesam, varat skatīt tā vērtību **Automatizācijas statuss** lapā **Kreditoru rēķini**.</span><span class="sxs-lookup"><span data-stu-id="8317c-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="8317c-114">Tālāk minētie statusi tiek izsekoti:</span><span class="sxs-lookup"><span data-stu-id="8317c-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="8317c-115">**Iekļauts** — automatizētie procesi, kas ir definēti lapā **Kreditoru parametri**, darbojas pareizi, bet vēl nav pabeigti.</span><span class="sxs-lookup"><span data-stu-id="8317c-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="8317c-116">**Pārtraukts** — automatizētie procesi, kas ir definēti lapā **Kreditoru parametri**, ir palaisti, bet vismaz viena procesa darbība neizdevās.</span><span class="sxs-lookup"><span data-stu-id="8317c-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="8317c-117">Arī statuss **Pārtraukts** tiek piemērots, ja lauks **Iekļaut automatizētajā apstrādē** ir iestatīts uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="8317c-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="8317c-118">Varat apskatīt kļūmes, atlasot **Skatīt visjaunākos rezultātus**.</span><span class="sxs-lookup"><span data-stu-id="8317c-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="8317c-119">**Darbplūsmā** — importētais rēķins ir iesniegts darbplūsmas sistēmā, vai nu automatizētā darbplūsmā iesniegšanas procesa rezultātā, vai manuāli.</span><span class="sxs-lookup"><span data-stu-id="8317c-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="8317c-120">**Darbplūsma pabeigta** — darbplūsmas process importētajam rēķinam ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="8317c-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>
