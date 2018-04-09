---
title: "Viens dokumenta ar vairākiem debitora vai kreditora ierakstiem"
description: "Šajā tēmā ir sniegts pārskats par to, kas notiek, grāmatojot vienu dokumentu ar vairākiem debitora vai kreditora ierakstiem. Šī funkcionalitāte nebūs pieejama turpmākajās Microsoft Dynamics 365 for Finence and Operations versijās, tāpēc nav ieteicams izmantot šo grāmatošanas metodi, jo uzskaite ietekmē norēķinu apstrādi."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4c499e31fb42a69dff6ac41faac0c78f7f4d1876
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Viens dokumenta ar vairākiem debitora vai kreditora ierakstiem

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegts pārskats par to, kas notiek, grāmatojot vienu dokumentu ar vairākiem debitora vai kreditora ierakstiem. Šī funkcionalitāte nebūs pieejama turpmākajās Microsoft Dynamics 365 for Finence and Operations versijās, tāpēc nav ieteicams izmantot šo grāmatošanas metodi, jo uzskaite ietekmē norēķinu apstrādi. 

Daži visbiežāk sastopamie piemēri, kur viens dokuments tiek izmantots vairākiem debitoriem vai kreditoriem, ir bilances pārskaitījumi starp debitoriem, un tīkla bilances starp debitoriem un kreditoriem tajā pašā organizācijā. 

Dokumentu, kas satur vairāk nekā vienu debitoru vai kreditoru var ievadīt, izmantojot vienu no šīm metodēm:

-   Izmantojot žurnālu ar atlasītu opciju **Tikai 1 dokumenta numurs**, lai katra rinda, kas tiek pievienota žurnālam ir iekļauta tajā pašā dokumentā.
-   Izmantojot vairāku rindu dokumentu, ja nav norādīts korespondējošais virsgrāmatas konts, ar vairāk nekā vienu debitoru vai kreditoru.
-   Ievadot dokumentu ar kontu, un korespondējošais konts ir kreditors/kreditors, debitors/debitors, kreditors/debitors vai debitors/kreditors.

Šajā tēmā ir parādīts, kā tiks apstrādāta nosegšana, grāmatojot vienu dokumentu ar vairākiem debitora vai kreditora ierakstiem. Turklāt šajā tēmā sniegti risinājumi, kas palīdz saprast, kā izvairīties no viena dokumenta ar vairākiem debitoriem vai kreditoriem. Jo īpaši, ir piemēri, kas ilustrē divus visizplatītākos segšanas scenārijus, kas tiek ietekmēti, izmantojot vienu dokumentu ar vairākiem debitoriem vai kreditoriem:

-   Termiņatlaides uzskaite
-   Pārvērtēšanas uzskaite

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Kā segšana ietekmē viena dokumenta lietošanu
Grāmatojot dokumentu, kas ietver vairākus debitora vai kreditora ierakstus, tiek izveidots viens uzskaites dokuments, kas satur vairākus debitoru vai kreditoru atlikumus. Segšanas procesa laikā sākotnējās uzskaites ieraksti tiek izmantoti, lai izveidotu uzskaites ieraksti termiņatlaidei, nerealizētajai peļņai un zaudējumiem, realizētajai peļņai un zaudējumiem, un atvieglojumam oriģinālā dokumenta kopsavilkuma kontā. Piemēram, ja termiņatlaide tiek pieņemta, sedzot kreditora maksājumu rēķinam, termiņatlaides uzskaite jāgrāmato Kreditoru parādu virsgrāmatas kontā no oriģinālā rēķina. Grāmatojot rēķina oriģinālu dokumentā, kas satur vairākus kreditora ierakstus, sākotnējā uzskaite tiek apkopota. Šajā gadījumā, jo nav iespējams piekļūt detalizētam uzskaites ierakstam katrai kreditora darbībai vienā dokumentā, nav iespējams noteikt, kā jāuzskaita lietotājam paredzētā termiņatlaide.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Viens dokuments ar vairākiem kreditoriem un ietekme uz termiņatlaides uzskaiti

Šajā piemērā vairāki kreditora rēķini tiek ierakstīti vienā dokumentā Virsgrāmatā, lapā **Virsgrāmatas žurnāls**. Šie rēķini tiek sadalīti starp vairākām konta dimensijām.

|             |                  |              |                 |           |            |
|-------------|------------------|--------------|-----------------|-----------|------------|
| **Dokuments** | **Konta veids** | **Konts**  | **Apraksts** | **Debetkarte** | **Kredītkarte** |
| GNJL001     | Kreditors           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Kreditors           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Kreditors           | 1001         | INV3            |           | 300,00     |
| GNJL001     | Virsgrāmata           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Virsgrāmata           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Virsgrāmata           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Virsgrāmata           | 606300-004-- | INV3            | 300,00    |            |

Pēc grāmatošanas tiek izveidots viens dokuments.

|             |              |                  |                                    |
|-------------|--------------|------------------|------------------------------------|
| **Dokuments** | **Konts**  | **Grāmatošanas tips** | **Summa darījuma valūtā** |
| GNJL001     | 606300-001-- | Virsgrāmatas žurnāls   | 50,00                              |
| GNJL001     | 606300-002-- | Virsgrāmatas žurnāls   | 50,00                              |
| GNJL001     | 606300-003-- | Virsgrāmatas žurnāls   | 200,00                             |
| GNJL001     | 606300-004-- | Virsgrāmatas žurnāls   | 300,00                             |
| GNJL001     | 200110-001-  | Kreditora bilance   | -100,00                            |
| GNJL001     | 200110-001-  | Kreditora bilance   | –200,00                            |
| GNJL001     | 200110-001-  | Kreditora bilance   | -300.00                            |

Ievērojiet, ka dokuments satur trīs ierakstus vienā dokumentā kreditora bilances grāmatošanas tipam. Nav iespējams norādīt, ka 50,00 debets 606300-001 un 50,00 debets 606300-002 ir paredzēts, lai kompensētu 200110-001 kreditora bilances ierakstu. Tas ir tāpēc, ka lietotājs ir ievadījis vairākus kreditora ierakstus vienā dokumentā.

Izmantojot šo piemēru, iespējams analizēt ietekmi, kas rodas, izmantojot vienu dokumentu, pakārtotā norēķinu uzskaitē. Pieņemsim, ka jums jāmaksā 197,00 no 200,00 rēķina, pieņemot termiņatlaidi 3,00 apmērā. Ievērojiet, ka termiņatlaides konta vērtība tiek piešķirta visām dimensijām no rēķina dokumenta izdevumu kontiem. Tas ir tāpēc, ka tika izmantots viens dokuments, lai grāmatotu augstāk minēto rēķinu bez norādes, kā lietotājs paredz izdevumu sadali, lai savstarpēji saistītu kreditora bilanci vienā dokumentā.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Dokuments** | **Konts**  | **Grāmatošanas tips**     | **Debetkarte** | **Kredītkarte** |
| APPAYM001   | 200110-001-  | Kreditora bilance       | 197.00    |            |
| APPAYM001   | 110110-001-  | Banka                 |           | 197.00     |
| 14000056    | 520200-001-- | Kreditora termiņatlaide |           | 0.25       |
| 14000056    | 520200-002-- | Kreditora termiņatlaide |           | 0.25       |
| 14000056    | 520200-003-- | Kreditora termiņatlaide |           | 1,00       |
| 14000056    | 520200-004-- | Kreditora termiņatlaide |           | 1.50       |
| 14000056    | 200110-001-  | Kreditora bilance       | 3,00      |            |

Ja lietotājs ir neapmierināts ar termiņatlaidi, kas tiek piešķirta visās izdevumu sadalēs no oriģinālā rēķina, nevis no viena dokumenta, jāizmanto vairāki dokumenti, lai ierakstītu rēķinus. Lūk, piemērs, kā vairākus dokumentus var ievadīt Virsgrāmatā, nevis izmantojot vienu dokumentu, kā parādīts šī piemērā sākumā.

|             |                  |              |                 |           |            |                 |                    |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| **Dokuments** | **Konta veids** | **Konts**  | **Apraksts** | **Debetkarte** | **Kredītkarte** | **Korespondējošais veids** | **Korespondējošais konts** |
| GNJL001     | Kreditors           | 1001         | INV1            |           | 100,00     | Virsgrāmata          | &lt;tukšs&gt;      |
| GNJL001     | Virsgrāmata           | 606300-001-- | INV1            |   50,00   |            | Virsgrāmata          | &lt;tukšs&gt;      |
| GNJL001     | Virsgrāmata           | 606300-002-- | INV1            |   50,00   |            | Virsgrāmata          | &lt;tukšs&gt;      |
| GNJL002     | Kreditors           | 1001         | INV2            |           | 200,00     | Virsgrāmata          | 606300-003--       |
| GNJL003     | Kreditors           | 1001         | INV3            |           | 300,00     | Virsgrāmata          | 606300-004--       |

Tagad, kad ir apmaksāts INV2, tiks veikts šāds ieraksts. Ņemiet vērā, ka termiņatlaides finanšu dimensijas seko saistīto izdevumu finanšu dimensijām.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Dokuments** | **Konts**  | **Grāmatošanas tips**     | **Debetkarte** | **Kredītkarte** |
| APPAYM001   | 200110-001-  | Kreditora bilance       | 197.00    |            |
| APPAYM001   | 110110-001-  | Banka                 |           | 197.00     |
| 14000056    | 520200-003-- | Kreditora termiņatlaide |           | 3,00       |
| 14000056    | 200110-001-  | Kreditora bilance       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Viens dokuments ar vairākiem kreditoriem un ietekme uz realizētās peļņas/zaudējumu uzskaiti

|             |                  |             |                 |           |            |                  |              |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| **Dokuments** | **Konta veids** | **Konts** | **Apraksts** | **Debetkarte** | **Kredītkarte** | **Konta veids** | **Konts**  |
| GNJL001     | Kreditors           | 1001        | INV1            |           | 100,00     | Virsgrāmata           | 606300-001-- |
| GNJL001     | Kreditors           | 1001        | INV2            |           | 200,00     | Virsgrāmata           | 606300-002-- |

Šajā piemērā vairāki kreditora rēķini tiek ierakstīti vienā dokumentā Virsgrāmatā, lapā **Virsgrāmatas žurnāls**. Šie rēķini tiek sadalīti starp vairākām konta dimensijām. Pēc grāmatošanas tiek izveidots viens dokuments.

|             |              |                  |                                          |                                         |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| **Dokuments** | **Konts**  | **Grāmatošanas tips** | **Summa darījuma valūtā (EUR)** | **Summa uzskaites valūtā (USD)** |
| GNJL001     | 606300-001-- | Virsgrāmatas žurnāls   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | Virsgrāmatas žurnāls   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Kreditora bilance   | -100,00                                  | -114.00                                 |
| GNJL001     | 200110-001-  | Kreditora bilance   | –200,00                                  | -228.00                                 |

Ievērojiet, ka dokuments satur divus ierakstus vienā dokumentā kreditora bilances grāmatošanas tipam. Nav iespējams norādīt, ka 606300-001 debets ir paredzēts, lai kompensētu piegādātāja bilances ierakstu 100,00 uz 200110-001. Tas ir tāpēc, ka lietotājs ir ievadījis vairākus kreditora ierakstus vienā dokumentā. 

Izmantojot šo piemēru, iespējams analizēt ietekmi, kas rodas, izmantojot vienu dokumentu, pakārtotā norēķinu uzskaitē. Pieņemsim, ka jūsu uzskaites valūta ir USD, un iepriekš minētās darbības tika grāmatotas darbības valūtā EUR. Pieņemsim, ka jūs pilnībā apmaksājat 200,00 EUR rēķinu, bet saskaraties ar realizētiem zaudējumiem, sakarā ar valūtas maiņas kursa starpību laikā, kad jūs grāmatojāt jūsu rēķinu un maksājumu. Ievērojiet, ka realizētā zaudējuma konta vērtība tiek piešķirta visām dimensijām no rēķina dokumenta izdevumu kontiem. Šajā gadījumā tika piešķirtas abas dimensijas 001 un 002, lai gan lietotāja uztverē varētu būt, ka tikai 002 pieder izdevumu kontam no rēķina, kas tiek kompensēts. Tas ir tāpēc, ka tika izmantots viens dokuments, lai grāmatotu augstāk minēto rēķinu bez norādes, kā lietotājs paredz izdevumu sadali, lai savstarpēji saistītu kreditora bilanci vienā dokumentā.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Dokuments** | **Konts** | **Grāmatošanas tips**   | **Summa darījuma valūtā (EUR)** | **Summa uzskaites valūtā (USD)** |
| APPAYM001   | 200110-001- | Kreditora bilance     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Banka               | –200,00                                  | -230.00                                 |
| 14000056    | 801300-001- | Valūtas kursa svārstību zaudējumi | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Valūtas kursa svārstību zaudējumi | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Kreditora bilance     |                                          | -2.00                                   |

Ja lietotājs ir neapmierināts ar Valūtas kursa svārstību zaudējumiem, kas tiek piešķirta visās izdevumu sadalēs no oriģinālā rēķina, nevis no viena dokumenta, jāizmanto vairāki dokumenti, lai ierakstītu rēķinus. Lūk, piemērs, kā vairākus dokumentus var ievadīt Virsgrāmatā, nevis izmantojot vienu dokumentu, kā parādīts šī piemērā sākumā.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Dokuments** | **Konta veids** | **Konts** | **Apraksts** | **Debetkarte** | **Kredītkarte** | **Korespondējošais veids** | **Korespondējošais konts** |
| GNJL002     | Kreditors           | 1001        | INV1            |           | 100,00     | Virsgrāmata          | 606300-001--       |
| GNJL003     | Kreditors           | 1001        | INV2            |           | 200,00     | Virsgrāmata          | 606300-002--       |

Tagad, kad ir apmaksāts INV2, tiks veikts šāds ieraksts. Ņemiet vērā, ka valūtas kursa svārstību zaudējumu finanšu dimensijas seko saistīto izdevumu finanšu dimensijām.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Dokuments** | **Konts** | **Grāmatošanas tips**   | **Summa darījuma valūtā (EUR)** | **Summa uzskaites valūtā (USD)** |
| APPAYM001   | 200110-001- | Kreditora bilance     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Banka               | –200,00                                  | -230.00                                 |
| 14000056    | 801300-002- | Valūtas kursa svārstību zaudējumi | 0,00                                     | 2,00                                    |
| 14000056    | 200110-001- | Kreditora bilance     |                                          | -2.00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Viens dokuments bilances pārskaitījumiem un tīkla scenārijiem
Divi visbiežāk izmantotie scenāriji, kas izmanto vienu dokumentu, kas satur vairākus debitorus vai kreditorus, satur bilances pārskaitījumus no viena debitora/kreditora uz citu debitoru/kreditoru, veicot debitora un kreditora ieskaitu, kas ir vienas un tās pašas organizācijas. Nākamie divi piemēri parāda vēlamo metodi, ievadot šos scenārijus programmatūrā Finance and Operations, kā alternatīvu to ievadīšanai vienā dokumentā. 

*Bilances pārsūtīšana* ir viens dokuments ar vairākiem debitoriem, kas tika ievadīti, lai pārsūtītu bilanci no viena debitora citam debitoram (tas pats kreditoriem). Šis scenārijs var notikt, ja atbildība par rēķinu apmaksu pāriet pie citas puses, piemēram meitas uzņēmums maina atbildību uz mātes uzņēmumu. 

Šajā piemērā tiek pieņemts, ka pārdošana, kurā debitors ir piemērots termiņatlaidei, ja maksājums tiek veikts 10 dienu laikā. Šajā piemērā debitors izmanto apdrošināšanas uzņēmumu, kas būs atbildīgs par rēķina apmaksu. Apdrošināšanas uzņēmums sistēmā tiek iestatīts kā otrs debitors. Oriģinālā debitora bilance tiek pārsūtīta uz apdrošināšanas uzņēmumu, kurš apmaksā rēķinu, saņemot 2% termiņatlaidi, apmaksājot atlaides perioda ietvaros. 

Lai ilustrētu, pieņemsim, ka šāda pārdošana tiek veikta debitoram ACME. Šādas uzskaites ieraksti atspoguļo pārdošanu.

|                    |                  |           |            |
|--------------------|------------------|-----------|------------|
| **Virsgrāmatas konts** | **Grāmatošanas tips** | **Debetkarte** | **Kredītkarte** |
| 401100-002-023-    | Ieņēmumi          |           | 100        |
| 130100-002-        | Debitora bilance | 100       |            |

Pēc tam lietotājs pārsūta bilanci apmaksai no ACME apdrošināšanas kompānijai vienā dokumentā Debitoru parādu žurnālā. Programmatūrā Finance and Operations apdrošināšanas uzņēmums tiek iestatīts kā debitors Apdrošināšana.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Dokuments** | **Konta veids** | **Konts** | **Apraksts** | **Debetkarte** | **Kredītkarte** | **Korespondējošais veids** | **Korespondējošais konts** |
| ARPAYM001   | Debitors         | ACME        | Pārsūtījums        |           | 100,00     | Debitors        | Apdrošināšana          |

Ņemiet vērā, ka augstāk minētais ieraksts ir ietverts vienā dokumentā. Šis dokuments satur divus debitora ierakstus. Šāds dokuments tiek izveidots, kad tiek grāmatots augstāk minētais Virsgrāmatas ieraksts.

|             |             |                  |                                    |
|-------------|-------------|------------------|------------------------------------|
| **Dokuments** | **Konts** | **Grāmatošanas tips** | **Summa darījuma valūtā** |
| ARPAYM001   | 130100-002- | Debitora bilance | 100,00                             |
| ARPAYM001   | 130100-002- | Debitora bilance | -100,00                            |

Tālāk, pieņemsim, ka jūs saņemat maksājumu no debitora Apdrošināšana par 98,00 un izvēlaties kompensēt maksājumu ar rēķinu, kas tika izveidots bilances pārsūtīšanai. Tā rezultātā tiek grāmatots šāds dokuments. Var būt cerības, ka nosegšana izmanto finanšu dimensijas no oriģinālā rēķina, bet tas nav iespējams, jo debitoram Apdrošināšana nav rēķina dokumenta. Ņemiet vērā, ka pēc noklusējuma sadales dimensijas termiņatlaide nāk no debitora darbības, kas izveidota no pārsūtīšanas, nevis no oriģinālā rēķina ieņēmumu konta. Noklusējums ir viena dokumenta izmantošanas bilanču pārsūtīšanai rezultāts.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Dokuments** | **Konts** | **Grāmatošanas tips** | **Debetkarte** | **Kredītkarte** |
| ARPAYM002   | 110110-002- | Banka             | 98.00     |            |
| ARPAYM002   | 130100-002- | Debitora bilance |           | 98.00      |

Termiņatlaides saistītajā dokumentā, noklusējums finanšu dimensijai tiek ņemts no debitora darbības, kas tiek izveidota no pārsūtīšanas, jo pārsūtījumam ir vairāk nekā viens debitors.

|             |             |                        |           |            |
|-------------|-------------|------------------------|-----------|------------|
| **Dokuments** | **Konts** | **Grāmatošanas tips**       | **Debetkarte** | **Kredītkarte** |
| ARP-00001   | 403300-002- | Debitora termiņatlaide | 2,00      |            |
| ARP-00001   | 130100-002- | Debitora bilance       |           | 2,00       |

Ja lietotājs ir neapmierināts ar noklusējumu finanšu dimensijām termiņatlaidei, viena dokumenta vietā nepieciešams izmantot vairākus dokumentus, lai ierakstītu bilances pārsūtīšanu. Šis scenārijs jāpaveic, izveidojot kredītrēķinu debitoram, kura bilance tiek pārvietota NO, un debetrēķinu vai rēķinu debitoram, kura bilance tiek pārveidota UZ. Šajā piemērā ir parādīts, kā vairākus dokumentus var ievadīt Debitoru parādu žurnālā, lai pārsūtītu bilanci, nevis izmantot vienu dokumentu, kā aprakstīts iepriekš šajā piemērā.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Dokuments** | **Konta veids** | **Konts** | **Apraksts** | **Debetkarte** | **Kredītkarte** | **Korespondējošais veids** | **Korespondējošais konts** |
| ARPAYM001   | Debitors         | ACME        |                 |           | 100,00     | Virsgrāmata          | 401100-002-023-    |
| ARPAYM002   | Debitors         | Apdrošināšana   |                 | 100,00    |            | Virsgrāmata          | 401100-002-023-    |

Tas nozīmē, ka ja debitors Apdrošināšana maksā 98,00 ar dokumentu ARPAYM02, tiks izmantotas pareizas finanšu dimensijas no dokumenta ARPAYM002 virsgrāmatas konta ieraksta.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Dokuments** | **Konts** | **Grāmatošanas tips** | **Debetkarte** | **Kredītkarte** |
| ARPAYM003   | 110110-002- | Banka             | 98.00     |            |
| ARPAYM003   | 130100-002  | Debitora bilance |           | 98.00      |

Termiņatlaides saistītajā dokumentā, finanšu dimensijas tiks izmantotas no korespondējošā ieņēmumu konta, kas redzams ARPAYM002 dokumentā.

|             |                 |                        |           |            |
|-------------|-----------------|------------------------|-----------|------------|
| **Dokuments** | **Konts**     | **Grāmatošanas tips**       | **Debetkarte** | **Kredītkarte** |
| ARP-00001   | 403300-002-023- | Debitora termiņatlaide | 2,00      |            |
| ARP-00001   | 130100-002-     | Debitora bilance       |           | 2,00       |

### 

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Viens dokuments ar kompensēšanu vairākiem debitoriem un kreditoriem
Kompensēšana var būt noderīga, ja uzņēmums pērk un pārdod vienā uzņēmumā. Tā vietā, lai maksātu kreditora rēķinus un gaidītu, lai saņemtu maksājumu par debitora rēķiniem, kreditora un debitora rēķini tiek kompensēti. Kompensēšanas darbība tiek nosegta pret nesamaksātajām bilancēm. 

Lai ilustrētu, pieņemsim, ka kreditors 1001 un klients US-008 ir viena juridiska persona, tāpēc jūsu uzņēmums vēlas nosegt maksājumu un ieņēmumu bilances pirms atlikušās bilances maksāšanas/saņemšanas. Pieņemsim, ka debitora ieraksts ir parādā 75.00 EUR, un kreditora ieraksts ir parādā 100,00 EUR, tas nozīmē, ka jūs vēlētos nosegt bilances un apmaksāt kreditoram tikai 25,00 EUR. Tālāk pieņemsim, ka uzskaites valūta ir USD. Šajā gadījumā nosegšanas darbība tiek ievadīta vienā dokumentā parādu kreditoriem maksājumu žurnālā.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Dokuments** | **Konta veids** | **Konts** | **Apraksts** | **Debetkarte** | **Kredītkarte** | **Korespondējošais veids** | **Korespondējošais konts** |
| APPAYM001   | Kreditors           | 1001        | Tīkli         |  75,00    |            | Debitors        | US-008             |

Lai novērstu nevēlamas problēmas ar turpmāku nosegšanu šai darbībai, viena viena dokumenta izmantošanas vietā, žurnālā vajadzētu ievadīt vairākus dokumentus, lai ierakstītu nosegšanas darbību. Ņemiet vērā, ka debitoru un kreditoru bilances tiek kompensētas ar vienu klīringa kontu, lai izvairītos no viena dokumenta izmantošanas, kas satur vairākas debitoru un kreditoru bilances.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Dokuments** | **Konta veids** | **Konts** | **Apraksts** | **Debetkarte** | **Kredītkarte** | **Korespondējošais veids** | **Korespondējošais konts** |
| 001         | Debitors         | US-008      |                 |           |  75,00     | Virsgrāmata          | 999999---          |
| 002         | Kreditors           | 1001        |                 |  75,00    |            | Virsgrāmata          | 999999---          |

 




