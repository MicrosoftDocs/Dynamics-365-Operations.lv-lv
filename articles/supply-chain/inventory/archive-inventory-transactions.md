---
title: Arhivēt krājumu transakcijas
description: Šajā tēmā ir aprakstīts, kā arhivēt krājumu darbību datus, lai palīdzētu uzlabot sistēmas veiktspēju.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b740da1a8a349f4a1a80b41bf717c388fd3db0c0
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881836"
---
# <a name="archive-inventory-transactions"></a>Arhivēt krājumu transakcijas

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Laika gaitā krājumu darbību tabula (`InventTrans`) turpinās pieaugt un patērēt vairāk vietas datu bāzē. Tāpēc vaicājumi, kas ir veikti attiecībā pret tabulu, pakāpeniski kļūs lēnāki. Šajā tēmā aprakstīts, kā var lietot krājumu *Darbību arhīva līdzekli*, lai arhivētu datus par krājumu darbībām, tādējādi uzlabojot sistēmas veiktspēju.

> [!NOTE]
> Atlasītajā slēgtajā Virsgrāmatas periodā var arhivēt tikai finansiāli atjauninātas krājumu darbības. Lai to arhivētu, finansiāli atjauninātajām izejošām krājumu darbībām jābūt ar izejas plūsmas statusu *Pārdots* un ienākošo krājumu darbībām jābūt ar statusu *Nopirkts*.

Arhivējot krājumu darbības, visas saistītās darbības tiek pārvietotas uz `InventTransArchive` tabulu. Krājumu izdošanas darbības un krājumu saņemšanas darbības tiek arhivēta atsevišķi, pamatojoties uz krājuma ID (`itemId`) un krājumu dimensijas ID (`inventDimId`) kombināciju, un tās tiek novietotas apkopotās izejas plūsmas un summētās saņemšanas darbībās.

Ja vienā `itemId` un `inventDimId` kombinācijā ir tikai viena saņemšanas vai izdošanas darbība, darbība netiks arhivēta.

## <a name="turn-on-the-feature-in-your-system"></a>Līdzekļa ieslēgšana sistēmā

Ja sistēmā vēl nav ietverti šajā tēmā aprakstītie līdzekļi, pārejiet uz sadaļu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet līdzekli *Krājumu darbību arhīvs*. Ņemiet vērā, ka šo līdzekli nevar atspējot, ja tas ir iespējots.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Lietas, kas jāņem vērā pirms krājumu darbību arhivēšanas

Pirms krājumu darbību arhivēšanas ir jāapsver šādi biznesa scenāriji, jo tos ietekmēs darbība:

- Kad jūs auditējat krājumu darbības no saistītiem dokumentiem, piemēram, pirkšanas pasūtījuma rindām, tās tiks parādītas kā arhivētas. Lai pārskatītu arhivētās darbības, dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Tīrīt \> Krājumu darbību arhīvs**.
- Arhivētajiem periodiem nevar atcelt krājumu slēgšanu. Pirms varat atcelt krājumu slēgšanu, ir jāatgriež krājumu darbību arhīvs derīgs periodam.
- Standarta izmaksu pārveidošanu nevar veikt arhivētiem periodiem. Pirms varat atcelt krājumu slēgšanu, ir jāatgriež krājumu darbību arhīvs derīgs periodam.
- Krājumu pārskati, kas ir nākuši no krājumu darbībām, tiks ietekmēti, kad arhivēsiet krājumu darbības. Šie pārskati ietver krājumu vecumstruktūras pārskatu un krājumu vērtību pārskatus.
- Krājumu prognozes var tikt ietekmētas, ja tās tiek palaistas arhivēto periodu laika periodā.

## <a name="prerequisites"></a>Priekšnosacījumi

Krājumu darbības var arhivēt tikai to periodu laikā, kuros ir ievēroti šādi nosacījumi:

- Virsgrāmatas periodam jābūt slēgtam.
- Krājumu slēgšana jāveic arhīva perioda datumā vai pēc tā.
- Periodam jābūt vismaz vienu gadu pirms arhīva perioda sākuma datuma.
- Nedrīkst būt eksistējošu krājumu pārrēķini.

## <a name="archive-inventory-transactions"></a>Arhivēt krājumu transakcijas

Lai arhivētu krājumu darbības, izpildiet tālāk aprakstītos norādījumus.

1. Dodieties uz **Krājumu pārvaldība** \> **Periodiskie uzdevumi** \> **Tīrīt** \> **Krājumu darbību arhīvs**.

    Parādās lapa **Krājumu darbību arhīvs**, kurā parādīts arhivēto procesu ierakstu saraksts.

    ![Krājumu transakcijas arhīva lapa](media/archive-inventory-empty.png "Krājumu darbību arhīva lapa")

1. Darbību rūtī atlasiet **Krājumu darbību arhīvs**, lai izveidotu krājumu darbību arhīvu.
1. Kopsavilkuma cilnes **Parametri** dialoglodziņā **Krājumu darbību arhīvs** iestatiet šādus laukus:

    - **No datuma slēgtajā Virsgrāmatas periodā** – atlasiet agrāko darbības datumu, ko iekļaut arhīvā.
    - **Līdz datuma slēgtajā Virsgrāmatas periodā** – atlasiet jaunākās darbības datumu, ko iekļaut arhīvā.

    ![Krājumu transakcijas arhīva dialoglodziņš](media/archive-inventory-dates.png "Krājumu darbību arhīva dialoglodziņš")

    > [!NOTE]
    > Atlasei būs pieejami tikai [priekšnosacījumiem](#prerequisites) atbilstošie periodi.

1. Kopsavilkuma cilnē **Izpildīt fonā** iestatiet pakešapstrādes detaļas pēc pieprasījuma. Veiciet pakešuzdevumu darbības programmā Microsoft Dynamics 365 Supply Chain Management, kā parasti.
1. Atlasiet **Labi**.
1. Jūs saņemat ziņojumu, kurā tiek parādīta uzvedne ar aicinājumu apstiprināt, ka vēlaties turpināt. Uzmanīgi izlasiet ziņojumu un pēc tam atlasiet **Jā**, ja vēlaties turpināt.

    Tiek saņemts ziņojums, ka krājumu darbību arhīva darbs ir pievienots pakešuzdevumu rindai. Uzdevums sāks arhivēt krājumu darbības no atlasītā perioda.

## <a name="view-archived-inventory-transactions"></a>Skatīt arhivētās krājumu transakcijas

Lapa **Krājumu darbību arhīvs** rāda visu arhivēšanas vēsturi. Katra režģa rinda rāda tādu informāciju kā arhīva izveidošanas datumu, lietotāju, kas to izveidoja, un tā statusu.

![Vēstures arhivēšana Krājumu darbību arhīva lapā](media/archive-inventory-full.png "Vēstures arhivēšana Krājumu darbību arhīva lapā")

Nolaižamajā sarakstā lapas augšpusē atlasiet vienu no šīm vērtībām, lai filtrētu režģī parādītos arhīvus:

- **Aktīvs** – rādīt tikai aktīvos arhīvus, neatgrieztos arhīvus.
- **Visi** – parāda visus arhīvus: gan aktīvos, gan apgrieztos.

Katram arhīvam režģī tiek sniegta šāda informācija:

- **Aktīvs** – atzīme norāda, ka arhīvs ir aktīvs.
- **No datuma** – senākās darbības datums, kuru var iekļaut arhīvā.
- **No datuma** – jaunākās darbības datums, kuru var iekļaut arhīvā.
- **Plānots pēc** – lietotāja konts, kas izveidoja arhīvu.
- **Izpildīts** – arhīva izveidošanas datums.
- **Reverss** – atzīme norāda, ka arhīvs ir anulēts.
- **Pārtraukt pašreizējo atjaunināšanu** – atzīme norāda, ka arhīvs notiek, bet tas ir apturēts.
- **Stāvoklis** – arhīva apstrādes statuss. Iespējamās vērtības ir *Gaida*, *Notiek* un *Pabeigts*.

Rīkjosla virs režģa nodrošina šādas pogas, kuras var izmantot darbam ar atlasīto arhīvu:

- **Arhivētās darbības** – apskatiet visas izvēlētā arhīva detaļas. **Arhivēto darbību** lapa, kurā parādītas visas arhīva darbības.

    ![Arhivēto darbību lapa](media/archive-inventory-transactions.png "Arhivēto darbību lapa")

    Lai skatītu papildinformāciju par noteiktu darbību lapā **Arhivētās darbības**, atlasiet to režģī un pēc tam darbību rūtī atlasiet **Arhivētās darbības detaļas**. Lapa **Arhivēto darbību detaļas**, kas parādās, parāda tādu informāciju kā grāmatošana Virsgrāmatā, saistītās apakšgrāmatas atsauces un finanšu dimensijas.

- **Apturēt arhivēšanu** - apturēt atlasīto arhīvu, kas pašlaik tiek apstrādāts. Pauze stājas spēkā tikai pēc tam, kad ir izveidots arhivēšanas uzdevums. Tāpēc var būt neliela aizkave, pirms pauze stājas spēkā. Ja arhīvs ir apturēts, laukā **Pārtraukt pašreizējo atjaunināšanu** tiek parādīta atzīme.
- **Atsākt arhivēšanu** - atsākt atlasītā arhīva apstrādi, kas pašlaik ir apturēts.
- **Atsaukt** – anulēt atlasīto arhīvu. Arhīvu var atsaukt tikai tad, ja tā lauks **Stāvoklis** ir iestatīts uz *Pabeigts*. Ja arhīvs ir apturēts, laukā **Pārtraukt pašreizējo atjaunināšanu** tiek parādīta atzīme.
