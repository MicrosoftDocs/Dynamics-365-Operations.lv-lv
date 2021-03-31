---
title: Centralizēti maksājumi debitoriem
description: Organizācijas, kurās ir iekļautas vairākas juridiskās personas, var izveidot un pārvaldīt maksājumus, izmantojot vienu juridisko personu, kura apstrādā visus maksājumus. Tāpēc viena un tā pati transakcija nav jāievada vairākās juridiskajās personās. Šajā rakstā ir sniegti piemēri, kas parāda, kā tiek veikta centralizēto maksājumu grāmatošana dažādās situācijās.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edba4e496de9cbb99765857d0d5e87c32477f803
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228891"
---
# <a name="centralized-payments-for-accounts-receivable"></a>Centralizēti maksājumi debitoriem

[!include [banner](../includes/banner.md)]

Organizācijas, kurās ir iekļautas vairākas juridiskās personas, var izveidot un pārvaldīt maksājumus, izmantojot vienu juridisko personu, kura apstrādā visus maksājumus. Tāpēc viena un tā pati transakcija nav jāievada vairākās juridiskajās personās. Šajā rakstā ir sniegti piemēri, kas parāda, kā tiek veikta centralizēto maksājumu grāmatošana dažādās situācijās.

Organizācijas, kurās ir iekļautas vairākas juridiskās personas, var izveidot un pārvaldīt maksājumus, izmantojot vienu juridisko personu, kas apstrādā visus maksājumus. Tāpēc viena un tā pati transakcija nav jāievada vairākās juridiskajās personās. Turklāt organizācija arī ietaupa laiku, jo maksājumu priekšlikumu, nosegšanas un atvērto vai slēgto transakciju rediģēšanas procesi centralizētajiem maksājumiem notiek racionalizēti. 

Organizācijā ar centralizētiem maksājumiem operācijām ir daudz juridisko personu, un katra juridiskā persona pārvalda savu rēķinos saņemamo informāciju. Maksājumus visām juridiskajām personām saņem viena juridiskā persona, kura tiek saukta par maksājuma juridisko personu. Apmaksas segšanas laikā tiek veidotas piemērojamās izpildes termiņa un izpildes veicēja darbības. Varat norādīt, kura no organizācijas juridiskajām personām saņem realizēto ieguvumu vai realizēto zaudējumu transakcijas un kā tiks apstrādātas termiņatlaižu transakcijas, kas ir saistītas ar centralizēto maksājumu. Centralizēto maksājumu žurnāla rindā vienumam **Konta tips** jābūt atlasītam iestatījumam Debitors. Vienumam **Korespondējošā konta tips** jābūt atlasītam iestatījumam Banka vai Virsgrāmata. Bankas kontam jābūt pašreizējā uzņēmumā. 

Turpmākie piemēri parāda, kā tiek veikta grāmatošana dažādās situācijās. Turpmākā konfigurācija attiecas uz visiem šiem piemēriem.

-   Juridiskās personas ir Fabrikam, Fabrikam East un Fabrikam West. Debitora maksājumi tiek ievadīti juridiskajai personai Fabrikam.
-   Lauks **Grāmatot termiņatlaidi** lapā **Starpuzņēmumu uzskaite** ir iestatīts uz **Rēķinā norādītā juridiskā persona**.
-   Lauks **Grāmatot valūtas maiņas ieguvumus vai zaudējumus** lapā **Starpuzņēmumu uzskaite** ir iestatīts uz **Maksājumā norādītā juridiskā persona**.
-   Debitors Northwind Traders ir iestatīts kā debitors katrā juridiskajā personā. Debitori no dažādajām juridiskajām personām tiek identificēti kā tas pats debitors, jo viņi koplieto vienu un to pašu globālo adrešu grāmatas ID.

| Adrešu grāmatas ID | Debitora konts | Nosaukums              | Juridiska persona  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Fabrikam East |
| 4050            | 10000            | Northwind Traders | Fabrikam West |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>1. piemērs. Debitora maksājums par rēķinu no citas juridiskās personas
Fabrikam saņem maksājumu par 600,00 Fabrikam debitora kontam 4000, uzņēmumam Northwind Traders. Šis maksājums tiek segts ar neapmaksātu rēķinu debitora kontam 4000 uzņēmumā Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Rēķins tiek grāmatots uzņēmumā Fabrikam East debitoram 4000

| Konts                             | Summa debetā | Summa kredītā |
|-------------------------------------|--------------|---------------|
| Debitoru parādi (Fabrikam East) | 600,00       |               |
| Pārdošanas (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Maksājums ir saņemts un grāmatots sadaļā Fabrikam klientam 4000

| Konts                        | Summa debetā | Summa kredītā |
|--------------------------------|--------------|---------------|
| Skaidra nauda (Fabrikam)                | 600,00       |               |
| Debitoru parādi (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam maksājums tiek nosegts ar Fabrikam East rēķinu

**Fabrikam grāmatošana**

| Konts                         | Summa debetā | Summa kredītā |
|---------------------------------|--------------|---------------|
| Debitoru parādi (Fabrikam)  | 600,00       |               |
| Fabrikam East (Fabrikam) kreditora parādi |              | 600,00        |

**Fabrikam East grāmatojums**

| Konts                             | Summa debetā | Summa kredītā |
|-------------------------------------|--------------|---------------|
| Fabrikam (Fabrikam East) debitora parādi   | 600,00       |               |
| Debitoru parādi (Fabrikam East) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>2. piemērs. Debitora rēķina maksājums no citas juridiskās personas ar termiņatlaidi
Fabrikam saņem maksājumu par 580,00 Fabrikam debitoram 4000, uzņēmumam Northwind Traders. Fabrikam East ir atvērts rēķins debitoram 4000. Rēķinam ir pieejama 20,00 termiņatlaide. Maksājums tiek segts ar neapmaksātajiem Fabrikam East rēķiniem. Termiņatlaide tiek grāmatota rēķinā norādītajā juridiskajā personā — Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Rēķini ir grāmatoti sadaļā Fabrikam East, Fabrikam East klientam 4000

| Konts                             | Debeta summa | Kredīta summa |
|-------------------------------------|--------------|---------------|
| Debitoru parādi (Fabrikam East) | 580.00       |               |
| Pārdošanas (Fabrikam East)               |              | 580.00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Maksājums ir saņemts un grāmatots sadaļā Fabrikam, Fabrikam klientam 4000

| Konts                        | Summa debetā | Summa kredītā |
|--------------------------------|--------------|---------------|
| Skaidra nauda (Fabrikam)                | 600,00       |               |
| Debitoru parādi (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam maksājums tiek nosegts ar Fabrikam East rēķinu

**Fabrikam grāmatošana**

| Konts                         | Summa debetā | Summa kredītā |
|---------------------------------|--------------|---------------|
| Debitoru parādi (Fabrikam)  | 580,00       |               |
| Fabrikam East (Fabrikam) kreditora parādi |              | 580,00        |

**Fabrikam East grāmatojums**

| Konts                             | Summa debetā | Summa kredītā |
|-------------------------------------|--------------|---------------|
| Fabrikam (Fabrikam East) debitora parādi   | 580,00       |               |
| Debitoru parādi (Fabrikam East) |              | 580,00        |
| Termiņatlaide (Fabrikam East)       | 20,00        |               |
| Debitoru parādi (Fabrikam East) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>3. piemērs. Debitora rēķina maksājums no citas juridiskās personas ar realizēto maiņas kursa ieguvumu
Fabrikam saņem maksājumu par 600,00 EUR Fabrikam debitoram 4000 — uzņēmumam Northwind Traders. Maksājums tiek segts ar neapmaksātu rēķinu debitoram 4000 uzņēmumā Fabrikam East. Valūtas maiņas ieguvuma darbība tiek izveidota segšanas procesa laikā.

-   Maiņas kurss no EUR uz ASV dolāriem (USD) rēķina datumā: 1,2062
-   Maiņas kurss no EUR uz USD maksājuma datumā: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Rēķini ir grāmatoti sadaļā Fabrikam East, Fabrikam East klientam 4000

| Konts                             | Summa debetā            | Summa kredītā           |
|-------------------------------------|-------------------------|-------------------------|
| Debitoru parādi (Fabrikam East) | 600,00 EUR / 723,72 USD |                         |
| Pārdošanas (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Maksājums ir saņemts un grāmatots sadaļā Fabrikam, Fabrikam klientam 4000

| Konts                        | Summa debetā            | Summa kredītā           |
|--------------------------------|-------------------------|-------------------------|
| Skaidra nauda (Fabrikam)                | 600,00 EUR / 736,62 USD |                         |
| Debitoru parādi (Fabrikam) |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam maksājums tiek nosegts ar Fabrikam East rēķinu

**Fabrikam grāmatošana**

| Konts                         | Summa debetā            | Summa kredītā           |
|---------------------------------|-------------------------|-------------------------|
| Debitoru parādi (Fabrikam)  | 600,00 EUR / 736,62 USD |                         |
| Fabrikam East (Fabrikam) kreditora parādi |                         | 600,00 EUR / 736,62 USD |
| Fabrikam East (Fabrikam) kreditora parādi | 0,00 EUR / 12,90 USD    |                         |
| Realizētais pastiprinājums (Fabrikam)        |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East grāmatojums**

| Konts                             | Summa debetā            | Summa kredītā           |
|-------------------------------------|-------------------------|-------------------------|
| Fabrikam (Fabrikam East) debitora parādi   | 600,00 EUR / 736,62 USD |                         |
| Debitoru parādi (Fabrikam East) |                         | 600,00 EUR / 736,62 USD |
| Debitoru parādi (Fabrikam East) | 0,00 EUR / 12,90 USD    |                         |
| Fabrikam (Fabrikam East) debitora parādi   |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>4. piemērs. Debitora rēķina maksājums no citas juridiskās personas ar termiņatlaidi un realizēto maiņas kursa ieguvumu
Fabrikam grāmato maksājumu Fabrikam debitoram 4000, Northwind Traders, par neapmaksātu rēķinu uzņēmumā Fabrikam East. Šim rēķinam ir pieejama termiņatlaide, un ir izveidota pārdošanas nodokļa transakcija. Maksājums tiek segts ar neapmaksāto Fabrikam East rēķinu. Valūtas maiņas ieguvuma darbība tiek izveidota segšanas procesa laikā. Termiņatlaide tiek grāmatota rēķinā norādītajai juridiskajai personai (Fabrikam East), un valūtas maiņas ieguvums tiek grāmatots maksājumā norādītajai juridiskajai personai (Fabrikam).

-   Maiņas kurss no EUR uz USD rēķina datumā: 1,2062
-   Maiņas kurss no EUR uz USD maksājuma datumā: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>Fabrikam East debitoram 4000 tiek grāmatots brīva teksta rēķins un izveidota nodokļu darbība

| Konts                             | Summa debetā            | Summa kredītā           |
|-------------------------------------|-------------------------|-------------------------|
| Debitoru parādi (Fabrikam East) | 638,22 EUR / 769,82 USD |                         |
| Pārdošanas (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |
| PVN (Fabrikam East)           |                         | 38,22 EUR / 46,10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Maksājums ir saņemts un grāmatots sadaļā Fabrikam klientam 4000

| Konts                        | Summa debetā            | Summa kredītā           |
|--------------------------------|-------------------------|-------------------------|
| Skaidra nauda (Fabrikam)                | 626,22 EUR / 768,81 USD |                         |
| Debitoru parādi (Fabrikam) |                         | 626,22 EUR / 768,81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam maksājums tiek nosegts ar Fabrikam East rēķinu

**Fabrikam grāmatošana**

| Konts                         | Summa debetā            | Summa kredītā           |
|---------------------------------|-------------------------|-------------------------|
| Debitoru parādi (Fabrikam)  | 626,22 EUR / 768,81 USD |                         |
| Fabrikam East (Fabrikam) kreditora parādi |                         | 626,22 EUR / 768,81 USD |
| Fabrikam East (Fabrikam) kreditora parādi | 0,00 EUR / 13,46 USD    |                         |
| Realizētais pastiprinājums (Fabrikam)        |                         | 0,00 EUR / 13,46 USD    |

**Fabrikam East grāmatojums**

| Konts                             | Summa debetā            | Summa kredītā           |
|-------------------------------------|-------------------------|-------------------------|
| Fabrikam (Fabrikam East) debitora parādi   | 626,22 EUR / 768,81 USD |                         |
| Debitoru parādi (Fabrikam East) |                         | 626,22 EUR / 768,81 USD |
| Debitoru parādi (Fabrikam East)  | 0,00 EUR / 13,46 USD    |                         |
| Fabrikam (Fabrikam East) debitora parādi   |                         | 0,00 EUR / 13,46 USD    |
| Termiņatlaide (Fabrikam East)       | 12,00 EUR / 14,47 USD   |                         |
| Debitoru parādi (Fabrikam East) |                         | 12,00 EUR / 14,47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>5. piemērs: debitora kredīta nota ar primāro maksājumu
Fabrikam saņem maksājumu par 75,00 no debitora 4000, uzņēmuma Northwind Traders. Šis maksājums tiek segts ar neapmaksātu rēķinu Fabrikam West debitoram 10000 un neapmaksātu kredīta notu Fabrikam East debitoram 4000. Šis maksājums tiek atlasīts kā primārais maksājums lapā **Segt transakcijas**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Rēķins ir grāmatots Fabrikam West, klientam 10000

| Konts                             | Summa debetā | Summa kredītā |
|-------------------------------------|--------------|---------------|
| Debitoru parādi (Fabrikam West) | 100,00       |               |
| Pārdošanas (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kredīta nota ir grāmatota Fabrikam East, klientam 4000

| Konts                             | Summa debetā | Summa kredītā |
|-------------------------------------|--------------|---------------|
| Pārdošanas ienesīgums (Fabrikam East)       | 25,00        |               |
| Debitoru parādi (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Maksājums ir grāmatots Fabrikam, klientam 4000

| Konts                        | Summa debetā | Summa kredītā |
|--------------------------------|--------------|---------------|
| Skaidra nauda (Fabrikam)                | 75,00        |               |
| Debitoru parādi (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam maksājums ir nosegts ar Fabrikam West rēķinu un Fabrikam East kredīta notu

**Fabrikam grāmatošana**

| Konts                           | Summa debetā | Summa kredītā |
|-----------------------------------|--------------|---------------|
| Fabrikam East (Fabrikam) debitora parādi | 25,00        |               |
| Debitoru parādi (Fabrikam)    |              | 25,00         |
| Debitoru parādi (Fabrikam)    | 100,00       |               |
| Jāmaksā Fabrikam West (Fabrikam)   |              | 100,00        |

**Fabrikam East grāmatojums**

| Konts                             | Summa debetā | Summa kredītā |
|-------------------------------------|--------------|---------------|
| Debitoru parādi (Fabrikam East) | 25,00        |               |
| Fabrikam (Fabrikam East) kreditora parādi     |              | 25,00         |

**Fabrikam West grāmatošana**

| Konts                             | Summa debetā | Summa kredītā |
|-------------------------------------|--------------|---------------|
| Jāsaņem no Fabrikam (Fabrikam West)   | 100,00       |               |
| Debitoru parādi (Fabrikam West) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>6. piemērs: debitora kredīta nota bez primārā maksājuma
Fabrikam saņem maksājumu par 75,00 no debitora 4000, uzņēmuma Northwind Traders. Šis maksājums tiek segts ar neapmaksātu rēķinu Fabrikam West debitoram 10000 un neapmaksātu kredīta notu Fabrikam East debitoram 4000. Šis maksājums netiek atlasīts kā primārais maksājums lapā **Segt transakcijas**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Rēķins ir grāmatots Fabrikam West, klientam 10000

| Konts                             | Summa debetā | Summa kredītā |
|-------------------------------------|--------------|---------------|
| Debitoru parādi (Fabrikam West) | 100,00       |               |
| Pārdošanas (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kredīta nota ir grāmatota Fabrikam East, klientam 4000

| Konts                             | Summa debetā | Summa kredītā |
|-------------------------------------|--------------|---------------|
| Pārdošanas ienesīgums (Fabrikam East)       | 25,00        |               |
| Debitoru parādi (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Maksājums ir grāmatots Fabrikam, klientam 4000

| Konts                        | Summa debetā | Summa kredītā |
|--------------------------------|--------------|---------------|
| Skaidra nauda (Fabrikam)                | 75,00        |               |
| Debitoru parādi (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam maksājums ir nosegts ar Fabrikam West rēķinu un Fabrikam East kredīta notu

**Fabrikam grāmatošana**

| Konts                         | Summa debetā | Summa kredītā |
|---------------------------------|--------------|---------------|
| Debitoru parādi (Fabrikam)  | 75,00        |               |
| Jāmaksā Fabrikam West (Fabrikam) |              | 75,00         |

**Fabrikam East grāmatojums**

| Konts                              | Summa debetā | Summa kredītā |
|--------------------------------------|--------------|---------------|
| Debitoru parādi (Fabrikam East)  | 25,00        |               |
| Maksājuma saņēmējs - Fabrikam West (Fabrikam East) |              | 25,00         |

**Fabrikam West grāmatošana**

| Konts                                | Summa debetā | Summa kredītā |
|----------------------------------------|--------------|---------------|
| Jāsaņem no Fabrikam (Fabrikam West)      | 75,00        |               |
| Debitoru parādi (Fabrikam West)    |              | 75,00         |
| Maksājuma veicējs - Fabrikam East (Fabrikam West) | 25,00        |               |
| Debitoru parādi (Fabrikam West)    |              | 25,00         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]