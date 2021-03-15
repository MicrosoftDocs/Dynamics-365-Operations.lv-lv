---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 3. marts)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 3. martu.
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e4007daa51d661a2a6b67c323cfaf05c22543371
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128045"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 3. marts)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.2955. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse risinājums tagad ir pieejams ar šādām izmaiņām:

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

3.  Sameklējiet vidi, ko vēlaties atjaunināt. Apkārtējai videi ir jāatbilst **Vides nosaukumam** **Common Data Service informācijas** sadaļā, kas atrodas sadaļā **Par** personāla vadības veidlapā.

4.  Atlasiet vidi, lai skatītu vides informāciju.

5.  Darbību joslas augšdaļā atlasiet pogu **Pārvaldīt risinājumus**. Tiks atvērts jauns pārlūkprogrammas logs un navigēs uz **Dynamics 365 administrēšanas centru** vides kontekstā.

6.  **Risinājumu** sarakstā atlasiet **Dynamics 365 Human Resources enkurs**.

7.  Atlasiet **Atjaunināt**, lai izmantotu jaunāko risinājumu.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Importēt problēmas, kas saistītas ar reģistrācijas datu elementu (406082)

Tagad varat reģistrēt darbinieku jaunā atvaļinājuma plānā ar tādu pašu veidu, ja vien jaunais reģistrācijas datums ir vēlāks par iepriekšējā plāna reģistrācijas datumu, kas ir beidzies.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Problēma ar eksporta ieguldījumu likmēm 401k payrollWorkerEnrolledBenefitDetail elementā DMF (420700)

Šīs izmaiņas labo **payrollWorkerEnrolledBenefitDetail** elementa eksporta funkcionalitāti, lai atspoguļotu pašreizējās darba devēja iemaksas vērtības.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Meklēšana racionalizētajā nodarbinātā veidlapā izraisa ziņojumu, kurā teikts, ka personas laukam jābūt aizpildītam (402525)

Kad meklējat darbinieku, jūs vairs nesaņemsit ziņojumu, kurā teikts, ka jāaizpilda lauks **Persona**.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Piezīmes lauka vērtība neveidojas veidlapā Pievienot papildu prasmes (380134)

Šīs izmaiņas labo problēmu, kad personalizējat veidlapu **Pievienot papildu prasmes** darbinieku pašapkalpošanās pakalpojumā.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Vairāki fiksētās atlīdzības plāni nebeidzas, pārsūtot darbiniekus (389466)

Ar šīm izmaiņām visiem aktīvajiem fiksētās atlīdzības ierakstiem vecajā pozīcijā beigsies pārejas datums.

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie priekšskatījuma līdzekļi kļuva pieejami 2020. gada 3. februārī:

- **Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi** – Papildu informāciju skatiet [Atvaļinājuma un prombūtnes priekšskatījuma līdzekļi](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Atvieglojumu pārvaldības priekšskatījums** — plašāku informāciju, ieskaitot zināmās problēmas, skatiet [Atvieglojumu pārvaldības apskatā](hr-benefits-management-overview.md).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]