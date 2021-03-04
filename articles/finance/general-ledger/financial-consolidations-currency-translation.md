---
title: Pārskats par finanšu konsolidācijām un valūtas konvertāciju
description: Šajā tēmā ir aprakstītas finanšu konsolidācijas un valūtas pārrēķināšana Virsgrāmatā.
author: aprilolson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 2a6685a2dcf9d7bf7ac82c3dede9c3ece0c08698
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445707"
---
# <a name="financial-consolidations-and-currency-translation-overview"></a>Finanšu konsolidācijas un valūtas pārrēķināšanas pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta pieeja, kas tiek izmantota konsolidācijai gan programmā Microsoft Dynamics 365 Finance, gan modulī Finanšu pārskatu izveide. Tēmā ir aprakstīti scenāriji, kas ietver vairāku uzņēmumu pārskatu veidošanu, apkopojumu, elimināciju un mazākuma līdzdalības daļu. Tajā ir arī paskaidrots, kā rīkoties īpašās situācijās, piemēram, scenārijos, kur juridiskajām personām ir dažādi finanšu periodi vai dažādi kontu plāni.

Šī tēma tika rakstīta lietotājiem un funkcionāliem konsultantiem, pieņemot, ka lasītājiem ir vispārīga izpratne par programmu Finance un par finanšu pārskatu veidošanu. Pamata iestatījumi netiek apskatīti.

> [!NOTE]
> Termins *juridiska persona* tiek izmantots programmā Finance, un termins *uzņēmums* tiek izmantots finanšu pārskatu veidošanā. Šajā tēmā tiek izmantoti abi minētie termini. Tomēr šīs tēmas ietvaros to nozīmes ir vienādas.

## <a name="audience"></a>Mērķauditorija
Šī tēma ir paredzēta finanšu un grāmatvedības lietotājiem un programmas konsultantiem, kuri vēlas izmantot programmu Finance and Reporting un finanšu pārskatu vairāku uzņēmumu un vairāku valūtu datu konsolidācijai.

## <a name="approach"></a>Pieeja
Programmā Finance konsolidācijas apstrādei tiek izmantota atsevišķa juridiska persona. Tas iespējo vienas instances konsolidāciju, bet nodrošina opciju papildināt datus no citiem avotiem. Konsolidācijas process ir jāveic katru reizi, kad izcelsmes juridiskajām personām tiek veiktas izmaiņas.

Finanšu pārskatu var konsolidēt vairāku uzņēmumu pārskata ģenerēšanas laikā. Lai gan dati tiek uzglabāti datuvē, tiek versionēti un tos var eksportēt, katrs izcelsmes uzņēmums ir datu īpašnieks un konteiners. Pārskatu var veikt jebkurā laikā, pat katru minūti (piemēram). Tas sniedz daudz papildu priekšrocību, piemēram, iespēju rādīt detalizēti visus uzņēmumus un dimensijas.

Lietotāji var izmantot tiešsaistes konsolidēšanas vai finanšu pārskatu sniegšanas iespēju, vai abas kopā. Izvēle ir atkarīga no lietotāju uzņēmuma vajadzībām un to auditoru preferencēm.

## <a name="consolidations"></a>Konsolidācija
**Konsolidācijas** modulis ietver opcijas vairāku juridisku personu konsolidēšanai konsolidācijas procesa laikā, un uzņēmuma bilances importēšanai vai eksportēšanai. Var arī iestatīt eliminācijas un grāmatot eliminācijas žurnālus.

## <a name="benefits-of-using-consolidate-online"></a>Konsolidēšanas tiešsaistē lietošanas priekšrocības
Klienti, kuri izmanto moduli **Konsolidācijas**, gūst dažādas tālāk minētās priekšrocības.

- **Datu dziļums** — var izveidot konsolidētus pārskatus, kas apvieno faktiskos un budžeta datus gan konta līmenī, gan dimensiju līmenī.
- **Dinamiskas konsolidācijas** — konsolidācijas var apstrādāt vairākas reizes.
- **Audita iespējas** — dimensijas un konti tiek uzturēti analīzei un auditam, un bilances tiek izveidotas pēc datuma.
- **Valūtas konvertācija** — var iestatīt kontu diapazonus un likmes, lai veiktu konvertāciju no izcelsmes uzņēmuma uzskaites valūtas uz konsolidēšanas uzņēmuma uzskaites valūtu.
- **Elimināciju apstrāde konsolidētā vai eliminācijas uzņēmumā** — var apstrādāt un grāmatot eliminācijas kā vienu procesu konsolidācijas laikā. Vai arī varat apstrādāt piedāvājumu atsevišķi.

## <a name="supported-consolidation-scenarios"></a>Atbalstīto konsolidāciju scenāriji
Tālāk aprakstīti daži konsolidēšanas tiešsaistē programmas atbalstītie konsolidācijas scenāriji.

- Viena līmeņa juridisko personu konsolidācijas
- Konsolidācijas, kas ietver eliminācijas
- Mazākuma līdzdalības daļa (šim scenārijam ir jāveic manuāls aprēķins un ieraksts uzņēmumā)
- Vairāki juridisko personu kontu plāni
- Dažādi finanšu kalendāri vairākām juridiskajām personām
- Konsolidācijas, kas ietver vairākas pārskata valūtas

## <a name="legal-entity-setup"></a>Juridiskas personas iestatīšana
Juridiskā persona ir jāiestata pirms konsolidāciju apstrādes. Konsolidāciju var veikt, cik vien reižu nepieciešams, un visi dati tiks konvertēti no izcelsmes uzņēmuma grāmatvedības valūtas uz valūtu, kas noteikta konsolidācijas uzņēmumam. Tāpēc tālāk norādītās organizatoriskās struktūras gadījumā, ja visiem Ziemeļamerikas uzņēmumiem vispirms ir jāveic pārrēķins uz ASV dolāriem (USD) un pēc tam uz eiro (EUR), kas ir mātes uzņēmuma valūta, ir jābūt vismaz diviem konsolidācijas uzņēmumiem.

![Organizācijas struktūra](./media/organizational-structure.png "Organizācijas struktūra")

Iepriekšējā organizatoriskajā struktūrā ir jābūt juridiskai personai Ziemeļamerikas konsolidācijai, jo konsolidācijas vienmēr konsolidē no izcelsmes uzņēmuma uzskaites valūtas uz konsolidācijas uzņēmuma valūtu. Šajā piemērā, ja visi uzņēmumi ir iekļauti vienā konsolidācijā, tad Meksikas filiālei tiks veikts pārrēķins no Meksikas peso (MXN) uz EUR, nevis no MXN uz USD uz EUR.

Veidojot juridisko personu, var norādīt, vai uzņēmums tiek izmantots gan konsolidācijas procesā, gan eliminācijas procesā, vai tikai vienā no minētajiem procesiem. Tālāk redzamajā piemērā uzņēmums tiek izmantots abiem procesiem. Ņemiet vērā, ka ikdienas žurnālus nevar grāmatot konsolidācijas uzņēmumā, bet tos var grāmatot eliminācijas uzņēmumā. Tāpēc ieteicams apsvērt atsevišķa eliminācijas uzņēmuma esamību.

![Juridiska persona, kas tiek izmantota gan konsolidācijai, gan dzēšanai](./media/sep-elimination-company.png "Juridiska persona, kas tiek izmantota gan konsolidācijai, gan dzēšanai")

## <a name="main-accounts-and-consolidation-account-groups"></a>Galvenie konti un konsolidācijas kontu grupas
Ir jāveic izvēle, kā jūs vēlaties konsolidēt savu kontu plānu. Konsolidācijas procesa laikā jums ir trīs galveno kontu konsolidēšanas iespējas.

Pirmā iespēja ir lietot galvenos kontus no izcelsmes uzņēmumiem. Šajā gadījumā tiks konsolidēti visu uzņēmumu visi konti. Piemēram, ja Kase ir konts 100000 USMF uzņēmumā un konts 1100 DEMF uzņēmumā, konsolidācijas uzņēmums ietvers abus kontus. Katram kontam būs sava attiecīga bilance.

Otrā iespēja ir norādīt noklusējuma konsolidācijas kontu lapā **Galvenie konti**. Šādā gadījumā konts tiks kartēts uz konsolidācijas kontu. Šī iespēja var būt noderīga, ja ir dažādi kontu plāni vai ir jākartē uz galvenās pārvaldes noteiktu plānu.

![Noklusējuma konsolidācijas konts, kas norādīts lapā Galvenie konti](./media/main-accounts.png "Noklusējuma konsolidācijas konts, kas norādīts lapā Galvenie konti")

Trešā iespēja ir izmantot konsolidācijas kontu grupas. Konsolidācijas kontu grupu skaitu var noteikt pēc nepieciešamības. Pēc tam lapā **Papildu konsolidācijas konti** tikai jākartē galvenais konts no kontu plāna uz kontu, kas nepieciešams šai grupai.

![Kartēšana lapā Papildu konsolidācijas pārskati](./media/additional-consolidation-accounts.png "Kartēšana lapā Papildu konsolidācijas pārskati")

## <a name="consolidating-online"></a>Konsolidācija tiešsaistē
Lai uzzinātu, kā ievadīt datus konsolidācijai tiešsaistē, skatiet sadaļu [Finanšu konsolidēšana tiešsaistē](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Konsolidācijas transakciju pārvaldīšana
Konsolidācijas rezultātu skatīšanai ir vairākas iespējas, kā norādīts tālāk.

- Izveidojiet finanšu pārskatu pret konsolidācijas uzņēmumu.
- Pārskatiet saraksta lapu **Apgrozījuma bilance** konsolidācijas uzņēmumā.
- Konsolidācijas transakciju sarakstā lapā **Konsolidācijas** skatiet bilances, kas tiek izveidotas pēc datuma katram izcelsmes uzņēmumam par katru periodu.

    ![Konsolidācijas darbības lapā Konsolidācija](./media/managing-consolidation-transactions.png "Konsolidācijas darbības lapā Konsolidācija")

Lai veiktu konsolidāciju vēlreiz, varat tikai apstrādāt konsolidāciju. Vai arī varat vispirms atlasīt vienumu **Noņemt transakcijas** lapā **Konsolidācijas**.
Ja bilances jūsu konsolidētajā kontā nav precīzas, šīs bilances var labot, izmantojot lapu **Slēgšanas perioda korekcijas**.

## <a name="consolidate-with-import"></a>Konsolidēt ar importēšanu
Funkcionalitāte Konsolidēt ar importu darbojas tāpat kā funkcionalitāte Konsolidēt tiešsaistē. Atlasot juridiskās personas, tiks pārlūkoti izcelsmes faili, kas satur datus.

## <a name="export-company-balances"></a>Eksportēt uzņēmuma bilances
Funkcionalitāte Eksportēt uzņēmuma bilances arī darbojas tāpat kā funkcionalitāte Konsolidēt tiešsaistē. Atlasot juridiskās personas, jāiestata faila ceļš rezultātam.

## <a name="elimination-rules"></a>Korekcijas kārtulas
Lai eliminētu starpuzņēmumu transakcijas, var izveidot eliminācijas kārtulu. Var arī veikt manuālu eliminācijas ierakstu uzņēmumā, kas ir noteikts kā eliminācijas uzņēmums. Izveidojot eliminācijas kārtulu, pastāv divas eliminācijas metodes iespējas: **neto izmaiņas** un **fiksēts**.

### <a name="set-up-elimination-rules"></a>Korekcijas noteikumu iestatīšana
Iestatot eliminācijas kārtulas programmā Finance, varat izveidot finanšu dimensiju, kas tiek izmantota tieši eliminācijas nolūkiem. Vairums klientu šai finanšu dimensijai piešķir nosaukumu **Darījumu partneris** vai tamlīdzīgu. Ja izlemjat kādu finanšu dimensiju nelietot, jums noteikti ir nepieciešami galvenie konti, kas tiek izmantoti tikai starpuzņēmumu transakcijām.

Elimināciju iestatījumi atrodami moduļa **Konsolidācijas** apgabalā **Iestatīšana**. Kad esat ievadījis kārtulas aprakstu, ir jāatlasa uzņēmums, uz kuru šis elimināciju žurnāls tiks grāmatots. Atlasītajam uzņēmumam juridiskās personas iestatījumos ir jābūt atlasītai opcijai **Lietot finanšu elimināciju procesā**.

Pēc nepieciešamības varat iestatīt datumu, kad eliminācijas kārtula stājas spēkā un datumu, kad tā beidzas. Ja vēlaties, lai eliminācijas kārtula būtu pieejama eliminācijas piedāvājuma procesā, tad opcija **Aktīvs** ir jāiestata uz **Jā**. Atlasiet žurnāla nosaukumu, kura tips ir **Eliminācija**.

![Dzēšanas kārtulas bāzes rekvizīti](./media/ledger-elimination-rule-journal.png "Dzēšanas kārtulas bāzes rekvizīti")

Kad pamatīpašības ir definētas, atlasiet **Rindas**, lai definētu faktiskās apstrādes kārtulas. Eliminācijai ir divas opcijas — var eliminēt neto izmaiņas summu vai definēt fiksētu summu.

Atlasiet avota kontus. Varat izmantot zvaigznīti (\*) kā aizstājzīmi. Piemēram, **1\*** kā sadalījuma datu avotu atlasa visus kontus, kas sākas ar **1**.

Kad ir atlasīti avota konti, izmantojiet lauku **Konta specifikācijas**, lai noteiktu kontu, ko izmanto no mērķa uzņēmuma. Atlasiet vērtību **Avots**, lai lietotu to pašu galveno kontu, kurš definēts avota kontā. Ja atlasāt vērtību **Lietotāja definēts**, jums ir jānorāda galamērķa konts.

![Virsgrāmatas korekcijas kārtulas rinda](./media/ledger-elimination-rule-line.png "Virsgrāmatas korekcijas kārtulas rinda")

Lauks **Dimensijas specifikācija** darbojas tāpat kā lauks **Konta specifikācija**. Atlasiet vērtību **Avots**, lai mērķa uzņēmumā un avota uzņēmumā lietotu tādas pašas dimensijas. Ja atlasāt vērtību **Lietotāja definēts**, tad jums ir jānorāda dimensijas mērķa uzņēmumā, atlasot **Mērķa dimensijas**. Pēc tam atlasiet avota dimensijas un finanšu dimensijas un vērtības, kuras tiek lietotas kā eliminācijas avots.

### <a name="process-elimination-transactions"></a>Korekcijas transakciju apstrāde
Ir divi veidi, kā apstrādāt eliminācijas transakcijas. Transakcijas var apstrādāt, kamēr notiek process Konsolidēt tiešsaistē, vai arī var izveidot elimināciju žurnālu un izpildīt elimināciju piedāvājuma procesu. Šajā sadaļā uzmanība vērsta uz otro opciju.

Uzņēmumā, kas ir definēts kā eliminācijas uzņēmums, atlasiet opciju **Eliminācijas žurnāls** modulī **Konsolidācijas**. Pēc žurnāla nosaukuma atlasīšanas atlasiet **Rindas**. Lai izpildītu piedāvājumu, atlasiet **Piedāvājumi** \> **Eliminācijas piedāvājums**.

Atlasiet uzņēmumu, kurš ir konsolidēto datu avots, un pēc tam atlasiet kārtulu, kuru apstrādāt. Ievadiet sākuma un beigu datumus, lai norādītu datumu diapazonu, kurā tiek meklētas eliminācijas summas. Lauks **VG grāmatošanas datums** norāda datumu, kurš tiek izmantots, lai žurnālu grāmatotu virsgrāmatā. Atlasot **Labi**, varat pārskatīt summas un grāmatot šo žurnālu.

> [!NOTE]
> Eliminācijas žurnāls parāda konta vērtību summas sākotnējā transakciju valūtā, nevis uzskaites valūtā. Pārskatot šīs summas eliminācijas žurnālā, šī rīcība varētu šķist neskaidra.

Plašāku informāciju un piemērus skatiet sadaļā [Eliminācijas kārtulas](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Valūtas pārvērtēšana konsolidācijas uzņēmumā
Veicot datu konsolidāciju no vienas norēķinu valūtas uz citu, joprojām jāizpilda valūtas pārvērtēšana, ja valūtas maiņas kursi mainās, lai jūsu konta bilances tiktu pareizi pārvērtētas. Sākotnēji konsolidējot datus, izmantojiet cilni **Valūtas pārrēķināšana**, lai atlasītu sākotnējos maiņas kursus, kuri jāizmanto pārrēķināšanai konsolidācijas procesa laikā. Pēc jaunā valūtas maiņas kursa ievadīšanas (piemēram, nākamajā mēnesī), nepieciešams pārvērtēt kontu bilances. Nerealizētā peļņa vai zaudējumi pēc tam tiek atjaunināta, pamatojoties uz jauno valūtas maiņas kursu un datumu.

Plašāku informāciju par valūtas pārvērtēšanu konsolidācijas uzņēmumā skatiet sadaļā [Valūtas pārvērtēšana konsolidācijas uzņēmumā](currency-revaluation-consolidation-company.md).

Plašāku informāciju par valūtas pārvērtēšanas darbību modulī **Virsgrāmata** moduli, skatiet sadaļu [Ārvalstu valūtas pārvērtēšana Virsgrāmatai](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Papildinformācija
- Visi grāmatošanas līmeņi tiek konsolidēti, apstrādājot konsolidāciju.
- Eliminācijas žurnālus var grāmatot tikai pašreizējā līmenī.
- Tiek konsolidētas tikai darbības bilances. Tādēļ, lai apskatītu sākuma bilances, joprojām jāizpilda gada beigu slēgšana konsolidācijas uzņēmumā.
- Ikdienas žurnālus varat grāmatot eliminācijas uzņēmumā, bet ne konsolidācijas uzņēmumā.
- Konsolidācijas uzņēmuma bilanču korekcijas var veikt tikai, izmantojot lapu **Slēgšanas perioda korekcijas**. 

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Priekšrocības, ko sniedz funkcijas Finanšu pārskatu sniegšana izmantošana finanšu konsolidācijām un valūtas pārrēķināšanai vai lai papildinātu funkciju Konsolidēt tiešsaistē konsolidēto pārskatu sniegšanai
Klienti, kuri izmanto funkciju Finanšu pārskati finanšu konsolidācijai un valūtas pārrēķināšanai vai lai papildinātu funkciju Konsolidēt tiešsaistē konsolidētajiem pārskatiem, gūst vairākas tālāk aprakstītās priekšrocības.

- **Datu dziļums** — var izveidot konsolidētus pārskatus, kas apvieno faktiskos un budžeta datus gan konta līmenī, gan dimensiju līmenī. Programmā Finance šie dati ietver datus gan no budžeta kontroles, gan no budžeta plānošanas.
- **Dinamiskās konsolidācijas** — konsolidācijas var veikt jebkurā laikā un jebkurā organizatoriskās hierarhijas līmenī.
- **Pilnīga audita iespējas** — visas dimensijas, konti un transakciju dati tiek uzturēti analīzei un auditam. Turklāt funkcija Finanšu pārskatu sniegšana nodrošina pilnīgu skatījumu uz sākotnējo transakciju jebkurai no konsolidētajām juridiskajām personām.
- **Racionalizēta valūtas pārrēķināšana** — pēc minimālā uzstādījuma programmā Finance jebkuru funkcijas Finanšu pārskatu veidošana pārskatu var pārrēķināt uzstādītajā pārskata valūtā. Turklāt jūs varat iestatīt neierobežotu pārskata valūtu skaitu.
- **Elimināciju grāmatošana izcelsmes vietā** — varat izveidot un izdrukāt eliminācijas pārskatu, lai pārbaudītu eliminācijas transakcijas. Pēc tam varat grāmatot jaunas eliminācijas kā standarta starpuzņēmumu transakcijas. Varat arī izmantot eliminācijas juridisko personu jebkurai transakcijai, kuru nevēlaties savās juridiskajās personās.

## <a name="supported-consolidation-scenarios"></a>Atbalstīto konsolidāciju scenāriji
Tālāk aprakstīti daži programmas Finanšu pārskatu sniegšana atbalstītie konsolidācijas scenāriji.

- Viena līmeņa un vairāku līmeņu juridisko personu konsolidācijas
- Konsolidācijas, kas izmanto organizācijas struktūras, kas izveidotas no juridiskām personām
- Konsolidācijas, kas ietver eliminācijas
- Mazākuma līdzdalības daļa
- Vairāki juridisko personu kontu plāni
- Dažādi finanšu kalendāri vairākām juridiskajām personām
- Konsolidācijas, kas ietver vairākas pārskata valūtas
- Biznesa vienības konsolidācijas

## <a name="generating-consolidated-financial-statements"></a>Konsolidēto finanšu pārskatu ģenerēšana
Informāciju par scenārijiem, kuros varētu veidot konsolidētos finanšu pārskatus, skatiet sadaļu[Konsolidēto finanšu pārskatu veidošana](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]