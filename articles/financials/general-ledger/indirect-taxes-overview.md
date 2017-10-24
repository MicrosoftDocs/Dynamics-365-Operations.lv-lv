---
title: "Pārdošanas nodokļa apskats"
description: "Šajā rakstā ir sniegts pārskats par pārdošanas nodokļa sistēmu. Tajā ir paskaidroti pārdošanas nodokļa iestatīšanas elementi un to mijiedarbība."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f4838dade6b2694a11f4b9775fe53560b1332f18
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="sales-tax-overview"></a>Pārdošanas nodokļa apskats

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Šajā rakstā ir sniegts pārskats par pārdošanas nodokļa sistēmu. Tajā ir paskaidroti pārdošanas nodokļa iestatīšanas elementi un to mijiedarbība.

<a name="overview"></a>Pārskats
--------

PVN struktūra atbalsta daudzus netiešo nodokļu veidus, piemēram, PVN, pievienotās vērtības nodokli (PVN), preču un pakalpojumu nodokli (GST), no vienībām atkarīgās papildmaksas un ieturēto nodokli. Šie nodokļi tiek aprēķināti un dokumentēti pirkšanas un pārdošanas transakciju laikā. Periodiski par tiem ir jāziņo un tie ir jāsamaksā nodokļu iestādēm. 

Nākamajā diagrammā ir parādīti nodokļu iestatījumu elementi un kā tie ir saistīti.

[![TaxOverview](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Katram PVN veidam, par kuru uzņēmumam ir jāatskaitās, ir jādefinē PVN kods. Pārdošanas nodokļa kods glabā nodokļu likmes un aprēķina kārtulas šim pārdošanas nodoklim. 

Katrs pārdošanas nodokļa kods ir jāsaista ar pārdošanas nodokļa apmaksas periodu. Pārdošanas nodokļa apmaksas periodi definē intervālus, kādos par pārdošanas nodokli ir jāziņo un tas ir jāsamaksā pārdošanas nodokļa iestādei. Katrs pārdošanas nodokļa apmaksas periods ir jāpiešķir kādai pārdošanas nodokļa iestādei. Pārdošanas nodokļa iestāde ir persona, kam tiek ziņots par pārdošanas nodokli un kam tas tiek samaksāts. Tas definē arī pārdošanas nodokļa atskaites izkārtojumu. Pārdošanas nodokļa iestādes var būt saistītas ar kreditoru kontiem. Plašāku informāciju skatiet šeit: [Iestatīt PVN apmaksas periodus](tasks/set-up-sales-tax-settlement-periods.md).

Katrs pārdošanas nodokļa kods ir jāsaista arī ar virsgrāmatas grāmatošanas grupu. Virsgrāmatas grāmatošanas grupa norāda galvenos kontus, kuros ir jāgrāmato pārdošanas nodokļa kodu summas. 

Var definēt arī papildu pārdošanas nodokļa atskaišu veidošanas kodus. Tos var piešķirt pārdošanas nodokļa kodiem dažādu veidu summām, kuras tiek aprēķinātas pārdošanas nodokļa kodam. Atskaitē **Pārdošanas nodokļa maksājums pa kodiem** ir redzamas kopsummas katram pārdošanas nodokļa atskaišu kodam attiecībā uz noteiktu pārdošanas nodokļa apmaksas periodu un intervālu. 

Katrai transakcijai, kurai ir jāaprēķina un jāgrāmato pārdošanas nodoklis, ir nepieciešama pārdošanas nodokļu grupa un krājuma pārdošanas nodokļu grupa. Pārdošanas nodokļu grupas ir saistītas ar transakcijas pusi (piemēram, debitoru vai kreditoru), bet krājumu pārdošanas nodokļu grupas ir saistītas ar transakcijas resursu (piemēram, ar krājumu vai sagādes kategoriju). Nodokļu grupas ietver nodokļu kodu sarakstu. Nodokļu kodi, kas atrodas gan pārdošanas nodokļu grupā, gan krājumu pārdošanas nodokļu grupā attiecībā uz transakciju, ir nodokļu kodi, kas attiecas uz šo transakciju. 

Nākamajā tabulā ir aprakstīti nodokļa iestatīšanas elementi un to secība.

| Iestatīšanas darbība                                                  | Vai darbība ir obligāta/neobligāta un tās apraksts                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Izveidojiet galvenos kontus.                                           | Obligāta. Pirms pārdošanas nodokļa funkcionalitātes iestatīšanas ir jāizveido galvenie konti, ko uzņēmums lieto nodokļu samaksai un to ierakstīšanai.                                                                                                                                                                             |
| Iestatiet Virsgrāmatas grāmatošanas grupas pievienotās vērtības nodoklim.                     | Obligāta. Virsgrāmatas grāmatošanas grupas definē galvenos kontus pārdošanas nodokļu reģistrēšanai un maksāšanai.   Plašaku informāciju skatiet šeit: [Virsgrāmatas PVN grāmatošanas grupu iestatīšana](tasks/set-up-ledger-posting-groups-sales-tax.md).                                                                                 |
| Iestatiet pārdošanas nodokļa iestādes.                                   | Obligāta. Pārdošanas nodokļa iestādes ir iestādes, kurām šis nodoklis ir jāziņo un jāmaksā.    Plašāku informāciju skatiet šeit: [PVN iestāžu iestatīšana](tasks/set-up-sales-tax-authorities.md).                                                                                                                                          |
| Iestatiet pārdošanas nodokļa apmaksas periodus.                            | Obligāta. Pārdošanas nodokļa apmaksas periodi satur informāciju par to, kad un cik bieži ir jāatskaitās par pārdošanas nodokli un tas ir jāmaksā. Tie ir saistīti ar pārdošanas nodokļa iestādi.                                                                                                                                                       |
| Iestatiet pārdošanas nodokļu atskaišu kodus.                               | Neobligāta. Pārdošanas nodokļa atskaišu kodus var piešķirt pārdošanas nodokļa kodiem, lai ziņotu summas vairākiem pārdošanas nodokļa kodiem saskaņā ar vienu pārdošanas nodokļa atskaišu kodu. Plašāku informāciju skatiet šeit: [Iestatīt PVN pārskatu kodus](tasks/set-up-sales-tax-reporting-codes.md).                                         |
| Iestatiet pārdošanas nodokļa kodus.                                         | Obligāta. Pārdošanas nodokļa kodi ietver nodokļu likmes un aprēķina kārtulas katram pārdošanas nodoklim. Pārdošanas nodokļa kodi ir saistīti ar pārdošanas nodokļa apmaksas periodu un virsgrāmatas grāmatošanas grupu. Plašāku informāciju skatiet šeit: [Iestatīt PVN kodus](tasks/set-up-sales-tax-codes.md).                                |
| Iestatiet pārdošanas nodokļu grupas.                                        | Obligāta. Pārdošanas nodokļu grupas satur sarakstu ar pārdošanas kodiem, kas attiecas uz transakcijas pusi (debitoru vai kreditoru). Attiecīgajai transakcijai pārdošanas nodokļa kodu krustpunkts pārdošanas nodokļu grupā un krājumu pārdošanas nodokļu grupā nosaka pārdošanas nodokļa kodus, kas attiecas uz šo transakciju.                  |
| Iestatiet krājumu pārdošanas nodokļu grupas.                                   | Obligāta. Krājumu pārdošanas nodokļu grupas satur sarakstu ar pārdošanas kodiem, kas attiecas uz transakcijas resursu (preci, pakalpojumu un citiem resursiem). Attiecīgajai transakcijai pārdošanas nodokļa kodu krustpunkts pārdošanas nodokļu grupā un krājumu pārdošanas nodokļu grupā nosaka pārdošanas nodokļa kodus, kas attiecas uz šo transakciju. Plašāku informāciju skatiet šeit: [PVN grupu un krājumu PVN grupu iestatīšana](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md). |
| Iestatiet pārdošanas nodokļa parametrus programmas parametru lapās. | Obligāta. Dažādos apgabalos, piemēram, apgabalos Virsgrāmata, Debitori un Kreditori, ir jāiestata parametri pareizai netiešo nodokļu aprēķināšanai. Lai gan lielākajai daļai šo parametru ir noklusējuma vērtības, tās ir jāmaina, lai atbilstu katra uzņēmuma vajadzībām.                                          |

## <a name="sales-tax-on-transactions"></a>Pārdošanas nodoklis transakcijām
Katrā transakcijā (pārdošanas/pirkšanas dokumentu rindās, žurnālos un citur) jums ir jāievada pārdošanas nodokļu grupa un krājumu pārdošanas nodokļu grupa pārdošanas nodokļa aprēķināšanai. Noklusējuma grupas ir norādītas pamatdatos (piemēram, debitoram, kreditoram, krājumam un sagādes kategorijai), bet transakcijas grupas varat manuāli mainīt, ja nepieciešams. Abās grupās ietilpst saraksts ar pārdošanas nodokļa kodiem, un pārdošanas nodokļa kodu abu sarakstu krustpunkts nosaka transakcijai piemērojamo pārdošanas nodokļa kodu sarakstu. 

Katrā transakcijā aprēķināto pārdošanas nodokli varat uzmeklēt, atverot lapu **Pārdošanas nodokļa transakcija**. Varat uzmeklēt pārdošanas nodokli dokumenta rindai vai visam dokumentam. Noteiktiem dokumentiem (piemēram, kreditora rēķinam un virsgrāmatas žurnāliem) varat pielāgot aprēķināto pārdošanas nodokli, ja sākotnējā dokumentā tiek rādītas summas ar novirzēm.

## <a name="sales-tax-settlement-and-reporting"></a>Pārdošanas nodokļa apmaksa un atskaišu veidošana
Pārdošanas nodoklis regulāri (reizi mēnesī, reizi ceturksnī un citos intervālos) ir jāziņo un jāmaksā nodokļu iestādēm. Microsoft Dynamics 365 for Finance and Operations, izdevums Enterprise nodrošina funkcijas, kas sniedz iespēju segt nodokļu kontus par to intervālu un nobīdīt bilances tam nodokļa apmaksas kontam, kas ir norādīts virsgrāmatas grāmatošanas grupās. Šīm funkcijām var piekļūt lapā **Nosegt un grāmatot PVN**. Ir jānorāda PVN segšanas periods, par kuru ir jāsedz PVN. 

Kad pārdošanas nodoklis ir samaksāts, bilance pārdošanas nodokļa apmaksas kontā vajadzētu būt saskaņotai pret bankas kontu. Ja pārdošanas nodokļa iestāde, kas ir norādīta pārdošanas nodokļa apmaksas periodam, ir saistīta ar kreditora kontu, tad pārdošanas nodokļa bilance tiek grāmatota kā atvērts kreditora rēķins, un to var iekļaut regulāra maksājuma priekšlikumā.

## <a name="conditional-sales-tax"></a>Nosacījuma PVN
Nosacījuma PVN ir PVN, kas tiek maksāts proporcionāli faktiskajai rēķina apmaksas summai. Turpretim standarta PVN tiek aprēķināts rēķina izrakstīšanas laikā. Nosacījuma PVN ir jāmaksā nodokļu iestādei maksājuma grāmatošanas laikā, nevis rēķina grāmatošanas laikā. Rēķina grāmatošanas laikā transakcija ir jāreģistrē PVN grāmatas pārskata. Taču transakcija ir jāizslēdz no PVN maksājuma pārskata. 

Ja veidlapā Virsgrāmatas parametri ir atzīmēta izvēles rūtiņa Nosacījuma PVN, PVN nevar ieturēt līdz rēķina apmaksai. Dažās valstīs/reģionos tā ir likumā noteikta prasība.

> [!NOTE]
> Ja ir atzīmēta izvēles rūtiņa Nosacījuma PVN, ir jāiestata PVN kodi un PVN grupas un jāizveido Virsgrāmatas grāmatošanas grupas šīs funkcijas atbalstam. |

###  <a name="example"></a>Piemērs

Jūs sedzat PVN katru mēnesi. 15. jūnijā jūs izveidojat debitora rēķinu par 10 000 plus PVN.
-   PVN ir 25 procenti jeb 2500.
-   Rēķins ir jāapmaksā līdz 30. jūlijam.

Parasti nodokļu iestādei ir jāsamaksā 2500 jūnijā, kad tiek grāmatots rēķins, lai gan vēl neesat saņēmis maksājumu no debitora. 

Taču, ja lietojat nosacījuma PVN, PVN nodokļu iestādei ir jāmaksā 30. jūlijā, kad saņemat maksājumu no debitora.


Plašāku informāciju skatiet šeit: [Iestatīt ieturētā nodokļa kodus](tasks/set-up-withholding-tax.md).

