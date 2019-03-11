---
title: Virsgrāmatas žurnāla apstrāde
description: Šajā tēmā ir aprakstītas programmā Microsoft Dynamics 365 for Finance and Operations pieejamās iespējas, kas var palīdzēt atvieglot Virsgrāmatas žurnāla apstrādi, kā arī palīdzēt nodrošināt, ka tiek iegūti pareizie dati un netiek pārkāpti iekšējās kontroles kritēriji.
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e77aafafed5c972a6ad8c064107306d3ebde0b79
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "358443"
---
# <a name="general-journal-processing"></a>Virsgrāmatas žurnāla apstrāde

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas programmā Microsoft Dynamics 365 for Finance and Operations pieejamās iespējas, kas var palīdzēt atvieglot Virsgrāmatas žurnāla apstrādi, kā arī palīdzēt nodrošināt, ka tiek iegūti pareizie dati un netiek pārkāpti iekšējās kontroles kritēriji.  

## <a name="journal-names"></a>Žurnālu nosaukumi

Viena no svarīgākajām iestatījumu jomām ir žurnālu nosaukumi. Ir ieteicams norādīt žurnālu nosaukumus katram mērķim, piemēram, starpuzņēmumu transakcijām, uzkrājumu korekcijai un kļūdu labošanai. Varat pielāgot katra žurnāla nosaukumu, lai palīdzētu padarīt katram mērķim paredzēto datu ievadi vienkāršu un drošu. 

Lapā **Žurnālu nosaukumi**, jūs varat iestatīt šādus elementus:

-   **Darbplūsmas apstiprinājums** – lai palielinātu iekšējo pārbaudi, definējiet žurnāla darbplūsmas, kas izveido būtiskuma ierobežojumus pārskatīšanas un apstiprināšanas soļiem, pamatojoties uz tādiem kritērijiem, kā debeta summa. Varat iestatīt darbplūsmas virsgrāmatas žurnāliem lapā **Virsgrāmatas darbplūsmas**.
-   **Noklusētās vērtības** – atlasiet noklusētās vērtības korespondējošiem kontiem, valūtai un finanšu dimensijām.
-   **Žurnāla pārbaude** – varat iestatīt ierobežojumus attiecībā uz uzņēmumu un konta tipu, kā arī segmentu vērtībām. 

**Piemēri**

Žurnāla nosaukums var tikt izmantots tikai korekcijām. Šādā gadījumā, jūs varat norādīt, ka tikai **Virsgrāmatas** konta tips ir derīgs visos uzņēmumos. 

[![Žurnāla pārbaudes kontu veidi](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Žurnāla nosaukumu var izmantot tikai galveno kontu noteiktam segmentam vai diapazonam. 

[![Žurnāla pārbaudes segments](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Virsgrāmatas žurnālos ir pieejama opcija **Automātiskās atgriešana**. Piemēram, jums ir uzkrājuma korekcija, kur faktiskais dokuments vēl nav apstrādāts, kā parādīts šajā attēlā.
[![Virsgrāmatas žurnāla storno](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel pievienojumprogramma žurnāla ierakstu izveidei nodrošina papildu automatizācijas līmeni un atvieglo datu ievadi. Darbība **Atvērt rindas programmā Excel** ir pieejama lapās **Virsgrāmatas žurnāls** un **Žurnāla dokuments**. 

Lapā **Periodiskie žurnāli**, jūs varat iestatīt periodiskos žurnālus, lai automatizētu žurnāla apstrādi. 

Jebkurā laikā varat izmantot dokumentu veidnes. Lapā **Virsgrāmatas žurnāli** darbības **Saglabāt** un **Atlasīt dokumenta veidni** ir pieejamas lapas **Žurnāla dokuments** dokumentu rindiņu sadaļā **Funkcijas**.

## <a name="related-setup"></a>Saistītā iestatīšana
Tālāk aprakstīta iestatīšana nav raksturīga Virsgrāmatas žurnāliem, bet palīdzēs nodrošināt pareizu un ērtu datu ievadi.

### <a name="main-account"></a>Galvenais konts

Galvenā konta iestatīšana sniedz daudzas opcijas Virsgrāmatas žurnāla apstrādei:

-   **DC/CR prasība** – izmantojiet šo opciju, ja galvenais konts ir ierobežots ar debeta vai kredīta darbībām. Iestatīšana ir apstiprināta, kad žurnāls tiek pārbaudīts vai grāmatots.

-   **Noklusētais korespondējošais konts**
-   **Atlikts** — apturēt galvenā konta datu ievadi visiem uzņēmumiem vai konkrētam uzņēmumam/juridiskai personai.
-   **Neļaut manuālu ievadi** – neļaut lietotājiem manuāli ievadīt vērtību konta žurnālos.
-   **Noklusējuma/Pārbaudīt valūtu**
-   **Juridiskās personas ignorēšana** – šis iestatījums ir specifisks noteiktam uzņēmumam/juridiskai personai:
    -   **Noklusējuma/Validēt PVN**
    -   **Noklusējuma dimensija** – **Nav noteikta** vai **Fiksēta vērtība**. **Fiksēta vērtība** palīdzēs nodrošināt, ka visiem grāmatojumiem šajā galvenajā kontā vienmēr tiks izmantota jebkura dimensijas vērtība, kas iestatīta kā **Fiksēta**.
-   **Grāmatojuma pārbaude**
    -   **Lietotāja pārbaude** – šī opcija pārbauda, kuri lietotāji var grāmatot galvenajā kontā.
    -   **Grāmatošanas veida validēšana** – šī opcija pārbauda, kuri grāmatošanas veidi ir atļauti galvenajam kontam.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Grāmatvedības struktūras un papildu kārtulu struktūras

Grāmatvedības struktūras un papildu kārtulu struktūras ir ļoti svarīgas, lai nodrošinātu, ka dati, kas ir nepieciešami finanšu pārskatiem un veiktspējas izsekošanai, tiek tverti Virsgrāmatas žurnāla un jebkuru dokumentu apstrādes laikā. Grāmatvedības struktūras un papildu kārtulu struktūras ļauj pielāgot datu ievades iespējas. Datu ievadi var atļaut tikai finanšu dimensijām, kas ir atbilstošas katrā situācijā, kā arī ieviest prasību, ka vienmēr ir jātver obligāti nepieciešami un pareizi dati.

Lai iegūtu papildu informāciju, skatiet šādas tēmas:
- [Plānošana: kontu plāns](plan-chart-of-accounts.md). 
- [Žurnālu papildu kārtulu izveide](tasks/create-advanced-rules-journals.md)
- [Žurnāla ieraksta izveide, izmantojot veidni](tasks/create-journal-entry-template.md)
- [Žurnālu izveide un validēšana](tasks/create-validate-journals.md)
- [Periodisko žurnālu grāmatošana](tasks/post-periodic-journals.md)
- [Virsgrāmatas sadalījumu žurnāla apstrāde](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Simulēt grāmatošanu
Vairumā žurnālu opcija **Simulēt grāmatošanu** ir pieejama izvēlnē **Apstiprināt**. Apstiprinot žurnālu, izmantojot funkciju **Apstiprināt**, sistēma pārbauda, vai žurnālā nav noteiktu kļūdas nosacījumu. Ja tiek izmantota funkcija **Simulēt grāmatošanu**, sistēma palaiž visus tos pašus procesus, kas tiek palaisti grāmatošanas laikā bez faktiskas žurnāla grāmatošanas. Pēc tam varat pārskatīt parādītos grāmatošanas ziņojumus, izlabot atrastās kļūdas, un pēc tam noklikšķiniet uz izvēlnes **Grāmatot**, lai grāmatotu žurnālu. 

Opcija **Simulēt grāmatošanu** nav pieejama pakešveida apstrādei. Taču ir pieejams pakešveida grāmatošanas simulēšanas kods, un izstrādātāji var paplašināt kodu, lai pievienotu šo funkcionalitāti.  
