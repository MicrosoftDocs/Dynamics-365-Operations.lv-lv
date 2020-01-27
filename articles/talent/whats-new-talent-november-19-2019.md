---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 19. novembris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
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
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 88ed678cdd37b4bd3d1a7ae92b505b2cfdea4fc8
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896731"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 19. novembris)

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2621. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Finance and Operations Platform update 31 lietojumprogramma

Lai iegūtu vairāk informācijas, skatiet [Priekšskatījumu līdzekļi platformas 31. atjauninājumā, kas paredzēts Finance and Operations programmām (2020. gada janvāris)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31).

### <a name="feature-management-workspace-383856"></a>Līdzekļu pārvaldības darbvieta (383856)

**Funkciju pārvaldības** darbvieta sniedz katrā laidienā piegādāto līdzekļu sarakstu. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju. Papildinformāciju par Līdzekļu pārvaldību skatiet [Pārskats par līdzekļu pārvaldību](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Visi jaunie līdzekļi paliek priekšskatījumā vismaz 30 dienas, un parasti 30-60 dienas. Galvenās funkcijas parasti ir pieejamas katra gada oktobrī un aprīlī pēc priekšskatījuma perioda. Tiklīdz jūs redzat jaunas iespējas **Līdzekļu pārvaldības** darbvietā, varat tās ieslēgt. Daži līdzekļi var būt ieslēgti pēc noklusējuma.
 
Reizēm šis līdzeklis būs ieslēgts pēc noklusējuma, un to nevar izslēgt (piemēram, **Līdzekļu pārvaldības** darbvieta).
 
Kolīdz līdzeklis ir vispārīgi pieejams, to var ieslēgt vai izslēgt ražošanas vidēs. **Līdzekļu pārvaldības** darbvieta norāda, kad priekšskatījuma līdzeklis kļūs obligāts. Šis datums parasti ir 1. oktobris vai 1. aprīlis, lai to saskaņotu ar pusgada laidiena plāniem. Jūs nevarat izslēgt obligātos līdzekļus. Kamēr tas kļūst obligāts, varat ieslēgt vai izslēgt līdzekli visās vidēs.

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>Ziņojums parādās, ja pozīcijai pastāv atcelšanas darbība (382887)

Šāds ziņojums vairs netiek parādīts, kad atlasāt noteiktu amatu un atcelšanas darbība ir vienīgais, kas ir pieejams šim amatam: **Nepabeigta darbība ir notikusi pozīcijā XXXXXX**.

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>Apgūstot analītiku, kursa tips un statuss parāda nepareizus datus (381151)

Šīs nedēļas laidiena atjauninātā apmācības analītika, lai pareizi parādītu **Kursa tipu** un **Statusu**.

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>Personāla numuram jāparādās jaunā darbinieka formas reklāmkarogā (383832)

Formā **Jaunais darbinieks** **Personāla numurs** tagad tiek parādīts reklāmkaroga ātrajā atsaucē.

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>Pozīcijas sākuma datums nosaka darba ierakstu, ko izmantot, atgūstot atlīdzības līmeni darbā pieņemšanas laikā (350361)

Šajā laidienā **Atlīdzības sākuma datums** nosaka jaunajam darbam piešķirto līmeni.

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>Pielāgotie izdošanas saraksta lauki pozīcijas tabulā netiek sinhronizēti ar Common Data Service (387503)

Ar šo laidienu izdošanas saraksta elementi tagad ir sinhronizēti ar Common Data Service.

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>Darbinieka adreses elements netiek sinhronizēts ar Common Data Service, importējot jaunus datus (349673)

Šīs nedēļas laidienā adrešu dati tagad tiek sinhronizēti ar Common Data Service, importējot jaunus datus.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Aplūkojiet [Drukāšanas veiktspējas pārskati](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) Dynamics 365: 2019. gada izlaiduma 2. laidiena plāns.
