---
title: "Darbplūsmu sistēmas apskats"
description: "Šajā tēmā ir aprakstīta darbplūsmu sistēma programmatūrā Microsoft Dynamics 365 for Operations."
author: sericks007
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5432e67ffa41e6a38b19c9fe5bb12c5acb2c345c
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="workflow-system-overview"></a>Darbplūsmu sistēmas apskats

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīta darbplūsmu sistēma programmatūrā Microsoft Dynamics 365 for Operations.

<a name="what-is-workflow"></a>Kas ir darbplūsma?
-----------------

Terminu *darbplūsma* var definēt divos veidos — gan kā sistēmu, gan kā biznesa procesu.
### <a name="workflow-is-a-system"></a>Darbplūsma ir sistēma

Darbplūsma ir sistēma, kas tiek instalēta kopā ar programmatūru Dynamics 365 for Operations un darbojas serverī Application Object Server (AOS). Darbplūsmas sistēma nodrošina funkcionalitāti, kuru jūs varat izmantot, lai izveidotu individuālas darbplūsmas vai biznesa procesus.

### <a name="workflow-is-a-business-process"></a>Darbplūsma ir biznesa process

Darbplūsma attēlo biznesa procesu. Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kam ir jāpabeidz uzdevums, jāpieņem lēmums vai jāapstiprina dokuments. Piemēram, nākamajā attēlā ir redzama darbplūsma izdevumu pārskatiem. 

![Darbplūsma ar lietotājiem piešķirtajiem elementiem](./media/workflow_user.gif) 

Lai varētu labāk izprast šo darbplūsmu, pieņemsim, ka Sems iesniedz izdevumu pārskatu par summu USD 7000. Šajā gadījumā Jānim ir jāpārskata kvītis, kuras viņam ir maršrutējis Sems. Pēc tam Kārlim un Santai ir jāapstiprina izdevumu pārskats. Tagad pieņemsim, ka Sems iesniedz izdevumu pārskatu par 11 000 USD. Šajā scenārijā Jānim ir jāpārskata kvītis un Kārlim, Sanitai un Annai ir jāapstiprina izdevumu pārskats.

## <a name="benefits-of-using-the-workflow-system"></a>Darbplūsmas sistēmas izmantošanas priekšrocības

Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.
-   **Saskaņoti procesi** — varat definēt noteiktu dokumentu, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu. Izmantojot darbplūsmas sistēmu, jūs nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti saskaņotā un efektīvā veidā.
-   **Procesa pārskatāmība** — varat izsekot noteiktu darbplūsmas instanču statusa, vēsturiskajiem un veiktspējas rādītājiem. Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.
-   **Centralizēts darbu saraksts** — lietotāji var apskatīt centralizētu darbu sarakstu, kurā ir iekļauti tiem piešķirtie darbplūsmas uzdevumi un apstiprinājumi.


## <a name="workflow-content"></a>Darbplūsmas saturs

+ [Darbplūsmas arhitektūra](workflow-system-architecture.md)
+ [Darbplūsmas elementi](workflow-elements.md)
+ [Darbplūsmas darbības](workflow-actions.md)
+ [Izveidot darbplūsmu](create-workflow.md)
+ [Konfigurēt darbplūsmas rekvizītus](configure-workflow-properties.md)
+ [Konfigurēt manuālu uzdevumu darbplūsmā](configure-manual-task-workflow.md)
+ [Konfigurēt automatizētu uzdevumu darbplūsmā](configure-automated-task-workflow.md)
+ [Konfigurēt apstiprināšanas procesu darbplūsmā](configure-approval-process-workflow.md)
+ [Konfigurēt apstiprināšanas darbību darbplūsmā](configure-approval-step-workflow.md)
+ [Konfigurēt manuālu lēmumu darbplūsmā](configure-manual-decision-workflow.md)
+ [Konfigurēt nosacījuma lēmumu darbplūsmā](configure-conditional-decision-workflow.md)
+ [Konfigurēt paralēlu aktivitāti darbplūsmā](configure-parallel-activity-workflow.md)
+ [Konfigurēt paralēlu zaru darbplūsmā](configure-parallel-branch-workflow.md)
+ [Konfigurēt dokumenta rindas darbplūsmu](configure-line-item-workflow.md)
