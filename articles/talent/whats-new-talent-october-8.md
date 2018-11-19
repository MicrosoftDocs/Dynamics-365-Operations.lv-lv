---
title: "Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 1. oktobris)"
description: "Šajā tēmā ir aprakstīti līdzekļi, kas ir jauni vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 657c19896b20a514dc5308bf7fb086085b482fec
ms.openlocfilehash: 92eb1508905309294e17b770829b1c5a22be1316
ms.contentlocale: lv-lv
ms.lasthandoff: 10/08/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="1dd89-103">Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 8. oktobris)</span><span class="sxs-lookup"><span data-stu-id="1dd89-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1dd89-104">**8.1.1050.0 būvējums**</span><span class="sxs-lookup"><span data-stu-id="1dd89-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="1dd89-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="1dd89-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="1dd89-106">Ļaušana atvaļinājuma pakāpes bāzei izmantot citus datumus (atvaļinājumu pārvaldība)</span><span class="sxs-lookup"><span data-stu-id="1dd89-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="1dd89-107">Piešķirot darbiniekiem atvaļinājumu, piemaksas pakāpes bāze nosaka, cik daudz brīvā laika darbinieks uzkrāj.</span><span class="sxs-lookup"><span data-stu-id="1dd89-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="1dd89-108">Pašlaik šīs pakāpes ir balstītas uz darbinieka sākuma datumu un darba stāža datumu.</span><span class="sxs-lookup"><span data-stu-id="1dd89-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="1dd89-109">Noteiktos scenārijos organizācijām ir nepieciešams, lai šīs pakāpes būtu balstītas uz citiem datumiem, piemēram, uz gadadienas datumu vai sākotnējās darbā pieņemšanas datumu.</span><span class="sxs-lookup"><span data-stu-id="1dd89-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="1dd89-110">Šie datumi jau tiek izmantoti atvaļinājumu plānā, lai noteiktu, kad tiek veikti uzkrājumi, un tagad ir pievienota iespēja šos pašus datumus izmantot, kad darbinieks tiek reģistrēts kādā plānā, lai noteiktu uzkrājuma summu.</span><span class="sxs-lookup"><span data-stu-id="1dd89-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="1dd89-111">Cita izmaiņas</span><span class="sxs-lookup"><span data-stu-id="1dd89-111">Other changes</span></span>
<span data-ttu-id="1dd89-112">Šajā laidienā ir ietverti dažādi labojumi.</span><span class="sxs-lookup"><span data-stu-id="1dd89-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="1dd89-113">Zināma problēma</span><span class="sxs-lookup"><span data-stu-id="1dd89-113">Known issue</span></span>

<span data-ttu-id="1dd89-114">**Problēma:** pievienojot nodarbinātajam jaunu pielikumu, tiek deaktivizēta poga **Jauns** un **Rediģēt**. **Risinājums:** pirms pielikuma lapas atvēršanas pārbaudiet, vai lapā **Nodarbinātais** ir aizvērta papildinformācija.</span><span class="sxs-lookup"><span data-stu-id="1dd89-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="1dd89-115">Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas.</span><span class="sxs-lookup"><span data-stu-id="1dd89-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="1dd89-116">(Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)</span><span class="sxs-lookup"><span data-stu-id="1dd89-116">(This issue will be fixed in the next platform update.)</span></span>

