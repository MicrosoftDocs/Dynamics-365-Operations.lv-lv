---
title: Commerce tērzēšanas moduļa proaktīvās tērzētavas parametri
description: Šajā rakstā ir aprakstīti Commerce tērzēšanas moduļu proaktīvās tērzētavas parametri sadaļā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690959"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Commerce tērzēšanas moduļa proaktīvās tērzētavas parametri

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīti commerce Chat ar Debitoru pakalpojumu un Commerce Chat moduļu proaktīvās tērzēšanas Power Virtual Agents parametri Microsoft Dynamics 365 Commerce.

## <a name="proactive-chat-properties"></a>Proaktīvie tērzētavas rekvizīti

Proaktīvie tērzētavas rekvizīti atrodas Rekvizītu rūtī commerce Chat ar Nechannel, kas paredzēts Customer Service un Commerce Chat Power Virtual Agents moduļiem Commerce Site Builder.

> [!NOTE]
> Pēc noklusējuma visi šeit uzskaitītie proaktīvās tērzētavas rekvizīti ir tukši. Mēs iesakām jums uzzināt vairāk par šiem rekvizītiem un iestatīt tos tikai pēc vajadzības. Šī pieeja palīdzēs samazināt kļūdainu proaktīvo tērzēšanu parādīšanu.

### <a name="proactive-chat"></a>Apsteidzēt tērzēšanu

| Draudzīgais nosaukums | Apraksts | Noklusējuma vērtība |
|---------------|-------------|---------------|
| Aktivizēts | Proaktīvi iesaistīti debitori, pamatojoties uz dažādiem trigeriem. | Atspējota |
| Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. | Tukšs |

### <a name="wait-time-proactive-chat"></a>Gaidīšanas laiks (proaktīvā sarakste)

| Draudzīgais nosaukums | Apraksts |
|---------------|-------------|
| Gaidīšanas laiks (sek.) | Laiks (sekundēs), ko vietnes lietotāji tērē vietnes lapai, pirms tiek izraisīta proaktīvā sarakste. |
| Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. |

### <a name="number-of-page-visits-proactive-chat"></a>Lapas apmeklējumu skaits (proaktīvā tērzēšana)

| Draudzīgais nosaukums | Apraksts |
|---------------|-------------|
| Lapas apmeklējumu skaits | Lapu apmeklējumu skaits pirms proaktīvās tērzēšanas aktivizēšanas. Vietnes lietotājiem vispirms ir jāakceptē uzvedne sīkfaila atļaujas lietotājiem. |
| Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. |

### <a name="specific-pages-proactive-chat"></a>Noteiktas lapas (proaktīvā tērzēta)

| Draudzīgais nosaukums | Apraksts |
|---------------|-------------|
| Lapas | Lapu saraksts, kas aktivizēs proaktīvo tērzēšanu, kad tās būs apmeklētas. |
| Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. |

### <a name="from-specific-pages-proactive-chat"></a>No noteiktām lapām (proaktīvā tērzēšana)

| Draudzīgais nosaukums | Apraksts |
|---------------|-------------|
| Lapas | Lapu saraksts, kas aktivizēs proaktīvo tērzēšanu, kad lietotāji no tām naviģēs. |
| Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. |

### <a name="specific-countryregion-proactive-chat"></a>Noteikta valsts/reģions (proaktīvā tērzēšana)

| Draudzīgais nosaukums | Apraksts |
|---------------|-------------|
| Valsts kods | Lietotāji, kuri apmeklē norādītās valstis vai reģionus, aktivizēs proaktīvo tērzēšanu. Valsts/reģiona kodiem jābūt diviem lielajiem burtiem (piemēram, **ASV**). |
| Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. |

### <a name="date-range-proactive-chat"></a>Datumu diapazons (proaktīvā tērzēšana)

| Draudzīgais nosaukums | Apraksts |
|---------------|-------------|
| Sākuma datums (dd/mm/gggg) | Datums, kurā vai pēc kura tiks izraisīta proaktīvā sarakste. |
| Beigu datums (dd/mm/GGGG) | Datums, kurā vai pirms kura tiks izraisīta proaktīvā sarakste. |
| Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. |

### <a name="total-amount-in-cart-proactive-chat"></a>Kopsumma grozā (proaktīvā tērzēšana)

| Draudzīgais nosaukums | Apraksts |
|---------------|-------------|
| Minimālā | Minimālā naudas summa (ietveroša) iepirkumu grozā, kas aktivizēs apsteidzošo tērzēšanu, kad lietotāji apmeklē iepirkumu groza lapu. |
| Maksimālā | Maksimālā naudas summa (ietveroša) iepirkumu grozā, kas aktivizēs apsteidzošo tērzēšanu, kad lietotāji apmeklē iepirkumu groza lapu. |
|Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Kopējais krājumu skaits grozā (proaktīvā tērzēšana)

| Draudzīgais nosaukums | Apraksts |
|---------------|-------------|
| Minimālā | Minimālais krājumu skaits (ietveroša) iepirkumu grozā, kas aktivizēs proaktīvo tērzēšanu, kad lietotāji apmeklēs groza lapu. |
| Maksimālā | Maksimālais krājumu skaits (ietveroša) iepirkumu grozā, kas aktivizēs proaktīvo tērzēšanu, kad lietotāji apmeklēs iepirkumu groza lapu. |
| Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. |

### <a name="specific-products-in-cart-proactive-chat"></a>Noteiktas preces grozā (proaktīvā tērzēšana)

| Draudzīgais nosaukums | Apraksts |
|---------------|-------------|
| Preces ID/NV | To preču IDENTIFIKĀCIJAS/noliktavas vienību (NV) numuru saraksts, kas izraisa proaktīvo tērzēšanu, kad lietotāji apmeklē grozu lapu. |
| Tērzēta apsveikums | Apsveikuma ziņojums, kas tiek izmantots, kad ir izraisīta proaktīvā sarakste. |

## <a name="additional-resources"></a>Papildu resursi

[Commerce tērzēšanas līdzekļu pārskats](commerce-chat-overview.md)

[Commerce Tērzēšana ar Debitorachannel klientu pakalpojuma modulim](commerce-chat-module.md)

[Commerce Tērzēšana ar moduli Power Virtual Agents](chat-module-pva.md)
