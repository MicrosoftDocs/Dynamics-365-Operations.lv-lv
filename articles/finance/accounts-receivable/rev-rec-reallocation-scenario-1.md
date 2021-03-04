---
title: Ieņēmumu atzīšanas atkārtota sadale — 1. scenārijs
description: Šajā tēmā ir iekļauts atkārtotas sadales scenārijs, kur tiek ievadīti divi pārdošanas pasūtījumi, taču tie tiek tikai apstiprināti. Viens un tas pats scenārijs radīs līdzīgus rezultātus, ja vairāk nekā divu pārdošanas pasūtījumu statuss ir Apstiprināts.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a0add2d4bc01127c1f359736398123a6a3df9fe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969656"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Ieņēmumu atzīšanas atkārtota sadale — 1. scenārijs

[!include [banner](../includes/banner.md)]

Šajā tēmā ir iekļauts atkārtotas sadales scenārijs, kur tiek ievadīti divi pārdošanas pasūtījumi, taču tie tiek tikai apstiprināti. Viens un tas pats scenārijs radīs līdzīgus rezultātus, ja vairāk nekā divu pārdošanas pasūtījumu statuss ir Apstiprināts.

Šim scenārijam **virsgrāmatas parametru** lapas cilnē **Ieņēmumu atzīšana** opcija **Grāmatot rēķinu labojumus debitoru parādos** ir iestatīta uz **Nē**(**Ieņēmumu atzīšana \> iestatīšana \> Virsgrāmatas parametri**).

[![Opcija Grāmatot rēķinu labojumus debitoru parādos ir iestatīta uz Nē](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir izveidots debitoram US\_SI\_0003. Debitors iegādājas klēpjdatoru (krājuma numurs S0012) un tam paredzētu atbalsta plānu (krājuma numurs S0008, "Nepārtraukts inženierijas pakalpojums"). Klēpjdatora ieņēmumi tiek nekavējoties atpazīti (nav ieņēmumu atzīšanas grafika). Atbalsta plāna ieņēmumi tiks atlikti un atzīti 12 mēnešu laikā, kā definēts saskaņā ar līguma laika periodu.

[![Klēpjdatora un atbalsta plāna pārdošanas pasūtījuma rindas](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Pārdošanas pasūtījums ir apstiprināts. Tā kā abi krājumi ir iestatīti ieņēmumu cenas sadalījumam, ieņēmumu cena tiek aprēķināta, kad tiek apstiprināts pārdošanas pasūtījums. Ieņēmumus, kas tiks atpazīti, var apskatīt **ieņēmumu cenas sadalījuma** lapā (**pārdošanas pasūtījuma** lapas darbību rūts cilnes **Pārvaldīt** grupā **Ieņēmumu atzīšana** atlasiet **Ieņēmumu cenas sadalījums**). Klēpjdatora ieņēmumi tiks grāmatoti ieņēmumu kontā 1008,01 $ summas apmērā. Atbalsta plāna ieņēmumi tiks grāmatoti atlikto ieņēmumu kontā 190,99 $ summas apmērā. Ieņēmumu cenu summai jābūt vienādai ar to rindu summu, kas tika iestatītas ieņēmumu cenu sadalījuma tveršanai (1199,00 $).

[![Ieņēmumu cenas sadalījuma lapa](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Debitors pārdošanas laikā izvēlējās neiegādāties instalēšanas pakalpojumus (krājuma numurs S0001), taču vēlāk pārdomāja. Tāpēc tam pašam debitoram tiek ievadīts otrs pārdošanas pasūtījums.

[![Pārdošanas pasūtījuma rinda instalēšanas pakalpojumiem](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

Otrais pārdošanas pasūtījums ir apstiprināts. Tā kā šajā pārdošanas pasūtījumā ir tikai viena rinda, ieņēmumu cenas sadalījums netiek veikts, kad tiek apstiprināts pārdošanas pasūtījums. Ieņēmumu cenas sadalījums notiek tikai tad, ja ir divi vai vairāki unikāli krājumi un ja šie krājumi ir iestatīti ieņēmumu cenas sadalījumam.

Ja šis jaunais pārdošanas pasūtījums ir vienīgās izmaiņas debitora līgumā, tagad var palaist atkārtotas sadales procesu. Vienā no abiem pārdošanas pasūtījumiem atlasiet **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**, lai atvērtu lapu **Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**. Vai arī dodieties uz **Ieņēmumu atzīšana \> Periodiski uzdevumi \> Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām**. Atlasiet divus pārdošanas pasūtījumus un atbilstošās pārdošanas pasūtījuma rindas un pēc tam atlasiet **Atjaunināt atkārtoto sadali**. Kolonna **Atkārtoti sadalītā summa** parāda jauno ieņēmumu cenu katrai pārdošanas pasūtījuma rindai.

[![Jaunas ieņēmumu cenas lapā Atkārtoti sadalīt cenu ar jaunām pasūtījuma rindām](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Ja atlasāt **paredzēto dokumentu**, nekas netiek rādīts, jo nav grāmatots neviens rēķins.

Lai pabeigtu atkārtoto sadali, atlasiet **Apstrādāt**. Tiek parādīts uzaicinājums ievadīt grāmatošanas datumu, pat ja nekas nav grāmatots. Kad atkārtotā sadale ir pabeigta, **ieņēmumu cenas sadalījuma** lapa katram pārdošanas pasūtījumam parāda cenu sadalījumu visiem krājumiem abos pārdošanas pasūtījumos. Citiem vārdiem sakot, **ieņēmumu cenas sadalījuma** lapa katram pārdošanas pasūtījumam ietver krājumu, kas šajā pārdošanas pasūtījumā nepastāv, jo tas ir daļa no tā paša līguma, bet no cita pārdošanas pasūtījuma.

> [!TIP]
> Lai parādītu kontekstu, kāpēc šie papildu krājumi tiek rādīti, režģim var pievienot citas kolonnas, piemēram, **Atkārtotas sadales ID** un **Pārdošanas pasūtījums**.
> 
> [![Papildu kolonnas ieņēmumu cenu sadalījumu lapā](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]