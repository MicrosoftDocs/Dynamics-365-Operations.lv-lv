---
title: "Virsgrāmatas žurnāla apstrāde"
description: "Šo izstrādājumu apraksta iespējas Microsoft Dynamics 365 operācijām, kas var palīdzēt veikt Virsgrāmatas žurnāla apstrādes vieglāk un kuras var palīdzēt garantēt, ka pareizos datus notverti un iekšējo kontroli vai nav apdraudēta."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 50cd203025be8857de943e458fc32315e494fb7a
ms.lasthandoff: 03/31/2017


---

# <a name="general-journal-processing"></a>Virsgrāmatas žurnāla apstrāde

Šajā rakstā ir aprakstītas iespējas programmatūrā Microsoft Dynamics AX, kas var palīdzēt vienkāršot vispārējo žurnālu apstrādi un turklāt var palīdzēt garantēt, ka tiek iztverti pareizie dati un netiek bojāta iekšējā kontrole.  

Žurnālu nosaukumi

Viena no svarīgākajām jomām, līdz iestatīšana ir žurnālu nosaukumus. Tā ir laba ideja, lai definētu noteiktu žurnālu nosaukumus katrai mērķiem, piemēram, starpuzņēmumu, uzkrāšanas korekcijas un kļūdu labošana. Jūs varat pielāgot katra žurnāla nosaukumu, lai palīdzētu veikt datu ievadi katram mērķim, vienkārša un droša. 

Lapā **Žurnālu nosaukumi**, jūs varat iestatīt šādus elementus:

-   **Darbplūsmas apstiprinājums** – lai palielinātu iekšējo pārbaudi, definējiet žurnāla darbplūsmas, kas izveido būtiskuma ierobežojumus pārskatīšanas un apstiprināšanas soļiem, pamatojoties uz tādiem kritērijiem, kā debeta summa. Jums iestatīt darbplūsmas Virsgrāmatas žurnālos * * Virsgrāmatu darbplūsmas * lapa.
-   **Noklusētās vērtības** – atlasiet noklusētās vērtības korespondējošiem kontiem, valūtai un finanšu dimensijām.
-   **Žurnāla pārbaude** – varat iestatīt ierobežojumus attiecībā uz uzņēmumu un konta tipu, kā arī segmentu vērtībām. 

**Piemēri**

Žurnāla nosaukums var tikt izmantots tikai korekcijām. Šādā gadījumā, jūs varat norādīt, ka tikai **Virsgrāmatas** konta tips ir derīgs visos uzņēmumos. [![Žurnāla kontroles kontu tipi](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Žurnāla nosaukumu var izmantot tikai galveno kontu noteiktam segmentam vai diapazonam. [![Žurnāla kontroles segments](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Virsgrāmatas žurnālos ir pieejama opcija **Automātiskās atgriešana**. Piemēram, jums ir uzkrājuma korekcija, kur faktiskais dokuments vēl nav apstrādāts, kā parādīts šajā attēlā.
[![Virsgrāmatas žurnāla atpakaļgaitas](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel pievienojumprogramma žurnāla ierakstam nodrošina papildu automatizācijas līmeni un atvieglo datu ievadi. Darbība **Atvērt rindas programmā Excel **ir pieejama lapās **Virsgrāmatas žurnāls** un **Žurnāla dokuments**. 

Lapā **Periodiskie žurnāli**, jūs varat iestatīt periodiskos žurnālus, lai automatizētu žurnāla apstrādi. 

Dokumenta veidnes var izmantot jebkurā laikā. Par **Virsgrāmatas žurnālos** lapu, **saglabāt** un **atlasiet dokumenta veidni** darbībām atrodamas **žurnāla dokuments** lapu, zem **funkcijas** dokumenta rindām.

## <a name="related-setup"></a>Saistītā iestatīšana
Šī iestatīšana nav raksturīga Virsgrāmatas žurnāliem, bet palīdzēs garantēt, ka datu ievade notiek pareizi un viegli.

### <a name="main-account"></a>Galvenais konts

Galvenā konta iestatīšana sniedz daudzas opcijas Virsgrāmatas žurnāla apstrādei:

-   **DC/CR prasība** – izmantojiet šo opciju, ja galvenais konts ir ierobežots ar debeta vai kredīta darbībām. Iestatīšana ir apstiprināta, kad žurnāls tiek pārbaudīts vai grāmatots.
-   **Noklusētais korespondējošais konts**
-   **Atlikts** – apturēt galvenā konta datu ievadi visiem uzņēmumiem vai konkrētam uzņēmumam/juridiskai personai.
-   **Neļaut manuālu ievadi** – neļaut lietotājiem manuāli ievadīt vērtību konta žurnālos.
-   **Noklusējuma/Pārbaudīt valūtu**
-   **Juridiskās personas ignorēšana** – šis iestatījums ir specifisks noteiktam uzņēmumam/juridiskai personai:
    -   **Noklusējuma/Validēt PVN**
    -   **Noklusējuma dimensija** – **Nav noteikta** vai **Fiksēta vērtība**. **Fiksēta vērtība** palīdzēs nodrošināt, ka visi grāmatojumi šajā galvenajā kontā vienmēr izmantos jebkuru dimensijas vērtību, kas iestatīta kā **Fiksēta**.
-   **Grāmatojuma pārbaude**
    -   **Lietotāja pārbaude** – šī opcija pārbauda, kuri lietotāji var grāmatot galvenajā kontā.
    -   **Grāmatošanas veida validēšana** – šī opcija pārbauda, kuri grāmatošanas veidi ir atļauti galvenajam kontam.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Grāmatvedības struktūras un papildu kārtulu struktūras

Grāmatvedības struktūras un papildu kārtulu struktūras ir ļoti svarīgas, lai nodrošinātu, ka dati, kas ir nepieciešami finanšu pārskatiem un veiktspējas izsekošanai, tiek tverti Virsgrāmatas žurnāla un jebkādas dokumentācijas apstrādes laikā. Grāmatvedības struktūras un papildu kārtulu struktūras ļauj pielāgot datu ievades iespējas. Jūs varat atļaut datu ievadi tikai finanšu dimensijām, kas ir atbilstošas katrā situācijā, kā arī ieviest prasību par to, ka vienmēr jātver obligāti un pareizi dati.

Lai iegūtu papildinformāciju, skatiet [plānošana: kontu](plan-chart-of-accounts.md). 


