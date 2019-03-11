---
title: SEPA tiešā debeta pārskats
description: Vienoto eiro maksājumu zonu (SEPA) ir izveidojusi Eiropas Komisija un tā nosaka, ka visi elektroniskie maksājumi tiek uzskatīti par iekšzemes maksājumiem neatkarīgi no privātpersonas, uzņēmuma vai organizācijas un bankas atrašanās valsts/reģiona. Starp nacionālajiem un pārrobežu maksājumiem nav nekādas atšķirības. SEPA ietver 28 Eiropas Savienības (ES) dalībvalstis, kā arī Islandi, Lihtenšteinu, Norvēģiju, Šveici, Monako un Sanmarīno. SEPA palīdz veidot vienoto maksājumu transakciju tirgus Eiropas Ekonomikas zonā (EEZ). Visbeidzot, paredzams, ka SEPA samazinās maksājumu formātu skaitu, ar kuru ir jāstrādā bankām, uzņēmumiem un privātpersonām.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23c418c6412e4bd300616eed4577e2b1d3f3d181
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "359202"
---
# <a name="sepa-direct-debit-overview"></a>SEPA tiešā debeta pārskats

[!include [banner](../includes/banner.md)]

Vienoto eiro maksājumu zonu (SEPA) ir izveidojusi Eiropas Komisija un tā nosaka, ka visi elektroniskie maksājumi tiek uzskatīti par iekšzemes maksājumiem neatkarīgi no privātpersonas, uzņēmuma vai organizācijas un bankas atrašanās valsts/reģiona. Starp nacionālajiem un pārrobežu maksājumiem nav nekādas atšķirības. SEPA ietver 28 Eiropas Savienības (ES) dalībvalstis, kā arī Islandi, Lihtenšteinu, Norvēģiju, Šveici, Monako un Sanmarīno. SEPA palīdz veidot vienoto maksājumu transakciju tirgus Eiropas Ekonomikas zonā (EEZ). Visbeidzot, paredzams, ka SEPA samazinās maksājumu formātu skaitu, ar kuru ir jāstrādā bankām, uzņēmumiem un privātpersonām.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>Kāds ir SEPA tiešā debeta mērķis?
---------------------------------------

SEPA tiešais debets ļauj kreditoram iekasēt līdzekļus no debitora bankas konta ar nosacījumu, ka šim kreditoram attiecīgais debitors ir piešķīris parakstītu mandātu. Debitors paraksta mandātu, kas kreditoru pilnvaro maksājuma saņemšanai un klienta bankai sniedz norādījumus par iekasējamās summas izmaksāšanu. 

SEPA tiešā debeta shēma pirmoreiz izveido maksāšanas līdzekli, ko var izmantot gan valsts, gan pārrobežu eiro tiešā debeta transakcijās 32 SEPA valstīs/reģionos. 

Ir pieejamas divas shēmas: SEPA galvenā tiešā debeta shēma un SEPA uzņēmums uzņēmumam (B2B) tiešā debeta shēma. Abām shēmām ir vienāds failu formāts.

## <a name="what-is-the-core-direct-debit-scheme"></a>Kas ir galvenā tiešā debeta shēma?
SEPA galvenā tiešā debeta shēma ir pamatshēma. Tai ir tālāk minētie atribūti.
-   Naudas līdzekļu pārskaitījumi notiek eiro (pat tad, ja bankas kontos var būt līdzekļi citās valūtās).
-   Debitoram un kreditoram ir jābūt kontam kredīta iestādē, kas atrodas SEPA.
-   Debitoram ir jāpiešķir kreditoram parakstītais mandāts.
-   Mandāti beidzas 36 mēnešus pēc pēdējās uzsāktas iekasēšanas.
-   Kreditoram ir jāglabā mandāti, kamēr tie ir derīgi un vismaz 14 mēnešus pēc pēdējās iekasēšanas.
-   Šo shēmu var izmantot vienai (vienreizējai) vai periodiskai tiešā debeta iekasēšanai.
-   Debitoriem ir “neapšaubāmas” tiesības saņemt atmaksu astoņu nedēļu laikā pēc to kontu debitēšanas.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Kas ir SEPA uzņēmums uzņēmumam (B2B) tiešā debeta shēma?
SEPA B2B tiešā debeta shēma ir piemērojama transakcijām starp uzņēmumiem un pamatojas uz SEPA galveno tiešā debeta shēmu. Galvenās atšķirības ir šādas:
-   SEPA B2B tiešā debeta shēma nav pieļaujama, ja debitors ir privātpersona (patērētājs).
-   Debitoram nav tiesību uz autorizētas transakcijas atmaksu.
-   Debitora bankām jāpārliecinās, ka iekasēšana ir autorizēta, salīdzinot iekasēšanu ar informāciju par mandātu. Debitoru bankām un debitoriem ir jāvienojas par katra tiešā debeta pārbaudi.
-   Šai shēmai ir īsāks tiešo debetu parādīšanas laiks un īsāks atgriešanas periods.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Vai COR1 shēmu var izmantot tiešā debeta mandātiem?
Jā. COR1 shēmu varat izmantot SEPA tiešā debeta mandātiem Austrijā, Beļģijā, Vācijā, Francijā, Itālijā, Spānijā un Nīderlandē. Šī shēma nodrošina kreditoram īsāku pirmspaziņojuma periodu tiešā debeta iekasēšanai.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Kas ir starptautiskie bankas kontu numuri (IBAN) un banku identifikācijas kodi (BIC)?
Starptautiskais bankas konta numurs (IBAN) un bankas identifikācijas kods (BIC) tiek izmantots, lai identificētu jebkuru kontu 32 SEPA valstīs/reģionos. Ievadiet BIC laukā SWIFT kods un IBAN laukā IBAN. Abi lauki atrodas kopsavilkuma cilnē Papildu identifikācija, cilnē Bankas konts, lapā Banku konti. Tas attiecas uz kreditora bankas kontu un debitora bankas kontu.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Kur jāievada kreditora identifikatori (tiešā debeta ID)?
SEPA katru kreditoru identificē pēc unikāla kreditora identifikatora. Šis identifikators ļauj debitoram un debitora bankai filtrēt katru tiešo debetu un pēc tam apstrādāt vai noraidīt tiešo debetu atbilstoši debitora norādījumiem. Kreditoriem jāpieprasa šis identifikators caur savu banku. Šo identifikatoru attiecīgās juridiskās personas bankas kontam ievadiet laukā Tiešā debeta ID.

## <a name="what-are-mandates"></a>Kas ir mandāti?
Debitors paraksta mandātu, kas kreditoru pilnvaro maksājuma saņemšanai un klienta bankai sniedz norādījumus par iekasējamās summas izmaksāšanu. Debitors var izsniegt mandātu papīra formā vai elektroniski. Pēc noklusējuma mandāta derīguma termiņš izbeidzas 36 mēnešus pēc tiešā debeta pēdējās uzsākšanas.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Kur norādīt SEPA tiešā debeta faila formātu (ISO 20022)?
SEPA datu formāti ir balstīti uz ISO 20022 ziņojumu standartiem. Jums ir jāatzīmē izvēles rūtiņa Vispārīga elektronisko atskaišu veidošana un kā eksporta formāta konfigurācija ir jāatlasa SEPA tiešā debeta formāts, kad maksājumam konfigurējat debitoru metodes. Šo maksājuma metodi jūs izmantojat, kad debitoru maksājumu žurnālā ģenerējat maksājuma failu.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>Kādos faila formātos var ģenerēt SEPA tiešā debeta maksājumu failus?
SEPA tiešā debeta elektronisko maksājumu failus varat ģenerēt šādos formātos:
-   SEPA tiešā debeta maksājumu faili PAIN.008.001.02 XML failu formātā Beļģijai, Vācijai, Spānijai, Francijai, Itālijai un Nīderlandei.
-   SEPA tiešā debeta maksājumu faili PAIN.008.001.02 XML failu formātā Austrijai un PAIN.008.003.02 XML failu formātā Vācijai.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Kā veikt atmaksu un atgriešanu SEPA tiešā debeta transakcijām?
Abās SEPA tiešā debeta shēmās debitoriem ir noteiktas tiesības uz atmaksu. Debitoram ir atļauts, nenorādot iemeslu, atsaukt jebkuras autorizētās transakcijas astoņu nedēļu laikā pēc izpildes termiņa. Neautorizētu transakciju gadījumā šis periods tiek pagarināts līdz 13 mēnešiem pēc izpildes termiņa. Jebkuru veikto maksājumu anulēšana ir jāveic manuāli, lapā Debitoru transakcijas izmantojot pogu Atcelt maksājumu.





