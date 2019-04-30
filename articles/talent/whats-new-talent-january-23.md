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
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2019. gada 23. janvāris)

[!include [banner](includes/banner.md)]

**8.1.2121 būvējums**

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.

## <a name="changes"></a>Izmaiņas

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>Darbinieku fiksētās atlīdzības imports nedarbojas, izveidojot jaunus fiksētās atlīdzības ierakstus
Ir veiktas izmaiņas darbinieku fiksētās atlīdzības elementam, lai izgūtu atlīdzības līmeni pēc importēšanas. Pirms šī laidiena tika rādīts paziņojums ar norādi, ka līmenis ir obligāts.

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>Minimālās bilances lauka noņemšana no brīvā laika pieprasīšanas dialoglodziņa
Lauks **Minimālā bilance** ir noņemts no dialoglodziņa **Brīvā laika pieprasījums**. Šīs izmaiņas ietekmē visus apgabalus, kuros var pieprasīt brīvo laiku.

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>Datu jaunināšana atlīdzības līmeņiem, kas netiek atjaunināti visos scenārijos
Ir veiktas izmaiņas, lai atjauninātu atlīdzības līmeni fiksētās atlīdzības plānos. Ar šīm izmaiņām tiks aizpildīts atlīdzības līmenis fiksētajos plānos darbam, kas piešķirts attiecīgajam darbiniekam.

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>Algas informācija lapā Pārvaldīt izmaiņas ir pieejama, tikai piesakoties sistēmā kā sistēmas administrators
Šīs izmaiņas ļauj darbiniekiem, kuriem ir loma Algu administrators, piekļūt attiecīgā amata algas informācijai lapā **Izmaiņu laika skala > Pārvaldīt izmaiņas**.

### <a name="job-fields-default-to-positions"></a>Darba laukos pēc noklusējuma tiek iestatīti amati
Mainot darbu amatam, darba laukos pēc noklusējuma tiek iestatīts amats. Tiks parādīts brīdinājuma ziņojums, piedāvājot iespēju apstiprināt noklusējuma vērtības vai saglabāt esošās vērtības attiecīgajos laukos.

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>Turpmāk darbā pieņemtajiem darbiniekiem netiek rādīts izmēģinājuma periods un kalendārs.
Ar šīm izmaiņām lapā **Pārvaldīt izmaiņas** ir pievienoti lauki **Izmēģinājuma periods** un **Kalendārs**, lai nodrošinātu datu ievadi turpmākiem un iepriekšējiem darbiniekiem.

### <a name="platform-update-23"></a>Platform update 23
Atjauninājumā Platform update 23 ir iekļauti nelieli kļūdu labojumi. Plašāku informāciju skatiet tēmā [Jaunumi un izmaiņas programmā Dynamics 365 for Finance and Operations atjauninājumā Platform update 23 (2019. gada janvāris)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23). 
