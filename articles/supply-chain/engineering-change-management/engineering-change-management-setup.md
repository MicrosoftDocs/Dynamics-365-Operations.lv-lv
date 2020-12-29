---
title: Izveidot kopīgas vērtības tehnisko izmaiņu pārvaldībai
description: Šajā tēmā ir aprakstīts, kā izveidot kopīgas vērtības, kas tiek izmantotas parametriem dažādās tehnisko izmaiņu pārvaldības daļās.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 86de050ef4110e3485a77099440f3402e46cc498
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2020
ms.locfileid: "4433232"
---
# <a name="establish-common-values-for-engineering-change-management"></a>Izveidot kopīgas vērtības tehnisko izmaiņu pārvaldībai

[!include [banner](../includes/banner.md)]

Iestatot tehnisko izmaiņu pārvaldību, ir jāizveido vairākas vērtību kolekcijas, kas tiks izmantotas, lai aizpildītu nolaižamos sarakstus citās lietotāja interfeisa (UI) daļās. Šīs vērtības ir jānorāda atbilstoši ražoto produktu veidiem un konkrētajām biznesa vajadzībām.

## <a name="engineering-change-categories"></a>Tehnisko izmaiņu kategorijas

Izmantojiet tehnisko izmaiņu kategorijas, lai organizētu tehnisko izmaiņu pasūtījumus, lai tos būtu vieglāk pārvaldīt un pārskatīt. Piemēram, var būt noderīgi iestatīt darbplūsmu, kurā atkarībā no kategorijas konkrētai nodaļai ir jāpārskata piedāvātās izmaiņas. Tāpēc tehnisko izmaiņu pasūtījumā ir ietverts lauks **Kategorija**.

Lai izveidotu to tehnisko izmaiņu kategoriju apkopojumu, kas tiek izmantotas jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu kategorijas**. Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.

## <a name="engineering-change-priorities"></a>Tehnisko izmaiņu prioritātes

Varat izmantot tehnisko izmaiņu prioritātes, lai norādītu tehnisko izmaiņu secības svarīgumu vai steidzamību. Tās palīdz izsekot tehnisko izmaiņu pasūtījuma nozīmīgumu, lai varētu viegli identificēt, kuri pasūtījumi vispirms jāapstrādā, un cik ātri.

Lai izveidotu to tehnisko izmaiņu prioritāšu apkopojumu, kas tiek izmantotas jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu prioritātes**. Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.

## <a name="engineering-change-reasons"></a>Tehnisku izmaiņu iemesli

Tehnisko izmaiņu iemesli norāda mainītā pasūtījuma izmaiņu iemeslu vai būtību.

Lai izveidotu to tehnisko izmaiņu iemeslu apkopojumu, kas tiek izmantoti jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu iemesli**. Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.

## <a name="material-disposal-codes"></a>Materiālu izvietojumu kodi

Materiālu likvidēšanas kodi tiek izmantoti, lai kategorizētu materiālus, kas tiek izmantoti pabeigtiem produktiem, vai komponentiem, kas ir jālikvidē noteiktā veidā vai, kas prasa zināmu apstrādi, pirms tos var pievienot jūsu parastajai miskastei. Kad pievienojat attiecīgo produktu tehnisko izmaiņu pasūtījumam, varat piešķirt likvidēšanas kodu kā daļu no izmaiņu detalizētās informācijas.

Lai izveidotu to materiālu likvidēšanas kodu apkopojumu, kas tiek izmantoti jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Materiālu likvidēšanas kodi**. Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.

## <a name="received-customer-approval"></a>Saņemts klienta apstiprinājums

Projektējot produktus konkrētam klientam, dizains un specifikācijas bieži ir jāapstiprina, pirms produktu var iestatīt kā gatavu. Lauks **Saņemtais klienta apstiprinājums** ļauj norādīt, cik tālu klientu apstiprināšanas procesā produkts ir un/vai apstiprinājums ir saņemts.

Lai izveidotu to saņemto klientu apstiprinājumu vērtību apkopojumu, kas tiek izmantoti jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Saņemtais klientu apstiprinājums**. Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.

## <a name="engineering-change--environmental-health-and-safety-codes"></a>Tehniskā izmaiņa — vides veselības un drošības kodi

Ja, ražojot produktus, ir jāņem vērā kādi standarta vides veselības un drošības noteikumi, vai uzņēmumam raksturīgi noteikumi vai procedūras, varat izmantot vides veselības un drošības kodus, lai tos definētu. Tehnsko izmaiņu pasūtījumā varat norādīt, kurus kodus piemērot produkta ražošanai, rediģējot ietekmētā produkta informāciju.

Lai izveidotu to veselības un drošības vērtību apkopojumu, kas tiek izmantotas jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Vides veselības un drošības kodi**. Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.

## <a name="engineering-change-severities"></a>Tehnisko izmaiņu nozīmīgums

Tiek izmantotas tehnisko izmaiņu pakāpes, lai norādītu ietekmes līmeni, kas attiecas uz produktiem tehnisko izmaiņu pasūtījumā.

Lai izveidotu to tehnisko izmaiņu stingrības apkopojumu, kas tiek izmantotas jūsu uzņēmumā, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu stingrība**. Pēc tam var izmantot darbību rūts pogas, lai pievienotu, noņemtu un rediģētu vērtības un sakārtotu tās secībā, kādā tās ir redzamas nolaižamajos sarakstos, kur tās tiek rādītas.

Varat izveidot noteikumus, kas attiecas uz katru izveidoto stingrības līmeni. Plašāku informāciju par šo noteikumu piešķiršanu skatiet nākamajā sadaļā.

## <a name="engineering-change-severity-rule-sets"></a>Tehnisko izmaiņu nozīmīguma kārtulu kopas

Lai izveidotu noteikumu grupu, ko varat izmantot, lai automātiski aprēķinātu izmaiņu pasūtījuma smagumu, pamatojoties uz ietekmēto produktu izmaiņu veidu, izmantojiet tehnisko izmaiņu stingrības noteikumu kopas. Lai izmantotu stingrības nosacījumus, atveriet lapu **Tehnisko izmaiņu pārvaldības parametri** un iestatiet lauku **Stingrības noteikums** uz *Aprēķināt* vai *Automātiski aprēķināt*.

Kad sistēma novērtē stingrību, tā apstrādā kārtulas tādā secībā, kādā tās parādās lapā, no sākuma līdz beigām. Lai kārtula tiktu atlasīta un tās prioritāte tiktu noteikta, ir jāizpilda visas noteikumu kopas kārtulas.

Lai iestatītu noteikumus, kas attiecas uz katru norādītās izmaiņas stingrības līmeni, dodieties uz **Tehnisko izmaiņu pārvaldība \> Iestatīšana \> Tehnisko izmaiņu pārvaldība \> Tehnisko izmaiņu stingrības noteikumu kopas**. Pēc tam izpildiet kādu no norādītajām darbībām.

- Lai izveidotu noteikumu kopu, darbības rūtī atlasiet **Jauns** un pēc tam iestatiet laukus, kā aprakstīts tālāk šajā sadaļā.
- Lai rediģētu esošu noteikumu kopu, atlasiet to saraksta rūtī, atlasiet **Rediģēt** darbību rūtī un pēc tam iestatiet laukus, kā aprakstīts tālāk šajā sadaļā.
- Lai dzēstu esošu noteikumu kopu, atlasiet to saraksta rūtī un pēc tam darbības rūtī atlasiet vienumu **Dzēst**.
- Lai pārkārtotu noteikumu kopu sarakstu, atlasiet noteikumu kopu saraksta rūtī un pēc tam izmantojiet pogas **Uz augšu** un **Uz leju** darbības rūtī, lai mainītu tās novietojumu.

Katrai noteikumu kopai iestatiet tālāk norādīto lauku.

- **Stingrība** – Atlasiet stingrības līmeni, lai izveidotu noteikumus. Lai izveidotu un nosauktu līmeņus, izmantojiet lapu **Tehnisko izmaiņu stingrība**. (Papildinformāciju skatiet iepriekšējā sadaļā.)

Izmantojiet pogas kopsavilkuma cilnē **Kārtulas**, lai pievienotu vai noņemtu kārtulu pašreizējam stingrības iestatījumam. Katrai kārtulai ir lauks **Kārtula** un lauks **Nosaukums**. Šos noteikumus nosaka sistēma, un tajos ir norādīti produkta iespējamo izmaiņu veidi. Nosaukums norāda izmaiņu veidu.
