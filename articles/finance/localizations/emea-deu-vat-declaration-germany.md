---
title: PVN deklarācija (Vācija)
description: Šajā tēmā ir aprakstīts, kā iestatīt un ģenerēt papildu pievienotās vērtības nodokļa (PVN) deklarāciju Vācijai oficiālajā XML formātā.
author: anasyash
ms.date: 11/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 29c04e1034c05b4672f3657ce0b7bc9d5f6d7c9c
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860868"
---
# <a name="vat-declaration-germany"></a>PVN deklarācija (Vācija)

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt un ģenerēt papildu pievienotās vērtības nodokļa (PVN) deklarāciju Vācijai oficiālajā XML formātā. Šajā tēmā skaidrots arī, kā priekšskatīt PVN deklarāciju Microsoft Excel.

Lai pārskatu ģenerētu automātiski, izveidojiet pietiekamus PVN kodus, lai saglabātu atsevišķu PVN uzskaiti katrai izvēles rūtiņai avansa PVN deklarācijā. Turklāt elektronisko pārskatu (ER) formāta, kas paredzēts avansa PVN deklarācijai, konkrētos pieteikuma parametros PVN kodi tiek asociēti ar uzmeklēšanas rezultātu meklēšanas rezultātiem PVN deklarācijas lodziņiem.

Vācijai ir jākonfigurē **pārskata lauka pārlūkošana**. Papildinformāciju par to, kā iestatīt programmai raksturīgos parametrus, skatiet tālāk šīs tēmas sadaļā Iestatīt lietojumprogrammai raksturīgos parametrus [PVN](#set-up-application-specific-parameters-for-vat-declaration-fields) deklarācijas laukiem.

Šajā tabulā kolonna "Meklēšanas rezultāts" parāda uzmeklēšanas rezultātu, kas ir iepriekš konfigurēts noteiktai PVN deklarācijas rindai PVN deklarācijas formātā. Izmantojiet šo informāciju, lai pareizi saistītu PVN kodus ar uzmeklēšanas rezultātu un tad ar PVN deklarācijas rindu.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a> PVN deklarācijas apskats

Avansa PVN deklarācijā Vācijā ir šāda informācija.

**SADAĻA – PIEGĀDES UN CITI PAKALPOJUMI**

**Ar PVN apliekamā tirdzniecība**

| Rinda | Kaste - nodokļa bāze | Kaste - nodokļa summa | Apraksts                                                                                                                                      | Uzmeklēšanas rezultāts                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Bez koda     | Ar nodokli apliekamā pārdošana ar nodokļa likmi 19 procenti.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – ar mīnus zīmi             |
| 21  | 86             | Bez koda     | Ar nodokli apliekamā pārdošana ar nodokļa likmi 7 procenti.                                                                                                        | 21 — Ar nodokli apliekamās pārdošanasreturā</br>73-BadDebtsWriteOffRerite (86/50) – ar mīnus zīmi               |
| 22  | 35             | 36               | Ar nodokli apliekamā pārdošana ar citām nodokļu likmēm.                                                                                                                | 22 — TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – ar mīnusa zīmi      |
| 23  | 77             | *Nav nodokļa summas*  | Saskaņā ar Vācijas PVN akta (UStG) 24. panta piegādes debitoriem ar PVN ID numuru. | 23— EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) — ar mīnusa zīmi |
| 24  | 76             | 80               | Pārdošana, par kuru jāmaksā nodoklis saskaņā ar UStG 24. krājumu (neproduktīviem, dzērienu un vājamiem šķidruma).                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Ar nodokļiem neapliekama tirdzniecība ar priekšnodokļa ieturējumu**

| Rinda | Kaste - nodokļa bāze | Kaste - nodokļa summa | Apraksts                                                                       | Uzmeklēšanas rezultāts                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Nav nodokļa summas*  | Intra-Community piegādes debitoriem ar PVN ID.                       | 26-EUSales                          |
| 27  | 44             | *Nav nodokļa summas*  | Jaunu transportlīdzekļu iekšējās piegādes pircējiem, kam nav PVN ID.    | 27-EUSalesNewVeges               |
| 28  | 49             | *Nav nodokļa summas*  | Iekšējo transportlīdzekļu piegādes ārpus uzņēmuma.                     | 28–EUSalesNewVesidelesOutsideCompany |
| 29  | 43             | *Nav nodokļa summas*  | Cita ar nodokli ne atbrīvojamā pārdošana, kas ietur ievades nodokļa ieturējumu, piemēram, eksporta piegādes. | 29— ExportOtherTaxFreeSales          |

**Ar nodokļiem neapliekama tirdzniecība bez priekšnodokļa ieturējuma**

| Rinda | Kaste - nodokļa bāze | Kaste - nodokļa summa | Apraksts                                            | Uzmeklēšanas rezultāts                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Nav nodokļa summas*  | Pārdošana bez nodokļiem, kam nav ieturējuma nodokļa. | 30— TaxFreeSalesWithoutInputTaxDeduction |

**INTRA-Community iegāde**

| Rinda | Kaste - nodokļa bāze | Kaste - nodokļa summa | Apraksts                                                                                                                   | Uzmeklēšanas rezultāts                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Nav nodokļa summas*  | Dažu objektu un investīciju zelta iegāde, kas nav brīva no nodokļiem.                                                    | 33— TaxFreeEUPurchase                                             |
| 34  | 89             | Bez koda     | Ar nodokli apliekamā iegāde Kopienas teritorijā ar nodokļu likmi 19 procenti.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Bez koda     | Ar nodokli apliekamās kopienas iekšējās iegādes ar nodokļu likmi 7 procenti.                                                              | 35-EUPurchaseRehaved</br>35— UseTaxEUPurchaseRemonied (93/61)          |
| 36  | 95             | 98               | Ar nodokli apliekamā iegāde Kopienas teritorijā ar citām nodokļu likmēm.                                                                      | 36-EUPurchaseOtherRates</br>36— UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Ar PVN apliekamā jaunu transportlīdzekļu iegāde kopienas teritorijā no piegādātājiem, kuriem nav PVN ID numurs un kuru nodokļu likme ir vispārīga. | 37-EUPurchaseVevs</br>37– UseTaxEUPurchaseVe papildmaksas (94/96/61)     |

**SADAĻA – SAŅĒMĒJS KĀ NODOKĻU MAKSĀTĀJA**

| Rinda | Kaste - nodokļa bāze | Kaste - nodokļa summa | Apraksts                                                                        | Uzmeklēšanas rezultāts                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Citi peles pakalpojumi, kas balstīti uz pārējo Kopienas zonu.        | 40 – BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Pārdošana, kas ietilpst 13.b sadaļas (2) nr. 3 no UStG.                               | 41 – BeneficiaryTaxDebtorRealEstateTransfer</br>41– UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Citi pakalpojumi, kas ietilpst 13.b sadaļas (2) nr. 1, 2 un 4 līdz 12 no UStG. | 42 – BeneficiaryTaxDebtorOther</br>42 – UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**SADAĻA - PAPILDU INFORMĀCIJA PAR PĀRDOŠANU**

| Rinda | Kaste - nodokļa bāze  | Kaste - nodokļa summa | Apraksts                                                                                                | Uzmeklēšanas rezultāts                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Nav nodokļa summas*  | Pirmā debitora piegādes kopienas iekšējās triangulāras darbības gadījumā.                   | 48 — DeliveriesFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Nav nodokļa summas*  | Ar nodokli apliekamā pārdošanas summa, ja pakalpojuma saņēmējs ir parādā nodoklim. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Nav nodokļa summas*  | Citi ar nodokli neapliekami pakalpojumi.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Nav nodokļa summas*  | Cita ar nodokli neapliekama pārdošana, ja veiktspējas vieta nav Vācijā.                                    | 51-CitiPārdošanasNonTaxable                                                                          |
| 52  | *Nav nodokļa summas* | *Nav nodokļa summas*  | PVN.                                                                                                       | 20. rinda + 21. rinda + 22. rinda + 4. rinda + 34. rinda + 35. rinda + 36. rinda + 37. rinda + 40. rinda + 41. rinda + 42. rinda |

**SADAĻA — IETURAMAIS IEVADES NODOKLIS**

| Rinda | Kaste - nodokļa summa | Apraksts                                                                                                | Uzmeklēšanas rezultāts                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Ievades rēķina nodokļu summas no citiem uzņēmumiem, pakalpojumiem un KOPIENAS iekšējās triangulācijas darbībām.     | 55- InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – ar mīnus zīmi                                                                   |
| 56  | 61               | Ievades nodokļa summas no preču iegādes Kopienas teritorijā.                                           | 56- InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35— UseTaxEUPurchaseRemonied (93/61)</br>36— UseTaxEUPurchaseOtherRates (95/98/61)</br>37– UseTaxEUPurchaseVe papildmaksas (94/96/61) |
| 57  | 62               | Importa PVN radās.                                                                                 | 57 — InputTaxImport                                                                                                                                                            |
| 58  | 67               | Ievades nodokļa summas no pakalpojumiem UStG objekta '13b' nozīmē.                                        | 58-InputTaxServices</br>41– UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42 – UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Ievades nodokļa summas, kas tiek aprēķinātas saskaņā ar vispārējām vidējām likmēm.                                  | 59 — InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) — ar mīnusa zīmi                                                                                    |
| 60  | 59               | Ieturējums nodokļa ieturējums jaunu transportlīdzekļu piegādēm ārpus uzņēmuma un maziem uzņēmumiem. | 60—InputTaxEUPurchaseNewVevs</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVelejas (59/37) – ar mīnusa zīmi                                                                  |
| 61  | 64               | Ievades nodokļa ieturējuma labojums.                                                                     | 61 - InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Atlikusī summa.                                                                                      | 52. rinda – 55. rinda – 56. rinda – 57. rinda – 58. rinda – 50. rinda – 60. rinda – 61. rinda                                                                                                        |

**SADAĻA - CITAS NODOKĻU SUMMAS**

| Rinda | Kaste - nodokļa summa | Apraksts                                                                                                                                                                                                                                                         | Uzmeklēšanas rezultāts                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Nodoklis, ko izraisa nodokļu likmes izmaiņas taksācijas formā un papildu nodoklis par samazināto nodokli.                                                                                                                                        | 64 — AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Nepareizas vai neattaisnotas nodokļa summas, kas parādītas rēķinos, un nodokļu summas, kas ir pienākas saskaņā ar 6.a (4) sadaļu. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Fiksētā īpašā avansa maksājuma ieturējumi pastāvīgam paplašinājumam. Parasti šī rinda tiek aizpildīta tikai ar pēdējo nodokļu perioda avansa paziņojumu.                                                                                                  | Lietotāja ievades parametrs pārskata dialoglodziņā |
| 68  | 83               | Atlikušais avansa PVN maksājums un atlikušais pārpalikums. Pirms summas iekļaut mīnusa žurnālu.                                                                                                                                                          | 62. rinda + 64. rinda – 65. rinda – 66. rinda             |

**SADAĻA - PAPILDINFORMĀCIJA PAR SAMAZINĀŠANU**

| Rinda | Kaste - nodokļa bāze | Kaste - nodokļa summa | Apraksts                                                            | Uzmeklēšanas rezultāts                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Nodokļa bāzes samazinājums rindās 20 līdz 24.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffRerite (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73– BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Ieturējamā ievades nodokļa summu samazināšana 55., 59. un 60. rindā. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74–BadDebtsWriteOffInputTaxEUPurchaseNewVeharles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Pirkšanas atgrieztās maksas PVN

Ja konfigurējat PVN kodus ienākošās atgriezeniskās PVN grāmatošanai, izmantojot izmantošanas nodokli, saistiet pvn kodus ar pārskata lauka uzmeklēšanas rezultātu, kas nosaukumā **satur** "UseTax".

Alternatīvi var konfigurēt divus atsevišķus PVN kodus: vienu apmaksas PVN un vienu PVN ieturējumiem. Pēc tam saistiet katru kodu ar atbilstošajiem pārskata lauka **uzmeklēšanas** rezultātiem.

Piemēram, ar nodokli apliekamām kopienas iegādēm pēc standarta likmes, konfigurē PVN kodu UT_S_EU ar importa nodokli un saista to ar pārskata lauka uzmeklēšanas **rezultātu** **34-UseTaxEUPurchaseStandard.** **·** Šajā gadījumā summas, kas izmanto nodokļu UT_S_EU, tiek atainotas **lodziņos** 089 un 061 (rindas 34 un 56).

Alternatīvi var konfigurēt divus PVN kodus:

  - **VAT_S_EU,** kuras nodokļa likmes vērtība ir -19 procenti
  - **InVAT_S_EU,** kuras nodokļa likme ir 19 procenti

Pēc tam jūs saistāt kodus ar pārskata **lauku uzmeklēšanas** rezultātiem šādā veidā:

  - Saistiet **VAT_S_EU** ar **uzmeklēšanas rezultātu 34-EUPurchaseStandard.**
  - Saistiet **InVAT_S_EU** ar **uzmeklēšanas rezultātu 56-InputTaxEUPurchase.**

Šajā gadījumā summas, kas izmanto VAT_S_EU PVN kodu, tiek attēlotas lodziņā **089** (34. rinda). Summas, kas izmanto **InVAT_S_EU** PVN kodu, tiek atainotas lodziņā 061 (56. rinda).

Plašāku informāciju par to, kā konfigurēt atgriezeniskos PVN maksājumus, skatiet Sadaļā [Apgrieztās](emea-reverse-charge.md) maksas.

## <a name="configure-system-parameters"></a>Sistēmas parametru konfigurēšana

Lai ģenerētu PVN deklarāciju, ir jākonfigurē jūsu organizācijas nodokļu numurs (Steuernummer).

1. Pārejiet uz sadaļu **Organizācijas administrēšana** > **Organizācijas** > **Juridiskās personas**.
2. Atlasiet juridisko personu un pēc tam **atlasiet reģistrācijas** identifikators.
3. Atlasiet vai izveidojiet adresi Vācijā un pēc tam reģistrācijas **ID kopsavilkuma cilnē atlasiet** **Pievienot**.
4. Laukā Reģistrācijas tips atlasiet reģistrācijas tipu, kas atvēlēts Vācijai un kas **izmanto uzņēmuma ID** **(COID)** reģistrācijas kategoriju.
5. Laukā **Reģistrācijas numurs** ievadiet nodokļa numuru.
6. Cilnes **Vispārīgi** laukā Darbības **sākums** ievadiet datumu, kad skaitlis stājas spēkā.

Papildinformāciju par to, kā iestatīt reģistrācijas kategorijas un reģistrācijas [tipus, skatiet reģistrācijas](emea-registration-ids.md) tipiem.

## <a name="set-up-a-vat-declaration-for-germany"></a>Iestatīt PVN deklarāciju Vācijai

### <a name="import-er-configurations"></a>ER konfigurāciju importēšana

Atveriet elektronisko **pārskatu** darbvietu un importējiet šādas versijas vai jaunākas no šiem ER formātiem:

   - PVN deklarācijas Excel (DE).version.101.16.12.xml
   - PVN deklarācijas XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a> Iestatīt pieteikumu parametrus PVN deklarācijas laukiem

Lai automātiski ģenerētu PVN deklarāciju, saistiet PROGRAMMĀ PVN kodus un uzmeklēšanas rezultāti tiks izveidoti ER konfigurācijā.

Sekojiet šiem soļiem, lai noteiktu, kuri PVN kodi ģenerē tos laukus PVN deklarācijā.

1. Dodieties **uz** > **darbalauku** elektronisko pārskatu sniegšanu un atlasiet Pārskatu izveides **konfigurācijas**.
2. Atlasiet PVN **deklarācijas XML (DE)** konfigurāciju un pēc tam atlasiet konfigurācijas programmai noteiktu parametru **\>** iestatījumu.
3. Lapā **Programmai specifiskie** parametri kopsavilkuma cilnē **Pārlūki** atlasiet Pārskata lauka **uzmeklēšanu.**
4. Kopsavilkuma cilnē **Nosacījumi** iestatiet tālāk norādītos laukus, lai saistītu PVN kodus un pārskata laukus.

    | Lauks                  | Apraksts                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Uzmeklēšanas rezultāts          | Atlasiet pārskata lauka vērtību. Plašāku informāciju par vērtībām un to piešķiršanu PVN deklarācijas rindām skatiet [PVN deklarācijas pārskata sadaļā šīs tēmas](#vat-declaration-overview) agrāk.                                                                                               |
    | Nodokļa kods               | Atlasiet PVN kodu, ko saistīt ar pārskata lauku. Grāmatotās nodokļu darbības, kas izmanto atlasīto PVN kodu, tiks savāktas atbilstošajā deklarācijas lodziņā. Ieteicams atdalīt PVN kodus tā, lai viens PVN kods ģenerētu summas tikai vienā deklarācijas lodziņā. |
    | Transakcijas klasifikators | Ja izveidojāt pietiekamus PVN kodus deklarācijas lodziņa noteikšanai, atlasiet **\* Nav \*** tukšs. Ja netiek izveidoti pietiekami daudz PVN kodu, lai viens PVN kods ģenerētu summas tikai vienā deklarācijas lodziņā, varat iestatīt transakcijas klasifikatoru. Ir pieejami šādi darbību klasifikatori:</br>-   **Pirkšana**</br>-   **PurchaseExempt** (pirkšana ar nodokli neapliekamā summa)</br>-   **PurchaseReverseCharge** (no pirkšanas apgrieztās maksas saņemamajiem nodokļiem)</br>-   **Pārdošana**</br>-   **SalesExempt** (ar nodokli neapliekamā pārdošana)</br>-   **SalesReverseCharge** (maksājamie nodokļi no pirkšanas atgriezes maksas vai pārdošanas atgriezeniskās maksas)</br>-   **Izmantot** nodokli. </br>Katram transakcijas klasifikatoram ir pieejams arī kredīta notas klasifikators. Piemēram, viens no šiem klasifikatori ir **PurchaseCreditNote** (pirkšanas kredīta nota).</br>Pārliecinieties, vai katram PVN kodam ir jāizveido divas rindas: viena, kam ir transakcijas klasifikatora vērtība, un viena ar transakcijas klasifikatoru kredīta notas vērtībai. |

    > [!NOTE]
    > Visus PVN kodus saistīt ar uzmeklēšanas rezultātiem. Ja jebkuriem PVN kodiem nav jāģenerē vērtības PVN deklarācijā, saistiet tos ar **citiem** uzmeklēšanas rezultātiem.

    ![Programmai specifisku parametru lapa](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. Laukā **Stāvoklis** mainiet vērtību uz **Pabeigts**.
6. Darbību rūtī atlasiet Eksportēt, **lai** eksportētu programmai raksturīgo parametru iestatījumus.
7. Atlasiet PVN deklarācijas Excel (DE) konfigurāciju un pēc tam darbību rūtī atlasiet Importēt, lai importētu parametrus, kas konfigurēti **PVN** deklarācijas **XML** **(DE)** importam.
8. Laukā **Statuss** atlasiet **Pabeigts**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Iestatiet PVN pārskata formātu summu priekšskatījumam programmā Excel

1. Līdzekļu pārvaldības **darbvietā** atrodiet un iespējojiet **PVN deklarācijas formāta pārskatu** līdzekli.
2. Dodieties uz **Virsgrāmatas** > **iestatījumu Virsgrāmatas** > **parametriem**.
3. Cilnes PVN kopsavilkuma cilnes Nodokļu opcijas laukā PVN deklarācijas formāta kartēšana atlasiet PVN deklarācijas **Excel** **·** **·** **·** (DE).

   Šis formāts tiek drukāts, kad darbināt **pārskatu par PVN maksājumu perioda** pārskatam. To var drukāt arī tad, ja **PVN** maksājumu lapā **atlasāt** Drukāt.

4. Lapā **Nodokļu iestādes** atlasiet nodokļu iestādi un pēc tam laukā Pārskata **izkārtojums atlasiet** **Noklusējuma**.

Ja jūs konfigurējat PVN deklarāciju juridiskajā persona, kam ir vairākas [PVN](emea-reporting-for-multiple-vat-registrations.md) reģistrācijas, sekojiet šiem soļiem:

1. Dodieties uz **Virsgrāmatas** > **iestatījumu Virsgrāmatas** > **parametriem**.
2. Cilnē PVN kopsavilkuma cilnes Elektroniskie **pārskati** **valstīm/reģioniem, DEU rindā atlasiet PVN deklarācijas** **Excel** **(DE)** ER formātu.

## <a name="set-up-electronic-messages"></a>Iestatīt elektroniskos ziņojumus

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Lejupielādēt un importēt datu pakotni, kam ir elektronisko ziņojumu iestatījumu piemērs

Datu pakotne ietver elektroniskā ziņojuma iestatījumus, kas tiek izmantoti PVN deklarācijas ģenerēšanai XML formātā un pēc tam priekšskatiet to programmā Excel. Šos iestatījumus var paplašināt vai izveidot pats. Papildinformāciju par to, kā strādāt ar elektronisko ziņapmaiņu un izveidot savus iestatījumus, skatiet sadaļā [Elektroniskā](../general-ledger/electronic-messaging.md) ziņojumapmaiņa.

1. Programmas Lifecycle Services(LCS) koplietojamā līdzekļu bibliotēkā atlasiet Datu pakotni kā līdzekļu veidu un pēc tam lejupielādējiet [Microsoft Dynamics](https://lcs.dynamics.com/v2) DE PVN **deklarācijas** **EM** pakotni. Lejupielādētā faila nosaukums ir **DE PVN deklarācijas EM package.zip.**
2. Datu Dynamics 365 Finance pārvaldības **darbvietā** atlasiet **Importēt**.
3. Kopsavilkuma **cilnes** Imports laukā **Grupas nosaukums** ievadiet darba nosaukumu.
4. Kopsavilkuma cilnē **Atlasītās entītijas** atlasiet **Pievienot failu**.
5. Dialoglodziņā Pievienot failu pārbaudiet, vai avota datu formāta lauks ir iestatīts uz Pakotne, atlasiet Augšupielādēt un pievienojiet un pēc tam atlasiet **agrāk** **·** **·** **lejupielādēto** zip failu.
6. Atlasiet **Aizvērt**.
7. Kad datu elementi ir augšupielādēti, darbību rūtī atlasiet **Importēt**.
8. Dodieties **uz nodokļu pieprasījumiem un** > **·** > **pārskatiem** > **Elektroniskie ziņojumi Elektroniskie ziņojumi un** apstipriniet importēto elektronisko ziņojumu apstrādi.

### <a name="configure-electronic-messages"></a>Konfigurēt elektroniskos ziņojumus

1. Doties uz **nodokļu** > **iestatīšanas** > **·** > **elektroniskajiem ziņojumiem Aizpildīt ierakstu** darbības.
2. Atlasiet rindu DE **aizpilda PVN atgriešanas ierakstus** un tad izvēlieties Rediģēt **vaicājumu**.
3. Izmantojiet filtru, lai norādītu segšanas periodus, ko iekļaut pārskatā.
4. Ja pārskats par nodokļu darbībām no citiem segšanas periodiem jāsniedz citā deklarācijā, izveidojiet jaunu aizpilda ierakstu darbību un **atlasiet** atbilstošos apmaksas periodus.

## <a name="preview-the-vat-declaration-in-excel"></a>Priekšskatīt PVN deklarāciju programmā Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Priekšskatīt PVN deklarāciju programmā Excel no pārskata PVN par nosegšanas perioda periodisko uzdevumu

1. Doties uz **nodokļu** > **·** > **periodiskajiem** > **uzdevumiem. Deklarācijas** > **PVN pārskats par PVN maksājumu** periodam.
2. Laukā **Apmaksas** periods atlasiet vērtību.
3. Laukā **PVN maksājuma versija atlasiet vienu no šīm** vērtībām:

    - **Oriģināls: izveidojiet pārskatu oriģinālā PVN maksājuma PVN** darbībām vai pirms PVN maksājuma ģenerēšanas.
    - **Labojumi**: ģenerējiet pārskatu par visu turpmāko PVN maksājumu PVN darbībām par periodu.
    - **Kopējais** saraksts: ģenerēt pārskatu par visām PVN darbībām par periodu, ieskaitot oriģinālos un visus labojumus.

4. Laukā **No datuma atlasiet pārskata perioda sākuma** datumu.
5. Atlasiet **Labi** un pārskatiet Excel pārskatu.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Nosegt un grāmatot PVN

1. Doties **uz** > **periodisko uzdevumu** > **nodokļiem** > **deklarācijas PVN** > **kārtošanu un PVN** iegrāmatošanu.
2. Laukā **Apmaksas** periods atlasiet vērtību.
3. Laukā **PVN maksājuma versija atlasiet vienu no šīm** vērtībām:

    - **Oriģināls:** ģenerējiet maksājuma perioda sākotnējo PVN maksājumu.
    - **Pēdējie** labojumi: ģenerēt PVN labojuma maksājumu pēc tam, kad maksājuma periodam tika izveidots sākotnējais PVN maksājums.

4. Laukā **No datuma atlasiet pārskata perioda sākuma** datumu.
5. Atlasiet **Labi**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Priekšskatīt PVN deklarāciju programmā Excel no PVN maksājuma

1. Dodieties **uz nodokļu** > **vaicājumiem un pārskatiem par PVN pieprasījumiem par PVN maksājumiem un atlasiet PVN maksājuma** > **·** > **rindu**.
2. Atlasiet **Drukāt pārskatu un pēc tam atlasiet** **Labi**.
3. Pārskatiet Excel failu, kas tiek ģenerēts atlasītajai PVN maksājuma rindai.

    > [!NOTE]
    > Pārskats tiek ģenerēts tikai atlasītajai PVN maksājuma rindai. Ja vēlaties izveidot, piemēram, labojošo deklarāciju, kas ietver visus perioda labojumus, vai aizstāj deklarāciju, kurā ietverti sākotnējie dati un visi labojumi, izmantojiet pārskata PVN nosegšanas perioda periodiskajam **uzdevumam**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Ģenerējiet PVN deklarāciju no elektroniskajiem ziņojumiem

Kad izmantojat elektroniskos ziņojumus, lai ģenerētu pārskatu, varat apkopot nodokļu datus no vairākām juridiskām personām. Papildinformāciju skatiet [tālāk šīs tēmas sadaļā Vairāku juridisko personu sadaļu](#run-a-vat-declaration-for-multiple-legal-entities) PVN deklarācijas palaišana.

Šī procedūra attiecas uz elektronisko ziņojumu apstrādes piemēru, ko importējat no LCS koplietojamās līdzekļu bibliotēkas.

1. Dodieties uz **nodokļu** > **vaicājumiem un pārskatiem** > **·** > **Elektroniskie** ziņojumi.
2. Kreisās puses rūtī izvēlieties **DE PVN** deklarāciju.
3. Kopsavilkuma **cilnē** Ziņojumi atlasiet Jauns un pēc tam dialoglodziņā Palaist apstrādi **atlasiet** **·** **Labi**.
4. Atlasiet izveidoto ziņojuma rindu, ievadiet aprakstu un pēc tam norādiet deklarācijas sākuma un beigu datumus.

    > [!NOTE]
    > No 5. līdz 7. solim nav obligāti.

5. Nav obligāti: kopsavilkuma **cilnē Ziņojumi atlasiet Apkopot datus un pēc tam atlasiet** **·** **Labi**. Iepriekš izveidotie PVN maksājumi tiek pievienoti ziņojumam. Plašāku informāciju skatiet iepriekš šajā [tēmā sadaļā PVN](#settle-and-post-sales-tax) kārtošana un grāmatošana. Ja izlaidīsiet šo soli, jūs joprojām varat ģenerēt PVN deklarāciju, izmantojot nodokļu deklarācijas **versijas** lauku deklarācijas **dialoglodziņā**.
6. Nav obligāti: kopsavilkuma **cilnē Ziņojumu** krājumi pārskatiet PVN maksājumus, kas tiek pārsūtīti apstrādei. Pēc noklusējuma tiek iekļauti visi atlasītā perioda PVN maksājumi, kas netika iekļauti citā tā paša apstrādes ziņojumā.
7. Nav obligāti: **atlasiet** Oriģinālais dokuments, lai pārskatītu PVN maksājumus, vai atlasiet **Dzēst,** lai izslēgtu PVN maksājumus no apstrādes. Ja izlaidīsiet šo soli, jūs joprojām varat ģenerēt PVN deklarāciju, izmantojot nodokļu deklarācijas **versijas** lauku deklarācijas **dialoglodziņā**.
8. Kopsavilkuma **cilnē** Ziņojumi atlasiet statusu **Atjaunināt**. Dialoglodziņā Atjaunināt **statusu** atlasiet Gatavs **ģenerēšanu un pēc tam atlasiet** **Labi**. Pārbaudiet, vai ziņojuma statuss ir mainīts uz **Gatavs ģenerēšanas uzdevumam.**
9. Atlasiet **ģenerēt** pārskatu. Lai priekšskatītu PVN deklarācijas summas, dialoglodziņā **Palaist apstrādi** atlasiet Priekšskatījuma pārskats un pēc **tam atlasiet** **Labi**.
10. Dialoglodziņā Elektronisko **pārskatu parametri iestatiet tālāk** norādītos laukus un pēc tam atlasiet **Labi**.

    | **Lauks**                                   | **Apraksts**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Nosegšanas periods                           | Atlasiet apmaksas periodu. Ja **5**. solī atlasījāt Apkopot datus, varat atstāt šo lauku tukšu. Pārskats tiks ģenerēts PVN darbībām, kas iekļautas savāktos PVN maksājumos. |
    | Nodokļu deklarācijas versija                     | Atlasiet vienu no šīm vērtībām:</br>-   **Oriģināls** - ģenerējiet pārskatu PVN darbībām oriģinālajam PVN maksājumam vai pirms PVN maksājuma ģenerēšanas.</br>-   **Labojumi** – ģenerējiet pārskatu pvn darbībām visiem turpmākajiem PVN maksājumiem par periodu.</br>-   **Kopējais saraksts** – ģenerējiet pārskatu par visām PVN darbībām par periodu, ieskaitot oriģinālos un visus labojumus.|
    | Ar nodokli apliekamais pārstāvis | Ja piemērojams, atlasiet pusi, kas ir PVN deklarācijas nodokļu pārstāvis. Informācija par atlasīto pusi tiek eksportēta uz **elementu DatenLieferant** XML. |
    | Kontaktpersona | Atlasiet organizācijas personu, kas ir datu piegādātājs. Informācija par atlasīto personu tiek eksportēta **uz elementu DatenLieferant** XML. |
    | Koriģējoša atgriešana | Atlasiet **Jā**, ja šī ir labojoša PVN deklarācija. Šajā gadījumā XML elementam KZ10 būs vērtība **1**.|
    | Pavaddokumenti | Atlasiet **Jā**, ja nosūtat arī pavaddokumentus. Šajā gadījumā XML elementam KZ22 būs vērtība **1**.|
    | SEPA tiešā debeta pilnvarojums tiks atcelts izņēmuma kārtā| Atlasiet **Jā**, ja SEPA tiešā debeta pilnvarojums tiks atcelts kā izņēmums šim pirms reģistrācijas periodam. Piemēram, ieskaita pieprasījumu dēļ. Atlikusī bilance jāapmaksā atsevišķi. Šajā gadījumā XML elementam KZ26 būs vērtība **1**. |
    | Korespondējošā summa vēlamajai izdevumu summai | Atlasiet **Jā**, ja atlīdzības summa tiek kompensēta pēc pieprasītās summas vai ja atlīdzības summa ir piešķirta. Šajā gadījumā XML elementam KZ29 būs vērtība **1**. |
    | Īpašais avansa maksājuma pastāvīgais paplašinājums | Ievadiet fiksētā īpašā avansa maksājuma ieturējumu summu pastāvīgam paplašinājumam. Šie ieturējumu apjomi parasti tiek pabeigti tikai nodokļu perioda pēdējās iepriekšējas reģistrācijas laikā. Summa tiek eksportēta PVN deklarācijas 67. rindā (39. lodziņā) un XML elementā KZ39. |

11. Atlasiet **pielikumus** lapas augšējā labajā stūrī un pēc tam atlasiet **Atvērt**.
12. Pārskatiet summas Excel dokumentā un pēc tam atlasiet **Ģenerēt** pārskatu.
13. Lai ģenerētu PVN deklarāciju XML formātā, dialoglodziņā Palaist apstrādi atlasiet Ģenerēt **pārskatu un pēc tam atlasiet** **·** **Labi**.
14. Dialoglodziņā Elektronisko **pārskatu parametri** iestatiet laukus atbilstoši 10. darbībā aprakstītajiem laukiem.
15. Atlasiet pielikumus lapas augšējā labajā stūrī, lejupielādējiet failu un izmantojiet **to** iesniegšanai nodokļu iestādei.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a> Palaist PVN deklarāciju vairākām juridiskām personām

Lai lietotu formātus, lai iesniegtu pārskatu par PVN deklarāciju juridisko personu grupai, vispirms ir jāiestata ER formātu programmai raksturīgie parametri PVN kodiem no visām juridiskajām personām.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Iestatīt elektroniskos ziņojumus, lai apkopotu nodokļu datus no vairākām juridiskām personām

Sekojiet šiem soļiem, lai iestatītu elektroniskos ziņojumus, kas apkopos datus no vairākām juridiskām personām.

1. Pārejiet uz **sadaļu** > **Darbalauku līdzekļu** pārvaldība.
2. Atrodiet un atlasiet **starpuzņēmumu vaicājumus aizpildīto ierakstu darbību līdzeklim sarakstā un pēc tam** atlasiet Aktivizēt **tagad**.
3. Doties uz **nodokļu** > **·** > **iestatīšanas \> elektroniskajiem ziņojumiem Aizpildīt ierakstu darbības**.
4. Darbības lapā **Aizpildīt ierakstus atlasiet** rindu, kas paredzēts DE **aizpilda PVN atgriešanas** ierakstus.

   Datu **avotu iestatījumu** režģī ir pieejams **jauns** uzņēmuma lauks. Esošiem ierakstiem šajā laukā tiek rādīts pašreizējās juridiskās personas identifikators.

5. Datu **avotu iestatījumu** režģī pievienojiet rindu katrai papildu juridiskajai personai, kas ir jāiekļauj pārskatā. Katrai jaunai rindai iestatiet šādus laukus.

    | Lauks                  | Apraksts                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Nosaukums                   | Ievadiet vērtību, kas palīdzēs saprast, no kurienes ir šis ieraksts. Piemēram, ievadiet **PVN maksājumu 1.** filiālē. |
    | Ziņojuma krājuma veids      | Izvēlieties **PVN** atgriešanu. Šī vērtība ir vienīgā vērtība, kas pieejama visiem ierakstiem.                                    |
    | Konta veids           | Atlasīt **visu**                                                                                                               |
    | Galvenās tabulas nosaukums      | Norādiet **TaxReportVoucher** visiem ierakstiem.                                                                             |
    | Dokumenta numura lauks  | Norādīt **dokumentu** visiem ierakstiem.                                                                                      |
    | Dokumenta datuma lauks    | Norādiet **TransDate** visiem ierakstiem.                                                                                    |
    | Dokumenta konta lauks | Visiem **ierakstiem norādiet** TaxPeriod.                                                                                    |
    | Uzņēmums                | Atlasiet juridiskās personas ID.                                                                                            |
    | Lietotāja vaicājums             | Šī izvēles rūtiņa tiek automātiski atzīmēta, kad definējat kritērijus, atlasot **Vaicājumu** Labot.                                 |

6. Katrai jaunai rindai atlasiet vaicājumu Rediģēt un norādiet juridiskās personas saistīto segšanas periodu, kas **norādīts** rindas **laukā** Uzņēmums.

Kad iestatīšana ir pabeigta, lapā Elektroniskie ziņojumi datu apkopošanas funkcija apkopo **PVN** **maksājumus** no visām juridiskajām personām, ko esat definējis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
