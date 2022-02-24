---
title: Automātisko maksu iespējošana un konfigurēšana katram kanālam
description: Šajā tēmā skaidrots, kā iespējot un konfigurēt automātisko izmaksu pa kanāliem programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 1be07c754e563298d82f6ca54f09ae3aa9118602
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414028"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Automātisko maksu iespējošana un konfigurēšana katram kanālam

Šajā tēmā skaidrots, kā iespējot un konfigurēt automātiskās izmaksas pa kanāliem programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Jūs varat izmantot scenārijus, kuros maksas par pārstrādi vai citām maksām ir jāpiemēro preču grupai, kas tiek pārdota visos vai dažos veikalos noteiktā štatā (piemēram, Kalifornijā). **Iespējot filtra automātiskās izmaksas pēc kanāla** līdzeklis programmā Commerce ļauj norādīt automātiskās maksas pēc kanāla (piemēram, fiziskas pārdošanas kanāls). Šis līdzeklis ir pieejams programmā Dynamics 365 Commerce 10.0.10 un jaunākās versijās.

Lai iespējotu un konfigurētu automātiskās izmaksas pēc kanāla, ir jāveic šādi uzdevumi:

- Ieslēdziet līdzekli **Iespējot filtra automātiskās izmaksas pēc kanāla**.
- Konfigurējiet organizācijas hierarhijas nolūku.
- Definēt automātiskās izmaksas pēc kanāla.

> [!NOTE]
> **Iespējot filtra automātiskās izmaksas pēc kanāla** līdzeklis darbojas tikai tad, ja ir ieslēgts arī papildu automātiskās izmaksas līdzeklis. Informāciju par to, kā ieslēgt papildu automātiskās izmaksas līdzekli, skatiet [Omni-Channel Advanced automātiskā izmaksas](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Ieslēdziet līdzekli Iespējot filtra automātiskās izmaksas pēc kanāla

Lai aktivizētu automātiskās izmaksas pēc kanāla programmā Commerce, veiciet šādas darbības.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.
1. Cilnē **Neiespējots**, kas atrodas sarakstā **Līdzekļa nosaukums**, atrodiet un atlasiet opciju **Iespējot filtra automātiskas izmaksas pēc kanāla**.
1. Labajā apakšējā stūrī atlasiet opciju **Iespējot tagad**. Pēc tam, kad līdzeklis ir ieslēgts, tas tiks parādīts cilnes **Visas** sarakstā.
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
1. Kreisajā rūtī atrodiet un atlasiet **1110** (**Globālā konfigurācija**) darbu.
1. Darbības rūtī atlasiet **Palaist tagad**, lai ieviestu konfigurācijas izmaiņas.

> [!WARNING]
> Izslēdzot līdzekli **Iespējot filtra automātiskās izmaksas pēc kanāla** pēc tam, kad esat to jau izmantojis, **Mazumtirdzniecības kanālu relāciju** lauks sadaļā **Automātiskās izmaksas** vairs netiks rādīts un jūs pazaudēsiet visas esošās konfigurācijas. Ja **Mazumtirdzniecības kanāla relāciju** konfigurāciju noņemšana izraisīs automātisku izmaksu noteikumu dublēšanos, mēģinājums izslēgt līdzekli būs neveiksmīgs. Pirms līdzekļa izslēgšanas noteikti pārskatiet visus automātiskās izmaksas nosacījumus un veiciet nepieciešamās izmaiņas.

## <a name="configure-the-organization-hierarchy-purpose"></a>Konfigurējiet organizācijas hierarhijas nolūku

Tiek izveidots jauns organizācijas hierarhijas nolūks ar nosaukumu **Mazumtirdzniecības automātiskā izmaksa**, kas ir izveidota, lai pārvaldītu automātisko izmaksu hierarhiju pēc kanāla.

Lai piešķirtu noklusējuma hierarhiju uzņēmuma hierarhijas mērķim programmā Commerce, veiciet šīs darbības.
        
1. Dodieties uz **Organizācijas administrēšana \> Organizācijas \> Organizācijas hierarhijas nolūki**.
1. Kreisajā rūtī atlasiet **Mazumtirdzniecības automātiskā izmaksa**.
1. Sadaļā **Piešķirtās hierarhijas** atlasiet **Pievienot**.
1. Dialoglodziņā **Organizācijas hierarhijas** atlasiet organizācijas hierarhiju (piemēram, **Mazumtirdzniecības veikali pēc reģiona**) un pēc tam atlasiet **Labi**.
1. Sadaļā **Piešķirtās hierarhijas** atlasiet **Iestatīt kā noklusējumu**.
1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
1. Kreisajā rūtī atrodiet un atlasiet **1040** (**Preces**) darbu.
1. Darbību rūtī atlasiet **Palaist tagad**.
1. Atkārtojiet iepriekšējos divus soļus, lai palaistu **1070** (**Kanāla konfigurācija**) un **1110** (**Globālā konfigurācija**) darbus.

![Mazumtirdzniecības automātiskās izmaksas organizācijas hierarhijas nolūka konfigurācija](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Definēt automātiskās izmaksas pēc kanāla

Pēc tam, kad esat ieslēdzis līdzekli **Iespējot filtra automātiskās izmaksas pēc kanāla** un konfigurējis **Mazumtirdzniecības automātiskās izmaksas** organizācijas hierarhijas mērķi, automātiskās izmaksas pēc kanāla var definēt vai nu pasūtījuma virsraksta līmenī, vai pasūtījuma rindas līmenī.

Lai definētu automātiskās izmaksas pēc kanāla programmā Commerce, veiciet šādas darbības.

1. Pārejiet uz sadaļu **Kreditori \> Izmaksu iestatīšana \> Automātiskās izmaksas**.
1. Kreisajā rūtī laukā **Līmenis** izvēlieties vai nu **Galveni** vai **Rindu** atkarībā no jūsu biznesa vajadzībām.
1. Laukā **Mazumtirdzniecības kanāla kods** izvēlieties atbilstošo kanāla kodu (piemēram, **Tabula** vai **Grupa**). Ja tiek izmantots noklusētais iestatījums **Visi**, izmaksas noteikumi tiek piemēroti visiem kanāliem.

    - Ja atlasāt **Grupu**, pārliecinieties, ka mazumtirdzniecības kanāla izmaksu grupa tiek izveidota sadaļā **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> Izmaksas \> Mazumtirdzniecības kanāla izmaksas grupas**.
    - Ja atlasāt **Tabulu**, jūs varat atlasīt noteiktu kanālu (piemēram, **Sanfrancisko**) laukā **Mazumtirdzniecības kanāla relācija**.

1. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
1. Kreisajā rūtī atrodiet un atlasiet **1040** (**Preces**) darbu.
1. Darbību rūtī atlasiet **Palaist tagad**.
1. Atkārtojiet iepriekšējos divus soļus, lai palaistu **1070** (**Kanāla konfigurācija**) un **1110** (**Globālā konfigurācija**) darbus.
    
![Automātiskās izmaksas definētas pēc kanāla](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Piemēra situācija

Sekojošajā piemērā aprakstīti soļi, kas nepieciešami preces konfigurēšanai, lai otrreizējās pārstrādes izmaksas tiktu iekasētas, kad prece tiek pārdota, izmantojot Sanfrancisko faktiskās pārdošanas kanālu. Piemērā ir arī parādīts, kā automātiskās izmaksas parādās Commerce pārdošanas punkta (POS) programmā.

Organizācija nosaka izmaksu kodu ar nosaukumu **PĀRSTRĀDE**, kā parādīts sekojošajā ilustrācijā.

![PĀRSTRĀDES izmaksu kods](media/Auto-charges-charge-code.png)

Automātiska izmaksa ir izveidota rindas līmenī. Tai ir tālāk minētā konfigurācija:

- Lauks **Konta kods** ir iestatīts uz **Visi**.
- Lauks **Krājuma kods** ir iestatīts uz **Tabula**.
- Lauks **Krājuma relācija** ir iestatīts uz preces ID **91001**.
- Lauks **Piegādes veida kods** ir iestatīts uz **Visi**.
- Lauks **Mazumtirdzniecības kanāla kods** ir iestatīts uz **Tabula**.
- Lauks **Mazumtirdzniecības kanāla relācija** ir iestatīts uz **Sanfrancisko** veikalu.

Tiek izveidota automātiskā izmaksu rinda. Tai ir tālāk minētā konfigurācija:

- Lauks **Valūta** ir iestatīts uz **USD**.
- Lauks **Izmaksu kods** ir iestatīts uz **PĀRSTRĀDE**.
- Lauks **Kategorija** ir iestatīts uz **Fiksēts**.
- Lauks **Izmaksas** ir iestatīts uz **$6.25**.

![Rindas līmeņa automātiskās izmaksas un automātiskās izmaksas rindas konfigurācija](media/Auto-charges-recyclingfee-line-fee.png)

POS programmā ir izveidots pārdošanas pasūtījums **Sanfrancisko** veikala kanālā. **Izmaksu** rindā ir redzama pārstrādes izmaksa **$6.25**.

Atlasot **Transakciju opcijas \> Izmaksas \> Pārvaldīt maksas** POS programmā, varat skatīt izmaksu kodu un aprakstu par pārstrādes izmaksu.

![Otrreizējās pārstrādes maksa POS programmā](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Papildu resursi

[Omni kanāla papildu automātiskās maksas](omni-auto-charges.md)

[Proporcionāla virsraksta maksu sadalīšana atbilstošajās pārdošanas rindās](pro-rate-charges-matching-lines.md)
