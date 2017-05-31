---
title: Lietot Excel pievienojumprogrammu
description: "Šajā tēmā ir paskaidrots, kā elementa datus atvērt programmā Microsoft Excel un pēc tam šos datus apskatīt, atjaunināt un rediģēt, izmantojot Microsoft Dynamics Office pievienojumprogrammu programmai Excel. Lai atvērtu elementa datus, varat sākt no programmas Excel vai no sistēmas Microsoft Dynamics 365 for Operations."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c391fb70d837db9c0f167b392291fc1c5cc2bb53
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="use-the-excel-add-in"></a>Lietot Excel pievienojumprogrammu

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā elementa datus atvērt programmā Microsoft Excel un pēc tam šos datus apskatīt, atjaunināt un rediģēt, izmantojot Microsoft Dynamics Office pievienojumprogrammu programmai Excel. Lai atvērtu elementa datus, varat sākt no programmas Excel vai no sistēmas Microsoft Dynamics 365 for Operations.

Atverot elementa datus programmā Microsoft Excel, šos datus varat ātri un vienkārši apskatīt un rediģēt, izmantojot Microsoft Dynamics Office pievienojumprogrammu programmai Excel. Šai pievienojumprogrammai ir nepieciešama programma Microsoft Excel 2016. **Piezīme.** Ja jūsu Microsoft Azure Active Directory (Azure AD) nomnieks ir konfigurēts Active Directory federācijas pakalpojumu (AD FS) lietošanai, jums ir jānodrošina, ka ir lietots 2016. gada maija atjauninājums, lai Excel pievienojumprogramma jūs varētu pierakstīt pareizi.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Atvērt elementa datus programmā Excel, kas sākat no Dynamics 365 for Operations
1.  Kādā sistēmas Microsoft Dynamics 365 for Operations lapā noklikšķiniet uz **Atvērt, izmantojot Microsoft Office**. Ja saknes datu avots (tabula) šai lapai ir tāda pati kā saknes datu avots jebkuriem elementiem, šai lapai tiek ģenerētas noklusējuma opcijas **Atvērt programmā Excel**. Opcijas **Atvērt programmā Excel** ir atrodamas bieži izmantotajās lapās, piemēram, **Visi kreditori** un **Visi debitori**.
2.  Noklikšķiniet uz kādas opcijas **Atvērt programmā Excel**, un atveriet ģenerēto darbgrāmatu. Šajā darbgrāmatā ir saistību informācija par attiecīgo elementu, rādītājs uz jūsu vidi un rādītājs uz Excel pievienojumprogrammu.
3.  Programmā Excel noklikšķiniet uz **Iespējot rediģēšanu**, lai iespējotu Excel pievienojumprogrammas palaišanu. Excel pievienojumprogramma darbojas rūtī, kas atrodas Excel loga labajā pusē.
4.  Ja Excel pievienojumprogrammu palaižat pirmo reizi, noklikšķiniet uz **Uzticēties šai pievienojumprogrammai**.
5.  Ja tiek prasīts pierakstīties, noklikšķiniet uz **Pierakstīties** un pēc tam pierakstieties, izmantojot tos pašus akreditācijas datus, ko izmantojāt, lai pierakstītos sistēmā Dynamics 365 for Operations. Excel pievienojumprogramma lieto iepriekšējās pierakstīšanās kontekstu no Internet Explorer un jūs pieraksta automātiski, ja iespējams. Tādēļ pārbaudiet lietotājvārdu Excel pievienojumprogrammas labajā augšējā stūrī.

Excel pievienojumprogramma automātiski nolasa datus par jūsu atlasīto elementu. Ņemiet vērā, ka darbgrāmatā nav nekādu datu, līdz Excel pievienojums tos ielasa.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Atvērt elementa datus programmā Excel, kas sākat no Excel
1.  Programmā Excel, cilnē **Iespraust**, grupā **Pievienojumprogrammas** noklikšķiniet uz **Veikals**, lai atvērtu Office veikalu.
2.  Office veikalā meklējiet pēc atslēgvārda “Dynamics” un noklikšķiniet uz **Pievienot** blakus vienumam **Microsoft Dynamics Office pievienojumprogramma** (Excel pievienojumprogramma).
3.  Ja Excel pievienojumprogrammu palaižat pirmo reizi, noklikšķiniet uz **Uzticēties šai pievienojumprogrammai**, lai šai Excel pievienojumprogrammai ļautu darboties. Excel pievienojumprogramma darbojas rūtī, kas atrodas Excel loga labajā pusē.
4.  Noklikšķiniet uz **Pievienot servera informāciju**, lai atvērtu rūti **Opcijas**.
5.  Nokopējiet pārlūkprogrammas vietrādi URL no savas mērķa Dynamics 365 for Operations instances, ielīmējiet to laukā **Servera URL** un pēc tam izdzēsiet visu aiz resursdatora nosaukuma. Rezultātā iegūtajam vietrādim URL vajadzētu būt tikai resursdatora nosaukumam.
Piemēram, ja vietrādis URL ir https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage, tad izdzēsiet visu, izņemot **https://xxx.dynamics.com**.
6.  Noklikšķiniet uz **Labi** un pēc tam noklikšķiniet uz **Jā**, lai apstiprinātu veiktās izmaiņas. Excel pievienojumprogramma restartējas un ielādē metadatus. Tagad ir pieejama poga **Dizains**. Ja Excel pievienojumprogrammai ir poga **Ielādēt sīkprogrammas**, visticamāk, jūs neesat pierakstījies kā pareizais lietotājs. Papildinformāciju skatiet šīs tēmas sadaļas “Problēmu novēršana” punktā “Tiek rādīta poga Ielādēt sīkprogrammas”.
7.  Noklikšķiniet uz **Dizains**. Excel pievienojumprogramma izgūst elementa metadatus.
8.  Noklikšķiniet uz **Pievienot tabulu**. Tiek parādīts elementu saraksts. Elementi ir uzskaitīti formātā “Nosaukums - Etiķete”.
9.  Sarakstā atlasiet kādu elementu, piemēram, **Debitors - Debitori**, un pēc tam noklikšķiniet uz **Tālāk**.
10. Lai kādu lauku no saraksta **Pieejamie lauki** pievienotu sarakstam **Atlasītie lauki**, noklikšķiniet uz attiecīgā lauka un pēc tam noklikšķiniet uz **Pievienot**. Vai arī veiciet dubultklikšķi uz attiecīgā lauka.
11. Kad esat beidzis pievienot laukus sarakstam **Atlasītie lauki**, pārliecinieties, ka kursors atrodas pareizajā darblapas vietā (piemēram, šūnā A1), un pēc tam noklikšķiniet uz **Gatavs**. Pēc tam noklikšķiniet uz **Gatavs**, lai aizvērtu veidotāju.
12. Noklikšķiniet uz **Atsvaidzināt**, lai ievilktu kādu datu kopu.

## <a name="view-and-update-entity-data-in-excel"></a>Skatīt un atjaunināt elementa datus programmā Excel
Kad Excel pievienojumprogramma elementa datus ielasa darbgrāmatā, šos datus jebkurā laikā varat atjaunināt, Excel pievienojumprogrammā noklikšķinot uz **Atsvaidzināt**.

## <a name="edit-entity-data-in-excel"></a>Rediģēt elementa datus programmā Excel
Elementa datus pēc nepieciešamības varat mainīt un pēc tam tos publicēt atpakaļ, Excel pievienojumprogrammā noklikšķinot uz **Publicēt**. Lai rediģētu kādu ierakstu, darblapā atlasiet kādu šūnu un pēc tam mainiet šīs šūnas vērtību. Lai pievienotu jaunu ierakstu, izpildiet tālāk aprakstītās darbības.

-   Noklikšķiniet jebkurā datu avotu tabulas vietā un pēc tam Excel pievienojumprogrammā noklikšķiniet uz **Jauns**.
-   Noklikšķiniet uz pēdējās rindas datu avotu tabulā un pēc tam spiediet tabulēšanas taustiņu, līdz kursors izkļūst no pēdējas kolonnas šajā rindā un tiek izveidota jauna rinda.
-   Noklikšķiniet uz rindas, kas atrodas tieši zem datu avotu tabulas, un sāciet šūnā ievadīt datus. Kad fokusu pārslēdzat ārpus šīs šūnas, tabula izplešas, lai iekļautu jauno rindu.
-   Lai iegūtu virsraksta ierakstu lauku saistības, noklikšķiniet uz kāda no laukiem un pēc tam Excel pievienojumprogrammā noklikšķiniet uz **Jauns**.

Ņemiet vērā, ka jaunu ierakstu var izveidot tikai tad, ja visi galvenie un obligātie lauki darblapā ir saistīti vai ja noklusējuma vērtības tika aizpildītas, izmantojot filtra nosacījumu.
Lai dzēstu kādu ierakstu, izpildiet tālāk aprakstītās darbības.

-   Ar peles labo pogu noklikšķiniet uz rindas numura blakus darblapas rindai, kuru vēlaties dzēst, un pēc tam noklikšķiniet uz **Dzēst**.
-   Ar peles labo pogu noklikšķiniet darblapas rindā, kuru vēlaties dzēst, un pēc tam noklikšķiniet uz **Dzēst** &gt; **Tabulas rindas**.
Ja datu avoti ir pievienoti kā saistīti, tad virsraksts tiek publicēts pirms rindām. Ja pastāv atkarības starp citiem datu avotiem, iespējams, ir jāmaina noklusējuma publicēšanas secība. Lai mainītu publicēšanas secību, Excel pievienojumprogrammā noklikšķiniet uz pogas **Opcijas** (zobrata simbols). Pēc tam kopsavilkuma cilnē **Datu savienotājs** noklikšķiniet uz **Konfigurēt publicēšanas secību**.

## <a name="add-or-remove-columns"></a>Pievienot vai noņemt kolonnas
Varat izmantot veidotāju, lai regulētu kolonnas, kuras darblapai ir pievienotas automātiski.

1.  Palaidiet Excel pievienojumprogrammas datu avota veidotāju, noklikšķinot uz pogas **Opcijas** (zobrata simbols) un pēc tam atzīmējot izvēles rūtiņu **Iespējot dizainu**.
2.  Excel pievienojumprogrammā noklikšķiniet uz **Dizains**. Ir uzskaitīti visi datu avoti.
3.  Blakus datu avotam noklikšķiniet uz pogas **Rediģēt** (zīmuļa simbols).
4.  Pēc nepieciešamības pielāgojiet sarakstu **Atlasītie lauki** tālāk aprakstītajā veidā.
    -   Lai kādu lauku no saraksta **Pieejamie lauki** pievienotu sarakstam **Atlasītie lauki**, noklikšķiniet uz attiecīgā lauka un pēc tam noklikšķiniet uz **Pievienot**. Vai arī veiciet dubultklikšķi uz attiecīgā lauka.
    -   Lai no saraksta **Atlasītie lauki** noņemtu kādu lauku, noklikšķiniet uz šī lauka un pēc tam noklikšķiniet uz **Noņemt**. Vai arī veiciet dubultklikšķi uz attiecīgā lauka.
    -   Lai mainītu lauku secību, noklikšķiniet uz lauka sarakstā **Atlasītie lauki**, noklikšķiniet uz kāda lauka un pēc tam klikšķiniet uz **Uz augšu** vai **Uz leju**.

5. Lai datu avotam stātos spēkā veiktās izmaiņas, noklikšķiniet uz **Atjaunināt**. Pēc tam noklikšķiniet uz **Gatavs**, lai aizvērtu veidotāju. 
6. Ja pievienojāt kādu lauku (kolonnu), noklikšķiniet uz **Atsvaidzināt**, lai ievilktu atjauninātu datu pogu.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Problēmu novēršana
Noteiktas problēmas var atrisināt ar dažām vienkāršām darbībām.

-   **Tiek rādīta poga Ielādēt sīkprogrammas.** Ja pēc pierakstīšanās Excel pievienojumprogrammai ir poga **Ielādēt sīkprogrammas**, visticamāk, jūs neesat pierakstījies kā pareizais lietotājs. Lai atrisinātu šo problēmu, pārbaudiet, vai Excel pievienojumprogrammas labajā augšējā stūrī tiek rādīts pareizais lietotājvārds. Ja tiek rādīts nepareizs lietotājvārds, noklikšķiniet uz tā, izrakstieties un pēc tam pierakstieties atpakaļ.
-   **Jūs saņemat ziņojumu “Aizliegts”.** Ja saņemat ziņojumu “Aizliegts”, kamēr Excel pievienojumprogramma ielādē metadatus, tad kontam, kurš ir pierakstījies Excel pievienojumprogrammā, nav atļauju lietot attiecīgo pakalpojumu, instanci vai datu bāzi. Lai atrisinātu šo problēmu, pārbaudiet, vai Excel pievienojumprogrammas labajā augšējā stūrī tiek rādīts pareizais lietotājvārds. Ja tiek rādīts nepareizs lietotājvārds, noklikšķiniet uz tā, izrakstieties un pēc tam pierakstieties atpakaļ.
-   **Pār programmu Excel tiek rādīta tukša tīmekļa lapa.** Ja pierakstīšanās procesa laikā tiek atvērta tukša tīmekļa lapa, tad kontam ir nepieciešams AD FS, bet Excel versija, kurā darbojas pievienojumprogramma, nav pietiekami jauna, lai ielādētu pierakstīšanās dialoglodziņu. Lai atrisinātu šo problēmu, atjauniniet izmantoto Excel versiju. Lai atjauninātu Excel versiju, kad esat uzņēmumā, kurš atrodas atliktajā kanālā, izmantojiet [Office izvietošanas rīku](https://technet.microsoft.com/library/jj219422.aspx), lai [no atliktā kanāla pārietu uz pašreizējo kanālu](https://technet.microsoft.com/library/mt455210.aspx).





