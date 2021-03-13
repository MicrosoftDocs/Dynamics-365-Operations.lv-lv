---
title: Krājumu vērtības glabāšanas pārskats
description: Šajā tēmā skaidrots, kā palaist Krājumu vērtības uzglabāšanas pārskatu un padarīt rezultātu pieejamu digitāli vai nu kā interaktīvu lapu programmā Microsoft Dynamics 365 Supply Chain Management, vai kā eksportētu dokumentu jebkurā no vairākiem formātiem.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0f54c02fc828d60f4ddb28be932bbf8eb137ee92
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008178"
---
# <a name="inventory-value-storage-report"></a>Krājumu vērtības glabāšanas pārskats

Šajā tēmā skaidrots, kā palaist **Krājumu vērtības uzglabāšanas** pārskatu un padarīt rezultātu pieejamu digitāli vai nu kā interaktīvu lapu programmā Microsoft Dynamics 365 Supply Chain Management, vai kā eksportētu dokumentu jebkurā no vairākiem formātiem.

Skatot pārskatu pārlūkā, kolonnas un uzkrātās bilances tiek dinamiski pielāgotas atkarībā no jūsu konfigurētā izkārtojuma. Varat sakārtot rezultātus, filtrēt tos, detalizēt datus un veikts citas darbības.

Pārskata rezultāti tiek uzglabāti **Krājumu vērtības** datu elementā. Tāpēc varat filtrēt un eksportēt rezultātus formātā, piemēram, ar komatu atdalītas vērtības (CSV) vai Microsoft Excel formātā.

**Krājumu vērtības uzglabāšanas** pārskats noder, ja rezultātos ir daudz rindu. Piemēram, jums ir 50 000 krājumi, un 300 veikali ir izveidoti kā noliktavas. Šādā gadījumā, ja pieprasāt krājumu beigu bilances pēc krājuma, vietas un noliktavas, rezultāti saturēs daudz rindu.

> [!NOTE]
> Pārskatā netiek iekļautas starpsummas, kas definētas pārskata izkārtojumā. Tas arī neietver virsgrāmatas bilances, pat ja tās ir definētas pārskata izkārtojumā. Saskaņošana ar virsgrāmatu ir jāveic, izmantojot apgrozījuma bilances.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Ieslēgt Krājumu vērtības uzglabāšanas līdzekli

Lai varētu ģenerēt **Krājumu vērtības uzglabāšanas** pārskatu, ir jāieslēdz līdzeklis sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis** - Izmaksu pārvaldība
- **Līdzekļa nosaukums** – Krājumu vērtības uzglabāšana

## <a name="generate-an-inventory-value-storage-report"></a>Ģenerēt Krājumu vērtības uzglabāšanas pārskatu

Veiciet šīs darbības, lai ģenerētu un uzglabātu **Krājumu vērtību uzglabāšanas** pārskatu.

1. Dodieties uz **Izmaksu pārvaldība \> Vaicājumi un pārskati \> Krājuma vērtības pārskata uzglabāšana**.
1. Atlasiet **Jauns**.
1. Parādītajā dialoglodziņā **Krājuma vērtība** iestatiet tālāk norādītās vērtības, lai definētu, kuri ieraksti ir ietverti pārskatā:

    - Kopsavilkuma cilnē **Parametri** ievadiet unikālu pārskata nosaukumu un lietojiet laukus **Datumu intervālu** sadaļā, lai definētu, kuri ieraksti tiek iekļauti pārskatā. Lai definētu datumu intervālu, varat vai nu atlasīt iepriekšnoteiktu diapazonu (saistībā ar pārskata izveides datumu) **Datumu intervāla koda** laukā, vai atlasīt konkrētus datumus laukos **No datuma** un **Līdz datumam**.
    - Kopsavilkuma cilnē **Iekļaujamie ieraksti** iestatiet filtrus un ierobežojumus, lai noteiktu, kuri dati ir iekļauti pārskatā.
    - Kopsavilkuma cilnē **Palaist fonā** norādiet, kā, kad un cik bieži pārskats tiek ģenerēts.

    > [!NOTE]
    > Šis pārskats vienmēr tiek palaists kā daļa no pakešuzdevuma.

1. Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu dialoglodziņu.

Kad pakešuzdevums ir pabeigts, pārskats tiks uzrādīts lapā **Krājumu vērtības pārskata uzglabāšana**. Iespējams, būs nepieciešams atsvaidzināt lapu, lai redzētu pārskatu.

## <a name="explore-an-inventory-value-storage-report"></a>Izpētiet Krājumu vērtības uzglabāšanas pārskatu

Pēc pārskata izveidošanas to var apskatīt un izpētīt jebkurā laikā, veicot šādas darbības.

1. Dodieties uz **Izmaksu pārvaldība \> Vaicājumi un pārskati \> Krājuma vērtības pārskata uzglabāšana**.
1. Sarakstā atlasiet pārskatu.
1. Atlasiet **Skatīt detalizēti**, lai parādītu pārskata saturu.
1. Izpētiet pārskatu, izpildot kādu no šīm darbībām:

    - Kā vairumam standarta lapu pakalpojumā Supply Chain Management, jūs varat atlasīt gandrīz jebkuru kolonnas virsrakstu, lai kārtotu vai filtrētu režģi pēc vērtībām šajā kolonnā.
    - Lietojiet **Filtrēt** lauku, lai filtrētu pārskatu pēc jebkuras vērtības jebkurā no pieejamajām kolonnām.
    - Izmantojiet skata izvēlni (virs **Filtrēt** lauka), lai saglabātu un ielādētu jūsu iecienītās izlases un filtrēšanas opciju kombinācijas.

## <a name="export-an-inventory-value-storage-report"></a>Eksportēt Krājumu vērtības uzglabāšanas pārskatu

Katrs pārskats, ko izveidojat, tiek saglabāts datu elementā **Krājumu vērtība**. Varat izmantot Supply Chain Management standarta datu pārvaldības līdzekļus, lai eksportētu datus no šīs entītijas uz jebkuru atbalstīto datu formātu, piemēram CSV vai Excel formātus.

Šajā piemērā ir parādīts, kā eksportēt **Krājumu vērtības pārskata** pārskatu.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Datu pārvaldība**.
1. Sadaļā **Importēt/eksportēt** atlasiet **Eksportēt** cilni. 
1. Lapā **Eksportēt** jūs iestatīsiet eksporta darbu. Vispirms ievadiet grupas nosaukumu darbam.
1. Sadaļā **Atlasītie elementi** atlasiet **Pievienot elementu**.
1. Parādītajā dialoglodziņā iestatiet sekojošus laukus:

    - **Elementa nosaukums** — atlasiet **Krājumu vērtību**.
    - **Mērķa datu formāts** — atlasiet formātu, uz kuru eksportēt datus.

1. Atlasiet **Pievienot**, lai pievienotu jaunu rindu, un pēc tam atlasiet **Aizvērt**, lai dialoglodziņu aizvērtu.
1. Parasti katru reizi jūs eksportēsiet vienu pārskatu. Lai eksportētu atsevišķu pārskatu, iestatiet filtru rindai, ko tikko pievienojāt **Pieprasījuma** dialoglodziņā. Šādā veidā varat definēt, kurš pārskats no **Krājumu vērtības** elementa tiek iekļauts jūsu eksportā. Sekojiet šīm darbībām, lai iestatītu šādas filtra opcijas, lai eksportētu vienu pārskatu:

    1. Cilnē **Diapazons** atlasiet **Pievienot**, lai pievienotu rindu.
    2. Iestatiet lauku **Tabula** uz **Krājumu vērtība**.
    3. Iestatiet lauku **Atvasinātā tabula** uz **Krājumu vērtība**.
    4. Iestatiet lauku **Lauks** uz lauku, pēc kura vēlaties filtrēt. Parasti tiek izmantots **Izpildes nosaukuma** lauks un/vai lauks **Izpildes laiks**.
    5. Laukā **Kritēriji** iestatiet vērtību, kuru vēlaties meklēt atlasītajā laukā. (Ja iepriekšējā solī atlasījāt lauku **Izpildes nosaukums**, šī vērtība būs pārskata nosaukums. Ja atlasījāt lauku **Izpildes laiks**, tas būs laiks, kad pārskats tika ģenerēts.)
    6. Pievienojiet cilnei **Diapazons** nepieciešamās papildu rindas, līdz esat unikāli identificējis pārskatu, kuru meklējat.

1. Atlasiet **Labi**, lai iestatījumus saglabātu un aizvērtu dialoglodziņu.
1. Atlasiet **Saglabāt**, lai saglabātu eksporta iestatījumus.
1. Cilnē **Eksporta opcijas** atlasiet **Eksportēt tūlīt**, lai ģenerētu eksporta failu.
1. Tiek atvērta lapa **Izpildes kopsavilkums**, kurā ir redzams eksportētā darba statuss un eksportēto elementu saraksts. Sadaļā **Elementa apstrādes statuss** atlasiet **Krājuma vērtības** elementu sarakstā un pēc tam atlasiet **Lejupielādēt failu**, lai no šī elementa lejupielādētu eksportētos datus.

Papildinformāciju par to, kā izmantot datu pārvaldību, lai eksportētu datus, skatiet šeit: [Datu importēšanas un eksportēšanas darbu apskats](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
