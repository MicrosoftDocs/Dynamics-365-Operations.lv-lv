---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 10. septembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0aadecd5b37759492f7895ccfda1a777793a08b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461869"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 10. septembris)

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

### <a name="candidate-e-mail-login"></a>Kandidāta e-pasta pieteikšanās

Kandidāti tagad var izmantot jebkuru e-pasta adresi, lai izveidotu kontu un pieteikties karjeras vietnē Talent, lai pieteiktos darbiem un pārbaudīt viņu pieteikuma statusu. Tas ir papildus tam, ka jau ir iespējams pieteikties karjeras vietnei Talent, izmantojot savu sociālo kontu vai savas organizācijas akreditācijas datus.

### <a name="job-activation-and-posting"></a>Darbu aktivizēšana un izlikšana

Ir veiktas dažas izmaiņas darbu aktivizācijai un izlikšanai. Jums ir jāaktivizē darbi pirms to izlikšanas talantu karjeras vietnē vai jebkuras ārējiem darbu izlikšanas vietās, tostarp LinkedIn vai Broadbean.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2482. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Jūs varat iespējot priekšskatījuma līdzekļus smilškastes un izmēģinājuma vidē

Kad nodrošināt jaunu Talent instanci, varat norādīt, vai šīs instances tips ir Ražošana vai Smilškaste. Instances, kuru tips ir Smilškaste, ļauj agri testēt jaunos līdzekļus. Ja vēlaties, lai kāda no jūsu esošajām instancēm tiktu atjaunināta uz instances tipu Smilškaste, sazinieties ar atbalsta dienestu, lai sāktu izmaiņu pieprasījumu.

Papildinformāciju par to, kā tiek publicētas izmaiņas, skatiet tēmā [Talent nodrošinājums](./provisioning-talent.md).

### <a name="platform-update-29"></a>Platformas update 29

Papildinformāciju par atjauninājumu Platform update 29 skatiet rakstā [Priekšskatījuma līdzekļi versijā Dynamics 365 for Finance and Operations Platform update 29 (2019. gada oktobris)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Jauns darba pamatelements ir pieejams datu pārvaldības struktūrā (347202)

Ar šo laidienu, datu importēšanai/eksportēšanai ir pieejama jauna pamata darba vienība. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Darbinieku uzlabotā drošības politika nepareizi rāda pozīcijas Pozīciju hierarhijā (354868)

Ar šo laidienu, pozīcijas vairs netiek atvērtas ar "tukšu" darbinieku, ja lietotājiem ir ierobežota piekļuve.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Darba formas slēgšanas lodziņš neaizvērs formu noteiktās situācijās (342467)

Šajā laidienā ietilpst izmaiņas, kas ļauj darba formai slēgt visus scenārijus.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Jauns pieteikums darbinieka ierakstā ir bloķēts personāla vadības vadītāja lomai (337111)

Ar šo izmaiņu, kad piekļūstat no darbinieka formas, pieteikumu pārvaldības forma vairs netiek bloķēta.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Nodarbinātības beigu datums vienmēr pēc noklusējuma ir 23:59:59 (351492)

Ar šo izmaiņu, jūs varat mainīt nodarbinātības datumu uz laiku, citu nekā 23:59:59, manuāli pabeidzot darbu.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Nevar iestatīt beiguma datumu ienākumu veida kodam, izmantojot Datu pārvaldību (336604)

Šajā laidienā varat iestatīt ienākumu veida kodus, kas beidzas ar **PayrollWorkerPositionEarningCodeEntity** elementu.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Darbinieku attīstības analītiskajā pārskatā netiek rādīti dati (348737)

Šīs nedēļas laidienā darbinieku prasmju analīze ir atjaunināta, lai nodrošinātu precīzu pārskatu veidošanu.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Nodarbinātības noteikumu datums/laiks nav pēc noklusējuma dienas sākums (349101)

Ar šīm izmaiņām, sākuma datums/laiks pēc noklusējuma tiek nomainīts uz dienas sākumu un beigu datums/laiks pēc noklusējuma tiek nomainīts uz dienas beigām.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Nodarbinātības beigu datuma maiņas laikā Darbinieka darbības veidlapā parādas kļūda (354092) 

Šī izmaiņa labo problēmu, kas parādas, modificējot nodarbinātības beigu datumu kā daļu no darbinieka darbības.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Pievienojamo kontrolsarakstu izmantošana uzņēmumiem (338433)

Šis laidiens tagad sniedz iespēju piemērot kontrolsarakstus darbiniekiem, kas ir nodarbināti kā juridiskās personas, bet kas nav pierakstījušās juridiskās personas.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="streamlined-employee-entry-and-navigation"></a>Racionalizēta darbinieku ievade un navigācija

Šī funkcionalitāte tagad ir pieejama smilškastes vidē. Lai ieslēgtu šo līdzekli, dodieties uz **Sistēmas administrēšana > Saites > Iestatīšana > Sistēmas parametri > Priekšskatījuma līdzekļi**. Atlasiet **Uzlabotā darbinieka veidlapa un navigācija**. Tas ļaus iespējot šīs izmaiņas visiem lietotājiem. Šo opciju varat izslēgt jebkurā laikā.

Papildinformāciju skatiet rakstā [Racionalizēts darbinieka ieraksts un navigācija](./streamlined-employee-entry.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]