---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 18. februāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 18. februāri.
author: andreabichsel
ms.date: 02/18/2020
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
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6c28d0dc76195cc0aedc132f348a229af0421c43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790432"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 18. februāris)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.2903. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="platform-update-32"></a>Platformas update 32 

Platform update 32 tagad ir pieejams. Plašāku informāciju skatiet [Kas jauns vai mainīts Platform update 32 for Finance and Operations lietotnēs (2020. gada februāris)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Meklēšanas vērtības tiek saglabātas, kad tiek mainītas skatījuma opcijas racionalizētajā darbinieku veidlapā (383833)

Jaunā **Darbinieka** veidlapa tagad atceras meklēšanas vērtības, ja maināt skata opcijas un piemērojat izmaiņas.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Atlīdzības pārvaldības kopsavilkuma elementi priekšskatījuma līdzeklī novirza uz nepareizo veidlapu (401861)

Fiksētās un mainīgās atlīdzības pārvaldības elementi tagad rāda pareizos ierakstus jaunajā veidlapā **Darbinieks**. Attiecas tikai uz racionalizētās darbinieku veidlapas priekšskatījuma līdzekli. Varat iespējot šo priekšskatījuma līdzekli **Līdzekļu pārvaldībā**. Papildinformāciju skatiet tēmā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a>Tukša statusa lauks dažiem atvaļinājuma pieprasījumu ierakstiem pakalpojumā Dataverse (414915)

Šī izmaiņa labo Dataverse problēmu, kad **Statusa** lauks atvaļinājuma pieprasījumā ir iestatīts uz **Pārskats**. Dataverse tagad ataino statusu.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Prasmju atbilstību analīze ir iespējama tikai piešķirtajam darbam (411390)

Tagad varat veikt prasmju atbilstību analīzi par jebkuru darbu, kas definēts Human Resources.

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a>Sistēmas valūta netiek sinhronizēta no Dataverse uz Human Resources jaunās vidēs (418011)

Sistēmas valūtu Dataverse tagad var sinhronizēt ar Human Resources.

## <a name="in-preview"></a>Priekšskatījumā

- [Atvaļinājumu un prombūtnes priekšskatījuma līdzekļi](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Atvieglojumu pārvaldības priekšskatījuma līdzekļi](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Drīzumā

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