---
title: Atribūtu un atribūtu grupu pārvaldība
description: Šajā rakstā ir aprakstīts, kā pārvaldīt atribūtus un atribūtu grupas, lai aprakstītu preces un to īpašības Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386977"
---
# <a name="manage-attributes-and-attribute-groups"></a>Atribūtu un atribūtu grupu pārvaldība

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pārvaldīt atribūtus un atribūtu grupas, lai aprakstītu preces un to īpašības Microsoft Dynamics 365 Commerce.

*Atribūti nodrošina* veidu, kā aprakstīt preces un to īpašības, izmantojot lietotāja definētos laukus. Piemēri ietver atmiņas lielumu, cietajā diskā saglabāto noslodzi un saskaņotību ar enerģijas izmēriem.

Atribūtus var saistīt ar dažādām Commerce vienībām, piemēram, preču kategorijām un kanāliem, tiem var iestatīt noklusētās vērtības. Ja atribūti ir saistīti ar preču kategorijām vai kanāliem, preces pārmanto šīs īpašības un to noklusējuma vērtības. Noklusējuma atribūtu vērtības var ignorēt atsevišķā preču līmenī, kanāla līmenī vai katalogā.

Piemēram, parastam televizoram var būt tālāk minētie atribūti.

| Kategorija   | Atribūts           | Pieļaujamās vērtības                        | Noklusētā vērtība |
|------------|---------------------|-------------------------------------------|---------------|
| TV un Video | Zīmols               | Jebkura derīga zīmola vērtība                     | Neviens          |
| TV         | Ekrāna izmērs         | 20–85 collas                              | 55 collas     |
|            | Vertikālā izšķirtspēja | 4K (2160p), pilns HD (1080p) vai HD (720p) | 4K (2160p)    |
|            | Ekrāna atsvaidzes intensitāte | 60 Hz, 120 Hz, vai 240 Hz                     | 60 Hz          |
|            | HDMI ievades         | 0–10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Atribūti un to veidi

Atribūti ir balstīti uz *atribūtu veidiem*. Atribūta tips identificē datu tipu, ko var ievadīt noteiktam atribūtam. Programmā Commerce tiek atbalstīti šādi atribūtu tipi:

- **Valūta** – šis veids atbalsta valūtas vērtību. Tas var būt saistīts (var atbalstīt vērtību diapazonu) vai palikt atvērts.
- **DateTime** – šis veids atbalsta datuma un laika vērtības. Tas var būt saistīts vai palikt atvērts.
- **Decimāldaļa** – šis veids atbalsta skaitliskās vērtības, kas ietver decimāldaļskaitļus. Tas atbalsta arī mērvienības. Tas var būt saistīts vai palikt atvērts.
- **Vesels skaitlis** – šis veids atbalsta skaitliskas vērtības. Tas atbalsta arī mērvienības. Tas var būt saistīts vai palikt atvērts.
- **Teksts** – šis veids atbalsta teksta vērtības. Tas atbalsta arī iepriekš definētu iespējamo vērtību kopu, ja fiksētā **saraksta iestatījums** ir aktivizēts.
- **Būla** – šis veids atbalsta binārās vērtības (**true** vai **false**).
- **Atsauce** – šis veids satur atsauces uz citiem atribūtiem.

> [!NOTE]
> Azure meklēšanas [indeksa ierobežojumu dēļ decimāldaļskaitļu](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search)**atribūta** veids netiek atbalstīts mākoņa meklēšanas pieredzei. Azure kolitive meklēšana neatbalsta **decimāldaļskaitļu atribūtu tipu** **pārvēršanu uz Edm.Double mērķa** indeksa lauku tipiem, jo šī pārvēršana samazinās precizitāti.

### <a name="set-up-attribute-types"></a>Iestatīt atribūtu tipus

Lai iestatītu atribūtu tipus, izpildiet šajā piemērā aprakstītās procedūras darbības.

1. Kā tirdzniecības pārvaldnieku piesakieties komercijas galvenajā birojā.
1. Pārejiet uz **sadaļu Preču informācijas \> pārvaldības \> iestatījuma kategorijas un atribūtu \> atribūtu tipi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Atribūta tipa nosaukums ievadiet** in somas **veidu**.
1. Laukā **Veids** atlasiet **Teksts**.
1. Iestatiet fiksētā **saraksta** opciju kā **Jā**.
1. Kopsavilkuma cilnē **Vērtības** atlasiet **Pievienot**.
1. Lauka Vērtība jaunajā rindā **ievadiet** **Sathall**.
1. Pievienojiet vēl piecas rindas. Katras vērtības **laukā ievadiet citu vērtību:** Attīrīt **,** Purse **, Atpakot,** **Kurjers** **vai Kurjers** **.**
1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Atribūta veida nosaukums** ievadiet **Taslaglas zīmolu**.
1. Laukā **Veids** atlasiet **Teksts**.
1. Iestatiet fiksētā **saraksta** opciju kā **Jā**.
1. Kopsavilkuma cilnē **Vērtības** atlasiet **Pievienot**.
1. Jaunā rindā, laukā **Vērtība**, ievadiet Siam **ban**.
1. Pievienojiet vēl divas rindas. Katras vērtības **laukā** ievadiet citu vērtību: **Aviator vai** **Bakastēr.**
1. Darbību rūtī atlasiet **Saglabāt**.

![Atribūtu tipu lapa.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Iestatīt atribūtu

Lai iestatītu atribūtu, izpildiet šajā piemērā aprakstītās procedūras darbības.

1. Kā tirdzniecības pārvaldnieku piesakieties komercijas galvenajā birojā.
1. Pārejiet **uz informāciju par preču \> informācijas \> pārvaldības iestatījuma kategorijām un atribūtu \> atribūtiem**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā Nosaukums **ievadiet** in somas **veidu**.
1. Laukā **Atribūta tips** atlasiet in somas **veidu**.
1. Darbību rūtī atlasiet **Saglabāt**.

![Atribūtu lapa.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Atribūta metadati

*Atribūta metadati* ļauj atlasīt opcijas, lai norādītu katra preces atribūta izturēšanos. Piemēram, varat norādīt, vai atribūti ir obligāti, vai tos var izmantot meklēšanā un kā filtru.

Precēm atribūtu metadatu iestatījumus var ignorēt kanāla līmenī.

Atribūta atribūtu lapa ietver **vairākas opcijas**, kas ir saistītas ar atribūta metadatiem. Piemēram, **·** **·** **ja komercijas kanālu atribūta metadatos** iestatāt opciju Var precizēt uz Jā, atribūts tiks rādīts preču filtram vai filtrēšanai meklēšanas rezultātos un kategoriju pārlūkošanas lapās. Lai atribūtu konfigurētu kā konfigurējamu, darbību **rūtī** vispirms jāatlasa filtra iestatījumi un jāapstiprina atribūta filtra iestatījumi.

## <a name="filter-settings-for-attributes"></a>Atribūtu filtra iestatījumi

Atribūtu filtra iestatījumi ļauj definēt, kā pārdošanas punktā (POS) tiek rādīti atribūtu filtri. Lai piekļūtu atribūta filtra iestatījumiem atribūtu **atribūtu lapā** darbību rūtī, atlasiet Filtra **iestatījumi**.

Filtra **iestatījumu lapa** ietver sekojošos laukus:

- **Nosaukums** – pēc noklusējuma šis lauks ir iestatīts uz atribūta nosaukumu. Tomēr vērtību var mainīt.
- **Rādīšanas opcija** – ir pieejamas tālāk uzskaitītās opcijas.

    - **Viena vērtība** – opcija ir pieejama šādiem atribūtu veidiem: **Būla**, **Valūta**, **Decimāldaļa**, **Vesels skaitlis** un **Teksts**. Tā ļauj atlasīt tikai vienu vērtību preču saraksta lapu uzlabotājiem, piemēram, kategoriju pārlūkošanai un preču meklēšanas rezultātu lapām.
    - **Vairākas vērtības** – opcija ir pieejama šādiem atribūtu veidiem: **Valūta**, **Decimāldaļa**, **Vesels skaitlis** un **Teksts**. Tas iespējo vairākas vērtības, kas atlasītas atribūtam klientā, uzlabojumui.

- **Rādīšanas vadība** – ir pieejamas tālāk uzskaitītās opcijas.

    - **Saraksts** – šī opcija ir pieejama visiem atribūtu tipiem.
    - **Diapazons** – opcija ir pieejama šādiem atribūtu veidiem: **Valūta**, **Decimāldaļa** un **Vesels skaitlis**.
    - **Slīdnis** – opcija ir pieejama šādiem atribūtu veidiem: **Valūta**, **Decimāldaļa** un **Vesels skaitlis**.
    - **Slīdnis ar joslām** – opcija ir pieejama šādiem atribūtu veidiem: **Valūta**, **Decimāldaļa** un **Vesels skaitlis**.

- **Sliekšņa vērtība** – šis iestatījums ir nepieciešams, ja atlasījāt **Diapazons** kā displeja vadības veidu. Vērtības var definēt, kā atdalītāju izmantojot semikolu (;).

    Piemēram, atribūtam Bag **Volume**, **kura atribūta tips ir Vesels** skaitlis, **sliekšņa vērtība varētu būt 10; 20; 50; 100; 200; 500; 1000; 5000**. Šajā gadījumā POS rādīs tālāk minētos diapazonus. Diapazoni, kuros nav nevienas preces rezultātu kopā, tiks blānēti.

    - Mazāk nekā 10
    - 10–20
    - 20–50
    - 50–100
    - 100–200
    - 200–500
    - 500 vai vairāk

Atribūtu filtra iestatījumi ir piemērojami tikai preču īpašībām, un tos var izmantot, lai uzlabotu preču meklēšanas un kategoriju pārlūkošanas rezultātus. Tie neattiecas uz debitoru meklēšanu vai pasūtījumu meklēšanu, lai gan debitora vai pasūtījuma informācijas bagātināšanai var izmantot vienus un tos pašus atribūtus.

Noklusējuma Commerce moduļos **rādīšanas** **kontroles** filtra iestatījumiem, piemēram, Diapazons, **Dimensija** un Dimensija ar joslām, **nav pieejams neviens papildu atbalsts.** Joprojām **tiek** **atbalstīti** POS **risinājumu diapazona un iestatīšanas iestatījums, bet IestatījumsEco ar joslām ir piemērojams mantojuma tiešsaistes veikala iestatījumam un joprojām ir pieejams trešās** SharePoint puses integrācijai un pielāgotiem scenārijiem.

Mēs iesakām, lai pārdefinējamiem atribūtiem būtu atribūts tā teksta tipam, kur ir aktivizēta pamatlīdzekļu saraksta opcija, un ka saraksts ir **pārvaldāms** **·** (līdz 100–200 unikālām vērtībām). Ja uzlabotājam būs 1000 vai vairāk unikālu vērtību, **·** **atbilstošāk** ir lietot atribūtu teksta tipam, kur atspējota pamatlīdzekļu saraksta opcija.

Tulkojumi ir kritiski atribūtu nosaukumiem un to vērtībām. Atribūtiem ar tipu **Teksts**, kur **aktivizēta** opcija Fiksēts saraksts, atribūtu vērtībām var definēt atribūtu tipu **tulkojumus**. Katram citam atribūta tipam varat definēt tulkojumus lapā, kur definējat atribūtu vērtības. Piemēram, atribūta tipa **atribūtam** varat definēt noklusējuma vērtības tulkojumus **atribūtu lapā**. Tomēr, ja preces līmenī tiek ignorēta noklusējuma vērtība, varat definēt atribūtu tulkojumus **preces īpašību** lapā.

Kad atribūts kanālam ir atzīmēts kā atkārtoti definējams, atribūta tipu nedrīkst atjaunināt. Pretējā gadījumā tiks ietekmēta preču datu publicēšana meklēšanas indeksā. Tā vietā ieteicams izveidot jaunu atribūtu jaunam uzlabotāja tipam un noriet iepriekšējo atribūtu, atņemot to no citām atribūtu grupām.

Tiek atbalstīta meklēšana pēc atribūtiem, bet ineseko tikai rezultātus precīzai meklēšanas vārdu atbilstībai. Piemēram, atribūta **"Sastāvs** " vērtība ir **Cashmmid rīcībā**. Ja debitors meklē "Skaidra nauda", netiks **izgūtas preces, kuru materiālam ir Cashmtona**. Tomēr, ja debitors meklē "Cashmmid", "Debitors" vai "Cashmieri", preces, **kuru** nīkstāļi ir Kā materiāls, tiks izgūtas.

### <a name="additional-attribute-metadata-options"></a>Papildu atribūtu metadatu opcijas

> [!NOTE]
> Šīs atribūtu metadatu opcijas ir piemērojamas tikai mantojuma tiešsaistes SharePoint storefront un ārējām integrācijām. Papildinformāciju par šīm atribūtu metadatu opcijām skatiet [meklēšanas shēmas apskatā serverī SharePoint 2013](/SharePoint/search/search-schema-overview).

Atribūtu lapā ir pieejamas arī šādas papildu atribūtu **metadatu** opcijas:

- Meklējams
- Izgūstams
- Var veidot vaicājumu
- Kārtojams
- Ignorēt burtu reģistru un formatējumu
- Pilnīga atbilstība

Šīs opcijas sākotnēji bija paredzētas, lai uzlabotu meklēšanas funkcionalitāti mantojuma SharePoint tiešsaistes veikalā. Tām nav obligāti jāattiecina uz Commerce e-commerce vietnēm vai POS termināļiem. Tā kā tiek atbalstīta bezatgriezības integrācija, šīs opcijas ir pieejamas atribūtu metadatu eksportēšanai, izmantojot Commerce programmatūras izstrādes komplektu (SDK). Varat lietot Commerce SDK, lai produktus ievietotu pielāgotā, optimizētā ārējās meklēšanas indeksā. Šādā veidā var nodrošināt, ka tiek indeksēti tikai tie atribūti, kas ir jāindeksē.

## <a name="attribute-groups"></a>Atribūtu grupas

Atribūtu *grupa tiek* izmantota, lai preces konfigurācijas modelī grupētu komponenta vai apakškomponenta atsevišķus atribūtus. Atribūtu varat iekļaut arī vairākās atribūtu grupās. Atribūtu grupas var palīdzēt lietotājiem konfigurēt preces, jo dažādas atlases tiek sakārtotas noteiktā kontekstā. Atribūtu grupas varat no jauna piešķirt kategorijām vai kanāliem. Atribūtu grupā atribūtiem var iestatīt arī noklusējuma vērtības.

![Atribūtu grupu lapa](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Izveidot atribūtu grupu

Lai izveidotu atribūtu grupu, izpildiet šajā piemērā aprakstītās procedūras darbības.

1. Kā tirdzniecības pārvaldnieku piesakieties komercijas galvenajā birojā.
1. Pārejiet uz **sadaļu Preču \> informācijas pārvaldības \> iestatījumu kategorijas un atribūtu \> atribūtu grupas**.
1. Izveidojiet atribūtu grupu, kas ir nosaukta **Kārļi Kreklus**.
1. Pievienot šādus atribūtus: CleaningMethod **,** CollarType **,** Collection **un** Design **.**

> [!NOTE]
> Atribūtu grupas atribūtu rādīšanas secības vērtības neietekmē vai attiecas uz uzlabotāju secību meklēšanas un kategoriju pārlūkošanas rezultātos. Tās ir piemērojamas tikai scenārijam "pasūtījuma atribūti".

### <a name="assign-attribute-groups-to-categories"></a>Atribūtu grupu piešķiršana kategorijām

Viena vai vairākas atribūtu grupas var būt saistītas ar kategoriju mezgliem šādos kategoriju hierarhiju tipos:

- Komercijas preču hierarhija
- Kanāla navigācijas kategoriju hierarhija
- Papildu preču kategoriju hierarhija

Kad preces ir iekļautas kategorijās, kas ir saistītas ar atribūtu grupām, tās pārmanto atribūtus, kas ir iekļauti šajās atribūtu grupās.

![Preču īpašību grupu kopsavilkuma cilne Commerce Product Hierarchy lapā.](media/AGRetailProdHierarchy_2022Series.png)

Lai piešķirtu atribūtu grupas kategorijām Commerce preču hierarhijā, izpildiet šīs piemēra procedūras soļus.

1. Kā tirdzniecības pārvaldnieku piesakieties komercijas galvenajā birojā.
1. Pārejiet uz **Mazumtirdzniecība un tirdzniecība \> Preces un kategorijas \> Tirdzniecības preču hierarhija**.
1. Atlasiet modes **navigācijas** hierarhiju.
1. Cilnē **Menspeciāļi** **atlasiet kategoriju Nosūtīšana** **·** **un pēc tam kopsavilkuma cilnē Preces īpašību grupas pievienojiet atribūtu grupu, kuras nosaukums ir Vīriešu summu.**
1. Atlasiet kategoriju **Modernas saulesbrilles** un pārbaudiet jaunos atribūtu grupas **Modernas saulesbrilles** atribūtus, atlasot **Skatītu atribūtus**. Atribūtu grupā jābūt parādītam jaunajam atribūtam **Lēcu forma** un **Saulesbriļļu zīmols**.
1. **Atlasiet Sevī** kategoriju un apstipriniet atribūtus **Vīriešu** atribūtu grupai, atlasot Skatīt **atribūtus**. Atribūtu grupā ir jārāda atribūti **Vīriešu siksnu zīmols**, **Siksnas audums** un **Siksnas lielums**.

To pašu pamata procedūru var izmantot arī, lai piešķirtu atribūtu grupas kategorijām kanāla navigācijas kategoriju hierarhijā un papildu preču kategoriju hierarhijā. Tomēr 2. solī izmantojiet vienu no šiem ceļiem, atkarībā no hierarhijas, kurai vēlaties piešķirt atribūtu grupas:

- **Kanāla navigācijas kategoriju hierarhija: dodieties uz sadaļu** Mazumtirdzniecības un komercijas **kategoriju un preču pārvaldības kanāla \> navigācijas kategorijas \>.**
- **Papildu preču kategoriju hierarhija: dodieties uz sadaļu** **Mazumtirdzniecība un komercijas \> kategorija un preču pārvaldības \> papildu preču kategorijas**.

> [!NOTE]
> Nodrošiniet, lai atribūtu grupas **kategoriju** hierarhijā tiktu sasaistītas tikai kopsavilkuma cilnē Preces atribūtu grupas, **nevis kopsavilkuma cilnē Kategorijas atribūtu** vērtības. Ja atribūti kopsavilkuma cilnē Kategorijas **atribūtu lielumi parādās**, darbību rūtī **atlasiet** Rediģēt kategoriju hierarhiju. Pēc tam Kopsavilkuma cilnē **Kategoriju atribūtu** grupas atlasiet kategoriju mezglus un atlasiet **Noņemt**. Nav atbalsta atribūtu ineses pa kategorijām, izmantojot Commerce Scale Unit.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Identificējiet skatāmus un atkārtoti definējamus atribūtus commerce kanāliem noklusējuma preču kolekcijai

Pēc tam, kad esat saistījuši dažādas atribūtu grupas ar kategorijām dažādās hierarhijās (Commerce preču hierarhijā vai kanāla navigācijas kategorijās) un definētu atribūtu vērtības katrai precei, balstoties uz kategoriju saistību, **ir** jāiespējo atribūts Rādīt kanāla karodziņā, lai padarītu šos atribūtus skatāmus noteiktā kanālā.

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Kanālu kategorijas un preču īpašības**.
1. Atlasiet **Atribūtu metadatu iestatīšana** un pēc tam kreisajā navigācijas rūtī atlasiet atribūtu.
1. Kopsavilkuma cilnē **Kanāla preces īpašības** (**nevis** kategoriju īpašības **FastTab** **·**) iestatiet opciju Rādīt kanāla atribūtu uz Jā, lai atribūtu padarītu skatāmu.
1. Ja vēlaties, lai atribūts arī būtu refinējams, iestatiet **opciju Var precizēt** uz **Jā**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Kontrolēt uz dimensiju balstītu uzlabotāju redzamību, piemēram, izmēru, stilu un krāsu

Preču dimensijas, piemēram, izmērs, stils un krāsa, ir visbiežāk izmantotie uzlabotāji. Lai šīs preces dimensijas padarītu pieejamas kā uzlabotājus, atribūtu grupa ir jāsaista kanāla līmenī, kas satur atsauci uz atribūta tipu, kas automātiski pārmanto vērtības no preces dimensiju vērtībām.

Varat norādīt, ka preces dimensijas ir skatāmas un refinējamas, atjauninot karodziņus **kanāla kategoriju un preču īpašību** lapā. Navigācijas rūtī atlasiet saknes zaru un **pēc tam kopsavilkuma cilnē Kanāla preces īpašības iestatiet opciju Rādīt kanāla atribūtus** **·** **·** **uz** Jā atribūtiem Izmērs, **Stils** **un** Krāsa. Ja vēlaties, lai šie atribūti arī būtu atkārtoti jādefinē, **katram iestatiet opciju** Var precizēt **uz** Jā.

![Atribūtu metadatu iestatīšana dimensiju uzlabotājiem.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Lai iespējotu atribūtus tā, ka tie ir pieejami uz demonstrācijas datiem balstītā Uz cēlu kanālu, izpildiet šīs piemēra procedūras soļus.

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Kanālu kategorijas un preču īpašības**.
1. Atlasiet kanālu **Hjūstona**.
1. Darbību rūtī atlasiet **Atribūtu metadatu iestatīšana**.
1. Atlasiet kategorijas mezglu **Mode** un pēc tam kopsavilkuma cilnē **Kanāla preces īpašības** katram atribūtam atlasiet **Iekļaut atribūtu**.
1. Atlasiet kategorijas mezglu **Modes aksesuāri**, atlasiet kategoriju **Modernas saulesbrilles** un pēc tam kopsavilkuma cilnē **Kanāla preces īpašības** katram atribūtam atlasiet **Iekļaut atribūtu**.
1. Atlasiet kategorijas mezglu **Vīriešu apģērbi**, atlasiet kategoriju **Bikses** un pēc tam kopsavilkuma cilnē **Kanāla preces īpašības** katram atribūtam atlasiet **Iekļaut atribūtu**.
1. Pēc atribūtu metadatu atjaunināšanas paredzētajiem atribūtiem un uzlabotājiem nodrošiniet, lai **jūs saglabātu izmaiņas un palaistu publicēšanas kanāla atjaunināšanas** darbu. Pēc tam pēc atjauninājumu publicēšanas ir jāpalaiž šādi darbi: 1070 (kanāla konfigurācija), **1040** (**Preces**) **un 1150** (**katalogs**).**·** **·**

> [!NOTE]
> - Ja jūsu uzņēmumam bieži jāpievieno vai jānoņem preces navigācijas hierarhijā vai jāveic tādas izmaiņas kā rādīšanas pasūtījuma vērtību atjaunināšana, jaunu kategoriju pievienošana un jaunu atribūtu grupu pievienošana kategorijām, **ieteicams** konfigurēt publicēt kanāla atjauninājumus, lai tas tiktu paveikts kā pēdējais pakešuzdevums. Vai arī manuāli **aktivizēiet darbu Publicēt kanāla atjauninājumus un** pēc tam tālāk norādītos (CDX) darbus: Commerce Data Exchange 1070 **(** Kanāla **konfigurācija),** 1040 **(** Preces **·**) un 1150 **(** Katalogs **).**
> - Opcija **Mantot** ļauj norādīt, ka kanālam ir jāmanto atribūtu grupas no tā hierarhijas vecākelementa kanāla. Ja opcijai **Mantot** iestatīsiet **Jā**, atvasinātā kanāla mezgls pārmantos atribūtu grupas un visus atribūtus no šīm atribūtu grupām.
> - Ja atribūta **metadatu iestatīšanas** poga darbību rūtī nav pieejama, nodrošiniet, **lai** navigācijas hierarhija būtu saistīta **ar** kanālu kopsavilkuma cilnē Vispārīgi.
> - Jūs nedrīkstat saistīt nevienu atribūtu grupu, izņemot atribūtu grupas, kas pamatotas uz dimensijām kanāla līmenī (piemēram, **·** **atribūtu grupās kanāla kategorijās un preču īpašību** lapā).
> - Pēc atbalsta ievads debitoriem specifiskajiem "uz bizness-biznesam" katalogiem Commerce versijā 10.0.27, ir paredzēts identificēt uzlabotāju un atribūtu iestatījumus katram B2B katalogam tādā pašā veidā, kā aprakstīts šajā rakstā.

## <a name="override-attribute-values"></a>Ignorēt atribūtu vērtības

Preču līmenī var ignorēt atsevišķu preču atribūtu noklusējuma vērtības. Tos var ignorēt arī atsevišķām precēm konkrētos katalogos, kas tiek mērķēti konkrētos kanālos.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Atsevišķas preces atribūtu vērtību ignorēšana

Lai ignorētu atsevišķas preces atribūtu vērtības, izpildiet šajā piemērā veiktajā procedūrā aprakstītās darbības.

1. Kā tirdzniecības pārvaldnieku piesakieties komercijas galvenajā birojā.
1. Dodieties uz **Sadaļu Mazumtirdzniecība un \> Komercija, Kā arī Pēc kategorijas \> izlaisto preču pārvaldība**.
1. Izvēlieties **Modes \> modes piederumi \> modes modes modes preces**.
1. Režģī atlasiet nepieciešamo preci. Pēc tam darbību rūts grupas **Iestatīšana** cilnē **Prece** atlasiet **Preces īpašības**.
1. Kreisajā rūtī atlasiet atribūtu un pēc tam labajā rūtī atjauniniet tā vērtību.

![Preces īpašību vērtību lapa.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Ignorēt visu kataloga preču atribūtu vērtības

Lai ignorētu visu preču atribūtu vērtības katalogā, izpildiet šajā piemērā aprakstītās procedūras darbības.

1. Kā tirdzniecības pārvaldnieku piesakieties komercijas galvenajā birojā.
1. Dodieties uz **sadaļu Mazumtirdzniecības un Commerce \> Catalog management \> visi katalogi**.
1. Atlasiet katalogu **Fabrikam Base Catalog**.
1. Izvēlieties **Modes \> modes piederumi \> modes modes modes preces**.
1. Kopsavilkuma cilnē **Preces** atlasiet vajadzīgo preci un pēc tam atlasiet **Atribūti** virs preču režģa.
1. Tālāk minētajās kopsavilkuma cilnēs atjauniniet nepieciešamo atribūtu vērtības.

    - Koplietotie preces plašsaziņas līdzekļi
    - Koplietotās preces īpašības
    - Kanāla plašsaziņas līdzekļi
    - Kanāla preces īpašības

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Ignorēt visu kanāla preču atribūtu vērtības

Lai ignorētu visu preču atribūtu vērtības kanālā, izpildiet šajā piemērā aprakstītās procedūras darbības.

1. Kā tirdzniecības pārvaldnieku piesakieties komercijas galvenajā birojā.
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Kanālu kategorijas un preču īpašības**.
1. Atlasiet kanālu **Hjūstona**.
1. Kopsavilkuma cilnē **Preces** atlasiet vajadzīgo preci un pēc tam atlasiet **Atribūti** virs preču režģa.
1. Ja neviena prece nav pieejama, kopsavilkuma **cilnē** **Preces** atlasiet Pievienot un pēc tam **dialoglodziņā** Pievienot preces atlasiet nepieciešamās preces.
1. Tālāk minētajās kopsavilkuma cilnēs atjauniniet nepieciešamo atribūtu vērtības.

    - Koplietotie preces plašsaziņas līdzekļi
    - Koplietotās preces īpašības
    - Kanāla plašsaziņas līdzekļi
    - Kanāla preces īpašības

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Definēt variantam raksturīgās atribūtu vērtības un definēt vairākas preces īpašību vērtības

Lai definētu variantam specifiskas atribūtu vērtības un definētu vairākas preces īpašību vērtības, izpildiet šīs piemēra procedūras soļus.

1. Kā tirdzniecības pārvaldnieku piesakieties komercijas galvenajā birojā.
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Kanālu kategorijas un preču īpašības**.
1. Atlasiet kanālu **Hjūstona**.
1. Kopsavilkuma cilnē **Preces** atlasiet nepieciešamo preces variantu un pēc tam atlasiet īpašības **virs** preču režģa.
1. Ja neviena prece nav **pieejama** **·**, kopsavilkuma cilnē Preces atlasiet Pievienot un pēc tam dialoglodziņā Pievienot preces atlasiet **nepieciešamos preces** variantus.
1. Tālāk minētajās kopsavilkuma cilnēs atjauniniet nepieciešamo atribūtu vērtības.

    - Koplietotie preces plašsaziņas līdzekļi
    - Koplietotās preces īpašības
    - Kanāla plašsaziņas līdzekļi
    - Kanāla preces īpašības

#### <a name="example-of-variant-specific-attribute-configuration"></a>Variantam raksturīga atribūta konfigurācijas piemērs
        
Šajā piemērā prece P001-Master **ir vairāku aktivitāšu pamata prece,** kam ir trīs varianti: **Running**, **Krājuma** un **Trekings.** Katram variantam jūs vēlaties unikāli definēt atribūta Aktivitāte **vērtību**. Kanāla kategoriju **un preču īpašību** **lapas kopsavilkuma cilnē Preces definējiet variantu aktivitātes atribūta vērtību,** **kā tas ir parādīts šajā tabulā.**

| Variants     | Aktivitātes atribūta vērtība |
|-------------|--------------------------|
| P001-Šablons | Sporta                   |
| P001-1      | Tiek izpildīts                  |
| P001-2      | Iešana                  |
| P001-3      | Pārgājieni                 |

Ja lietotājs meklē "valūtā", **P001-Šablona** prece tiks parādīta meklēšanas rezultātos. **Ja** atribūts Aktivitāte konfigurēts kā refinējams, **·** **aktivitātes** uzlabotājs kā definējama vērtība uzdingēs tikai sporta veidu, **·** **jo šī vērtība tika definēta atribūtam Aktivitāte preču līmenī P001-Master.**

Pēc noklusējuma varianta līmeņa atribūtus ir paredzēts izmantot tikai preces informācijas lapās (PDP). Kad PDP atlasāt noteiktu preces variantu, šim konkrētam variantam tiek atjauninātas preces specifikācijas PDP.

Lai uzlabotāji varētu saņemt preces varianta līmenī definētās atribūtu vērtības, ir jādefinē atribūts preces šablona līmenī, **·** **atzīmējiet izvēles rūtiņu Atļaut vairākas vērtības un iestatiet atribūta tipu uz Teksts.**

Pēc tam jums ir jānosaka visas iespējamās vērtības preces variantiem. Šajā piemērā **izmantotajā** atribūtam **Aktivitāte iespējamās vērtības var būt: Running**, Siam **,** **Dejotā**, **Trekinga**, **Atkātošana**, **Krājumuporti** un **Parkāsporti**.

Pēc varianta atribūta vērtību definēšanas tās var definēt preces šablona līmenī, izmantojot ar pipeti atdalītas vērtības. Atribūtam **Aktivitāte** varat definēt preces šablona īpašības vērtību kā Running **| Ierašanās | Piestācīšana| Trekēšana| Ierašanās | Krājumu | Darba vietas**.

Pēc tam katram variantam ir iespējams definēt atribūtu vērtības, ievadot ar programmkanālu atdalītas vērtības vai arī atsevišķas vērtības. **Atribūtu Aktivitāte** var konfigurēt kā esošu atsevišķu preces **variantu| Ierašanās | Nomāšana**, **darbojas**, **darbojas| Piestācīšana| Krājumu pārstās** utt.

Pēc varianta **atribūtu vērtību definēšanas kanāla kategoriju un preču īpašību lapā darbību** **rūtī** atlasiet Publicēt kanāla atjauninājumus un pēc tam izpildiet darbus **1150**, **1040** un **1070.**

Kad darbi ir pabeigti un meklēšanas indekss ir atjaunināts, visām paredzamajām vērtībām ir jāparādās meklēšanas rezultātos un kategoriju pārlūkošanas rezultātos.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
