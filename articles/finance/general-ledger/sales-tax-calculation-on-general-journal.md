---
title: PVN aprēķins vispārējā žurnālā.
description: Šajā tēmā izskaidrots, kā PVN tiek aprēķināts dažādiem kontu tipiem (kreditora, klienta, virsgrāmatas un projekta) vispārējā žurnālā.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 25eb8dd6965f659f0febe53a6340cb1381c5664f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204910"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>PVN aprēķins vispārējā žurnālā.
[!include [banner](../includes/banner.md)]

Šajā tēmā izskaidrots, kā PVN tiek aprēķināts dažādiem kontu tipiem (kreditora, klienta, virsgrāmatas un projekta) vispārējā žurnālā.

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

Ja dokumentam ir žurnāla rinda, kur konta tips ir **Klients**, visas žurnāla rindas dokumentā lieto vienu un to pašu nodokļu virzienu. Šie punkti parāda iespējamos nodokļu norādījumus klientu kontiem.

• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.

• Ja PVN kods ir iekšējais nodoklis, tad PVN virziens ir Saņemamais PVN.

• Ja PVN kods ir apgrieztais nodoklis, tad PVN virziens ir Saņemamais PVN.

Pretējā gadījumā PVN virziens ir Maksājamais PVN.

Sekojošā diagramma attēlo šo kārtulu grafiski.

![Nodokļu virziena iespējas klientu kontiem.](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a>Konta veids ir Virsgrāmata.

Sekojošajā attēlā ir parādīts noteikums, kas tiek lietots, kad dokumentam ir tikai tās žurnāla rindas, kurās konta tips ir **Virsgrāmata**. Šie punkti parāda iespējamos nodokļu norādījumus virsgrāmatu kontiem.

• Ja PVN kods ir importa nodoklis, tad arī PVN virziens ir importa nodoklis.

• Ja PVN kods ir ar nodokli neapliekams, tad arī PVN virziens ir nodokli neapliekams pirkums.

Pretējā gadījumā, ja žurnāla summa ir debets (pozitīvs), PVN virziens ir Saņemamais PVN; ja žurnāla summa ir kredīts (negatīvs), PVN virziens ir Maksājamais PVN.

Sekojošā diagramma attēlo šo kārtulu grafiski.

![Nodokļu virziena iespējas virsgrāmatu kontiem.](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Labojiet PVN virzienu.

PVN virzienu var ignorēt, ja dokumentā ir tikai rindas, kurās konta tips ir **Virsgrāmata**.

Dodieties uz **Virsgrāmata\>Kontu plāns\>Konti\>Galvenie konti** un atlasiet **Juridisko personu labojumi** kopsavilkuma cilnē.

## <a name="determine-the-sales-tax-amount"></a>Nosakiet PVN summu

Šajā sadaļā ir aprakstīts, kā tiek aprēķināta PVN summa.

![PVN darījumu lapa](media/sales-tax-amount-sign.jpg)

Sekojošajā tabulā ir parādīts vispārīgais noteikums, lai noteiktu PVN summas apjomu pagaidu PVN tabulā.

| Žurnāla līniju apjoms | PVN virziens  | PVN summas apjoms |
|---------------------|----------------------|-----------------------|
| Pozitīvs            | Saņemamais PVN | Pozitīvs              |
| Pozitīvs            | Maksājamais PVN    | Negatīvs              |
| Negatīvs            | Saņemamais PVN | Negatīvs              |
| Negatīvs            | Maksājamais PVN    | Pozitīvs              |

Pastāv īpašs noteikums dokumentiem, kuriem ir tikai **Projekta** vai **Virsgrāmatas** rindas gadījumos, kad **Virsgrāmatas** rindā ir atlasīta PVN grupa vai preces PVN grupa. Šo noteikumu kontrolē, iespējojot neatkarīgu PVN aprēķināšanas funkciju vispārējiem žurnāliem. Kad šī funkcija ir izslēgta, **Virsgrāmatas** rindas nodokļa summa izmanto **Projekta** rindas debeta/kredīta virzienu. Kad šī funkcija ir ieslēgta, **Virsgrāmatas** rindas nodokļa summa izmanto savu projekta rindas debeta/kredīta virzienu. Sekojošajās Tabulās ir parādīts katra scenārija noteikums. 

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