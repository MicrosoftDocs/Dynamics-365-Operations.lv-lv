---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2020. gada 21. janvāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528126"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2020. gada 21. janvāris)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract. Esam Attract pievienojuši funkcionalitāti, lai atbalstītu mūsu neseno paziņojumu [Veidojot veiksmīgāku darbaspēku ar Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>Vides datu lejupielāde

Administratori var lejupielādēt savus vides datus. Dati tiek eksportēti standarta JSON formātā ar visiem darbiem, kandidātiem un konfigurāciju, kas eksportēta ZIP failā. Papildinformāciju skatiet sadaļā [Datu eksportēšana no Attract un Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Piekļuves ierobežošana vidēm lietotājiem, kas nav administratori

Administratori tagad var ierobežot piekļuvi videi lietotājiem, kas nav administratori. Šo darbību nevar atsaukt. Papildinformāciju skatiet tēmā [Ierobežot piekļuvi Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>Pievienošanās ceļvežu eksportēšana

Lietotāji tagad var eksportēt visus savus pievienošanās ceļvežus un pievienošanās veidnes Word dokumenta formātā. Papildinformāciju skatiet sadaļā [Datu eksportēšana no Attract un Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2726. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Pēdējā gada atlīdzības lauks Nodarbinātības pārbaudes veidlapā neatbilst (392092)

Šajā laidienā ir iekļautas izmaiņas, kas pastāvīgi attēlos pēdējo valūtu, pamatojoties uz uzņēmuma atlasītāju veidlapā **Pārbaudīt nodarbinātību**.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Zināms kā lauks, kas pievienots atsauksmes saņēmēja meklēšanai (407789)

Sniedzot veiktspējas atsauksmes, informācijas meklēšana darbiniekiem nesniedz pietiekamu informāciju, lai noteiktu, vai atgriezeniskā saite nonākusi pie pareizās personas. Pievienojām kolonnu **Zināms kā**, lai palīdzētu identificēt darbinieka unikālo vārdu.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo ieraksts tiek izveidots bez saistības ar darbinieku (394526)

Šajā laidienā ir iekļautas izmaiņas nerakstīt HCMWorkerPayrollInfo ierakstus bez atsauces uz darbinieku.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Var rediģēt nodaļu, pārvietojoties no pozīciju hierarhijas (341001)

Ja drošība ir iestatīta tā, lai liegtu piekļuvi rediģēšanas nodaļām, labošana ir atspējota, pārvietojoties uz veidlapu **Nodaļas** visos scenārijos.

## <a name="coming-soon"></a>Drīzumā

Jauns Common Data Service risinājums drīzumā būs pieejams ar šādām izmaiņām:

| Apraksts | Labot |
| --- | --- |
| **Darba/amata** elementa izmaiņas | <ul><li>**Kompensācijas reģions** pievienots</li><li>**Finanšu dimensijas** pievienotas</li></ul> |
| **Darbinieka** elementa izmaiņas | <ul><li>**Vārdu secība** pievienota</li><li>**Darbi no mājām** pievienoti</li><li>**Valoda** pievienota</li><li>**Darba stāža datums** pievienots</li><li>**Gadadienas datums** pievienots</li><li>**Sākotnējais darbā pieņemšanas datums** pievienots</li></ul> |
| **Nodarbinātības** elementa izmaiņas | <ul><li>**Finanšu dimensijas** pievienotas</li><li>**Darba attiecību pārtraukšanas pamatojums** pievienots</li><li>**Beigu datums** pārdēvēts no **Pārejas datuma**</li><li>**Probācijas datums** pievienots</li></ul> |
| **Darbinieka adreses** elementa izmaiņas | <ul><li>**Adrese** pievienota</li><li>**1. adreses rinda**, **2. adreses rinda** un **3. adreses rinda** atzīmēta norakstīšanai</li></ul> |
| Jaunas mainīgās atlīdzības iestatījuma entitījas | <ul><li>**Atlīdzības mainīgā plāna tips**</li><li>**Atlīdzības mainīgā sistēma**</li><li>**Izmaksas noteikumi**</li><li>**Atlīdzības mainīgā plāna līmenis**</li></ul> |
| Jauna **Darbinieka kalendāra nodarbinātības** entitīja | <ul><li>**Darba kalendāra elements** pievienots</li></ul> |
