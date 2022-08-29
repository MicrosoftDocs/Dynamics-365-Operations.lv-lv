---
title: PVN deklarācija (Dānija)
description: Šajā rakstā ir aprakstīts, kā iestatīt un ģenerēt papildu pievienotās vērtības nodokļa (PVN) deklarāciju Dānijai.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: a47b2b98d86daf50876c783f879362ec1addb579
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272146"
---
# <a name="vat-declaration-denmark"></a>PVN deklarācija (Dānija)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iestatīt pievienotās vērtības nodokļa (PVN) deklarāciju Dānijai un priekšskatīt to Microsoft Excel.

Lai pārskatu ģenerētu automātiski, vispirms izveidojiet pietiekamu PVN kodu, lai saglabātu atsevišķu PVN uzskaiti katrai izvēles rūtiņai avansa PVN deklarācijā. Turklāt elektronisko pārskatu (ER) formāta, kas paredzēts avansa PVN deklarācijai, konkrētos pieteikuma parametros PVN kodi tiek asociēti ar uzmeklēšanas rezultātu meklēšanas rezultātiem PVN deklarācijas lodziņiem.

Dānijā jums ir jākonfigurē pārskata **lauka pārlūkošana**. Papildinformāciju par to, kā iestatīt programmai raksturīgos parametrus, [skatiet tālāk šī raksta sadaļā Iestatīt lietojumprogrammai raksturīgos parametrus PVN](#set-up-application-specific-parameters) deklarācijas laukiem.

Šajā tabulā kolonna "Meklēšanas rezultāts" parāda uzmeklēšanas rezultātu, kas ir iepriekš konfigurēts noteiktai PVN deklarācijas rindai PVN deklarācijas formātā. Izmantojiet šo informāciju, lai pareizi saistītu PVN kodus ar uzmeklēšanas rezultātu un tad ar PVN deklarācijas rindu.

### <a name="vat-declaration-overview"></a>PVN deklarācijas apskats

PVN deklarācija Dānijā satur šādu informāciju.

**Maksājamais VAT**

| Apraksts                                                  | Nodokļa bāze/nodokļa summa | Uzmeklēšanas rezultāts/kopsumma                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pārdošanas PVN                                                   | Nodokļa summa          | **IzvadesVAT**</br> **DomesticVATUseTax** (iekļauts arī lodziņā "Ievades PVN")                                                                                                                                                                                                                                                                       |
| Preču PVN u.c. Iegādāts ārvalstīs                           | Nodokļa summa          | **PirkšanasgoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** (iekļauts arī lodziņā "Ievades PVN")</br>**PurchaseGoodsEU** (nodokļu bāze ir ziņota "Lodziņā A — preču iegāde".)</br>**PurchaseGoodsEUUseTax** (nodokļu summa arī ir ziņota lodziņā "Ievades PVN". Nodokļa bāze ir ziņota "A kaste - preču iegāde".                   |
| PVN par pakalpojumiem, kuri iegādāti ārvalstīs un uz kuriem attiecas apgrieztais maksājums | Nodokļa summa          | **Pirkšanas pakalpojumiAbroad**</br> **PurchaseServicesAbroadUseTax** (iekļauts arī lodziņā "Ievades PVN")</br>**PurchaseServicesEU** (nodokļu bāze ir uzrādīta "A lodziņā - pakalpojumu iegāde".)</br>**PurchaseServicesEUUseTax** (pvn summa arī ir ziņota lodziņā "Ievades PVN". Nodokļu bāze ir ziņota "A. lodziņā — pakalpojumu iegāde". |
| Kopā kreditors                                                | Nodokļa summa          | Iepriekšējo trīs lodziņu kopsumma                                                                                                                                                                                                                                                                                                            |

**Ieturējumi**

| Apraksts                                                                               | Nodokļa bāze/nodokļa summa | Uzmeklēšanas rezultāts/kopsumma                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pirkšanas PVN                                                                                 | Nodokļa summa          | **InputVAT (vat)**</br> **DomesticVATUseTax** (iekļauts arī lodziņā "Izvades PVN")</br>**PurchaseGoodsAbroadUseTax** (iekļauts arī "Preču PVN u.c." Iegādāts ārzemju", kastē)</br>**PurchaseServicesAbroadUseTax** (iekļauts arī "PVN par ārvalstīs iegādātajiem pakalpojumiem, uz ko attiecas atgriezeniskā maksa" lodziņā)</br>**PurchaseGoodsEUUseTax** (iekļauts arī "Preču PVN u.c." Iegādāts ārzemju", kastē)</br> **PurchaseServicesEUUseTax** (iekļauts arī "PVN par ārvalstīs iegādātajiem pakalpojumiem, uz ko attiecas atgriezeniskā maksa" lodziņā) |
| Naftas un balonu gāzes nodoklis                                                                  | Nodokļa summa          | **NaftaGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Dabasgāzes un koksa gāzes nodoklis                                                             | Nodokļa summa          | **NaturalLotGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Oglekļa nodoklis                                                                               | Nodokļa summa          | **Varmācība**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Co2Duty                                                                                   | Nodokļa summa          | **Co2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Maksa par ūdeni                                                                              | Nodokļa summa          | **Scharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Ieturējumu kopsumma                                                                          | Nodokļa summa          | Iepriekšējo sešu lodziņu kopsumma                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Kopējā nodokļu summa (pozitīva summa = veikt maksājumu, negatīva summa = saņemt atmaksu) | Nodokļa summa          | "Kopā jāmaksā" — "Kopējie ieturējumi"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Papildinformācija**

| Apraksts                                                                                                                                                                                                                                | Nodokļa bāze/nodokļa summa | Uzmeklēšanas rezultāts/kopsumma                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| A lodziņš — preču iegāde. Vērtība bez PVN par preču iegādi Eiropas Kopienas teritorijā.                                                                                                                                                   | Nodokļu bāzes vērtība            | **PurchaseGoodsEU PirkšanasgoodsEUUseTax**       |
| A lodziņš — pakalpojumu iegāde. Pakalpojumu iekšējās iegādes vērtība bez PVN.                                                                                                                                             | Nodokļu bāzes vērtība            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| B kaste - preču piegāde - pārskatā "ES pārdošana bez PVN"/DK VIES. Vērtība bez PVN par preču piegādi Eiropas Kopienas teritorijā                                                                                                           | Nodokļu bāzes vērtība            | **PārdošanaGoodsEU**                                |
| Kaste B - piegādes - nav jāziņo "ES tirdzniecība bez PVN"/DK VIES. Atsevišķu ar nodokli neapliekamo piegāžu, piemēram, transportlīdzekļu, montāžas, attāluma pārdošanas un jaunu transporta veidu, kas nav apliekami ar nodokli, vērtība bez PVN. | Nodokļu bāzes vērtība            | **SalesInstallationAssemblyEtcEU**              |
| B kaste – pakalpojumu piegāde. Vērtība bez PVN par preču piegādēm Eiropas Kopienas teritorijā, par kuru pircējs ir atbildīgs kā atgriezeniskas maksas pvn maksājums— ir jāziņo arī "ES tirdzniecība bez PVN"/DK VIES.                          | Nodokļu bāzes vērtība            | **Pārdošanas pakalpojumuEU**                             |
| C kaste — citas piegādes. Citu preču un pakalpojumu piegādes vērtība, kas tiek piegādāta bez PVN Dānijas teritorijā, uz citām ES dalībvalstīm un trešajām valstīm vai trešajām teritoriju.                                     | Nodokļu bāzes vērtība            | **CitiappliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Pirkšanas atgrieztās maksas PVN

Ja konfigurējat PVN kodus ienākošās atgriezeniskās PVN grāmatošanai, izmantojot izmantošanas nodokli, **saistiet** pvn kodus ar pārskata lauka uzmeklēšanas rezultātu, kas nosaukumā satur "UseTax".

Alternatīvi var konfigurēt divus atsevišķus PVN kodus: vienu apmaksas PVN un vienu PVN ieturējumiem. Pēc tam saistiet katru kodu ar atbilstošajiem pārskata lauka uzmeklēšanas **rezultātiem**.

Piemēram, ar nodokli apliekamām kopienas iegādēm jūs konfigurējat PVN kodu UT_S_EU ar importa nodokli un saistāt to ar pārskata lauka uzmeklēšanas **rezultātu PurchaseGoodsEUUseTax** **·**.**·** Šajā gadījumā nodokļu summas, kas izmanto UT_S_EU **PVN** kodu, tiek attēlotas sadaļā "Preču PVN u.c. Iegādāts ārvalstīs" un "Ievades PVN". Nodokļu bāzes parādītas "A lodziņā - preču iegādē".

Alternatīvi var konfigurēt divus PVN kodus:

- **VAT_S_EU**, kuras nodokļa likmes vērtība ir -25 procenti
- **InVAT_S_EU**, kuras nodokļa likme ir 25 procenti

Pēc tam jūs saistāt kodus ar pārskata **lauku uzmeklēšanas** rezultātiem šādā veidā:

- Saistiet **VAT_S_EU** ar **uzmeklēšanas rezultātu PurchaseGoodsEU**.
- Saistiet **InVAT_S_EU** ar **InputVAT uzmeklēšanas** rezultātu.

Šajā gadījumā summas, kas izmanto VAT_S_EU **PVN** kodu, tiek attēlotas sadaļā "Preču PVN u.c. Iegādāts ārzemju" kastē un "A kaste - preču iegāde". Summas, kas izmanto **InVAT_S_EU** PVN kodu, tiek parādītas lodziņā "Ievades PVN".

Papildinformāciju par to, kā konfigurēt atgriezeniskos PVN maksājumus, skatiet sadaļā Apgrieztās [maksas](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Sistēmas parametru konfigurēšana

Lai ģenerētu PVN deklarāciju, ir jākonfigurē PVN numurs.

1. Pārejiet uz sadaļu **Organizācijas administrēšana** > **Organizācijas** > **Juridiskās personas**.
2. Atlasiet juridisko personu un pēc tam **atlasiet reģistrācijas identifikators**.
3. Atlasiet vai izveidojiet adresi Dānijā un pēc tam reģistrācijas **ID kopsavilkuma cilnē** atlasiet **Pievienot**.
4. Laukā **Reģistrācijas tips** atlasiet reģistrācijas tipu, kas atvēlēts Dānijai un kas izmanto **PVN ID** reģistrācijas kategoriju.
5. Laukā **Reģistrācijas** numurs ievadiet nodokļa numuru.
6. Cilnes Vispārīgi **laukā** Darbības sākums **ievadiet** datumu, kad skaitlis stājas spēkā.

Papildinformāciju par to, kā iestatīt reģistrācijas kategorijas un reģistrācijas tipus, skatiet [reģistrācijas tipiem](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Iestatīt PVN deklarācijas priekšskatījumu Dānijai

### <a name="import-er-configurations"></a>ER konfigurāciju importēšana

Atveriet elektronisko **pārskatu darbvietu** un importējiet **PVN deklarācijas Excel (DK)** ER formātu.

Plašāka informācija pieejama rakstā [Elektronisko pārskatu (ER) konfigurāciju lejupielāde no konfigurācijas pakalpojuma globālā repozitorija](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a> Iestatīt pieteikumu parametrus PVN deklarācijas laukiem

> [!NOTE]
> Ieteicams iespējot šo līdzekli. Izmantojiet programmai raksturīgos **parametrus no iepriekšējām ER formātu versijām** līdzekļu **pārvaldības darbvietā**. Kad šī funkcija ir aktivizēta, parametri, kas konfigurēti agrākai ER formāta versijai, automātiski kļūst piemērojami vēlākai tā paša formāta versijai. Ja šī funkcija nav iespējota, programmai raksturīgie parametri ir jākonfigurē tikai katrai formāta versijai. Funkcija **Izmantot programmai raksturīgos parametrus no iepriekšējām ER** **formātu** līdzekļa versijām ir pieejama līdzekļu pārvaldības darbvietā, kas sākas finanšu versijā 10.0.23. Papildinformāciju par to, kā iestatīt ER formāta parametrus katrai juridiskajai personai, [skatiet ER formāta parametru iestatīšana juridiskajai personai](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Lai automātiski ģenerētu PVN deklarāciju, saistiet PROGRAMMĀ PVN kodus un uzmeklēšanas rezultāti tiks izveidoti ER konfigurācijā.

Sekojiet šiem soļiem, lai noteiktu, kuri PVN kodi ģenerē tos laukus PVN deklarācijā.

1. Dodieties uz **darbalauku** > **elektronisko** pārskatu sniegšanu un atlasiet **Pārskatu izveides konfigurācijas**.
2. Atlasiet PVN **deklarācijas Excel (DK)** konfigurāciju un pēc tam atlasiet konfigurācijas **programmai \> noteiktu parametru iestatījumu**.
3. Lapā Programmai **specifiskie parametri** kopsavilkuma **cilnē Pārlūki** atlasiet Pārskata **lauka uzmeklēšanu**.
4. Kopsavilkuma cilnē **Nosacījumi** iestatiet tālāk norādītos laukus, lai saistītu PVN kodus un pārskata laukus.

    | Lauks                  | Apraksts                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Uzmeklēšanas rezultāts          | Atlasiet pārskata lauka vērtību. Papildinformāciju par vērtībām un to piešķiršanu PVN deklarācijas rindām skatiet šī [raksta](#vat-declaration-overview) iepriekšējā PVN deklarācijas pārskata sadaļā.                                                                                               |
    | Nodokļa kods               | Atlasiet PVN kodu, ko saistīt ar pārskata lauku. Grāmatotās nodokļu darbības, kas izmanto atlasīto PVN kodu, tiks savāktas atbilstošajā deklarācijas lodziņā. Ieteicams atdalīt PVN kodus tā, lai viens PVN kods ģenerētu summas tikai vienā deklarācijas lodziņā. |
    | Transakcijas klasifikators | Ja izveidojāt pietiekamus PVN kodus deklarācijas lodziņa noteikšanai, atlasiet Nav **\* tukšs\***. Ja netiek izveidoti pietiekami daudz PVN kodu, lai viens PVN kods ģenerētu summas tikai vienā deklarācijas lodziņā, varat iestatīt transakcijas klasifikatoru. Ir pieejami šādi darbību klasifikatori:</br>-   **Pirkšana**</br>-   **PurchaseExempt** (pirkšana ar nodokli neapliekamā summa)</br>-   **PurchaseReverseCharge** (no pirkšanas apgrieztās maksas saņemamajiem nodokļiem)</br>-   **Pārdošana**</br>-   **SalesExempt** (ar nodokli neapliekamā pārdošana)</br>-   **SalesReverseCharge** (maksājamie nodokļi no pirkšanas atgriezes maksas vai pārdošanas atgriezeniskās maksas)</br>-   **Izmantošanas nodoklis**. </br>Katram transakcijas klasifikatoram ir pieejams arī kredīta notas klasifikators. Piemēram, viens no šiem klasifikatori ir **PurchaseCreditNote** (pirkšanas kredīta nota).</br>Pārliecinieties, vai katram PVN kodam ir jāizveido divas rindas: viena, kam ir transakcijas klasifikatora vērtība, un viena ar transakcijas klasifikatoru kredīta notas vērtībai. |


    > [!NOTE]
    > Visus PVN kodus saistīt ar uzmeklēšanas rezultātiem. Ja jebkuriem PVN kodiem nav jāģenerē vērtības PVN deklarācijā, saistiet tos ar citiem **uzmeklēšanas** rezultātiem.

    ![Programmai specifisku parametru lapa.](media/7db74920fad66a0db7fad60758698cc0.png)


5. Laukā **Stāvoklis** mainiet vērtību uz **Pabeigts**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Iestatiet PVN pārskata formātu summu priekšskatījumam programmā Excel

1. Līdzekļu pārvaldības **darbvietā** atrodiet un atlasiet PVN **deklarācijas formāta pārskatus.** Sarakstā līdzekli <a0/& un pēc tam atlasiet **Iespējot tagad**.
2. Dodieties uz **Virsgrāmatas** > **iestatījumu** > **Virsgrāmatas parametriem**.
3. Cilnes PVN **kopsavilkuma** **·** **cilnes Nodokļu opcijas laukā PVN** **deklarācijas formāta kartēšana atlasiet PVN deklarācijas Excel (DK)** ER formātu.

   Šis formāts tiek drukāts, kad darbināt pārskatu **par PVN maksājumu perioda pārskatam**. To var drukāt arī tad, ja PVN **maksājumu** lapā **atlasāt** Drukāt.

4. **Lapā Nodokļu iestādes** atlasiet nodokļu iestādi un pēc tam laukā Pārskata izkārtojums **atlasiet** Noklusējuma **·**.

Ja jūs konfigurējat PVN deklarāciju juridiskajā persona, kam ir vairākas [PVN reģistrācijas](emea-reporting-for-multiple-vat-registrations.md), sekojiet šiem soļiem.

1. Dodieties uz **Virsgrāmatas** \> **iestatījumu** \> **Virsgrāmatas parametriem**.
2. **Cilnē PVN** **kopsavilkuma cilnes Elektroniskie pārskati valstīm/** reģioniem **DNK** **rindā atlasiet PVN deklarācijas Excel (DK)** ER formātu.

## <a name="set-up-electronic-messages"></a>Iestatīt elektroniskos ziņojumus

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Lejupielādēt un importēt datu pakotni, kam ir elektronisko ziņojumu iestatījumu piemērs

Datu pakotne ietver elektroniskā ziņojuma iestatījumus, kas tiek izmantoti PVN deklarācijas priekšskatšanai programmā Excel. Šos iestatījumus var paplašināt vai izveidot pats. Papildinformāciju par to, kā strādāt ar elektronisko ziņapmaiņu un izveidot savus iestatījumus, skatiet sadaļā [Elektroniskā ziņojumapmaiņa](../general-ledger/electronic-messaging.md).

1. Programmas [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2)**koplietoto** līdzekļu bibliotēkā atlasiet Datu pakotni kā līdzekļu veidu un pēc tam lejupielādējiet **DK PVN deklarācijas pakotni.** Lejupielādētais fails tiek nosaukts **DK PVN deklarācijas package.zip**.
2. Finanšu sadaļā Datu pārvaldības **darbvieta** atlasiet **Importēt**.
3. **Kopsavilkuma cilnes** Imports laukā **Grupas nosaukums** ievadiet darba nosaukumu.
4. Kopsavilkuma cilnē **Atlasītās entītijas** atlasiet **Pievienot failu**.
5. Dialoglodziņā Pievienot **failu pārbaudiet**, **·** **vai** avota datu formāta lauks ir iestatīts uz Pakot, **atlasiet** Augšupielādēt un pievienojiet un pēc tam atlasiet agrāk lejupielādēto zip failu.
6. Atlasiet **Aizvērt**.
7. Kad datu elementi ir augšupielādēti, darbību rūtī atlasiet **Importēt**.
8. Dodieties uz **nodokļu pieprasījumiem un** > **pārskatiem Elektronisko** > **ziņojumu elektroniskie** > **ziņojumi un apstipriniet importēto elektronisko ziņojumu apstrādi (** DK PVN **deklarācija**).

### <a name="configure-electronic-messages"></a>Konfigurēt elektroniskos ziņojumus

1. Doties uz nodokļu **iestatīšanas** > **·** > **elektroniskajiem ziņojumiem** > **Aizpildīt ierakstu darbības**.
2. Atlasiet dk rindu, lai **aizpildītu PVN atgriešanas ierakstus**, un pēc tam atlasiet **Rediģēt vaicājumu**.
3. Izmantojiet filtru, lai norādītu segšanas periodus, ko iekļaut pārskatā.
4. Ja pārskats par nodokļu darbībām no citiem segšanas periodiem jāsniedz citā deklarācijā, **izveidojiet jaunu aizpilda ierakstu** darbību un atlasiet atbilstošos apmaksas periodus.

## <a name="preview-the-vat-declaration-in-excel"></a>Priekšskatīt PVN deklarāciju programmā Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a> Priekšskatīt PVN deklarāciju programmā Excel no pārskata PVN par nosegšanas perioda periodisko uzdevumu

1. Doties uz **nodokļu** > **periodiskajiem** > **uzdevumiem.** > **Deklarācijas PVN** > **pārskats par PVN maksājumu periodam**.
2. Laukā **Apmaksas** periods atlasiet vērtību.
3. Laukā **PVN maksājuma versija** atlasiet vienu no šīm vērtībām:

    - **Oriģināls**: izveidojiet pārskatu oriģinālā PVN maksājuma PVN darbībām vai pirms PVN maksājuma ģenerēšanas.
    - **Labojumi**: ģenerējiet pārskatu par visu turpmāko PVN maksājumu PVN darbībām par periodu.
    - **Kopējais saraksts**: ģenerēt pārskatu par visām PVN darbībām par periodu, ieskaitot oriģinālos un visus labojumus.

4. **Laukā No** datuma atlasiet pārskata perioda sākuma datumu.
5. Atlasiet **Labi**, un pārskatiet Excel pārskatu.

### <a name="settle-and-post-sales-tax"></a>Nosegt un grāmatot PVN

1. Doties uz **periodiskajiem** > **nodokļu** > **uzdevumiem, deklarācijas** > **par PVN** > **maksājumu un PVN iegrāmatošanu**.
2. Laukā **Apmaksas** periods atlasiet vērtību.
3. Laukā **PVN maksājuma versija** atlasiet vienu no šīm vērtībām:

    - **Oriģināls**: ģenerējiet maksājuma perioda sākotnējo PVN maksājumu.
    - **Pēdējie labojumi**: ģenerēt PVN labojuma maksājumu pēc tam, kad maksājuma periodam tika izveidots sākotnējais PVN maksājums.

4. **Laukā No** datuma atlasiet pārskata perioda sākuma datumu.
5. Atlasiet **Labi**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Priekšskatīt PVN deklarāciju programmā Excel no PVN maksājuma

1. Dodieties **uz** > **nodokļu vaicājumiem un** > **pārskatiem par** > **PVN pieprasījumiem** par PVN maksājumiem un atlasiet PVN maksājuma rindu.
2. Atlasiet **Drukāt pārskatu** un pēc tam atlasiet **Labi**.
3. Pārskatiet Excel failu, kas tiek ģenerēts atlasītajai PVN maksājuma rindai.

> [!NOTE]
> Pārskats tiek ģenerēts tikai atlasītajai PVN maksājuma rindai. Ja jums jāģenerē, piemēram, labojoša deklarācija, kas ietver visus perioda labojumus, vai aizstājējdeklarācija, kurā ietverti sākotnējie dati un visi labojumi, **izmantojiet** pārskata PVN maksājumu perioda periodiskajam uzdevumam.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Ģenerējiet PVN deklarāciju no elektroniskajiem ziņojumiem

Kad izmantojat elektroniskos ziņojumus, lai ģenerētu pārskatu, varat apkopot nodokļu datus no vairākām juridiskām personām. Papildinformāciju skatiet tālāk [šī raksta sadaļā Vairāku juridisko personu sadaļu](#run-vat-declaration) PVN deklarācijas palaišana.

Šī procedūra attiecas uz elektronisko ziņojumu apstrādes piemēru, ko iepriekš importjāt no LCS koplietojamās līdzekļu bibliotēkas.

1. Dodieties uz nodokļu **\> vaicājumiem un pārskatiem \> Elektroniskie \> ziņojumi**.
2. Kreisajā rūtī atlasiet **DK PVN deklarāciju**.
3. Kopsavilkuma cilnē **Ziņojumi** atlasiet Jauns **un** pēc tam dialoglodziņā **Palaist apstrādi** atlasiet **Labi**.
4. Atlasiet izveidoto ziņojuma rindu, ievadiet aprakstu un pēc tam norādiet deklarācijas sākuma un beigu datumus.

   > [!NOTE]
   > No 5. līdz 7. solim nav obligāti.

5. Nav obligāti: kopsavilkuma **cilnē** Ziņojumi atlasiet Apkopot **datus un** pēc tam atlasiet **Labi**. Iepriekš izveidotie PVN maksājumi tiek pievienoti ziņojumam. Papildinformāciju skatiet šī raksta [sadaļā PVN sadaļā](#settle-and-post-sales-tax) Nosegt un grāmatot. Ja izlaidīsiet šo soli, jūs joprojām varat ģenerēt **PVN deklarāciju, izmantojot nodokļu** deklarācijas versijas lauku **deklarācijas** dialoglodziņā.
6. Nav obligāti: kopsavilkuma **cilnē Ziņojumu** krājumi pārskatiet PVN maksājumus, kas tiek pārsūtīti apstrādei. Pēc noklusējuma tiek iekļauti visi atlasītā perioda PVN maksājumi, kas netika iekļauti citā tā paša apstrādes ziņojumā.
7. Nav obligāti: atlasiet **Oriģinālais** dokuments, lai pārskatītu PVN maksājumus, **vai** atlasiet Dzēst, lai izslēgtu PVN maksājumus no apstrādes. Ja izlaidīsiet šo soli, jūs joprojām varat ģenerēt **PVN deklarāciju, izmantojot nodokļu** deklarācijas versijas lauku **deklarācijas** dialoglodziņā.
8. Kopsavilkuma cilnē **Ziņojumi** atlasiet statusu **Atjaunināt**. Dialoglodziņā Atjaunināšanas **statuss** atlasiet Gatavs **ģenerēšanu un** pēc tam atlasiet **Labi**. Pārbaudiet, vai ziņojuma statuss ir mainīts uz **Gatavs ģenerēšanas uzdevumam**.
9. Atlasiet **Ģenerēt pārskatu**. Lai priekšskatītu PVN deklarācijas summas, dialoglodziņā **Palaist apstrādi atlasiet Priekšskatīt** pārskatu **un pēc** tam atlasiet **Labi**.
10. Dialoglodziņā Elektronisko **pārskatu** parametri iestatiet laukus tā, [kā tas ir aprakstīts PVN deklarācijas priekšskatīšanas programmā Excel](#preview-vat-excel) no atskaites PVN par nosegšanas perioda periodisko uzdevumu sadaļu, kā arī pēc tam atlasiet **Labi**.
11. Atlasiet lapas **augšējā** labajā stūrī pogu Pielikumi (papīra sagriešanas simbols) un pēc tam atlasiet **Atvērt**, lai atvērtu failu. Pārskatiet summas Excel dokumentā.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a> Palaist PVN deklarāciju vairākām juridiskām personām

Lai lietotu formātus, lai iesniegtu pārskatu par PVN deklarāciju juridisko personu grupai, vispirms ir jāiestata ER formātu programmai raksturīgie parametri PVN kodiem no visām juridiskajām personām.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Iestatīt elektroniskos ziņojumus, lai apkopotu nodokļu datus no vairākām juridiskām personām

Sekojiet šiem soļiem, lai iestatītu elektroniskos ziņojumus, lai savāktu datus no vairākām juridiskajām personām.

1. Pārejiet uz **sadaļu Darbalauku** > **līdzekļu pārvaldība**.
2. Atrodiet un atlasiet starpuzņēmumu **vaicājumus aizpildīto ierakstu darbību līdzeklim** sarakstā un pēc tam atlasiet Aktivizēt **tagad**.
3. Doties uz nodokļu **iestatīšanas** > **·** > **elektroniskajiem ziņojumiem** > **Aizpildīt ierakstu darbības**.
4. Darbības lapā **Aizpildīt ierakstus atlasiet** rindu DK aizpildīt **PVN atgriešanas ierakstiem**.

   **Datu avotu iestatījumu** režģī ir pieejams jauns **uzņēmuma** lauks. Esošiem ierakstiem šajā laukā tiek rādīts pašreizējās juridiskās personas identifikators.

5. Datu avotu **iestatījumu režģī** pievienojiet rindu katrai papildu juridiskajai personai, kas ir jāiekļauj pārskatā. Katrai jaunai rindai iestatiet šādus laukus.

    | Lauks                  | Apraksts                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Vārds/nosaukums                   | Ievadiet vērtību, kas palīdzēs saprast, no kurienes ir šis ieraksts. Piemēram, ievadiet **PVN maksājumu 1. filiālē**. |
    | Ziņojuma krājuma veids      | Atlasiet **PVN atgriešanu**. Šī vērtība ir vienīgā vērtība, kas pieejama visiem ierakstiem.                                    |
    | Konta veids           | Atlasiet **visu**.                                                                                                               |
    | Galvenās tabulas nosaukums      | Norādiet **TaxReportVoucher** visiem ierakstiem.                                                                             |
    | Dokumenta numura lauks  | **Norādīt** dokumentu visiem ierakstiem.                                                                                      |
    | Dokumenta datuma lauks    | Norādiet **TransDate** visiem ierakstiem.                                                                                    |
    | Dokumenta konta lauks | Visiem **ierakstiem norādiet TaxPeriod**.                                                                                    |
    | Uzņēmums                | Atlasiet juridiskās personas ID.                                                                                            |
    | Lietotāja vaicājums             | Šī izvēles rūtiņa tiek automātiski atzīmēta, kad definējat kritērijus, atlasot **Vaicājumu Labot**.                                 |

6. Katrai jaunai rindai atlasiet **vaicājumu** Rediģēt un norādiet **juridiskās personas saistīto segšanas periodu, kas ir norādīts** rindas laukā Uzņēmums.

Kad iestatīšana ir pabeigta, lapā **·** **Elektroniskie** ziņojumi datu apkopošanas funkcija apkopo PVN maksājumus no visām juridiskajām personām, ko esat definējis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
