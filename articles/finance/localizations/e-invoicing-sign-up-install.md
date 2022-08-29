---
title: Reģistrēties elektronisko rēķinu izrakstīšanas pakalpojumā un instalēt to
description: Šajā rakstā ir sniegta informācija, kā pierakstīties uz elektronisko rēķinu izrakstīšanas pakalpojumu un to instalēt.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283963"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Reģistrēties elektronisko rēķinu izrakstīšanas pakalpojumā un instalēt to

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija, kā pierakstīties uz elektronisko rēķinu izrakstīšanas pakalpojumu un to instalēt. Šim procesam ir četri soļi. Ir jāveic 1. līdz 3. darbība, un 4. solis nav obligāts.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>1. darbība: pierakstīšanās regulēšanas konfigurācijas pakalpojumā

Regulēšanas konfigurācijas pakalpojums (RCS) nodrošina konfigurācijas un dizaina pieredzi, kas tiek izmantota elektronisko rēķinu konfigurēšanai. Resursi, piemēram, vides un elektronisko rēķinu izrakstīšanas līdzekļi, tiek izveidoti, uzturēti un pārvaldīti RCS. Kad resursi ir gatavi, tie tiek publicēti Elektronisko rēķinu izrakstīšanas pakalpojumā.

Papildinformāciju par RCS skatiet regulēšanas [konfigurācijas pakalpojumi (RCS) — globalizācijas līdzekļi](rcs-globalization-feature.md).

Lai pierakstītos uz RCS, dodieties uz lapu [Regulēšanas konfigurācijas](https://marketing.configure.global.dynamics.com/) pakalpojums.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>2. darbība: mikropakāpju pievienojumprogrammas instalēšana pakalpojumos Microsoft Dynamics Lifecycle Services

Elektronisko rēķinu izrakstīšanas pakalpojums ir mikropakoņu kopa, kas tiek viesota Microsoft datacenters. Pēc noklusējuma Dynamics 365 finanšu debitoriem Dynamics 365 Supply Chain Management nav piekļuves elektronisko rēķinu izrakstīšanas pakalpojumam. Jums tā ir jāinstalē kā pievienojumprogramma programmā Microsoft Dynamics Lifecycle Services (LCS). Kad instalējat pievienojumprogrammu, finanšu vai piegādes ķēdes pārvaldības vide tiek reģistrēta to programmu reģistrā, kurām ir atļauts izveidot savienojumu ar Elektronisko rēķinu izrakstīšanas pakalpojumu.

Lai veiktu šo darbību, skatiet [programmu Programmu Lifecycle Services pievienojumprogrammu pakalpojumam Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>3. darbība: RCS iestatīšana

Ir jāiestata integrācija starp RCS un Elektronisko rēķinu izrakstīšanas pakalpojumu. Ir jāiestata arī galvenie komponenti.

Lai pabeigtu šo darbību, skatiet [iestatīt regulēšanas konfigurācijas pakalpojumu (RCS).<a1/&](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>4. solis: Microsoft Power Platform spraudņa administratora atsauce

Dažiem scenārijiem nepieciešama integrācija Dataverse darbības jomā Microsoft Power Platform.

Šis iestatījums ir obligāts, ja Indonēzijas elektronisko rēķinu izrakstīšanas scenārijiem izmantosit elektronisko rēķinu izrakstīšanas risinājumus. Tomēr, tas ir obligāts Saūda Arābijas elektronisko rēķinu izrakstīšanas scenārijiem. Papildinformāciju skatiet sadaļā [Elektronisko rēķinu izrakstīšanas līdzekļu pieejamība pēc valsts vai reģiona](e-invoicing-country-specific-availability.md).

Lai pabeigtu šo darbību, skatiet [Microsoft Power Platform spraudņa administratora atsauci](e-invoicing-power-platform-plug-in.md).
