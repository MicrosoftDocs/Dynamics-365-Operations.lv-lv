---
title: Skatīt un atjaunināt entītijas datus programmā Excel
description: Šajā rakstā ir izskaidrots, kā Microsoft Excel atvērt elementa datus, pēc tam skatīt, atjaunināt un rediģēt datus, izmantojot Microsoft Dynamics Excel pievienojumprogrammu.
author: jasongre
ms.date: 05/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 388be651164af622dbabd7b2c7b3437233454bea
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108607"
---
# <a name="view-and-update-entity-data-with-excel"></a>Skatīt un atjaunināt entītijas datus programmā Excel 

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]


Šajā rakstā ir izskaidrots, kā Microsoft Excel atvērt elementa datus, pēc tam skatīt, atjaunināt un rediģēt datus, izmantojot Microsoft Dynamics Excel pievienojumprogrammu. Lai atvērtu elementa datus, varat sākties no Excel vai finanšu un operāciju programmām.

Atverot elementa datus programmā Excel, varat ātri un vienkārši apskatīt un rediģēt šos datus, izmantojot Excel pievienojumprogrammu. Šai pievienojumprogrammai ir nepieciešama programma Microsoft Excel 2016.

> [!NOTE]
> Ja jūsu Microsoft Azure Active Directory (Azure AD) nomnieks ir konfigurēts Active Directory federācijas pakalpojumu (AD FS) lietošanai, pārliecinieties, ka ir instalēts 2016. gada maija Office atjauninājums, lai Excel pievienojumprogramma varētu nodrošināt pareizu jūsu pierakstīšanu.

Lai iegūtu plašāku informāciju par Excel pievienojumprogrammas lietošanu, noskatieties īso video [Excel veidnes izveidošana galveņu un rindu modeļiem](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-a-finance-and-operations-app"></a>Atveriet elementa datus programmā Excel, kad sākat no finanšu un operāciju programmas
1. Finanšu un operāciju programmas lapā atlasiet Atvērt **Microsoft Office**.

    Ja saknes datu avots (tabula) šai lapai ir tāda pati kā saknes datu avots jebkuriem elementiem, šai lapai tiek ģenerētas noklusējuma opcijas **Atvērt programmā Excel**. Opcijas **Atvērt programmā Excel** ir atrodamas bieži izmantotajās lapās, piemēram, **Visi kreditori** un **Visi debitori**.
 
2. Atlasiet opciju **Atvērt programmā Excel** un atveriet ģenerēto darbgrāmatu. Šajā darbgrāmatā ir saistību informācija par attiecīgo elementu, rādītājs uz jūsu vidi un rādītājs uz Excel pievienojumprogrammu.
3. Programmā Excel atlasiet **Iespējot rediģēšanu**, lai iespējotu Excel pievienojumprogrammas palaišanu. Excel pievienojumprogramma darbojas rūtī, kas atrodas Excel loga labajā pusē.
4. Ja pirmo reizi palaižat Excel pievienojumprogrammu, atlasiet **Uzticēties šai pievienojumprogrammai**.
5. Ja tiek piedāvāts pieteikties, atlasiet pieteikos un pēc tam piesakieties, **izmantojot** tos pašus akreditācijas datus, kurus izmantojat, lai pieteiktos finanšu un operāciju programmā. Excel pievienojumprogramma lieto iepriekšējās pierakstīšanās kontekstu no un jūs pieraksta automātiski, ja iespējams. (Informāciju par pārlūkprogrammu, kas tiek izmantota balstoties uz operētājsistēmas, skatiet [Office pievienojumprogrammu lietotās pārlūkprogrammas](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins). Lai nodrošinātu, ka pierakstīšanās bija veiksmīga, pārbaudiet lietotājvārdu Excel pievienojumprogrammas augšējā labajā stūrī. 

Excel pievienojumprogramma automātiski nolasa datus par jūsu atlasīto elementu. Ņemiet vērā, ka darbgrāmatā nav nekādu datu, līdz Excel pievienojums tos ielasa.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Atvērt elementa datus programmā Excel, kas sākat no Excel
1. Programmas Excel cilnes **Ievietošana** grupā **Pievienojumprogrammas** atlasiet **Veikals**, lai atvērtu pakalpojumu Office veikals.
2. Pakalpojumā Office veikals meklējiet pēc atslēgvārda **Dynamics** un pēc tam atlasiet vienumu **Pievienot**, kas atrodas blakus vienumam **Microsoft Dynamics Office pievienojumprogramma** (Excel pievienojumprogramma).
3. Ja pirmo reizi palaižat Excel pievienojumprogrammu, atlasiet **Uzticēties šai pievienojumprogrammai**, lai iespējotu Excel pievienojumprogrammas palaišanu. Excel pievienojumprogramma darbojas rūtī, kas atrodas Excel loga labajā pusē.
4. Atlasiet **Pievienot servera informāciju**, lai atvērtu rūti **Opcijas**.
5. Pārlūkā nokopējiet mērķa finanšu un operāciju programmas instances URL, **ielīmējiet to laukā Servera URL** un pēc tam dzēsiet visu pēc hostdatora nosaukuma. Iegūtajam URL ir jāsatur tikai resursdatora nosaukums.

    Piemēram, ja URL ir `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, dzēsiet visu, izņemot `https://xxx.dynamics.com`.

6. Atlasiet **Labi** un pēc tam atlasiet **Jā**, lai apstiprinātu izmaiņas. Excel pievienojumprogramma tiek restartēta, un tajā tiek ielādēti metadati.

    Tagad ir pieejama poga **Dizains**. Ja Excel pievienojumprogrammai ir poga **Ielādēt sīkprogrammas**, visticamāk, jūs neesat pierakstījies kā pareizais lietotājs. Papildinformāciju par šīs problēmas novēršanai skatiet sadaļā [Noslodzes](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) problēmu novēršanas ieraksts.

7. Atlasiet **Dizains**. Excel pievienojumprogramma izgūst elementa metadatus.
8. Atlasiet **Pievienot tabulu**. Tiek parādīts elementu saraksts. Elementi ir uzskaitīti formātā “Nosaukums - Etiķete”.
9. Sarakstā atlasiet kādu elementu, piemēram, **Debitors — debitori**, un pēc tam atlasiet **Tālāk**.
10. Lai kādu lauku no saraksta **Pieejamie lauki** pievienotu sarakstam **Atlasītie lauki**, atlasiet attiecīgo lauku un pēc tam atlasiet **Pievienot**. Vai arī veiciet dubultklikšķi uz lauka sarakstā **Pieejamie lauki**.
11. Kad esat pabeidzis pievienot laukus sarakstam **Atlasītie lauki**, pārliecinieties, ka kursors atrodas pareizajā darblapas vietā (piemēram, A1 šūnā), un pēc tam atlasiet **Gatavs**. Pēc tam atlasiet **Gatavs**, lai aizvērtu noformētāju.
12. Atlasiet **Atsvaidzināt**, lai ievilktu datu kopu.

## <a name="view-and-update-entity-data-in-excel"></a>Skatīt un atjaunināt elementa datus programmā Excel
Kad Excel pievienojumprogramma ir ielasījusi elementa datus darbgrāmatā, varat jebkurā brīdī atjaunināt šos datus, Excel pievienojumprogrammā atlasot **Atsvaidzināt**.

## <a name="edit-entity-data-in-excel"></a>Rediģēt elementa datus programmā Excel
Elementa datus varat mainīt pēc savas izvēles un pēc tam publicēt atpakaļ finanšu un operāciju lietojumprogrammās, **atlasot** Publicēt Excel pievienojumprogrammai. Lai rediģētu kādu ierakstu, darblapā atlasiet kādu šūnu un pēc tam mainiet šīs šūnas vērtību. Lai pievienotu jaunu ierakstu, izpildiet tālāk aprakstītās darbības.

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

## <a name="change-the-publish-batch-size"></a>Mainiet publicēšanas partijas lielumu
Kad lietotāji publicē izmaiņas datu ierakstos, izmantojot Excel pievienojumprogrammu, atjauninājumi tiek iesniegti paketēs. Noklusējuma (un maksimālā) publicēšanas partijas lielums ir 100 rindas; **Tomēr publicēšanas paketes lieluma atļaut konfigurācija Excel pievienojumprogrammas līdzekļa ļauj jums elastīgāk publicēt partijas lielumu, it īpaši, ja, mēģinot publicēt atjauninājumus no Excel**, redzēt taimautus.

Sistēmas administratori var norādīt visas sistēmas ierobežojumu publicēšanas paketes lielumam darbgrāmatām "Atvērt Excel", iestatot lauku **Partijas ierobežojuma publicēšana** **Office lietojumprogrammas parametru** lapas sadaļā **Lietojumprogrammas parametri**.

Publicēšanas paketes lielumu var arī mainīt atsevišķai darbgrāmatai, izmantojot Excel pievienojumprogrammu.

1. Atveriet darbgrāmatu programmā Excel.
2. Excel pievienojumprogrammas augšējā labajā stūrī atlasiet pogu **Opcijas** (zobrata ikona).
3. Pēc izvēles iestatiet lauku **Publicēt partijas lielumu**. Jūsu iestatītās vērtības vērtībai ir jābūt mazākai par sistēmas mēroga publicēšanas paketes ierobežojumu.
4. Atlasiet **Labi**.
5. Saglabājiet darbgrāmatu. Ja darbgrāmatu nesaglabāsit pēc pievienojumprogrammu iestatījumu izmaiņu veikšanas, šīs izmaiņas netiks saglabātas, atverot darbgrāmatu atkārtoti.

Excel darbgrāmatas veidņu autori var izmantot to pašu procedūru, lai iestatītu publicēšanas paketes lielumu veidnēm, pirms tās tiek augšupielādētas sistēmā.

## <a name="copy-environment-data"></a>Kopēt vides datus

No vienas vides darblapā ielasītos datus var kopēt uz citu vidi. Taču jūs nevarat vienkārši mainīt savienojuma URL, jo darblapas datu kešatmiņā dati joprojām tiks apstrādāti kā esoši dati. Tā vietā ir jāizmanto funkcionalitāte Kopēt vides datus, lai publicētu datus jaunā vidē kā jaunus datus.

1. Atlasiet pogu **Opcijas** (zobrata simbolu) un pēc tam kopsavilkuma cilnē **Datu savienotājs** atlasiet **Kopēt vides datus**. 
2. Ievadiet jaunās vides servera URL. 
3. Atlasiet **Labi** un pēc tam atlasiet **Jā**, lai apstiprinātu darbību. Excel pievienojumprogramma tiek restartēta, un tajā tiek izveidots savienojums ar jauno vidi. Visi darbgrāmatā esošie dati tiek apstrādāti kā jauni dati.

    Pēc Excel pievienojumprogrammas restartēšanas tiek parādīts ziņojuma lodziņš ar informāciju, ka darbgrāmata ir pārslēgta vides kopēšanas režīmā.

4. Lai kopētu datus uz jauno vidi kā jaunus datus, atlasiet **Publicēt**. Lai atceltu vides kopēšanas operāciju un pārskatītu jaunajā vidē esošos datus, atlasiet **Atsvaidzināt**.

## <a name="troubleshooting"></a>Problēmu novēršana
Noteiktas problēmas var atrisināt ar dažām vienkāršām darbībām.

- **Tiek parādīta noslodzes saite** – Papildinformāciju par šīs problēmas novēršanai skatiet sadaļā [Noslodzes](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) problēmu novēršanas ieraksts. 
- **Saņemat ziņojumu “Aizliegts”**  — ja laikā, kad Excel pievienojumprogrammā notiek metadatu ielāde, saņemat ziņojumu “Aizliegts”, tad kontam, kas ir izmantots, lai pierakstītos Excel pievienojumprogrammā, nav atļaujas lietot attiecīgo pakalpojumu, instanci vai datu bāzi. Lai atrisinātu šo problēmu, pārbaudiet, vai Excel pievienojumprogrammas labajā augšējā stūrī tiek rādīts pareizais lietotājvārds. Ja tiek rādīts nepareizs lietotājvārds, atlasiet to, izrakstieties un pēc tam atkal pierakstieties.
- **Virs programmas Excel tiek rādīta tukša tīmekļa lapa** — ja pierakstīšanās procesa laikā tiek atvērta tukša tīmekļa lapa, tad kontam ir nepieciešams AD FS, bet Excel versija, kurā darbojas Excel pievienojumprogramma, ir pārāk veca, lai ielādētu pierakstīšanās dialoglodziņu. Lai atrisinātu šo problēmu, atjauniniet izmantoto Excel versiju. Lai atjauninātu Excel versiju, kad esat uzņēmumā, kurš atrodas atliktajā kanālā, izmantojiet [Office izvietošanas rīku](/deployoffice/overview-office-deployment-tool), lai [no atliktā kanāla pārietu uz pašreizējo kanālu](/deployoffice/overview-update-channels).
- **Datu izmaiņās publicēšanas laikā tiek saņemts taimauts** - ja saņemat taimauta ziņojumus, mēģinot publicēt datu izmaiņas entītijā, apsveriet iespēju samazināt ietekmētās darbgrāmatas publicēšanas paketes lielumu. Entītijas, kas ieraksta izraisīs lielāku loģikas apjomu, iespējams, būs jāsūta atjauninājumi mazākās paketēs, lai palīdzētu novērst taimautus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

