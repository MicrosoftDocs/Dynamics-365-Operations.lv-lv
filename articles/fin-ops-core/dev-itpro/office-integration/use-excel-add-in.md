---
title: Elementa datu atvēršana programmā Excel un to atjaunināšana, izmantojot Excel pievienojumprogrammu
description: Šajā tēmā ir paskaidrots, kā elementa datus atvērt programmā Microsoft Excel un pēc tam šos datus apskatīt, atjaunināt un rediģēt, izmantojot Microsoft Dynamics Office pievienojumprogrammu programmai Excel.
author: ChrisGarty
manager: AnnBe
ms.date: 04/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 210231bb442928674b490d83f50bf787d7bfa60c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181017"
---
# <a name="open-entity-data-in-excel-and-update-it-by-using-the-excel-add-in"></a>Elementa datu atvēršana programmā Excel un to atjaunināšana, izmantojot Excel pievienojumprogrammu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā elementa datus atvērt programmā Microsoft Excel un pēc tam šos datus apskatīt, atjaunināt un rediģēt, izmantojot Microsoft Dynamics Office pievienojumprogrammu programmai Excel. Lai atvērtu elementa datus, varat sākt no programmas Excel vai Finance and Operations.

Atverot elementa datus programmā Excel, varat ātri un vienkārši apskatīt un rediģēt šos datus, izmantojot Excel pievienojumprogrammu. Šai pievienojumprogrammai ir nepieciešama programma Microsoft Excel 2016.

> [!NOTE]
> Ja jūsu Microsoft Azure Active Directory (Azure AD) nomnieks ir konfigurēts Active Directory federācijas pakalpojumu (AD FS) lietošanai, pārliecinieties, ka ir instalēts 2016. gada maija Office atjauninājums, lai Excel pievienojumprogramma varētu nodrošināt pareizu jūsu pierakstīšanu.

Lai iegūtu plašāku informāciju par Excel pievienojumprogrammas lietošanu, noskatieties īso video [Excel veidnes izveidošana virsrakstu un rindu modeļiem programmatūrā Dynamics 365 for Finance and Operations](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-finance-and-operations"></a>Elementa datu atvēršana programmā Excel, sākot darbu programmā Finance and Operations
1. Kādā programmas Finance and Operations lapā atlasiet **Atvērt, izmantojot Microsoft Office**.

    Ja saknes datu avots (tabula) šai lapai ir tāda pati kā saknes datu avots jebkuriem elementiem, šai lapai tiek ģenerētas noklusējuma opcijas **Atvērt programmā Excel**. Opcijas **Atvērt programmā Excel** ir atrodamas bieži izmantotajās lapās, piemēram, **Visi kreditori** un **Visi debitori**.
 
2. Atlasiet opciju **Atvērt programmā Excel** un atveriet ģenerēto darbgrāmatu. Šajā darbgrāmatā ir saistību informācija par attiecīgo elementu, rādītājs uz jūsu vidi un rādītājs uz Excel pievienojumprogrammu.
3. Programmā Excel atlasiet **Iespējot rediģēšanu**, lai iespējotu Excel pievienojumprogrammas palaišanu. Excel pievienojumprogramma darbojas rūtī, kas atrodas Excel loga labajā pusē.
4. Ja pirmo reizi palaižat Excel pievienojumprogrammu, atlasiet **Uzticēties šai pievienojumprogrammai**.
5. Ja tiek prasīts pierakstīties, atlasiet **Pierakstīties** un pēc tam pierakstieties, izmantojot tos pašus akreditācijas datus, ko izmantojāt, lai pierakstītos programmā Finance and Operations. Excel pievienojumprogramma lieto iepriekšējās pierakstīšanās kontekstu no Internet Explorer un jūs pieraksta automātiski, ja iespējams. Tādēļ pārbaudiet lietotājvārdu Excel pievienojumprogrammas labajā augšējā stūrī.

Excel pievienojumprogramma automātiski nolasa datus par jūsu atlasīto elementu. Ņemiet vērā, ka darbgrāmatā nav nekādu datu, līdz Excel pievienojums tos ielasa.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Atvērt elementa datus programmā Excel, kas sākat no Excel
1. Programmas Excel cilnes **Ievietošana** grupā **Pievienojumprogrammas** atlasiet **Veikals**, lai atvērtu pakalpojumu Office veikals.
2. Pakalpojumā Office veikals meklējiet pēc atslēgvārda **Dynamics** un pēc tam atlasiet vienumu **Pievienot**, kas atrodas blakus vienumam **Microsoft Dynamics Office pievienojumprogramma** (Excel pievienojumprogramma).
3. Ja pirmo reizi palaižat Excel pievienojumprogrammu, atlasiet **Uzticēties šai pievienojumprogrammai**, lai iespējotu Excel pievienojumprogrammas palaišanu. Excel pievienojumprogramma darbojas rūtī, kas atrodas Excel loga labajā pusē.
4. Atlasiet **Pievienot servera informāciju**, lai atvērtu rūti **Opcijas**.
5. Pārlūkprogrammā nokopējiet mērķa Finance and Operations instances URL, ielīmējiet to laukā **Servera URL** un pēc tam izdzēsiet visus simbolus, kas seko resursdatora nosaukumam. Iegūtajam URL ir jāsatur tikai resursdatora nosaukums.

    Piemēram, ja URL ir `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, dzēsiet visu, izņemot `https://xxx.dynamics.com`.

6. Atlasiet **Labi** un pēc tam atlasiet **Jā**, lai apstiprinātu izmaiņas. Excel pievienojumprogramma tiek restartēta, un tajā tiek ielādēti metadati.

    Tagad ir pieejama poga **Dizains**. Ja Excel pievienojumprogrammai ir poga **Ielādēt sīkprogrammas**, visticamāk, jūs neesat pierakstījies kā pareizais lietotājs. Papildinformāciju skatiet šīs tēmas sadaļas [Problēmu novēršana](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting) apakšsadaļā “Tiek rādīta poga Ielādēt sīkprogrammas”.

7. Atlasiet **Noformējums**. Excel pievienojumprogramma izgūst elementa metadatus.
8. Atlasiet **Pievienot tabulu**. Tiek parādīts elementu saraksts. Elementi ir uzskaitīti formātā “Nosaukums - Etiķete”.
9. Sarakstā atlasiet kādu elementu, piemēram, **Debitors — debitori**, un pēc tam atlasiet **Tālāk**.
10. Lai kādu lauku no saraksta **Pieejamie lauki** pievienotu sarakstam **Atlasītie lauki**, atlasiet attiecīgo lauku un pēc tam atlasiet **Pievienot**. Vai arī veiciet dubultklikšķi uz lauka sarakstā **Pieejamie lauki**.
11. Kad esat pabeidzis pievienot laukus sarakstam **Atlasītie lauki**, pārliecinieties, ka kursors atrodas pareizajā darblapas vietā (piemēram, A1 šūnā), un pēc tam atlasiet **Gatavs**. Pēc tam atlasiet **Gatavs**, lai aizvērtu noformētāju.
12. Atlasiet **Atsvaidzināt**, lai ievilktu datu kopu.

## <a name="view-and-update-entity-data-in-excel"></a>Skatīt un atjaunināt elementa datus programmā Excel
Kad Excel pievienojumprogramma ir ielasījusi elementa datus darbgrāmatā, varat jebkurā brīdī atjaunināt šos datus, Excel pievienojumprogrammā atlasot **Atsvaidzināt**.

## <a name="edit-entity-data-in-excel"></a>Rediģēt elementa datus programmā Excel
Varat pēc nepieciešamības mainīt elementa datus un pēc tam tos publicēt atpakaļ, Excel pievienojumprogrammā atlasot **Publicēt**. Lai rediģētu kādu ierakstu, darblapā atlasiet kādu šūnu un pēc tam mainiet šīs šūnas vērtību. Lai pievienotu jaunu ierakstu, izpildiet tālāk aprakstītās darbības.

- Noklikšķiniet jebkurā datu avotu tabulas vietā un pēc tam Excel pievienojumprogrammā atlasiet **Jauns**.
- Noklikšķiniet jebkurā vietā pēdējā datu avotu tabulas rindā un pēc tam nospiediet tabulēšanas taustiņu, līdz kursors tiek pārvietots ārā no pēdējās kolonnas šajā rindā un tiek izveidota jauna rinda.
- Noklikšķiniet jebkurā vietā rindā, kas atrodas tieši zem datu avotu tabulas, un sāciet datu ievadi šūnā. Kad fokusu pārslēdzat ārpus šīs šūnas, tabula izplešas, lai iekļautu jauno rindu.
- Lai izveidotu virsraksta ierakstu lauku saistības, atlasiet kādu no laukiem un pēc tam Excel pievienojumprogrammā atlasiet **Jauns**.

Ņemiet vērā, ka jaunu ierakstu var izveidot tikai tad, ja visi galvenie un obligātie lauki darblapā ir saistīti vai ja noklusējuma vērtības tika aizpildītas, izmantojot filtra nosacījumu.

Lai dzēstu kādu ierakstu, izpildiet tālāk aprakstītās darbības.

- Ar peles labo pogu noklikšķiniet uz rindas numura blakus dzēšamajai darblapas rindai un pēc tam atlasiet **Dzēst**.
- Ar peles labo pogu noklikšķiniet jebkurā vietā dzēšamajā darbplūsmas rindā un pēc tam atlasiet **Dzēst** &gt; **Tabulas rindas**.

Ja datu avoti ir pievienoti kā saistīti datu avoti, virsraksts tiek publicēts pirms rindām. Ja pastāv atkarības starp citiem datu avotiem, iespējams, ir jāmaina noklusējuma publicēšanas secība. Lai mainītu publicēšanas secību, Excel pievienojumprogrammā atlasiet pogu **Opcijas** (zobrata simbolu) un pēc tam kopsavilkuma cilnē **Datu savienotājs** atlasiet **Konfigurēt publicēšanas secību**.

## <a name="add-or-remove-columns"></a>Pievienot vai noņemt kolonnas
Varat izmantot veidotāju, lai regulētu kolonnas, kuras darblapai ir pievienotas automātiski.

> [!NOTE]
> Ja Excel pievienojumprogrammā zem pogas **Filtrs** netiek parādīta poga **Noformējums**, ir jāiespējo datu avota noformētājs. Atlasiet pogu **Opcijas** (zobrata ikonu) un pēc tam atzīmējiet izvēles rūtiņu **Iespējot noformējumu**.

1. Excel pievienojumprogrammā atlasiet **Noformējums**. Ir uzskaitīti visi datu avoti.
2. Atlasiet pogu **Rediģēt** (zīmuļa simbolu) blakus datu avotam.
3. Sarakstā **Atlasītie lauki** pēc nepieciešamības pielāgojiet lauku sarakstu.

    - Lai kādu lauku no saraksta **Pieejamie lauki** pievienotu sarakstam **Atlasītie lauki**, atlasiet attiecīgo lauku un pēc tam atlasiet **Pievienot**. Vai arī veiciet dubultklikšķi uz lauka sarakstā **Pieejamie lauki**.
    - Lai noņemtu lauku no saraksta **Atlasītie lauki**, atlasiet lauku un pēc tam atlasiet **Noņemt**. Vai arī veiciet dubultklikšķi uz attiecīgā lauka.
    - Lai mainītu laiku secību sarakstā **Atlasītie lauki**, atlasiet lauku un pēc tam atlasiet **Uz augšu** vai **Uz leju**.

4. Lai lietotu veiktās izmaiņas datu avotam, atlasiet **Atjaunināt**. Pēc tam atlasiet **Gatavs**, lai aizvērtu noformētāju.
5. Ja pievienojāt lauku (kolonnu), atlasiet **Atsvaidzināt**, lai ievilktu atjauninātu datu kopu.

## <a name="copy-environment-data"></a>Kopēt vides datus

No vienas vides darblapā ielasītos datus var kopēt uz citu vidi. Taču jūs nevarat vienkārši mainīt savienojuma URL, jo darblapas datu kešatmiņā dati joprojām tiks apstrādāti kā esoši dati. Tā vietā ir jāizmanto funkcionalitāte Kopēt vides datus, lai publicētu datus jaunā vidē kā jaunus datus.

1. Atlasiet pogu **Opcijas** (zobrata simbolu) un pēc tam kopsavilkuma cilnē **Datu savienotājs** atlasiet **Kopēt vides datus**. 
2. Ievadiet jaunās vides servera URL. 
3. Atlasiet **Labi** un pēc tam atlasiet **Jā**, lai apstiprinātu darbību. Excel pievienojumprogramma tiek restartēta, un tajā tiek izveidots savienojums ar jauno vidi. Visi darbgrāmatā esošie dati tiek apstrādāti kā jauni dati.

    Pēc Excel pievienojumprogrammas restartēšanas tiek parādīts ziņojuma lodziņš ar informāciju, ka darbgrāmata ir pārslēgta vides kopēšanas režīmā.

4. Lai kopētu datus uz jauno vidi kā jaunus datus, atlasiet **Publicēt**. Lai atceltu vides kopēšanas operāciju un pārskatītu jaunajā vidē esošos datus, atlasiet **Atsvaidzināt**.

## <a name="troubleshooting"></a>Problēmu novēršana
Noteiktas problēmas var atrisināt ar dažām vienkāršām darbībām.

- **Tiek rādīta poga Ielādēt sīkprogrammas** — ja pēc pierakstīšanās Excel pievienojumprogrammai tiek rādīta poga **Ielādēt sīkprogrammas**, visticamāk, esat pierakstījies, izmantojot nepareizu lietotāja kontu. Lai atrisinātu šo problēmu, pārbaudiet, vai Excel pievienojumprogrammas labajā augšējā stūrī tiek rādīts pareizais lietotājvārds. Ja tiek rādīts nepareizs lietotājvārds, atlasiet to, izrakstieties un pēc tam atkal pierakstieties.
- **Saņemat ziņojumu “Aizliegts”**  — ja laikā, kad Excel pievienojumprogrammā notiek metadatu ielāde, saņemat ziņojumu “Aizliegts”, tad kontam, kas ir izmantots, lai pierakstītos Excel pievienojumprogrammā, nav atļaujas lietot attiecīgo pakalpojumu, instanci vai datu bāzi. Lai atrisinātu šo problēmu, pārbaudiet, vai Excel pievienojumprogrammas labajā augšējā stūrī tiek rādīts pareizais lietotājvārds. Ja tiek rādīts nepareizs lietotājvārds, atlasiet to, izrakstieties un pēc tam atkal pierakstieties.
- **Virs programmas Excel tiek rādīta tukša tīmekļa lapa** — ja pierakstīšanās procesa laikā tiek atvērta tukša tīmekļa lapa, tad kontam ir nepieciešams AD FS, bet Excel versija, kurā darbojas Excel pievienojumprogramma, ir pārāk veca, lai ielādētu pierakstīšanās dialoglodziņu. Lai atrisinātu šo problēmu, atjauniniet izmantoto Excel versiju. Lai atjauninātu Excel versiju, kad esat uzņēmumā, kurš atrodas atliktajā kanālā, izmantojiet [Office izvietošanas rīku](https://technet.microsoft.com/library/jj219422.aspx), lai [no atliktā kanāla pārietu uz pašreizējo kanālu](https://technet.microsoft.com/library/mt455210.aspx).
