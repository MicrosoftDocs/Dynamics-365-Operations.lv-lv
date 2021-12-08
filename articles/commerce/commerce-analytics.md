---
title: Commerce Analytics (priekšskatījums)
description: Šajā tēmā skaidrots, kā instalēt un izmantot analīzes iespējas sadaļā Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862777"
---
# <a name="commerce-analytics-preview"></a>Commerce Analytics (priekšskatījums)

[!include [banner](includes/banner.md)]

Šajā tēmā skaidrots, kā instalēt Commerce Analytics (priekšskatījums), funkcionālo analīzes spēju, kas ir iekļauta Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>Commerce Analytics (priekšskatījums) tiešais demonstrācija

Varat mēģināt kādu live [demonstrāciju pakalpojumā Commerce Analytics (preview)](https://aka.ms/CommerceAnalyticsDemo).

![Commerce Analytics (Preview) Kopsavilkums](media/CommerceAnalytics_Summary.png)
![Commerce Analytics (priekšskatījums) Maksājumi](media/CommerceAnalytics_Payments.png)
![Commerce Analytics (priekšskatījums) web aktivitāte](media/CommerceAnalytics_WebActivity.png)


## <a name="commerce-analytics-preview-system-architecture"></a>Commerce Analytics (Preview) sistēmas arhitektūra

### <a name="key-components"></a>Galvenie komponenti

Commerce Analytics (Preview) sastāv no šādiem galvenajiem komponentiem:

- Lietošanai gatavie interaktīvie Power BI pārskati
- SQL skati Azure Synapse analīzes pakalpojumā
- Elementa un ontoloģijas dati Azure datu līdzās
- Neapstrādātie dati Uzr.

![Commerce Analytics sistēmas arhitektūras galvenie komponenti](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Datu plūsmas

#### <a name="step-1-data-generation"></a>1. darbība: datu ģenerēšana

Dati rodas kā darbību dati vai uzvedības dati no viena no šiem avotiem:

- Zvanu centra piesaiste izmanto Commerce HQ klientu, lai apstrādātu pārdošanas pasūtījumus.
- Kasieris pārdošanas punktā (POS) apstrādā pārdošanas darbības.
- Pārdošana tiek veidota pielāgotās programmās, izmantojot bezatgriezīgu commerce (Commerce Scale Unit).
- E-komercijas veikalā tiek pārlūkota jūsu e-komercijas vietne.
- E-komercijas veikalā jūsu e-komercijas vietnē tiek pasūtīts pasūtījums.
- Datus sagatavo citas sistēmas, Dynamics 365 Connected Spaces piemēram, .

#### <a name="step-2-ingestion-and-pre-processing"></a>2. solis. Iesācīšana un pirmapstrāde

Transakciju dati tiek iet uz Commerce HQ tieši (pasūtījumu gadījumā, kas tiek notverti tieši Commerce HQ klientā) vai caur Commerce Scale Unit (ja pasūtījumi ir notverti POS, e-komercijas ietvaros vai pielāgotos klientos, kas izmanto bezgalīgo tirdzniecību).

Pēc tam funkcija Eksportēt uz datu Konta tiek izmantota, lai kopētu darbības datus uz jūsu datiem kā neapstrādātus datus. Neapstrādātie dati saglabāts mapē Tabulas.

E-komercijas tīmekļa aktivitātes dati tiek sūtīti tieši uz datu darbību. Datus, ko sagatavo citas sistēmas, Dynamics 365 Connected Spaces piemēram, tos, nosūta tieši uz šo sistēmu datiem.

#### <a name="step-3-transformation-and-aggregation"></a>3. darbība: pārvēršana un apkopošana

Kad neapstrādātie dati ir jūsu datu struktūrā, Commerce Analytics pakalpojums to nolasa, pārveido, uzkopē un ieraksta atpakaļ datu ierakstītājā loģisko entītiju formā (entītiju mapē) un uzkrātos rādītājus (ontoloģijas mapē).

#### <a name="step-4-querying"></a>4. darbība: vaicājums

Azure Synapse Analītisko analīzi izmanto, lai vaicātu par datiem datu veidā, izmantojot Transact-SQL (T-SQL) interfeisu. Šis interfeiss ietver SQL skatus. SQL skati iespējo datu ārējas vaicāšanas datu pakalpojumā, vai nu tieši, izmantojot T-SQL klientu (ekspromtanai) vai vizualizēšanas Power BI rīku, piemēram.

#### <a name="step-5-modeling-and-serving"></a>5. solis. Modelēšana un apkalpošana

Dati, uz kuriem attiecas Azure Synapse Analīzes Power BI vaicājums, ir uz semantisko modeli. Atkarībā no datu tipa tie ir periodiski importēti atmiņā vai tieši vaicājumā Power BI izpildlaikā.

Visbeidzot dati tiek atveidoti Power BI vizuāli, lai lietotāji varētu tos apskatīt un mijiedarboties.

## <a name="commerce-analytics-preview-functional-overview"></a>Commerce Analytics (Preview) funkcionālā apskats

### <a name="summary"></a>Kopsavilkums

Commerce Analytics veidnes programmā ir ietvertas šādas galvenās pārskatu lapas:

1. [Augstākā līmeņa filtri](#TopLevelFilters)
2. [Produkti](#ProductsPage)
3. [Debitori](#CustomersPage)
4. [Kanāli](#ChannelsPage)
5. [Pārdošana](#SalesPage)
6. [Robežas](#MarginsPage)
7. [Atgriešanas darbības](#ReturnsPage)
8. [Atlaides](#DiscountsPage)
9. [Maksājumi](#PaymentsPage)
10. [Debitori](#CustomersPage)
11. [Salīdzinājums](#ComparisonPage)
12. [Aktivitāte tīmeklī](#WebActivityPage)
13. [Web aktivitāte — augstākā līmeņa filtrs](#WebActivityTopLevelFilters)

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Augstākā līmeņa filtri

- Datuma iestatījumi

    - Gads
    - Ceturksnis
    - mēnesis;
    - Nedēļa
    - diena;

- Kanāla iestatījumi

    - Juridiska persona
    - Kanāla veids
    - Debitora veids
    - Pārdošanas tips
    - Kanāls
    - Organizācijas hierarhija

- Preces iestatījumi

    - Kategoriju hierarhija
    - Kategorija

####  <a name="products"></a><a name="ProductsPage"></a> Produktiem

- Pārdošana
- Peļņa
- Atgriešanas darbības

####  <a name="customers"></a><a name="CustomersPage"></a> Klientiem

- Pārdošana
- Peļņa
- Atgriešanas darbības

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanālus

- Pārdošana
- Peļņa
- Atgriešanas darbības

### <a name="sales"></a>Pārdošanas<a name="SalesPage"></a>

- Pēc piegādes vietas
- Pēc kanāla/veikala/termināļa
- Pa darbiniekiem
- Pēc datuma
- Pa stundām
- Pēc preču kategorijas

### <a name="margins"></a><a name="MarginsPage"></a> Piemales

- Pēc piegādes vietas
- Blakusprodukts
- Pēc datuma

### <a name="returns"></a><a name="ReturnsPage"></a> Atgriež

- Atgriešana pēc summas

    - Pēc veikala
    - Blakusprodukts
    - Pēc datuma

- Atgriešana pēc darbības

    - Pēc veikala
    - Blakusprodukts
    - Pēc datuma

### <a name="discounts"></a><a name="DiscountsPage"></a> Atlaides

- Pēc veikala
- Blakusprodukts
- Pēc datuma
- Dekompozīcija

    - Juridiska persona
    - Veikals
    - Atlaides veids
    - Atlaides nosaukums
    - Prece

### <a name="payments"></a><a name="PaymentsPage"></a> Maksājumus

- Pēc kanāla/termināļa
- Pēc maksāšanas metodes/tipa
- Pēc datuma
- Dekompozīcija

    - Juridiska persona
    - Kanāla veids
    - Veikals
    - Terminālis
    - Maksāšanas veids

### <a name="customers"></a><a name="CustomersPage"></a> Klientiem

- Darbmūžs vērtība (LTV)

    LTV tiek aprēķināts, ņemot vērā kopējo summu, kādu debitors tērē visos Dynamics 365 Commerce pārdošanas kanālos (tostarp POS, e-komercija un zvanu centrā).

- Recency

    Recency tiek aprēķināts, ņemot vērā dienu skaitu, kopš debitora pēdējās darbību saistības ar organizāciju. Pašlaik recency neaplūko ar transakcijām nesaistīšanos signālus, piemēram, e-komercijas pārlūkošanas aktivitāti.

- Biežums

    Biežums tiek aprēķināts, ņemot vērā debitora darbību saistībām ar organizāciju. Šobrīd biežums neietver darījumu piesaistes signālus, piemēram, e-komercijas pārlūkošanas aktivitāti.

- Attiecību garums

    Attiecību garums tiek aprēķināts, ņemot vērā dienu skaitu, kopš sistēmā tika izveidots debitora ieraksts.

- Transakciju skaits

### <a name="comparison"></a><a name="ComparisonPage"></a> Salīdzinājums

- Preču salīdzinājums pēc laika perioda

    - Pārdošanas un pārdošanas starpība
    - Uzcenojuma un uzcenojuma starpība

- Debitors pēc laika perioda

    - Pārdošanas un pārdošanas starpība
    - Uzcenojuma un uzcenojuma starpība

### <a name="web-activity"></a><a name="WebActivityPage"></a> Tīmekļa aktivitāte

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Augstākā līmeņa filtri

- Datumu diapazons
- Kanāla veids
- Kanāls
- Kategoriju hierarhija

#### <a name="acquisitions"></a>Iegādes

- Lapas skati

    - Pēc valsts vai reģiona
    - Blakusprodukts
    - Kad lietotājs ir pierakstījies statusā
    - Pēc datuma

- E-komercijas pasūtījumi
- Konvertēšanas maiņas kurss

    - Pēc datuma

- Konversijasnels

    - Lapas skats pēc lapas tipa (mājas lapa, kategorijas lapa vai lapa ar detalizētu informāciju par preci)
    - Pievienot grozam
    - Norēķināšanās
    - Pirkšana

#### <a name="sessions"></a>Sesijas

Sesija ir lietotāja apmeklējums jūsu e-komercijas vietnē. Sesija tiek uzskatīta par pabeigtu pēc 30 neaktivitātes minūtēm vai 24 aktīvas lietošanas stundām.

- Pēc valsts vai reģiona
- Pēc izcelsmes (ārējs atsauces lietotājs)
- Kad lietotājs ir pierakstījies statusā
- Sesiju skaits

    - Pēc datuma
    - Pēc ierakstu lapas

- Pasūtījums pa sesijām

    - Pēc datuma

- Sesijas sesija sesija

    Sesijas sesija ir sesija, kurā lietotājs pamet tūlīt pēc jūsu e-komercijas vietnes apmeklējuma. Papildinformāciju skatiet Sadaļā [Vaidu likme](https://en.wikipedia.org/wiki/Bounce_rate).

- Klikšķi pa sesijām

#### <a name="visitors"></a>Apmeklētāji

Anonīms konta numurs jūsu e-komercijas vietnē ir unikāli identificēts, balstoties uz noteiktu pārlūkprogrammu un specifisku ierīci, ko lieto lietotājs. Commerce Analytics neizseko anonīmos darījumos dažādās pārlūkprogrammās vai ierīcēs. Anonīms lietotājs, kurš izmanto to pašu pārlūkprogrammu vienā un tajā pašā ierīcē, ir unikāli identificēts vairākās lietotāja sesijās, līdz pārlūkprogrammas kešatmiņā saglabātie dati ir notīrīti vai arī periods (parasti 12 mēneši) tiek nokārtots atkarībā no tā, kas notiek vispirms.

Ja jūsu e-komercijas vietne tiek pārlūkota, kamēr tā ir reģistrēta, Commerce Analytics var sniegt papildinformāciju par to. Šī informācija ir balstīta uz esošajām attiecībām, kas jūsu organizācijai ir ar aizturēto informāciju, ko rada to iepriekšējie pirkumi visos pārdošanas kanālos Dynamics 365 Commerce (tostarp POS, e-komercija un zvanu centrs). Papildu informācija ietver recency, attiecību garumu, darbmūžu vērtību un biežuma datus.

- Seguma summa
- Vidējā pasūtījumu vērtība
- Vidējā pārdošanas vērtība
- E-komercijas skaits

    - Pēc datuma
    - Pēc novietojuma

        Commerce Analytics sniedz tikai valsts/reģiona līmeņa granularitātei vietas ieskatījumā e-komercijai.

    - Pēc recency

        Recency tiek aprēķināts, ņemot vērā dienu skaitu, kopš debitora pēdējās darbību saistības ar organizāciju. Pašlaik recency neaplūko ar transakcijām nesaistīšanos signālus, piemēram, e-komercijas pārlūkošanas aktivitāti.

    - Pēc attiecību garuma

        Attiecību garums tiek aprēķināts, ņemot vērā dienu skaitu, kopš sistēmā tika izveidots debitora ieraksts.

    - Pēc darbmūžs vērtības (LTV)

        LTV tiek aprēķināts, ņemot vērā kopējo summu, kādu debitors tērē visos Dynamics 365 Commerce pārdošanas kanālos (tostarp POS, e-komercija un zvanu centrā).

    - Pēc biežuma

        Biežums tiek aprēķināts, ņemot vērā debitora darbību saistībām ar organizāciju. Šobrīd biežums neietver darījumu piesaistes signālus, piemēram, e-komercijas pārlūkošanas aktivitāti.

#### <a name="impressions"></a>Iespaidi

Iespaids ir atsevišķs e-komercijas uzņēmuma skatījums par preci, kas ir vizuāla. Piemēram, e-komercijas apskats tiek atvērts uz jūsu e-komercijas vietnes sākumlapu un skatiem kādu no lietojumprogrammas lietojumprogrammu lapām **augšējā pārdošanas** saraksta modulī. Skatījums šeit skata to pašu mat preci **saraksta modulī** Izdotais. Šajā gadījumā ir divi preces iespaidi. 

Pašlaik iespaidi tiek izsekoti šādās virsmas:

- Saraksti (piemēram, **Ieteicamais**, **Augšējais** pārdošanas, **Izdošanas jums un** **Tendences**)
- Groza modulis
- Meklēšanas rezultāta konteiners
- Kategorijas meklēšanas rezultāta konteiners

Pašlaik preces, kas ir atveidotas karuseļa modulī vai pielāgotā vizuālajās attiecībās, nav skaitītas ar attēlu saistītajos metrikās.

Pārskatā **par pārskatu par pārskatu ir iekļauti šādi** rādītāji:

- Iespaida skaits

    - Pēc lapas tipa un moduļa

        Lapas tips ir vispārīgs lapas tips, kas tiek definēts katrai lapai jūsu e-komercijas vietnē. Moduļa tips ir e-commerce vizuālā moduļa tips, kurā tiek rādīta prece.

        Lai skatītu iespaidus pēc moduļa, iespējams, būs detalizēti jāskata lapas un moduļa vizualizēs.

    - Blakusprodukts
    - Kad lietotājs ir pierakstījies statusā
    - Pēc datuma

- Iespaida klikšķa skaits

    Noklikšķiniet uz iespaida, kas notiek, kad e-komercijas laikā tiek atlasīts preces vizuāls vienums. Parasti precei pēc tam tiek paņemta preču informācijas lapa.

- Iespaids par klikšķināšanas koeficientu (KTR)

    CTR tiek aprēķināts, kā kopējais skatījumu skaits, kas tiek dalīts ar skatījumu kopējo skaitu.

## <a name="commerce-analytics-preview-installation"></a>Commerce Analytics (Preview) instalēšana

> [!NOTE]
> Commerce Analytics (Preview) ir priekšskatījumā Amerikas Savienotajās Valstīs, Kanādā, Apvienotajā Karalistē, Eiropā, Dienvidāzijā, Austrumāzijā, Austrālijā un Japānas reģionos. Ja vide atrodas jebkurā no šiem reģioniem, šo funkciju var iespējot jūsu Finance and Operations vidē, izmantojot pakalpojumu Microsoft Dynamics Lifecycle Services (LCS). Pirms šo funkciju varat izmantot, skatiet [sadaļu Eksporta konfigurēšana uz Azure data](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) Nosūtīšana.

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a> Iespējot un konfigurēt Commerce Analytics (Priekšskatījums)

Lai instalētu Commerce Analytics (priekšskatījumu), jums ir nepieciešamas atļaujas izveidot resursus Azure abonementā. Jums ir arī jābūt atļaujām instalēt pievienojumprogrammas LCS. Šeit sniegts darbību apskats:

1. [Iesniedziet Commerce Analytics (Preview) formu Preview.](#joinPreview)
2. [Iespējojiet un konfigurējiet eksportēšanu uz datu](#enableExportToDataLake) failu...
3. [Iespējojiet un konfigurējiet Commerce Analytics (Preview)](#enableCommerceAnalyticsAddin) pievienojumprogrammu.
4. [Ģenerējiet koplietoto piekļuves parakstu (SAS) marķieri jūsu glabāšanas](#getSASToken) kontam.
5. [Lejupielādējiet izvietošanas skriptus Azure Synapse](#downloadSynapseDeploymentScripts) skatiem.
6. [Instalējiet un konfigurējiet Azure Synapse](#configureAzureSynapse) darbvietu.
7. [Instalējiet veidnes Power BI](#powerbi) programmu.

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a> Iesniegt Priekšskatījuma veidlapas Commerce Analytics (Priekšskatījums)

Iesniedziet [Commerce Analytics (Preview) formu Preview.](https://forms.office.com/r/vW5VLJGXZ2) Līdz trīs darba dienām laika posmu, kad forma tiks apstrādāta. Pēc apstrādes uz e-pasta adresi, ko nosūtījāt formā, tiks nosūtīts apstiprinājuma e-pasta ziņojums.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a> Iespējot un konfigurēt eksportu uz datu failu

Commerce Analytics (Priekšskatījums) balstās uz iespēju Eksportēt uz datuKursi, lai eksportētu Commerce HQ datus uz Datu Diena un paturētu šos datus jaunu. Pirms Commerce Analytics (priekšskatījums) konfigurēšanas iespējojiet un konfigurējiet eksportēšanu uz datu [plkst](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Konfigurējot eksportēšanu uz datu To ir, atzīmējiet tālāk norādīto informāciju, jo tas būs jāievada vēlāk:

- <a name="keyVault"></a> Atslēgas Kases sistēmas Domēna nosaukumu (DNS) nosaukums un slepenie vārdi, kuros glabā lietojumprogrammas ID un programmas noslēpumu. Papildinformāciju skatiet sadaļā [Noslēpumu pievienošana](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets) atslēgai.
- <a name="storageAccount"></a> Datu Pārsūtīšanas konta nosaukums datu Līdzinstancim. Papildinformāciju skatiet [abonementā izveidojiet datu Lei Storage (Gen2) kontu](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a> Iespējot un konfigurēt Commerce Analytics (Preview) pievienojumprogrammu

Lai instalētu Commerce Analytics (Preview) pievienojumprogrammu LCS, jums ir jābūt vides administratoram LCS vidē, ko plānojat izmantot.

Lai instalētu un konfigurētu Commerce Analytics (Preview) pievienojumprogrammu, veiciet šos soļus.

1. Pieteikties [LCS](https://lcs.dynamics.com/) un doties uz vidi.
2. Vides lapas cilnē **Vides** **pievienojumprogrammas** atlasiet Instalēt **jaunu** pievienojumprogrammu.
3. Dialoglodziņā atlasiet Commerce **Analytics (Priekšskatījums).**

    Ja **Commerce Analytics (Preview)** nav uzskaitīts, pārliecinieties, ka esat pievienojis Insider Programmu.

4. Dialoglodziņā **Iestatīšanas** pievienojumprogramma ievadiet šādu informāciju.

    | Informācija | Modulis | Vērtības piemērs |
    |---|---|---|
    | Azure AD Nomnieka ID jūsu videi | Pieteikties Azure [portālā](https://portal.azure.com/) un atvērt **Azure Active Directory** pakalpojumu. Pēc tam atveriet **rekvizītu** lapu un kopējiet vērtību **laukā Direktorija** ID. | 72f988, kas-0000-0000-00000-2d7cd011db47 |
    | Jūsu atslēgas DNS nosaukums | Ievadiet [jūsu](#keyVault) atslēgas, piemēram, DNS nosaukumu. Iepriekšējā sadaļā esat veicis šīs vērtības piezīmi. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Noslēpums, kas satur pieteikuma ID | Ievadiet [slepeno vārdu, kurā tiek glabāts programmas](#keyVault) ID. Iepriekšējā sadaļā esat veicis šīs vērtības piezīmi. | app-id |
    | Noslēpums, kas satur pieteikuma noslēpumu | Ievadiet [slepeno vārdu, kas glabā pieteikuma](#keyVault) noslēpumu. Iepriekšējā sadaļā esat veicis šīs vērtības piezīmi. | app-secret |

5. Akceptējiet piedāvājuma noteikumus, atzīmējot šo izvēles rūtiņu, un pēc tam atlasiet **Instalēt**.

    Sistēma instalē un konfigurē Commerce Analytics (Preview) pievienojumprogrammu videi. Šis process var ilgt dažas minūtes. Kad komercijas analīze (priekšskatījums) ir jāuzskaita vides lapā un statusam **ir** jābūt **·** **Instalēts**.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a> Ģenerēt SAS marķieri jūsu glabāšanas kontam

SAS marķieris ļauj ārējām entītijām piekļūt jūsu glabāšanas kontam un izmantot noteiktu privilēģiju kopu noteiktam laika daudzumam. Azure Synapse izmantos SAS pilnvara, lai piekļūtu pamatdatiem Datu Programmā.

> [!NOTE]
> Zināmā Commerce Analytics (Preview) ierobežojuma dēļ instance zaudēs piekļuvi datiem, kad Azure Synapse SAS marķieris beidzas. Tāpēc, ģenerējot SAS marķieri, ir jāiestata maksimālais beigu datums, ko atļauj jūsu organizācijas drošības politika.

Lai ģenerētu SAS marķieri, sekojiet šiem soļiem.

1. Azure portālā dodieties uz glabāšanas kontu, [ko](#storageAccount) izveidojāt, konfigurējot eksportēt uz datu failu.
2. Kreisās puses rūtī zem glabāšanas konta atlasiet **Koplietotās piekļuves** paraksts.
3. **SAS opciju** lapā iestatiet sekojošos laukus.

    | Lauks | Vērtība |
    |---|---|
    | Atļautie pakalpojumi | Atlasiet **BLOB**. |
    | Atļautie resursu tipi | Pakalpojuma, **konteinera** un **objekta** **atlase**. |
    | Atļautās atļaujas | Atlasiet **Lasīt**, **Rakstīt**, **·** **Dzēst**, **Saraksts**, Pievienot un **Izveidot**. |
    | BLOB versijas atļaujas | Atlasiet **Iespējo versiju** dzēšanu. |
    | Sākuma un beigu datums/laiks | Iestatīt SAS marķiera sākuma un beigu datumu un laiku pēc vajadzības. |
    | Atļautās IP adreses | Atstājiet šo lauku tukšu. |
    | Atļautie protokols | Atlasiet **tikai** HTTPS. |
    | Vēlamā maršrutēšanas pakāpe | Atlasiet **Pamata (noklusējums).** |
    | Parakstīšanas atslēga | Ja **nepieciešams**, atlasiet **taustiņu 1 vai** taustiņu2. |

4. Atlasiet **ģenerēt SAS un savienojuma** virkni.
5. Kopējiet vērtību **SAS marķiera** laukā un ielīmējiet to teksta redaktorā, piemēram, Notepad.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a> Lejupielādēt skatu izvietošanas Azure Synapse skriptus

Lai izveidotu un publicētu pieprasītos Azure Synapse skatus darbvietā, jāpalaiž skriptu kopa. Izpildiet šīs darbības, lai lejupielādētu skriptus.

1. GitHub dodieties uz [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) repozitoriju (repo).
2. Lejupielādējiet skriptus lokālajā datorā, nometot repo vai lejupielādējot to kā zip failu.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a> Darbvietas instalēšana un Azure Synapse konfigurācija

Lai instalētu un konfigurētu Azure Synapse darbvietu, veiciet šādas darbības.

1. Instalējiet Azure Synapse darbvietu savā Azure abonementā. Papildinformāciju skatiet Sadaļā [Ātrā startēšana: Darbalauku izveidošana par Darbalauku](/azure/synapse-analytics/quickstart-create-workspace).
2. Programmā Notepad vai citā teksta redaktorā atveriet SetupScaurapse.sql skripta failu no mapes lokālajā datorā, kuru esat lejupielādējis vai lejupielādējis **Dynamics365Commerce**.Solutions repo iepriekšējā sadaļā. Skripta fails atrodas mapē /Pipeline/CommerceAnalyticsShuapse/. Skriptā aizstājiet viettura tekstu ar vērtībām, kā parādīts šajā tabulā.

    | Viettura teksts | Aizstāšanas vērtība |
    |---|---|
    | placeholder_storageaccount | Tā glabāšanas konta [nosaukums, kuru](#storageAccount) izveidojāt, konfigurējot eksportēšanu uz datu noliktavu. |
    | <a name="phContainer"></a> placeholder_container | Tā glabāšanas konteinera nosaukums, kas tika izveidots datu Pārsūtīšanas instancē pēc tam, kad veiksmīgi instalējāt eksportēšanu uz datu Mapi ar pievienojumprogrammu LCS. Lai saņemtu konteinera nosaukumu, azure portālā ir jāizmanto storage Explorer, lai pārlūkotu glabāšanas kontu. |
    | placeholder_sastoken | Jūsu [ģenerētais SAS](#getSASToken) marķieris Noteikti noņemiet jautājuma **zīmi** (?) no SAS marķiera vērtības sākuma. |
    | <a name="phUserPwd"></a> placeholder_password | Stipra parole pēc savas izvēles. Atzīmējiet šo paroli. Tas tiks iestatīts kā parole jaunajam **reportreadonlyuser** kontam, ko izveido skripts. **Neiestatiet** **SQLAdminuser konta** paroli. |

3. Kopējiet skripta faila atjaunināto saturu.
4. Azure portālā dodieties uz jauno Azure Synapse darbalauku. Pārskata **lapā** atlasiet Atvērt **Nekartes** studiju.
5. Objektā No Srakses Studio atlasiet Jauns SQL skripts un ielīmējiet skripta **\> faila saturu SQL** skripta redaktorā.
6. Pārliecinieties, vai lauks **Izmantot datu bāzes ir** iestatīts kā **šablons**.
7. Atlasiet **Palaist** un gaidiet, kamēr skripts tiks pabeigts. Veiksmīga skripta izpilde izveidos Commerce Analytics datu bāzi, akreditācijas datus, lai piekļūtu datu failā, un tikai lasāmu lietotāja kontu, kas tiks izmantots savienojumam Power BI ar Azure Synapse instanci.
8. Lokālajā datorā atveriet Windows PowerShell administratora režīmā un dodieties uz mapi /Pipeline/CommerceAnalyticsS pirkšanasapse/mapē, kurā jūs esat to lejupielādējis vai esiet lejupielādējis Dynamics365Commerce.Solutions repo.
9. Iestatiet Windows PowerShell izpildes politiku, palaižot tālāk norādīto komandu.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Ja SQL Server PowerShell modulis vēl nav instalēts, instalējiet to, izpildot tālāk norādīto komandu.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Šī moduļa instalēšanas laikā, iespējams, tiks piedāvāts instalēt NuGet nodrošinātāju. Šajā gadījumā atlasiet **Y, lai** instalētu NuGet nodrošinātāju. Iespējams, tiksiet aicināts apstiprināt, ka moduļi tiek atkārtoti instalēti no ne jau pārinstalēta repozitorija. Šajā gadījumā atlasiet **Y,** lai turpinātu instalēšanu. Pēc izvēles varat darbināt **Set-PSRepository** cmdlet, lai uzticētos **PS Repository** repozitorijam.

11. Publicējiet Azure Synapse skatījumus, palaižot šādu komandu.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Izpildot šo komandu, aizstājiet viettura vērtības kā parādīts šajā tabulā.

    | Viettura vērtība | Aizstāšanas vērtība |
    |---|---|
    | SERVER_NAME | Bezservera Azure Synapse SQL galapunkta nosaukums. Šo vērtību varat iegūt no **Darbvietas** Pārskata lapas Azure Synapse Azure portālā. |
    | PAROLI | **SQLAdminuser konta** parole. |
    | STORAGE_ACCOUNT | Datu Pārsūtīšanas konta nosaukums. |
    | CONTAINER_NAME | Tā konteinera nosaukums, ko izveidoja funkcija Eksportēt uz datu Tajām. Šis konteiners ir tas pats konteiners, ko [norādījāt kā placeholder_container vērtība](#phContainer) 2. darbībā. |
    | DATA_ROOT_PATH | Mapes nosaukums konteinerā, kurā ir visi dati. |

    > [!NOTE]
    > Varat atrast glabāšanas konta nosaukumu, konteinera nosaukumu un datu saknes ceļu, azure portālā izmantojot Azure glabāšanas pārlūkprogrammu un savu datu krātuves kontu.

12. Uzgaidiet, kamēr skripts tiks pabeigts. Veiksmīga skripta izpilde izveidos SQL skatus Azure Synapse Bezservera SQL instancē.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a> Instalējiet Power BI veidnes programmu

Lai instalētu Power BI Commerce Analytics veidnes programmu (Priekšskatījums), izpildiet šīs darbības.

1. Piesakieties [Power BI](https://powerbi.microsoft.com/) portālā, izmantojot organizācijas ID.
2. Instalējiet Commerce Analytics (Preview) Power BI veidnes programmu, ejot uz [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Varat saņemt brīdinājumu, ka programma nav uzskaitīta AppSource. Atlasiet **Instalēt**.
3. Ja programmu atkārtoti instalējot pirmo reizi, pārejiet pie 5. soļa. Ja iepriekš instalējāt šo programmu, tiek rādītas tālāk norādītās programmas atjaunināšanas opcijas.

    - **Atjauniniet darbvietu un programmu — atjauniniet esošo veidnes programmu un pārrakstiet esošos programmas** iestatījumus, piemēram, programmas instances nosaukumu un atļauju konfigurācijas.
    - **Atjaunināt tikai darbvietas saturu,** neatjauninot programmu — atjaunināt esošo veidnes programmu, bet paturēt esošos programmas iestatījumus. *Šī opcija ir ieteicamā programmu atjaunināšanas opcija.*
    - **Instalējiet citu programmas kopiju jaunā darbvietā — izveidojiet jaunu darbalauku un pēc tam izveidojiet tajā** esošās veidnes programmas kopiju. Esošā darbvieta netiks neskarta.

4. Atlasiet vienu no atjaunināšanas opcijām un pēc tam atlasiet **Instalēt**.
5. Atveriet instalēto programmu, kreisajā **rūtī** atlasot Programmas un pēc tam atlasot programmu.
6. Savienojiet programmu ar datu avotu, atlasot **Pievienot**. Ja programmu instalējāt iepriekš, dzelteno ziņojumu joslā atlasiet datu **saiti** Savienot ar datiem.
7. Iestatiet tālāk minētos laukus.

    | Lauks | Vērtība |
    |---|---|
    | Serveris | Ievadiet iepriekšējā sadaļā Azure Synapse izveidotā Bezservera SQL galapunkta nosaukumu. Šo vērtību varat iegūt no **Darbvietas** Pārskata lapas Azure Synapse Azure portālā. |
    | Datu bāze | Ievadiet **CommerceAnalytics.** |
    | Valoda | Atlasiet sarakstā vērtību. Šis lauks tiek izmantots lokalizētiem preču un kategoriju nosaukumiem. Vērtība ir reģistrjutīga. |
    | Datumu diapazons | Atlasiet sarakstā vērtību. Dati par atlasītajiem mēnešiem tiks importēti Power BI datu kopā. Atlasītā vērtība ietekmē datu kopas lielumu un sinhronizācijai nepieciešamo laiku. |

8. Atlasiet **Nākamais**. Tiek piedāvāts ievadīt akreditācijas datus, lai varētu izveidot savienojumu ar Azure Synapse SQL datu bāzi. Iestatiet laukus tā, kā parādīts šajā tabulā.

    | Lauks | Vērtība |
    |---|---|
    | Autentifikācijas metode | Atlasiet **Pamata**. |
    | Lietotājvārds | Ievadiet **reportreadonlyuser.** |
    | Parole | Ievadiet vērtību, kuru aizstājāt [placeholder_password](#phUserPwd) vietturim skriptā SetupSfiskapse.sql. Šī ir **reportreadonlyuser konta** parole. |

9. Atlasiet **pieteiksies un izveidojiet** savienojumu.
10. Uzgaidiet, līdz datu kopa tiks sekmīgi atjaunināta. Pēc tam atlasiet **pogu** Rediģēt programmu, lai atvērtu programmas darbvietu, kur varat skatīt datu kopas atjauninājuma statusu. Programmas darbvietā pēc izvēles varat arī iestatīt automātiskās atjaunināšanas grafikus datu kopai, pārvaldīt atļaujas un pārdēvēt programmas instanci.

### <a name="privacy"></a><a name="privacy"></a>Konfidencialitāte

Mums ir svarīga jūsu konfidencialitāte. Lai uzzinātu vairāk, izlasiet mūsu [Paziņojumu par konfidencialitāti](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
