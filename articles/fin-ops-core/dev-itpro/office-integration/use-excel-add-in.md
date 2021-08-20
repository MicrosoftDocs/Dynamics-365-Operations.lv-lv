---
title: Skatīt un atjaunināt entītijas datus programmā Excel
description: Šajā tēmā ir paskaidrots, kā atvērt entītijas datus programmā Microsoft Excel un pēc tam skatīt, atjaunināt un rediģēt tos, izmantojot Microsoft Dynamics Office pievienojumprogrammu programmai Excel.
author: jasongre
ms.date: 01/22/2021
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
ms.openlocfilehash: aefebe094a0429f22a1a7038a55ab2190e41da6348447850148b8b98e082e743
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761358"
---
# <a name="view-and-update-entity-data-with-excel"></a>Skatīt un atjaunināt entītijas datus programmā Excel 

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā atvērt entītijas datus programmā Microsoft Excel un pēc tam skatīt, atjaunināt un rediģēt tos, izmantojot Microsoft Dynamics Office pievienojumprogrammu programmai Excel. Lai atvērtu entītijas datus, varat sākt no programmas Excel vai Finance and Operations.

Atverot elementa datus programmā Excel, varat ātri un vienkārši apskatīt un rediģēt šos datus, izmantojot Excel pievienojumprogrammu. Šai pievienojumprogrammai ir nepieciešama programma Microsoft Excel 2016.

> [!NOTE]
> Ja jūsu Microsoft Azure Active Directory (Azure AD) nomnieks ir konfigurēts Active Directory federācijas pakalpojumu (AD FS) lietošanai, pārliecinieties, ka ir instalēts 2016. gada maija Office atjauninājums, lai Excel pievienojumprogramma varētu nodrošināt pareizu jūsu pierakstīšanu.

Lai iegūtu plašāku informāciju par Excel pievienojumprogrammas lietošanu, noskatieties īso video [Excel veidnes izveidošana galveņu un rindu modeļiem](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-a-finance-and-operations-app"></a>Atveriet entītijas datus programmā Excel, sākot no programmas Finance and Operations
1. Finance and Operations lapā atlasiet **Atvērt programmā Microsoft Office**.

    Ja saknes datu avots (tabula) šai lapai ir tāda pati kā saknes datu avots jebkuriem elementiem, šai lapai tiek ģenerētas noklusējuma opcijas **Atvērt programmā Excel**. Opcijas **Atvērt programmā Excel** ir atrodamas bieži izmantotajās lapās, piemēram, **Visi kreditori** un **Visi debitori**.
 
2. Atlasiet opciju **Atvērt programmā Excel** un atveriet ģenerēto darbgrāmatu. Šajā darbgrāmatā ir saistību informācija par attiecīgo elementu, rādītājs uz jūsu vidi un rādītājs uz Excel pievienojumprogrammu.
3. Programmā Excel atlasiet **Iespējot rediģēšanu**, lai iespējotu Excel pievienojumprogrammas palaišanu. Excel pievienojumprogramma darbojas rūtī, kas atrodas Excel loga labajā pusē.
4. Ja pirmo reizi palaižat Excel pievienojumprogrammu, atlasiet **Uzticēties šai pievienojumprogrammai**.
5. Ja tiek prasīts pierakstīties, atlasiet **Pierakstīties** un pēc tam pierakstieties, izmantojot tos pašus akreditācijas datus, ko izmantojāt, lai pierakstītos programmā Finance and Operations. Excel pievienojumprogramma lieto iepriekšējās pierakstīšanās kontekstu no un jūs pieraksta automātiski, ja iespējams. (Informāciju par pārlūkprogrammu, kas tiek izmantota balstoties uz operētājsistēmas, skatiet [Pārlūkprogrammas, ko izmanto Office pievienojumprogrammas](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins.) Lai pārliecinātos, ka pierakstīšanās ir veiksmīga, pārbaudiet lietotāja vārdu Excel pievienojumprogrammas augšējā labajā stūrī. 

Excel pievienojumprogramma automātiski nolasa datus par jūsu atlasīto elementu. Ņemiet vērā, ka darbgrāmatā nav nekādu datu, līdz Excel pievienojums tos ielasa.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Atvērt elementa datus programmā Excel, kas sākat no Excel
1. Programmas Excel cilnes **Ievietošana** grupā **Pievienojumprogrammas** atlasiet **Veikals**, lai atvērtu pakalpojumu Office veikals.
2. Pakalpojumā Office veikals meklējiet pēc atslēgvārda **Dynamics** un pēc tam atlasiet vienumu **Pievienot**, kas atrodas blakus vienumam **Microsoft Dynamics Office pievienojumprogramma** (Excel pievienojumprogramma).
3. Ja pirmo reizi palaižat Excel pievienojumprogrammu, atlasiet **Uzticēties šai pievienojumprogrammai**, lai iespējotu Excel pievienojumprogrammas palaišanu. Excel pievienojumprogramma darbojas rūtī, kas atrodas Excel loga labajā pusē.
4. Atlasiet **Pievienot servera informāciju**, lai atvērtu rūti **Opcijas**.
5. Pārlūkprogrammā nokopējiet programmas Finance and Operations mērķa instances URL, ielīmējiet to laukā **Servera URL** un pēc tam izdzēsiet visus simbolus, kas seko resursdatora nosaukumam. Iegūtajam URL ir jāsatur tikai resursdatora nosaukums.

    Piemēram, ja URL ir `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, dzēsiet visu, izņemot `https://xxx.dynamics.com`.

6. Atlasiet **Labi** un pēc tam atlasiet **Jā**, lai apstiprinātu izmaiņas. Excel pievienojumprogramma tiek restartēta, un tajā tiek ielādēti metadati.

    Tagad ir pieejama poga **Dizains**. Ja Excel pievienojumprogrammai ir poga **Ielādēt sīkprogrammas**, visticamāk, jūs neesat pierakstījies kā pareizais lietotājs. Papildinformāciju skatiet šīs tēmas sadaļas [Problēmu novēršana](../office-integration/use-excel-add-in.md#troubleshooting) apakšsadaļā “Tiek rādīta poga Ielādēt sīkprogrammas”.

7. Atlasiet **Noformējums**. Excel pievienojumprogramma izgūst elementa metadatus.
8. Atlasiet **Pievienot tabulu**. Tiek parādīts elementu saraksts. Elementi ir uzskaitīti formātā “Nosaukums - Etiķete”.
9. Sarakstā atlasiet kādu elementu, piemēram, **Debitors — debitori**, un pēc tam atlasiet **Tālāk**.
10. Lai kādu lauku no saraksta **Pieejamie lauki** pievienotu sarakstam **Atlasītie lauki**, atlasiet attiecīgo lauku un pēc tam atlasiet **Pievienot**. Vai arī veiciet dubultklikšķi uz lauka sarakstā **Pieejamie lauki**.
11. Kad esat pabeidzis pievienot laukus sarakstam **Atlasītie lauki**, pārliecinieties, ka kursors atrodas pareizajā darblapas vietā (piemēram, A1 šūnā), un pēc tam atlasiet **Gatavs**. Pēc tam atlasiet **Gatavs**, lai aizvērtu noformētāju.
12. Atlasiet **Atsvaidzināt**, lai ievilktu datu kopu.

## <a name="view-and-update-entity-data-in-excel"></a>Skatīt un atjaunināt elementa datus programmā Excel
Kad Excel pievienojumprogramma ir ielasījusi elementa datus darbgrāmatā, varat jebkurā brīdī atjaunināt šos datus, Excel pievienojumprogrammā atlasot **Atsvaidzināt**.

## <a name="edit-entity-data-in-excel"></a>Rediģēt elementa datus programmā Excel
Varat pēc nepieciešamības mainīt entītijas datus un pēc tam tos publicēt atpakaļ Finance and Operations programmās, atlasot Excel pievienojumprogrammā **Publicēt**. Lai rediģētu kādu ierakstu, darblapā atlasiet kādu šūnu un pēc tam mainiet šīs šūnas vērtību. Lai pievienotu jaunu ierakstu, izpildiet tālāk aprakstītās darbības.

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
Kad lietotāji publicē izmaiņas datu ierakstos, izmantojot Excel pievienojumprogrammu, atjauninājumi tiek iesniegti paketēs. Noklusējuma publicēšanas partijas lielums ir 100 rindas. Versijā 10.0.17 un jaunākā versijā **Atļaut publicējamā partijas lieluma konfigurēšanu Excel pievienojumprogrammas līdzeklī** sniedz elastīgu kontroli publicēšanas partijas lielumam.

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

- **Tiek rādīta poga Ielādēt sīkprogrammas** — ja pēc pierakstīšanās Excel pievienojumprogrammai tiek rādīta poga **Ielādēt sīkprogrammas**, visticamāk, esat pierakstījies, izmantojot nepareizu lietotāja kontu. Lai atrisinātu šo problēmu, pārbaudiet, vai Excel pievienojumprogrammas labajā augšējā stūrī tiek rādīts pareizais lietotājvārds. Ja tiek rādīts nepareizs lietotājvārds, atlasiet to, izrakstieties un pēc tam atkal pierakstieties.
- **Saņemat ziņojumu “Aizliegts”**  — ja laikā, kad Excel pievienojumprogrammā notiek metadatu ielāde, saņemat ziņojumu “Aizliegts”, tad kontam, kas ir izmantots, lai pierakstītos Excel pievienojumprogrammā, nav atļaujas lietot attiecīgo pakalpojumu, instanci vai datu bāzi. Lai atrisinātu šo problēmu, pārbaudiet, vai Excel pievienojumprogrammas labajā augšējā stūrī tiek rādīts pareizais lietotājvārds. Ja tiek rādīts nepareizs lietotājvārds, atlasiet to, izrakstieties un pēc tam atkal pierakstieties.
- **Virs programmas Excel tiek rādīta tukša tīmekļa lapa** — ja pierakstīšanās procesa laikā tiek atvērta tukša tīmekļa lapa, tad kontam ir nepieciešams AD FS, bet Excel versija, kurā darbojas Excel pievienojumprogramma, ir pārāk veca, lai ielādētu pierakstīšanās dialoglodziņu. Lai atrisinātu šo problēmu, atjauniniet izmantoto Excel versiju. Lai atjauninātu Excel versiju, kad esat uzņēmumā, kurš atrodas atliktajā kanālā, izmantojiet [Office izvietošanas rīku](/deployoffice/overview-office-deployment-tool), lai [no atliktā kanāla pārietu uz pašreizējo kanālu](/deployoffice/overview-update-channels).
- **Datu izmaiņās publicēšanas laikā tiek saņemts taimauts** - ja saņemat taimauta ziņojumus, mēģinot publicēt datu izmaiņas entītijā, apsveriet iespēju samazināt ietekmētās darbgrāmatas publicēšanas paketes lielumu. Entītijas, kas ieraksta izraisīs lielāku loģikas apjomu, iespējams, būs jāsūta atjauninājumi mazākās paketēs, lai palīdzētu novērst taimautus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
