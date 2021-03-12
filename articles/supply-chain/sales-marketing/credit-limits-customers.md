---
title: Debitoru kredīta limiti
description: Šajā rakstā ir sniegts apskats par to, kā darbojas kredīta limiti programmā Dynamics 365 Supply Chain Management.
author: omulvad
manager: tfehr
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc991e03ba88846a8077fbebb7a7412c8abe1f18
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994106"
---
# <a name="credit-limits-for-customers"></a>Debitoru kredīta limiti

[!include [banner](../includes/banner.md)]

Kredīta limita iestatīšana jums ļauj norādīt maksimālo kredīta summu, kādu pagarināt saviem debitoriem. Ja ir norādīts kredīta limits, tas tiek automātiski pārbaudīts, kad lietotājs mēģina atjaunināt dokumentu. Ja kredīta limits ir pārsniegts, lietotājam tiek parādīts ziņojums. Šajā rakstā ir sniegts apskats par to, kā darbojas kredīta limiti, un ir sniegtas atbildes uz šādiem jautājumiem:

-   Kādiem dokumentiem un procesiem var pārbaudīt kredīta limitus?

-   Kur konfigurēt veidu, kā tiek aprēķināts debitora atlikušais kredīts?

-   Kur tiek izmantota informācija par debitora atlikušo kredītu?

-   Kur norādīt, vai debitoram pagarināmam kredītam ir nepieciešama identifikācija, kā arī kredīta limita summu, kurai ir nepieciešama identifikācija?

-   Kur norādīt, vai ir jāparāda brīdinājums vai kļūda, ja tiek pārsniegts kredīta limits?

-   Kā norādīt kredīta limitu konkrētam debitoram?

-   Kā kredīta limitus manuāli pārbaudīt pārdošanas pasūtījumos?

**Kādiem dokumentiem un procesiem var pārbaudīt kredīta limitus?**

Lai norādītu, kuriem dokumentiem pārbaudīt kredīta limitus, izmantojiet formu **Debitoru parādu parametri**. Lai varētu veikt izmaiņas šajā formā, jums ir jābūt drošības lomas Sistēmas administrators (-SYSADMIN-) dalībniekam. Kredīta limitus varat pārbaudīt tālāk uzskaitītajiem dokumentiem un procesiem.

-   Rēķini pārdošanas pasūtījumiem, kad grāmatojat rēķinus

-   Pavadzīmes pārdošanas pasūtījumiem, kad atjaunināt pavadzīmes

-   Pārdošanas pasūtījumi, kad pievienojat rindas formā **Pārdošanas pasūtījums**

-   Pārdošanas pasūtījumi, kad tie tiek izveidoti, izmantojot pakalpojumu

-   Brīva teksta rēķini, kad šos rēķinus grāmatojat

Kredīta limiti tiek pārbaudīti automātiski, ja ir iestatīta kāda no tālāk norādītajām opcijām.

-   Formā **Debitoru parādu parametri** lauks **Kredīta limita tips** ir iestatīts uz jebkādu vērtību, izņemot **Nav**. Kredīta limiti tiek pārbaudīti visiem debitoriem.

-   Formas **Debitoru parādu parametri** lauks **Kredīta limita tips** ir iestatīts uz **Nav**, bet debitoram formā **Debitori** ir atlasīts **Obligātais kredīta limits**. Kredīta limiti tiek pārbaudīti tikai noteiktajam debitoram.

Lai kredīta limitus pārbaudītu tālāk norādītajiem dokumentiem, ir jānorāda papildu iestatījumi.

|    Dokuments                                    |    Papildu iestatījums                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Brīva teksta rēķins                         |    Formas Debitoru parādu parametri apgabalā Kredītreitings atzīmējiet opciju Pārbaudīt kredīta limitu brīva teksta rēķinā.     |
|    Pārdošanas pasūtījums (ievadīts manuāli)            |    Formas Debitoru parādu parametri apgabalā Kredītreitings atzīmējiet opciju Pārbaudīt kredīta limitu pārdošanas pasūtījumā.           |
|    Pārdošanas pasūtījums (saņemts elektroniski)     |    Formas Debitoru parādu parametri apgabalā AIF atzīmējiet opciju Pārbaudīt kredīta limitu pārdošanas pasūtījumiem.                     |

**Kur konfigurēt veidu, kā tiek aprēķināts debitora atlikušais kredīts?**

Debitora atlikušā kredītu aprēķināšanai programmatūru Dynamics 365 varat konfigurēt tālāk norādītajos veidos.

-   Kredīta limitu salīdziniet ar debitora bilanci.

-   Kredīta limitu salīdziniet ar debitora bilances un pavadzīmes summu.

-   Kredīta limitu salīdziniet ar debitora bilanci un visu atvērto transakciju darbību. Tostarp ietilpst pavadzīmju summas un pārdošanas pasūtījumu summas.

Lai norādītu informāciju, ar kuru salīdzināt, izmantojiet formu **Debitoru parādu parametri**. Lai varētu veikt izmaiņas šajā formā, jums ir jābūt drošības lomas Sistēmas administrators (-SYSADMIN-) dalībniekam. Laukā **Kredīta limita tips** atlasiet, vai ir jāveic kredīta limita pārbaudes un kāda transakciju informācija kredīta limita pārbaudes laikā ir jāietver. Atlasiet no sekojošajām opcijām:

-   **Nav** — kredīta limits nav jāpārbauda. Šo opciju noteiktam debitoram varat ignorēt, atzīmējot izvēles rūtiņu **Obligātais kredīta limits** formā **Debitori**. Tādā gadījumā kredīta limits tiek pārbaudīts pret debitora bilanci.

-   **Bilance** — kredīta limits tiek pārbaudīts pret debitora bilanci.

-   **Bilance + pavadzīme vai produktu ieejas plūsma** — kredīta limits tiek pārbaudīts pret debitora bilanci un piegādēm.

-   **Bilance+viss** — kredīta limits tiek pārbaudīts pret debitora bilanci, piegādēm un atvērtajiem pasūtījumiem.

**Kur tiek izmantota informācija par debitora atlikušo kredītu?**

Kad veidojat vecumstruktūras momentuzņēmumu, informācija par debitora bilanci un atlikušā kredīta summu tiek aprēķināta un saglabāta, un tā tiek rādīta formā **Iekasēšana**. Kamēr nav izveidots jauns vecumstruktūras momentuzņēmums, formā **Iekasēšana** rādītās summas var neietvert visas transakciju darbības. Plašāku informāciju skatiet rakstā [Iekasēšana un kredīts modulī Debitoru parādi](https://technet.microsoft.com/library/hh209221.aspx).

Atkarībā no atlasītajiem dokumentiem informācija par debitora bilanci un atlikušo kredīta summu tiek aprēķināta, kad tiek atjaunināti pārdošanas pasūtījumi, pavadzīmes un debitora rēķini. Ja tā dokumenta summa, ar kuru strādājat, izraisītu kredīta limita pārsniegšanu, tiek parādīts ziņojums.

**Kur norādīt, vai debitoram pagarināmam kredītam ir nepieciešama identifikācija, kā arī kredīta limitu, kuram ir nepieciešama identifikācija?**

Lai norādītu, vai pieprasīt identifikāciju un kādai kredīta limita summai šo identifikāciju pieprasīt, izmantojiet formu **Debitoru parādu parametri**.
Lai varētu veikt izmaiņas šajā formā, jums ir jābūt drošības lomas Sistēmas administrators (-SYSADMIN-) dalībniekam.

|    Lauks                                    |    Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Ar kredītu pieprasīt identifikāciju     |    Izvēlieties identifikācijas tipu, kas ir jāievada debitoriem, kuriem jūsu juridiskā iestāde pagarina kredītu. Šajā laukā atlasītā opcija nosaka, kad un kāda tipa informācija ir nepieciešama formas Debitori laukos Valsts iestādes izsniegta identifikācija.        Nē — neatkarīgi no debitora kredīta limita nav nepieciešama valsts iestādes izsniegta identifikācija.     Jā — ja debitora kredīta limits ir lielāks par vai vienāds ar nulli, ir nepieciešams valsts iestādes izsniegts licences numurs vai cita valsts iestādes izsniegta identifikācija.     Minimālais limits — valsts iestādes izsniegts licences numurs vai cita valsts iestādes izsniegta identifikācija ir nepieciešama, ja debitora kredīta limits ir lielāks par vai vienāds ar limitu, kuru ievadāt šīs formas laukā Limits.        |
|    Limits                                    |    Ievadiet kredīta limitu, pie kura debitoriem ir nepieciešams valsts iestādes izsniegts licences numurs vai cita identifikācija.    Ierakstiet, piemēram, 2000, lai pieprasītu ievadīt kādu identifikācijas numuru, piemēram, autovadītāja apliecības numuru, tādiem debitoriem, kuru kredīta limits ir 2000 vai vairāk.    Šis lauks ir pieejams, ja laukā Ar kredītu pieprasīt identifikāciju atlasījāt vienumu Minimālais limits.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Kur norādīt, vai ir jāparāda brīdinājums vai kļūda, ja tiek pārsniegts kredīta limits?**

Lai norādītu, vai ir jāparāda brīdinājums vai kļūda, ja tiek pārsniegts kredīta limits, izmantojiet formu **Debitoru parādu parametri**. Šī brīdinājuma vai kļūda tiks parādīts, kad lietotājs ievada vai grāmato informāciju, vai tas tiek ietverts žurnālā, kad dokumenti tiek apstrādāti, izmantojot elektronisku pakalpojumu. Lai varētu veikt izmaiņas šajā formā, jums ir jābūt drošības lomas Sistēmas administrators (-SYSADMIN-) dalībniekam.

|    Lauks                                                               |    Apraksts                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Ziņojums, pārsniedzot kredīta limitu (apgabalā Kredītreitings)     |    Atlasiet, kā lietotājiem tiek rādīti ziņojumi par kredīta limitu pārsniegšanu. Atlasiet no tālāk aprakstītajām opcijām.        Kļūda — tiek parādīts kļūdas ziņojums. Tas parasti pārtrauc pašreizējo operāciju, un pirms procesa turpināšanas konflikts ir jāatrisina.     Brīdinājums — tiek parādīts brīdinājuma ziņojums, bet procesu var turpināt.                     |
|    Ziņojums, pārsniedzot kredīta limitu (apgabalā AIF)               |    Atlasiet, kā ziņojumi par kredīta limita pārsniegšanu tiek piegādāti žurnālā. Atlasiet no tālāk aprakstītajām opcijām.        Kļūda — formā Izņēmumi tiek parādīts kļūdas ziņojums, un dokuments netiek apstrādāts, kamēr kļūda nav atrisināta.     Brīdinājums — formā Izņēmumi tiek parādīts brīdinājuma ziņojums, bet procesu var turpināt.        |

**Kā norādīt kredīta limita summu konkrētam debitoram?**

Lai kredīta limita summu norādītu konkrētam debitoram, izmantojiet formu **Debitori**. Lai veiktu izmaiņas šajā formā, jums ir jābūt dalībniekam ar tādu drošības lomu, kurai ir piešķirts pienākums Uzturēt debitoru pamatdatus (CustCustomersMaintain).

1.  Noklikšķiniet uz **Debitoru parādi** \> **Vispārīgi** \> **Debitori** \> **Visi debitori**. Veiciet dubultklikšķi uz debitora konta.

2.  Formas **Debitori** darbību rūtī noklikšķiniet uz **Rediģēt**.

3.  Ievadiet valūtas summu laukā **Kredīta limits**. Šai vērtībai ir jābūt lielākai par nulli (0), un tā tiks izmantota kā kredīta limita summa.

4.  Ja nepieciešams, laukā **Valsts iestādes izsniegta identifikācija** ievadiet licences numuru vai citu valsts iestādes izsniegtu identifikāciju.

> [!NOTE]
> Formā **Debitoru parādu parametri** parasti ir atlasīts kredīta limita tips. Taču, ja kredīta limita tips ir iestatīts uz **Nav**, tad jums ir jāatzīmē arī izvēles rūtiņa **Obligātais kredīta limits** formā **Debitori**, lai debitora kredīta limitu pārbaudītu pret šī debitora bilanci. Plašāku informāciju par kredīta limita tipiem skatiet šīs tēmas sadaļā “Kādiem dokumentiem un procesiem var pārbaudīt kredīta limitus?” . 

**Kā kredīta limitus manuāli pārbaudīt pārdošanas pasūtījumos?**

Reizēm debitora kredīta limitu var būt nepieciešams pārbaudīt manuāli. Debitora kredīta limitu varat manuāli pārbaudīt, piemēram, pirms sākat ievadīt pārdošanas pasūtījumu. Lai kredīta limitus pārbaudītu manuāli, varat izmantot formu **Pārdošanas pasūtījums**. Lai veiktu izmaiņas šajā formā, jums ir jābūt dalībniekam ar tādu drošības lomu, kurai ir piešķirts pienākums Uzturēt pārdošanas pasūtījumu (SalesOrderMaintain).

1.  Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Pārdošanas pasūtījumi** \> **Visi pārdošanas pasūtījumi**. Veiciet dubultklikšķi uz pārdošanas pasūtījuma.

2.  Formas **Pārdošanas pasūtījums** darbību rūts cilnē **Pārvaldīt** noklikšķiniet uz **Pārbaudīt kredīta limitu**.
