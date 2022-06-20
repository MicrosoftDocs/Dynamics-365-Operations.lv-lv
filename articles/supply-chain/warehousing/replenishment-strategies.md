---
title: Papildināšanas stratēģijas
description: Šajā rakstā ir sniegta informācija par papildināšanas stratēģiju un skaidrots, kā var izmantot lauku Papildināšanas stratēģija kopuma pieprasījuma papildināšanas veidnes rindās, lai atlasītu veidu, kā tiek veikta papildināšana.
author: Mirzaab
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3b4d691bbcf88cc73d10e3bb401710508ec641e1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893154"
---
# <a name="replenishment-strategies"></a>Papildināšanas stratēģijas

[!include [banner](../includes/banner.md)]

Veidnes, kas norādītas lapā **Papildināšanas veidnes**, ietver kopuma pieprasījuma papildināšanas veidnes rindas, kas ļauj izvēlēties, kā tiek veikta papildināšana. Katrai rindai tagad ir ietverts **Papildināšanas stratēģijas** lauks.

*Kopuma pieprasījuma daudzuma* stratēģija ir noklusējuma stratēģija. Tā ir papildināšanas stratēģija, kas tika izmantota pirms **Papildināšanas stratēģijas** lauka ieviešanas. Tā izmanto papildināšanas novietojuma direktīvas, lai atrastu vietas, ko var papildināt. Pēc tam tā papildina šīs vietas, līdz pieprasījums tiek segts.

*Maksimālā vietas noslodzes* stratēģija ievieš jaunu funkcionalitāti. Līdzīgi kā *Kopuma pieprasījuma daudzuma* stratēģija, šī stratēģija izmanto papildināšanas novietojuma direktīvas, lai atrastu atrašanās vietas, ko var papildināt, un tad tās papildina, līdz pieprasījums tiek segts. Tas atšķiras no *Kopuma pieprasījuma daudzuma* stratēģijas ar to, ka visas atjaunotās atrašanās vietas tiek papildinātas ar to maksimālo noslodzi, kā noteikts novietojuma krājumu ierobežojumos. *Maksimālā vietas noslodzes* stratēģija mēģina izveidot darbu, lai piesaistītu pieprasīto daudzumu, plus vēl papildu daudzumu, lai aizpildītu papildināšanas vietas. Tomēr dažos gadījumos šis mēģinājums var neizdoties. Piemēram, lielapjoma novietojumiem var nebūt pietiekami daudz krājumu, lai nosegtu papildu daudzumu. Šādos gadījumos sistēma konstatē kļūmi un mēģina atkopties.

Aktīvākā sezona ir viens piemērs situācijai, kur *Maksimālā vietas noslodzes* stratēģija ir vēlamāka nekā *Kopuma pieprasījuma daudzuma* stratēģija. Aktīvākās sezonas laikā daži krājumi var tikt pārdoti lielā apjomā. Tāpēc, iespējams, vēlēsities aktīvi papildināt atbilstošās izdošanas vietas, cik vien iespējams, lai samazinātu papildināšanai izveidoto darba ID skaitu.

> [!IMPORTANT]
> Lai pilnībā izmantotu *Maksimālo vietas noslodzes* stratēģiju, pārdefinējiet krājumu ierobežojumus attiecīgajām atrašanās vietām. Pretējā gadījumā šī stratēģija darbojas tieši tāpat kā *Kopuma pieprasījuma daudzuma* stratēģija.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>Ieslēgt Papildinājumu uz maksimumu, pamatojoties uz krājumu ierobežojumu līdzekli

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams. Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Papildinājums uz maksimumu, pamatojoties uz krājumu ierobežojumiem*

## <a name="set-up-replenishment-strategies"></a>Papildināšanas stratēģiju uzstādīšana

Lai piekļūtu veidnēm, dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes**. Sadaļā **Pārskats** atlasiet vai izveidojiet kopuma pieprasījuma papildināšanas veidni, kur **Papildināšanas tipa** lauks ir iestatīts kā *Kopuma pieprasījums*. Pēc tam iestatiet papildināšanas veidnes rindas sadaļā **Papildināšanas veidnes detaļas**. Katrai rindai laukā **Papildināšanas stratēģija** atlasiet papildināšanas stratēģiju, ko vēlaties izmantot.

![Papildināšanas veidnes lapa.](media/ReplenTempWaveDmdMaxLocCap.png "Papildināšanas veidnes lapa")

Ja **Papildināšanas stratēģijas** kolonna neparādās režģī sadaļā **Papildināšanas veidnes detaļas**, pārliecinieties, ka līdzeklis ir ieslēgts un atlasītajai papildināšanas veidnei ir *Kopuma pieprasījuma* papildināšanas veids.

> [!NOTE]
> *Kopuma pieprasījuma daudzuma* stratēģija ir noklusējuma stratēģija. Tāpēc ir tikai jāatjaunina papildināšanas veidnes rindas, kurās vēlaties izmantot *Maksimālo novietojuma noslodzes* stratēģiju.

## <a name="example-scenarios"></a>Piemēra situācijas

### <a name="example-1"></a>1. piemērs

Šajā piemērā ir tikai viena papildināšanas veidne, kurai ir tikai viena papildināšanas veidnes rinda.

Tiek izveidots pārdošanas pasūtījums 130 vienībām (gab.) krājumam A0001. Pirms pasūtījuma nodošanas noliktavai noliktava ir iestatīta šādā veidā:

- Ir tikai viena lielapjoma atrašanās vieta, un tai ir 500 datori ar pieejamiem rīcībā esošiem krājumiem.
- Ir trīs izdošanas vietas, un katrai no tām ir 100 personālo datoru krājumu ierobežojums. (Atcerieties, ka krājumu limiti ir nepieciešami *Maksimālās novietojuma noslodzes* stratēģijai.)
- Papildināšanas izvietojuma atrašanās vietas ir vienādas ar pārdošanas izvietošanas atrašanās vietām.
- Papildināšanas vienība ir lodziņš (1 lodziņš = 20 gab.).

Pasūtījuma laikā pārdošanas saņemšanas atrašanās vietās ir pieejami sekojošie krājumi:

- **Izdošana-001:** 20 gab. (1 kastīte)
- **Izdošana-002:** 0 gab.
- **Izdošana-003:** 0 gab.

Sākotnēji papildināšanas stratēģija ir iestatīta uz *Kopuma pieprasījuma daudzumu*.

Kad pārdošanas pasūtījums tiek nodots noliktavai un kopuma apstrāde tiek palaista kopumam, tiek parādīts šāds papildināšanas darbs:

- **Papildināšanas darbs 1:** Izlaidiet 4 kastes no lielapjoma atrašanās vietas un ievietojiet tās novietojumā izdošana-001.
- **Papildināšanas darbs 2:** Izlaidiet 2 kastes no lielapjoma atrašanās vietas un ievietojiet tās novietojumā izdošana-002.

Tiek ierakstīti divi papildināšanas darba ID, jo ir jāpapildina divas atrašanās vietas, un papildu ievietošana netiek atbalstīta.

Iestatot papildināšanas stratēģiju uz *Maksimālo novietojuma noslodzi*, tiek parādīts šāds papildināšanas darbs:

- **Papildināšanas darbs 1:** Izlaidiet 4 kastes no lielapjoma atrašanās vietas un ievietojiet tās novietojumā izdošana-001.
- **Papildināšanas darbs 2:** Izlaidiet 5 kastes no lielapjoma atrašanās vietas un ievietojiet tās novietojumā izdošana-002.

[![Piemērs 1.](media/ReplenTemp_example_1.png "1. piemērs")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>2. piemērs

Šajā piemērā parādīts, kas notiek, kad lielapjoma novietojumam nav pietiekami daudz krājumu, lai nosegtu papildu daudzumu. Tas izmanto tādu pašu scenāriju kā 1. piemērs, bet lielapjoma atrašanās vietai ir 160 gabali (8 kastes).

*Kopuma pieprasījuma daudzuma* stratēģija izveido tādu pašu darbu, kāds tas bija 1. piemērā.

Tomēr, tā kā *Maksimālā novietojuma noslodzes* stratēģija mēģina izveidot darba ID, kāds tas bija 1. piemērā, tas var neizdoties. Šajā brīdī sistēma mēģina atkopties.

Atkarībā no opcijas **Atļaut sadalīt** iestatījuma novietojuma direktīvās papildināšanas izdošanai ir iespējami divi rezultāti:

- Ja opcija **Atļaut sadalīt** ir iestatīta uz *Jā*, tiek izveidots šāds papildināšanas darbs:

    - **Papildināšanas darbs 1:** Izlaidiet 4 kastes no lielapjoma atrašanās vietas un ievietojiet tās novietojumā izdošana-001.
    - **Papildināšanas darbs 2:** Izlaidiet 4 kastes no lielapjoma atrašanās vietas un ievietojiet tās novietojumā izdošana-002.

- Ja opcija **Atļaut sadalīt** ir iestatīta uz *Nē*, tiek izveidots šāds papildināšanas darbs:

    - **Papildināšanas darbs 1:** Izlaidiet 4 kastes no lielapjoma atrašanās vietas un ievietojiet tās novietojumā izdošana-001.
    - **Papildināšanas darbs 2:** Izlaidiet 2 kastes no lielapjoma atrašanās vietas un ievietojiet tās novietojumā izdošana-002.

Rezultāti atšķiras pieejamās informācijas dēļ darba izveides laikā. Ja opcija **Atļaut sadalīt** ir iestatīta uz *Jā*, novietojuma direktīvās par papildināšanas izdošanu, jūs zināt, ka jums ir izdevies atrast 160 gab. Tādējādi varat izveidot darbu šim daudzumam. Tomēr, ja opcija **Atļaut sadalīt** ir iestatīta uz *Nē*, jūs nezināt par 160 gab. esamību. Tā kā papildu daudzums, kuru jūs nolēmāt papildināt, bija 3 kastes, jūs nometīsiet šo papildu daudzumu un vēlreiz mēģināsiet veikt sākotnējo daudzumu.

[![Piemērs 2.](media/ReplenTemp_example_2.png "2. piemērs")](media/ReplenTemp_example_2_large.png)

Tāpēc, lai iegūtu maksimālo daudzumu uz papildinātajām atrašanās vietām, ir jāiestata opcija **Atļaut sadalīt** uz *Jā* novietojuma direktīvās papildināšanas izdošanai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]