---
title: "Centralizētie maksājumi norēķiniem ar piegādātājiem"
description: "Organizācijas, kurās ir iekļautas vairākas juridiskās personas, var izveidot un pārvaldīt maksājumus, izmantojot vienu juridisko personu, kura apstrādā visus maksājumus. Tāpēc vieniem un tiem pašiem maksājumiem nav jāievada vairākās juridiskajās personās. Šajā rakstā ir sniegti piemēri, kas parāda, kā tiek veikta centralizēto maksājumu grāmatošana dažādās situācijās."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 49d5242168cd43e78dd4b0c63da363f91f680904
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="centralized-payments-for-accounts-payable"></a>Centralizētie maksājumi norēķiniem ar piegādātājiem

[!include[banner](../includes/banner.md)]


Organizācijas, kurās ir iekļautas vairākas juridiskās personas, var izveidot un pārvaldīt maksājumus, izmantojot vienu juridisko personu, kura apstrādā visus maksājumus. Tāpēc vieniem un tiem pašiem maksājumiem nav jāievada vairākās juridiskajās personās. Šajā rakstā ir sniegti piemēri, kas parāda, kā tiek veikta centralizēto maksājumu grāmatošana dažādās situācijās.

Organizācijas, kurās ir iekļautas vairākas juridiskās personas, var izveidot un pārvaldīt maksājumus, izmantojot vienu juridisko personu, kas apstrādā visus maksājumus. Tāpēc vieniem un tiem pašiem maksājumiem nav jāievada vairākās juridiskajās personās. Turklāt organizācijas ietaupa laiku, jo maksāšanas process tiek racionalizēts.

Organizācijā ar centralizētiem maksājumiem ir daudz juridisku personu, un katra juridiskā persona pārvalda savu piegādātāju rēķinus. Maksājumi visām juridiskajām personām tiek iegūti no vienas juridiska personas, kas zināma kā maksājuma dokumentā norādītā juridiskā persona. Apmaksas segšanas laikā tiek veidotas piemērojamās izpildes termiņa un izpildes veicēja darbības. Varat norādīt, kura no organizācijas juridiskajām personām saņems realizēto peļņu vai realizēto zaudējumu transakcijas un kā tiks apstrādātas termiņatlaides, kas saistītas ar starpuzņēmumu maksājumiem. 

Turpmākie piemēri parāda, kā tiek veikta grāmatošana dažādās situācijās. Turpmākā konfigurācija attiecas uz visiem šiem piemēriem.

-   Juridiskās personas ir Fabrikam, Fabrikam East un Fabrikam West. Maksājumi tiek veikti no Fabrikam.
-   Lauks **Grāmatot termiņatlaidi** lapā **Starpuzņēmumu uzskaite** ir iestatīts uz **Rēķinā norādītā juridiskā persona**.
-   Lauks **Grāmatot valūtas maiņas ieguvumus vai zaudējumus** lapā **Starpuzņēmumu uzskaite** ir iestatīts uz **Maksājumā norādītā juridiskā persona**.
-   Piegādātājs Fourth Coffee ir iestatīts kā katras juridiskās personas kreditors. Dažādu juridisko personu piegādātāji tiek uzskatīti par to pašu piegādātāju, ja viņi koplieto vienu un to pašu globālo adrešu grāmatas ID.

| Direktorija ID | Kreditora konts | Nosaukums          | Juridiska persona  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Coffee ceturtdaļa | Fabrikam      |
| 1050         | 100            | Coffee ceturtdaļa | Fabrikam East |
| 1050         | 3004           | Coffee ceturtdaļa | Fabrikam West |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>1. piemērs: kreditora maksājums par rēķinu no citas juridiskās personas.
Fabrikam East ir atvērts rēķins kreditora kontam 100, Fourth Coffee. Fabrikam ievada un grāmato maksājumu Fabrikam kreditora kontam 3004, Fourth Coffee. Maksājums ir nosegts ar atvērtu rēķinu.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Rēķins ir grāmatots Fabrikam East, kreditoram 100

| Konts                          | Summa debetā | Summa kredītā |
|----------------------------------|--------------|---------------|
| Izdevumi (Fabrikam East)          | 600,00       |               |
| Parādi kreditoriem (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Maksājums tiek ģenerēts un grāmatots Fabrikam, Fabrikam kreditoram 3004

| Konts                     | Summa debetā | Summa kredītā |
|-----------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam) | 600,00       |               |
| Skaidra nauda (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam maksājums tiek nosegts ar Fabrikam East rēķinu

**Fabrikam grāmatošana**

| Konts                           | Summa debetā | Summa kredītā |
|-----------------------------------|--------------|---------------|
| Fabrikam East (Fabrikam) debitora parādi | 600,00       |               |
| Parādi kreditoriem (Fabrikam)       |              | 600,00        |

**Fabrikam East grāmatojums**

| Konts                          | Summa debetā | Summa kredītā |
|----------------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam East) | 600,00       |               |
| Fabrikam (Fabrikam East) kreditora parādi  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>2. piemērs: kreditora maksājums par rēķinu no citas juridiskās personas ar termiņatlaidi.
Fabrikam East ir atvērts rēķins kreditoram 100, Fourth Coffee. Rēķinam ir pieejama 20,00 termiņatlaide. Fabrikam ievada un grāmato 580,00 lielu maksājumu Fabrikam kreditoram 3004, Fourth Coffee. Maksājums tiek segts ar neapmaksātajiem Fabrikam East rēķiniem. Termiņatlaide tiek grāmatota rēķinā norādītajā juridiskajā personā — Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Rēķins tiek grāmatots Fabrikam East, Fabrikam East kreditoram 100

| Konts                          | Summa debetā | Summa kredītā |
|----------------------------------|--------------|---------------|
| Izdevumi (Fabrikam East)          | 600,00       |               |
| Parādi kreditoriem (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Maksājums tiek ģenerēts un grāmatots Fabrikam, Fabrikam kreditoram 3004

| Konts                     | Summa debetā | Summa kredītā |
|-----------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam) | 580,00       |               |
| Skaidra nauda (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam maksājums tiek nosegts ar Fabrikam East rēķinu

**Fabrikam grāmatošana**

| Konts                           | Summa debetā | Summa kredītā |
|-----------------------------------|--------------|---------------|
| Fabrikam East (Fabrikam) debitora parādi | 580,00       |               |
| Parādi kreditoriem (Fabrikam)       |              | 580,00        |

**Fabrikam East grāmatojums**

| Konts                          | Summa debetā | Summa kredītā |
|----------------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam East) | 580,00       |               |
| Fabrikam (Fabrikam East) kreditora parādi  |              | 580,00        |
| Parādi kreditoriem (Fabrikam East) | 20,00        |               |
| Termiņatlaide (Fabrikam East)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>3. piemērs: kreditora maksājums par rēķinu no citas juridiskās personas ar realizētu apmaiņas likmes zaudējumu.
Fabrikam East ir atvērts rēķins kreditoram 100, Fourth Coffee. Fabrikam ievada un grāmato maksājumu Fabrikam kreditoram 3004, Fourth Coffee. Maksājums ir nosegts ar atvērtu Fabrikam East rēķinu. Segšanas procesa laikā ir ģenerēta valūtas maiņas zaudējumu darbība.

-   Maiņas kurss no Euro (EUR) uz ASV dolāriem (USD) pēc rēķina datuma: 1,2062
-   Maiņas kurss no EUR uz USD maksājuma datumā: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Rēķins tiek grāmatots Fabrikam East, Fabrikam East kreditoram 100

| Konts                          | Summa debetā            | Summa kredītā           |
|----------------------------------|-------------------------|-------------------------|
| Izdevumi (Fabrikam East)          | 600,00 EUR / 723,72 USD |                         |
| Parādi kreditoriem (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Maksājums tiek ģenerēts un grāmatots Fabrikam, Fabrikam kreditoram 3004

| Konts                     | Summa debetā            | Summa kredītā           |
|-----------------------------|-------------------------|-------------------------|
| Parādi kreditoriem (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Skaidra nauda (Fabrikam)             |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam maksājums tiek nosegts ar Fabrikam East rēķinu

**Fabrikam grāmatošana**

| Konts                           | Summa debetā            | Summa kredītā           |
|-----------------------------------|-------------------------|-------------------------|
| Fabrikam East (Fabrikam) debitora parādi | 600,00 EUR / 736,62 USD |                         |
| Parādi kreditoriem (Fabrikam)       |                         | 600,00 EUR / 736,62 USD |
| Realizētie zaudējumi (Fabrikam)          | 0,00 EUR / 12,90 USD    |                         |
| Fabrikam East (Fabrikam) debitora parādi |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East grāmatojums**

| Konts                          | Summa debetā            | Summa kredītā           |
|----------------------------------|-------------------------|-------------------------|
| Parādi kreditoriem (Fabrikam East) | 600,00 EUR / 736,62 USD |                         |
| Fabrikam (Fabrikam East) kreditora parādi  |                         | 600,00 EUR / 736,62 USD |
| Fabrikam (Fabrikam East) kreditora parādi  | 0,00 EUR / 12,90 USD    |                         |
| Parādi kreditoriem (Fabrikam East) |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>4. piemērs: kreditora maksājums par rēķinu no citas juridiskās personas ar termiņatlaidi un realizētiem maiņas likmes zaudējumiem.
Fabrikam East ir atvērts rēķins kreditoram 100, Fourth Coffee. Šim rēķinam ir pieejama termiņatlaide, un ir izveidota pārdošanas nodokļa transakcija. Fabrikam grāmato maksājumu Fabrikam kreditoram 3004, Fourth Coffee. Maksājums ir nosegts ar atvērto Fabrikam East rēķinu. Segšanas procesa laikā ir ģenerēta valūtas maiņas zaudējumu darbība. Termiņatlaide ir iegrāmatota rēķinā norādītajai juridiskajai personai (Fabrikam East), un valūtas maiņas zaudējumi ir iegrāmatoti maksājuma dokumentā norādītajai juridiskajai personai (Fabrikam).

-   Maiņas kurss no EUR uz USD rēķina datumā: 1,2062
-   Maiņas kurss no EUR uz USD maksājuma datumā: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Rēķins ir grāmatots un nodokļu darbība ir ģenerēta Fabrikam East, kreditoram 100

| Konts                          | Summa debetā            | Summa kredītā           |
|----------------------------------|-------------------------|-------------------------|
| Izdevumi (Fabrikam East)          | 564,07 EUR / 680,38 USD |                         |
| PVN (Fabrikam East)        | 35,93 EUR / 43,34 USD   |                         |
| Parādi kreditoriem (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Maksājums tiek ģenerēts un grāmatots Fabrikam, Fabrikam kreditoram 3004

| Konts                     | Summa debetā            | Summa kredītā           |
|-----------------------------|-------------------------|-------------------------|
| Parādi kreditoriem (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Skaidra nauda (Fabrikam East)        |                         | 588,72 EUR / 722,77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam maksājums tiek nosegts ar Fabrikam East rēķinu

**Fabrikam grāmatošana**

| Konts                           | Summa debetā            | Summa kredītā           |
|-----------------------------------|-------------------------|-------------------------|
| Fabrikam East (Fabrikam) debitora parādi | 588,72 EUR / 722,77 USD |                         |
| Parādi kreditoriem (Fabrikam)       |                         | 588,72 EUR / 722,77 USD |
| Realizētie zaudējumi (Fabrikam)          | 0,00 EUR / 12,66 USD    |                         |
| Fabrikam East (Fabrikam) debitora parādi |                         | 0,00 EUR / 12,66 USD    |

**Fabrikam East grāmatojums**

| Konts                          | Summa debetā            | Summa kredītā           |
|----------------------------------|-------------------------|-------------------------|
| Parādi kreditoriem (Fabrikam East) | 588,72 EUR / 722,77 USD |                         |
| Fabrikam (Fabrikam East) kreditora parādi  |                         | 588,72 EUR / 722,77 USD |
| Pienākas Fabrikam (Fabrikam East   | 0,00 EUR / 12,66 USD    |                         |
| Parādi kreditoriem (Fabrikam East) |                         | 0,00 EUR / 12,66 USD    |
| Parādi kreditoriem (Fabrikam East) | 11,28 EUR / 13,61 USD   |                         |
| Termiņatlaide (Fabrikam East)    |                         | 11,28 EUR / 13,61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>5. piemērs: kreditora kredīta nota ar primāro maksājumu
Fabrikam ģenerē 75,00 lielu maksājumu kreditoram 3004, Fourth Coffee. Maksājums ir nosegts ar atvērtu rēķinu Fabrikam West kreditoram 3004 un atvērtu kredīta notu Fabrikam East kreditoram 100. Šis maksājums tiek atlasīts kā primārais maksājums lapā **Segt transakcijas**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Rēķins ir grāmatots Fabrikam West kreditoram 3004

| Konts                          | Summa debetā | Summa kredītā |
|----------------------------------|--------------|---------------|
| Izdevumi (Fabrikam West)          | 100,00       |               |
| Parādi kreditoriem (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kredīta nota ir grāmatota Fabrikam East kreditoram 100

| Konts                          | Summa debetā | Summa kredītā |
|----------------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam East) | 25,00        |               |
| Pirkumu atgriešana (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Maksājums ir grāmatots Fabrikam kreditoram 3004

| Konts                     | Summa debetā | Summa kredītā |
|-----------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam) | 75,00        |               |
| Skaidra nauda (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam maksājums ir nosegts ar Fabrikam West rēķinu un Fabrikam East kredīta notu

**Fabrikam grāmatošana**

| Konts                           | Summa debetā | Summa kredītā |
|-----------------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam)       | 25,00        |               |
| Fabrikam East (Fabrikam) kreditora parādi   |              | 25,00         |
| Fabrikam West (Fabrikam) debitora parādi | 100,00       |               |
| Parādi kreditoriem (Fabrikam)       |              | 100,00        |

**Fabrikam East grāmatojums**

| Konts                           | Summa debetā | Summa kredītā |
|-----------------------------------|--------------|---------------|
| Fabrikam (Fabrikam East) debitora parādi | 25,00        |               |
| Parādi kreditoriem (Fabrikam East)  |              | 25,00         |

**Fabrikam West grāmatošana**

| Konts                          | Summa debetā | Summa kredītā |
|----------------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam West) | 100,00       |               |
| Fabrikam (Fabrikam West) kreditora parādi  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>6. piemērs: kreditora kredīta nota bez primārā maksājuma
Fabrikam ģenerē 75,00 lielu maksājumu kreditoram 3004, Fourth Coffee. Maksājums ir nosegts ar atvērtu rēķinu Fabrikam West kreditoram 3004 un atvērtu kredīta notu Fabrikam East kreditoram 100. Šis maksājums netiek atlasīts kā primārais maksājums lapā **Segt transakcijas**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Rēķins ir grāmatots Fabrikam West kreditoram 3004

| Konts                          | Summa debetā | Summa kredītā |
|----------------------------------|--------------|---------------|
| Izdevumi (Fabrikam West)          | 100,00       |               |
| Parādi kreditoriem (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kredīta nota ir grāmatota Fabrikam East kreditoram 100

| Konts                          | Summa debetā | Summa kredītā |
|----------------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam East) | 25,00        |               |
| Pirkumu atgriešana (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Maksājums ir grāmatots Fabrikam kreditoram 3004

| Konts                     | Summa debetā | Summa kredītā |
|-----------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam) | 75,00        |               |
| Skaidra nauda (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam maksājums ir nosegts ar Fabrikam West rēķinu un Fabrikam East kredīta notu

**Fabrikam grāmatošana**

| Konts                           | Summa debetā | Summa kredītā |
|-----------------------------------|--------------|---------------|
| Fabrikam West (Fabrikam) debitora parādi | 75,00        |               |
| Parādi kreditoriem (Fabrikam)       |              | 75,00         |

**Fabrikam East grāmatojums**

| Konts                                | Summa debetā | Summa kredītā |
|----------------------------------------|--------------|---------------|
| Pienākas no Fabrikam West (Fabrikam East) | 25,00        |               |
| Parādi kreditoriem (Fabrikam East)       |              | 25,00         |

**Fabrikam West grāmatošana**

| Konts                              | Summa debetā | Summa kredītā |
|--------------------------------------|--------------|---------------|
| Parādi kreditoriem (Fabrikam West)     | 75,00        |               |
| Fabrikam (Fabrikam West) kreditora parādi      |              | 75,00         |
| Parādi kreditoriem (Fabrikam West)     | 25,00        |               |
| Pienākas Fabrikam East (Fabrikam West) |              | 25,00         |






