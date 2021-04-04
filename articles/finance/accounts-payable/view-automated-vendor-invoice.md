---
title: Skatīt kreditora rēķina automatizācijas rezultātus (priekšskatījums)
description: Šajā tēmā skaidrots, kā skatīt to kreditoru rēķinu statusu, kas ir iekļauti automatizētajā darbplūsmā iesniegšanas procesā.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b87af4c64f8021a1b23cca5d8f38ac21c8efbd4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248096"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="8b6d5-103">Kreditoru rēķinu automatizācijas rezultātu skatīšana</span><span class="sxs-lookup"><span data-stu-id="8b6d5-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b6d5-104">Šajā tēmā skaidrots, kā skatīt to kreditoru rēķinu statusu, kas ir iekļauti automatizētajā darbplūsmā iesniegšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="8b6d5-105">Detalizēta informācija par automatizācijas vēsturi tiek uzturēta katram importētajam kreditora rēķinam.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="8b6d5-106">Atkarībā no biznesa procesiem, ko esat automatizējuši, lapa **Gaidošie kreditoru rēķini** parāda vērtības **Automatizētās preču ieejas plūsmas atbilstības statuss** un **Automatizētās darbplūsmā iesniegšanas statuss**.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="8b6d5-107">Varat apskatīt detalizētu informāciju un izveidot plānu, lai koncentrētos uz rēķiniem, kam automatizēta darbība bijusi nesekmīga.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="8b6d5-108">Pēc tam, kad esat novērsis problēmu, varat atsākt importētā rēķina automatizēto procesu.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="8b6d5-109">Pirms iesniegta rēķina rediģēšanas, ir jāpārtrauc automātiskā apstrāde.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="8b6d5-110">Ja automatizētajā darbplūsmā iesniegšanas procesā ir jāpārtrauc rēķins, iestatiet lauku **Iekļaut automatizētajā apstrādē** uz **Nē** lapā **Kreditoru rēķini**.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="8b6d5-111">Pēc tam automatizācija netiks palaista, kamēr lauks **Iekļaut automatizētajā apstrādē** netiks iestatīts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="8b6d5-112">Var pārtraukt rēķina turpmāku automatizāciju, ja rēķins vēl nav darbplūsmas sistēmā un netiek izmantots automatizētajā procesā.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="8b6d5-113">Ja importētais rēķins ir pakļauts darbplūsmā iesniegšanas procesam, varat skatīt tā vērtību **Automatizācijas statuss** lapā **Kreditoru rēķini**.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="8b6d5-114">Tālāk minētie statusi tiek izsekoti:</span><span class="sxs-lookup"><span data-stu-id="8b6d5-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="8b6d5-115">**Iekļauts** — automatizētie procesi, kas ir definēti lapā **Kreditoru parametri**, darbojas pareizi, bet vēl nav pabeigti.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="8b6d5-116">**Pārtraukts** — automatizētie procesi, kas ir definēti lapā **Kreditoru parametri**, ir palaisti, bet vismaz viena procesa darbība neizdevās.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="8b6d5-117">Arī statuss **Pārtraukts** tiek piemērots, ja lauks **Iekļaut automatizētajā apstrādē** ir iestatīts uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="8b6d5-118">Varat apskatīt kļūmes, atlasot **Skatīt visjaunākos rezultātus**.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="8b6d5-119">**Darbplūsmā** — importētais rēķins ir iesniegts darbplūsmas sistēmā, vai nu automatizētā darbplūsmā iesniegšanas procesa rezultātā, vai manuāli.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="8b6d5-120">**Darbplūsma pabeigta** — darbplūsmas process importētajam rēķinam ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="8b6d5-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]