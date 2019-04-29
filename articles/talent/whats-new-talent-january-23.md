---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2019. gada 23. janvāris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f27698c257301f52e5c77eaa8a04ca13a0315825
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "859625"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="d868d-103">Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2019. gada 23. janvāris)</span><span class="sxs-lookup"><span data-stu-id="d868d-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d868d-104">**8.1.2121 būvējums**</span><span class="sxs-lookup"><span data-stu-id="d868d-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="d868d-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="d868d-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="d868d-106">Izmaiņas</span><span class="sxs-lookup"><span data-stu-id="d868d-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="d868d-107">Darbinieku fiksētās atlīdzības imports nedarbojas, izveidojot jaunus fiksētās atlīdzības ierakstus</span><span class="sxs-lookup"><span data-stu-id="d868d-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="d868d-108">Ir veiktas izmaiņas darbinieku fiksētās atlīdzības elementam, lai izgūtu atlīdzības līmeni pēc importēšanas.</span><span class="sxs-lookup"><span data-stu-id="d868d-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="d868d-109">Pirms šī laidiena tika rādīts paziņojums ar norādi, ka līmenis ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="d868d-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="d868d-110">Minimālās bilances lauka noņemšana no brīvā laika pieprasīšanas dialoglodziņa</span><span class="sxs-lookup"><span data-stu-id="d868d-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="d868d-111">Lauks **Minimālā bilance** ir noņemts no dialoglodziņa **Brīvā laika pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="d868d-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="d868d-112">Šīs izmaiņas ietekmē visus apgabalus, kuros var pieprasīt brīvo laiku.</span><span class="sxs-lookup"><span data-stu-id="d868d-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="d868d-113">Datu jaunināšana atlīdzības līmeņiem, kas netiek atjaunināti visos scenārijos</span><span class="sxs-lookup"><span data-stu-id="d868d-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="d868d-114">Ir veiktas izmaiņas, lai atjauninātu atlīdzības līmeni fiksētās atlīdzības plānos.</span><span class="sxs-lookup"><span data-stu-id="d868d-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="d868d-115">Ar šīm izmaiņām tiks aizpildīts atlīdzības līmenis fiksētajos plānos darbam, kas piešķirts attiecīgajam darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="d868d-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="d868d-116">Algas informācija lapā Pārvaldīt izmaiņas ir pieejama, tikai piesakoties sistēmā kā sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="d868d-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="d868d-117">Šīs izmaiņas ļauj darbiniekiem, kuriem ir loma Algu administrators, piekļūt attiecīgā amata algas informācijai lapā **Izmaiņu laika skala > Pārvaldīt izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="d868d-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="d868d-118">Darba laukos pēc noklusējuma tiek iestatīti amati</span><span class="sxs-lookup"><span data-stu-id="d868d-118">Job fields default to positions</span></span>
<span data-ttu-id="d868d-119">Mainot darbu amatam, darba laukos pēc noklusējuma tiek iestatīts amats.</span><span class="sxs-lookup"><span data-stu-id="d868d-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="d868d-120">Tiks parādīts brīdinājuma ziņojums, piedāvājot iespēju apstiprināt noklusējuma vērtības vai saglabāt esošās vērtības attiecīgajos laukos.</span><span class="sxs-lookup"><span data-stu-id="d868d-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="d868d-121">Turpmāk darbā pieņemtajiem darbiniekiem netiek rādīts izmēģinājuma periods un kalendārs.</span><span class="sxs-lookup"><span data-stu-id="d868d-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="d868d-122">Ar šīm izmaiņām lapā **Pārvaldīt izmaiņas** ir pievienoti lauki **Izmēģinājuma periods** un **Kalendārs**, lai nodrošinātu datu ievadi turpmākiem un iepriekšējiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="d868d-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="d868d-123">Platform update 23</span><span class="sxs-lookup"><span data-stu-id="d868d-123">Platform update 23</span></span>
<span data-ttu-id="d868d-124">Atjauninājumā Platform update 23 ir iekļauti nelieli kļūdu labojumi.</span><span class="sxs-lookup"><span data-stu-id="d868d-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="d868d-125">Plašāku informāciju skatiet tēmā [Jaunumi un izmaiņas programmā Dynamics 365 for Finance and Operations atjauninājumā Platform update 23 (2019. gada janvāris)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="d868d-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
