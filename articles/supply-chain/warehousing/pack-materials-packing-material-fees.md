---
title: Iepakojuma materiāli un maksas
description: Šajā tēmā sniegta informācija par iepakojuma materiālu maksām, kas tiek maksātas pārstrādes uzņēmumiem noteiktos intervālos.
author: MarkusFogelberg
manager: tfehr
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1061f336701461df7a2cf78661788e4c6100c84d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432662"
---
# <a name="packing-materials-and-fees"></a>Iepakojuma materiāli un maksas

[!include [banner](../includes/banner.md)]

Iepakojuma materiālu papildmaksas pārstrādes uzņēmumam tiek maksātas konkrētos laika intervālos. Apmaksa tiek veikta par smaguma mērvienību katram iepakojuma vienības sastāvā esošajam materiālam. Lai arī iepakojuma materiālu papildmaksas tiek aprēķinātas un iekļautas atskaitēs, virsgrāmatas transakcijas netiek grāmatotas, jo papildmaksas netiek uzskatītas par valsts iestādei maksājamiem nodokļiem.

Iepakojuma materiālu svars un maksa tiek aprēķināti pārdošanas pasūtījumu rindām un pirkšanas pasūtījumu rindām.

Vienu vai vairākas iepakojuma vienības varat definēt vienam krājumam, krājumu grupai (iepakojumu grupai) vai visiem krājumiem. Iepakojuma vienība sastāv no iepakojuma materiāliem, to svara un no iepakojuma vienībā ietilpstošo krājumu skaita. Iepakojuma materiāla kods tiek piešķirts katram definētajam iepakojuma materiālu tipam. Pamatojoties uz iepakojuma materiāla kodu, konkrētam periodam varat norādīt cenu. Iepakojuma materiāla maksa tiek aprēķināta, pamatojoties uz šo informāciju.

> [!NOTE]
> Pat ja uzņēmumam nav jāsedz iepakojuma materiālu maksas, šo funkcionalitāti varat izmantot, lai aprēķinātu iepakojuma materiālu svara statistisko informāciju.

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a>Iepakojuma materiālu sadalījuma iestatīšana

Pirms varat aprēķināt iepakojuma materiālu svaru, iepakojuma materiālu maksas vai abus, ir jāieslēdz aprēķins un jānosaka, kuri materiāli un maksas attiecas uz kurām precēm.

1. Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Krājumu un noliktavas pārvaldības parametri**.
1. Cilnes **Vispārīgi** sadaļā **Iepakojuma materiāls** iestatiet opciju **Aprēķināt iepakojuma materiālu maksas** uz **Jā**.
1. Dodieties uz **Krājumu pārvaldība \>Iestatījumi \>Iepakojuma materiāls \>Iepakojuma grupas** un izveidojiet visas jūsu izmantotās iepakojuma grupas. Visi iepakojuma grupas krājumi izmanto vienu un to pašu iepakojuma materiālu sadalījumu. Ja neizmantojat iepakojuma grupas, varat šo darbību izlaist.

    > [!TIP]
    > Pēc tam, kad esat izveidojis iepakojuma grupas, katrai precei var piešķirt grupu pēc vajadzības. Dodieties uz **Preču informācijas pārvaldība \>Preces \> Izlaistās preces**, atlasiet preci un pēc tam kopsavilkuma cilnē **Pārvaldīt krājumus**, laukā **Iepakojuma grupa** atlasiet attiecīgo iepakojuma grupu.

1. Dodieties uz **Krājumu pārvaldība \>Iestatīšana \> Iepakojuma materiāls \> Iepakojuma materiāla kodi**, definējiet katru iepakojuma materiāla veidu, kuru izmantojat, un konkretizējiet vienību, kurā iepakojuma materiāls tiek patērēts, kad sagatavojat sūtījumus.
1. Dodieties uz **Krājumu pārvaldība \>Iestatīšana \> Iepakojuma materiāls \> Iepakojuma materiāla maksas** un iestatiet papildmaksu katram tikko definētajam iepakojuma materiāla veidam. Maksas tiek aprēķinātas, pamatojoties uz vienas patērētās vienības cenu.
1. Lai krājumiem iedalītu iepakojuma materiālus, dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Iepakojuma materiāls \> Iepakojuma materiālu sadalījums** un izveidojiet sadalījumus. Varat izveidoti tik daudz sadalījumu, cik nepieciešams. Varat sadalīt iepakojuma materiālus atsevišķiem krājumiem, krājumu grupām (iepakošanas grupām) vai visiem krājumiem atkarībā no tā, cik detalizēta ir jūsu sadale.

    Katram izveidotajam sadalījumam izpildiet tālākās darbības.

    1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus.

        - **Krājuma kods** — atlasiet sadalījuma tvērumu:

            - **Tabula** — izveidojiet sadalījumu vienam noteiktam krājumam.
            - **Grupa** – izveidojiet sadalījumu visiem krājumiem, kas pieder iepakojumu grupai, kas definēta lapā **Iepakojumu grupas**.
            - **Visi** – izveidojiet sadalījumu visiem krājumiem.

            > [!NOTE]
            > Parasti visiem jūsu sadalījumiem ir jābūt vienā līmenī (**Tabula**, **Grupa** vai **Visi**). Ja izmantojat vairāk nekā vienu līmeni, katram krājumam tiek izmantots viskonkrētāk atbilstošākais sadalījums. ( **Tabulas** līmenis dominē pār **Grupas** līmeni, un abiem šiem līmeņiem ir prioritāte pār līmeni **Visi** līmeni.)

        - **Krājumu relācija** — ja piešķirat vienam krājumam, atlasiet krājumu. Ja piešķirat krājumu grupai, atlasiet iepakojuma grupu. Ja piešķirat visiem krājumiem, atstājiet šo lauku tukšu.
        - **Konfigurācija**, **Izmērs**, **Krāsa** un **Stils** — pēc nepieciešamības ievadiet šo dimensiju vērtības, lai vēl vairāk definētu krājumu, ko piešķirat.
        - **Iepakojuma vienība** — atlasiet vienību, kurā krājums tiek iepakots, kad tiek izmantots iepakojuma materiāls. Šī vienība var atšķirties no vienības, kurā krājums tiek pirkts un glabāts.
        - **Iepakojuma vienības faktors** — ievadiet konvertēšanas koeficientu, kas tiek izmantots, lai konvertētu no krājuma vienības uz iepakojuma vienību. ( Konvertēšana izmanto formulu *Iepakošanas vienības* = *Krājuma vienības* x *Iepakojuma vienības koeficients*.)

    1. Kopsavilkuma cilnē **Iepakojuma materiāls** pievienojiet rindu katrai iepakojuma materiāla vienībai, kura ir nepieciešama pašreizējam sadalījumam. Katrā rindā norādiet materiāla tipu (kā definēts lapā **Iepakojuma materiāla kodi**) un tā summu, kas tiek patērēta katrai dotā krājuma sūtītajai vienībai.

## <a name="packing-units-on-sales-order-lines"></a>Iepakojuma vienības pārdošanas pasūtījuma rindās

Pēc tam, kad[ ir ieslēgts iepakojuma materiāla maksu aprēķins un iestatīti sadalījumi](#allocations), sistēma pārbauda, vai katram krājumam, kas tiek pievienots pārdošanas pasūtījumam, ir norādītas iepakojuma vienības. Pēc tam tas aprēķina visas nepieciešamās maksas. Kad krājums ir pievienots pārdošanas pasūtījumam, notiek viena no šīm darbībām:

- **Ja krājumam tiek piemērots iepakojuma sadalījums:** Pārdošanas pasūtījuma rindu sistēma atjaunina ar norādīto iepakojuma vienību un iepakojuma vienības daudzumu. (Iepakojuma vienības daudzums tiek aprēķināts, izmantojot formulu *Iepakojuma vienību daudzums* = *Pasūtītais daudzums* ÷ *Krājumu skaits atlasītajā iepakojuma vienībā*.)
- **Ja krājumam netiek piemērots iepakojuma sadalījums:** iepakojuma vienību un iepakojuma vienību skaitu varat manuāli ievadīt pārdošanas pasūtījuma rindā.

Iepakojuma vienību un iepakojuma vienību daudzumu varat arī mainīt, kad grāmatojat pārdošanas pasūtījuma rindu. Šī iespēja ir svarīga, ja pārdošanas pasūtījuma rinda ir tikai daļēji piegādāta vai daļēji iekļauta rēķinā.

Kad izrakstāt rēķinu par pārdošanas pasūtījumu, sistēma izveido iepakojuma materiālu transakcijas. Iepakojuma materiālu transakcijas ietver iepakojuma materiālu svaru attiecīgajai pārdošanas rindai. Pēc rēķinu izrakstīšanas transakcijas var modificēt. Pēc tam varat izveidot jaunas transakcijas.

## <a name="packing-units-on-purchase-order-lines"></a>Iepakojuma vienības pirkšanas pasūtījuma rindās

Sistēma neveido iepakojuma materiāla darījumus pirkšanas pasūtījuma rindām. Tā vietā jūs manuāli izveidojat transakcijas rēķinā iekļautajām pirkšanas pasūtījuma rindām lapā **Iepakojuma materiāla transakcijas**.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Iestatiet licenču numurus debitoriem, kuriem ir jāmaksā iepakojuma materiālu maksas

Ja pārdošanas pasūtījumiem noteiktam debitoram jāietver maksas par iepakojuma materiāliem, kas tiek izmantoti katram pasūtījumam, rīkojieties šādi.

1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
1. Atlasiet debitoru, no kura jāietur maksa par iepakojuma materiāliem.
1. Kopsavilkuma cilnē **Rēķini un piegāde**, iestatiet tālāk minētos laukus:

    - Sadaļā **PVN** laukā **Iepakojuma nodokļa licences numurs** ievadiet uzņēmuma licences numuru.
    - Sadaļā **Iepakojuma materiāla maksa** laukā **Licences numurs** ievadiet uzņēmuma licences numuru.

Veidojot un izrakstot rēķinu pārdošanas pasūtījumam, kas ietver vienu vai vairākus krājumus, kas izmanto iepakojuma materiālus, rēķins parāda iepakojuma materiālu maksas.

Debitoriem, kuriem nav jāmaksā iepakošanas materiālu maksas, veiciet tās pašas darbības, bet dzēsiet licenču numurus no laukiem **Iepakojuma nodokļa licences numurs** un **Licences numurs**. Rēķini debitoriem, kuri nemaksā iepakojuma materiāla maksas, rāda iepakojuma materiālu svaru, bet nerāda maksas.

Lai ģenerētu pārskatu, kurā redzamas visas iepakojuma materiālu maksas, ko uzņēmums būs parādā noteiktam periodam dodieties uz **Krājumu pārvaldība \> Vaicājumi un pārskati \> Iepakojuma materiāla pārskati \> Iepakojuma materiāla maksas aprēķins**, norādiet datumu diapazonu un pēc tam atlasiet **Labi**.

## <a name="print-packing-material-weights-on-invoices"></a>Iepakojuma materiāla svaru drukāšana rēķinos

Iepakojuma materiāla svaru varat drukāt uz rēķina un norādīt, kurš maksā saistītās maksas. Svars tiek summēts pēc iepakojuma koda.

1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
1. Cilnē **Atjauninājumi**, kopsavilkuma cilnē **Rēķins** iestatiet opciju **Drukāt iepakojuma materiāla svaru** uz **Jā**.
