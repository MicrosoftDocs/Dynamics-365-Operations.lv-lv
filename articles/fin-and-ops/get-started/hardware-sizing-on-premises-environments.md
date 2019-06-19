---
title: Aparatūras lieluma maiņas prasības lokālām vidēm
description: Šajā tēmā uzskaitītas aparatūras lieluma maiņas prasības lokālai videi.
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 4832a056a99e0f7521e022982b7db7b16d7064a3
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595497"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a>Aparatūras lieluma maiņas prasības lokālām vidēm

[!include [banner](../includes/banner.md)]

Pirms sākat aparatūras un infrastruktūras lieluma maiņas procesu lokālai videi, iepazīstieties ar informāciju sadaļās [Sistēmas prasības](system-requirements.md) un [Iestatīšanas un izvietošanas norādījumi](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md), lai iegūtu padziļinātu izpratni par pamatā esošo infrastruktūru.

> [!NOTE]
> Īpašu uzmanību pievērsiet labākajām praksēm sistēmas iestatīšanai, kas nodrošina optimālu darbību.

Pēc dokumentācijas pārskatīšanas varat sākt novērtēt savu transakciju un vienlaicīgo lietotāju apjomu un mainīt vides lielumu atbilstoši vidējai kodola caurlaidei.

## <a name="factors-that-affect-sizing"></a>Faktori, kas ietekmē lieluma maiņu

Lieluma maiņu ietekmē visi tālāk esošajā attēlā parādītie faktori. Jo detalizētāka ir apkopotā informācija, jo precīzāk varat noteikt lieluma maiņu. Bez atbalstošiem datiem aparatūras lieluma maiņa, visticamāk, būs neprecīza. Nepieciešamo datu absolūtais minimums ir maksimālā transakciju rindu noslodze stundā.

[![Aparatūras lieluma maiņa lokālām vidēm](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Skatoties attēlā no kreisās uz labo pusi, pirmais un svarīgākais faktors, kas jāņem vērā precīzai lieluma maiņas novērtēšanai, ir transakciju profils jeb transakciju raksturojums. Ir svarīgi vienmēr noteikt maksimālo transakciju apjomu stundā. Ja ir vairāki maksimālās noslodzes periodi, šie periodi ir precīzi jādefinē.

Tāpat kā apzināties noslodzi, kas ietekmē jūsu infrastruktūru, jums arī padziļinātāk jāizprot tālāk norādītie faktori.

- **Transakcijas** — parasti transakcijām ir noteiktas noslodzes virsotnes dienā/nedēļā. Tas galvenokārt ir atkarīgs no transakcijas tipa. Laika un izdevumu ieraksti parasti sekmē maksimālo noslodzi vienreiz nedēļā, savukārt pārdošanas pasūtījumu ieraksti bieži sistēmā nonāk lielā apjomā, izmantojot integrāciju, vai tiek ievadīti pakāpeniski dienas laikā.
- **Vienlaicīgo lietotāju skaits** — vienlaicīgo lietotāju skaits ir otrs svarīgākais lieluma maiņas faktors. Uzticamu lieluma maiņas novērtējumu nevar iegūt, pamatojoties uz vienlaicīgo lietotāju skaitu, tādēļ, ja šie ir vienīgie jums pieejami dati, aprēķiniet aptuveno skaitu un, kad jūsu rīcībā ir vairāk datu, atkārtoti pārskatiet šo informāciju. Precīza vienlaicīgo lietotāju definīcija ietver tālāk norādīto.

    - Nosauktie lietotāji nav vienlaicīgi lietotāji.
    - Vienlaicīgie lietotāji vienmēr ir nosaukto lietotāju apakškopa. 
    - Maksimālā darba slodze nosaka maksimālo vienlaicīgumu lieluma maiņai.

    Vienlaicīgo lietotāju kritērijs ir lietotāju atbilstība visiem tālāk norādītajiem kritērijiem.

    - Lietotājs ir pieteicies.
    - Darbs ar transakcijām/pieprasījumiem uzskaites laikā.
    - Sesija nav dīkstāves sesija.

- **Datu salikums** — tas galvenokārt attiecas uz to, kā sistēma tiks iestatīta un konfigurēta. Piemēram, cik jums būs juridisko personu, krājumu, MK līmeņu un cik sarežģīti būs drošības iestatījumi. Katram no šiem faktoriem var būt neliela ietekme uz veiktspēju, tāpēc šos faktorus var neitralizēt, veicot gudras izvēles attiecībā uz infrastruktūru.
- **Paplašinājumi** — pielāgojumi var būt vienkārši vai sarežģīti. Pielāgojumu skaitam un sarežģītības un lietojuma raksturam ir dažāda ietekme uz nepieciešamo infrastruktūras lielumu. Sarežģītiem pielāgojumiem ir ieteicams veikt veiktspējas novērtējumus, lai nodrošinātu ne tikai to efektivitātes pārbaudi, bet arī izpratni par infrastruktūras vajadzībām. Vēl būtiskāk tas ir gadījumos, kad paplašinājumi nav kodēti saskaņā ar labākajām praksēm veiktspējas un mērogojamības nodrošināšanai.
- **Pārskatu veidošana un analīze** — šie faktori parasti ietver smagu vaicājumu palaišanu dažādām datu bāzēm Finance and Operations datu bāzu sistēmās. Izprotot un samazinot dārgu pārskatu izpildes biežumu, varēsit labāk izprast to ietekmi.
- **Trešo pušu risinājumi** — šiem risinājumiem, piemēram, ISV, ir tāda pati ietekme un ieteikumi kā paplašinājumiem.

## <a name="sizing-your-finance-and-operations-environment"></a>Finance and Operations vides lieluma maiņa

Lai izprastu lieluma maiņas prasības, jums ir jāzina maksimālais apstrādājamo transakciju apjoms. Vairums papildu sistēmas, piemēram, pārvaldības pārskatu sastādītājs vai SSRS, ir mazāk būtiskas uzdevumam. Tā rezultātā šajā dokumentā uzmanība ir vērsta galvenokārt uz AOS un SQL Server.

> [!NOTE]
> Kopumā skaitļošanas pakāpes paplašinās un ir jāiestata N+1 veidā, proti, ja novērtējat trīs AOS, pievienojiet ceturto AOS. Datu bāzes pakāpe ir jāiestata, izmantojot AlwaysOn augstas pieejamības iestatījumu.

## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Lieluma maiņa

- 3–15 tūkst. transakciju rindu stundā katram kodolam DB serverī.
- Tipiska AOS-SQL kodolu attiecība 3:1 primārajam SQL Server. Atbilstoši izvēlētajai augstas pieejamības konfigurācijai ir nepieciešami papildu kodoli.

    - Apstrādes operācijām ar lielu datu bāzes noslodzi attiecība var regresēt uz 2:1.

- Variācijas ietekmē tālāk norādītie faktori.

    - Lietotie parametru iestatījumi.
    - Paplašinājumu līmeņi.
    - Papildu funkcionalitātes, piemēram, datu bāzes žurnāla un brīdinājumu, izmantošana. Īpaši izteikta datu bāzes reģistrācija vēl vairāk samazinās caurlaidi stundā katram kodolam zem 3 tūkst. rindām.
    - Datu salikuma sarežģītība — vienkāršs kontu plāns un detalizēts kontu plānu katrs atšķirīgi ietekmē caurlaidi (šis ir viens piemērs).
    - Transakciju raksturojums.
    - 2–16 GB atmiņas katram kodolam.
    - Papildu datu bāzes DB serverī, piemēram, pārvaldības pārskatu sastādītājs un SSRS datu bāzes.
    - Pagaidu DB = 15% no DB lieluma ar fiziskajiem procesoriem atbilstošu failu skaitu.
    - SAN lielums un caurlaide, pamatojoties uz kopējo vienlaicīgo transakciju apjomu/lietojumu.

### <a name="high-availability"></a>Augsta pieejamība

Ieteicams SQL Server vienmēr izmantot ar klastera vai spoguļošanas iestatījumiem. Otrajam SQL mezglam ir jābūt tādam pašam kodolu skaitam kā primārajam mezglam.

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory federācijas pakalpojums (AD FS)

Informāciju par AD FS lieluma maiņu skatiet rakstā [AD FS servera noslodzes dokumentācija](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

Instanču skaita plānošanai izvietojumā ir pieejama [lieluma maiņas izklājlapa](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx).

## <a name="aos-online-and-batch"></a>AOS (tiešsaistes un partijas)

### <a name="sizing"></a>Lieluma maiņa

- Lieluma maiņa pēc transakciju apjoma/lietojuma

    - 2–6 tūkst. rindu katram kodolam
    - 16 GB vienā instancē
    - Standarta komplektācija — 4–24 kodoli
    - 10–15 Enterprise lietotāji katram kodolam
    - 15–25 Activity lietotāji katram kodolam
    - 25–50 Team dalībnieki katram kodolam

- Pakete

    - 1–4 partijas pavedieni katram kodolam
    - Lielums atbilstoši pakešizpildes loga raksturlielumiem

- Ņemiet vērā, ka AOS, datu pārvaldībai un partijai platformā Service Fabric ir viena loma. Ir jāmaina lielums atbilstoši šīm trīs darba slodzēm kopā, nevis atsevišķi kā programmā Microsoft Dynamics AX 2012.
- Ir spēkā tie paši SQL Server mainīguma faktori.

### <a name="high-availability"></a>Augsta pieejamība

- Pārliecinieties, vai jums ir pieejams AOS skaits, kas par vismaz 1 vai 2 AOS pārsniedz aprēķinā paredzēto skaitu.
- Pārliecinieties, vai jums ir pieejami vismaz 3–4 virtuālie resursdatori.

## <a name="management-reporter"></a>Pārvaldības pārskatu sastādītājs

Vairumā gadījumu, ja vien lietojums nav intensīvs, divi mezgli atbilstoši ieteicamajām minimālajām prasībām darbojas labi. Tikai tad, ja paredzams intensīvs lietojums, nepieciešami vairāk nekā divi mezgli. Mērogojiet, kā nepieciešams.

## <a name="sql-server-reporting-services"></a>SQL Server pārskatu izveides pakalpojumi (SSRS)

Vispārējas pieejamības laidienam var izvietot tikai vienu SSRS mezglu. Testēšanas laikā pārraugiet SSRS mezglu un pēc nepieciešamības palieliniet pakalpojumiem SSRS pieejamo kodolu skaitu. Pārliecinieties, vai iepriekš konfigurētais sekundārais mezgls pieejams no SSRS virtuālās mašīnas atšķirīgā virtuālajā resursdatorā. Tas ir svarīgi gadījumos, ja virtuālajai mašīnai, kas vieso SSRS, vai virtuālajam resursdatoram rodas kāda problēma. Šajā gadījumā tie ir jāaizstāj.

## <a name="environment-orchestrator"></a>Vides vadības modulis

Vadības moduļa pakalpojums ir pakalpojums, kas pārvalda jūsu izvietojumu un saistīto saziņu ar LCS. Šis pakalpojums ir izvietots kā primārais Service Fabric pakalpojums, un tam ir nepieciešamas vismaz trīs virtuālās mašīnas. Šis pakalpojums ir izvietots kopā ar Service Fabric vadības moduļa pakalpojumiem. Tā lielums ir jāpielāgo atbilstoši klastera maksimālajai noslodzei. Papildinformāciju skatiet rakstā [Service Fabric klastera noslodzes plānošanas apsvērumi](/azure/service-fabric/service-fabric-cluster-capacity).

## <a name="virtualization-and-oversubscription"></a>Virtualizācija un pārabonēšana

Tādi uzdevumam būtiski pakalpojumi kā AOS ir jāvieso virtuālajās mašīnās ar specializētiem resursiem — kodoliem, atmiņu un disku.
