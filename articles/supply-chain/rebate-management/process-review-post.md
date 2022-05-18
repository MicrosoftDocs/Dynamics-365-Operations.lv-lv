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
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 524aec8025378391057275f77e31191f88e4a98b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690279"
---
# <a name="process-review-and-post-rebates"></a>Apstrādāt, pārskatīt un grāmatot atlaides

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā apstrādāt atlaižu pārvaldības piedāvājumus, aprēķināt to atlaides, pārskatīt ģenerētās darbības, grāmatot darbības un pārskatīt grāmatojumus.

## <a name="change-the-status-of-a-deal"></a>Piedāvājuma statusa maiņa

Katram piedāvājumam var piešķirt statusu, lai palīdzētu to izsekot. Statuss ir paredzēts tikai informatīviem nolūkiem.

1. Atlasiet piedāvājumu (piemēram, [**Visi atlaižu pārvaldības piedāvājumi** lapā](rebate-management-deals.md)).
1. Darbību rūtī cilnē **Atlaižu pārvaldības piedāvājumi** grupā **Uzturēt** atlasiet **Statusa maiņa**.
1. Dialoglodziņā **Statusa maiņa** iestatiet lauku **Atlaides statuss** uz jaunu statusu.
1. Atlasiet **Labi**.

## <a name="calculate-fifo-purchase-prices"></a>Aprēķināt FIFO pirkšanas cenas

Jāpalaiž periodiskais uzdevums **Aprēķināt FIFO pirkšanas cenu**, lai aprēķinātu atlaides [piedāvājumiem](rebate-management-deals.md), kuru **Cenas bāze** ir iestatīta uz *FIFO*. Sistēma izmantos First in, first out (FIFO) kārtulu, lai aprēķinātu pārdoto akciju vērtību. Pēc tam šī vērtība tiks izmantota, lai aprēķinātu kreditoru atlaides.

Dodieties uz **Atlaižu pārvaldība \> Periodiskie uzdevumi \> Aprēķināt FIFO pirkšanas cenu**. Parādītajā dialoglodziņā atlasiet **Labi**, lai palaistu aprēķinu.

## <a name="create-source-transactions"></a>Izveidot avota transakcijas

Jūs varat izveidot pārdošanas pasūtījumus vai pirkšanas pasūtījumus, kuriem ir avota transakcijas pirms vai pēc piemērojama atlaides pārvaldības darījuma izveides.

Jūs varat iestatīt katru darījuma rindu tā, lai tā automātiski izveidotu atlaides uzkrājumu, grāmatojot pārdošanas pasūtījuma vai pirkšanas pasūtījuma piegādi vai rēķinu. Iestatiet lauku **Transakcijas veids** darījuma rindai uz *Piegāde* vai *Rēķins* un iestatiet opciju **Apstrādāt grāmatošanas laikā** uz *Jā*. Ja lauka **Transakcijas veids** iestatījums ir *Pasūtījums*, grāmatošanas apstrāde ir deaktivizēta. Avota transakcijām, kas tika izveidotas pēc darījuma aktivizēšanas, jūs joprojām varat apstrādāt uzkrājumus, kā aprakstīts sadaļā [Procesa atlaides pārvaldības darījumi](#process-deals) vēlāk šajā tēmā.

### <a name="enable-price-details"></a>Iespējot detalizētu informāciju par cenu

Pirms varat izveidot avota darbības, debitoru parādos ir jāiespējo opcija **Iespējot detalizētu informāciju par cenu**.

1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
1. Cilnes **Cenas** kopsavilkuma cilnē **Detalizētu informāciju par cenu** iestatiet opcijas **Iespējot detalizētu informāciju par cenu** vērtību uz *Jā*.

### <a name="create-a-source-transaction"></a>Izveidot avota transakciju

Lai izveidotu avota transakciju, veiciet tālāk aprakstītās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**.

    Lai imitētu atlaides prasību ģenerēšanas veidu, tagad ir jāizveido pārdošanas pasūtījums, kur prece un daudzums dod debitoram tiesības uz atlaidi.

1. Laukā **Debitora konts** ievadiet vai atlasiet debitoru, kas būs kvalificēts atlaides darījumam.
1. Atlasiet **Labi**, lai izveidotu pārdošanas pasūtījumu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet rindu un iestatiet tai šādus laukus:

    - **Krājuma numurs** – norādiet krājumu, kas atbilst atlaidei.
    - **Daudzums** – norādiet daudzumu, kas atbilst atlaižu darījumam, kurš ietver rindu, kur lauks **Pamats** iestatīts uz *Daudzums*.
    - **Vienības cena** – norādiet cenu, kas atbilst atlaižu darījumam, kurš ietver rindu, kur lauks **Pamats** iestatīts uz *Vērtība*.
    - **Vieta** – atlasiet vietu, kurā ir pieejama prece, un kas atbilst atlaides darījumam.
    - **Noliktava** – atlasiet noliktavu, kurā ir pieejama prece, un kas atbilst atlaides darījumam.

1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** rīkjoslā atlasiet **Pārdošanas pasūtījuma rinda \> Preces informācija**. Šī komanda ir pieejama tikai tad, ja ir iespējota detalizēta informācija par cenu, kā aprakstīts iepriekšējā sadaļā.
1. Lapā **Detalizēta informācija par cenu** atlasiet kopsavilkuma cilni **Atlaižu pārvaldība**. Kopsavilkuma cilnē uzskaitīti atlaižu pārvaldības darījumi, kas attiecas uz pašreizējo pasūtījuma rindu un tiek parādīta novērtētā atlaides summa pasūtījuma valūtā. Ņemiet vērā, ka šīs summas ir tikai turpmāko atlaižu prasību novērtējumi. Faktiskās atlaižu summas var atšķirties. Šeit ir daži faktori, kas varētu ietekmēt faktiskās summas:

    - Kopējais pārdošanas apjoms, ko debitors ir sasniedzis saskaņā ar periodisko atlaides līgumu.
    - Vai debitors atgrieza visus daudzumus vai daļējus daudzumus.
    - Vai piemērojamais pārdošanas pasūtījums sasniedzis transakcijas veidu (*Pasūtījums, piegāde* vai *Rēķins*), kas definēts Atlaižu pārvaldības darījumam.
    - Darījuma vērtība **Izvade**. Darījumiem, kuru lauks **Izvade** ir iestatīts uz *Krājums*, tiks parādīta tukša atlaides summa.

1. Kopsavilkuma cilnē **Detalizēta informācija** ievērojiet, ka sadaļa **Maržas novērtējums** ietver tālāk norādītos laukus. Šie lauki ir pievienoti, izmantojot atlaižu pārvaldību. Visi no tiem parāda vienības vērtības (bet lauki kopsavilkuma cilnē **Atlaižu pārvaldība** rāda rindas kopējās vērtības).

    - **Atlaižu pārvaldības atlaides summa** (tikai pārdošanas pasūtījumi)
    - **Atlaižu pārvaldības honorāra summa** (tikai pārdošanas pasūtījumi)
    - **Atlaižu pārvaldības kreditora atlaides summa** (pārdošanas pasūtījumi un pirkšanas pasūtījumi)

1. Aizveriet lapu **Detalizēta informācija par cenu**.
1. Ja pārdošanas pasūtījumam nav jābūt kvalificētam atlaidēm, ko tikko skatījāt, veiciet šīs darbības, lai izslēgtu atlaides. (Tomēr parasti neizslēdzat atlaides.)

    1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet atbilstošo rindu.
    1. Kopsavilkuma cilnē **Rindas detaļas** cilnē **Cena un atlaide** iestatiet opciju **Izslēgt no atlaižu pārvaldības** uz *Jā*. Šī opcija nav piemērojama pirkšanas pasūtījumiem. Turklāt, ja šī opcija ir iestatīta uz *Jā*, tiek izslēgtas tikai debitora atlaides. Joprojām ir spēkā debitora honorāru atlaides un kreditora atlaides.

1. Darbību rūts cilnē **Izdot un iepakot** grupā **Ģenerēt** atlasiet **Grāmatot pavadzīmi**.
1. Kopsavilkuma cilnē **Parametri** laukā **Daudzums** atlasiet *Visi*.
1. Atlasiet **Labi**.
1. Atlasiet **Labi**, ja jums tiek piedāvāts apstiprināt darbību.
1. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
1. Kopsavilkuma cilnē **Parametri** laukā **Daudzums** atlasiet *Visi* vai *Pavadzīme*.
1. Atlasiet **Labi**.
1. Atlasiet **Labi**, ja jums tiek piedāvāts apstiprināt darbību.

## <a name="process-rebate-management-deals"></a><a name="process-deals"></a>Procesu atlaižu pārvaldības piedāvājumi

Apstrādājot piedāvājumu, sistēma aprēķina visas iestatītās atbilstošās atlaides un autoratlīdzības. Tiks apstrādāti tikai atlasītie piedāvājumi, kuriem ir aprēķina periodi, kas ir gatavi aprēķināšanai un kuru statuss ir *Aktīvs*. Kad apstrāde ir pabeigta, sistēma ģenerē darbību kopu, kuru var pārskatīt un pēc tam grāmatot.

> [!NOTE]
> Visos gadījumos atlaides tiek apstrādātas līmenī, ko nosaka katra darījuma **Saskaņot**, iestatot (*Darījums* vai *Rinda*). Vienas rindas aprēķinus var veikt tikai tiem darījumiem, kuriem lauks **Saskaņot** ir iestatīts uz *Rinda*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Apstrādāt visas rindas vienam vai vairākiem piedāvājumiem

1. Atveriet atbilstošo [atlaižu piedāvājumu saraksta lapu](rebate-management-deals.md) tam piedāvājuma veidam, ar kuru vēlaties strādāt.
1. Atlasiet rindu katram piedāvājumam, kuru vēlaties apstrādāt (vai atveriet piedāvājumu, kuru vēlaties apstrādāt).
1. Darbību rūts cilnes **Atlaižu pārvaldības piedāvājumi** grupā **Ģenerēt** atlasiet vienu no šīm komandām:

    - **Apstrāde \> Nodrošinājums** – nosako uzkrājumu komplektu katram attiecīgajam atlaižu piedāvājumam, bet negrāmato tos. Šis izvēlnes vienums nav pieejams darījumiem, kuru lauks **Atlaides izvade** ir iestatīts uz *Krājums*.
    - **Apstrāde \> Atlaižu pārvaldība** – apstrādājiet darījumu sēriju, kas nodrošina atlaides vērtību katram darījumam.
    - **Process \> Norakstīt** - katram atlaižu darījuma avota darījumam un noteiktam periodam apstrādā novirzes starp summām, kas tika grāmatotas uzkrājumiem un atlaižu pārvaldībai. Šis izvēlnes vienums nav pieejams darījumiem, kuru lauks **Atlaides izvade** ir iestatīts uz *Krājums*.

1. Parādītajā dialoglodziņā iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu aprēķina datumu diapazonu.
1. Atlasiet **Labi**, lai palaistu aprēķinu.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Apstrādāt vienu vai vairākas konkrētas piedāvājuma rindas atlasītajam piedāvājumam

1. Atveriet atbilstošo [atlaižu piedāvājumu saraksta lapu](rebate-management-deals.md) tam piedāvājuma veidam, ar kuru vēlaties strādāt.
1. Atveriet piedāvājumu, no kura vēlaties apstrādāt rindu.
1. Augšējā labajā stūrī atlasiet cilni **Rindas**.
1. Kopsavilkuma cilnē **Atlaižu pārvaldība** atlasiet rindu katrai piedāvājuma rindai, kuru vēlaties apstrādāt.
1. Kopsavilkuma cilnes **Atlaižu pārvaldība** rīkjoslā atlasiet vienu no šīm komandām. (Šīs komandas ir pieejamas tikai darījumiem, kuros lauks **Saskaņot** ir iestatīts uz *Rinda*.)

    - **Apstrāde \> Nodrošinājums** – nosako uzkrājumu komplektu katrai attiecīgā piedāvājuma rindai, bet negrāmato tos. Šis izvēlnes vienums nav pieejams darījumiem, kuru lauks **Atlaides izvade** ir iestatīts uz *Krājums*.
    - **Apstrāde \> Atlaižu pārvaldība** – apstrādājiet darījumu sēriju, kas nodrošina atlaides vērtību katrai piedāvājuma rindai.
    - **Process \> Norakstīt** - katram atlaižu darījuma avota darījumam un noteiktam periodam apstrādā novirzes starp summām, kas tika grāmatotas uzkrājumiem un atlaižu pārvaldībai. Šis izvēlnes vienums nav pieejams darījumiem, kuru lauks **Atlaides izvade** ir iestatīts uz *Krājums*. 

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

### <a name="process-deals-by-using-the-rebate-workbench"></a>Apstrādāt darījumus, izmantojot atlaižu rīku

Tā vietā, lai apstrādātu noteiktus piedāvājumus vai darījumu rindas, varat izmantot *atlaižu rīku*, lai vienlaikus apstrādātu vairākus darījumus. Pēc izvēles var lietot ierakstu filtrus un/vai uzstādīt periodisku grafiku. Nav jāatlasa neviena rinda. Sistēma apstrādās visas rindas, kas atbilst iestatītajām datumu un filtrēšanas prasībām.

Lai apstrādātu piedāvājumus, izmantojot atlaižu rīku, rīkojieties šādi.

1. Ejiet uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Atlaižu rīks**.
1. Darbību rūts cilnes **Atlaižu rīks** grupā **Apstrāde** atlasiet vienu no šīm komandām:

    - **Apstrāde \> Nodrošinājums** – nosako uzkrājumu komplektu katrai attiecīgā piedāvājuma rindai, bet negrāmato uzkrājumus.
    - **Apstrāde \> Atlaižu pārvaldība** – apstrādājiet darījumu sēriju, kas nodrošina atlaides vērtību katrai piedāvājuma rindai.
    - **Process \> Norakstīt** - apstrādājiet atšķirību starp nodrošinājumu un atlaižu pārvaldību, kas tiek grāmatota katram avota darījumam katrā atlaižu darījumā un noteiktā periodā.

1. Dialoglodziņā **Atlaižu pārvaldība** sadaļā **Periods** iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu aprēķina datumu diapazonu.
1. Sadaļā **Garantētais periods** iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu garantiju aprēķina datumu diapazonu.
1. Kopsavilkuma cilnē **Iekļaujamie ieraksti** var uzstādīt filtrus, lai ierobežotu piedāvājumu kopu, ko pakešuzdevums apstrādās. Šie iestatījumi darbojas tāpat kā citi pakešuzdevumu tipi.
1. Ja nepieciešams, jūs varat ātrajā cilnē **Palaist fonā** uzstādīt automātisku atjauninājumu kā pakešuzdevumu. Šie iestatījumi darbojas tāpat kā citi pakešuzdevumu tipi.
1. Atlasiet **Labi**, lai palaistu un/vai plānotu aprēķinu.

## <a name="view-and-edit-rebate-management-transactions"></a>Skatīt un rediģēt Atlaižu pārvaldības darbības

Apstrādājot vienu vai vairākus piedāvājumus, sistēma izveido darbības, kuras var skatīt un, iespējams, rediģēt pirms to grāmatošanas.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-deals-list-page"></a>Skatīt un rediģēt atlaižu pārvaldības transakcijas, izmantojot atlaižu darījumu saraksta lapu

Lai skatītu un rediģētu atlaižu pārvaldības transakcijas, izmantojot atlaižu darījumu saraksta lapu, veiciet šīs darbības.

1. Izpildiet kādu no šīm darbībām:

    - Atlasiet darījumu, par kuru skatīt darbības (piemēram, [**Visi atlaižu pārvaldības piedāvājumi** lapā](rebate-management-deals.md)). Darbību rūts cilnes **Atlaižu pārvaldības piedāvājumi** grupā **Darbības** atlasiet **Darbības** vai **Garantijas darbības** atkarībā no darbības tipa, kuru vēlaties skatīt.
    - Atlasiet darījumu, par kuru skatīt darbības (piemēram, [**Visi atlaižu pārvaldības piedāvājumi** lapā](rebate-management-deals.md)), lai skatītu detalizētu informāciju. Kopsavilkuma cilnē **Atlaižu pārvaldība** atlasiet darījuma rindu, lai skatītu darbības. Pēc tam rīkjoslā atlasiet **Darbības** vai **Garantijas darbības** atkarībā no darbības tipa, kuru vēlaties skatīt. (Šīs pogas ir pieejamas tikai piedāvājumiem, kuros lauks **Saskaņot** ir iestatīts uz *Rinda*.)

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

    - Darbību rūtī atlasiet **Grāmatot**, lai grāmatotu prasību visām attiecīgajām rindām. Ja izmantojat prasību procesu (kad opcija **Izmantot prasības procesu** ir iespējota lapā **Atlaižu pārvaldības parametri** ), tiek grāmatotas tikai tās rindas, kas ir atzīmētas kā **Pieprasītas**. Pretējā gadījumā tiek grāmatoti visi atlasīto atlaižu darījumu avota darījumi. Poga **Grāmatot** ir pieejama tikai atlaižu darbībām. Tas nav pieejams uzkrājumu un norakstīšanas darījumiem. Dialoglodziņā **Grāmatot** automātiski tiek iestatīti lauki **No datuma** un Līdz **Līdz datumam**. Iestatiet lauku **Grāmatošanas datums**, tad atlasiet **Labi**.
    - Lai koriģētu summu, kas tiek rādīta jebkurai atvērtai vai negrāmatotai darbībai, atlasiet darbību un pēc tam izpildiet kādu no šīm darbībām:

        - Labojiet vērtību laukā **Labotā summa**.
        - Darbību rūtī atlasiet **Korekcijas iestatīšana**. Pēc tam parādītajā nolaižamajā dialoglodziņā laukā **Labotā summa** ievadiet vērtību.

> [!NOTE]
> Ja izmantojat prasību procesu, apstrādājot nākamo periodu, darbību sarakstā tiks iekļautas visas iepriekšējās grāmatošanas nepieprasītās darbības, kā arī visas jaunās darbības atlasītajam periodam.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-workbench"></a>Skatīt un rediģēt atlaižu pārvaldības transakcijas, izmantojot atlaižu rīku

Lai skatītu un rediģētu atlaižu pārvaldības transakcijas, izmantojot atlaižu rīku, veiciet šīs darbības.

1. Ejiet uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Atlaižu rīks**.
1. Iestatiet lauku **Rādīt** kā *Negrāmatots*.
1. Lapā **Atlaižu rīks** ir redzams transakciju saraksts. Katra transakcija sniedz atbilstošu informāciju. Šīs detaļas mainās atkarībā no transakcijas tipa. Šajā lapā varat veikt tālāk norādītās darbības:

    - Lai skatītu papildinformāciju par jebkuru darbību, atlasiet to un pēc tam atlasiet cilni **Vispārīgi**, **Finanšu dimensija** vai **Dimensija**.
    - Ja izmantojat prasību procesu, varat atzīmēt transakcijas kā pieprasītas vai nepieprasītas. Atlasiet atbilstošās rindas un pēc tam darbību rūts cilnes **Atlaižu rīks** atlasiet vienu no šīm komandām. (Jūs iespējojat prasību procesus [**Atlaižu pārvaldības parametru**](rebate-management-parameters.md) lapā.)

        - **Iestatīt pieprasīto** – atzīmējiet atlasītās darbības kā pieprasītas.
        - **Iestatīt nepieprasīto** – atzīmējiet atlasītās darbības kā nepieprasītas.

    - Lai grāmatotu prasību vienai vai vairākām rindām, atlasiet atbilstošās rindas. Pēc tam darbību rūts cilnē **Atlaižu rīks** atlasiet **Grāmatot**. Poga **Grāmatot** ir pieejama uzkrājuma, atlaides un norakstīšanas transakcijām. Dialoglodziņā **Grāmatot** automātiski tiek iestatīti lauki **No datuma** un Līdz **Līdz datumam**. Iestatiet lauku **Grāmatošanas datums**, tad atlasiet **Labi**.
    - Lai koriģētu summu, kas tiek rādīta jebkurai atvērtai vai negrāmatotai darbībai, atlasiet darbību un pēc tam izpildiet kādu no šīm darbībām:

        - Labojiet vērtību laukā **Labotā summa**.
        - Darbību rūts cilnē **Atlaižu rīks** atlasiet **Iestatīt korekciju**. Pēc tam parādītajā nolaižamajā dialoglodziņā laukā **Labotā summa** ievadiet vērtību.

> [!NOTE]
> Ja izmantojat prasību procesu, apstrādājot nākamo periodu, darbību sarakstā tiks iekļautas visas iepriekšējās grāmatošanas nepieprasītās darbības, kā arī visas jaunās darbības atlasītajam periodam.

## <a name="post-rebates-transactions"></a>Grāmatojiet atlaižu darbības

Lai grāmatotu apstrādāto uzkrājumu, atlaižu pārvaldības summas un norakstīšanas vērtību, jāpalaiž grāmatošanas process. Grāmatošanas process atzīmē uzkrājumu, atlaižu pārvaldības vai norakstīšanas darījumus kā grāmatotus un izveido mērķa darījumu. Ja nav jāpārskata mērķa darījums, šos darījmus var iestatīt tā, lai tie tiktu grāmatoti automātiski.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Sistēmas iestatīšana, lai automātiski grāmatotu visus mērķa darījumus

Lai iestatītu sistēmu visu mērķa transakciju grāmatošanai, tiklīdz tās tiek ģenerētas, grāmatojot uzkrājumu, atlaižu pārvaldību un norakstīšanu, ieslēdziet opciju **Automātiski grāmatot žurnālus** un/vai **Automātiski grāmatot brīva teksta rēķinus** lapā **Atlaižu pārvaldības parametri**. Plašāku informāciju skatiet [Atlaižu pārvaldības parametri](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Grāmatot darbības vienam vai vairākiem piedāvājumiem

Pēc attiecīgo darījumu apstrādes izpildiet šīs darbības, lai pārskatītu un grāmatotu ģenerētās darbības visām rindām vienam vai vairākiem darījumiem.

1. Atveriet atbilstošo [atlaižu piedāvājumu saraksta lapu](rebate-management-deals.md) tam piedāvājuma veidam, ar kuru vēlaties strādāt.
1. Atlasiet rindu katram darījumam, kuru vēlaties grāmatot (vai atveriet darījumu, kuru vēlaties grāmatot).
1. Darbību rūts cilnes **Atlaižu pārvaldības piedāvājumi** grupā **Ģenerēt** atlasiet vienu no šīm komandām:

    - **Grāmatot \> Nodrošinājums** – grāmatojiet pieejamās uzkrāšanas darbības, kuras esat izveidojis.
    - **Grāmatot \> Atlaižu pārvaldība** – grāmatojiet pieejamās atlaižu darbības, kuras esat izveidojis.
    - **Grāmatot \> Norakstīšana** – grāmatojiet pieejamās norakstīšanas darbības, kuras esat izveidojis.

1. Parādītajā dialoglodziņā iestatiet lauku **Grāmatošanas datums**. Parādītajā dialoglodziņā iestatiet laukus **No datuma** un **Līdz datumam**, lai definētu grāmatojamo darījumu diapazonu.
1. Atlasiet **Labi**, lai grāmatotu darījumus.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Grāmatot darījumus vienu vai vairākas konkrētas piedāvājuma rindas atlasītajam piedāvājumam

Pēc attiecīgo darījumu apstrādes izpildiet šīs darbības, lai pārskatītu un grāmatotu ģenerētās darbības vienai vai vairākām noteiktām darījuma rindām atlasītajam darījumam. Šī procedūra ir piemērojama tikai darījumiem, kuros lauks **Saskaņot** ir iestatīts uz *Rinda*.

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

### <a name="post-transactions-by-using-the-rebate-workbench"></a>Grāmatot transakcijas, izmantojot atlaižu rīku

Pēc tam, kad esat apstrādājis uzkrājuma, atlaides vai norakstīšanas transakcijas, veiciet šīs darbības, lai izmantotu šo atlaižu rīku, lai pārskatītu un grāmatotu ģenerētās transakcijas vienai vai vairākām specifiskām transakciju rindām visiem darījumiem.

1. Ejiet uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Atlaižu rīks**.
1. Režģī atlasiet rindu katrai transakcijas rindai, kuru vēlaties grāmatot. Var atlasīt negrāmatotās uzkrājuma, atlaides un/vai norakstīšanas transakcijas. Ir spēkā šādi nosacījumi:

    - Sistēma arī grāmatos visas rindas, kurām ir tāda pati vērtība **Atlaides transakcijas numurs** kā jūsu atlasāmajām rindām.
    - Sistēma negrāmatos nevienu transakcijas veida *Atlaide* rindu, kas nav atzīmēta kā pieprasīta.
    - Ja atlasīsiet rindas, kas jau ir iegrāmatotas, sistēma izlaiž iegrāmatotās rindas.
    - Poga **Grāmatot** ir pieejama tikai tad, ja atlasāt vismaz vienu negrāmatoto rindu.

1. Darbību rūtī cilnes **Atlaižu rīks** grupā **Apstrāde**, atlasiet **Grāmatot**.
1. Dialoglodziņā **Grāmatot** iestatiet lauku **Grāmatošanas datums**. Lauki **No datuma** un **Līdz datumam** tiek iestatīti automātiski, pamatojoties uz agrāko **No datuma** vērtību un pēdējo **Līdz datumam** vērtību atlasītajām rindām.
1. Atlasiet **Labi**, lai grāmatotu darījumus.

## <a name="review-rebate-management-journals"></a><a name="review-journals"></a>Atlaižu pārvaldības žurnālu pārskatīšana

Pēc transakciju iegrāmatošanas varat pārskatīt iegūtos žurnālus, dokumentus vai preces. Atlaižu un autoratlīdzību mērķa darbību pamatā ir maksājuma tips, kas iestatīts grāmatošanas metodē, un atlaides izvades tips. Piemēram, ja atlaides izvade ir iestatīta uz *Krājums*, debitora atlaidei tiks izveidots pārdošanas pasūtījums, un kreditora atlaidei tiks izveidots pirkšanas pasūtījums. Šos pasūtījumus var apskatīt, izmantojot mērķa darījumus. Ja maksājums ir iestatīts kreditoru atlaižu izmantošanai, debitora atlaidēm tiek izveidots kreditora rēķins kreditoram, kas iestatīts debitoram.

### <a name="review-journals-by-using-the-rebate-deals-list-page"></a>Pārskatīt žurnālus, izmantojot atlaižu darījumu saraksta lapu

Lai pārskatītu žurnāla ierakstus, kas ir saistīti ar atlaižu pārvaldības darījumu, rīkojieties šādi.

1. Atveriet atbilstošo [atlaižu piedāvājumu saraksta lapu](rebate-management-deals.md) tam piedāvājuma veidam, ar kuru vēlaties strādāt.
1. Atlasiet darījumu, kura grāmatošanai jāpārbauda žurnāla ieraksti.
1. Darbību rūts cilnes **Atlaižu pārvaldības piedāvājumi** grupā **Darbības** atlasiet **Darbības** vai **Garantiju darbības** atkarībā no darbības tipa, kuru vēlaties skatīt.
1. Iestatiet lauku **Rādīt** kā *Visus* vai *Grāmatotus*.
1. Atrodiet un atlasiet darbību kolekciju, kuru vēlaties pārbaudīt, un pēc tam darbību rūtī atlasiet vienu no šīm pogām. (Šīs pogas ir pieejamas tikai tad, ja atlasītajai darbību kolekcijai ir atbilstoši grāmatojumi.)

    - **Mērķa darbības** – pārskatiet atbilstošos žurnālus un cita veida dokumentus, ko ģenerējis atlasītais darījums.
    - **Krājumi** – pārskatiet atbilstošos pārdošanas pasūtījumus vai pirkšanas pasūtījumus, ko ģenerējis atlasītais darījums.

1. Tiek parādīts atbilstošo žurnālu, dokumentu vai preču saraksts. Lai skatītu papildinformāciju par jebkuru žurnālu, dokumentu vai vienumu, atlasiet tā rindu un pēc tam darbību rūtī atlasiet **Skatīt detalizētu informāciju**.

### <a name="review-journals-by-using-the-rebate-workbench"></a>Pārskatiet žurnālus, izmantojot atlaižu rīku

Lai pārskatītu žurnālus, izmantojot atlaižu rīku, rīkojieties šādi.

1. Ejiet uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Atlaižu rīks**.
1. Iestatiet lauku **Rādīt** kā _Visus_ vai _Grāmatotus_.
1. Atrodiet un atlasiet rindu, kuru vēlaties pārbaudīt. Pēc tam darbību rūts cilnē **Atlaižu rīks** grupā **Skatīt** atlasiet **Mērķa transakcijas**. Šī poga ir pieejama tikai tad, ja atlasītajai rindai pastāv atbilstoši grāmatojumi.
1. Tiek parādīts atbilstošo žurnālu, dokumentu vai preču saraksts. Lai skatītu papildinformāciju par jebkuru žurnālu, dokumentu vai vienumu, atlasiet tā rindu un pēc tam darbību rūtī atlasiet **Skatīt detalizētu informāciju**.

## <a name="rebate-management-transactions-on-the-deduction-workbench"></a>Atlaižu pārvaldības transakcijas ieturējumu rīkā

Kad grāmatojat atlaižu pārvaldības transakciju, kurai ir kāda no šādām **Maksājuma veida** vērtībām, sistēma izveido debitoru ieturējumu žurnālu vai brīva teksta rēķinu atbilstošam debitora kontam:

- Ieturējumi debitoriem
- Debitoru nodokļu rēķina ieturējumi
- Tirdzniecības izdevumi
- Pārskatu veidošana

Pēc mērķa transakcijas izveides un grāmatošanas tā būs pieejama kā atvērta transakcija lapā **Ieturējumu rīks** (**Pārdošana un mārketings \> Tirdzniecības atlaides \> Ieturējumi \> Ieturējumu rīks**). Atvērtajām transakcijām ir *Atlaižu pārvaldības* vērtība **Prasības veids**, un vērtība **Atlaides transakcijas numurs** ir pieejama, lai iespējotu izsekošanu. Datums ir iestatīts uz atlaižu pārvaldības mērķa transakcijas grāmatošanas datumu. Lai izmantotu ieturējumu rīku, lai nosegtu atvērtās transakcijas ar esošajiem ieturējumiem tam pašam debitora kontam, darbību rūtī atlasiet **Uzturēt \> Saskaņot**.

Papildinformāciju skatiet [Ieturējumu pārvaldīšana, izmantojot ieturējumu rīku](deduction-workbench.md).

## <a name="purge-unposted-transactions"></a>Dzēst negrāmatotās transakcijas

Pēc uzkrājumu, atlaižu vai norakstīšanas transakciju apstrādes izpildiet šīs darbības, lai dzēstu atlasītās negrāmatotās transakcijas.

1. Ejiet uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Atlaižu rīks**.
2. Iestatiet lauku **Rādīt** kā *Negrāmatots*.
3. Atrodiet un atlasiet dzēšamās transakcijas. Pēc tam darbību rūtī cilnes **Atlaižu rīks** grupā **Apstrāde**, atlasiet **Tīrīt**.
4. Atlasiet **Labi**, lai dzēstu negrāmatotas transakcijas.

## <a name="cancel-a-posted-provision"></a>Atceliet grāmatotus uzkrājumus

Pēc uzkrājumu apstrādes un grāmatošanas veiciet šīs darbības, lai atceltu iegrāmatotās uzkrājumu transakcijas.

1. Ejiet uz **Atlaižu pārvaldība \> Atlaižu pārvaldības darījumi \> Atlaižu rīks**.
2. Iestatiet lauku **Rādīt** kā *Grāmatots*.
3. Atrodiet un atlasiet uzkrājumu transakcijas, kuras ir jāatceļ. Pēc tam darbību rūtī cilnes **Atlaižu rīks** grupā **Apstrāde**, atlasiet **Atcelt uzkrājumu**.
4. Atlasiet **Labi**, lai atgrieztu darījumus.

Šīs uzkrājumu atgriešanas būs redzamas arī atbilstošos [Atlaižu pārvaldības žurnālos](#review-journals).
