---
title: Commerce analīze (priekšskatījums)
description: Šajā rakstā skaidrots, kā instalēt un izmantot analīzes iespējas Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 9ffa0affa0b80af65dd2aa37ef2fe969752ae332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887170"
---
# <a name="commerce-analytics-preview"></a>Commerce analīze (priekšskatījums)

[!include [banner](includes/banner.md)]

Šajā rakstā ir izskaidrots, kā instalēt Commerce Analytics (priekšskatījums), funkcionālo analīzes spēju, kas ir iekļauta Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>Commerce Analytics (priekšskatījums) tiešais demonstrācija

Varat mēģināt kādu live [demonstrāciju pakalpojumā Commerce Analytics (preview)](https://aka.ms/CommerceAnalyticsDemo).

![Commerce Analytics (Preview) Summary](media/CommerceAnalytics_Summary.png)
![Commerce Analytics (priekšskatījums) Maksājumi](media/CommerceAnalytics_Payments.png)
![Commerce Analytics (priekšskatījums) web aktivitāte](media/CommerceAnalytics_WebActivity.png)

## <a name="commerce-analytics-preview-system-architecture"></a>Commerce Analytics (Preview) sistēmas arhitektūra

### <a name="key-components"></a>Galvenie komponenti

Commerce Analytics (Preview) sastāv no šādiem galvenajiem komponentiem:

- Lietošanai gatavie interaktīvie Power BI pārskati
- SQL skati Azure Synapse Analytics
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
- Datus sagatavo citas sistēmas, piemēram,Dynamics 365 Connected Spaces.

#### <a name="step-2-ingestion-and-pre-processing"></a>2. solis. Iesācīšana un pirmapstrāde

Transakciju dati tiek iet uz Commerce HQ tieši (pasūtījumu gadījumā, kas tiek notverti tieši Commerce HQ klientā) vai caur Commerce Scale Unit (ja pasūtījumi ir notverti POS, e-komercijas ietvaros vai pielāgotos klientos, kas izmanto bezgalīgo tirdzniecību).

Pēc tam funkcija Eksportēt uz datu Konta tiek izmantota, lai kopētu darbības datus uz jūsu datiem kā neapstrādātus datus. Neapstrādātie dati saglabāts mapē Tabulas.

E-komercijas tīmekļa aktivitātes dati tiek sūtīti tieši uz datu darbību. Datus, ko sagatavo citas sistēmas, piemēram Dynamics 365 Connected Spaces, tos, nosūta tieši uz šo sistēmu datiem.

#### <a name="step-3-transformation-and-aggregation"></a>3. darbība: pārvēršana un apkopošana

Kad neapstrādātie dati ir jūsu datu struktūrā, Commerce Analytics pakalpojums to nolasa, pārveido, uzkopē un ieraksta atpakaļ datu ierakstītājā loģisko entītiju formā (entītiju mapē) un uzkrātos rādītājus (ontoloģijas mapē).

#### <a name="step-4-querying"></a>4. darbība: vaicājums

Azure Synapse Analytics tiek lietots, lai vaicātu datos, lietojot Transact-SQL (T-SQL) interfeisu. Šis interfeiss ietver SQL skatus. SQL skati iespējo datu ārējas vaicāšanas datu pakalpojumā, vai nu tieši, izmantojot T-SQL klientu (ekspromtanai) vai vizualizēšanas rīku, piemēram Power BI.

#### <a name="step-5-modeling-and-serving"></a>5. solis. Modelēšana un apkalpošana

Dati, uz kuriem attiecas vaicājums Azure Synapse Analytics, Power BI attiecas uz semantisko modeli. Atkarībā no datu tipa tie ir Power BI periodiski importēti atmiņā vai tieši vaicājumā izpildlaikā.

Visbeidzot dati tiek atveidoti vizuāli Power BI, lai lietotāji varētu tos apskatīt un mijiedarboties.

## <a name="commerce-analytics-preview-functional-overview"></a>Commerce Analytics (Preview) funkcionālā apskats

### <a name="summary"></a>Kopsavilkums

Commerce Analytics veidnes programmā ir ietvertas šādas galvenās pārskatu lapas:

1. [Augstākā līmeņa filtri](#TopLevelFilters)
2. [Produkti](#ProductsPage)
3. [Debitori](#CustomersPage)
4. [Kanāli](#ChannelsPage)
5. [Pārdošana](#SalesPage)
6. [Robežas](#MarginsPage)
7. [Atgriešanas](#ReturnsPage)
8. [Atlaides](#DiscountsPage)
9. [Maksājumi](#PaymentsPage)
10. [Debitori](#CustomersPage)
11. [Salīdzinājums](#ComparisonPage)
12. [Aktivitāte tīmeklī](#WebActivityPage)
13. [Web aktivitāte — augstākā līmeņa filtrs](#WebActivityTopLevelFilters)

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Augstākā līmeņa filtri

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

#### <a name="products"></a><a name="ProductsPage"></a> Produktiem

- Pārdošana
- Peļņa
- Atgriešanas

#### <a name="customers"></a><a name="CustomersPage"></a> Klientiem

- Pārdošana
- Peļņa
- Atgriešanas

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanālus

- Pārdošana
- Peļņa
- Atgriešanas

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
    - Produkts

### <a name="payments"></a><a name="PaymentsPage"></a> Maksājumus

- Pēc kanāla/termināļa
- Pēc maksāšanas metodes/tipa
- Pēc datuma
- Dekompozīcija

    - Juridiska persona
    - Kanāla veids
    - Veikals
    - Terminālis
    - Maksājuma metode

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
    - Paņemt
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

    Sesijas sesija ir sesija, kurā lietotājs pamet tūlīt pēc jūsu e-komercijas vietnes apmeklējuma. Papildinformāciju skatiet Sadaļā Vaidu [likme](https://en.wikipedia.org/wiki/Bounce_rate).

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

Iespaids ir atsevišķs e-komercijas uzņēmuma skatījums par preci, kas ir vizuāla. Piemēram, e-komercijas apskats tiek atvērts uz jūsu e-komercijas **vietnes sākumlapu un skatiem kādu no lietojumprogrammas lietojumprogrammu lapām augšējā pārdošanas** saraksta modulī. Skatījums šeit skata to pašu mat preci saraksta **modulī** Izdotais. Šajā gadījumā ir divi preces iespaidi.

Pašlaik iespaidi tiek izsekoti šādās virsmas:

- Saraksti (piemēram, Recommended **, Top selling**, **Picks for you** un **Trending**)**·**
- Groza modulis
- Meklēšanas rezultāta konteiners
- Kategorijas meklēšanas rezultāta konteiners

Pašlaik preces, kas ir atveidotas karuseļa modulī vai pielāgotā vizuālajās attiecībās, nav skaitītas ar attēlu saistītajos metrikās.

Pārskatā **par pārskatu par** pārskatu ir iekļauti šādi rādītāji:

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
> Commerce Analytics (Preview) ir priekšskatījumā Amerikas Savienotajās Valstīs, Kanādā, Apvienotajā Karalistē, Eiropā, Dienvidāzijā, Austrumāzijā, Austrālijā un Japānas reģionos. Ja finanšu un operāciju vide ir jebkurā no šiem reģioniem, varat iespējot šo funkciju savā vidē Microsoft Dynamics, izmantojot lifecycle Services (LCS). Pirms šo funkciju varat izmantot, skatiet sadaļu [Eksporta konfigurēšana uz Azure Data Nosūtīšana](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a> Iespējot un konfigurēt Commerce Analytics (Priekšskatījums)

Lai instalētu Commerce Analytics (priekšskatījumu), jums ir nepieciešamas atļaujas izveidot resursus Azure abonementā. Jums ir arī jābūt atļaujām instalēt pievienojumprogrammas LCS.

Lai iespējotu un konfigurētu Commerce Analytics (Preview), veiciet šos soļus.

1. [Iesniegt Priekšskatījuma veidlapas Commerce Analytics (Priekšskatījums)](#joinPreview)
2. [Iespējojiet un konfigurējiet eksportēšanu uz datu Galapunkta pievienojumprogrammu](#enableExportToDataLake).
3. [Instalējiet un konfigurējiet darbvietu Azure Synapse](#configureAzureSynapse).
4. [Pievienojiet atslēgas noslēpumus atslēgai](#addSecrets).
5. [Iespējojiet un konfigurējiet Commerce Analytics (Preview) pievienojumprogrammu](#enableCommerceAnalyticsAddin).
6. [Instalējiet veidnes Power BI programmu](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a> Iesniegt Priekšskatījuma veidlapas Commerce Analytics (Priekšskatījums)

Iesniedziet [Commerce Analytics (Preview) formu Preview](https://forms.office.com/r/vW5VLJGXZ2). Kad jūsu pieprasījums ir apstrādāts, uz e-pasta adresi, ko nosūtījāt formā, tiks nosūtīts apstiprinājuma e-pasta ziņojums.

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a> Iespējot un konfigurēt pievienojumprogrammu Eksports uz datu Galapunktu

> [!IMPORTANT]
> Konfigurējot pievienojumprogrammu Eksportēt uz datuPapildinformāciju, **notīriet izvēles rūtiņas Real-time data** izmaiņas izvēles rūtiņu Eksportēt uz datu reģistrēšanās iestatīšanas lapā, lai nodrošinātu, ka reāllaika datu izmaiņas nav iespējotas. Reāllaika **datu izmaiņu līdzeklis** ir priekšskatījumā un to pašlaik neatbalsta Commerce Analytics. Ja iespējojat šo funkciju, Commerce Analytics nevarēs apstrādāt datus datu kontā, Power BI un lielākā daļa pārskatu nerādīs datus.

Commerce Analytics (Priekšskatījums) balstās uz iespēju Eksportēt uz datuKursi, lai commerce headquarters datus eksportētu uz Data Lai gana un paturētu datus jaunu. Pirms Commerce Analytics (preview) konfigurēšanas iespējojiet un konfigurējiet eksportēšanu uz datu [plkst](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Konfigurējot Pievienojumprogrammu Eksportēt uz datuPapildinformāciju, atzīmējiet šo informāciju, jo jums tā būs jāievada vēlāk:

- <a name="keyVault"></a> Jūsu sniegtās atslēgas Domēna nosaukuma sistēmas (DNS) nosaukums.
- Jūsu sniegtie slepenie vārdi un kuros ietverts pieteikuma ID un pieteikuma noslēpums. Papildinformāciju skatiet sadaļā [Noslēpumu pievienošana atslēgai](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a> Darbvietas instalēšana un Azure Synapse konfigurācija

Commerce Analytics (priekšskatījums) prasība, lai Paralēle SQL pēc pieprasījuma tiktu nodrošināta jūsu darbvietā Azure Synapse. Lai instalētu un konfigurētu darbvietu Azure Synapse, veiciet šādas darbības.

1. Instalējiet darbvietu Azure Synapse savā Azure abonementā. Papildinformāciju skatiet Sadaļā [Ātrā startēšana: Darbalauku izveidošana par Darbalauku Bez darbalauku](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a> Pēc darbvietas nodrošināšanas atveriet resursu pārskata **lapu un atzīmējiet bezservera SQL galapunkta** vērtību. Šī vērtība ir jāsaglabā galvenās sadaļas atslēgas.
1. Apskata lapā atlasiet saiti **Atvērt Darbalauku** Studio, lai atvērtu darbalauku Azure Synapse.
1. Izvēlnē **Pārvaldīt** atlasiet Pārvaldīt. Lai apskatītu izvēlnes nosaukumus, iespējams, kreisajā izvēlnē jāatlasa izvēršanas saite.
1. Sadaļā **Drošības grupa** atlasiet **Piekļuves kontrole**. 
1. Atlasiet **Pievienot**.
1. Rūtī Pievienot **lomu piešķiri** iestatiet opcijas tā, kā aprakstīts šajā tabulā.

    | Opcija | Vērtība |
    |--------|-------|
    | Tvērums | Atlasiet **darbalauku**. |
    | Loma | Atlasiet **Pakalpojuma SQL administratoru**.|
    | Atlasīt lietotāju | Meklējiet tās programmas nosaukumu, kas tika [izveidota, instalācijas laikā eksportējot pievienojumprogrammu Eksportēt uz datu mapi](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Kad programma parādās meklēšanas rezultātos, atlasiet to. Programma tiks parādīta sadaļā Atlasītie **lietotāji, grupas vai pakalpojumu vadītāji**. |

1. Atlasīt Lietot **,** lai pabeigtu lomu piešķiri. Programmai tiek piešķirtas Neapse SQL administratora privilēģijas. Tāpēc commerce Analytics (Preview) LCS pievienojumprogrammas konfigurācijas laikā var izveidot nepieciešamos skatus.

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a> Pievienot atslēgas noslēpumus atslēgai

Tajā pašā atslēgā [,](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault) ko izmantojāt, konfigurējot eksportēšanu uz Data Neipus pievienojumprogrammu, ir jāpievieno noslēpumi, kas tiek rādīti šajā tabulā. Katram noslēpumam ir jānorāda noslēpuma vārds un norādītā vērtība.

| Ieteicamais slepenais vārds | Noslēpuma vērtība | Piemērs slepeno vērtību |
|---------|---------|---------|
| , <a0/&; sql-server | Bezservera SQL galapunkta vērtība, ko atzīmēāt, konfigurējot [darbvietu Azure Synapse](#serverlessep). | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a> readonly-SQL-pwd | Parole, kas jāiestata SQL tikai lasāmam lietotājam. Pārskats Power BI izmantos šo paroli, lai izveidotu savienojumu ar bezservera SQL. Lai iestatītu paroli, izpildiet organizācijas paroles politikas. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a> Iespējot un konfigurēt Commerce Analytics (Preview) pievienojumprogrammu

Lai instalētu Commerce Analytics (Preview) pievienojumprogrammu LCS, jums ir jābūt vides administratoram LCS vidē, ko plānojat izmantot.

Lai instalētu un konfigurētu Commerce Analytics (Preview) pievienojumprogrammu, veiciet šos soļus.

1. [pieteikties LCS](https://lcs.dynamics.com/) un doties uz vidi.
2. **Vides lapas** cilnē **Vides pievienojumprogrammas** atlasiet Instalēt **jaunu pievienojumprogrammu**.
3. Dialoglodziņā atlasiet Commerce **Analytics (Priekšskatīt)**.
4. Dialoglodziņā Iestatīšanas **pievienojumprogramma** ievadiet šādu informāciju.

    | Informācija | Avots | Vērtības piemērs |
    |---|---|---|
    | Azure Active Directory(Azure AD) Nomnieka ID | [pieteikties Azure portālā](https://portal.azure.com/) un atvērt **Azure Active Directory** pakalpojumu. Pēc tam atveriet **rekvizītu** lapu un kopējiet vērtību laukā **Nomnieka ID**. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | Jūsu Azure atslēgas DNS nosaukums | Ievadiet jūsu atslēgas, piemēram, DNS nosaukumu. Šai vērtībai ir jābūt piezīmei, konfigurējot [pievienojumprogrammu Eksportēt uz datu neitu](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Slepenais vārds, kas satur pieteikuma ID | Ievadiet slepeno vārdu, kurā tiek glabāts programmas ID. Šai vērtībai ir jābūt piezīmei, konfigurējot [pievienojumprogrammu Eksportēt uz datu neitu](#keyVault). | `app-id` |
    | Noslēpuma vārds, kas satur pieteikuma noslēpumu | Ievadiet slepeno vārdu, kas glabā pieteikuma noslēpumu. Šai vērtībai ir jābūt piezīmei, konfigurējot [pievienojumprogrammu Eksportēt uz datu neitu](#keyVault). | `app-secret` |
    | Slepenais vārds, kas satur serverless SQL galapunktu šim: Azure Synapse | Ievadiet slepeno vārdu, kas saglabā bezservera SQL galapunktu. Jums būtu jābūt izveidojuši noslēpumu, kamēr atslēgas [vērtībai esat pievienojis noslēpumus](#addSecrets). | `synapse-sql-server` |
    | Slepenais vārds, kas satur paroli, kas jāiestata SQL tikai lasāmajiem lietotājiem Azure Synapse | Ievadiet slepeno vārdu, kas glabā paroli, kas jāiestata bezservera SQL tikai lasāmam lietotājam. Šis lietotājs tiks jums izveidots un tiks izmantots pārskatā, Power BI lai izveidotu savienojumu ar bezservera SQL serveri. Kamēr atslēgas vērtībai esat pievienojis noslēpumus [, jums bija jāizveido noslēpums](#addSecrets). | `readonly-sql-pwd` |

1. Apstipriniet piedāvājuma nosacījumus, atzīmējot šo izvēles rūtiņu, un pēc tam atlasiet **Instalēt**.

    Sistēma instalē un konfigurē Commerce Analytics (Preview) pievienojumprogrammu videi. Šis process var ilgt dažas minūtes. Kad commerce analytics (priekšskatījums) ir pabeigts, **tam jābūt uzskaitītam** vides **lapā un statusam jābūt Instalēts** **.**

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a> Instalējiet veidnes Power BI programmu

Lai instalētu Commerce Power BI Analytics veidnes programmu (Priekšskatījums), izpildiet šīs darbības.

1. Piesakieties portālā [Power BI](https://powerbi.microsoft.com/), izmantojot organizācijas ID.
1. Instalējiet Commerce Analytics (Preview) Power BI veidnes programmu, ejot uz [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Vai arī skatiet lapu analīzes [AppSource atlasei Dynamics 365 Commerce](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) un atlasiet Iegūt **to tūlīt**.
1. Ja programmu atkārtoti instalējot pirmo reizi, pārejiet pie 5. soļa. Ja programma ir instalēta iepriekš, tad programmas atjaunināšanai ir pieejamas šādas opcijas:

    - **Atjauniniet darbvietu un programmu** — atjauniniet esošo veidnes programmu un pārrakstiet esošos programmas iestatījumus, piemēram, programmas instances nosaukumu un atļauju konfigurācijas.
    - **Atjaunināt tikai darbvietas saturu, neatjauninot programmu** — atjaunināt esošo veidnes programmu, bet paturēt esošos programmas iestatījumus. *Šī opcija ir ieteicamā programmu atjaunināšanas opcija.*
    - **Instalējiet citu programmas kopiju jaunā darbvietā** — izveidojiet jaunu darbalauku un pēc tam izveidojiet tajā esošās veidnes programmas kopiju. Esošā darbvieta netiks neskarta.

1. Atlasiet vienu no atjaunināšanas opcijām un pēc tam atlasiet **Instalēt**.
1. Atveriet instalēto programmu, kreisajā **rūtī** atlasot Programmas un pēc tam atlasot programmu.
1. Savienojiet programmu ar datu avotu, atlasot **Pievienot**. Ja programmu instalējāt iepriekš, dzelteno **ziņojumu** joslā atlasiet datu saiti Savienot ar datiem.
1. Iestatiet tālāk minētos laukus.

    | Lauks | Vērtība |
    |---|---|
    | Serveris | Ievadiet bezservera SQL galapunktu, ko izdarījāt ar piezīmi par to, ka izveidojāt [darbvietu Azure Synapse](#serverlessep). |
    | Datu bāze | Ievadiet **CommerceAnalytics**. |
    | Valoda | Atlasiet sarakstā vērtību. Šis lauks tiek izmantots lokalizētiem preču un kategoriju nosaukumiem. Vērtība ir reģistrjutīga. |
    | Datumu diapazons | Atlasiet sarakstā vērtību. Dati par atlasītajiem mēnešiem tiks importēti Power BI datu kopā. Atlasītā vērtība ietekmē datu kopas lielumu un sinhronizācijai nepieciešamo laiku. |

1. Atlasiet **Nākamais**. Kad tiek piedāvāts ievadīt akreditācijas datus savienojumam Azure Synapse ar SQL datu bāzi, iestatiet lauka vērtības kā parādīts šajā tabulā.

    | Lauks | Vērtība |
    |---|---|
    | Autentifikācijas metode | Atlasiet **Pamata**. |
    | Lietotājvārds | Ievadiet **reportreadonlyuser**. |
    | Parole | Ievadiet paroli, kuru [esiet saglabājis SQL tikai lasāmā lietotāja atslēgā](#roUser). |

1. Atlasiet **pieteiksies un izveidojiet savienojumu**.
1. Uzgaidiet, līdz datu kopa tiks veiksmīgi atjaunināta. Pēc tam **atlasiet Rediģēt programmu**, lai atvērtu programmas darbvietu, kurā varat skatīt datu kopas atjauninājuma statusu. Programmas darbvietā pēc izvēles varat arī iestatīt automātiskās atjaunināšanas grafikus datu kopai, pārvaldīt atļaujas un pārdēvēt programmas instanci.

### <a name="privacy"></a><a name="privacy"></a>Konfidencialitāte

Mums ir svarīga jūsu konfidencialitāte. Lai uzzinātu vairāk, izlasiet mūsu [Paziņojumu par konfidencialitāti](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
