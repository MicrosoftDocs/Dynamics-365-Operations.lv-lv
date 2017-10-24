---
title: "Virsgrāmatas žurnāla apstrāde"
description: "Šajā rakstā ir aprakstītas programmatūras Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise iespējas, kas var palīdzēt vienkāršot virsgrāmatas žurnālu apstrādi un arī nodrošināt pareizu datu ieguvi un pienācīgu iekšējo kontroli."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 68da281cb4793ed83f70c68d061d327aa8a8c772
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="general-journal-processing"></a>Virsgrāmatas žurnāla apstrāde

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstītas programmatūras Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise iespējas, kas var palīdzēt vienkāršot virsgrāmatas žurnālu apstrādi un arī nodrošināt pareizu datu ieguvi un pienācīgu iekšējo kontroli.  

Žurnālu nosaukumi

Viena no svarīgākajām iestatījumu jomām ir žurnālu nosaukumi. Ir ieteicams norādīt žurnālu nosaukumus katram mērķim, piemēram, starpuzņēmumu transakcijām, uzkrājumu korekcijai un kļūdu labošanai. Varat pielāgot katra žurnāla nosaukumu, lai palīdzētu padarīt katram mērķim paredzēto datu ievadi vienkāršu un drošu. 

Lapā **Žurnālu nosaukumi**, jūs varat iestatīt šādus elementus:

-   **Darbplūsmas apstiprinājums** – lai palielinātu iekšējo pārbaudi, definējiet žurnāla darbplūsmas, kas izveido būtiskuma ierobežojumus pārskatīšanas un apstiprināšanas soļiem, pamatojoties uz tādiem kritērijiem, kā debeta summa. Virsgrāmatas žurnālu darbplūsmas var iestatīt lapā **Virsgrāmatas darbplūsmas**.
-   **Noklusētās vērtības** – atlasiet noklusētās vērtības korespondējošiem kontiem, valūtai un finanšu dimensijām.
-   **Žurnāla pārbaude** – varat iestatīt ierobežojumus attiecībā uz uzņēmumu un konta tipu, kā arī segmentu vērtībām. 

**Piemēri**

Žurnāla nosaukums var tikt izmantots tikai korekcijām. Šādā gadījumā, jūs varat norādīt, ka tikai **Virsgrāmatas** konta tips ir derīgs visos uzņēmumos. [![Žurnāla pārbaudes kontu veidi](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Žurnāla nosaukumu var izmantot tikai galveno kontu noteiktam segmentam vai diapazonam. [![Žurnāla pārbaudes segments](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Virsgrāmatas žurnālos ir pieejama opcija **Automātiskās atgriešana**. Piemēram, jums ir uzkrājuma korekcija, kur faktiskais dokuments vēl nav apstrādāts, kā parādīts šajā attēlā.
[![Virsgrāmatas žurnāla storno](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel pievienojumprogramma žurnāla ierakstu veidošanai nodrošina papildu automatizācijas līmeni un atvieglo datu ievadi. Darbība **Atvērt rindas programmā Excel** ir pieejama lapās **Virsgrāmatas žurnāls** un **Žurnāla dokuments**. 

Lapā **Periodiskie žurnāli**, jūs varat iestatīt periodiskos žurnālus, lai automatizētu žurnāla apstrādi. 

Jebkurā laikā varat izmantot dokumentu veidnes. Lapā **Virsgrāmatas žurnāli** darbības **Saglabāt** un **Atlasīt dokumenta veidni** ir pieejamas lapas **Žurnāla dokuments** dokumentu rindiņu sadaļā **Funkcijas**.

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

Lai iegūtu papildu informāciju, skatiet šādas tēmas:
- [Plānošana: kontu plāns](plan-chart-of-accounts.md). 
- [Žurnālu papildu kārtulu izveide](tasks/create-advanced-rules-journals.md)
- [Žurnāla ieraksta izveide, izmantojot veidni](tasks/create-journal-entry-template.md)
- [Žurnālu izveide un validēšana](tasks/create-validate-journals.md)
- [Periodu žurnālu grāmatošana](tasks/post-periodic-journals.md)
- [Virsgrāmatas sadalījuma žurnāla apstrāde](tasks/process-ledger-allocation-journal.md)



