---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 10. decembris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528175"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 10. decembris)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2660. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Līdzekļu pārvaldības darbvieta

**Funkciju pārvaldības** darbvieta sniedz katrā laidienā piegādāto līdzekļu sarakstu. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju. Papildinformāciju par Līdzekļu pārvaldību skatiet [Pārskats par līdzekļu pārvaldību](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Visi jaunie līdzekļi paliek priekšskatījumā vismaz 30 dienas, un parasti 30-60 dienas. Galvenās funkcijas parasti ir pieejamas katra gada oktobrī un aprīlī pēc priekšskatījuma perioda. Tiklīdz jūs redzat jaunas iespējas **Līdzekļu pārvaldības** darbvietā, varat tās ieslēgt. Daži līdzekļi var būt ieslēgti pēc noklusējuma.
 
Reizēm šis līdzeklis būs ieslēgts pēc noklusējuma, un to nevar izslēgt (piemēram, **Līdzekļu pārvaldības** darbvieta).
 
Kolīdz līdzeklis ir vispārīgi pieejams, to var ieslēgt vai izslēgt ražošanas vidēs. **Līdzekļu pārvaldības** darbvieta norāda, kad priekšskatījuma līdzeklis kļūs obligāts. Šis datums parasti ir 1. oktobris vai 1. aprīlis, lai to saskaņotu ar pusgada laidiena plāniem. Jūs nevarat izslēgt obligātos līdzekļus. Kamēr tas kļūst obligāts, varat ieslēgt vai izslēgt līdzekli visās vidēs.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Racionalizēta nodarbinātā veidlapa ir pārvietota uz līdzekļu pārvaldības darbvietu (390583)

Ar šīm izmaiņām racionalizētā nodarbinātā veidlapu tagad var iespējot darbvietā **Līdzekļu pārvaldība**. Šis līdzeklis ir pārvietots no veidlapas **Sistēmas parametri** sadaļā **Sistēmas administrēšana**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Novērsta HcmWorkerPayrollInfo ierakstu rakstīšana bez nodarbinātā vērtības (394526)

Ar šo laidienu **HcmWorkerPayrollInfo** ieraksti vairs netiek izveidoti bez nodarbinātā raksturojuma šajā scenārijā. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Ar darbību saistītais ziņojumu žurnāls netiek aizpildīts, ja darbību neizdodas pabeigt (374007)

Šajā laidienā ir ietvertas izmaiņas darbību ziņojumu žurnāla aizpildīšanā, ja darbība neizdodas noteiktos scenārijos. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Common data service integrācijas pakešuzdevuma izveide (388030)

Ar šīm izmaiņām pakešuzdevumi Common Data Service integrācijai tiek izveidoti, ja pakalpojums ir iespējots.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Papildu izdošanas saraksta vērtības pielāgotos laukos netiek parādītas Common Data Service pēc "lietot" noklikšķināšanas pielāgoto lauku formā (379599).

Ar šīm izmaiņām Talent ievadītās jaunās izdošanas saraksta vērtības tagad tiek sinhronizētas ar Common Data Service, kad pielietojat savas izmaiņas.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Atjauniniet uz Common Data Service, lai transakcijas entītija "Atstāt tukšu" kļūtu par ieliktni Talent pusē (352938)

Šīs izmaiņas novērš problēmu, kur atjaunināšana atstāt tukšu transakciju izveido jaunu ierakstu Talent.

## <a name="in-preview"></a>Priekšskatījumā

Priekšskatījuma līdzekļi ir pieejami tikai **Smilškastes** vidēs.

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Aplūkojiet [Drukāšanas veiktspējas pārskati](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) Dynamics 365: 2019. gada izlaiduma 2. laidiena plāns.

