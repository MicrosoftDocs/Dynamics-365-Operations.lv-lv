---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 25. februāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 25. februāri.
author: andreabichsel
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd86361e4f9e1b6a08f3aa9f400d7f0029584d73
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689331"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 25. februāris)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>Nodarbinātā amata piešķire netiek veidota Dataverse, kad tas tiek atlasīts dialoglodziņā Jauns nodarbināmais (413479)

Šī izmaiņa labo problēmu, kurā nolīgst jaunu nodarbināto un piešķir to pozīcijai, izmantojot dialoglodziņu **Jauns nodarbinātais**. Tagad pozīcijas piešķire tiek atainota Dataverse.

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

Nākamo dažu nedēļu laikā šīs elementa izmaiņas būs pieejamas visās vidēs. Lai manuāli instalētu jaunāko Dataverse risinājumu Personāla vadībai:

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

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]