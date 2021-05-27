---
title: Apstrādāt, pārskatīt un grāmatot atlaides
description: Šajā tēmā ir aprakstīts, kā apstrādāt atlaižu pārvaldības piedāvājumus, aprēķināt to atlaides, pārskatīt ģenerētās darbības, grāmatot darbības un pārskatīt grāmatojumus.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 5188fa271cd9eb24140a9edcf507a3da72b61074
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020535"
---
# <a name="process-review-and-post-rebates"></a>Apstrādāt, pārskatīt un grāmatot atlaides

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā apstrādāt atlaižu pārvaldības piedāvājumus, aprēķināt to atlaides, pārskatīt ģenerētās darbības, grāmatot darbības un pārskatīt grāmatojumus.

## <a name="change-the-status-of-a-deal"></a>Piedāvājuma statusa maiņa

Katram piedāvājumam var piešķirt statusu, lai palīdzētu to izsekot. Statuss ir paredzēts tikai informatīviem nolūkiem.

1. Atlasiet piedāvājumu (piemēram, lapā [**Visi atlaižu pārvaldības piedāvājumi**](rebate-management-deals.md)).
1. Darbību rūtī cilnē **Atlaižu pārvaldības piedāvājumi** grupā **Uzturēt** atlasiet **Statusa maiņa**.
1. Dialoglodziņā **Statusa maiņa** iestatiet lauku **Atlaides statuss** uz jaunu statusu.
1. Atlasiet **Labi**.

## <a name="calculate-fifo-purchase-prices"></a>Aprēķināt FIFO pirkšanas cenas

Jāpalaiž periodiskais uzdevums **Aprēķināt FIFO pirkšanas cenu**, lai aprēķinātu atlaides [piedāvājumiem](rebate-management-deals.md), kuru **Cenas bāze** ir iestatīta uz *FIFO*. Sistēma izmantos First in, first out (FIFO) kārtulu, lai aprēķinātu pārdoto akciju vērtību. Pēc tam šī vērtība tiks izmantota, lai aprēķinātu kreditoru atlaides.

Dodieties uz **Atlaižu pārvaldība \> Periodiskie uzdevumi \> Aprēķināt FIFO pirkšanas cenu**. Parādītajā dialoglodziņā atlasiet **Labi**, lai palaistu aprēķinu.

## <a name="process-rebate-management-deals"></a>Procesu atlaižu pārvaldības piedāvājumi

Apstrādājot piedāvājumu, sistēma aprēķina visas iestatītās atbilstošās atlaides un autoratlīdzības. Tiks apstrādāti tikai atlasītie piedāvājumi, kuriem ir aprēķina periodi, kas ir gatavi aprēķināšanai un kuru statuss ir *Aktīvs*. Kad apstrāde ir pabeigta, sistēma ģenerē darbību kopu, kuru var pārskatīt un pēc tam grāmatot.

> [!NOTE]
> Visos gadījumos atlaides tiek apstrādātas līmenī, ko nosaka katra darījuma **Saskaņot**, iestatot (*Darījums* vai *Rinda*). Vienas rindas aprēķinus var veikt tikai tiem darījumiem, kuriem lauks **Saskaņot** ir iestatīts uz *Rinda*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Apstrādāt visas rindas vienam vai vairākiem piedāvājumiem

1. Atveriet atbilstošo [atlaižu piedāvājumu saraksta lapu](rebate-management-deals.md) tam piedāvājuma veidam, ar kuru vēlaties strādāt.
1. Atlasiet rindu katram piedāvājumam, kuru vēlaties apstrādāt (vai atveriet piedāvājumu, kuru vēlaties apstrādāt).
1. Darbību rūts cilnes **Atlaižu pārvaldības piedāvājumi** grupā **Ģenerēt** atlasiet vienu no šīm komandām:

    - **Apstrāde \> Nodrošinājums** – nosako uzkrājumu komplektu katram attiecīgajam atlaižu piedāvājumam, bet negrāmato tos.
    - **Apstrāde \> Atlaižu pārvaldība** – apstrādājiet darījumu sēriju, kas nodrošina atlaides vērtību katram darījumam.
    - **Apstrāde \> Norakstīšana** – atceliet iepriekš grāmatotās darbības, lai tās norakstītu un varētu aprēķināt jaunas atlaižu piedāvājumu darbības.

1. Parādītajā dialoglodziņā iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu aprēķina datumu diapazonu.
1. Atlasiet **Labi**, lai palaistu aprēķinu.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Apstrādāt vienu vai vairākas konkrētas piedāvājuma rindas atlasītajam piedāvājumam

1. Atveriet atbilstošo [atlaižu piedāvājumu saraksta lapu](rebate-management-deals.md) tam piedāvājuma veidam, ar kuru vēlaties strādāt.
1. Atveriet piedāvājumu, no kura vēlaties apstrādāt rindu.
1. Augšējā labajā stūrī atlasiet cilni **Rindas**.
1. Kopsavilkuma cilnē **Atlaižu pārvaldība** atlasiet rindu katrai piedāvājuma rindai, kuru vēlaties apstrādāt.
1. Kopsavilkuma cilnes **Atlaižu pārvaldība** rīkjoslā atlasiet vienu no šīm komandām. (Šīs komandas ir pieejamas tikai darījumiem, kuros lauks **Saskaņot** ir iestatīts uz *Rinda*.)

    - **Apstrāde \> Nodrošinājums** – nosako uzkrājumu komplektu katrai attiecīgā piedāvājuma rindai, bet negrāmato tos.
    - **Apstrāde \> Atlaižu pārvaldība** – apstrādājiet darījumu sēriju, kas nodrošina atlaides vērtību katrai piedāvājuma rindai.
    - **Apstrāde \> Norakstīšana** – atceliet iepriekš grāmatotās darbības, lai tās norakstītu un varētu aprēķināt jaunas atlaižu piedāvājumu darbības.

1. Parādītajā dialoglodziņā iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu aprēķina datumu diapazonu.
1. Atlasiet **Labi**, lai palaistu aprēķinu.

### <a name="process-deals-using-a-batch-job"></a>Apstrādāt piedāvājumus, izmantojot pakešuzdevumu

Tā vietā, lai apstrādātu noteiktus piedāvājumus vai darījumu rindas, varat palaist pakešuzdevumu, lai vienlaikus apstrādātu vairākus piedāvājumus. Pēc izvēles var lietot ierakstu filtrus un/vai uzstādīt periodisku grafiku. Lai apstrādātu piedāvājumus, izmantojot pakešuzdevumu, rīkojieties šādi.

1. Izpildiet kādu no šīm darbībām:

    - Dodieties **uz Atlaižu pārvaldība \> Periodiskie uzdevumi \> Apstrāde \> Nodrošinājums**, lai nodrošinātu uzkrājumu komplektu katram attiecīgajam darījumam, tos neizgrāmatojot.
    - Dodieties uz **Atlaižu pārvaldība \> Periodiskie uzdevumi \> Apstrāde \> Atlaižu pārvaldība**, lai apstrādātu darījumu sēriju, kas nodrošina atlaides vērtību katrai piedāvājuma rindai.
    - Dodieties uz **Atlaižu pārvaldība \> Periodiskie uzdevumi \> Apstrāde \> Norakstīšana**, lai atsauktu iepriekš grāmatotās darbības, norakstot tās, lai varētu aprēķināt jauno atlaižu piedāvājumu darījumus.

1. Parādītā dialoglodziņa kopsavilkuma cilnes **Parametri** sadaļā **Periods** iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu aprēķina datumu diapazonu darbībām.
1. Sadaļā **Garantētais periods** iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu garantiju aprēķina datumu diapazonu.
1. Kopsavilkuma cilnē **Iekļaujamie ieraksti** var uzstādīt filtrus, lai ierobežotu piedāvājumu kopu, ko pakešuzdevums apstrādās. Šie iestatījumi darbojas tāpat kā citi pakešuzdevumu tipi.
1. Ja nepieciešams, jūs varat ātrajā cilnē **Palaist fonā** uzstādīt automātisku atjauninājumu kā pakešuzdevumu. Šie iestatījumi darbojas tāpat kā citi pakešuzdevumu tipi.
1. Atlasiet **Labi**, lai palaistu un/vai plānotu aprēķinu.

## <a name="view-and-edit-rebate-management-transactions"></a>Skatīt un rediģēt Atlaižu pārvaldības darbības

Apstrādājot vienu vai vairākus piedāvājumus, sistēma izveido darbības, kuras var skatīt un, iespējams, rediģēt pirms to grāmatošanas.

1. Izpildiet kādu no šīm darbībām:

    - Atlasiet darījumu, par kuru skatīt darbības (piemēram, lapā [**Visi atlaižu pārvaldības piedāvājumi**](rebate-management-deals.md)). Darbību rūts cilnes **Atlaižu pārvaldības piedāvājumi** grupā **Darbības** atlasiet **Darbības** vai **Garantijas darbības** atkarībā no darbības tipa, kuru vēlaties skatīt.
    - Atlasiet darījumu, par kuru skatīt darbības (piemēram, lapā [**Visi atlaižu pārvaldības piedāvājumi**](rebate-management-deals.md)), lai skatītu detalizētu informāciju. Kopsavilkuma cilnē **Atlaižu pārvaldība** atlasiet darījuma rindu, lai skatītu darbības. Pēc tam rīkjoslā atlasiet **Darbības** vai **Garantijas darbības** atkarībā no darbības tipa, kuru vēlaties skatīt. (Šīs pogas ir pieejamas tikai piedāvājumiem, kuros lauks **Saskaņot** ir iestatīts uz *Rinda*.)

1. Tiek parādīta lapa **Atlaižu pārvaldības datuma darījumi** vai **Atlaižu pārvaldības garantiju darījumi**. Tajā ir režģis, kurā katra rinda attēlo darījumu kolekciju no viena atlaižu vai garantijas perioda. Atlasiet režģa rindu un pēc tam darbību rūtī atlasiet **Avota darbības**, lai skatītu šai rindai piederošās transakcijas.
1. Parādītajā lapā tiek rādīts atlasītajai rindai piederošā atlasītā tipa darbību saraksts. Katrs darījums sniedz būtisku informāciju atkarībā no darbības tipa. Garantiju darbībām sarakstu var tikai skatīt. Cita veida transakcijām šajā lapā varat veikt šādas darbības:

    - Lai pārbaudītu visu pieprasīto darbību kopējo vērtību lapā, skatiet lauku **Pieprasītā summa**.
    - Lai skatītu papildinformāciju par jebkuru darbību, atlasiet to un pēc tam atlasiet cilni **Vispārīgi**, **Finanšu dimensija** vai **Dimensija**.
    - Lai skatītu visus piemērotos samazinājumus, darbību rūtī atlasiet **Samazināšanas darbības**. Plašāku informāciju skatiet [Atlaižu samazināšanas principi](rebate-reduction-principle.md).
    - Lai atzīmētu darbības kā pieprasītas vai nepieprasītas, ja izmantojat prasību procesu, atlasiet atbilstošās rindas un pēc tam darbību rūtī atlasiet vienu no šīm komandām. (Jūs iespējojat prasību procesus [**Atlaižu pārvaldības parametru** lapā](rebate-management-parameters.md).)

        - **Iestatīt pieprasītos \> Visi** – atzīmējiet visas darbības kā pieprasītas.
        - **Iestatīt pieprasīto \> Atlasītie** – atzīmējiet atlasītās darbības kā pieprasītas.
        - **Iestatīt nepieprasītos \> Visi** – atzīmējiet visas darbības kā nepieprasītas.
        - **Iestatīt nepieprasīto \> Atlasītie** – atzīmējiet atlasītās darbības kā nepieprasītas.

    - Lai grāmatotu prasību vienai vai vairākām rindām, atlasiet atbilstošās rindas un pēc tam darbību rūtī atlasiet **Grāmatot**. (Poga **Grāmatot** ir pieejama tikai atlaižu darbībām. Tas nav pieejams uzkrājumu un norakstīšanas darījumiem.) Dialoglodziņā **Grāmatot** lauki **No datuma** un **Līdz datumam** ir iestatīti automātiski. Iestatiet lauku **Grāmatošanas datums**, tad atlasiet **Labi**.
    - Lai koriģētu summu, kas tiek rādīta jebkurai atvērtai vai negrāmatotai darbībai, atlasiet darbību un pēc tam izpildiet kādu no šīm darbībām:

        - Labojiet vērtību laukā **Labotā summa**.
        - Darbību rūtī atlasiet **Korekcijas iestatīšana**. Pēc tam parādītajā nolaižamajā dialoglodziņā laukā **Labotā summa** ievadiet vērtību.

> [!NOTE]
> Apstrādājot nākamo periodu, darbību sarakstā tiks iekļautas visas iepriekšējās grāmatošanas nepieprasītās darbības, kā arī visas jaunās darbības atlasītajam periodam.

## <a name="post-rebates-transactions"></a>Grāmatojiet atlaižu darbības

Lai grāmatotu atlaižu un ieturējumu vērtību, ir jāpalaiž grāmatošanas process, ja vien nav iestatīta sistēma to automātiskai grāmatošanai.

### <a name="set-up-the-system-to-post-all-transactions-automatically"></a>Iestatīt sistēmu automātiskai visu darbību grāmatošanai

Lai iestatītu sistēmu visu transakciju grāmatošanai, tiklīdz tās tiek ģenerētas, ieslēdziet opciju **Automātiski grāmatot žurnālus** un/vai **Automātiski grāmatot brīva teksta rēķinus** lapā **Atlaižu pārvaldības parametri**. Plašāku informāciju skatiet [Atlaižu pārvaldības parametri](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Grāmatot darbības vienam vai vairākiem piedāvājumiem

Ja neizmantojat automātisko grāmatošanu, pēc attiecīgo darījumu apstrādes izpildiet šīs darbības, lai pārskatītu un grāmatotu ģenerētās darbības visām rindām vienam vai vairākiem darījumiem.

1. Atveriet atbilstošo [atlaižu piedāvājumu saraksta lapu](rebate-management-deals.md) tam piedāvājuma veidam, ar kuru vēlaties strādāt.
1. Atlasiet rindu katram darījumam, kuru vēlaties grāmatot (vai atveriet darījumu, kuru vēlaties grāmatot).
1. Darbību rūts cilnes **Atlaižu pārvaldības piedāvājumi** grupā **Ģenerēt** atlasiet vienu no šīm komandām:

    - **Grāmatot \> Nodrošinājums** – grāmatojiet pieejamās uzkrāšanas darbības, kuras esat izveidojis.
    - **Grāmatot \> Atlaižu pārvaldība** – grāmatojiet pieejamās atlaižu darbības, kuras esat izveidojis.
    - **Grāmatot \> Norakstīšana** – grāmatojiet pieejamās norakstīšanas darbības, kuras esat izveidojis.

1. Parādītajā dialoglodziņā iestatiet lauku **Grāmatošanas datums**. Parādītajā dialoglodziņā iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu grāmatojamo darījumu diapazonu.
1. Atlasiet **Labi**, lai grāmatotu darījumus.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Grāmatot darījumus vienu vai vairākas konkrētas piedāvājuma rindas atlasītajam piedāvājumam

Ja neizmantojat automātisko grāmatošanu, pēc attiecīgo darījumu apstrādes izpildiet šīs darbības, lai pārskatītu un grāmatotu ģenerētās darbības visām rindām vienam vai vairākiem darījumiem.

1. Atveriet atbilstošo [atlaižu piedāvājumu saraksta lapu](rebate-management-deals.md) tam piedāvājuma veidam, ar kuru vēlaties strādāt.
1. Atveriet darījumu, kuram ir rinda, kurai vēlaties grāmatot darbības.
1. Augšējā labajā stūrī atlasiet cilni **Rindas**.
1. Kopsavilkuma cilnē **Atlaižu pārvaldība** atlasiet rindu katrai piedāvājuma rindai, kuru vēlaties grāmatot.
1. Kopsavilkuma cilnes **Atlaižu pārvaldība** rīkjoslā atlasiet vienu no šīm komandām. (Šīs komandas ir pieejamas tikai darījumiem, kuros lauks **Saskaņot** ir iestatīts uz *Rinda*.)

    - **Grāmatot \> Nodrošinājums** – grāmatojiet pieejamās uzkrāšanas darbības, kuras esat izveidojis.
    - **Grāmatot \> Atlaižu pārvaldība** – grāmatojiet pieejamās atlaižu darbības, kuras esat izveidojis.
    - **Grāmatot \> Norakstīšana** – grāmatojiet pieejamās norakstīšanas darbības, kuras esat izveidojis.

1. Parādītajā dialoglodziņā iestatiet lauku **Grāmatošanas datums**. Parādītajā dialoglodziņā iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu grāmatojamo darījumu diapazonu.
1. Atlasiet **Labi**, lai grāmatotu darījumus.

### <a name="post-transactions-using-a-batch-job"></a>Darbību grāmatošana, izmantojot pakešuzdevumu

Tā vietā, lai grāmatotu noteiktus darījumus vai darījumu rindas, varat palaist pakešuzdevumu, lai vienlaikus grāmatotu vairākus piedāvājumus. Pēc izvēles var lietot ierakstu filtrus un/vai uzstādīt periodisku grafiku. Lai grāmatotu darījumus, izmantojot pakešuzdevumu, rīkojieties šādi.

1. Izpildiet kādu no šīm darbībām:

    - Dodieties **uz Atlaižu pārvaldība \> Periodiskie uzdevumi \> Grāmatot \> Nodrošinājums**, lai grāmatotu pieejamos izveidotos uzkrāšanas darījumus.
    - Dodieties uz **Atlaižu pārvaldība \> Periodiskie uzdevumi \> Grāmatot \> Atlaižu pārvaldība**, lai grāmatotu pieejamos izveidotos atlaižu darījumus.
    - Dodieties uz **Atlaižu pārvaldība \> Periodiskie uzdevumi \> Grāmatot \> Norakstīšana**, lai grāmatotu pieejamos izveidotos norakstīšanas darījumus.

1. Parādītā dialoglodziņa kopsavilkuma cilnes **Parametri** sadaļā **Periods** iestatiet lauku **Grāmatošanas datums**. Parādītajā dialoglodziņā iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu grāmatojamo darījumu diapazonu. 
1. Sadaļā **Garantētais periods** iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu garantiju aprēķina datumu diapazonu.
1. Kopsavilkuma cilnē **Iekļaujamie ieraksti** var uzstādīt filtrus, lai ierobežotu piedāvājumu kopu, ko pakešuzdevums apstrādās. Šie iestatījumi darbojas tāpat kā citi pakešuzdevumu tipi.
1. Ja nepieciešams, jūs varat ātrajā cilnē **Palaist fonā** uzstādīt automātisku atjauninājumu kā pakešuzdevumu. Šie iestatījumi darbojas tāpat kā citi pakešuzdevumu tipi.
1. Atlasiet **Labi**, lai palaistu un/vai plānotu aprēķinu.

## <a name="review-rebate-management-journals"></a>Atlaižu pārvaldības žurnālu pārskatīšana

Pēc transakciju iegrāmatošanas varat pārskatīt iegūtos žurnālus, dokumentus vai preces. Atlaižu un autoratlīdzību mērķa darbību pamatā ir maksājuma tips, kas iestatīts grāmatošanas metodē, un atlaides izvades tips. Piemēram, ja atlaides izdošana ir iestatīta uz *Krājums*, tiks izveidots pārdošanas pasūtījums, un to var skatīt, izmantojot mērķa darbības. Ja maksājums ir iestatīts kreditoru atlaižu izmantošanai, debitora atlaidēm tiek izveidots kreditora rēķins kreditoram, kas iestatīts debitoram.

Lai pārskatītu žurnāla ierakstus, kas ir saistīti ar atlaižu pārvaldības darījumu, rīkojieties šādi.

1. Atveriet atbilstošo [atlaižu piedāvājumu saraksta lapu](rebate-management-deals.md) tam piedāvājuma veidam, ar kuru vēlaties strādāt.
1. Atlasiet darījumu, kura grāmatošanai jāpārbauda žurnāla ieraksti.
1. Darbību rūts cilnes **Atlaižu pārvaldības piedāvājumi** grupā **Darbības** atlasiet **Darbības** vai **Atlaižu darbības** atkarībā no darbības tipa, kuru vēlaties skatīt.
1. Pārliecinieties, vai lauks **Rādīt** ir iestatīts uz *Visi* vai *Grāmatots*.
1. Atrodiet un atlasiet darbību kolekciju, kuru vēlaties pārbaudīt, un pēc tam darbību rūtī atlasiet vienu no šīm pogām. (Šīs pogas ir pieejamas tikai tad, ja atlasītajai darbību kolekcijai ir atbilstoši grāmatojumi.)

    - **Mērķa darbības** – pārskatiet atbilstošos žurnālus un cita veida dokumentus, ko ģenerējis atlasītais darījums.
    - **Krājumi** — pārskatiet atbilstošos krājumus, ko ģenerējis atlasītais darījums.

1. Tiek parādīts atbilstošo žurnālu, dokumentu vai preču saraksts. Lai skatītu papildinformāciju par jebkuru žurnālu, dokumentu vai vienumu, atlasiet tā rindu un pēc tam darbību rūtī atlasiet **Skatīt detalizētu informāciju**.
