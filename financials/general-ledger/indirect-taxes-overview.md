---
title: "Pārdošanas nodokļa apskats"
description: "Šajā rakstā ir sniegts pārskats par pārdošanas nodokļa sistēmu. Tajā ir paskaidroti pārdošanas nodokļa iestatīšanas elementi un to mijiedarbība."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 1adee145d705f239e0c663d310234286478fead0
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-overview"></a>Pārdošanas nodokļa apskats

Šajā rakstā ir sniegts pārskats par pārdošanas nodokļa sistēmu. Tajā ir paskaidroti pārdošanas nodokļa iestatīšanas elementi un to mijiedarbība.

<a name="overview"></a>Pārskats
--------

PVN struktūra atbalsta dažāda veida netiešos nodokļus kā PVN, pievienotās vērtības nodokļa (PVN), precēm un pakalpojumiem nodokli (GST), vienības pamatota maksa un ieturēto nodokli. Šie nodokļi tiek aprēķināti un dokumentēta laikā pirkšanas un pārdošanas darījumiem. Periodiski, tām jābūt ziņoja un maksā nodokļu iestādēm. 

Nākamajā diagrammā ir parādīti nodokļu iestatījumu elementi un kā tie ir saistīti.

[![TaxOverview](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Katru PVN sabiedrība jāveido, jādefinē PVN kodu. Pārdošanas nodokļa kods glabā nodokļu likmes un aprēķina kārtulas šim pārdošanas nodoklim. 

Katrs pārdošanas nodokļa kods ir jāsaista ar pārdošanas nodokļa apmaksas periodu. Pārdošanas nodokļa apmaksas periodi definē intervālus, kādos par pārdošanas nodokli ir jāziņo un tas ir jāsamaksā pārdošanas nodokļa iestādei. Katrs pārdošanas nodokļa apmaksas periods ir jāpiešķir kādai pārdošanas nodokļa iestādei. Pārdošanas nodokļa iestāde ir persona, kam tiek ziņots par pārdošanas nodokli un kam tas tiek samaksāts. Tas definē arī pārdošanas nodokļa atskaites izkārtojumu. Pārdošanas nodokļa iestādes var būt saistītas ar kreditoru kontiem. 

Katrs pārdošanas nodokļa kods ir jāsaista arī ar virsgrāmatas grāmatošanas grupu. Virsgrāmatas grāmatošanas grupa norāda galvenos kontus, kuros ir jāgrāmato pārdošanas nodokļa kodu summas. 

Var definēt arī papildu pārdošanas nodokļa atskaišu veidošanas kodus. Tos var piešķirt pārdošanas nodokļa kodiem dažādu veidu summām, kuras tiek aprēķinātas pārdošanas nodokļa kodam. Atskaitē **Pārdošanas nodokļa maksājums pa kodiem** ir redzamas kopsummas katram pārdošanas nodokļa atskaišu kodam attiecībā uz noteiktu pārdošanas nodokļa apmaksas periodu un intervālu. 

Katrai transakcijai, kurai ir jāaprēķina un jāgrāmato pārdošanas nodoklis, ir nepieciešama pārdošanas nodokļu grupa un krājuma pārdošanas nodokļu grupa. Pārdošanas nodokļu grupas ir saistītas ar transakcijas pusi (piemēram, debitoru vai kreditoru), bet krājumu pārdošanas nodokļu grupas ir saistītas ar transakcijas resursu (piemēram, ar krājumu vai sagādes kategoriju). Nodokļu grupas ietver nodokļu kodu sarakstu. Nodokļu kodi, kas atrodas gan pārdošanas nodokļu grupā, gan krājumu pārdošanas nodokļu grupā attiecībā uz transakciju, ir nodokļu kodi, kas attiecas uz šo transakciju. 

Nākamajā tabulā ir aprakstīti nodokļa iestatīšanas elementi un to secība.

| Iestatīšanas darbība                                                  | Vai darbība ir obligāta/neobligāta un tās apraksts                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Izveidojiet galvenos kontus.                                           | Obligāta. Pirms pārdošanas nodokļa funkcionalitātes iestatīšanas ir jāizveido galvenie konti, ko uzņēmums lieto nodokļu samaksai un to ierakstīšanai.                                                                                                                                                                             |
| Iestatiet Virsgrāmatas grāmatošanas grupas pievienotās vērtības nodoklim.                     | Obligāta. Virsgrāmatas grāmatošanas grupas definē galvenos kontus pārdošanas nodokļu reģistrēšanai un maksāšanai.                                                                                                                                                                                                                            |
| Iestatiet pārdošanas nodokļa iestādes.                                   | Obligāta. Pārdošanas nodokļa iestādes ir iestādes, kurām šis nodoklis ir jāziņo un jāmaksā.                                                                                                                                                                                                                                   |
| Iestatiet pārdošanas nodokļa apmaksas periodus.                            | Obligāta. Pārdošanas nodokļa apmaksas periodi satur informāciju par to, kad un cik bieži ir jāatskaitās par pārdošanas nodokli un tas ir jāmaksā. Tie ir saistīti ar pārdošanas nodokļa iestādi.                                                                                                                                                       |
| Iestatiet pārdošanas nodokļu atskaišu kodus.                               | Neobligāta. Pārdošanas nodokļa atskaišu kodus var piešķirt pārdošanas nodokļa kodiem, lai ziņotu summas vairākiem pārdošanas nodokļa kodiem saskaņā ar vienu pārdošanas nodokļa atskaišu kodu.                                                                                                                                                                 |
| Iestatiet pārdošanas nodokļa kodus.                                         | Obligāta. Pārdošanas nodokļa kodi ietver nodokļu likmes un aprēķina kārtulas katram pārdošanas nodoklim. Pārdošanas nodokļa kodi ir saistīti ar pārdošanas nodokļa apmaksas periodu un virsgrāmatas grāmatošanas grupu.                                                                                                                                        |
| Iestatiet pārdošanas nodokļu grupas.                                        | Obligāta. Pārdošanas nodokļu grupas satur sarakstu ar pārdošanas kodiem, kas attiecas uz transakcijas pusi (debitoru vai kreditoru). Attiecīgajai transakcijai pārdošanas nodokļa kodu krustpunkts pārdošanas nodokļu grupā un krājumu pārdošanas nodokļu grupā nosaka pārdošanas nodokļa kodus, kas attiecas uz šo transakciju.                  |
| Iestatiet krājumu pārdošanas nodokļu grupas.                                   | Obligāta. Krājumu pārdošanas nodokļu grupas satur sarakstu ar pārdošanas kodiem, kas attiecas uz transakcijas resursu (preci, pakalpojumu un citiem resursiem). Attiecīgajai transakcijai pārdošanas nodokļa kodu krustpunkts pārdošanas nodokļu grupā un krājumu pārdošanas nodokļu grupā nosaka pārdošanas nodokļa kodus, kas attiecas uz šo transakciju. |
| Iestatiet pārdošanas nodokļa parametrus programmas parametru lapās. | Obligāta. Dažādos apgabalos, piemēram, apgabalos Virsgrāmata, Debitori un Kreditori, ir jāiestata parametri pareizai netiešo nodokļu aprēķināšanai. Lai gan lielākajai daļai šo parametru ir noklusējuma vērtības, tās ir jāmaina, lai atbilstu katra uzņēmuma vajadzībām.                                          |

## <a name="sales-tax-on-transactions"></a>Pārdošanas nodoklis transakcijām
Katrā transakcijā (pārdošanas/pirkšanas dokumentu rindās, žurnālos un citur) jums ir jāievada pārdošanas nodokļu grupa un krājumu pārdošanas nodokļu grupa pārdošanas nodokļa aprēķināšanai. Noklusējuma grupas ir norādītas pamatdatos (piemēram, debitoram, kreditoram, krājumam un sagādes kategorijai), bet transakcijas grupas varat manuāli mainīt, ja nepieciešams. Abās grupās ietilpst saraksts ar pārdošanas nodokļa kodiem, un pārdošanas nodokļa kodu abu sarakstu krustpunkts nosaka transakcijai piemērojamo pārdošanas nodokļa kodu sarakstu. 

Katrā transakcijā aprēķināto pārdošanas nodokli varat uzmeklēt, atverot lapu **Pārdošanas nodokļa transakcija**. Varat uzmeklēt pārdošanas nodokli dokumenta rindai vai visam dokumentam. Noteiktiem dokumentiem (piemēram, kreditora rēķinam un virsgrāmatas žurnāliem) varat pielāgot aprēķināto pārdošanas nodokli, ja sākotnējā dokumentā tiek rādītas summas ar novirzēm.

## <a name="sales-tax-settlement-and-reporting"></a>Pārdošanas nodokļa apmaksa un atskaišu veidošana
Pārdošanas nodoklis regulāri (reizi mēnesī, reizi ceturksnī un citos intervālos) ir jāziņo un jāmaksā nodokļu iestādēm. Microsoft Dynamics 365 operācijām nodrošina funkcionalitāti, kas ļauj atrisināt nodokļu kontiem intervālam un kompensēt nodokļu norēķinu kontu, kas norādīts Virsgrāmatas grāmatošanas grupas bilances. Šo funkcionalitāti var piekļūt no **nokārtot un grāmatotu PVN** lapā. PVN apmaksas periodu, ka PVN būtu jāatrisina, ir jānorāda. 

Kad pārdošanas nodoklis ir samaksāts, bilance pārdošanas nodokļa apmaksas kontā vajadzētu būt saskaņotai pret bankas kontu. Ja pārdošanas nodokļa iestāde, kas ir norādīta pārdošanas nodokļa apmaksas periodam, ir saistīta ar kreditora kontu, tad pārdošanas nodokļa bilance tiek grāmatota kā atvērts kreditora rēķins, un to var iekļaut regulāra maksājuma priekšlikumā.

## <a name="conditional-sales-tax"></a>Nosacījuma PVN
Nosacījuma PVN ir PVN, par kuru izmaksā proporcionāli faktisko summu, kas tiek maksāts par rēķinu. Savukārt, standarta PVN tiek aprēķināts pēc rēķina izrakstīšanas laikā. Nosacījuma PVN ir samaksāti nodokļu iestādē, grāmatojot maksājumu, nevis tad, kad rēķins ir iegrāmatots. Iegrāmatojot rēķinu, darbība ir jāziņo par PVN grāmatas pārskatā. Tomēr darbība ir jāizslēdz no PVN maksājumu pārskats. 

Ja formas Virsgrāmatas parametri atzīmējiet izvēles rūtiņu nosacījuma PVN, nav PVN var atskaitīt līdz brīdim, kad jūs esat samaksājis rēķinu. Šī nav tikai juridiska prasība, dažās valstīs/reģionos.

> [!NOTE]
> Atzīmējot izvēles rūtiņu nosacījuma PVN, PVN kodi un PVN grupu iestatīšanu un arī izveidotu Virsgrāmatas kontējuma grupu, lai atbalstītu funkcionalitāti. |

###  <a name="example"></a>Paraugs

PVN apmaksā, katru mēnesi. 15. jūnijs, jāizveido debitora rēķina 10 000 plus PVN.
-   Pārdošanas nodoklis ir 25 procenti jeb 2500.
-   Rēķina apmaksa ir jāmaksā 30 jūlijs.

Jūs parasti ir nokārtot un maksāt 2,500 nodokļu iestādei pēc rēķina iegrāmatošanas jūnijā, pat tad, ja jums nav saņēmuši samaksu no klienta. 

Tomēr, izmantojot nosacījuma PVN, jūs norēķinātos ar nodokļu iestādei saņemot samaksu no klienta 30 jūlijā.


