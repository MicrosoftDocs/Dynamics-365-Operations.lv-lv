---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 25. februāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 720b4e03549a059c8945bec9d27de9cdcaada488
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092756"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 25. februāris)

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.2927. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Iespējot pieteikumu pārvaldības navigācijas un datu pārvaldības struktūras (DMF) elementu (414754)

Šis priekšskatījuma līdzeklis iespējo papildu navigāciju lietu pārvaldības gadījumos. Varat iespējot šo priekšskatījuma līdzekli darbvietā **Līdzekļu pārvaldība**. Šie izvēlnes elementi tiek rādīti Dynamics 365 Human Resources **Atbilstības** darbvietā. Ar šīm izmaiņām Personāla vadība var piekļūt:

- Visi pieteikumi
- Mani pieteikumi
- Mani atvērtie pieteikumi
- Mani nokavētie pieteikumi
- Darbplūsmā man piešķirtie pieteikumi

Kopā ar šiem jaunajiem skatiem gadījumos ir pieejams arī **Gadījuma detaļas** DMF elements.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Iespējojiet Attiecību definīcijas globālajā adrešu bBook (414762)

Attiecības tagad ir iespējotas globālajā adrešu grāmatā. Pirms šīs nedēļas izlaišanas **Attiecības** fakta lodziņš parāda visas sistēmas definētās attiecības. Tagad varat definēt šīs attiecības globālās adrešu grāmatas lapā.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>Pozīciju var noņemt, ja pozīcijai pastāv aktīvie kompensācijas ieraksti (414568)

Ar šīm izmaiņām tiek parādīts brīdinājums, ja mēģināt dzēst amatu, un nodarbinātajam ir aktīvs kompensācijas ieraksts tai pašai pozīcijai. Ja tā notiek, pirms amata noņemšanas ir jāatjaunina darbinieka fiksētās atlīdzības ieraksts.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Veiktspējas pārskata darbplūsma reizēm pievieno parakstīšanās no cilvēkiem, kuri nav procesa daļa (414171)

Šīs izmaiņas labo problēmu, kad papildu parakstīšanās dalībnieki ir pievienoti veiktspējas pārskatam.

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a>Nodarbinātā amata piešķire netiek veidota Common Data Service, kad tas tiek atlasīts dialoglodziņā Jauns nodarbināmais (413479)

Šī izmaiņa labo problēmu, kurā nolīgst jaunu nodarbināto un piešķir to pozīcijai, izmantojot dialoglodziņu **Jauns nodarbinātais**. Tagad pozīcijas piešķire tiek atainota Common Data Service.

## <a name="coming-soon"></a>Drīzumā

### <a name="updated-common-data-service-solution"></a>Atjaunināts Common Data Service risinājums

Jauns Common Data Service risinājums drīzumā būs pieejams ar šādām izmaiņām:

| Apraksts | Labot |
| ----------------------------------------- | --- |
| **Darba/amata** elementa izmaiņas | **Kompensācijas reģions** pievienots</br>**Finanšu dimensijas** pievienotas |
| **Darbinieka** elementa izmaiņas | **Vārdu secība** pievienota</br>**Darbi no mājām** pievienoti</br>**Valoda** pievienota</br>**Darba stāža datums** pievienots</br>**Gadadienas datums** pievienots</br>**Sākotnējais darbā pieņemšanas datums** pievienots |
| **Nodarbinātības** elementa izmaiņas | **Finanšu dimensijas** pievienotas</br>**Darba attiecību pārtraukšanas pamatojums** pievienots</br>**Beigu datums** pārdēvēts no **Pārejas datuma**</br>**Probācijas datums** pievienots |
| **Darbinieka adreses** elementa izmaiņas | **Adrese** pievienota</br>**1. adreses rinda**, **2. adreses rinda** un **3. adreses rinda** atzīmēta norakstīšanai |
| Jaunas mainīgās atlīdzības iestatījuma entitījas | **Atlīdzības mainīgā plāna tips**</br>**Atlīdzības mainīgā sistēma**</br>**Izmaksas noteikumi**</br>**Atlīdzības mainīgā plāna līmenis** |
| Jauna **Darbinieka kalendāra nodarbinātības** entitīja | **Darba kalendāra elements** pievienots |
| Jauna **Algas pozīcijas detalizētas informācijas** entitīja | **Algas pozīcijas detalizēta informācija** pievienota |
| Jauna **Nosaukuma** entitīja | **Nosaukums** pievienots. Jaunais elements **Nosaukums** tiks iekļauts sinhronizācijas procesā starp Human Resources un Common Data Service. Tam nebūs sākotnējas atsauces no entitījām **Amats** vai **Darbs**. |

Nākamo dažu nedēļu laikā šīs elementa izmaiņas būs pieejamas visās vidēs. Lai manuāli instalētu jaunāko Common Data Service risinājumu Personāla vadībai:

1.  Dodieties uz [Power Platform Administrēšanas centru](https://admin.powerplatform.microsoft.com).

2.  Atlasiet **Vides**.

3.  Sameklējiet vidi, ko vēlaties atjaunināt. Tai ir jāatbilst **Vides nosaukumam** **Common Data Service informācijas** sadaļā, kas atrodas sadaļā **Par** personāla vadības veidlapā.

4.  Atlasiet vidi, lai skatītu vides informāciju.

5.  Darbību joslas augšdaļā atlasiet pogu **Pārvaldīt risinājumus**. Tiks atvērts jauns pārlūkprogrammas logs un navigēs uz **Dynamics 365 administrēšanas centru** vides kontekstā.

6.  **Risinājumu** sarakstā atlasiet **Dynamics 365 Human Resources enkurs**.

7.  Atlasiet **Atjaunināt**, lai izmantotu jaunāko risinājumu.

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie priekšskatījuma līdzekļi kļuva pieejami 2020. gada 3. februārī:

- **Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi** – Papildu informāciju skatiet [Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Atvieglojumu pārvaldības priekšskatījums** — plašāku informāciju, ieskaitot zināmās problēmas, skatiet [Atvieglojumu pārvaldības apskatā](hr-benefits-management-overview.md).
