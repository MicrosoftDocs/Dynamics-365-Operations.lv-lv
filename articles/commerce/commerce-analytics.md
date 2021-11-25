---
title: Commerce Analytics (priekšskatījums)
description: Šajā tēmā sniegta detalizēta informācija par analīzes iespējas instalēšanu un lietošanu Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/15/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7f3e51cc3f7314bd33bca9e598bd0b1c9118caef
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817457"
---
# <a name="commerce-analytics-preview"></a>Commerce Analytics (priekšskatījums)

[!include [banner](includes/banner.md)]

Commerce Analytics ir funkcionālās analīzes iespēja, kas iekļauta Dynamics 365 Commerce. Šajā tēmā sīkāk aprakstīta Commerce Analytics informācija un skaidrots, kā to instalēt. 

## <a name="system-architecture"></a>Sistēmas arhitektūra
### <a name="key-components"></a>Galvenie komponenti
Commerce Analytics sastāv no šādiem galvenajiem komponentiem:
- Gatavs izmantot interaktīvus Power BI pārskatus
- SQL skati Azure Synapse analīzes pakalpojumā
- Elementa un ontoloģijas dati Azure datu līdzās
- Neapstrādātie dati Azure datu pārsūtīšanai

![Sistēmas arhitektūra Commerce Analytics](media/CommerceAnalytics.png)

### <a name="data-flow"></a>Datu plūsmas
#### <a name="step-1-data-generation"></a>1. darbība: datu ģenerēšana
Dati rodas kā darbību dati vai uzvedības dati no viena no šiem avotiem:
- Zvanu centra piesaiste, izmantojot Commerce HQ klientu, lai apstrādātu pārdošanas pasūtījumus
- Kasieris pārdošanas punktā (POS), kas apstrādā pārdošanas darbības
- Pārdošana, kas izveidota pielāgotās programmās, izmantojot bezatdošanas commerce (Commerce Scale Unit)
- E-commerce shopper pārlūkošana jūsu e-commerce vietnē 
- E-komercijas veikalā, kas ievieto pasūtījumu jūsu e-komercijas vietnē
- Citu sistēmu saražotie dati, piemēram, Dynamics 365 Connected Spaces

#### <a name="step-2-ingestion-and-pre-processing"></a>2. solis. Iesācīšana un pirmapstrāde
Transakciju dati ievada Commerce HQ tieši (pasūtījumus, kas ir notverti tieši Commerce HQ klientā) vai Commerce Scale Unit (pasūtījumi, kas notverti POS, e-komercijai, vai pielāgotos klientus, izmantojot Bezatgriezuma Commerce). 

Tad transakciju dati tiek pārkopti uz jūsu Azure datu Pārsūtīšanas kā neapstrādātie dati ar funkciju Eksportēt uz datu Par sakopošanu, un dati tiek glabāti **·** mapē "Tabulas". E-komercijas tīmekļa aktivitātes dati tiek sūtīti tieši uz datu darbību.

Citu sistēmu izveidotie dati, Dynamics 365 Connected Spaces piemēram, arī tiek nosūtīti tieši uz datu darbību.

#### <a name="step-3-transformation-and-aggregation"></a>3. darbība: pārvēršana un apkopošana
Kad neapstrādātie dati ir datu reģistrācijā, Commerce Analytics Service nolasa datus, pārveido, uzkopē tos un ieraksta tos atpakaļ datu ierakstītājā loģisko entītiju formā mapē "Entītijas" un apkopotos rādītājus mapē "Ontoloģijas". 

#### <a name="step-4-querying"></a>4. darbība: vaicājums
Dati, kas atrodas uz vietas, tiek vaicāti, izmantojot T-SQL interfeisu, Azure Synapse izmantojot Analīzes. Interfeiss ietver SQL skatījumus, kas ļauj izmantot pārsūtīšanas datu ārējo vaicājumu, vai nu tieši izmantojot T-SQL klientu ekspromta analīzei, vai izmantojot vizualizēšanas rīku, Power BI piemēram, .

#### <a name="step-5-modeling-and-serving"></a>5. solis. Modelēšana un apkalpošana
Pēc tam Analīzes Azure Synapse vaicājumā šie dati tiek Power BI aizķerti ar semantisko modeli. Atkarībā no datu tipa tie tiek importēti atmiņā periodiski vai tieši vaicājumā Power BI izpildes laikā. 

Pēdējais posms ir dati, kas tiks atveidoti vizuāli, Power BI lai lietotāji varētu skatīt un mijiedarboties. 

## <a name="commerce-analytics-functional-overview"></a>Commerce Analytics funkcionālā pārskata apskats
### <a name="1-summary"></a>1. Kopsavilkums
#### <a name="top-level-filters"></a>Augstākā līmeņa filtri
1.  Datuma iestatījumi
    1. Gads
    2. Ceturksnis    
    3. mēnesis;    
    4. Nedēļa    
    5. diena;
2. Kanāla iestatījumi
    1. Juridiska persona    
    2. Kanāla veids    
    3. Debitora veids    
    4. Pārdošanas tips    
    5. Kanāls    
    6. Organizācijas hierarhija
3. Preces iestatījumi
    1. Kategoriju hierarhija    
    2. Kategorija

#### <a name="a-product"></a>a. Prece
1. Pārdošana
2. Peļņa
3. Atgriešanas darbības

#### <a name="b-customer"></a>b. Debitors
1. Pārdošana
2. Peļņa
3. Atgriešanas darbības

#### <a name="c-channel"></a>c. Kanāls
1. Pārdošana
2. Peļņa
3. Atgriešanas darbības

### <a name="2-sales"></a>2. Pārdošana
1. Pēc piegādes vietas
2. Pēc kanāla/veikala/termināļa
3. Pa darbiniekiem
4. Pēc datuma
5. Pa stundām
6. Pēc preču kategorijas

### <a name="3-margin"></a>3. Peļņa
1. Pēc piegādes vietas
2. Blakusprodukts
3. Pēc datuma

### <a name="4-return"></a>4. Atgriešana
1. Atgriešana pēc summas
    1. Pēc veikala    
    2. Blakusprodukts    
    3. Pēc datuma
2. Atgriešana pēc darbības
    1. Pēc veikala    
    2. Blakusprodukts    
    3. Pēc datuma

### <a name="5-discount"></a>5. Atlaide
1. Pēc veikala
2. Blakusprodukts
3. Pēc datuma
4. Dekompozīcija
    1. Juridiska persona    
    2. Veikals    
    3. Atlaides veids    
    4. Atlaides nosaukums    
    5. Prece

### <a name="6-payment"></a>6. Maksājums
1. Pēc kanāla/termināļa
2. Pēc maksāšanas metodes/tipa
3. Pēc datuma
4. Dekompozīcija
    1. Juridiska persona    
    2. Kanāla veids    
    3. Veikals    
    4. Terminālis    
    5. Maksāšanas veids

### <a name="7-customer"></a>7. Debitors
1. Kalpošanas laika vērtība (LTV): kalpošanas laika vērtība tiek aprēķināta, pamatojoties uz kopējo summu, ko debitors izmanto visos Commerce Pārdošanas kanālos (POS, e-komercija un zvanu centrā).
2. Recency: recency tiek aprēķināts, ņemot vērā dienu skaitu, kopš debitora pēdējās transakciju saistības ar organizāciju. Recency neietver darījumu piesaistes signālus, piemēram, e-komercijas pārlūkošanas aktivitāti.
3. Biežums: biežums tiek aprēķināts, ņemot vērā debitora darbības saistībām ar organizāciju. Biežums neietver darījumu piesaistes signālus, piemēram, e-komercijas pārlūkošanas aktivitāti.
4. Attiecību garums. Attiecību garums tiek aprēķināts, pamatojoties uz dienu skaitu, kopš sistēmā tika izveidots debitora ieraksts. 
5. Transakciju skaits

### <a name="8-comparison"></a>8. Salīdzinājums
1. Preču salīdzinājums pēc laika perioda
    1. Pārdošanas un pārdošanas starpība
    2. Uzcenojuma un uzcenojuma starpība
2. Debitors pēc laika perioda
    1. Pārdošanas un pārdošanas starpība
    2. Uzcenojuma un uzcenojuma starpība

### <a name="9-web-activity"></a>9. Tīmekļa aktivitāte

#### <a name="top-level-filters"></a>Augstākā līmeņa filtri
1. Datumu diapazons
2. Kanāla veids
3. Kanāls
4. Kategoriju hierarhija

#### <a name="a-acquisition"></a>a. Iegāde
1. Lapas skati
    1. Pēc valsts/reģiona    
    2. Blakusprodukts    
    3. Kad lietotājs ir pierakstījies statusā    
    4. Pēc datuma
2. E-komercijas pasūtījumi
3. Konvertēšanas maiņas kurss
    1. Pēc datuma
4. Konversijasnels
    1. Lapas skats pēc lapas veida (mājas lapa, kategorijas lapa, lapa ar detalizētu informāciju par preci)  
    2. Pievienot grozam    
    3. Norēķināšanās   
    4. Pirkšana

#### <a name="b-session"></a>b. Sesija
Sesija ir definēta kā lietotāja apmeklējums jūsu e-komercijas vietnē. Sesija tiek uzskatīta par pabeigtu pēc 30 neaktivitātes minūtēm vai pēc 24 aktīvas lietošanas stundām.
1. Pēc valsts/reģiona
2. Pēc izcelsmes (ārējs atsauces lietotājs)
3. Kad lietotājs ir pierakstījies statusā
4. Sesiju skaits
    1. Pēc datuma    
    2. Pēc ierakstu lapas
5. Pasūtījums pa sesijām
    1. Pēc datuma
6. Sesijas sesija sesija: sesijas sesija ir definēta kā sesija, kurā lietotājs nekavējoties pamet pēc jūsu e-komercijas vietnes apmeklējuma. 
7. Klikšķi pa sesijām

#### <a name="c-visitor"></a>c. Apmeklētājs
Jūsu e-komercijas vietnē anonīms identifikators ir noteikts, pamatojoties uz unikālu identifikatoru šajā noteiktajā ierīcē noteiktā pārlūkprogrammā. Commerce Analytics neizseko anonīmos lietotājus dažādās pārlūkprogrammās vai ierīcēs. Anonīms lietotājs, kas izmanto vienu pārlūkprogrammu vienā datorā, ir unikāli identificēts vairākās lietotāja sesijās, līdz pārlūka kešatmiņas dati tiek notīrīti vai parasti līdz 12 mēnešu periodam atkarībā no tā, kas ir pirmais.

Commerce Analytics var sniegt papildu informāciju par to, kas pārlūkot jūsu e-komercijas vietni, kad esat pierakstījies. Informācija ir balstīta uz jūsu esošajām saistībām ar šiem lietotājiem, tostarp pirkšana, ko lietotāji ir veikti no jūsu organizācijas visos Commerce pārdošanas kanālos (POS, zvanu centrā un e-komercija) un ietver recency, attiecību garumu, darbmūžu vērtību un biežumu.

1. Seguma summa
2. Vidējā pasūtījumu vērtība
3. Vidējā pārdošanas vērtība
4. E-komercijas skaits
    1. Pēc datuma
    2. Pēc atrašanās vietas: Commerce Analytics var nodrošināt granularitāti tikai valsts/reģiona līmenī, lai varētu gūt priekšstatu par e-komercijas vietu.     
    3. Pēc recency: recency tiek aprēķināts, ņemot vērā dienu skaitu, kopš debitora pēdējās transakciju saistības ar organizāciju. Recency neietver darījumu piesaistes signālus, piemēram, e-komercijas pārlūkošanas aktivitāti.    
    4. Pēc attiecību ilguma: attiecību garums tiek aprēķināts, pamatojoties uz dienu skaitu, kopš sistēmā tika izveidots debitora ieraksts.     
    5. Pēc darbmūžs vērtības (LTV): kalpošanas laika vērtība tiek aprēķināta, pamatojoties uz kopējo summu, ko debitors izmanto visos Commerce Pārdošanas kanālos (POS, e-komercija un zvanu centrā).
    6. Pēc biežuma: biežums tiek aprēķināts, ņemot vērā debitora darbību saistībām ar organizāciju. Biežums neietver darījumu piesaistes signālus, piemēram, e-komercijas pārlūkošanas aktivitāti.

#### <a name="d-impression"></a>d. Iespaidu
Iespaids ir definēts kā katrs preces vizuālais skatījums, ko veic e-komercijas uzņēmums. Piemēram, ja e-commerce commerce naviģē uz jūsu vietnes sākumlapu un skata matētu preci augšējā pārdošanas saraksta modulī, kā arī skaita to pašu mato preci saraksta moduļa izvēles ietvaros, šīs mijiedarbības tiek skaitītas kā divi produktu skatījumi. Skatījumi izseko preču skatus šādās virsmas:
1. Saraksti (piemēram, rekomendēts, augšējais pārdošanas, izdošanas jums, tendences)
2. Groza modulis
3. Meklēšanas rezultāta konteiners
4. Kategorijas meklēšanas rezultāta konteiners
    
Preces, kas ir atveidotas karuseļa modulī vai pielāgotos vizuļos, netiek skaitītas metriskajā mērījumā.

Pārskatā **par pārskatu par pārskatu ir iekļauti šādi** rādītāji:
1. Iespaida skaits
    1. Pēc lapas tipa un moduļa: lapas veids ir vispārīgs lapas veids, kas katrā e-komercijas vietnes lapā ir definēts katrai lapai. Moduļa tips nosaka e-commerce vizuālā moduļa tipu, kurā tiek rādīta prece. Lai apskatītu rādīšanas pēc moduļa, iespējams, būs nepieciešams detalizēti apskatīt lapu un moduli.    
    2. Blakusprodukts    
    3. Kad lietotājs ir pierakstījies statusā    
    4. Pēc datuma
2. Iespaida klikšķa skaits: klikšķināšana uz e-komercijas ir definēta kā e-komercija, kas klikšķināt uz preces vizuāla, kas parasti pārvieto lietotājus uz šīs preces informācijas lapu.     
3. Iespaida likmi par klikšķa ir norādīta kā kopējais klikšķa skaits, kas dalīts ar sadalāmo tieksmju kopskaitu.

## <a name="install-commerce-analytics"></a>Instalēt Commerce Analytics

> [!NOTE]
> Commerce Analytics ir priekšskatījuma fāzē Amerikas Savienotajās Valstīs, Kanādā, Apvienotajā Karalistē, Eiropā, Dienvidāzijā, Austrumāzijā, Austrālijā, Austrālijā un Japānas reģionos. Ja jūsu vide atrodas jebkurā no šiem reģioniem, varat iespējot Commerce Analytics jūsu vidē ar Microsoft Dynamics Lifecycle Services (LCS). Pirms Commerce Analytics lietošanas skatiet sadaļu [Eksporta konfigurēšana uz Azure data Nosūtīšana](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics"></a>Iespējot un konfigurēt Commerce Analytics
Lai instalētu Commerce Analytics, jums ir nepieciešamas atļaujas, lai izveidotu resursus Azure abonementā un atļaujas programmu instalēšanai LCS. Veiciet tālāk aprakstītos soļus, lai iespējotu un konfigurētu Commerce Analytics.
1. [Iesniegt Priekšskatījuma īso formu Commerce Analytics (Preview)](#submit-the-preview-intake-form-for-commerce-analytics).
2. [Iespējojiet un konfigurējiet eksportēšanu uz datu Failu](#enable-and-configure-export-to-data-lake).
3. [Iespējojiet un konfigurējiet Commerce Analytics (Preview) pievienojumprogrammu](#enable-and-configure-commerce-analytics-add-in).
4. [Ģenerēt glabāšanas konta SAS](#generate-storage-account-sas-token) marķieri
5. [Lejupielādēt izvietošanas skriptus Azure Synapse](#download-deployment-scripts-for-azure-synapse-views) skatiem.
6. [Instalējiet un konfigurējiet Azure Synapse](#install-and-configure-azure-synapse-workspace) darbvietu.
7. [Instalējiet Power BI veidnes](#install-power-bi-template-app) programmu. 

### <a name="submit-the-preview-intake-form-for-commerce-analytics"></a>Iesniegt Priekšskatījuma veidlapas Commerce Analytics laukā
Pabeidziet un iesniedziet [Commerce Analytics (Preview)](https://forms.office.com/r/vW5VLJGXZ2) veidlapas. Lūdzu, uzgaidiet līdz trim darba dienām pieprasījuma apstrādei. Kad forma ir apstrādāta, uz e-pasta adresi, kas norādīta formā, tiks nosūtīts apstiprinājuma e-pasta ziņojums.

### <a name="enable-and-configure-export-to-data-lake"></a>Iespējot un konfigurēt eksportu uz datu failu
Commerce Analytics balstās uz līdzekli Eksportēt uz datu To Data Līdz, lai commerce HQ datus eksportētu uz **Azure Data Analytics un** paturētu datus jaunu. Pirms Commerce Analytics konfigurēšanas iespējojiet un konfigurējiet Eksportēšanu uz datu galapunktu, izpildot darbības, kas izklāstītas sadaļā **Eksporta konfigurēšana uz Azure Data**[...](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) Nosūtīšana. Konfigurējot funkciju **Eksportēt uz datu** Lei, ņemiet vērā šādu informāciju. Šī informācija būs jāievada sekojošās darbībās.
1. Atslēgas Dns nosaukums un slepenie nosaukumi, kur glabā programmas ID un programmas noslēpumu. Papildinformāciju skatiet sadaļā [Noslēpumu pievienošana](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets) atslēgai.
2. Azure datu pārsūtīšanas instances glabāšanas konta nosaukums. Papildinformāciju skatiet [abonementā izveidojiet datu Lei Storage (Gen2)](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription) kontu.

### <a name="enable-and-configure-commerce-analytics-add-in"></a>Commerce Analytics pievienojumprogrammas iespējošana un konfigurēšana
Lai instalētu Commerce Analytics pievienojumprogrammu LCS, jums ir jābūt vides administratoram LCS vidē, ko plānojat izmantot.

Lai konfigurētu Commerce Analytics pievienojumprogrammu, ir nepieciešama šāda informācija. 

|Lauks | Informācijas avots| Paraugs|
|----|----|----|
|Azure AD Nomnieka ID jūsu videi| Jūsu Azure AD nomnieka ID Azure portālā. Pieteikties Azure **portālā** un atvērt **Azure Active Directory** pakalpojumu. Atvērt **rekvizītu** lapu un kopēt vērtību **laukā Direktorija** ID.| 72f988, kas-0000-0000-00000-2d7cd011db47|
|Jūsu atslēgas DNS nosaukums|Ievadiet [jūsu](#enable-and-configure-export-to-data-lake) atslēgas, piemēram, DNS nosaukumu.| `https://contosod365datafeedpoc.vault.azure.net/`|
|Noslēpums, kas satur pieteikuma ID| Ievadiet [slepeno](#enable-and-configure-export-to-data-lake) vārdu, kurā tiek glabāts programmas ID. Šī ir tā pati vērtība, ko izmantojat, **instalējot pievienojumprogrammu Eksportēt** uz datu Neitu.|app-id|
|Noslēpums, kas satur pieteikuma noslēpumu| Ievadiet [slepeno](#enable-and-configure-export-to-data-lake) vārdu, kas glabā pieteikuma noslēpumu. Šī ir tā pati vērtība, ko izmantojat, **instalējot pievienojumprogrammu Eksportēt** uz datu Neitu.| app-secret|

1. Piesakieties [pakalpojumos Lifecycle Services](https://lcs.dynamics.com/) un dodieties uz vidi.
2. Lapā **Vide** atlasiet cilni Vides **·** pievienojumprogrammas.
3. Atlasiet **Instalēt jaunu pievienojumprogrammu un dialoglodziņā atlasiet Commerce** Analytics **(Priekšskatījums).** Ja **Commerce Analytics (Preview)** nav uzskaitīts, pārliecinieties, ka esat pievienojis Insider Programmu.
4. Dialoglodziņā **Iestatīšanas pievienojumprogramma** ievadiet nepieciešamo informāciju, kā aprakstīts augstāk esošajā tabulā.
5. Akceptējiet piedāvājuma noteikumus, atzīmējot izvēles rūtiņu un pēc tam atlasiet **·** Instalēt.

Sistēma instalē un konfigurē Commerce Analytics (Preview) videi. Operācija var ilgt dažas minūtes. Kad instalēšana un konfigurācija ir pabeigta, **Commerce analytics** (Priekšskatījums) ir uzskaitīts **vides lapā un statuss ir** **Instalēts**.

### <a name="generate-storage-account-sas-token"></a>Ģenerēt glabāšanas konta SAS marķieri
> [!NOTE]
> Zināms Commerce Analytics (Preview) ierobežojums ir tāds, ka instance zaudēs piekļuvi datiem, kad Azure Synapse SAS marķieris beidzas. Jums ir jāiestata maksimālais beigu datums, ko atļauj jūsu organizācijas drošības politikas, kad ģenerējiet koplietojamās piekļuves paraksta (SAS) marķieri.

SAS marķieris ļauj ārējām entītijām piekļūt jūsu glabāšanas kontam ar noteiktu privilēģiju kopu noteiktam laika daudzumam. Azure Synapse tiks izmantots SAS marķieris, lai piekļūtu Azure datu Krātuvē pamatdatiem. Lai ģenerētu SAS marķieri, veiciet tālāk aprakstītās darbības.
1. Dodieties uz glabāšanas kontu Azure portālā, ko izveidojāt, konfigurējot eksportēšanu uz **datu Krājumu...**[...](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription)
2. Cilnes **Opcijas** kreisajā pusē zem glabāšanas konta atlasiet Koplietotās **piekļuves** paraksts.
3. SaS opciju lapā atlasiet šādas opcijas:

    | Opcijas nosaukums | Opcijas vērtība |
    |-------------|--------------|
    | Atļautie pakalpojumi | Atlasiet **·** BLOB. |
    | Atļautie resursu tipi | Atlasīt **·** pakalpojumu, **konteineru** un **·** objektu.|
    | Atļautās atļaujas | Atlasiet **·** Lasīt, **·** Rakstīt, **·** **·** Dzēst, **·** Saraksts, Pievienot un **·** Izveidot. |
    | BLOB versijas atļaujas | Atlasiet **Iespējo versiju** dzēšanu. |
    | Sākuma un beigu datums/laiks | Atbilstoši iestatiet SAS marķiera beigu datumu un laiku. |
    | Atļautās IP adreses | Atstāt tukšu. |
    | Atļautie protokols | Atlasiet **tikai** HTTPS. |
    | Vēlamā maršrutēšanas pakāpe | Atlasiet **Pamata (noklusējums).** |
    | Parakstīšanas atslēga | Ja **nepieciešams,** atlasiet taustiņu **key1 vai key2.** |

4. Atlasiet **ģenerēt SAS un savienojuma** virkni.
5. Kopējiet vērtību no **SAS marķiera** teksta lodziņa teksta redaktorā, piemēram, Notepad.

### <a name="download-deployment-scripts-for-azure-synapse-views"></a>Lejupielādēt izvietošanas skriptus Azure Synapse skatiem
Lai izveidotu un publicētu nepieciešamos Azure Synapse skatus darbvietā, jums jālejupielādē un jāizpilda skriptu kopa. Izpildiet tālāk aprakstītās darbības, lai lejupielādētu skriptus.
1. Dodieties uz [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) GitHub repo. Skripti ir pieejami repo.
2. Lai lejupielādētu skriptus lokālajā datorā, varat šo atkārtošanu vai lejupielādēt repo kā zip failu.

### <a name="install-and-configure-azure-synapse-workspace"></a>Instalēt un konfigurēt Azure Synapse darbalauku
Lai instalētu un konfigurētu Azure Synapse darbvietu, veiciet tālāk aprakstītās darbības.
1. Instalējiet Azure Synapse Darbalauku jūsu Azure abonementā, izpildot Ātrās startēšanas [darbības: Darbalauku izveide.](/azure/synapse-analytics/quickstart-create-workspace)
2. Atveriet failu SetupS notepadapse.sql programmā Notepad no lokālā datora mapes, kur tika uzstādīts vai lejupielādēts Dynamics365Commerce.Solutions repo. Papildinformāciju skatiet [sadaļā Lejupielādes izvietošanas skripti Azure Synapse](#download-deployment-scripts-for-azure-synapse-views) skatiem. Skripta fails atrodas mapē "/Pipeline/CommerceAnalyticsSemanapse/". Rediģējiet skriptu, lai aizstātu viettura tekstu ar vērtībām zemāk.

   | Viettura teksts | Aizstāšanas vērtība |
   |------------------|-------------------|
   | placeholder_storageaccount | Aizstājiet ar nosaukumu glabāšanas kontam, ko izveidojāt, konfigurējot Eksportēšanu uz datu Krājumu... kā aprakstīts abonementa kontā Izveidot **·** datu Noliktavas [(Ģn.2).](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription) |
   | <a name="phContainer"></a> placeholder_container | Aizstājiet ar tā glabāšanas konteinera nosaukumu, kas tika izveidots Jūsu Azure data Azure Data Azure instancē pēc tam, kad instalējāt eksportēšanu uz **Datu Mapi** pievienojumprogramma LCS. Lai saņemtu konteinera nosaukumu, ir jāizmanto Storage Explorer Azure portālā, lai pārlūkotu glabāšanas kontu. |
   | placeholder_sastoken | Aizstāt ar SAS marķieri, kas tika kopēts [datu glabāšanas konta SAS](#generate-storage-account-sas-token) marķierim. Noteikti noņemiet **·** "?" SAS marķiera vērtības sākumā. |
   | <a name="phUserPwd"></a> placeholder_password | Aizstāt ar drošu paroli pēc savas izvēles. Izveidojiet paroles piezīmi. Parole tiks iestatīta kā parole jaunajam kontam 'reportreadonlyuser', kas tiks izveidota ar skriptu. **·** NEIESTATIET 'sqladminuser' konta paroli šeit.  |

3. Dodieties uz jauno Azure Synapse darbalauku Azure portālā. Atlasiet **opciju Atvērt Arapse Studio** pārskata **·** lapā.
4. Kopējiet tā satura `SetupSynapse.sql` informāciju, kuru atjauninājāties iepriekš 2. darbībā. Azure portālā No sieto,izvēlieties Jauns **> SQL** skripts. Ielīmēt saturu SQL skriptu redaktorā, kas atrodas Atsegtā Studio.
5. Pārbaudiet, vai **izmantot datu bāzi ir iestatīta uz** **·** Šablons. Atlasiet **·** Palaist, lai izpildītu skriptu.
6. Uzgaidiet, līdz skripts ir pabeigts. Skripts izveidos datu bāzi commerce analytics, akreditācijas datus, lai piekļūtu Azure datu pardošanas kontam, un tikai lasāmu lietotāja kontu, kas tiks izmantots, lai izveidotu savienojumu ar Power BI Azure Synapse instanci.
7. Lokālajā datorā atveriet PowerShell administratora režīmā. Dodieties uz mapi "/Pipeline/CommerceAnalyticsScaurapse/" mapē, kur tika izcelta vai lejupielādēta Dynamics365Commerce.Solutions repo, kā aprakstīts Lejupielādes izvietošanas skriptos [Azure Synapse](#download-deployment-scripts-for-azure-synapse-views) skatiem.
8. Iestatiet PowerShell izpildes politiku, izpildot šādu komandu PowerShell logā:

   ```powershell
   Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
   ```
   
9. Instalējiet SQL Server PowerShell moduli, izpildot norādīto komandu PowerShell logā:

   ```powershell
   Install-Module sqlserver
   ```
   
   > [!NOTE]
   > Ja SQL servera modulis jau ir instalēts, šo darbību varat izlaist. Šī moduļa instalēšanas laikā, iespējams, tiks piedāvāts instalēt NuGet nodrošinātāju. Lai **turpinātu** nodrošinātāja instalēšanu, nospiediet NuGet Y. Varat arī saņemt ziņojumu, ka instalējat moduļus no ne jau iepriekš ne uzrietās repozitorija. Nospiediet **·** Y, lai turpinātu instalēšanu. Pēc izvēles jūs varat darbināt cmdlet, lai `Set-PSRepository` uzticētos repozitorijam. `PSGallery`
   
10. PowerShell Azure Synapse logā publicējiet skatus, izpildot šādu komandu:

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```
    
    Aizstāt viettura vērtības komandā šādi:
    
    | Viettura vērtība | Aizstāšanas vērtība |
    |-------------------|-------------------|
    | SERVER_NAME | Aizstāt ar bezservera Azure Synapse SQL galapunkta nosaukumu. Šo vērtību varat iegūt no Azure Synapse darbvietas pārskata **lapas Azure** portālā. |
    | PAROLI | Aizstāt ar SQLAdminuser paroli. |
    | STORAGE_ACCOUNT | Aizstāt ar Azure Data Pārsūtīšana glabāšanas konta nosaukumu. |
    | CONTAINER_NAME | Aizstājiet ar tā konteinera nosaukumu, ko izveidojis eksporta **uz datuMM.** Nosaukums ir tam pašam konteineram, kuru norādījāt vērtību [placeholder_container](#install-and-configure-azure-synapse-workspace) vērtībai. |
    | DATA_ROOT_PATH | Aizstāt ar mapes nosaukumu konteinerā, kurā ir visi dati. |

    > [!NOTE]
    > Izmantojot Azure glabāšanas pārlūkprogrammu un azure datu glabāšanas kontu, varat atrast glabāšanas konta nosaukumu, konteinera nosaukumu un datu saknes ceļu no Azure portāla.

11. Uzgaidiet, līdz skripts ir pabeigts. Skripts izveidos SQL skatus Azure Synapse bezservera SQL instancē.

### <a name="install-power-bi-template-app"></a>Veidnes Power BI programmas instalēšana
Lai instalētu Power BI Commerce Analytics veidnes programmu, veiciet tālāk aprakstītās darbības.
1. Pieteikties [Power BI portālā,](https://powerbi.microsoft.com/) izmantojot jūsu organizācijas ID.
2. Instalējiet Commerce Analytics Power BI veidnes programmu, ejot [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) uz. Varat saņemt brīdinājumu par to, ka programma nav AppSource uzskaitīta. Atlasiet **Instalēt**.
3. Ja šī ir pirmā reize, kad instalējat programmu, pārejiet pie 5. soļa. Ja šī programma jau ir instalēta, jums tiks sniegtas tālāk norādītās opcijas, lai atjauninātu programmu.
   1. Atjauniniet darbvietu un programmu: šī opcija atjaunina esošo veidnes programmu un pārraksta programmas iestatījumus, piemēram, programmas instances nosaukumu un atļauju konfigurācijas.
   2. Atjauniniet darbvietas saturu, neatjauninot programmu: šī opcija atjaunina esošo veidnes programmu un saglabā programmas iestatījumus. Šī ir **programmas** atjaunināšanas ieteicamā opcija.
   3. Instalējiet citu programmas kopiju jaunā darbvietā: šī opcija izveido jaunu programmas kopiju jaunā darbalaukā, kas tiks jums izveidots. Esošā darbvieta netiek neskarta.      
4. Atlasiet vienu no iepriekšminētajām opcijām un pēc tam atlasiet **·** Instalēt.
5. Atveriet instalēto programmu, kreisajā **·** rūtī atlasot izvēlnes vienumu Programmas un pēc tam atlasot programmu.
6. Savienojiet programmu ar datu avotu, atlasot **·** Pievienot. Ja šī nav pirmā programmas instalēšana, atlasiet Pievienot **datus** dzeltenajā informācijas joslā.
7. Ievadiet šādas parametru vērtības:

   | Parametra nosaukums | Vērtība |
   |----------------|-------|
   | Serveris       | Ievadiet tā bezservera Azure Synapse SQL galapunkta nosaukumu, ko izveidojāt sadaļā [Darbvietas instalēšana Azure Synapse un](#install-and-configure-azure-synapse-workspace) konfigurēšana. Šo vērtību varat atrast Azure Azure Synapse portāla **·** darbvietas pārskata lapā. |
   | Datu bāze | Ievadiet vērtību "CommerceAnalytics".
   | Valoda | Atlasiet vērtību no nolaižamā saraksta. Šis iestatījums tiek izmantots lokalizētiem preču un kategoriju nosaukumiem. Vērtība ir reģistrjutīga. |
   | Datumu diapazons | Atlasiet vērtību no nolaižamā saraksta. Dati par atlasītajiem mēnešiem tiks importēti Power BI uz datu kopu. Datu kopas lielums un sinhronizēšanai nepieciešamais laiks ir atkarīgs no atlasītās vērtības. |

8. Atlasiet **Nākamais**. Jums tiks piedāvāts ievadīt akreditācijas datus savienojumam ar Azure Synapse SQL datu bāzi. Ievadiet šādas vērtības:

   | Parametra nosaukums | Vērtība |
   |----------------|-------|
   |Autentifikācijas metode|Atlasiet **·** Pamata.|
   |Lietotājvārds| Ievadiet "reportreadonlyuser".|
   |Parole|Ievadiet vērtību, kuru izmantojāt, lai placeholder_password un vērtību skriptā [...](#install-and-configure-azure-synapse-workspace) SetupSfiskapse.sql. Šī ir reportreadonlyuser konta parole.| 

9. Atlasiet **pieteiksies un izveidojiet** savienojumu.
10. Uzgaidiet, līdz datu kopa tiek atsvaidzināta. Pēc tam dodieties uz programmas darbvietu, **atlasot ikonu** Rediģēt programmu. Varat pārbaudīt darbvietas datu kopas atsvaidzināšanas statusu. Varat arī iestatīt automātiskās atsvaidzināšanas grafikus datu kopai, pārvaldīt atļaujas un pārdēvēt programmas instanci.

### <a name="privacy"></a>Konfidencialitāte
Mums ir svarīga jūsu konfidencialitāte. Lai uzzinātu vairāk par konfidencialitāti, izlasiet mūsu [paziņojumu par](https://go.microsoft.com/fwlink/?LinkId=521839) konfidencialitāti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
