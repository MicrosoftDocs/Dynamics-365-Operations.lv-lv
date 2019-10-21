---
title: Krājumu uzmeklēšana pārdošanas punktā (POS)
description: Šajā tēmā ir aprakstītas opcijas, kas ir pieejamas krājumu informācijas apskatīšanai pārdošanas punktā (Point of Sale — POS).
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 609f5f13f3af4a7621fe7ee152800dac4d68a9fc
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025153"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Krājumu uzmeklēšana pārdošanas punktā (POS)

[!include [banner](includes/banner.md)]

Krājumu pārlūkošana pārdošanas punktā (POS) palīdz mazumtirgotājiem sasniegt reāllaika operatīvo izcilību un gūt ieskatus, savienojot veikalus, POS un dokumentu apstrādes biroju. Šī funkcionalitāte nodrošina precīzu reāllaika skatu uz preču krājumiem dažādos veikalos un vairumtirdzniecības bāzēs. Tā arī palīdz mazumtirgotājiem uzlabot efektivitāti un izmaksu ietaupījumus, uzlabojot krājumu plānošanu reālajā laikā.

Precīzs reāllaika skats uz krājumiem visā organizācijā palīdz veikala darbiniekiem nodrošināt laicīgu un izcilu klientu apkalpošanu. Šīm iespējām vislielākā nozīme ir brīdī, kad debitors ir gatavs pieņemt lēmumu par pirkumu. Ir svarīgi, lai kasieriem veikalā pie rokas būtu informācija par reālā laika krājumiem un viņi varētu dot precīzus solījumus par preču piegādi un savākšanu.

Varat atvērt lapu **Krājumu pārlūkošana** darbvietā **Retail Modern POS** vai darbvietā **Retail Cloud POS**.

![Krājumu pārlūkošanas elements POS sākumlapā](media/POSHomepage.png)

Lapā **Krājumu pārlūkošana** varat izmantot cipartastatūru, lai ievadītu preces numuru. Pēc tam varat skatīt rīcībā esošo daudzumu vairākiem veikaliem un noliktavām.

![Standarta krājumu pārlūkošanas lapa](media/InventoryLookUp.png)

Katrai vietai tiek rādīts arī daudzums **Rezervēts** un **Pasūtīts**.

- **Rezervēts** — šis daudzums attiecas uz vērtību **Fiziski rezervēts** no dokumentu apstrādes biroja attiecībā uz norādīto preces numuru attiecīgajā vietā.
- **Pasūtīts** — šis daudzums attiecas uz vērtību **Pasūtīts kopā** no dokumentu apstrādes biroja attiecībā uz norādīto preces numuru attiecīgajā vietā.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Vietas, kurām tiek rādīta informācija par krājumu pieejamību

Šajā vietu sarakstā ir divu tālāk aprakstīto tipu elementi.

- **Mazumtirdzniecības veikali** — sarakstā tiek rādīti veikali, kas tiek konfigurēti, izmantojot veikalu vietrāžu grupu pašreizējam veikalam programmā Retail Headquarters.
- **Sadales centri** — programmā Retail var konfigurēt dažādus sadales centru veidus (piemēram, noliktavas). Taču šajā sarakstā tiek rādīta informācija par krājumu pieejamību tikai vairumtirdzniecības bāzēm ar noklusējuma tipu **Standarta**.

    > [!NOTE]
    > Informācija par krājumu pieejamību netiek rādīta noliktavām ar POS tipu **Tranzīts**, **Karantīna** un **Preces ceļā**.

Lapā **Krājumu pārlūkošana** varat skatīt daudzumus Pieejams solīšanai (Available to Promise — ATP) katram veikalam, kā arī pašreizējos rīcībā esošos daudzumus, rezervētos daudzumus un pasūtītos daudzumus. Atlasiet veikalu, kam vēlaties skatīt ATP informāciju, un pēc tam atlasiet vienumu **Rādīt veikalu pieejamību**.

![ATP daudzumi](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>No dimensijas atkarīgas matricas skata atvēršana, lai rādītu visus variantus

Preces šablona lapā **Informācija par preci** vai lapā **Krājumu pārlūkošana** no programmas joslas lapas apakšā atlasiet vienumu **Skatīt visus variantus**. Skatā **No dimensijas atkarīga matrica** sākotnējai palaišanai no šīm lapām tiek rādīta informācija par krājumu pieejamību visiem pašreizējā veikala preces varantiem.

> [!NOTE]
> Poga **Skatīt visus variantus** ir pieejama tikai tādiem krājumu preču šabloniem, kam ir preču varianti. Tā nav pieejama savrupām precēm vai komplektiem.

![Poga “Skatīt visus variantus” krājumu meklēšanas lapā](media/StandardToMatrix.png)

Atlasiet vienumu **Skatīt visus variantus** preces šablona lapā **Informācija par preci** vai lapā **Krājumu pārlūkošana**, neatlasot atrašanās vietu, lai pārietu uz skatu **No dimensijas atkarīga matrica** un redzētu informāciju par krājumu pieejamību visiem preces variantiem pašreizējā veikalā.

![Skats “No dimensijas atkarīga matrica” krājumu pārlūkošanas lapai](media/Matrix.png)

> [!NOTE]
> Iepriekšējā attēlā dimensiju rādīšanas secība ir pēc alfabēta, jo dimensiju rādīšanas secība atlasītajai precei nebija konfigurēta.

Skata **No dimensijas atkarīga matrica** preču variantu šūnās labajā apakšējā stūrī ir rīcībā esošā vērtība. Nākamajā tabulā ir paskaidrota dažādo vērtību nozīme.

| Rīcībā esošā vērtība                            | Apraksts |
|------------------------------------------|-------------|
| Skaitliska vērtība, kas ir lielāka par 0 (nulle) | Uz atlasīto vietu ir izlaists variants, un šajā šūnā jūs varat veikt arī papildu darbības. (Šīs darbības ir detalizētāk aprakstītas tālāk šajā tēmā.) |
| **0** (nulle)                             | Uz atlasīto vietu ir izlaists variants, bet krājums atlasītajā vietā nav pieejams. Taču šajā šūnā varat veikt papildu darbības. (Šīs darbības ir detalizētāk aprakstītas tālāk šajā tēmā.) |
| **Nav datu** vai neaktīva šūna              | Uz atlasīto vietu nav izlaists neviens variants, un šajā šūnā jūs nevarat veikt papildu darbības. |

Varat arī mainīt dimensiju rakursu, atlasot jaunas izmantojamās dimensijas.

![Rakursa maiņa](media/ChangePivot.png)

![Rakurss ir mainīts](media/PivotChanged.png)

> [!NOTE]
> Iepriekšējos attēlos atlasīto preču dimensiju rādīšanas secība ir pielāgota (nav pēc alfabēta). Tā ir balstīta uz dokumentu apstrādes birojā iestatīto dimensiju parādīšanas secību.

Turklāt skatā **No dimensijas atkarīga matrica** var veikt arī citas darbības, lai palīdzētu uzlabot veikala darbinieku produktivitāti. Daži piemēri:

- Mainīt veikala atrašanās vietu, lai uzmeklētu krājumu pieejamību visiem preču variantiem citās vietās. Šīs atrašanās vietas tostarp ir citi veikali attiecīgajā veikala vietrāžu grupā un vairumtirdzniecības bāzes ar noklusējuma tipu **Standarta**.
- Pārdot atsevišķu preces variantu kādam debitoram, izmantojot skaidru naudu un pārnešnu, saņemšanu veikalā vai nosūtīšanu uz kādu adresi.
- Debitoram nodrošināt ATP informāciju par atsevišķu preces variantu noteiktā vietā.

![Papildu darbības variantu elementi](media/VariantActions.png)

> [!NOTE]
> Iepriekšējā attēlā dimensiju rādīšanas secība ir pēc alfabēta, jo dimensiju rādīšanas secība atlasītajai precei nebija konfigurēta.

Nākamajā tabulā ir plašāka informācija par pieejamajām papildu darbībām.

| Darbība               | Apraksts |
|----------------------|-------------|
| Pārdot tagad             | Atlasīto preces variantu pievienot transakcijai un lietotāju novirzīt uz transakcijas ekrānu. (Šī darbība nav pieejama, ja atlasītā atrašanās vieta ir vairumtirdzniecības bāze.) |
| Saņemšana veikalā     | Izveidot debitora pasūtījumu preces variantam, kas tiks saņemts no atlasītās atrašanās vietas, un lietotāju novirzīt uz transakcijas ekrānu. (Šī darbība nav pieejama, ja atlasītā atrašanās vieta ir vairumtirdzniecības bāze.) |
| Nosūtīt preci         | Izveidot debitora pasūtījumu preces variantam, kas tiks nosūtīts no atlasītās atrašanās vietas, un lietotāju novirzīt uz transakcijas ekrānu. |
| Pieejamība         | Rādīt ATP informāciju atlasītajai variantu kombinācijai attiecībā uz atlasīto atrašanās vietu. |
| Rādīt visas vietas   | Pārslēgties uz standarta krājumu pārlūkošanas skatu un izcelt informāciju par krājumu pieejamību attiecībā uz nepieciešamo krājumu variantu visos veikalos šajā veikalu vietrāžu grupā, kā arī vairumtirdzniecības bāzēs ar tipu **Standarta/noklusējuma**. |
| Skatīt detalizētu informāciju par preci | Novirzīt lietotāju uz saistītā preces šablona lapu **Informācija par preci**. |
