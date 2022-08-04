---
title: Izmaksu darījumu elementi
description: Šajā rakstā ir sniegta informācija par izmaksu darbību elementiem, kas aktivizē izmaksu vērtību, lai tās sadalītu starp izmaksu apgabala saturu, izmantojot sadalīšanas metodes atlasi.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 0084d47bf85050749b2668d273db07670aaeae2a
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166809"
---
# <a name="cost-transaction-entities"></a>Izmaksu darījumu elementi

[!include [banner](../includes/banner.md)]

## <a name="apportionment"></a>Norīkojums

Kopējās sūtījuma izmaksas ļauj izmaksu vērtību sadalīt starp izmaksu zonas saturu (reiss, nosūtīšanas konteiners utt.) ar iespēju atlasīt iedalījuma metodi. Attiecību metode ir iestatīta kā daļa no automātisko izmaksu konfigurācijas, kas ir balstīta uz biznesa noteikumiem. Kad tiek izveidota reisa rinda, tā tiek vilkta cauri kā izmaksu daļa.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Konfigurēt izmantošanas kartēšanu izmantošanai ar datu elementiem

Izveidojot izmaksas no ārēja avota, piemēram, kravas ekspeditāja, šim ārējam avotam nevar norādīt vēlamo metodi izmaksu vērtības iedašanai. Sadales kartēšana nosaka noklusējuma sadales metodi katram izmaksu tipa kodam. Pie sadales kartēšanas tabulas **var** piekļūt no programmas Microsoft Dynamics 365 Supply Chain Management lapu Kategoriju kartēšana (**\>\> Ar zemes izmaksu iestatījumu kartējums**).

Ja kartēšanas kombinācija ir definēta un izmaksas, kas atbilst izmaksu tipa kodam, tiek izveidotas, izmantojot izmaksu darbības elementu, kartētā iekļaušanas metode tiks izmantota tā vietā, lai kādai vērtībai būtu jābūt sniegtai entītijai.

Ja kartēšanas tabulā nav nevienas vērtības, bet elementam ir sniegta vērtība, tiks izmantota šī vērtība.

Ja kartēšanas tabulā vai elementam iesniegtajā ierakstā nav vērtības, izveide neizdosies.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Pārkraušanas kartēšana (ITMApportionmentMapping)

Sadales kartēšanas elements (`ITMApportionmentMapping`) izveido sadales kartēšanas attiecības un ļauj lietotājiem izveidot vai atjaunināt ierakstus.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Norīkojuma metode | ITMApportionmentMapping.ApportionmentMethod | Int | Nē | Nē |
| Izmaksu veida kods | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Jā** | Nē |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Reisa izmaksas (ITMCostTransVoyageEntity)

Reisa izmaksu elements (`ITMCostTransVoyageEntity`) izveido reisa izmaksu darbības, kas tiek piemērotas reisa līmenī. Importēšanas procesa laikā sistēma izmanto metodes Kategorijas un Ieskaitīšana vērtības, **·** **kas** ir iekļautas entītijā, lai noteiktu, kā izmaksu vērtība tiek izmaksāta pār reisa saturu.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Norīkojuma metode | ITMCostTrans.ApportionmentMethod | Int | Nē | Nē |
| Izmaksu vērtība | ITMCostTrans.CostValue | Skaitlis (32, 6) | Nē | Nē |
| Valūta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nē | **Jā** |
| Rindas numurs | ITMCostTrans.LineNum | Skaitlis (32, 16) | **Jā** | Nē |
| Saistīto izmaksu veids | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nē | Nē |
| Minimālās izmaksas | ITMCostTrans.MinCostAmount | Skaitlis (32, 6) | Nē | Nē |
| Kategorija | ITMCostTrans.ShipCostCategory (Francija) | Int | Nē | Nē |
| Izmaksu veida kods | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nē | Nē |
| Uzņēmums | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nē | **Jā** |
| Reiss | ITMCostTrans.TransRecId | Nvarchar(20) | **Jā** | Nē |
| Krājumu PVN grupa | ITMCostTrans.TaxItemGroup (datu grupa) | Nvarchar(10) | Nē | Nē |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Piegādes konteinera izmaksas (ITMCostTransShippingContainerEntity)

Piegādes konteinera izmaksu elements (`ITMCostTransShippingContainerEntity`) izveido piegādes konteinera izmaksas, kas tiek piemērotas nosūtīšanas konteinera līmenī. Importēšanas procesa laikā sistēma izmanto kategorijas un ieskaita metodes vērtības, **·** **kas** ir iekļautas entītijā, lai noteiktu, kā izmaksu vērtība tiek izmaksāta pār nosūtīšanas konteinera saturu.

Lauki **Apkopot**, **Leg** un **Saistīts kājai** ir raksturīgi ierakstiem, kuru **izmaksu apgabala vērtība** ir Pārvadāšanas *konteiners*. Tāpēc to nav datu entītijās citiem izmaksu apgabaliem.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Uzkrātā | ITMCostTrans.AggregatedCost | Int | Nē | Nē |
| Norīkojuma metode | ITMCostTrans.ApportionmentMethod | Int | Nē | Nē |
| Izmaksu vērtība | ITMCostTrans.CostValue | Skaitlis (32, 6) | Nē | Nē |
| Valūta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nē | **Jā** |
| Rindas numurs | ITMCostTrans.LineNum | Skaitlis (32, 16) | **Jā** | Nē |
| Saistīto izmaksu veids | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nē | Nē |
| Saistītā fāze | ITMCostTrans.LinkLegId | Nvarchar(20) | Nē | Nē |
| Minimālās izmaksas | ITMCostTrans.MinCostAmount | Skaitlis (32, 6) | Nē | Nē |
| Pārvadāšanas konteiners | ITMCostTrans.TransRecId | Nvarchar(20) | **Jā** | Nē |
| Kategorija | ITMCostTrans.ShipCostCategory (Francija) | Int | Nē | Nē |
| Izmaksu veida kods | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nē | Nē |
| Uzņēmums | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nē | **Jā** |
| Reiss | ITMCostTrans.TransRecId | Nvarchar(20) | **Jā** | Nē |
| Fāze | ITMCostTrans.ShipLegId | Nvarchar(20) | Nē | Nē |
| Krājumu PVN grupa | ITMCostTrans.TaxItemGroup (datu grupa) | Nvarchar(10) | Nē | Nē |

## <a name="folio-costs-itmcosttransfolioentity"></a>Folio izmaksas (ITMCostTransFolioEntity)

Folio izmaksu elements (`ITMCostTransFolioEntity`) izveido izmaksu darbību ierakstus, kas attiecas uz folio līmeni. Importēšanas procesa laikā sistēma izmanto metodes Kategorijas un Ieskaitīšana vērtības, **·** **kas** ir iekļautas entītijā, lai noteiktu, kā izmaksu vērtība tiek izmaksāta pēc katra folio satura.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Norīkojuma metode | ITMCostTrans.ApportionmentMethod | Int | Nē | Nē |
| Izmaksu vērtība | ITMCostTrans.CostValue | Skaitlis (32, 6) | Nē | Nē |
| Valūta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nē | **Jā** |
| Rindas numurs | ITMCostTrans.LineNum | Skaitlis (32, 16) | **Jā** | Nē |
| Saistīto izmaksu veids | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nē | Nē |
| Minimālās izmaksas | ITMCostTrans.MinCostAmount | Skaitlis (32, 6) | Nē | Nē |
| Kategorija | ITMCostTrans.ShipCostCategory (Francija) | Int | Nē | Nē |
| Izmaksu veida kods | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nē | Nē |
| Uzņēmums | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nē | **Jā** |
| Folio | ITMCostTrans.TransRecId | Nvarchar(20) | **Jā** | Nē |
| Krājumu PVN grupa | ITMCostTrans.TaxItemGroup (datu grupa) | Nvarchar(10) | Nē | Nē |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Pirkšanas pasūtījuma izmaksas (ITMCostTransPurchaseEntity)

Pirkšanas pasūtījuma izmaksu elements (`ITMCostTransPurchaseEntity`) izveido izmaksu darbības, kas attiecas uz pirkšanas pasūtījuma virsrakstu. Importēšanas procesa laikā sistēma izmanto metodes Kategorijas un Ieskaitīšana vērtības, **·** **kas** ir iekļautas entītijā, lai noteiktu, kā izmaksu vērtība tiek izmaksāta pēc katra folio satura.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Norīkojuma metode | ITMCostTrans.ApportionmentMethod | Int | Nē | Nē |
| Izmaksu vērtība | ITMCostTrans.CostValue | Skaitlis (32, 6) | Nē | Nē |
| Valūta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nē | **Jā** |
| Rindas numurs | ITMCostTrans.LineNum | Skaitlis (32, 16) | **Jā** | Nē |
| Saistīto izmaksu veids | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nē | Nē |
| Minimālās izmaksas | ITMCostTrans.MinCostAmount | Skaitlis (32, 6) | Nē | Nē |
| Pirkšanas pasūtījums | ITMCostTrans.TransRecId | Nvarchar(20) | **Jā** | Nē |
| Kategorija | ITMCostTrans.ShipCostCategory (Francija) | Int | Nē | Nē |
| Izmaksu veida kods | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nē | Nē |
| Uzņēmums | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nē | **Jā** |
| Krājumu PVN grupa | ITMCostTrans.TaxItemGroup (datu grupa) | Nvarchar(10) | Nē | Nē |

## <a name="item-costs-itmcosttransitementity"></a>Krājumu izmaksas (ITMCostTransItemEntity)

Krājuma izmaksu elements (`ITMCostTransItemEntity`) izveido izmaksu darbības, kas attiecas uz krājuma līmeni. Šis elements ir raksturīgs krājumiem pirkšanas pasūtījuma rindās. Izmaksu vērtība tiek pilnībā pielietota rindai.

Lauki **Korekcijas** summa un **Vērtības** pielāgošana ir specifiski rindas līmeņa izmaksu apgabaliem. Tāpēc to nav datu entītijās citiem izmaksu apgabaliem.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Korekcijas summa | ITMCostTrans.AdjustmentAmount | Skaitlis (32, 6) | Nē | Nē |
| Izmaksu vērtība | ITMCostTrans.CostValue | Skaitlis (32, 6) | Nē | Nē |
| Valūta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nē | **Jā** |
| Rindas numurs | ITMCostTrans.LineNum | Skaitlis (32, 16) | **Jā** | Nē |
| Saistīto izmaksu veids | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nē | Nē |
| Minimālās izmaksas | ITMCostTrans.MinCostAmount | Skaitlis (32, 6) | Nē | Nē |
| Pirkšanas pasūtījums | ITMCostTrans.TransRecId | Nvarchar(20) | **Jā** | Nē |
| Pirkšanas pasūtījuma rindas numurs | ITMCostTrans.TransRecId | Nvarchar(20) | **Jā** | Nē |
| Kategorija | ITMCostTrans.ShipCostCategory (Francija) | Int | Nē | Nē |
| Izmaksu veida kods | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nē | Nē |
| Uzņēmums | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nē | **Jā** |
| Krājumu PVN grupa | ITMCostTrans.TaxItemGroup (datu grupa) | Nvarchar(10) | Nē | Nē |
| Vērtības korekcija | ITMCostTrans.ValueAdjustmentMethod | Int | Nē | Nē |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Pārsūtīšanas rindas izmaksas (ITMCostTransTransferLineEntity)

Pārsūtīšanas rindas izmaksu elements (`ITMCostTransTransferLineEntity`) izveido izmaksu darbības, kas attiecas uz pārsūtīšanas pasūtījuma rindas līmeni. Šo izmaksu vērtība pilnībā tiek piemērota pārsūtīšanas pasūtījuma rindai.

Lauki **Korekcijas** summa un **Vērtības** pielāgošana ir specifiski rindas līmeņa izmaksu apgabaliem. Tāpēc to nav datu entītijās citiem izmaksu apgabaliem.

| Nosaukums/vārds, uzvārds | Kartēšana | Datu veids | Taustiņš | Obligāts |
|---|---|---|---|---|
| Korekcijas summa | ITMCostTrans.AdjustmentAmount | Skaitlis (32, 6) | Nē | Nē |
| Izmaksu vērtība | ITMCostTrans.CostValue | Skaitlis (32, 6) | Nē | Nē |
| Valūta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nē | **Jā** |
| Rindas numurs | ITMCostTrans.LineNum | Skaitlis (32, 16) | **Jā** | Nē |
| Saistīto izmaksu veids | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nē | Nē |
| Minimālās izmaksas | ITMCostTrans.MinCostAmount | Skaitlis (32, 6) | Nē | Nē |
| Kategorija | ITMCostTrans.ShipCostCategory (Francija) | Int | Nē | Nē |
| Izmaksu veida kods | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nē | Nē |
| Uzņēmums | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nē | **Jā** |
| Pārsūtīšanas pasūtījums | ITMCostTrans.TransRecId | Nvarchar(20) | **Jā** | Nē |
| Pārsūtīšanas pasūtījuma rindas numurs | ITMCostTrans.TransRecId | Nvarchar(20) | **Jā** | Nē |
| Krājumu PVN grupa | ITMCostTrans.TaxItemGroup (datu grupa) | Nvarchar(10) | Nē | Nē |
| Vērtības korekcija | ITMCostTrans.ValueAdjustmentMethod | Int | Nē | Nē |

### <a name="transaction-table"></a>Darījumu tabula

Izmaksu darbības ieraksts tiek saistīts ar izmaksu apgabalu, izmantojot darbības tabulas numura piešķiri (`TransTableId`). Kad nepieciešami specifiski tabulas identifikācijas numuri, entītijas tiek sadalītas, pamatojoties uz šīm vērtībām, lai entītija eksistē katram izmaksu apgabalam.

Darbības tabulas (`TransTableId`) vērtība ir netieši izmaksu darbības elementa atlasē.

### <a name="calculated-fields"></a>Aprēķinātie lauki

Tālāk minētie lauki nav pieejami ievietošanai vai atjaunināšanai, izmantojot izmaksu darbības elementu, jo šie lauki tiek iestatīti tikai tad, ja attiecībā uz reisa ierakstu tiek veiktas specifiskas darbības:

- **Novērtētās** izmaksas – šis lauks ir iestatīts, kad ir saņemts rēķins par reisu (pirkšanas pasūtījumu) vai pārskaitījumu.
- **Prognozēto izmaksu valūta** – šis lauks ir iestatīts, kad ir saņemts rēķins par reisu (pirkšanas pasūtījumu) vai pārskaitījumu.
- **Faktiskās** izmaksas – šis lauks tiek iestatīts, kad kreditora rēķins ir iegrāmatots. Tā ir saistīta ar izmaksām.

### <a name="find-auto-costs"></a>Atrast automātiskās izmaksas

Poga **Atrast automātiskās izmaksas**, kas ir pieejama katram izmaksu apgabalam (reiss, nosūtīšanas konteiners utt.) nodrošina veidu, kā atjaunināt izmaksu darbības šai izmaksu apgabalam no informācijas konfigurācijas tabulās. Atlasot pogu izmaksu apgabalam, sistēma notīra esošās izmaksas šai izmaksu apgabalam un izveido jaunus ierakstus, pamatojoties uz pašreizējo automātisko izmaksu iestatījumu tabulu konfigurāciju.

Izmaksu darbību ieraksti, kas izveidoti, izmantojot datu elementu, tiek atzīmēti kā importēti. Šie ieraksti netiek dzēsti, atlasot **Atrast** automātiskās izmaksas, jo tie netiks atkārtoti izveidoti no automātiskās izmaksu iestatījumu tabulām. Tomēr izmaksu darbību ierakstu, kas ir atzīmēts kā importēts, joprojām var izdzēst.

### <a name="linked-fields"></a>Saistītie lauki

Katra izmaksu darbība var tikt saistīta ar citu ierakstu tajā pašā izmaksu apgabalā. Šī saistība tiek izveidota, izmantojot **saistīto izmaksu tipa** lauku. Tas ļauj izmaksu vērtību aprēķināt kā citu izmaksu procentus.

Saistīto **izmaksu tipa lauku** var pārbaudīt tikai tad, ja ieraksts, uz kuru ir atsauce, ir apstrādāts vispirms vai ja tas jau ir tabulā. Tā pati prasība attiecas uz lauku **Saistītajās** kājās, kas tiek izmantotas izmaksām tikai pārvadāšanas konteinera izmaksu zonā.
