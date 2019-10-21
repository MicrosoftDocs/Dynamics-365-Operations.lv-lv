---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2019. gada 11. janvāris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
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
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38be1da69d8443fd76a81f439f000602ddb75bab
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010387"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-january-11-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent: Core HR (2019. gada 11. janvāris)

[!include [banner](includes/banner.md)]

**8.1.2100 būvējums**

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.

## <a name="changes"></a>Izmaiņas

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Atvaļinājuma pieprasījumu pārbaude, prognozējot pieejamo bilanci
Izmaiņas, kas veiktas šajā laidienā, ļauj darbiniekiem pieprasīt turpmāko atvaļinājumu, neatņemot to no pašreizējās bilances. Visiem turpmākajiem pieprasījumiem tiks izmantotas standarta darbplūsmas. Lai iegūtu plašāku informāciju, lasiet tēmu [Brīvā laika uzkrāšana, pamatojoties uz nostrādātajām stundām](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Prognozētās atvaļinājuma bilances skatīšana darbvietā ESS un Personas
Šis līdzeklis ļauj skatīt bilanci turpmākajiem atvaļinājuma periodiem personāla vadības darbiniekiem, vadītājiem un darbiniekiem. Darbinieki var skatīt turpmāko bilanci darbvietā **Darbinieku pašapkalpošanās**, un personāla vadības darbiniekiem ir piekļuve tai pašai informācijai, izmantojot darbvietu **Personas**.

### <a name="notifications-for-changing-leave-balances"></a>Paziņojumi par atvaļinājuma bilances izmaiņām
Atvaļinājuma bilancē tiks parādīta darbinieka pašreizējā bilance. Turpmākā bilance ir pieejama darbvietās **Darbinieku pašapkalpošanās** un **Personas**, ievadot “datumu”, lai aprēķinātu prognozēto bilanci.

Ir pievienota navigācija, lai skatītu prognozēto bilanci šādos apgabalos:
  - Kartīte **Prombūtne** darbvietā **Darbinieku pašapkalpošanās**.
  - Kartīte **Atvaļinājumi un kavējumi** darbvietā **Vadītāju pašapkalpošanās**.
  - Lapa **Atvaļinājumi un kavējumi** darbvietā **Personas**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Atļaut decimāldaļas mainīgās atlīdzības plāniem (skaidras naudas plāni)
Mainīgām skaidras naudas piemaksām un plāniem tagad ir papildu elastība attiecībā uz summām un pārlabošanu vērtībām ar decimāldaļām.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Nevar mainīt datumus mainīgās atlīdzības reģistrācijām pēc plāna saglabāšanas
Šīs izmaiņas ļauj atjaunināt plāna beigu datumu (pagarināts vai beidzies derīguma termiņš) pēc plāna saglabāšanas. Plānu joprojām var aktivizēt vai deaktivizēt neatkarīgi no sākuma un beigu datuma.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Algas informācija, kas pieejama, piešķirot drošības lomu Algu administrators
Loma Algu administrators ir atjaunināta, lai tai būtu piekļuve algu informācijai pieprasījuma procesa laikā.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Darbinieku pašapkalpošanās | Amatu hierarhijas detalizētas rādīšanas rezultātā no elementa neizdodas iegūt pamatzaru
Ir veiktas izmaiņas, lai novērstu kļūdu, kas radās, pievienojot amatu hierarhiju jaunām darbvietām un pārvietojoties organizācijas struktūrā.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Jauns pārbaudes ziņojums, kad personāla numuru sērija tiek lietota
Ir veiktas izmaiņas, lai precizētu problēmu, ja pieņemat darbā darbinieku un nākamais personāla numurs tiek lietots.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Darbvieta Darbinieku pašapkalpošanās atlasīta kā pirmā startēšanas lapa
Ja darbvieta **Darbinieku pašapkalpošanās** ir atlasīta kā lietotāja pirmā startēšanas lapa un šim lietotājam nav piešķirta darbinieka loma, sistēma veiks novirzīšanu uz noklusējuma informācijas paneli.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Darba attiecību pārtraukšanas iemesla kods atjaunina amatu piešķires ierakstu
Darba attiecību pārtraukšanas iemesla kods tagad atjaunina amata piešķiri, pārtraucot darba saistības ar darbinieku un beidzot amata piešķiri. 
