---
title: PVN aprēķins vispārējā žurnālā
description: Šajā rakstā skaidrots, kā PVN tiek aprēķināti dažādiem kontu tipiem (kreditoram, debitoram, Virsgrāmatai un projektam) virsgrāmatas žurnāla rindās.
author: EricWangChen
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: a73e145dd26e930c860e9ea31d7dab4f1593c2a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845292"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>PVN aprēķins vispārējā žurnālā
[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā PVN tiek aprēķināti dažādiem kontu tipiem (kreditoram, debitoram, Virsgrāmatai un projektam) virsgrāmatas žurnāla rindās.

Procesu var sadalīt trīs daļās:

- Nosakiet PVN virzienu.

- Nosakiet PVN summu, kas tiks saglabāta pagaidu PVN tabulā.

- Nosakiet PVN summu un kontu dokumentā.

## <a name="determine-the-sales-tax-direction"></a>Nosakiet PVN virzienu.

PVN virziena noteikšanas veids ir atkarīgs no konta tipa dokumentā. PVN virzienu nosaka konta tipa un PVN koda kombinācija. Tālāk norādītajās sadaļās ir sīkāk aprakstītas iespējas. 

### <a name="account-type-is-project"></a>Konta tips ir projekts.

Ja dokumentam ir žurnāla rinda, kur konta tips ir **Projekts**, visas žurnāla rindas dokumentā lieto vienu un to pašu nodokļu virzienu. Tālāk esošajā attēlā ir parādīts kārtula. Šie punkti parāda iespējamos nodokļu norādījumus projektu kontos.

• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.

• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.

• Ja PVN kods ir iekšējais nodoklis, tad PVN virziens ir Maksājamais PVN.

• Ja PVN kods ir apgrieztais nodoklis, tad PVN virziens ir Maksājamais PVN.

Pretējā gadījumā PVN virziens ir Saņemamais PVN.

Sekojošā diagramma attēlo šo kārtulu grafiski.

![Nodokļu virziena iespējas projektu kontiem.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Konta tips ir Kreditors.

Ja dokumentam ir žurnāla rinda, kur konta tips ir **Kreditors**, visas žurnāla rindas dokumentā lieto vienu un to pašu nodokļu virzienu. Šie punkti parāda iespējamos nodokļu norādījumus kreditoru kontos. 

• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.

• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.

• Ja PVN kods ir iekšējais nodoklis, tad PVN virziens ir Maksājamais PVN.

• Ja PVN kods ir apgrieztais nodoklis, tad PVN virziens ir Maksājamais PVN.

Pretējā gadījumā PVN virziens ir Saņemamais PVN.

Sekojošā diagramma attēlo šo kārtulu grafiski.

![Nodokļu virziena iespējas kreditoru kontiem.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Konta tips ir Klients.

Ja dokumentam ir žurnāla rinda, kur konta tips ir **Debitors**, visas žurnāla rindas dokumentā piemēro vienādu PVN virzienu. 

Ja PVN kods ir neapliekams nodoklis, PVN virziens ir Pārdošana bez nodokļiem. Pretējā gadījumā PVN virziens ir Maksājamais PVN.

### <a name="account-type-is-ledger"></a>Konta veids ir Virsgrāmata.

Sekojošajā attēlā ir parādīts noteikums, kas tiek lietots, kad dokumentam ir tikai tās žurnāla rindas, kurās konta tips ir **Virsgrāmata**. Šie punkti parāda iespējamos nodokļu norādījumus virsgrāmatu kontiem.

• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.

• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.

Pretējā gadījumā, ja žurnāla summa ir debets (pozitīvs), PVN virziens ir Saņemamais PVN; ja žurnāla summa ir kredīts (negatīvs), PVN virziens ir Maksājamais PVN.

Sekojošā diagramma attēlo šo kārtulu grafiski.

![Nodokļu virziena iespējas virsgrāmatu kontiem.](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Labojiet PVN virzienu.

PVN virzienu var ignorēt, ja dokumentā ir tikai rindas, kurās konta tips ir **Virsgrāmata**.

Dodieties uz **Virsgrāmata \> Kontu plāns \> Konti \> Galvenie konti** un atlasiet **Juridisko personu labojumi** kopsavilkuma cilnē.

## <a name="determine-the-sales-tax-amount"></a>Nosakiet PVN summu

Šajā sadaļā ir aprakstīts, kā tiek aprēķināta PVN summa.

![PVN darījumu lapa.](media/sales-tax-amount-sign.jpg)

Sekojošajā tabulā ir parādīts vispārīgais noteikums, lai noteiktu PVN virzienu un summas apjomu pagaidu PVN tabulā.

| Žurnāla līniju apjoms | PVN virziens  | PVN summas apjoms |
|---------------------|----------------------|-----------------------|
| Pozitīvs            | Saņemamais PVN | Pozitīvs              |
| Pozitīvs            | Maksājamais PVN    | Negatīvs              |
| Negatīvs            | Saņemamais PVN | Negatīvs              |
| Negatīvs            | Maksājamais PVN    | Pozitīvs              |

Pastāv īpašs noteikums dokumentiem, kuriem ir tikai **Projekta** vai **Virsgrāmatas** rindas gadījumos, kad **Virsgrāmatas** rindā ir atlasīta PVN grupa vai preces PVN grupa. Šo noteikumu kontrolē līdzeklis **Iespējot neatkarīgu PVN aprēķināšanas līdzekli vispārējiem žurnāliem**. Kad šī funkcija ir izslēgta, **Virsgrāmatas** rindas nodokļa summa izmanto **Projekta** rindas debeta/kredīta virzienu. Kad šī funkcija ir ieslēgta, **Virsgrāmatas** rindas nodokļa summa izmanto savu projekta rindas debeta/kredīta virzienu. Sekojošajās Tabulās ir parādīts katra scenārija noteikums. 

**Noteikums, kad līdzeklis ir ieslēgts.**

| Projekta žurnāla rindas apjoms | PVN virziens  | PVN summas apjoms |
|--------------------------------|----------------------|-----------------------|
| Pozitīvs                       | Saņemamais PVN | Pozitīvs              |
| Negatīvs                       | Saņemamais PVN | Negatīvs              |

**Noteikums, kad līdzeklis ir izslēgts.**

| Virsgrāmatas žurnāla rindas apjoms  | PVN virziens  | PVN summas apjoms |
|--------------------------------|----------------------|-----------------------|
| Pozitīvs                       | Saņemamais PVN | Pozitīvs              |
| Negatīvs                       | Saņemamais PVN | Negatīvs              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>Nosakiet PVN summu un kontu dokumentā.

Grāmatojot PVN, galvenais konts tiek iegūts no Virsgrāmatas grāmatošanas grupas profila. Kad tiek saņemti PVN ieņēmumi, sistēma izmanto profilā norādīto PVN saņemamo kontu. Izejamajiem PVN maksājumiem sistēma izmanto profilā norādīto maksājamo PVN kontu.

Tālāk esošajā tabulā parādīts galvenais noteikums.

| PVN virziens  | PVN summas apjoms | PVN konts      | Dokumenta summa |
|----------------------|-----------------------|------------------------|-------------------|
| Saņemamais PVN | Pozitīvs              | Saņemamā nodokļa konts | Pozitīvs (debits)  |
| Saņemamais PVN | Negatīvs              | Saņemamā nodokļa konts | Negatīvs (kredīts)  |
| Maksājamais PVN    | Pozitīvs              | Kreditoru konts    | Negatīvs (kredīts)  |
| Maksājamais PVN    | Negatīvs              | Kreditoru konts    | Pozitīvs (debits)  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
