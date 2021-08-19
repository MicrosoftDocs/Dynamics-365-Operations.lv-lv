---
title: Konsolidēto finanšu pārskatu ģenerēšana
description: Šajā tēmā ir aprakstīti dažādi scenāriji, kuros var būt nepieciešams ģenerēt konsolidētos finanšu pārskatus.
author: aprilolson
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 10f8754c4156893034117a4d449d464754eacafb0c0f6725c36709632af730ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727363"
---
# <a name="generate-consolidated-financial-statements"></a>Konsolidēto finanšu pārskatu ģenerēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti dažādi scenāriji, kuros var būt nepieciešams ģenerēt konsolidētos finanšu pārskatus.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Viena līmeņa un vairāku līmeņu juridisko personu konsolidācijas
Vienkāršākā metode konsolidēšanai, izmantojot finanšu pārskatu sniegšanu, ir izmantot pārskata kokus, lai apkopotu datus dažādos uzņēmumos, kuriem ir vienādi kontu plāni un finanšu periodi. Šeit norādītas augsta līmeņa darbības konsolidēšanai, izmantojot pārskatu koku.

1. Izveidojiet rindas definīciju un pārliecinieties, vai visi attiecīgie konti visos uzņēmumos ir iekļauti rindās.
2. Izveidojiet kolonnas definīciju, kas ietver visas kolonnas, kas nepieciešamas jūsu veidotajam pārskatam.
3. Izveidojiet pārskata koku, kas ietver pārskata mezglu katram uzņēmumam, kuru izmantojat konsolidētos pārskatos.

> [!TIP]
> Plašāku informāciju par to, kā izveidot un pārvaldīt rindu definīcijas, kolonnu definīcijas un pārskatu kokus, skatiet sadaļu [Finanšu pārskata komponenti](../../fin-ops-core/dev-itpro/analytics/financial-report-components.md).

Tālāk redzamajā attēlā ir parādīts, kā pārskatu koka definīciju var izmantot finanšu pārskatu sniegšanā, lai identificētu katru uzņēmumu, kas tiks konsolidēts.

![Pārskatu koka definīcija.](./media/reporting-tree-definition.png "Pārskatu koka definīcija")

Kā norādīts konsolidētajā ziņojumā tālāk redzamajās attēlā, izmantojot pārskatu koka kopā ar pārskatu definīciju, katru uzņēmumu var apskatīt atsevišķi. Konsolidētās summas tiek parādītas kopsavilkuma līmenī.

![Konsolidēt summas kopsavilkuma līmeni.](./media/consolidate-amount-summary-level.png "Konsolidēt summas kopsavilkuma līmeni")

Varat arī izveidot vairāklīmeņu pārskatu koku, kas ietver tik daudz līmeņu, cik nepieciešams. Tālāk redzamajā attēlā parādīta daudzlīmeņu pārskatu koka definīcija ar apkopojumiem pēc pasaules reģioniem.

![Vairāklīmeņu pārskata koka definīcija ar apkopojumiem pēc reģiona.](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Vairāklīmeņu pārskata koka definīcija ar apkopojumiem pēc reģiona")

Tālāk redzamajā attēlā parādīta daudzlīmeņu pārskatu koka definīcija ar apkopojumiem pēc funkcijas.

![Vairāklīmeņu pārskata koka definīcija ar apkopojumiem pēc funkcijas.](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "Vairāklīmeņu pārskata koka definīcija ar apkopojumiem pēc funkcijas")

### <a name="viewing-companies-side-by-side"></a>Uzņēmumu skatīšana līdzās
Daudzi klienti dod priekšroku pārskatiem, kur uzņēmumi tiek parādīti līdzās un kolonnā redzama konsolidētā kopsumma. Šo formātu ir viegli iegūt pēc tam, kad esat izveidojis pārskatu koku. Tālāk norādītas augsta līmeņa darbības, kas veicamas, lai konsolidētajos finanšu pārskatos uzņēmumus skatītu līdzās.

1. Izveidojiet kolonnas definīciju, kas katram uzņēmumam ietver kolonnu **Finanšu dimensija**.
2. Izmantojiet lauku **Pārskata vienība**, lai atlasītu koku un pārskata vienību katrai kolonnai.
3. Pēc izvēles: pievienojiet galvenes un kopsummas kolonnas.

Tālāk redzamajā piemērā parādīta kolonnas definīcija līdzāsparādīšanas formātā.

![Kolonnas definīcija līdzāsparādīšanas formātā.](./media/column-definition-side-by-side-format.png "Kolonnas definīcija līdzāsparādīšanas formātā")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Konsolidācijas, kas izmanto organizācijas struktūras, kas izveidotas no juridiskām personām
Organizācijas hierarhijas, kas satur dimensijas vai juridiskas personas, dinamiski izveido pārskatu koka definīcijas programmā Finanšu pārskatu sniegšana. Ērts konsolidāciju racionalizēšanas veids ir organizācijas hierarhijas pievienošana pārskatam programmā Finanšu pārskatu sniegšana. Pamatojoties uz pārskata datumu, programma Financial Reporting atlasīs organizācijas hierarhiju aktīvajā datumā vai pirms tā, kā parādīts tālāk redzamajā ilustrācijā.

![Dinamiski izveidot pārskata koka definīciju.](./media/dynamically-create-reporting-tree-definitions.png "Dinamiski izveidot pārskata koka definīciju")

## <a name="consolidations-that-involve-eliminations"></a>Konsolidācijas, kas ietver eliminācijas
Eliminācijas transakcijas ir konsolidācijas procesa parasta daļa. Šajā piemērā pieci konti tiek eliminēti konsolidācijas laikā: 142600, 211400, 401420, 401180 un 510820. Uzņēmumi var iestatīt starpuzņēmumu kontus atšķirīgi. Piemēram, dažos uzņēmumos konta pēdējais cipars tiek iestatīts kā 9, ja konts tiek izmantots starpuzņēmumu transakcijās. Neatkarīgi no metodes, ja zināt starpuzņēmumu kontus, varat parādīt eliminācijas konsolidētajos finanšu pārskatos.

Tālāk redzamajā ilustrācijā ir parādīta kolonnas definīcija konsolidētajam ieņēmumu paziņojumam. Katram uzņēmumam, izmantojot dimensiju filtru, ir definēti trīs peļņas un zaudējumu starpuzņēmumu konti. F, G un H kolonnās ir iekļauti tikai USMF, USRT un DEMF uzņēmumu eliminācijas konti. Šīs kolonnas ir iestatītas tā, ka tās **netiek** drukātas finanšu pārskatā.

![Kolonnas definīcijas konsolidētais peļņas un zaudējumu pārskats.](./media/column-definition-consolidated-income-statement.png "Kolonnas definīcijas konsolidētais peļņas un zaudējumu pārskats")

Veidojot pārskatu, eliminācijas summas tiek aprēķinātas F, G un H kolonnās, un tās tiek summētas I kolonnā. J kolonna parāda konsolidētās summas. Šīs konsolidācijas summas neietver eliminācijas USMF, USRT un DEMF uzņēmumiem.

> [!TIP]
> Izveidojiet otru pārskatu, kas parāda tikai eliminācijas ierakstus, un izmantojiet to pārskatu grupā, kas ietver jūsu konsolidēto pārskatu. Šādā veidā jums ir visa nepieciešama informācija, lai izveidotu jebkurus nepieciešamos žurnāla ierakstus.

Tālāk redzamajā ilustrācijā parādīts konsolidētais pārskats.

![Ienākumu deklarācijas konsolidētais finanšu pārskats.](./media/consolidated-report-income-statement.png "Ienākumu deklarācijas konsolidētais finanšu pārskats")

Neatkarīgi no tā, vai izmantojat kontus, dimensijas vai abus, programma Finanšu pārskatu sniegšana ļauj atfiltrēt eliminācijas ierakstus, izmantojot filtrēšanas iespēju dimensiju.

## <a name="minority-interest"></a>Mazākuma līdzdalības daļa
Uzņēmumam var piederēt tikai daļa cita uzņēmuma. Šādā situācijā, veidojot konsolidētu pārskatu, ir svarīgi, ka veicat atskaiti tikai par uzņēmumam piederošo procentuālo vērtību. Finanšu pārskatu sniegšanā ir vairāki veidi, kā parādīt mazākuma līdzdalības daļu atkarībā no lietotāja preferences. Viens veids ir izmantot apkopojuma procentuālo vērtību pārskatu koka definīcijā. Cits veids ir parādīt mazākuma īpašumtiesības kā atsevišķu rindu pārskatā.

### <a name="using-the-reporting-tree-definition"></a>Pārskatu koka definīcijas izmantošana
Pārskatu koka definīcijā ievadiet īpašumtiesību procentuālo daļu kolonnā **Apkopojuma %** (H kolonna), kā parādīts tālāk redzamajā ilustrācijā. Veidojot pārskatu, šī procentuālā vērtība tiks izmantota, lai aprēķinātu konsolidēto summu. Šajā piemērā uzņēmumam Contoso pieder tikai 80 procenti no uzņēmuma Contoso Vācijā. Varat ievadīt vai nu **80**, vai **.8** kolonnā **Apkopojuma %**, un 80 procent tiks apkopoti uz konsolidēto līmeni.

> [!NOTE]
> Šo īpašumtiesību procentuālo vērtību var piemērot jebkurai pārskata vienībai, ne tikai uzņēmuma līmenī. 

![Pārskatu koka definīcijas īpatsvara izmantošana.](./media/Using-reporting-tree-definition-percentage.png "Pārskatu koka definīcijas īpatsvara izmantošana")

Veidojot pārskatu, uzņēmuma Contoso Vācija ziņojumā tiks parādi 100 procenti no pārdošanas summas, un 80 procenti no summas tiks piešķirti un apkopoti uz pārdošanas konsolidēto līmeni.

Ja jums pieder mazāk nekā 1 procents no uzņēmuma, varat atlasīt izvēles rūtiņu **Atļaut apkopojumu mazāku par 1 %** cilnē **Papildu opcijas** lapā **Pārskata iestatījumi**, kā parādīts tālāk redzamajā attēlā. Šajā gadījumā vērtības kolonnā **Apkopojuma %** pārskatu kokā tiks apstrādātas kā mazāk nekā 1 procents. Piemēram, ievadot **.8**, uz konsolidēto līmeni tiks apkopoti 0,8 procenti, nevis 80 procenti. To pašu rezultātu arī var iegūt, atstājot izvēles rūtiņu **Atļaut apkopojumu mazāku par 1 %** neatzīmētu un ievadot **.008** kolonnā **Apkopojuma %**.

![Pārskatu iestatījuma opcijas.](./media/reporting-setting-options.png "Pārskatu iestatījuma opcijas")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Īpašumtiesību parādīšana atsevišķā rindā konsolidētajā pārskatā
Vēl viena mazākuma līdzdalības daļas iespēja ir parādīt 100 procentus meitasuzņēmuma katrai rindai pārskatā, bet atņemt nekontrolējošos procentus no tīrā ienākuma.

Kā parādīts tālāk redzamajā attēlā, paziņojumu **JA TAD CITS** un kolonnas ierobežojumu rindas definīcijā var izmantot, lai aprēķinātu mazākuma līdzdalības daļu finanšu pārskatos.

![Īpašumtiesību parādīšana atsevišķā rindā konsolidētajā pārskatā.](./media/Showing-ownership-separate-row-consolidated-report.png "Īpašumtiesību parādīšana atsevišķā rindā konsolidētajā pārskatā")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Vairāki juridisko personu kontu plāni
Bieži vien dažādām juridiskajām personām ir dažādi kontu plāni, taču tās joprojām vēlas izveidot konsolidētus finanšu pārskatus. Šādā gadījumā programmu Finanšu pārskatu sniegšana var izmantot, lai konsolidētu datus, lai varētu izveidot konsolidētus finanšu pārskatus. Tālāk ir aprakstītas augsta līmeņa darbības, kas veicamas, lai veiktu konsolidāciju, ja juridiskajām personām ir dažādi kontu plāni.

1. Izveidojiet rindas definīciju ar vairākām saitēm uz finanšu dimensijām. Katram kontu plānam ir jābūt vienai saitei.
2. Kolonnas definīcijā izmantojiet pārskata vienības ierobežojumu, lai piešķirtu katru uzņēmumu atbilstošajai kolonnai.


Rindas definīcijā katram unikālam uzņēmuma kontu plānam katrai rindai var pievienot vairākas saites uz finanšu dimensijām. Tālāk redzamajā attēlā USMF uzņēmums izmanto kontu kopu pirmajā **Saite uz finanšu dimensijām** kolonnā (J kolonna), un DEMF uzņēmums izmanto kontus otrajā **Saite uz finanšu dimensijām** kolonnā (K kolonna).

> [!TIP]
> Papildinformāciju par šūnu **Saite uz finanšu dimensijām** skatiet šūnā Saites norādīšana uz finanšu dimensijām.

![Iestatīt kontu pirmo saiti uz finanšu dimensijām.](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Iestatīt kontu pirmo saiti uz finanšu dimensijām")

Pārskatu koku var izmantot, lai definētu, kura saite uz finanšu dimensijām no rindas definīcijas tiek izmantota katram uzņēmumam. Atlasiet rindas definīciju E kolonnā un pēc tam atlasiet atbilstošās rindas saiti F kolonnā, kā parādīts tālāk redzamajā attēlā.

![Saistīt izmantoto finanšu dimensiju rindas definīciju.](./media/link-financial-dimensions-row-definition-used.png "Saistīt izmantoto finanšu dimensiju rindas definīciju")

> [!TIP]
> Veidojot saites uz finanšu dimensijām, izmantojiet aprakstu, lai identificētu uzņēmumus, uz kuriem katra saite attiecas. Šādā veidā var vieglāk atlasīt pareizo uzņēmumu, veidojot pārskatu koku. Kolonnas definīcijā lauks **Pārskata vienība** ļauj ierobežot katru kolonnu līdz pārskata koka vienībai, lai datus varētu skatīt līdzās. Ja kolonnai netiek norādīts noteikts uzņēmums, tiks parādīti konsolidētie dati visiem uzņēmumiem.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Dažādi finanšu kalendāri vairākām juridiskajām personām
Dažādām juridiskajām personām var būt dažādi finanšu kalendāri, taču tām joprojām ir prasība izveidot konsolidētus finanšu pārskatus. Ja juridiskajām personām ir dažādi finanšu periodi, pastāv divi tālāk aprakstītie veidi, kā veikt konsolidāciju.

- Izveidojiet kolonnas definīciju un lietojiet periodu un gadu, lai kartētu atbilstošos periodus katram uzņēmumam.
- Sadaļā **Iestatījumi** \> **Citi** \> **Papildu opcijas** atlasiet, vai konsolidēt, izmantojot perioda beigu datumu vai perioda numuru.

Veidojot kolonnas definīciju vairākiem uzņēmumiem ar atšķirīgiem finanšu periodiem, ir svarīgi apsvērt, kurš uzņēmums tiks piešķirts laukam **Uzņēmuma nosaukums** pārskata definīcijā. Šī uzņēmuma finanšu kalendārs tiks lietots kā pamata finanšu kalendārs pārskata definīcijai. Piemēram, tālāk redzamajā tabulā ir parādīts finanšu periods, kas tika iestatīts USMF un INMF uzņēmumiem. Konsolidētajiem pārskatiem lietojiet USMF izmatoto finanšu kalendāru. "Kartēšanas" kolonnā tiek rādīts līdzvērtīgais periods un gads katram uzņēmumam, ja pārskats tiek veidots uz 2018. gada 30. jūniju.

| Uzņēmums   | Finanšu gads                                  | Kartēšana                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Finanšu gads, no 1. jūlija līdz 30. jūnijam          | 12. periods, 2018. finanšu gads | 
| INMF      | Kalendārais gads, no 1. janvāra līdz 31. decembrim | 6. periods, 2018. finanšu gads  |

Tālāk redzamajā attēlā USMF uzņēmums ir norādīts laukā **Uzņēmuma nosaukums** pārskata definīcijā. Tādēļ USMF uzņēmuma finanšu kalendārs tiks lietots kā pamata finanšu kalendārs. Šajā piemērā, veidojot pārskatu uz 2018. gada 30. jūniju, tiks izmantots USMF uzņēmuma BĀZES periods, kas ir definēts kā 12. periods pārskata definīcijā. INMF uzņēmums izmantos 6. BĀZI, kas ir 6. periods. Abās kolonnās tiks iekļauti dati par 2018. gada jūniju.

![Pārskata bāzes periods.](./media/report-base-period.png "Pārskata bāzes periods")

Tālāk redzamajā attēlā ir parādītas opcijas pārskata definīcijā, kas ļauj atlasīt, vai konsolidācijā tiek izmantots perioda numurs vai perioda beigu datums.

![Opciju pārskata definīcijas perioda numurs.](./media/options-report-definition-period-number.png "Opciju pārskata definīcijas perioda numurs")

## <a name="business-unit-consolidations"></a>Biznesa vienības konsolidācijas
Šajā tēmā tika apskatīta pārskatu koka definīciju un organizācijas hierarhijas izmantošana programmā Finanšu pārskatu sniegšana konsolidācijas nolūkos. Pārskatu koku var arī izmantot, lai izveidotu biznesa vienības konsolidācijas pārskatus, piemēram, pārskatus par pārdošanu vai operācijām visā pasaulē. Šie pārskati ir standarta prasība. Lai tos izveidotu, atlasiet uzņēmumu un dimensiju katrai vienībai, kuru vēlaties konsolidēt. Piemēram, tālāk redzamajā attēlā biznesa vienības apkopojums ir veikts, atkārtojot katru uzņēmumu kolonnā **Uzņēmums** (A kolonna) un identificējot nodaļas grupas dimensijas vērtības katram uzņēmumam kolonnā **Dimensijas** (D kolonna).

![Biznesa vienības konsolidācijas pārskati.](./media/business-unit-consolidation-reports.png "Biznesa vienības konsolidācijas pārskati")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Konsolidācijas, kas ietver vairākas pārskata valūtas
Finanšu pārskatu sniegšanas programma piedāvā lielāku elastību, skatot faktiskos, budžeta, budžeta kontroles un budžeta plānošanas datus vairākās valūtās. Pārceļot galvenos iestatījuma datus, nav nepieciešams veikts nekādus papildu iestatījumus finanšu pārskatu veikšanas programmā, lai skatītu jebkuru pārskatu jebkurā valūtā, jebkurā laikā un jebkuram lietotājam.

### <a name="prerequisites"></a>Priekšnosacījumi
Lai pareizi aprēķinātu pārrēķinātās bilances, finanšu pārskatu programma prasa, lai kategorija **Nesadalītās peļņas konts** tiktu piešķirta nesadalītās peļņas kontam sarakstā **Galvenais konts**. Finanšu pārskatu programma neatbalsta grāmatošanu uz nesadalītās peļņas kontu. Ja transakcijas tiek grāmatotas uz nesadalītās peļņas kontu, pārrēķinātās bilances netiks aprēķinātas pareizi. Mēs iesakām lietotājiem iestatīt papildu nesadalītās peļņas kontu, kurā grāmatot nesadalītās peļņas konta korekcijas.

Galvenajā kontā lauki **Finanšu pārskatu maiņas kursa tips** un **Valūtas pārrēķināšanas veids** kopsavilkuma cilnē **Finanšu pārskatu sniegšana** katram kontam ir jāiestata, kā parādīts tālāk redzamajā piemērā. Šo uzdevumu var veikt katrā kontā atsevišķi, vai arī varat izmantot kontu veidnes, lai ērti ieviestu izmaiņas.

- Laukā **Finanšu pārskatu maiņas kursa tips** atlasiet maiņas kursa tipu, kas satur kontam piemērojamās valūtas un maiņas kursus. Šī valūtu un maiņas kursu tabula tiks piemērota faktiskajiem datiem finanšu pārskatu programmā.
- Laukā **Valūtas pārrēķināšanas tips** atlasiet maiņas kursu aprēķināšanas metodi kontam. Šī valūtas metode tiek izmantota gan faktiskajiem, gan budžeta datiem finanšu pārskatu sniegšanas programmā.

![Finanšu pārskata galvenie konti.](./media/Financial-reporting-main-accounts.png "Finanšu pārskata galvenie konti")

Budžeta, budžeta kontroles un budžeta plānošanas datiem maiņas kursa tips tiek definēts lapā **Virsgrāmata**. Šī tabula tiks izmantota, lai iegūtu maiņas kursus un valūtas pārrēķināšanas veidu, kas ir piešķirti kontam.

### <a name="currency-translation-methods"></a>Valūtas pārrēķināšanas metodes
Finanšu pārskatu programmā ir četras maiņas kursu aprēķināšanas opcijas, kas aprakstītas tālāk.

- **Svērtais vidējais** – šī metode visbiežāk tiek izmantota peļņas un zaudējumu kontiem. Tajā tiek izmantota šāda formula:

    (maiņas kurss × dienas spēkā) ÷ dienu skaits periodā

- **Vidējais** – šī metode ir alternatīva metode peļņas un zaudējumu kontiem. Tajā tiek izmantota šāda formula:

    maiņas kursu kopsumma ÷ maiņas kursu skaits

- **Pašreizējais** – šī metode visbiežāk tiek izmantota bilances kontiem. Izmantotais maiņas kurss ir kurss, kāds ir bijis finanšu pārskatu programmas pārskata vai kolonnas datumā vai pirms tā.
- **Transakcijas datums** – šī metode tiek izmantota, lai pamatlīdzekļu kontos. Izmantotais maiņas kurss ir tās dienas kurss, kad līdzekļi tika iegādāti. Ja šī datuma kurss nav ievadīts, tiek izmantots kurss, kas ir iepriekš ievadīts vistuvāk līdzekļu iegādes datumam.

### <a name="report-designer-options-for-currency-translation"></a>Pārskata veidotāja opcijas valūtas pārrēķināšanai
Finanšu pārskata programmā jebkuru pārskatu var parādīt neierobežotā pārskata valūtu skaitā. Tālāk uzskaitītie lauki pārskata definīcijā atbalsta šo iespēju.

- Sadaļa **Valūtas informācija** lapā **Pārskata definīcija**. Šajā sadaļā redzama valūta, kurā vērtības tiek parādītas, izveidojot pārskatu.
- Jauna izvēles rūtiņa **Ietvert visas pārskata valūtas** Ja šī izvēles rūtiņa ir atlasīta, katrai pārskata valūtai tiks pievienots pārskats pārskatu rindā, pēc tam, kad tiek izveidots pārskats, kas izmanto uzņēmuma funkcionālo valūtu. Ja izvēles rūtiņa nav atzīmēta, joprojām var atlasīt pārskata valūtu tīmekļa skatītājā. Šajā gadījumā pārskata valūta tiks apstrādāta tikai tad, ja to atlasīsiet.

Pārskata definīcijas opcijas ļauj viegli pārrēķināt pārskatu visās pārskata valūtās. Tāpēc, iespējams, varēsiet eliminēt dublikātu pārskata definīcijas, kas atšķiras tikai ar izmantotajām valūtām. Ja ir nepieciešams pārskats, kurā līdzās tiek parādītas vairākās valūtas, varat turpināt lietot lauku **Valūtu parādīšana** lapā **Kolonnas definīcija**, lai pārrēķinātu tikai konkrēto pārskata kolonnu citā pārskata valūtā.

### <a name="currency-translation-adjustment"></a>Valūtas pārrēķināšanas korekcija
Valūtu pārrēķināšanas korekcija (VPK) ir starpība starp kursiem, kuri tiek izmantoti, lai aprēķinātu bilances kontus, un kursu, kas tiek izmantots ienākumu paziņojuma kontos. Šī atšķirības dēļ bilance nebūs līdzsvarā. Finanšu pārskatu programmu var izmantot, lai aprēķinātu VPK divos tālāk aprakstītajos veidos.

- Izmantojiet lapu **Noapaļošanas korekcijas** rindas definīcijā, kā parādīts tālāk redzamajā attēlā.

    ![Valūtas pārrēķina korekcijas noapaļošanas korekcijas.](./media/Currency-translation-adjustment-rounding-adjustments.png "Valūtas pārrēķina korekcijas noapaļošanas korekcijas")

    Norādot rindu, kurā jāparāda noapaļošanas korekcija (VPK), kopējo līdzekļu rindu, kopējo saistību un kapitāla rindu un pieņemamo slieksni, finanšu pārskatu programma aprēķinās starpību un ievadīs to vēlamajā rindā. Tiks izveidota rinda ar nosaukumu **Noapaļošanas korekcija**, un tā tiks parādīta detalizētā skatā, kā parādīts tālāk redzamajā attēlā.

    ![Noapaļošanas korekcija detalizēti.](./media/rounding-adjustment-drill-down.png "Noapaļošanas korekcija detalizēti")

- Lieciet visus kontus diapazonā, no aktīviem līdz izdevumiem. Kā parādīts tālāk redzamajā ilustrācijā, starpība būs tāda pati summa kā noapaļošanas korekcija (VPK). Tādēļ to var izmantot kā kopsummas pārbaudi, lai pārliecinātos, vai noapaļošanas korekcijas lapa neietver kādas kontu bilances, kas tika izlaistas.

    ![Noapaļošanas korekcijas formas pārbaude.](./media/rounding-adjustment-form-check.png "Noapaļošanas korekcijas formas pārbaude")

### <a name="balance-calculation-approach"></a>Bilances aprēķina pieeja
Lai iegūtu pareizi pārrēķinātas summas, kad tiek izmantotas valūtas, finanšu pārskatu programma izmanto tālāk aprakstītās bilanču aprēķina metodes.

- **Svērtais vidējais un vidējais** — katrs periods tiek aprēķināts kā svērtais vidējais un tiek summēts pēc kolonnām, piemēram, pēc ceturkšņa un no gada sākuma.
- **Vēsturiskais** – jebkurš konts, kas izmanto vēsturisko pārrēķina metodi, vienmēr atgriežas pie transakcijas datuma. Ja iegādes datums ir saistīts ar transakciju, šis datums tiek izmantots maiņas kursa iegūšanai. Katrs periods pēc tam tiek summēts un saglabāts, lai palīdzētu uzlabot aprēķina laiku.
- **Pašreizējais** – aprēķinātās un kopsummas kolonnas, piemēram, ceturkšņa un no gada sākuma līdz šim datumam, tiek aprēķinātas pēc valūtas kursa, kas ir noteikts kolonnā vai pārskatā. Piemēram, kolonnas **1. ceturksnis** izmantos 31. marta kursu, ja tiek izmantots kalendārais gads.

## <a name="additional-resources"></a>Papildu resursi

Lai iegūtu papildu informāciju par konsolidāciju un valūtas pārrēķiniem, skatiet šīs tēmas pamata tēmu [Finanšu konsolidācijas un valūtas pārrēķināšanas pārskats](./financial-consolidations-currency-translation.md).

Lai iegūtu plašāku informāciju par to, kā ievadīt konsolidācijas tiešsaistē datus, skatiet sadaļu [Finanšu konsolidēšana tiešsaistē](./consolidate-online.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]