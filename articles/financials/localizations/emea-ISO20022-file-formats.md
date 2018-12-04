---
title: "ISO20022 failu importēšana"
description: "Šajā tēmā izskaidrots, kā importēt maksājumu failus ISO 20022 camt.054 un pain.002 formātā programmā Microsoft Dynamics 365 for Finance and Operations."
author: neserovleo
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, CustBankAccounts, VendPaymMode, VendBankAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: f55e8fbc4d13f84686298cb8dbcebb4baf134cf3
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="import-iso20022-files"></a>Importēt ISO20022 failus

[!include [banner](../includes/banner.md)]

Varat importēt maksājumu failus, kas ir tālāk norādītajos formātos.

 - **ISO20022 camt.054 kredīta izziņa** – importējiet ienākošos maksājumus no šī formāta faila debitoru maksājumu žurnālā.
 - **ISO20022 pain.002 atgrieztais statuss** un **ISO20022 camt.054 debeta izziņa** — importējiet atgriešanas failus šajos formātos kreditoru maksājumu pārsūtījumu žurnālā.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Priekšnosacījumi camt.054 kredīta izziņas faila importēšanai
Lai bankas paziņojumus camt.054.001.002 formātā varētu importēt debitoru maksājumu žurnālā, jums ir jāizpilda tālāk norādītie priekšnosacījumi.

1. Importējiet **ISO20022 camt.054** elektronisko pārskatu veidošanas (ER) konfigurāciju no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS). Pēc tam lapas **Debitora maksāšanas metode** laukā **Importēt formāta konfigurāciju** atlasiet šo konfigurāciju. Papildinformāciju skatiet rakstā [Maksāšanas metožu failu formāti](emea-select-file-formats-for-the-method-of-payments.md).
2. Lapā **Visi debitori** ievadiet katra debitora nosaukumu un organizācijas numuru.
3. Lapā **Debitora bankas konts** iestatiet debitora bankas konta ierakstu, ievadot šādu informāciju: IBAN vai bankas konta numurs un SWIFT kods vai reģistrācijas numurs.
4. Lapā **Bankas konti** iestatiet juridiskās personas bankas kontus, ievadot šādu informāciju: IBAN vai bankas konta numurs un SWIFT kods vai reģistrācijas numurs, valūta un adrese.

   > [!NOTE]
   > Ja plānojat izmantot opciju Detalizēta bankas darbību saskaņošana, kopsavilkuma cilnē **Saskaņošana** opciju **Detalizēta bankas darbību saskaņošana** iestatiet uz **Jā**. Ja plānojat saskaņot negrāmatotos importētos maksājumus, opciju **Lietot bankas izrakstus kā elektronisko maksājumu apstiprinājumu** iestatiet uz **Jā**.

5. Neobligāti: lapā **Transakciju kodu kartēšana** iestatiet kartēšanu starp bankas transakciju kodiem failā un bankas transakciju tipiem.
6. Ja fails satur transakciju maksas, ko vēlaties grāmatot kopā ar ienākošo maksājumu, izveidojiet komisijas maksu lapā **Debitoru komisijas maksas**. Pēc tam lapā **Maksāšanas metodes** saistiet komisijas maksu ar bankas kontu komisijas maksu iestatījumos.
7. Ja ESR maksājumi tiks importēti un saturēs ISR atsauces (attiecas uz juridiskajām personām Šveicē), veiciet tālāk norādītos iestatījumus.

    - Laukā **Debitoru maksājumi, kontu garumi** ievadiet garumu debitora kodam, kas tiek izmantots ISR atsaucēs vai automātiskai debitora identifikācijai.
    - Pārliecinieties, vai debitora numurs un rēķina numurs (numuru sērijas) satur tikai ciparus. Tajos nedrīkst būt ietvertas citas rakstzīmes. Rēķina numurs nedrīkst sākties ar nullēm.
    - Ievadiet ESR, BESR un reģistrācijas numuru juridiskās personas bankas kontam. Papildinformāciju skatiet rakstā [Mantojuma ESR līdzeklis](emea-che-esr-customer-payments-import.md), jo tajā ir nepieciešami līdzīgi iestatījumi.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>camt.054 kredīta izziņas faila importēšana debitoru maksājumu žurnālā
1. Lapā **Debitoru maksājumu žurnāla rindas** noklikšķiniet uz **Funkcijas** > **Importēt maksājumus**.
2. Atlasiet maksāšanas metodi, kam ir ISO20022 camt.054 formātam nepieciešamie iestatījumi.
3. Norādiet nepieciešamos parametrus un faila ceļu un pēc tam noklikšķiniet uz **Labi**. Fails tiek importēts.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>Priekšnosacījumi failu importēšanai pain.002 atgrieztā statusa un camt.054 debeta izziņas formātos kreditoru maksājumu pārsūtījumu žurnālā
Lai bankas ziņojumus importētu šādos ISO20022 formātos lapā **Kreditoru maksājumu pārsūtīšana**: pain.002.001.003 atgrieztā statusa ziņojumi un camt.054.001.002 debeta izziņa, ir jāizpilda tālāk norādītie priekšnosacījumi.

1. Importējiet **ISO20022 camt.054** un **ISO20022 pain.002** ER konfigurācijas no LCS.
2. Lapas **Kreditora maksāšanas metode** laukos **Atgriešanas formāta konfigurācija** un **Atgriešanas formāta sekundārā konfigurācija** atlasiet ER konfigurācijas, ko importējāt. Jums būs jāaktivizē vispārīgais elektroniskās atgriešanas formāts atlasītajai maksāšanas metodei.
3. Lapā **Atgriešanas formāta statusa kartēšana** iestatiet statusa kodu kartējumu starp pain.002 statusiem un kreditoru maksājumu žurnāla statusiem.

    Tālāk ir sniegts statusa iestatījumu piemērs.

    Atgrieztais statuss | Maksājuma statuss
    --------------|---------------
    RJCT          | Noraidījis
    ACCP          | Pieņemts
    ACSP          | Saņemts

4. Lapā **Atgriešanas formāta kļūdu kodi** iestatiet pain.002 kļūdu kodus un aprakstus saskaņā ar ārējā ISO20022 statusa iemesla kodiem.

    Tālāk ir sniegts piemērs ar daļu no kļūdas koda iestatījuma.

    Kods | Nosaukums
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Ja camt.054 fails satur transakciju maksas, ko vēlaties grāmatot kopā ar ienākošo maksājumu, izveidojiet komisijas maksu lapā **Kreditoru komisijas maksas**. Pēc tam lapā **Maksāšanas metodes** saistiet komisijas maksu ar bankas kontu komisijas maksu iestatījumos.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>pain.002 atgrieztā statusa vai camt.054 debeta izziņas failu importēšana kreditoru maksājumu žurnālā
1. Izvēlnē Kreditori atveriet lapu **Maksājumu pārsūtījumi**.
2. Lapā **Maksājumu pārsūtījumi** noklikšķiniet uz **Ievades fails — kreditors**.
3. Atlasiet maksāšanas metodi, kam ir ISO20022 failiem nepieciešamie iestatījumi, un pēc tam noklikšķiniet uz **Labi**.
4. Atlasiet faila formātu, ko plānojat importēt, un pēc tam noklikšķiniet uz **Labi**.
5. Norādiet nepieciešamos parametrus un faila ceļu un pēc tam noklikšķiniet uz **Labi**.

Ja importējat pain.002 failu, tiek atjaunināts kreditora maksājumu rindu statuss, pamatojoties uz importētā faila informāciju.

Ja importējat camt.054 failu, jums ir jānorāda tālāk norādītie papildu parametri.

- **Maksas ID** — ievadiet maksas ID, kas definēs jaunās komisijas maksas rindas, kuras tiks izveidotas kreditoru maksājumu žurnāla rindā, ja camt.054 failā būs maksas summa.
- **Jauna žurnāla nosaukums** un **Jauna žurnāla apraksts** — ievadiet tā žurnāla nosaukumu un aprakstu, uz kuru tiks pārsūtītas apstrādātās transakcijas. Pēc pārsūtīšanas jaunajā žurnālā ir jāpiešķir jauni dokumentu numuri.
- **Importēt tiešā debeta transakcijas** — iestatiet šo opciju uz **Jā**, ja izejošie tiešie debeti ir jāimportē kreditoru maksājumu žurnālā.
- **Žurnāla nosaukums** — definējiet jaunu žurnāla nosaukumu importētajām tiešā debeta transakcijām.
- **Transakciju nosegšana** — iestatiet šo opciju uz **Jā**, ja importētie kreditoru maksājumi ir jānosedz ar rēķiniem, kas ir atrasti sistēmā.

Importēto informāciju var skatīt lapā **Maksājumu pārsūtījumi**. 

## <a name="additional-details"></a>Papildu informācija

Importējot formāta konfigurāciju no LCS, tiek importēts viss konfigurācijas koks, un tas nozīmē, ka ir iekļauts modelis un modeļa kartēšana konfigurācijas. Sākot no 8. versijas, maksājumu modelī kartējumi atrodas risinājumu kokā atsevišķās ER konfigurācijās (maksājumu modeļa kartējums 1611, maksājumu modeļa kartējums līdz galamērķim ISO20022 utt.). Atsevišķā modelī ir daudz dažādu maksājuma formātu (maksājuma modelis), tādējādi kartējumu apstrāde ir galvenais nosacījums vienkāršai risinājuma uzturēšanai. Piemērs. Jūs izmantojat ISO20022 maksājumus, lai ģenerētu kredīta pārskaitījuma failus, un pēc tam importējat atbildes ziņojumus no bankas. Šādā scenārijā jums būtu jāizmanto šādas konfigurācijas:

 - **Maksājuma modelis**
 - **Maksājumu modeļa kartējums 1611** — šis kartējums tiks lietots, lai ģenerētu eksporta failu
 - **Maksājumu modeļa kartējums līdz galamērķim ISO20022** — šajā konfigurācijā ir iekļauti visi kartējumi, kas tiks izmantoti datu importēšanai (kartējuma virziens: "uz galamērķi")
 - **ISO20022 kredīta pārskaitījums** — šajā konfigurācijā ir iekļauts formāta komponents, kas ir atbildīgs par eksporta faila ģenerēšana (pain.001), pamatojoties uz maksājumu modeļa kartējumu 1611, kā arī formāta-modeļa kartējuma komponents, kas tiks izmantots kopā ar maksājumu modeļa kartējumu līdz galamērķim ISO20022, lai reģistrētu eksportētos maksājumus sistēmā turpmākas importēšanas vajadzībām (importēšana tehniskajā tabulā CustVendProcessedPayments)
 - **ISO20022 pārskaitījums (CE)**, kur CE atbilst valsts paplašinājumam — ISO20022 kredīta pārskaitījuma atvasināts formāts ar tādu pašu struktūru un konkrētajai valstij raksturīgam atšķirībām
 - **Pain.002** — šis formāts tiks izmantots kopā ar maksājumu modeļa kartējumu līdz galamērķim ISO20022, lai importētu failu pain.002 kreditoru maksājumu pārskaitījumu žurnālu
 - **Camt.054** — šis formāts tiks izmantots kopā ar maksājumu modeļa kartējumu līdz galamērķim ISO20022, lai importētu failu camt.054 kreditoru maksājumu pārskaitījumu žurnālu. Tāda pati formātu konfigurācija tiks izmantota debitoru maksājumu importēšanas funkcionalitātē, tomēr atšķirīgs kartējums tiks izmantots maksājumu modeļa kartējumā līdz galamērķa ISO20022 konfigurācijai.

Plašāku informāciju par elektronisko pārskatu veidošanu skatiet šeit: [Elektronisko pārskatu veidošanas apskats](../../dev-itpro/analytics/general-electronic-reporting.md).

## <a name="additional-resources"></a>Papildu resursi
- [Kreditoru maksājumu izveide un eksportēšana, izmantojot maksājumu formātu ISO20022](./tasks/create-export-vendor-payments-iso20022-payment-format.md)
- [ISO20022 pārvietošanai kredītā konfigurācijas importēšana](./tasks/import-iso20022-credit-transfer-configuration.md)
- [ISO20022 tiešā debeta konfigurācijas importēšana](./tasks/import-iso20022-direct-debit-configuration.md)
- [Uzņēmuma bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)
- [Uzņēmuma bankas kontu iestatīšana ISO20022 tiešajiem debetiem](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)
- [Debitoru un debitoru bankas kontu iestatīšana ISO20022 tiešajiem debetiem](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)
- [Maksājuma metodes iestatīšana ISO20022 pārvietošanai kredītā](./tasks/set-up-method-payment-iso20022-credit-transfer.md)
- [Maksājumu metodes iestatīšana ISO20022 tiešajam debetam](./tasks/setup-method-payment-iso20022-direct-debit.md)
- [Kreditoru un kreditoru bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem](./tasks/set-up-vendor-iso20022-credit-transfers.md)

