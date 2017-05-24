---
title: "Lietot uzmeklēšanu, lai atrastu informāciju"
description: "Sistēmā Microsoft Dynamics 365 for Operations daudziem laukiem ir uzmeklēšana, kas jums palīdz ērti atrast pareizo vai vēlamo vērtību. Uzmeklēšanai ir pievienoti vairāki uzlabojumi, vadīklas padarot ērtāk lietojamas un lietotāju darbu — vēl produktīvāku. Šajā tēmā jūs uzzināsiet par šiem jaunajiem uzmeklēšanas līdzekļiem un saņemsiet noderīgus padomus par optimālu uzmeklēšanas lietojumu sistēmā."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 0a64e9dc4009850039e22e98f1c7330c81a5c4b3
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="use-lookups-to-find-information"></a>Lietot uzmeklēšanu, lai atrastu informāciju

[!include[banner](../includes/banner.md)]


Sistēmā Microsoft Dynamics 365 for Operations daudziem laukiem ir uzmeklēšana, kas jums palīdz ērti atrast pareizo vai vēlamo vērtību. Uzmeklēšanai ir pievienoti vairāki uzlabojumi, vadīklas padarot ērtāk lietojamas un lietotāju darbu — vēl produktīvāku. Šajā tēmā jūs uzzināsiet par šiem jaunajiem uzmeklēšanas līdzekļiem un saņemsiet noderīgus padomus par optimālu uzmeklēšanas lietojumu sistēmā.  

<a name="responsive-lookups"></a>Reaģējoša uzmeklēšana
------------------

Iepriekšējās Dynamics 365 for Operations versijās, mijiedarbojoties ar uzmeklēšanas vadīklu, lietotājam bija īpaši jārīkojas, lai atvērtu nolaižamo izvēlni. Šīs īpašās darbības varēja būt zvaigznītes (\*) ierakstīšana vadīklā, lai uzmeklēšanu filtrētu, pamatojoties uz vadīklas pašreizējo vērtību, noklikšķināšana uz nolaižamas pogas vai tastatūras saīsnes **Alt**+**Bultiņa uz leju** lietošana. Lai labāk atbilstu pašreizējai tīmekļa praksei, uzmeklēšanas vadīklas ir modificētas tālāk aprakstītajos veidos.

-   Uzmeklēšanas nolaižamās izvēlnes tagad atveras automātiski pēc tam, kad rakstīšanā ir ieturēta neliela pauze, un nolaižamās izvēlnes saturs ir filtrēts, pamatojoties uz uzmeklēšanas vadīklas vērtību.
    -   Ņemiet vērā, ka ir atmesta iepriekšējā uzvedība ar nolaižamās izvēlnes automātisku atvēršanu pēc zvaigznītes (\*) ierakstīšanas.
-   Kad uzmeklēšanas nolaižamā izvēlne ir atvērta, notiek tālāk aprakstītais.
    -   Kursors paliek uzmeklēšanas vadīklā (fokuss netiek pārcelts uz nolaižamo izvēlni), tādēļ vadīklas vērtību varat turpināt modificēt. Taču lietotājs joprojām var izmantot taustiņus **Bultiņa uz augšu** un **Bultiņa uz leju**, lai nolaižamajā izvēlnē mainītu rindas, un taustiņu Enter, lai nolaižamajā izvēlnē atlasītu pašreizējo rindu.
    -   Pēc jebkādu uzmeklēšanas vadīklas vērtības modifikāciju veikšanas nolaižamās izvēlnes saturs pielāgojas.

Piemēram, jūs izmantojat uzmeklēšanas lauku ar nosaukumu **Pilsēta**. 

Kad fokusu pārslēdzat uz lauku **Pilsēta**, varat sākt meklēt nepieciešamo pilsētu, ierakstot dažus burtus, piemēram, “col”.  Kad pārtraucat rakstīt, uzmeklēšana tiek atvērta automātiski, un tā ir filtrēta uz pilsētām, kas sākas ar “col”. 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Pašlaik kursors joprojām ir uzmeklēšanas laukā. Ja turpināt rakstīt un šī vērtība kļūst par “column”, tad uzmeklēšanas saturs automātiski pielāgojas, lai vadīklā rādītu visjaunāko vērtību. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Lai gan fokuss joprojām atrodas uzmeklēšanas vadīklā, varat arī izmantot taustiņus **Bultiņa uz augšu** vai **Bultiņa uz leju**, lai izceltu rindu, kuru vēlaties atlasīt. Ja nospiežat taustiņu **Enter**, izceltā rinda no uzmeklēšanas tiek atlasīta un vadīklas vērtība tiek atjaunināta. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Vairāku ID ierakstīšana
Ievadot datus, lietotāji bieži kādu elementu, piemēram, debitoru vai kreditoru, cenšas identificēt ar šī elementa nosaukumu, nevis šo elementu apzīmējošo identifikatoru. Sistēmas Dynamics 365 for Operations pašreizēja versijā daudzas (bet ne visas) uzmeklēšanas tagad ļauj izmantot kontekstuālu datu ievadi. Šis iespaidīgais līdzeklis lietotājam uzmeklēšanas vadīklā ļauj ierakstīt ID vai atbilstošo nosaukumu. 

Piemēram, apsveriet lauka **Debitora konts** iespējas pārdošanas pasūtījuma izveidošanas laikā. Šajā laukā debitoram tiek rādīts **Konta ID**, bet lietotājs, veidojot pārdošanas pasūtījumu, parasti dotu priekšroku iespējai šajā laukā ierakstīt vērtību **Konta nosaukums**, nevis vērtību **Konta ID**, piemēram, “Forest Wholesales”, nevis “US-003”.

Ja lietotājs uzmeklēšanas vadīklā sāk ievadīt vērtību **Konta ID**, automātiski tiek atvērta nolaižamā izvēlne, kā aprakstīts iepriekšējā sadaļā, un lietotājs redz tālāk norādīto uzmeklēšanu.

[![Kontekstuāla uzmeklēšana, kad ir ievadīts debitora konta ID](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Taču tagad lietotājs var ievadīt arī vērtības **Konta nosaukums** sākumu. Ja tas tiek noteikts, tad lietotājam tiek parādīta tālāk norādītā uzmeklēšana. Ievērojiet, kā kolonna **Nosaukums** uzmeklēšanā ir pārvietota uz pirmo kolonnu, un kā uzmeklēšana ir sakārtota un filtrēta, pamatojoties uz kolonnu **Nosaukums**.

[![Kontekstuāla uzmeklēšana, kad ir ievadīts debitora nosaukums](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Režģa kolonnu virsrakstu lietošana detalizētai filtrēšanai un kārtošanai
Iepriekšējās divās sadaļās aprakstītie uzmeklēšanas uzlabojumi ievērojami uzlabo lietotāja spējas pārvietotie pa uzmeklēšanas rindām, uzmeklēšanā pamatojoties uz meklēšanu “sākas ar” laukā **ID** vai **Nosaukums**. Taču reizēm pareizās rindas atrašanai ir nepieciešama detalizētāka filtrēšana (vai kārtošana). Šādos gadījums lietotājam ir jāizmanto filtrēšanas un kārtošanas opcijas, kuras uzmeklēšanā ir ietvertas režģa kolonnu virsrakstos. Piemēram, pieņemsim, ka darbinieks ievada pārdošanas pasūtījuma rindu, un kā prece šim darbiniekam ir jāatrod pareizais “kabelis”. Nepietiek ar uzraksta “kabelis” ierakstīšanu vadīklā **Krājuma kods**, jo nav tādu preču nosaukumu, kas sāktos ar “kabelis”. 

![emptyitemlookup](./media/emptyitemlookup.png) 

Tā vietā lietotājam ir jānotīra uzmeklēšanas vadīklas vērtība, jāatver uzmeklēšanas nolaižamā izvēlne un jāfiltrē šī nolaižamā izvēlne, izmantojot režģa kolonnas virsrakstu, kā parādīts tālāk. Peles (vai skārienvadības) lietotājs var vienkārši noklikšķināt uz jebkuras kolonnas (vai pieskarties jebkurai kolonnai), lai piekļūtu šīs kolonnas filtrēšanas un kārtošanas opcijām. Tastatūras lietotājam ir vienkārši ir vēlreiz jānospiež taustiņu kombinācija **Alt**+**Bultiņa** **uz leju**, lai kursoru pārvietotu uz nolaižamo izvēlni, pēc tam ar tabulēšanas taustiņu ir jāpāriet uz nākamo kolonnu un tad jānospiež taustiņu kombinācija **Ctrl**+**G**, lai atvērtu režģa kolonnu virsrakstu nolaižamo izvēlni. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Pēc filtra lietošanas (skatiet nākamo attēlu) lietotājs var atrast un atlasīt rindu kā parasti. 

![filtereditemlookup](./media/filtereditemlookup.png)



