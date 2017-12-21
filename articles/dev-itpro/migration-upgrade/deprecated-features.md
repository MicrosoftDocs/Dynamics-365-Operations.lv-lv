---
title: "Novecojušie līdzekļi"
description: "Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt."
author: sericks007
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: HT
ms.sourcegitcommit: 408854737847590841814ed74209618bbf22ec23
ms.openlocfilehash: b0eb041ee1a4309b010e510e1f7428d6c930e4a0
ms.contentlocale: lv-lv
ms.lasthandoff: 11/27/2017

---

# <a name="deprecated-features"></a>Novecojušie līdzekļi

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kas ir noņemti no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma vai ko ir plānots noņemt no tā.

## <a name="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Līdzekļi, kas ir novecojuši programmatūrā Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs) ar 8. platformas atjauninājumu

### <a name="warehouse-mobile-devices-portal"></a>Noliktavas mobilo ierīču portāls

Noliktavas mobilo ierīču portāls (Warehouse mobile devices portal — WMDP) bija savrupa komponents, kas bija paredzēts lokālai lietotāja veiktai izvietošanai. Šis komponents vairs netiek atbalstīta programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise. WMDP funkcionalitāte ir aizstāta ar iekšēju programmu, kas uzlabo lietotāju iespējas. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Atbalsta pārtraukšanas iemesls**       | Funkcionalitātes dublēšanās.                        |
| **Vai ir aizstāts ar citu līdzekli?** | Jā. Šis līdzeklis ir aizstāts ar programmu Dynamics 365 for Finance and Operations — Noliktava. Papildinformāciju par iestatīšanu un priekšnoteikumiem skatiet tēmē [Programmas Microsoft Dynamics 365 for Finance and Operations — Noliktava instalēšana un konfigurēšana](../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Ietekmētie moduļi**             | Noliktavas pārvaldība, Transportēšanas pārvaldība |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Detalizētās bankas darbību atbilstības kārtula manuālai atbilstības noteikšanai

Atbilstības kārtula tika izmantota, lai atlasītu un atzīmētu bankas dokumentu, manuāli nosakot dokumentu atbilstību saskaņošanas darblapā.

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Atbalsta pārtraukšanas iemesls**       | Ierobežots lietojums.                                                                         |
| **Vai ir aizstāts ar citu līdzekli?** | Nr.p.k. Saskaņojamo dokumentu atrašanai ir jāizmanto kolonnu filtrēšanas iespējas. |
| **Ietekmētie moduļi**             | Kases un bankas vadība                                                               |

### <a name="windows-8-tablet-app"></a>Windows 8 planšetdatoru programma

Windows 8 planšetdatoru programma nodrošināja izdevumu ievades un apstiprināšanas funkcijas.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Atbalsta pārtraukšanas iemesls**       | Programmatūra Dynamics 365 for Finance and Operations ir saderīga ar planšetdatoriem. Planšetdatoru programma vairs nav nepieciešama. |
| **Vai ir aizstāts ar citu līdzekli?** | Nr.p.k.                                                                                      |
| **Ietekmētie moduļi**             | Izmaksu pārvaldība                                                                       |


## <a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Līdzekļi, kas ir novecojuši versijā Dynamics 365 for Operations 1611 ar 3. platformas atjauninājumu

### <a name="aeb-payment-formats-for-spain"></a>AEB maksājumu formāti Spānijai

Consejo Superior Bancario maksājumu formāti tiek izmantoti, lai nosūtītu pārskaitījumu failus uz banku debitoru un kreditoru maksājumiem. Šo formātu saturu nosaka Asociación Española de Banca. Tas attiecas uz Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šie maksājumu formāti vairs netiek izmantoti.                                  |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO20022 formātiem Kredīta pārskaitījums un Tiešā debeta maksājums Spānijai |
| **Ietekmētie moduļi**             | Parādi kreditoriem, Debitoru parādi                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Bankas maksājumu pārskaitījums Lietuvai

Bankas maksājumu pārskaitījumi tiek ģenerēti un drukāti, Lietuvai izmantojot eksporta formātu Maksājuma pārsūtījums (LT). Lietuvas tirgus 2005. gadā sāka izmantot LITAS — vienoto elektronisko banku sistēmu.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šie maksājumu formāti vairs netiek izmantoti.                    |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Lietuvai |
| **Ietekmētie moduļi**             | Parādi kreditoriem                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Maksājumu formāti BBS Direkte Remittering Norvēģijai

Maksājumu formāti BBS Direkte Remittering ietver debitora maksājuma iekasēšanas eksportēšanu (tiešais debets) un atgrieztā ziņojuma importēšanu.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šie maksājumu formāti vairs netiek izmantoti.                                                                                                                        |
| **Vai aizstāts ar citu līdzekli?** | Tiešā debeta ziņojumu ģenerēšanai Norvēģijai var izmantot maksājumu formātu AvtaleGiro debitors. Atgrieztā ziņojuma importēšana tiks ieviesta turpmākajos laidienos. |
| **Ietekmētie moduļi**             | Parādi kreditoriem, Debitoru parādi                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Rīks Kontu plāns Spānijai

Šis rīks tiek lietots, kad kontu plānam Spānijā ir nepieciešamas būtiskas izmaiņas. Lietotāji jauno kontu plānu var importēt Microsoft Excel vai teksta formātā, kā arī var importēt finanšu pārskatus.

|                              |                |
|------------------------------|----------------|
| **Novecošanas pamatojums**       | Ierobežots lietojums  |
| **Vai aizstāts ar citu līdzekli?** | Nē             |
| **Ietekmētie moduļi**             | Virsgrāmata |

### <a name="dom80-payment-format-for-belgium"></a>Maksājuma formāts Dom80 Beļģijai

Mantojuma Beļģijas maksājuma formāts maksājumu iekasēšanai (tiešais debets).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Novecošanas pamatojums**      | Šis maksājuma formāts vairs netiek izmantots.                  |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO 20022 maksājuma formātu Tiešais debets Beļģijai |
| **Ietekmētie moduļi**            | Debitoru parādi                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG maksājumu formāti Šveicei

AMNA/EZAG formāti ir integrēti ESR sistēmā, jo tiem var būt atsauces numurs. Tā kā atsauces numurs nav obligāts, šos formātus var izmantot, lai apstrādātu jebkurus kreditoru maksājumus. Šos formātus lieto uzņēmumi, kuru bankas konta atrašanās vieta nav “Postfinance”.

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šie maksājumu formāti vairs netiek izmantoti.                      |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Šveicei |
| **Ietekmētie moduļi**             | Parādi kreditoriem                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>Maksājumu formāts EDIFACT-DIRDEB Austrijai

Maksājuma formāts EDIFACT-DIRDEB maksājumu iekasēšanai (tiešais debets).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Novecošanas pamatojums**       | Šis maksājuma formāts vairs netiek izmantots.                  |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO 20022 maksājuma formātu Tiešais debets Austrijai |
| **Ietekmētie moduļi**             | Debitoru parādi                                    |

### <a name="edivat-for-belgium"></a>EDIVAT Beļģijai

EDIVAT ir novecojis Beļģijas standarts elektroniskajai deklarēšanai, izmantojot drošu pastu. Microsoft Dynamics AX 2012 patur tikai lasāmo risinājumu, lai ļautu piekļūt vēsturiskajiem datiem.

|                              |                                      |
|------------------------------|--------------------------------------|
| **Novecošanas pamatojums**       | Šī funkcionalitāte vairs netiek izmantota. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                   |
| **Ietekmētie moduļi**             | Virsgrāmata                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>Maksājumu importēšanas formāts eGiro EDIFACT CREMUL Norvēģijai

eGiro ir balstīts uz starptautisko standartu UN EDIFACT CREMUL (Daudzkārtēja kredīta izziņas paziņojums), kurš tiek izmantots automātiskai debitoru maksājumu grāmatošanai. Programmā Microsoft Dynamics AX eGiro ir ieviests kā debitoru maksājumu importēšanas formāts.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šis maksājuma formāts vairs netiek izmantots.                                                     |
| **Vai aizstāts ar citu līdzekli?** | Nē. Turpmākajos laidienos šis formāts tiks aizstāts ar ISO 20022 izraksta importēšanas formātiem. |
| **Ietekmētie moduļi**             | Debitoru parādi                                                                       |

### <a name="external-inventory-for-poland"></a>Ārējie krājumi Polijai

Pierādījums par precēm, kas no kreditora tiek ņemtas pārdošanai bez pirkšanas. Preces, ar kurām darbības tiek veiktas ārējos krājumos, neietekmē standarta krājumus, un tās var pārdot un pēc tam iegādāties automātiski. Šis process izveido reālu krājumu kustības.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| **Novecošanas pamatojums**       | Aizstāts ar citu līdzekli                     |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar pamata funkcionalitāti Ienākošs sūtījums |
| **Ietekmētie moduļi**             | Parādi kreditoriem, Krājumu vadība          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finanšu pārskatu ģenerators Austrumeiropai

Tiek izmantots rīks, lai iestatītu uzskaites un nodokļu pārskatu datu vākšanu un eksportētu datus uz XLS un DOC pārskatu veidnēm.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Ierobežots lietojums                                                                            |
| **Vai aizstāts ar citu līdzekli?** | Nē. Turpmākajos laidienos šis rīks tiks aizstāts ar elektronisko pārskatu veidošanas konfigurācijām. |
| **Ietekmētie moduļi**             | Virsgrāmata                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Debitora maksājumu transakciju importēšana Somijai

Varat atlasīt importa formātu Somijas maksājumiem, lai importētu debitoru maksājumu transakcijas no bankas nodrošināta ārēja faila.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šis maksājuma formāts vairs netiek izmantots.                                                     |
| **Vai aizstāts ar citu līdzekli?** | Nē. Turpmākajos laidienos šis formāts tiks aizstāts ar ISO 20022 izraksta importēšanas formātiem. |
| **Ietekmētie moduļi**             | Debitoru parādi                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Maksājumu transakciju importēšana virsgrāmatas žurnālā Somijai

Formāts, kas ir raksturīgs Somijai, tiek izmantots, lai virsgrāmatā importētu uzskaites transakcijas.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šis maksājuma formāts vairs netiek izmantots.                                                     |
| **Vai aizstāts ar citu līdzekli?** | Nē. Turpmākajos laidienos šis formāts tiks aizstāts ar ISO 20022 izraksta importēšanas formātiem. |
| **Ietekmētie moduļi**             | Debitoru parādi                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integrācija ar Isabel sinhronizēto (CIS) Beļģijai

Isabel ir elektroniskās banku sistēmas struktūra Eiropā un faktiskais standarts Beļģijā.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Integrēšana ar Isabel klientu ir pārtraukta.                                                                |
| **Vai aizstāts ar citu līdzekli?** | Nē. Maksājumu formāti, kas vairs netiek izmantoti, tiek aizstādi ar ISO20022 maksājuma formātu Kredīta pārskaitījums Beļģijai. |
| **Ietekmētie moduļi**             | Parādi kreditoriem                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Kontu plāna un uzskaites nosacījumu modifikācijas Spānijai

Šis līdzeklis tiek izmantots kontu plāna un uzskaites nosacījumu izmaiņām Spānijā. Tas kartē kontus, lai veco kontu plānu palīdzētu pārveidot par jaunu kontu plānu, un iepriekšējo finanšu gadu salīdzina ar jauno finanšu gadu, pat ja tie tika grāmatoti dažādos kontu numuros.

|                              |                |
|------------------------------|----------------|
| **Novecošanas pamatojums**       | Ierobežots lietojums  |
| **Vai aizstāts ar citu līdzekli?** | Nē             |
| **Ietekmētie moduļi**             | Virsgrāmata |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Kreditora maksājuma formāts Pagamento Fornittori

Mantots Itālijas maksājuma formāts kredīta pārskaitījumiem.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Novecošanas pamatojums**       | Šis maksājuma formāts vairs netiek izmantots.                  |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Itālijai |
| **Ietekmētie moduļi**             | Parādi kreditoriem                                       |

### <a name="payment-export-formats-for-estonia"></a>Maksājuma eksportēšanas formāti Igaunijai

Formāti Telehansa un Teleservice tiek izmantoti bankas maksājumu eksportēšanai.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Novecošanas pamatojums**      | Šie maksājumu formāti vairs netiek izmantoti.                  |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Igaunijai |
| **Ietekmētie moduļi**             | Parādi kreditoriem                                         |

### <a name="payment-file-archive-for-norway"></a>Maksājumu failu arhīvs Norvēģijai

Kad tiek ģenerēti maksājumu faili, šo failu arhīvs automātiski arhivē visus failus, kas tiek izveidoti — pat failus, kas bija iepriekš rakstīti vai lasīti.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Aizstāts ar citu līdzekli                                        |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar arhivētajiem elektronisko pārskatu darbiem                            |
| **Ietekmētie moduļi**             | Parādi kreditoriem, Debitoru parādi, Organizācijas administrēšana |

### <a name="payment-import-formats-for-estonia"></a>Maksājuma importēšanas formāti Igaunijai

Formāti Telehansa un TeleTeenus tiek izmantoti bankas maksājumu importēšanai.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šie maksājumu formāti vairs netiek izmantoti.                                                    |
| **Vai aizstāts ar citu līdzekli?** | Nē. Turpmākajos laidienos šie formāti tiks aizstāti ar ISO 20022 izraksta importēšanas formātiem. |
| **Ietekmētie moduļi**             | Debitoru parādi                                                                        |

### <a name="performance-management-goal-workflow"></a>Veiktspējas pārvaldības mērķu darbplūsma

Veiktspējas pārvaldība ietver mērķu pārvaldīšanu un integrēšanu ar veiktspējas pārskatiem.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Veiktspējas pārvaldība tika pārveidota, un mērķa lapu skaits tika samazināts, lai vienkāršotu šo procesu.                 |
| **Vai aizstāts ar citu līdzekli?** | Nē. Mērķi ir redzami vadītājiem, izmantojot portālu Vadītāja pašapkalpošanās, un vadītājs tos var mainīt un apskatīt. |
| **Ietekmētie moduļi**             | Cilvēkkapitāla pārvaldība                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Maksājumu formāti Postgirot un Postgirot Utland Zviedrijai

Maksājumu formāti Postgirot un Postgirot Utland Zviedrijai.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| **Novecošanas pamatojums**       | Šie maksājumu formāti vairs netiek izmantoti.                 |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Zviedrijai |
| **Ietekmētie moduļi**             | Kreditoru parādi                                        |

### <a name="radio-frequency-identifier"></a>Radiofrekvences identifikators

Radiofrekvences identifikācija (RFID) ir datu vākšanas tehnoloģija, kas izmanto elektroniskos tagus identifikācijas datu glabāšanai un prasībām atbilstošu lasītāju šo identifikācijas datu uztveršanai.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Novecošanas pamatojums**       | Zems klientu lietojums un ierobežota līdzekļu kopa. |
| **Vai ir aizstāts ar citu līdzekli?** | Nē                                            |
| **Ietekmētie moduļi**             | Krājumu vadība                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Pārskats par valsts rēķinu numerāciju Latvijai

Latvijas likumdošana nodrošina īpašus noteikumus par pārdošanas rēķinu numerāciju. Šī funkcionalitāte jums ļauj pārdošanas rēķiniem piešķirt īpašus numurus, pamatojoties uz lietotāju vai lietotāju grupu. Pēc tam varat ģenerēt pārskatu vai XML failu. Varat arī izdrukāt pārskatu par izmantotajiem rēķinu numuriem.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Valsts rēķinu numerācija vairs nav jāuztur. Pārskats par izmantotajiem rēķinu numuriem vairs nav nepieciešams. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                                                                       |
| **Ietekmētie moduļi**             | Debitoru parādi                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Iestatīt uzņēmuma vadītāja un galvenā grāmatveža vārdus Lietuvai

Uzņēmuma vadītāja un galvenā grāmatveža vārdus var norādīta uzņēmuma informācijā un izmantot dažādās vietējo pārskatu izdrukās.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Novecošanas pamatojums**       | Aizstāts ar citu līdzekli                                     |
| **Vai aizstāts ar citu līdzekli?** | Jā, šiem pašiem nolūkiem var izmantot amatpersonu iestatīšanu.   |
| **Ietekmētie moduļi**             | Kreditori, Debitori, Kases un bankas vadība |

### <a name="telepay-payment-formats-for-norway"></a>Maksājumu formāti Telepay Norvēģijai

Maksājumu formāti Telepay ietver kreditoru maksājumu eksportēšanu (kredīta pārskaitījums) un debitoru maksājumu iekasēšanu (tiešais debets).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šie maksājumu formāti vairs netiek izmantoti.                                                        |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums un debitora maksājuma formātu AvtaleGiro Norvēģijai |
| **Ietekmētie moduļi**            | Parādi kreditoriem, Debitoru parādi                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Kreditoru maksājumu eksportēšanas formāti Somijai

Divi formāti maksājumu eksportēšanai ir pieejami Somijā. LM02 (FI) tiek izmantots iekšzemes maksājumiem un LUM2 (FI) tiek izmantots ārvalstu maksājumiem.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Novecošanas pamatojums**       | Šie maksājumu formāti vairs netiek izmantoti.                  |
| **Vai aizstāts ar citu līdzekli?** | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Somijai |
| **Ietekmētie moduļi**            | Parādi kreditoriem                                         |

### <a name="workflow-for-creating-goals"></a>Darbplūsma mērķu izveidošanai

Darbplūsma darbinieku mērķu izveidošanas pārvaldībai ir viena no vairākām darbplūsmām, kas bija pieejamas, lai palīdzētu koordinēt veiktspējas pārvaldības procesu.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Programmatūrā Microsoft Dynamics 365 for Finance and Operations ir pilnībā pārveidota veiktspējas pārvaldība.                                                                                                                                                                                                                                        |
| **Vai ir aizstāts ar citu līdzekli?** | Pārveidotais līdzeklis Veiktspējas pārvaldība sniedz lielāku kontroli pār mērķu saturu, mērījumiem, kas tiek izmantoti progresa izsekošanai, un pavaddokumentu piesaistīšanu. Mērķus var glabāt kā veidnes un pēc tam lietot atkārtoti. Šis līdzeklis jums var palīdzēt ātrāk iestatīt papildu mērķus saviem darbiniekiem. |
| **Ietekmētie moduļi**            | Cilvēkkapitāla pārvaldība                                                                                                                                                                                                                                                                                                               |

## <a name="features-that-have-been-deprecated-in-dynamics-ax-70-releases"></a>Novecojušie līdzekļi Dynamics AX 7.0 laidienos

### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Spēja atcelt kreditora rēķinā veiktās izmaiņas

|                              |                         |
|------------------------------|-------------------------|
| **Novecošanas pamatojums**       | Veiktspējas uzlabojums |
| **Vai aizstāts ar citu līdzekli?** | Nē                      |
| **Ietekmētie moduļi**            | Parādi kreditoriem        |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD un AxBC integrācijas

Programmu integrācijas struktūrā (Application Integration Framework — AIF) var veikt datu apmaiņu ar ārējām sistēmām, izmantojot biznesa loģiku, kas tiek izmantota kā pakalpojumi. Dynamics AX ietver pakalpojumus, kuru pamatā ir dokumenti un .NET Business Connector (AxBC). Dokuments tiek izveidots, izmantojot XML. XML ietver virsraksta informāciju, kas tiek pievienota, lai izveidotu *ziņojumu*, kuru var pārsūtīt uz programmu Dynamics AX vai no tās. Dokumentu piemēros ietilpst pārdošanas pasūtījumi un pirkšanas pasūtījumi. Taču gandrīz jebkuru elementu, piemēram, debitoru, var pārstāvēt ar dokumentu. Uz dokumentiem balstītie pakalpojumi lieto **Axd &lt;*Document*&gt;** klases.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | AIF un AxDs arhitektūru nevarēja mērogot uz mākoņa pakalpojumu. Radās veiktspējas problēmas saistībā ar lielapjoma importēšanu.                                                                               |
| **Vai aizstāts ar citu līdzekli?** | Pašreizējā Dynamics AX versijā šis līdzeklis ir aizstāts ar datu importēšanas/eksportēšanas struktūru, kura atbalsta periodisku lielapjoma importēšanu/eksportēšanu. Strādājot ar AxBC, ieteicams lietot faktiskās tabulas. |
| **Ietekmētie moduļi**             | AxDs, AxBCs un AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>MK bez MK versijām

Kad tika atspējota konfigurācijas atslēga **MK versijas**, materiālu komplektu (MK) versijas tika paslēptas visās formās, un starp izlaistajām precēm un MK sistēma lika izmantot attiecību 1:1. Pašreizējā Dynamics AX versijā konfigurācijas atslēgu **MK versijas** nevar atspējot.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**      | Konfigurācijas atslēgas izmantošana, lai kontrolētu MK versijas, netiek mērogota mākoņa vidē. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                                      |
| **Ietekmētie moduļi**            | Preču informācijas pārvaldība, Krājumu vadība                                    |

### <a name="brazilian-bordero"></a>Brazīlijas Bordero

Īpaša maksāšanas metode Brazīlijas uzņēmumiem

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Brazīlijas lokalizācijā ir pārtraukts atbalsts Brazīlijas maksāšanas metodei Bordero |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                                                    |
| **Ietekmētie moduļi**             | Parādi kreditoriem                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brazīlijas izraksts Sintegra

Federālā nodokļa izraksts ICMS nodokļiem

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šis izraksts vairs nav lietojams noteiktos Brazīlijas štatos.                                                     |
| **Vai aizstāts ar citu līdzekli?** | Nē. Lietotāji var izmantot vispārīgo elektronisko atskaišu veidošanas rīku, lai konfigurētu šo izrakstu, ja konkrētās situācijās tas ir nepieciešams. |
| **Ietekmētie moduļi**             | Finanšu grāmatas                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brazīlijas NF-e nejaušību režīms SCAN

(SCAN) nejaušību vide tiek izmantota, lai ģenerētu, eksportētu un importētu Nota Fiscal eletrônica (NF-e) statusu, kad nav pieejama vide Secretaria da Fazenda (SEFAZ).

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šī nejaušību metode vairs nav lietojama visos Brazīlijas štatos |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                          |
| **Ietekmētie moduļi**             | Debitoru parādi                                                         |

### <a name="business-analyzer"></a>Biznesa analizators

Šī mobilā programmas lietotājiem ļauj pārskatīt galvenos biznesa rādītājus.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šī funkcionalitāte ir aizstāta ar citu līdzekli.                                                                                                      |
| **Vai aizstāts ar citu līdzekli?** | Produktam Microsoft Power BI paredzētā satura pakotne Pārraudzīt finanšu veiktspēju ietvers galvenos finanšu rādītājus, kuri iepriekš bija pieejami biznesa analizatorā. |
| **Ietekmētie moduļi**             | Virsgrāmata                                                                                                                                                |

### <a name="business-statistics"></a>Vadības statistika

Biznesa statistikas uzziņu iestatījums, kas jums var palīdzēt analizēt organizācijas veiktspēju

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Mantojuma pieeja biznesa informācijai (BI), zems klientu lietojums un ierobežota līdzekļu kopa |
| **Vai aizstāts ar citu līdzekli?** | Ar jauniem BI risinājumiem pašreizējai Dynamics AX versijai                                      |
| **Ietekmētie moduļi**             | Sagāde un avoti, Kreditori, Pārdošana un mārketings, Debitori         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Mainīt dokumenta datuma funkciju rēķinu apstiprināšanas žurnālā

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Zems lietojums                                                               |
| **Vai aizstāts ar citu līdzekli?** | Jā. Grāmatotajā kreditora transakcijā var mainīt dokumenta datumu. |
| **Ietekmētie moduļi**             | Parādi kreditoriem                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03 maksājuma formāts Nīderlandei

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šis formāts Nīderlandē vairs nav lietojams, jo tas ir aizstāts ar SEPA funkcionalitāti. |
| **Vai aizstāts ar citu līdzekli?** | SEPA maksājumu eksportēšana                                                                                       |
| **Ietekmētie moduļi**             | Visi                                                                                                        |

### <a name="compliance-center"></a>Atbilstības centrs

Atbilstības centrs bija uzņēmuma portāla vietne dokumentācijas prasību pārvaldīšanai, lai nodrošinātu atbilstību ar Sarbanes-Oxley likumu saistītajām iniciatīvām.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Debitoru lietojuma trūkums. Microsoft SharePoint ietver tādas pašas iespējas, kādas bija pieejamas atbilstības centrā. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                                                                     |
| **Ietekmētie moduļi**             | Atbilstība un iekšējā kontrole                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Microsoft Dynamics paredzētā Connector sistēma

Šis rīks tika izmantots, lai atslēgas datus no Microsoft Dynamics CRM integrētu Microsoft Dynamics ERP programmās.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Novecošanas pamatojums**       | Šī funkcionalitāte ir aizstāta ar citu līdzekli. |
| **Vai aizstāts ar citu līdzekli?** | Ar Dynamics integrētāju                                      |
| **Ietekmētie moduļi**             | Microsoft Dynamics paredzētā Connector sistēma                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Konteinera vienība un rīcībā esošie vairākdimensiju krājumi

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Funkcionalitātes dublēšanās                                                                                                                                         |
| **Vai aizstāts ar citu līdzekli?** | Jā. Kopš versijas AX 2012 šī funkcionalitāte ir aizstāta ar konsolidēto partijas pasūtījumu līdzekļu kopu. Šī līdzekļu kopa ietver konsolidēto rīcībā esošo krājumu skatu. |
| **Ietekmētie moduļi**             | Preču informācijas pārvaldība, Ražošanas kontrole, Krājumu vadība, Pārdošana un mārketings                                                                   |

### <a name="cue-group-metadata"></a>Norādījumu grupas metadati

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Norādījumu grupas tika izmantotas, lai papildinformācijas apgabalā parādītu vienu vai vairākus norādījumus. Pastāvēja uzņemšanas ierobežojumi, un bija arī veiktspējas problēmas, jo ieraksta izmaiņas primārajā formā izraisīja vienu vaicājumu katram norādījumu grupas norādījumam. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                                                                                                                                                                            |
| **Ietekmētie moduļi**             | Visi                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Norādījuma metadati

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Norādījuma metadati bija ierobežoti ar informāciju par skaitu vai summu.                                                                                                                                                                                   |
| **Vai aizstāts ar citu līdzekli?** | Tika ieviesti elementa metadati, lai modelēšanai nodrošinātu lielāku elastību. Piemēram, varat modelēt pašreizējo skaitu, navigāciju un galvenos veiktspējas rādītājus (KPI). Skaita elementa metadati ir tiešs norādījuma metadatu aizstājējs. |
| **Ietekmētie moduļi**             | Visi                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Dānijas čeka formāts

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Ir pārtraukta atbalsta sniegšana Dānijas čeka formāta izkārtojumam, un šī atskaite ir noņemta no DK lokalizācijas. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                                                                      |
| **Ietekmētie moduļi**             | Visi                                                                                                                     |

### <a name="data-partitions"></a>Datu nodalījumi

Datu nodalījumi nodrošina loģisku datu nošķiršanu Microsoft Dynamics AX datu bāzē.

|   |   |
|---|---|
| **Novecošanas pamatojums**       | Datu nodalījumi tika ieviesti versijā Microsoft Dynamics AX 2012 R2, lai varētu izmantot datu izolēšanu. Tipiskā scenārijā uzņēmumam ir filiāles, un datiem no vienas filiāles nevajadzētu būt redzamiem citai filiālei, lai gan abas filiāles pārvalda tā pati IT nodaļa. Taču bija nepieciešami papildu skripti un pārvaldība visā programmā, lai izveidotu jaunus nodalījumus un aizpildītu tos ar datiem, kā arī lai veiktu nodalījuma datu dublējumus. Mākonī, kur mums ir piekļuve platformas kā pakalpojuma (PaaS) datu bāzu pakalpojumiem (Microsoft Azure SQL datu bāzei), daudz efektīvāk ir datu bāzi lietot kā izolācijas konteineru, nevis veikt izolēšanu programmā. Neatkarīgi no tā, vai datu nodalījumu izmantošana ir nepieciešama filiālēm, vairākiem nomniekiem vai tikai mērogam, mēs uzskatām, ka ar scenārijiem daudz labāk var strādāt, izmantojot vairākas Finance and Operations instances. |
| **Vai aizstāts ar citu līdzekli?** | Debitoriem, kas izmanto datu nodalījumus, ir jāizmanto vairākas Finance and Operations instances, ja datu bāzes līmeņu atdalīšana ir būtisks jautājums.    |
| **Ietekmētie moduļi**             | Visi  |

### <a name="database-and-file-share-storage-for-attachments"></a>Datu bāzes un failu koplietošanas krātuve pielikumiem
Microsoft Dynamics AX 2012 ļāva izmantot krātuvi pielikumiem datu bāzē un failu koplietojumos. Abas šīs opcijas vairs netiek atbalstītas.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Novecošanas pamatojums**       | Failu koplietošanas krātuve vairs netiek atbalstīta, jo mākoņvides nevar sazināties ar lokālajiem failu koplietojumiem. Datu bāzes krātuve ir novecojusi, un tās vietā tiek izmantota Azure Blob krātuve. Azure Blob krātuve ir ekvivalents krātuvei datu bāzē, jo dokumentiem var piekļūt, tikai izmantojot Dynamics 365 for Finance and Operations klienta formas. Tas nodrošina papildu priekšrocību — šī krātuve neietekmē negatīvi datu bāzes darbību. Blob krātuve ir noklusējuma krātuves mehānisms dokumentu pārvaldībai, un tā darbojas uzreiz. |
| **Vai ir aizstāts ar citu līdzekli?** | Datu bāzes krātuve ir novecojusi, un tās vietā tiek izmantota Azure Blob krātuve.       |
| **Ietekmētie moduļi**             | Visi                   |

### <a name="delimitation"></a>Norobežošana

|                              |                                        |
|------------------------------|----------------------------------------|
| **Novecošanas pamatojums**       | Šai funkcionalitātei netika atrasts pielietojums. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                     |
| **Ietekmētie moduļi**             | Laiks un apmeklētība                    |

### <a name="desktop-client"></a>Darbvirsmas klients

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Dynamics AX klienta lietošana ir pārveidota tā, lai uzlabotu izmantojamību dažādās platformās un ierīcēs.                      |
| **Vai aizstāts ar citu līdzekli?** | Jaunais tīmekļa klients ir balstīts uz darbvirsmas formas metadatiem un programmēšanas modeli, kas ir modificēti tā, lai nodrošinātu bagātīgu tīmekļa platformu. |
| **Ietekmētie moduļi**             | Visi                                                                                                                                    |

### <a name="direct-database-connection"></a>Tiešs datu bāzes savienojums

Programmā Dynamics AX 2012 R3 Retail Modern POS var izveidot tiešu savienojumu ar kanāla DB līdzīgi kā Uzņēmuma POS. Tas bija papildinājums Retail Modern POS standarta sakaru metodei, kas nodrošināja saziņu ar Retail Server starpniecību.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Tiešajai datu bāzes savienojamībai bija nepieciešami zemākas drošības protokoli, un tā galvenokārt tika izmantota, lai sasniegtu augstāko veiktspējas līmeni. Programmatūras Dynamics 365 for Finance and Operations veiktspējas un drošības uzlabojumu dēļ šī funkcionalitāte tagad rada vairāk problēmu, nekā tā atrisina. |
| **Vai ir aizstāts ar citu līdzekli?** | Nr.p.k. Tagad tiek atbalstīti tikai standarta Retail Server sakari.    |
| **Ietekmētie moduļi**             | Kanāla DB/Retail Modern POS                                    |

### <a name="dutch-swift-mt940"></a>Holandes SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Tagad tiek izmantota vispārīgā funkcionalitāte, nevis lokalizētā funkcionalitāte.                                                                                                                                                                 |
| **Vai aizstāts ar citu līdzekli?** | Jā, šī funkcionalitāte ir aizstāta ar detalizētas bankas darbību saskaņošanas funkcionalitāti. |
| **Ietekmētie moduļi**             | Visi                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL Vācijai)

Šī funkcionalitāte nodrošināja paplašināmās komerciālo atskaišu valodas (eXtensible Business Reporting Language — XBRL) izvades, kas ir paredzēta speciāli Vācijas eBilanz taksonomijai.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Debitoru lietojuma trūkums                                                                                                                                                 |
| **Vai aizstāts ar citu līdzekli?** | Šis līdzeklis nav aizstāts ar citu līdzekli, bet Vācijas tirgū ir pieejamas vairākas specializētas XBRL pakotnes, kas nodrošina bagātīgu XBRL funkcionalitāti. |
| **Ietekmētie moduļi**             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Uzņēmuma portāla klients

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Ir nodrošināta viena klienta platforma.                                                                                            |
| **Vai aizstāts ar citu līdzekli?** | Jaunais tīmekļa klients ir balstīts uz darbvirsmas formas metadatiem un programmēšanas modeli, kas ir modificēti tā, lai nodrošinātu bagātīgu tīmekļa platformu. |
| **Ietekmētie moduļi**             | Visi                                                                                                                                    |

### <a name="environmental-sustainability"></a>Vides ilgtspējība

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| **Novecošanas pamatojums**       | Zems klientu lietojums un ierobežota līdzekļu kopa       |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                 |
| **Ietekmētie moduļi**             | Atbilstības un iekšējās vadīklas, Kreditori |

### <a name="form-activex-and-managed-host-controls"></a>Forma ActiveX un pārvaldītās resursdatora vadīklas

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | ActiveX un pārvaldīto resursdatora vadīklu pamatā ir novecojušais darbvirsmas klients.                                                                                                             |
| **Vai aizstāts ar citu līdzekli?** | Paplašināmā kontroles struktūra atbalsta tādu jaunu vadīklu veidošanu, kuru pamatā ir HTML, CSS un JavaScript, un tā ir pirmās klases kontrole Microsoft Visual Studio rīku vidē. |
| **Ietekmētie moduļi**             | Visi                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Ģenerēt pārbaudes, izmantojot paketi

Pārbaudes ģenerēšanu nevar veikt, izmantojot paketi, bet lietotājs to joprojām var izdarīt.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Nav formas, ar kuru saglabāt un parādīt iegūto pārbaudes failu, kad tas tiek ģenerēts, izmantojot pakešuzdevumu. |
| **Vai aizstāts ar citu līdzekli?** | Pārbaudes joprojām var ģenerēt, un lietotājs kontrolē vietu, kur šis fails tiek saglabāts.   |
| **Ietekmētie moduļi**             | Kreditori, Debitori, Kases un bankas vadība                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Vācu DTAUS maksājuma eksportēšana un konta izraksta importēšana (kopsummas un transakcijas)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šis formāts Vācijā vairs nav lietojams, jo tas ir aizstāts ar vienotās eiro maksājumu zonas (Single Euro Payments Area — SEPA) funkcionalitāti.                                                                                                                                                                 |
| **Vai aizstāts ar citu līdzekli?** | Jā, šī funkcionalitāte ir aizstāta ar SEPA maksājumu eksportēšanas un detalizētās bankas darbību saskaņošanas funkcionalitāti kontu pārskatu importēšanai. |
| **Ietekmētie moduļi**             | Visi                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Vācijas DTAZV maksājumu formāts

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šis formāts Vācijā vairs nav lietojams, jo tas ir aizstāts ar SEPA funkcionalitāti. |
| **Vai aizstāts ar citu līdzekli?** | SEPA maksājumu eksportēšana                                                                               |
| **Ietekmētie moduļi**             | Visi                                                                                                |

### <a name="german-mt940-import"></a>Vācu MT940 importēšana

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Tagad tiek izmantota vispārīgā funkcionalitāte, nevis lokalizētā funkcionalitāte.                                                                                                                                                                 |
| **Vai aizstāts ar citu līdzekli?** | Jā, šī funkcionalitāte ir aizstāta ar detalizētas bankas darbību saskaņošanas funkcionalitāti. |
| **Ietekmētie moduļi**             | Visi                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Vācijas XML ES pārdošanas saraksts

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Vairs netiek atbalstīts XML formāts Vācijas ES pārdošanas saraksta atskaitēm. Lai ES pārdošanas saraksta atskaites iesniegtu Vācijas nodokļu birojā, var izmantot tikai ELMA5 teksta faila formātu. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                                                                                                                                 |
| **Ietekmētie moduļi**             | Nodokļi                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>GL SSRS atskaites

Ir noņemtas atskaites, kas ietvēra šādus izvēlnes vienumus: **Kopsavilkuma apgrozījuma bilance**, **Detalizēta apgrozījuma bilance**, **Kontu plāns**, **Auditācijas pieraksti**, **Bilances** un **Bilances saraksts**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Finanšu Microsoft SQL Server pārskatu izveides pakalpojumu (SSRS) atskaites ir aizstātas ar pārvaldības atskaišu sastādītāja iespējām un noklusējuma atskaitēm. |
| **Vai aizstāts ar citu līdzekli?** | Ar pārvaldības atskaišu sastādītāju (pašreizējā Dynamics AX versijā apzīmēts kā **Finanšu pārskati**)                                                  |
| **Ietekmētie moduļi**            | Virsgrāmata                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>InfoPart un FormPart metadati

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | InfoPart un FormPart metadati ļāva izveidot papildinformācijas lodziņus diviem dažādiem klientiem.                                                                                                                                    |
| **Vai aizstāts ar citu līdzekli?** | InfoPart metadati, kas bija vienkāršotā formas definīcija, ar jaunināšanas rīkiem ir pārveidoti par formu. FormPart metadati, kas veidoja atsauci uz formu, ir aizstāti ar tiešāku atsauci, ko veido jaunināšanas rīki. |
| **Ietekmētie moduļi**             | Visi                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Galvenā konta saraksta lapa

Saraksts ar kontiem juridiskajai personai un saistītā bilances informācija

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Bilances informācija ir pieejama saraksta lapā **Apgrozījuma bilance** pēc konta un dimensijas.                                                                                      |
| **Vai aizstāts ar citu līdzekli?** | Sadaļā **Galvenie konti** ir ietverts tāds pats kontu saraksts, kas atrodas saraksta lapā **Galvenais konts**. Režģa skats sadaļā **Galvenie konti** arī rāda vēl mazāku, režģa tipa skatu. |
| **Ietekmētie moduļi**             | Virsgrāmata                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaizijas un Singapūras bankas naudas plūsmas atskaite

Šis līdzeklis lietotājam ļauj drukāt naudas plūsmas atskaiti, kurā ir redzamas transakcijas un detalizēta informācija par skaidras naudas ienākošajām un izejošajām plūsmām attiecībā uz noteiktu laika diapazonu atlasītajiem bankas kontiem.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šo pašu informāciju var saņemt pieprasošās bankas transakcijas. |
| **Vai aizstāts ar citu līdzekli?** | Ar pieprasošās bankas transakciju                                            |
| **Ietekmētie moduļi**             | Kases un bankas vadība                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Meksikas CFD elektroniskais rēķins

Šis līdzeklis ļāva ģenerēt Meksikas elektroniskos rēķinus, izmantojot metodi Comprobante Fiscal Digital (CFD), kurā uzņēmums paraksta rēķinu, no valdības pieprasot saistīto autorizāciju. Šis līdzeklis nodrošina arī ikmēneša atskaiti, kas ietver visus šajā periodā izsniegtos elektroniskos rēķinus.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šī metode vairs nav piemērojama. Nodokļu iestādes atzina par novecojušu elektronisko rēķinu ģenerēšanu, izmantojot CFD metodi, un aizstāja ar metodi Comprobante Fiscal Digital a través de Internet (CFDI), kur parakstīšana tiek deleģēta trešās puses nodrošinātājam (PAC). Ikmēneša atskaite ir noņemta, un vaicājuma opcija lietotājam ļauj pieprasīt uzziņas par vēsturiskajām transakcijām. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Ietekmētie moduļi**             | Debitori, Projekts                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Meksikas realizētais un nerealizētais PVN

Microsoft Dynamics AX 2012 nerealizēto pievienotās vērtības nodokli (PVN) pārvaldīja, izmantojot Meksikai raksturīgo funkcionalitāti, kas paredzēta “nerealizētajiem nodokļiem”.

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Funkcionalitātes dublēšanās                                                                                             |
| **Vai aizstāts ar citu līdzekli?** | Jā, šī funkcionalitāte ir aizstāta ar standarta nosacījuma pārdošanas nodokļa funkcionalitāti, ko nodrošina pamats. |
| **Ietekmētie moduļi**             | Nodokļi                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook integrācija

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šī funkcionalitāte ir aizstāta ar Microsoft Exchange Server integrāciju. |
| **Vai aizstāts ar citu līdzekli?** | Jā                                                                            |
| **Ietekmētie moduļi**             | Pārdošana un mārketings                                                            |

### <a name="payroll-information-in-human-resources"></a>Algas informācija personāla vadībā

Personāla vadības algas informācija

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šī funkcionalitāte ir aizstāta ar pamata lapām Alga un Personāla vadība.                                                                                                                                                                                                                                              |
| **Vai aizstāts ar citu līdzekli?** | Lapas **Atvieglojumi**, **Ienākumi** un citas saistītās lapas, kas iepriekš atradās modulī ASV alga, ir pārkonfigurētas un tagad veido daļu no moduļa Personāla vadība pamata konfigurācijas, lai palīdzētu atbalstīt ārējo algu apstrādi. Šai funkcionalitātei piekļūst, izmantojot konfigurācijas atslēgu **Personāla vadība 1** &gt; **Alga**. |
| **Ietekmētie moduļi**             | Personāla vadība, Alga                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Krājumu un noliktavas vadības žurnālu privāta bloķēšana

Krājumu un noliktavas žurnāli vairs neatbalsta iespēju atzīmēt žurnālu kā privātu atlasītam lietotājam. Tiek atbalstīta tikai žurnālu kā privātu bloķēšana lietotāju grupām un bloķēšanas rediģēšanas laikā.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Novecošanas pamatojums**       | Šai funkcionalitātei netika atrasts pielietojums. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                     |
| **Ietekmētie moduļi**             | Krājumu vadība                   |

### <a name="product-builder"></a>Preču konfigurators

Preču konfigurators tika izmantots, lai dinamiski konfigurētu krājumus no pārdošanas pasūtījuma, pirkšanas pasūtījuma, ražošanas pasūtījuma, pārdošanas piedāvājuma, projektu piedāvājuma vai krājuma vajadzības. Pamatojoties uz preces modeli, kam bija modelēšanas mainīgie, lietotājs varēja atlasīt klienta prasībām atbilstošas vērtības un iegūt unikālu preces variantu, kuram bija MK un maršruts.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Preču konfigurators X++ kodu atklāja lietotājiem, un Dynamics AX pašreizējā versijā tas netiek atbalstīts. Tas ir noņemts, lai izvairītos no uzturēšanas darbu dublēšanās attiecībā uz ietilpīgām kodu bāzēm, kas pārklājas. |
| **Vai aizstāts ar citu līdzekli?** | Preces konfigurācija                                                                                                                                                                                   |
| **Ietekmētie moduļi**             | Preču informācijas pārvaldība, Pārdošana un mārketings                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Pārdēvējiet preces dimensiju

Šis līdzeklis jums ļauj nosaukumu vienai no trim standarta preces dimensijām (lielumam, krāsai vai stilam) mainīt pret nosaukumu, kas labāk atbilst jūsu biznesa vajadzībām. Pārdēvēšana iekļāva visas etiķetes, kurās tika izmantots šis preces dimensijas nosaukums.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Dynamics AX pašreizējā versija neatbalsta etiķešu izmaiņu veikšanu izpildlaikā. |
| **Vai ir aizstāts ar citu līdzekli?** | Nē                                                                            |
| **Ietekmētie moduļi**             | Preču informācijas pārvaldība                                                |

### <a name="retail-server-connectivity-using-http"></a>Retail Server savienojamība, izmantojot HTTP

Programmā Dynamics AX 2012 R3 Retail Server varēja darboties, izmantojot HTTP sakarus (nedroši). To varēja veikt papildus standarta sakariem, izmantojot HTTPS.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Jauno drošības prasību dēļ tagad tiek atbalstīti tikai droši sakari, izmantojot TLS 1.2 (vai jaunāka versija, ja pieejama). Pašapkalpošanās instalētājs automātiski konfigurēs datoru šādam saziņas veidam. |
| **Vai ir aizstāts ar citu līdzekli?** | Nr.p.k. Tagad tiek atbalstīti tikai standarta HTTPS sakari.                                                                           |
| **Ietekmētie moduļi**             | Mazumtirdzniecības serveris                                                |

### <a name="role-center-pages"></a>Informācijas centru lapas

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Lapas Lomu centrs tika veidotas uz novecojušās uzņēmuma portāla platformas, kura pašreizējā Dynamics AX versijā ir aizstāta ar jauno tīmekļa klienta platformu. |
| **Vai aizstāts ar citu līdzekli?** | Jaunais darbvietas formas modelis lietotājiem sniedz uz procesu centrētu dizainu, kas nodrošina ērtu piekļuvi bieži lietotajiem uzdevumiem šajā procesā.                       |
| **Ietekmētie moduļi**             | Visi                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>PVN jurisdikcijas

|                              |                                              |
|------------------------------|----------------------------------------------|
| **Novecošanas pamatojums**       | Zems klientu lietojums un ierobežota līdzekļu kopa |
| **Vai aizstāts ar citu līdzekli?** | Nē                                           |
| **Ietekmētie moduļi**             | ASV pārdošanas nodoklis                                 |

### <a name="shipping-carrier-interface"></a>Sūtījumu pārvadātāja interfeiss

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Funkcionalitātes dublēšanās                                                                                                                         |
| **Vai aizstāts ar citu līdzekli?** | Jā, šis līdzeklis ir daļēji aizstāts ar transportēšanas pārvaldību, bet vēl nav aizstāts ar pamata noliktavas vadību (WMS I). |
| **Ietekmētie moduļi**             | Pārdošana un mārketings, Krājumu vadība                                                                                                       |

### <a name="sites-services"></a>Site Services

Pakalpojumi Sites Services jums ļauj veidot vietnes, kas jūsu biznesa procesus paplašina uz internetu, neizmantojot IT atbalstu.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Ar Dynamics AX izmantotajai Microsoft Azure infrastruktūrai ir jaunas iespējas, ko var izmantot šī līdzekļa vietā (piemēram, Azure vietnes). |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                                                                                                       |
| **Ietekmētie moduļi**             | HR personāla atlase, Pieteikumu pārvaldība, Piedāvājumu pieprasījums, Kreditora reģistrēšana                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS pieprasījuma prognozēšanas stratēģija

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Līdzekļa dizainu nevar atbalstīt jaunajā mākoņa arhitektūrā. |
| **Vai ir aizstāts ar citu līdzekli?** | Azure algoritmiskās mācīšanās pieprasījuma prognozēšanas stratēģija                           |
| **Ietekmētie moduļi**             | Plānošana                                                                     |

### <a name="travel-requisitions"></a>Komandējuma pieprasījumi

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Novecošanas pamatojums**       | Zems lietojums, un vairums funkcionalitātes pastāvēja uzņēmuma portālā. |
| **Vai aizstāts ar citu līdzekli?** | Nē                                                              |
| **Ietekmētie moduļi**             | Izmaksu pārvaldība                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Kreditora rēķinu kopa bez detalizētās informācijas par grāmatošanu

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Zems lietojums. Šī funkcionalitāte ir aizstāta ar rēķinu žurnālu, kuram ir darbplūsmas funkcionalitāte. |
| **Vai aizstāts ar citu līdzekli?** | Ar rēķinu žurnāla darbplūsmas iespējām.                                                           |
| **Ietekmētie moduļi**             | Parādi kreditoriem                                                                                        |

### <a name="virtual-company-accounts"></a>Virtuālie datu faili

Virtuālo datu failu līdzeklis vairs netiek atbalstīts programmā Dynamics AX. Virtuālo datu failu līdzeklis lietotājiem ļāva iestatīt tabulas, ko varēja kopīgot ar uzņēmumu kopu. Šī līdzekļa aprakstu varat skatīt šeit: [Datu faili un virtuālie datu faili](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Šis līdzeklis darbojas, grupējot tabulas kolekcijās, kuras tiek piešķirtas virtuāliem datu failiem, kas ir esošo “reālo” uzņēmumu grupas. Vaicājumi tiek veidoti tā, lai visi uzņēmumi virtuālajā datu failā varētu piekļūt saistīto tabulu kolekcijās iekļautajiem datiem.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><b>Novecošanas pamatojums</b></td>
<td><ul>
<li>Pirms datu šķirošanas tabulās ir jāiestata virtuālie datu faili. Virtuālo datu failu modernizēšana esošajā implementācijā ir ļoti sarežģīta.</li>
<li>Tā kā pašreizējā Dynamics AX versijā ir bijis tik daudz datu normēšanas, ir kļuvis sarežģīti zināt, ko nepieciešams pievienot tabulu kolekcijām. Piemēram, ir grūti zināt, kuras tabulas kopīgot. Ir jāpievieno arī visas tabulas, uz kurām ir atsauces virtuālajā datu failā ietvertajās tabulās. Tabulu normalizēšanas dēļ pat vienkāršiem pamatdatiem, kas ir izklāti vairākās tabulās, ir jābūt daļai no virtuālā datu faila. Jebkāda šeit pieļauta kļūda izraisīs funkcionālas problēmas.</li>
<li>Kad tabula ir daļa no virtuāla datu faila, tā zaudē informāciju par datu izcelsmi, un tiek reģistrēts tikai virtuālais datu fails.</li>
</ul></td>
</tr>
<tr class="even">
<td><b>Vai aizstāts ar citu līdzekli?</b></td>
<td>Lai tabulas padarītu pieejamas no visiem uzņēmumiem, var izmantot globālās tabulas. Pašlaik aizstājēja nav.</td>
</tr>
<tr class="odd">
<td><b>Ietekmētie moduļi</b></td>
<td>Nav attiecināms</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>Noliktavas vadība II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Risinājums Noliktavas vadība II (WMS II), kas bija pieejams modulī **Krājumu vadība**, dublē funkcionalitāti, kas ir pieejama modulī **Noliktavas vadība**, kurš tika izlaists versijā Microsoft Dynamics AX 2012 R3.                                                                         |
| **Vai aizstāts ar citu līdzekli?** | Modulis **Noliktavas vadība**, kas tika izlaists versijā AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 un Microsoft Dynamics AX 2012 R3 CU9 aizstāj līdzekļus modulī Noliktavas vadība II. Jaunajam modulim ir uzlabotāki līdzekļi un elastīgāki noliktavas vadības procesi nekā modulim Noliktavas vadība II. |
| **Ietekmētie moduļi**             | Krājumu vadība, Pārdošana un mārketings, Sagāde un avoti                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Darbinieku atgādinājumi personāla vadībā

Personāla vadības algas informācija

|                              |                 |
|------------------------------|-----------------|
| **Novecošanas pamatojums**       | Zems lietojums       |
| **Vai aizstāts ar citu līdzekli?** | Nē              |
| **Ietekmētie moduļi**             | Personāla vadība |

### <a name="workplanner"></a>Darbu plānotājs

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Zems lietojums                                                                                                                                                            |
| **Vai aizstāts ar citu līdzekli?** | Nē, bet lapa **Profila saistība**, kura tiek atvērta no lapas **Profilu grupas**, atbalsta tādu pašu biznesa scenāriju kā novecojusī lapa **Darbu plānotājs**. |
| **Ietekmētie moduļi**             | Laiks un apmeklētība                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++ finanšu pārskati

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| **Novecošanas pamatojums**       | Šī funkcionalitāte ir aizstāta ar citu līdzekli.                                    |
| **Vai aizstāts ar citu līdzekli?** | Ar pārvaldības atskaišu sastādītāju (pašreizējā Dynamics AX versijā apzīmēts kā **Finanšu pārskati**) |
| **Ietekmētie moduļi**             | Virsgrāmata                                                                              |


