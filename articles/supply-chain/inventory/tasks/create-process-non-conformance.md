---
title: Neatbilstības izveide un apstrāde
description: Šajā tēmā ir aprakstīts, kā veikt neatbilstības pārvaldību, balstoties uz esošu kvalitātes pasūtījumu.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032f5b712c2be5312524129cd25e655e778f5f44
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580868"
---
# <a name="create-and-process-nonconformances"></a>Neatbilstības izveide un apstrāde

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā veikt neatbilstības pārvaldību, balstoties uz esošu kvalitātes pasūtījumu. Parasti neatbilstības pārvaldību veic kvalitātes darbinieks. Pēcnosacījumam jābūt pieejamam kvalitātes pārbaudes pasūtījumam. (Informāciju par to, kā izveidot kvalitātes pārbaudes pasūtījumu, skatiet [Pārbaudīt preču kvalitāti](inspect-quality-goods.md).)

Pirms lietotājs var apstrādāt neatbilstības apstiprinājumu, darbiniekiem jābūt piešķirtiem laukā **Persona** lapā **Lietotājs**. Turklāt, pirms lietotājs var lietot dokumentu piezīmes, lietotāja opcijās **Aktivizēt dokumentu apstrādi** jābūt iestatītai uz *Jā*.

## <a name="create-a-nonconformance"></a>Neatbilstības izveide

Lai izveidotu neatbilstību, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot neatbilstību** laukā **Problēmas veids** atlasiet problēmas veidu, kas tika atrasts pārbaudes procesa laikā.
1. Atlasiet **Labi**.

## <a name="approve-or-reject-a-nonconformance"></a>Neatbilstības apstiprināšana vai noraidīšana

Lai neatbilstību apstiprinātu vai noraidītu, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.
1. Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.

    > [!NOTE]
    > Varat pievienot labojumu tikai apstiprinātajai neatbilstībai.

1. Darbību rūtī atlasiet **Funkcijas \> Apstiprināt neatbilstību**, lai apstiprinātu neatbilstību vai **Funkcijas \> Noraidīt neatbilstību**, lai to noraidītu. Jūs varat saistīt apstiprinātas neatbilstības ar [saistītajām operācijām](../quality-operations.md). Šādā veidā var ierakstīt darbu, kas tiek veikts kā neatbilstības apstrādes un labošanas apstrādes daļa.
1. Tiek piedāvāts apstiprināt savu izvēli. Lai turpinātu, atlasiet **Jā**.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Pievienot neatbilstībai operācijas un citu detalizētu informāciju

Pēc tam, kad esat izveidojis neatbilstību, varat sākt pievienot saistītās operācijas un norādīt papildu informāciju par šīm operācijām. Varat pievienot saistītas operācijas tikai apstiprinātajai neatbilstībai.

Papildus pamatinformācijai, operācijai varat pievienot šādas detaļas:

- **Krājumi** – varat izveidot krājumu sarakstu, kas patērēti labošanas veikšanai. Piemēram, krājumi var būt produkti, kas nepieciešami iekārtas remontam vai sastāvdaļas, kas nepieciešamas pabeigtas preces remontam.
- **Kvalitātes izmaksas** – var izveidot to izmaksu sarakstu, kas radušās vai par kurām izrakstīts rēķins ārējiem avotiem.
- **Darba laika uzskaites tabula** – varat izveidot darba laika žurnālu, ko katrs darbinieks tērē operācijai.

Atlikušie iestātījumi nav obligāti. Katra krājuma, kvalitātes maksu un darba laika uzskaites tabulas izmaksas tiek summētas un parādītas operācijā. Operācijas lauku **Izmaksas** nevar labot tieši.

### <a name="create-an-operation-for-a-nonconformance"></a>Operācijas izveide neatbilstībai

Lai izveidotu operāciju neatbilstībai, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.
1. Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.

    > [!NOTE]
    > Varat pievienot vai atjaunināt operācijas tikai apstiprinātajai neatbilstībai.

1. Darbību rūtī atlasiet **Saistītās operācijas**.
1. Darbību rūts lapā **Saistītās operācijas** atlasiet **Jauns**, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādus laukus:

    - **Operācija** – atlasiet neatbilstībai veicamās operācijas kodu.
    - **Pamatojums** – ievadiet detalizētu aprakstu, kas skaidro, kāpēc operācija ir vajadzīga.
    - **Pārdošanas pasūtījums** - ja atlasītais operācijas kods ir saistīts ar pārdošanas pasūtījuma veidu, atlasiet pārdošanas pasūtījumu, ar kuru saistāt operāciju.
    - **Pirkšanas pasūtījums** - ja atlasītais operācijas kods ir saistīts ar pirkšanas pasūtījuma veidu, atlasiet pirkšanas pasūtījumu, ar kuru saistāt operāciju.

1. Aizveriet lapas.

### <a name="add-items-to-an-operation"></a>Pievienot krājumus operācijai

Lai pievienotu operācijai krājumus, veiciet šādas darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.
1. Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.

    > [!NOTE]
    > Varat pievienot vai atjaunināt operācijas tikai apstiprinātajai neatbilstībai.

1. Darbību rūtī atlasiet **Saistītās operācijas**.
1. Lapā **Saistītās operācijas** atlasiet operāciju, kurai vēlaties pievienot krājumus.
1. Darbību rūtī atlasiet **Krājumi**.
1. Darbību rūts lapā **Saistītās operācijas** atlasiet **Jauns**, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādus laukus:

    - **Krājuma numurs** – atlasiet preci, kas tiks patērēta kā daļa no atlasītās operācijas.
    - **Daudzums** – ievadiet krājumu skaitu, kas tiks patērēts.

    > [!NOTE]
    > Izmaksas par krājumu var skatīt laukā **Izmaksas**, cilnē **Vispārīgi**. Parādītās izmaksas nāk no izmaksām, kas iestatītas lapā **Izlaistā prece**. Izmaksas nevar atjaunināt tieši lapā **Saistīto operāciju krājums**. Visu krājumu izmaksas, kas tiek pievienotas lapā **Saistīto operāciju krājumi**, tiek automātiski pievienotas laukam **Izmaksas** lapā **Saistītās operācijas**.

1. Atkārtojiet iepriekšējo darbību katrai papildu precei, kas jāpievieno.
1. Aizveriet lapas.

### <a name="add-quality-charges-to-an-operation"></a>Kvalitātes maksu pievienošana darbībai

Lai pievienotu operācijai kvalitātes maksu, veiciet šādas darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.
1. Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.

    > [!NOTE]
    > Varat pievienot vai atjaunināt operācijas tikai apstiprinātajai neatbilstībai.

1. Darbību rūtī atlasiet **Saistītās operācijas**.
1. Lapā **Saistītās operācijas** atlasiet operāciju, kurai vēlaties pievienot kvalitātes maksu.
1. Darbību rūtī atlasiet **Kvalitātes maksa**.
1. Darbību rūts lapā **Saistītās operāciju maksas** atlasiet **Jauns**, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādus laukus:

    - **Izmaksu kods** — atlasiet kvalitātes maksu, ko vēlaties pievienot.
    - **Apraksts** — ievadiet maksas detālizēto aprakstu.
    - **Maksas vērtība** - Ievadiet maksas summu.

1. Atkārtojiet iepriekšējo darbību katrai papildu maksai, kas jāpievieno.
1. Aizveriet lapas.

> [!NOTE]
> Summa laukā **Izmaksu vērtība** tiek automātiski summēta visām kvalitātes maksām un pievienota visām citām summām laukā **Izmaksas**, lapā **Saistītās operācijas**.

### <a name="create-a-timesheet-on-an-operation"></a>Darba laika uzskaites tabulas izveide operācijā

Lai pievienotu operācijai darba laika uzskaites tabulu, veiciet šādas darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.
1. Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.

    > [!NOTE]
    > Varat pievienot vai atjaunināt operācijas tikai apstiprinātajai neatbilstībai.

1. Darbību rūtī atlasiet **Saistītās operācijas**.
1. Lapā **Saistītās operācijas** atlasiet operāciju, kurai vēlaties pievienot darba laika uzskaites tabulu.
1. Darbību rūtī atlasiet **Darba laika uzskaites tabula**.
1. Darbību rūts lapā **Saistītās operāciju darba laika uzskaites tabulas** atlasiet **Jauns**, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādus laukus:

    - **Datums** – norādiet datumu, kad darbs tika paveikts. Pēc noklusējuma šis lauks tiek iestatīts kā pašreizējais datums.
    - **Nodarbinātais** - Izvēlieties darbinieku, kurš paveica darbu. Pēc noklusējuma šis lauks ir iestatīts darbiniekam, kas piešķirts pašreizējam lietotājam.
    - **Operācijas stundas** – ievadiet stundu skaitu, kas tika nostrādāts atlasītajai operācijai.
    - **Izveidots rēķins** – atzīmējiet šo izvēles rūtiņu, ja rēķins ir izrakstīts debitoram vai kreditoram.

    > [!NOTE]
    > Izmaksas var skatīt laukā **Izmaksas** cilnē **Vispārīgi**. Izmaksas tiek aprēķinātas, izmantojot likmi, ko nosakiet lapā **Krājumu vadības parametri**.

1. Atkārtojiet iepriekšējo darbību katrai papildu darba laika uzskaites tabulas rindai, kas jāpievieno.
1. Aizveriet lapas.

> [!NOTE]
> Summa laukā **Izmaksas** tiek summēta visām darba laika uzskaites tabulas rindām un pievienota visām citām summām laukā **Izmaksas**, lapā **Saistītās operācijas**.

## <a name="add-a-correction-to-a-nonconformance"></a>Pievienot labojumu neatbilstībai

Lai neatbilstībai pievienotu labojumu, veiciet tālāk norādīto.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.
1. Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.

    > [!NOTE]
    > Varat pievienot labojumu tikai apstiprinātajai neatbilstībai.

1. Darbību rūtī atlasiet **Labojumi**.
1. Lapā **Labojumi**, darbības rūtī atlasiet **Jauns**, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādus laukus:

    - **Diagnostika** – atlasiet diagnostikas veidu, kas identificē jūsu veidotā labojuma veidu.
    - **Nodarbinātais** - Atlasiet par labojumu atbildīgo personu.
    - **Labošanas prioritāte** – atlasiet opciju, lai norādītu, kā labojumam vajadzētu būt prioritāram (*Zema*, *Normāla* VAI *Augsta*).
    - **Pieprasītais datums** – ievadiet datumu, kad tika pieprasīta labošanas darbība.
    - **Plānotais datums** – ievadiet datumu, kad būtu jāpabeidz labojums.
    - **Īstermiņa risinājums** - atzīmējiet šo izvēles rūtiņu, ja labojoša darbība izlabo neatbilstību tikai uz neilgu laiku.

1. Aizveriet lapas.

## <a name="mark-a-correction-as-completed"></a>Atzīmēt labojumu kā pabeigtu

Lai atzīmētu neatbilstības labojumu kā pabeigtu, veiciet šādas darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.
1. Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.

    > [!NOTE]
    > Varat pievienot labojumu tikai apstiprinātajai neatbilstībai.

1. Darbību rūtī atlasiet **Labojumi**.
1. Režģī lapā **Labojumi** atlasiet labojumu, kuru vēlaties atzīmēt kā pabeigtu.
1. Darbību rūtī atlasiet **Atzīmēt kā pabeigtu**.
1. Tiek piedāvāts apstiprināt savu izvēli. Lai turpinātu, atlasiet **Labi**. Lauks **Pabeigšanas datums un laiks** ir iestatīts uz pašreizējo datumu un laiku, un tiek atzīmēta izvēles rūtiņa **Pabeigts**.
1. Aizvērt lapu.

## <a name="reopen-a-completed-correction"></a>Atkārtoti atvērt pabeigto labojumu

Lai atkārtoti atvērtu pabeigto labojumu, veiciet šādas darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Neatbilstības**.
1. Sarakstā atlasiet neatbilstību, kuru vēlaties atjaunināt.
1. Darbību rūtī atlasiet **Labojumi**.
1. Režģī lapā **Labojumi** atlasiet labojumu, kuru vēlaties atkārtoti atvērt.
1. Darbību rūtī atlasiet **Atkārtoti atvērt**.
1. Tiek piedāvāts apstiprināt savu izvēli. Lai turpinātu, atlasiet **Labi**. Vērtība tiek notīrīta no lauka **Pabeigšanas datums un laiks**, un tiek notīrīta izvēles rūtiņa **Pabeigts**.
1. Aizvērt lapu.

Tagad labojumam var veikt papildu labojumus vai atjauninājumus. Pēc pabeigšanas labojumu var atzīmēt kā pabeigtu vēlreiz.

## <a name="close-a-nonconformance"></a>Neatbilstības aizvēršana

Lai aizvērtu neatbilstību, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pārbaudes pasūtījumi**.
1. Atlasiet režģī kvalitātes pasūtījumu.
1. Darbību rūtī atlasiet **Vaicājumi \> Neatbilstības**.
1. Lapā **Neatbilstības** atlasiet mērķa neatbilstību režģī.
1. Darbību rūtī atlasiet **Funkcijas \> Aizvērt neatbilstību**.
1. Tiek piedāvāts apstiprināt savu izvēli. Lai turpinātu, atlasiet **Jā**.
1. Aizveriet lapas.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības pārskats](../quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](../enable-quality-management.md)
- [Par neatbilstību apstiprināšanu atbildīgie darbinieki](../quality-responsible-workers.md)
- [Karantīnas zonas neatbilstībai](../quality-quarantine-zones.md)
- [Neatbilstību diagnostikas tipi](../quality-diagnostic-types.md)
- [Kvalitātes maksa par neatbilstībām](../quality-charges.md)
- [Operācijas neatbilstībai](../quality-operations.md)
- [Kvalitātes pārvaldība noliktavas procesiem](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
