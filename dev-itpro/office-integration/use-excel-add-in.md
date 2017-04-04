---
title: Izmantot Excel pievienojumprogrammu
description: "Šajā tēmā ir paskaidrots, kā programmā Microsoft Excel atverat datu subjekts un tad skatīt, atjaunināt un rediģēt datus, izmantojot pievienojumprogrammu Microsoft Dynamics Office Excel. Lai atvērtu datu subjekts, var sākt no programmas Excel vai Microsoft Dynamics 365 operācijām."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Izmantot Excel pievienojumprogrammu

Šajā tēmā ir paskaidrots, kā programmā Microsoft Excel atverat datu subjekts un tad skatīt, atjaunināt un rediģēt datus, izmantojot pievienojumprogrammu Microsoft Dynamics Office Excel. Lai atvērtu datu subjekts, var sākt no programmas Excel vai Microsoft Dynamics 365 operācijām.

Atverot vienību datus programmā Microsoft Excel, var ātri un viegli apskatīt un rediģēt datus, izmantojot pievienojumprogrammu Microsoft Dynamics Office Excel. Šī pievienojumprogramma ir nepieciešama Microsoft Excel 2016. **Piezīme:** ja Microsoft Azure Active Directory (AD debeszils) īrnieks ir konfigurēta, lai izmantotu Active Directory Federācijas pakalpojumi (AD FS), pārliecinieties, vai ir piemērots atjauninājumu maijā 2016, tā, lai Excel pievienojumprogrammu var pareizi pierakstīt jūs.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Atvērt vienību datus programmā Excel, startējot no Dynamics 365 operācijām
1.  Lapā Microsoft Dynamics 365 operāciju, noklikšķiniet uz **atvērt programmā Microsoft Office**. Ja saknes datu avots (tabula) lapa ir tāds pats kā saknes datu avots visiem subjektiem, noklusējuma **atvērta programmā Excel** opcijas tiek veidotas lapas. **Atvērta programmā Excel** opcijas var atrast biežāk lietotajām lapās, piemēram, **visiem kreditoriem** un **visus klientus**.
2.  Noklikšķiniet uz **atvērt programmā Excel** opcijas un atveriet darbgrāmatu, kas tiek ģenerēts. Šajā darbgrāmatā ir saistošu informāciju par entītiju, rādītājs uz savu vidi un rādītāju uz Excel pievienojumprogrammu.
3.  Programmā Excel noklikšķiniet **rediģēšanas iespējošana** lai iespējotu Excel pievienojumprogrammu palaišanai. Excel pievienojumprogramma darbojas rūtī Excel loga labajā pusē.
4.  Ja palaižat Excel pievienojumprogrammas pirmo reizi, noklikšķiniet uz **uzticēties šai pievienojumprogrammai**.
5.  Ja tiek parādīta uzvedne pieteikties, noklikšķiniet uz **pieteikties**, un pēc tam piesakieties, izmantojot tos pašus akreditācijas datus, kuru izmantojāt lai pieteiktos Dynamics 365 operācijām. Excel pievienojumprogrammu izmantotu iepriekšējās pierakstīšanās kontekstā no Internet Explorer un automātiski pierakstīt jūs, ja tas ir iespējams. Tādēļ pārbaudiet, vai lietotājvārds augšējā labajā stūrī Excel pievienojumprogrammu.

Excel pievienojumprogrammu automātiski nolasa datus par entītiju, ko esat atlasījis. Ņemiet vērā, ka nebūs nekādi dati darbgrāmatā līdz Excel pievienojumprogrammu lasa to.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Atvērt vienību datus programmā Excel, startējot Excel
1.  Programmā Excel, par **ievietot** cilni, jo **Add-ins** grupu, noklikšķiniet uz **Store** Office veikala atvēršanai.
2.  Office krātuvē, meklēt pēc atslēgvārda "Dinamika" un uz **pievienot** blakus **Microsoft Dynamics Office pievienojumprogramma** (Excel pievienojumprogrammu).
3.  Ja palaižat Excel pievienojumprogrammas pirmo reizi, noklikšķiniet uz **uzticēties šai pievienojumprogrammai** lai iespējotu Excel pievienojumprogrammu palaišanai. Excel pievienojumprogramma darbojas rūtī Excel loga labajā pusē.
4.  Noklikšķiniet uz **pievienot servera informāciju** atvērt **opcijas** rūti.
5.  Kopētu pārlūka URL no jūsu mērķa Dynamics 365 darbības gadījumam, ielīmējiet to **servera URL** lauks un pēc tam izdzēsiet visu pēc resursdatora nosaukumu (piemēram, izdzēsiet **/? cmp = usmf & mi = CustTableListPage**). Rezultātā URL jābūt tikai resursdatora nosaukumu (piemēram, **https://xxx.dynamics.com**).
6.  Noklikšķiniet uz **OK**, un pēc tam noklikšķiniet uz **Jā** lai apstiprinātu izmaiņas. Excel pievienot restartējas un ielādē metadatus. **Design** poga tagad ir pieejams. Ja Excel pievienojumprogramma ir **slodze sīklietotnes** pogu, jums droši vien nav pieteicies kā pareizs lietotāja. Plašāku informāciju skatiet "pogu Load sīklietotnes ir pierādījusi" šīs tēmas sadaļā "Problēmu novēršana".
7.  Noklikšķiniet uz **Design**. Excel pievienojumprogrammu iegūst metadatu entītijas.
8.  Noklikšķiniet uz **pievienot tabulu**. Tiek parādīts saraksts ar organizācijām. Juridiskās personas ir uzskaitītas "Vārds - Label" formātā.
9.  Atlasīt entītiju sarakstā, piemēram, **Debitori - klienti**, un pēc tam noklikšķiniet uz **nākamo**.
10. Pievienot lauku no **pieejamie lauki** saraksta **atlasītos laukus** sarakstu, noklikšķiniet laukā un pēc tam uz **pievienot**. Vai arī veiciet dubultklikšķi uz lauka.
11. Pēc tam, kad esat pievienojis vēlamais jomām **atlasītos laukus** sarakstu, pārliecinieties, ka kursors ir novietots pareizajā vietā (piemēram, šūna A1) darblapā un pēc tam noklikšķiniet uz **darīts**. Noklikšķiniet uz **darīts** lai izietu dizainers.
12. Noklikšķiniet uz **atsvaidzināt** ieraut datu kopa.

## <a name="view-and-update-entity-data-in-excel"></a>Skatīt un atjaunināt Excel datu subjekts
Pēc Excel pievienojumprogrammu nolasa vienību datus darbgrāmatā, datus var atjaunināt jebkurā brīdī, noklikšķinot uz **atsvaidzināt** programmā Excel pievienojumprogrammu.

## <a name="edit-entity-data-in-excel"></a>Rediģēt entītijas datus programmā Excel
Var mainīt datu subjekts pieprasa un pēc tam to publicējat, noklikšķinot uz **publicēt** programmā Excel pievienojumprogrammu. Lai rediģētu ierakstu, izvēlieties šūnu darblapā un pēc tam mainiet šūnas vērtību. Pievienot jaunu ierakstu, veiciet vienu no šīm darbībām:

-   Noklikšķiniet jebkurā vietā uz darblapas un pēc tam noklikšķiniet uz **New** programmā Excel pievienojumprogrammu.
-   Noklikšķiniet uz pēdējās darblapas rindas un pēc tam nospiediet taustiņu Tab, līdz kursors pārvietojas no rindā ieraksta tā uzskaites dokumenta pēdējā slejā, un tiek izveidota jauna rinda.
-   Noklikšķiniet uz rindas tūlīt zem tās darblapas un sāciet ievadīt datus šūnā. Pārvietojot fokusu no šīs šūnas, darblapā tiek izvērsts, lai iekļautu jaunās rindas.

Dzēst ierakstu, veiciet vienu no šīm darbībām:

-   Noklikšķiniet ar peles labo pogu uz rindas numurs pie darblapas rindu dzēst, un pēc tam noklikšķiniet uz **dzēst**.
-   Ar peles labo pogu noklikšķiniet darblapas rindā dzēst un pēc tam noklikšķiniet uz **dzēst**&gt;**tabulas rindas**.

## <a name="add-or-remove-columns"></a>Pievienot vai noņemt kolonnas
Varat izmantot izstrādes rīku, lai pielāgotu kolonnas, kas tiek automātiski pievienoti darblapai.

1.  Noklikšķinot uz sākt datu avota projektētāju Excel pievienojumprogrammu **opcijas** pogu (rīku simbols) un pēc tam atlasot **Iespējot noformējuma** izvēles rūtiņu.
2.  Noklikšķiniet uz **Design** programmā Excel pievienojumprogrammu. Ir uzskaitīti visi datu avoti.
3.  Blakus datu avotu, noklikšķiniet uz **rediģēt** pogu (zīmuļa simbols).
4.  Pielāgotu sarakstu **atlasītos laukus** uzskaitīt, cik jums nepieciešams:
    -   Pievienot lauku no **pieejamie lauki** saraksta **atlasītos laukus** sarakstu, noklikšķiniet laukā un pēc tam uz **pievienot**. Vai arī veiciet dubultklikšķi uz lauka.
    -   Lai noņemtu lauku no **atlasītos laukus** sarakstu, noklikšķiniet laukā un pēc tam uz **noņemt**. Vai arī veiciet dubultklikšķi uz lauka.
    -   Mainīt lauku secību, noklikšķiniet uz lauka **atlasītos laukus** sarakstu un pēc tam noklikšķiniet uz **līdz** vai **pa**.

5.  Savas izmaiņas lietot datu avotu, noklikšķinot uz **Update**. Noklikšķiniet uz **darīts** lai izietu dizainers. Ja pievienojat lauku (kolonnu), noklikšķiniet uz **atsvaidzināt** ieraut atjauninātu datu kopu.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Ir daži jautājumi, kas var atrisināt, izmantojot dažus soļus.

-   **Ir parādīta pogu Load sīklietotnes.** Ja Excel pievienojumprogramma ir **slodze sīklietotnes** pogu pēc pierakstīšanās, jums droši vien nav pieteicies kā pareizs lietotāja. Lai atrisinātu šo problēmu, pārbaudiet, vai pareizs lietotāja vārds parādās augšējā labajā stūrī Excel pievienojumprogrammu. Ja nepareizs lietotājvārds tiek parādīts, noklikšķiniet uz tā Izrakstīties, un pēc tam jāpierakstās atkal.
-   **Saņemat ziņojumu "Aizliegts".** Ja saņemat ziņojumu "Aizliegts", kamēr Excel pievienojumprogrammas ielāde metadatus, kontu, kas ir pieteicies uz Excel pievienojumprogrammu nav atļaujas izmantot mērķtiecīgi pakalpojumu, gadījuma vai datu bāzes. Lai atrisinātu šo problēmu, pārbaudiet, vai pareizs lietotāja vārds parādās augšējā labajā stūrī Excel pievienojumprogrammu. Ja nepareizs lietotājvārds tiek parādīts, noklikšķiniet uz tā Izrakstīties, un pēc tam jāpierakstās atkal.
-   **Tukšu lapu tiek rādīta programmas Excel.** Ja pieteikšanās procesa laikā atver tukšu lapu, kontam nepieciešams AD FS, bet darbojas pievienojumprogramma Excel versijā nav nesen, lai ielādētu pierakstīšanās dialoglodziņu. Lai atrisinātu šo problēmu, atjauninātu versiju, kuru lietojat Excel. Atjaunināt Excel versijā, kad tu esi tāds uzņēmums, kas ir atliktais kanālā, izmantojiet [Office ieviešanas rīks](https://technet.microsoft.com/library/jj219422.aspx) uz [pāriet no atliktā kanālu uz pašreizējo staciju](https://technet.microsoft.com/library/mt455210.aspx).



