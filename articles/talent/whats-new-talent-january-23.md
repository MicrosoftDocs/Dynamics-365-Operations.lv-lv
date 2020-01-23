---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2019. gada 23. janvāris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
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
ms.openlocfilehash: f97462f088fc1a3cb94f2a34204fc09f1cd66fb0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899132"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-23-2019"></a><span data-ttu-id="fe9ca-103">Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2019. gada 23. janvāris)</span><span class="sxs-lookup"><span data-stu-id="fe9ca-103">What's new or changed in Dynamics 365 Talent - Core HR (January 23, 2019)</span></span>

<span data-ttu-id="fe9ca-104">**8.1.2121 būvējums**</span><span class="sxs-lookup"><span data-stu-id="fe9ca-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="fe9ca-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="fe9ca-106">Izmaiņas</span><span class="sxs-lookup"><span data-stu-id="fe9ca-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="fe9ca-107">Darbinieku fiksētās atlīdzības imports nedarbojas, izveidojot jaunus fiksētās atlīdzības ierakstus</span><span class="sxs-lookup"><span data-stu-id="fe9ca-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="fe9ca-108">Ir veiktas izmaiņas darbinieku fiksētās atlīdzības elementam, lai izgūtu atlīdzības līmeni pēc importēšanas.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="fe9ca-109">Pirms šī laidiena tika rādīts paziņojums ar norādi, ka līmenis ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="fe9ca-110">Minimālās bilances lauka noņemšana no brīvā laika pieprasīšanas dialoglodziņa</span><span class="sxs-lookup"><span data-stu-id="fe9ca-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="fe9ca-111">Lauks **Minimālā bilance** ir noņemts no dialoglodziņa **Brīvā laika pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="fe9ca-112">Šīs izmaiņas ietekmē visus apgabalus, kuros var pieprasīt brīvo laiku.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="fe9ca-113">Datu jaunināšana atlīdzības līmeņiem, kas netiek atjaunināti visos scenārijos</span><span class="sxs-lookup"><span data-stu-id="fe9ca-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="fe9ca-114">Ir veiktas izmaiņas, lai atjauninātu atlīdzības līmeni fiksētās atlīdzības plānos.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="fe9ca-115">Ar šīm izmaiņām tiks aizpildīts atlīdzības līmenis fiksētajos plānos darbam, kas piešķirts attiecīgajam darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="fe9ca-116">Algas informācija lapā Pārvaldīt izmaiņas ir pieejama, tikai piesakoties sistēmā kā sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="fe9ca-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="fe9ca-117">Šīs izmaiņas ļauj darbiniekiem, kuriem ir loma Algu administrators, piekļūt attiecīgā amata algas informācijai lapā **Izmaiņu laika skala > Pārvaldīt izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="fe9ca-118">Darba laukos pēc noklusējuma tiek iestatīti amati</span><span class="sxs-lookup"><span data-stu-id="fe9ca-118">Job fields default to positions</span></span>
<span data-ttu-id="fe9ca-119">Mainot darbu amatam, darba laukos pēc noklusējuma tiek iestatīts amats.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="fe9ca-120">Tiks parādīts brīdinājuma ziņojums, piedāvājot iespēju apstiprināt noklusējuma vērtības vai saglabāt esošās vērtības attiecīgajos laukos.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="fe9ca-121">Turpmāk darbā pieņemtajiem darbiniekiem netiek rādīts izmēģinājuma periods un kalendārs.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="fe9ca-122">Ar šīm izmaiņām lapā **Pārvaldīt izmaiņas** ir pievienoti lauki **Izmēģinājuma periods** un **Kalendārs**, lai nodrošinātu datu ievadi turpmākiem un iepriekšējiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23-for-finance-and-operations"></a><span data-ttu-id="fe9ca-123">Finance and Operations Platform update 23</span><span class="sxs-lookup"><span data-stu-id="fe9ca-123">Platform update 23 for Finance and Operations</span></span>
<span data-ttu-id="fe9ca-124">Atjauninājumā Finance and Operations Platform update 23 ir iekļauti nelieli kļūdu labojumi.</span><span class="sxs-lookup"><span data-stu-id="fe9ca-124">Minor bug fixes have been included as part of Platform update 23 for Finance and Operations.</span></span> <span data-ttu-id="fe9ca-125">Plašāku informāciju skatiet tēmā [Jaunumi un izmaiņas programmā Dynamics 365 Finance and Operations atjauninājumā Platform update 23 (2019. gada janvāris)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="fe9ca-125">For more information, see [What's new or changed in Dynamics 365 Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
