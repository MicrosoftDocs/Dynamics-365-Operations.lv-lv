---
title: Darbplūsmu pārskata izveide
description: Šajā tēmā ir paskaidrots, kā izveidot darbplūsmu.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "195583"
- intro-internal
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: abdb8ce3186806ac1b756c9161d53547dd8ae40b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067962"
---
# <a name="create-workflows-overview"></a>Darbplūsmu pārskata izveide

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā tēmā ir paskaidrots, kā izveidot darbplūsmu.

## <a name="open-the-workflow-editor"></a>Atveriet darbplūsmas redaktoru

Tas, kāda veida darbplūsmas varat izveidot, ir atkarīgs no moduļa, kurā strādājat. Izpildiet šeit aprakstītās darbības, lai atlasītu izveidojamo darbplūsmas tipu un atvērtu darbplūsmas redaktoru.

1. Atveriet moduli, kuram vēlaties izveidot jaunu darbplūsmu. Piemēram, lai izveidotu darbplūsmu pirkšanas pieprasījumiem, noklikšķiniet uz **Sagāde un avoti**.
2. Noklikšķiniet uz **Iestatīšana** &gt; **\[Moduļa nosaukums\] darbplūsmas**.
3. Parādītās lapas darbību rūtī noklikšķiniet uz **Jauns**.
4. Lapā **Izveidot darbplūsmu** atlasiet izveidojamās darbplūsmas tipu un pēc tam noklikšķiniet uz **Izveidot darbplūsmu**. Tiek parādīts darbplūsmas redaktors. Tagad varat izmantot tālāk aprakstītās procedūras, lai veidotu darbplūsmu.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Velciet darbplūsmas elementus uz audekla

Darbplūsmas redaktora apgabals **Darbplūsmas elementi** satur elementus, ko varat pievienot savai darbplūsmai. Lai elementus pievienotu darbplūsmai, ievelciet tos audeklā.

## <a name="connect-the-elements"></a>Savienojiet elementus

Lai savienotu vienu darbplūsmas elementu ar citu, turiet rādītāju virs elementa, līdz savienojuma punkti tiek parādīti. Noklikšķiniet uz savienojuma punkta un velciet to uz citu elementu. Pārliecinieties, ka tiek savienoti visi elementi.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigurējiet darbplūsmas rekvizītus

Izpildiet šīs darbības, lai konfigurētu darbplūsmas rekvizītus.

1. Noklikšķiniet uz audekla, lai pārliecinātos, vai ir atlasīts darbplūsmas elements.
2. Noklikšķiniet uz **Rekvizīti**, lai darbplūsmai atvērtu lapu **Rekvizīti**.
3. Izpildiet tēmā [Konfigurēt darbplūsmas rekvizītus](configure-workflow-properties.md) aprakstītās procedūras.

## <a name="configure-the-elements-of-the-workflow"></a>Konfigurējiet darbplūsmas elementus

Konfigurējiet katru uz audekla uzvilkto elementu. Informāciju par to, kā konfigurēt katru darbplūsmas elementu, skatiet tālāk norādītajās tēmās.

- [Manuālu uzdevumu konfigurēšana darbplūsmā](configure-manual-task-workflow.md)
- [Automatizētu uzdevumu konfigurēšana darbplūsmā](configure-automated-task-workflow.md)
- [Apstiprināšanas procesu konfigurēšana darbplūsmā](configure-approval-process-workflow.md)
- [Apstiprināšanas darbību konfigurēšana darbplūsmā](configure-approval-step-workflow.md)
- [Manuālu lēmumu konfigurēšana darbplūsmā](configure-manual-decision-workflow.md)
- [Nosacījuma lēmumu konfigurēšana darbplūsmā](configure-conditional-decision-workflow.md)
- [Paralēlu zaru konfigurēšana darbplūsmā](configure-parallel-activity-workflow.md)
- [Konfigurēt paralēlu zaru](configure-parallel-branch-workflow.md)
- [Konfigurēt dokumenta rindas darbplūsmas](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Atrisināt jebkuras kļūdas vai brīdinājumus

Darbplūsmas redaktora apakšā esošajā rūtī **Kļūdas un brīdinājumi** tiek rādīti darbplūsmai ģenerētie ziņojumi. Lai atrastu elementu, kurā radās kļūda vai brīdinājums, veiciet dubultklikšķi uz kļūdas vai brīdinājuma ziņojuma. Lai darbplūsmu varētu padarīt par aktīvu, jums ir jāatrisina visas kļūdas un brīdinājumi.

## <a name="save-and-activate-the-workflow"></a>Saglabājiet un aktivizējiet darbplūsmu

Kad esat gatavs saglabāt un aktivizēt darbplūsmu, izpildiet tālāk aprakstītās darbības.

1. Noklikšķiniet uz **Saglabāt un aizvērt**, lai aizvērtu darbplūsmas redaktoru un atvērtu lapu **Saglabāt darbplūsmu**.
2. Ievadiet komentārus par darbplūsmā veiktajām izmaiņām un pēc tam noklikšķiniet uz **Labi**.
3. Ja visas kļūdas un brīdinājumi ir novērsti, tiek parādīta lapa **Aktivizēt darbplūsmu**. Izvēlieties vienu no šīm opcijām:

    - Lai aktivizētu šo darbplūsmas versiju, noklikšķiniet uz **Aktivizēt jauno versiju**. Kad darbplūsma ir aktīva, lietotāji var tajā iesniegt dokumentus apstrādei.
    - Ja nevēlaties aktivizēt šo versiju, noklikšķiniet uz **Neaktivizēt jauno versiju**. Varat aktivizēt darbplūsmu vēlāk.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]