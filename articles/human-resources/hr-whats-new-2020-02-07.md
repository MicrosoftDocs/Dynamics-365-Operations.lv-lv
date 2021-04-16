---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 7. februāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 7. februāri.
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: adfedbfeb3f4602d0c4d9b8cccec80749eaae2a4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790528"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 7. februāris)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.2835. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>Apmācību analīze neparāda kursu, ja mācību telpa ir tukša (388289)

Lapa apmācības analīze tagad rāda kursu, ja mācību telpa ir tukša.

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>Novietojuma uzmeklēšana neņem vērā laika joslu, ņemot vērā (405344)

Tagad atvērto pozīciju uzmeklēšana tiek ņemta vērā laika zonā, pārbaudot, vai pozīcija ir atvērta.

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>Pašreizējais bilances analīzes skatījums netiek atjaunināts ar pareizu pašreizējo atvaļinājuma bilanci pēc brīvā laika pieprasījumu iesniegšanas (409756)

Pašreizējā bilance tagad ietver iesniegtos brīvā laika pieprasījumus.

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie priekšskatījuma līdzekļi ir pieejami 2020. gada 3. februārī:

- **Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi** – Papildu informāciju skatiet [Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Atvieglojumu pārvaldības priekšskatījums** — plašāku informāciju, ieskaitot zināmās problēmas, skatiet [Atvieglojumu pārvaldības apskatā](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Drīzumā

### <a name="platform-update-32"></a>Platformas update 32 

Platformas update 32 būs pieejams drīzumā. [Skatiet papildinformāciju par Platform update 32 šeit](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

### <a name="updated-dataverse-solution"></a>Atjaunināts Dataverse risinājums

Jauns Dataverse risinājums drīzumā būs pieejams ar šādām izmaiņām:

| Apraksts | Labot |
| ----------------------------------------- | --- |
| **Darba/amata** elementa izmaiņas | **Kompensācijas reģions** pievienots</br>**Finanšu dimensijas** pievienotas |
| **Darbinieka** elementa izmaiņas | **Vārdu secība** pievienota</br>**Darbi no mājām** pievienoti</br>**Valoda** pievienota</br>**Darba stāža datums** pievienots</br>**Gadadienas datums** pievienots</br>**Sākotnējais darbā pieņemšanas datums** pievienots |
| **Nodarbinātības** elementa izmaiņas | **Finanšu dimensijas** pievienotas</br>**Darba attiecību pārtraukšanas pamatojums** pievienots</br>**Beigu datums** pārdēvēts no **Pārejas datuma**</br>**Probācijas datums** pievienots |
| **Darbinieka adreses** elementa izmaiņas | **Adrese** pievienota</br>**1. adreses rinda**, **2. adreses rinda** un **3. adreses rinda** atzīmēta norakstīšanai |
| Jaunas mainīgās atlīdzības iestatījuma entitījas | **Atlīdzības mainīgā plāna tips**</br>**Atlīdzības mainīgā sistēma**</br>**Izmaksas noteikumi**</br>**Atlīdzības mainīgā plāna līmenis** |
| Jauna **Darbinieka kalendāra nodarbinātības** entitīja | **Darba kalendāra elements** pievienots |
| Jauna **Algas pozīcijas detalizētas informācijas** entitīja | **Algas pozīcijas detalizēta informācija** pievienota |
| Jauna **Nosaukuma** entitīja | **Nosaukums** pievienots. Jaunais elements **Nosaukums** tiks iekļauts sinhronizācijas procesā starp Human Resources un Dataverse. Tam nebūs sākotnējas atsauces no entitījām **Amats** vai **Darbs**. |

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]