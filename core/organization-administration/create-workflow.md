---
title: "Darbplūsmas izveide"
description: "Šajā tēmā ir paskaidrots, kā izveidot darbplūsmu."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 1255cf90498f1968568dd2fa5a1377d989f40182
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-workflow"></a>Darbplūsmas izveide

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā izveidot darbplūsmu.

<a name="open-the-workflow-editor"></a>Atveriet darbplūsmas redaktoru
------------------------

To, kādus darbplūsmas tipus varat izveidot, nosaka Microsoft Dynamics 365 for Operations modulis, kurā jūs strādājat. Izpildiet šeit aprakstītās darbības, lai atlasītu izveidojamo darbplūsmas tipu un atvērtu darbplūsmas redaktoru.

1.  Atveriet moduli, kuram vēlaties izveidot jaunu darbplūsmu. Piemēram, lai izveidotu darbplūsmu pirkšanas pieprasījumiem, noklikšķiniet uz **Sagāde un avoti**.
2.  Noklikšķiniet uz **Iestatīšana** &gt; **\[Moduļa nosaukums\] darbplūsmas**.
3.  Parādītās lapas darbību rūtī noklikšķiniet uz **Jauns**.
4.  Lapā **Izveidot darbplūsmu** atlasiet izveidojamās darbplūsmas tipu un pēc tam noklikšķiniet uz **Izveidot darbplūsmu**. Tiek parādīts darbplūsmas redaktors. Tagad varat izmantot tālāk aprakstītās procedūras, lai veidotu darbplūsmu.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Velciet darbplūsmas elementus uz audekla
Darbplūsmas redaktora apgabals **Darbplūsmas elementi** satur elementus, ko varat pievienot savai darbplūsmai. Lai elementus pievienotu darbplūsmai, ievelciet tos audeklā.

## <a name="connect-the-elements"></a>Savienojiet elementus
Lai savienotu vienu darbplūsmas elementu ar citu, turiet rādītāju virs elementa, līdz savienojuma punkti tiek parādīti. Noklikšķiniet uz savienojuma punkta un velciet to uz citu elementu. Pārliecinieties, ka tiek savienoti visi elementi.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigurējiet darbplūsmas rekvizītus
Izpildiet šīs darbības, lai konfigurētu darbplūsmas rekvizītus.

1.  Noklikšķiniet uz audekla, lai pārliecinātos, vai ir atlasīts darbplūsmas elements.
2.  Noklikšķiniet uz **Rekvizīti**, lai darbplūsmai atvērtu lapu **Rekvizīti**.
3.  Izpildiet tēmā [Konfigurēt darbplūsmas rekvizītus](configure-workflow-properties.md) aprakstītās procedūras.

## <a name="configure-the-elements-of-the-workflow"></a>Konfigurējiet darbplūsmas elementus
Konfigurējiet katru uz audekla uzvilkto elementu. Informāciju par to, kā konfigurēt katru darbplūsmas elementu, skatiet tālāk norādītajās tēmās.

-   [Manuāla uzdevuma konfigurēšana](configure-manual-task-workflow.md)
-   [Automatizēta uzdevuma konfigurēšana](configure-automated-task-workflow.md)
-   [Apstiprināšanas procesa konfigurēšana](configure-approval-process-workflow.md)
-   [Apstiprinājuma darbības konfigurēšana](configure-approval-step-workflow.md)
-   [Manuāla lēmuma konfigurēšana](configure-manual-decision-workflow.md)
-   [Konfigurēt nosacījuma lēmumu](configure-conditional-decision-workflow.md)
-   [Konfigurēt paralēlu aktivitāti](configure-parallel-activity-workflow.md)
-   [Konfigurēt paralēlu zaru](configure-parallel-branch-workflow.md)
-   [Konfigurēt dokumenta rindas darbplūsmu](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Atrisināt jebkuras kļūdas vai brīdinājumus
Darbplūsmas redaktora apakšā esošajā rūtī **Kļūdas un brīdinājumi** tiek rādīti darbplūsmai ģenerētie ziņojumi. Lai atrastu elementu, kurā radās kļūda vai brīdinājums, veiciet dubultklikšķi uz kļūdas vai brīdinājuma ziņojuma. Lai darbplūsmu varētu padarīt par aktīvu, jums ir jāatrisina visas kļūdas un brīdinājumi.

## <a name="save-and-activate-the-workflow"></a>Saglabājiet un aktivizējiet darbplūsmu
Kad esat gatavs saglabāt un aktivizēt darbplūsmu, izpildiet tālāk aprakstītās darbības.

1.  Noklikšķiniet uz **Saglabāt un aizvērt**, lai aizvērtu darbplūsmas redaktoru un atvērtu lapu **Saglabāt darbplūsmu**.
2.  Ievadiet komentārus par darbplūsmā veiktajām izmaiņām un pēc tam noklikšķiniet uz **Labi**.
3.  Ja visas kļūdas un brīdinājumi ir novērsti, tiek parādīta lapa **Aktivizēt darbplūsmu**. Izvēlieties vienu no šīm opcijām:
    -   Lai aktivizētu šo darbplūsmas versiju, noklikšķiniet uz **Aktivizēt jauno versiju**. Kad darbplūsma ir aktīva, lietotāji var tajā iesniegt dokumentus apstrādei.
    -   Ja nevēlaties aktivizēt šo versiju, noklikšķiniet uz **Neaktivizēt jauno versiju**. Varat aktivizēt darbplūsmu vēlāk.






