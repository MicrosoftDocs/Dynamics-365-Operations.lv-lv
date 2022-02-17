---
title: Darbplūsmu sistēmas apskats
description: Šajā tēmā ir aprakstīta darbplūsmu sistēma.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70776ba0a0461998d2c1f62ba05b55cd4307a0f7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067937"
---
# <a name="workflow-system-overview"></a>Darbplūsmu sistēmas apskats

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā tēmā ir aprakstīta darbplūsmu sistēma.

## <a name="what-is-workflow"></a>Kas ir darbplūsma?

Terminu *darbplūsma* var definēt divos veidos — gan kā sistēmu, gan kā biznesa procesu.

### <a name="workflow-is-a-system"></a>Darbplūsma ir sistēma

Darbplūsma ir sistēma, kas darbojas serverī Application Object Server (AOS). Darbplūsmas sistēma nodrošina funkcionalitāti, kuru jūs varat izmantot, lai izveidotu individuālas darbplūsmas vai biznesa procesus.

### <a name="workflow-is-a-business-process"></a>Darbplūsma ir biznesa process

Darbplūsma attēlo biznesa procesu. Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kam ir jāpabeidz uzdevums, jāpieņem lēmums vai jāapstiprina dokuments. Piemēram, nākamajā attēlā ir redzama darbplūsma izdevumu pārskatiem.

![Darbplūsma ar lietotājiem piešķirtajiem elementiem.](./media/workflow_user.gif)

Lai varētu labāk izprast šo darbplūsmu, pieņemsim, ka Sems iesniedz izdevumu pārskatu par summu USD 7000. Šajā gadījumā Jānim ir jāpārskata kvītis, kuras viņam ir maršrutējis Sems. Pēc tam Kārlim un Santai ir jāapstiprina izdevumu pārskats. Tagad pieņemsim, ka Sems iesniedz izdevumu pārskatu par 11 000 USD. Šajā scenārijā Jānim ir jāpārskata kvītis un Kārlim, Sanitai un Annai ir jāapstiprina izdevumu pārskats.

## <a name="benefits-of-using-the-workflow-system"></a>Darbplūsmas sistēmas izmantošanas priekšrocības

Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.

- **Saskaņoti procesi** — varat definēt noteiktu dokumentu, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu. Izmantojot darbplūsmas sistēmu, jūs nodrošināt, ka dokumenti tiek apstrādāti un apstiprināti saskaņotā un efektīvā veidā.
- **Procesa pārskatāmība** — varat izsekot noteiktu darbplūsmas instanču statusa, vēsturiskajiem un veiktspējas rādītājiem. Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.
- **Centralizēts darbu saraksts** — lietotāji var apskatīt centralizētu darbu sarakstu, kurā ir iekļauti tiem piešķirtie darbplūsmas uzdevumi un apstiprinājumi.


## <a name="workflow-content"></a>Darbplūsmas saturs

+ [Darbplūsmas sistēmas arhitektūra](workflow-system-architecture.md)
+ [Darbplūsmas elementi](workflow-elements.md)
+ [Darbības darbplūsmas apstiprināšanas procesos](workflow-actions.md)
+ [Izveidot darbplūsmu pārskatu](create-workflow.md)
+ [Konfigurēt darbplūsmas rekvizītus](configure-workflow-properties.md)
+ [Manuālu uzdevumu konfigurēšana darbplūsmā](configure-manual-task-workflow.md)
+ [Automatizētu uzdevumu konfigurēšana darbplūsmā](configure-automated-task-workflow.md)
+ [Apstiprināšanas procesu konfigurēšana darbplūsmā](configure-approval-process-workflow.md)
+ [Apstiprināšanas darbību konfigurēšana darbplūsmā](configure-approval-step-workflow.md)
+ [Manuālu lēmumu konfigurēšana darbplūsmā](configure-manual-decision-workflow.md)
+ [Nosacījuma lēmumu konfigurēšana darbplūsmā](configure-conditional-decision-workflow.md)
+ [Paralēlu aktivitāšu konfigurēšana darbplūsmā](configure-parallel-activity-workflow.md)
+ [Paralēlu zaru konfigurēšana darbplūsmā](configure-parallel-branch-workflow.md)
+ [Konfigurēt dokumenta rindas darbplūsmas](configure-line-item-workflow.md)
+ [Bieži uzdotie jautājumi par darbplūsmām](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]