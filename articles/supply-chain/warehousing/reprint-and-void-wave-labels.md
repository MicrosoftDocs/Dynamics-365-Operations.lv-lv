---
title: Kopuma etiķešu atkārtota drukāšana un anulēšana
description: Šajā tēmā ir paskaidrots, kā anulēt un atkārtoti drukāt esošās kopuma etiķetes.
author: GarmMSFT
manager: PJacobse
ms.date: 07/09/2020
ms.topic: article
ms.service: dynamics-ax-applications
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: cc76a3915d6a1e58a71eb997b5af58941905e879
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996052"
---
# <a name="reprint-and-void-wave-labels"></a>Kopuma etiķešu atkārtota drukāšana un anulēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā pārvaldīt kopuma apstrādes laikā ģenerētās etiķetes. (Detalizētu aprakstu un konfigurācijas instrukcijas skatiet sadaļā [Konfigurēt kopuma etiķešu drukāšanu](../warehousing/configure-wave-label-printing.md).)

Kopuma etiķetes var atkārtoti drukāt jebkurā laikā. Piemēram, var būt nepieciešams drukāt vienu etiķeti, ja esošā etiķete ir pazaudēta vai bojāta. Vai arī noliktavas darbiniekam vai supervizoram var nākties atkārtoti drukāt veselu etiķešu rulli, ja ir mainījies visas kopuma etiķešu sērijas skaits un/vai sastāvs (piemēram, krājumu iztrūkuma vai citu iemeslu dēļ). Bieži pat tad, ja ir mainījies tikai kastu skaits, viss rullis ir jādrukā vēlreiz, lai saglabātu precīzu kopējo skaitu katras etiķetes “Kaste X no Y” sadaļā.

Kopuma etiķešu atkārtotas drukāšanas līdzeklis atbalsta šādu funkcionalitāti:

- Atkārtoti drukājiet etiķetes no noliktavas programmas un bagātinātā klienta.
- Anulējiet etiķetes un vienlaicīgi drukājiet tās atkārtoti. (Piemēram, iespēja anulēt etiķetes ir iegulta saīsinātajos izdošanas scenārijos.)
- Notīriet kopuma etiķešu vēsturi.

Šajā tēmā ir apkopoti scenāriji, kas, izmantojot piemērus, parāda, kā strādāt ar kopuma etiķešu atkārtotas drukāšanas līdzekli.

> [!IMPORTANT]
> Lai strādātu ar šajā tēmā aprakstītajiem scenārijiem, vispirms ir jāieslēdz un jākonfigurē atbilstošie kopuma drukāšanas līdzekļi, kā aprakstīts sadaļā [Konfigurēt kopuma etiķešu drukāšanu](../warehousing/configure-wave-label-printing.md). Vairāki no šīs tēmas scenārijiem pieprasa vispirms strādāt ar attiecīgās tēmas scenārijiem, lai ģenerētu priekšnosacījumu datu paraugus.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>1. scenārijs: atkārtota etiķešu drukāšana no tīmekļa klienta

Varat skatīt un atkārtoti drukāt kopuma etiķetes no šādām lapām. Katras lapas darbību rūts cilnē **Sūtījumi** grupā **Saistītā informācija**, atlasiet **Kopuma etiķetes**.

- Visi sūtījumi \> Sūtījuma informācija
- Visas kravas \> Kravas informācija
- Visi kopumi
- Kopuma etiķetes
- Kopuma etiķešu vēsture

Lai atkārtoti drukātu kopuma etiķeti no tīmekļa klienta, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \>Izejošie kopumi \>Sūtījuma kopumi \>Visi kopumi**.
1. Atlasiet kopumu, no kura atkārtoti drukāt etiķetes.
1. Darbību rūts cilnē **Kopums**, grupā **Drukāt** atlasiet **Kopuma etiķetes**.
1. Izpildiet vienu vai abas no tālāk minētajām darbībām:

    - Lai atkārtoti drukātu etiķeti, laukā **Printera nosaukums** atlasiet printeri. (Atstājiet šo lauku tukšu, ja vēlaties tikai atjaunināt kopuma etiķetes informāciju, nedrukājot etiķeti atkārtoti.)
    - Lai atjauninātu etiķeti, atzīmējiet izvēles rūtiņu **Atjaunināt kopuma etiķetes informāciju**. (Atstājiet šo izvēles rūtiņu neatzīmētu, ja vēlaties tikai atkārtoti drukāt iepriekšējo etiķeti.)

    > [!NOTE]
    > Katru reizi, kad kopuma etiķete tiek drukāta vai atkārtoti drukāta, tās dati tiek pārvērsti, izmantojot attiecīgo kopuma etiķešu izkārtojumu, un visi vietturi tiek aizstāti ar faktiskajām vērtībām. Iegūtā virkne tiek saglabāta kā ieraksts kopuma etiķešu vēsturē. Ja izvēles rūtiņa **Atjaunināt kopuma etiķetes informāciju** tiek notīrīta, Zebra programmēšanas valodas (ZPL) saglabātie dati tiek izmantoti, kad etiķete tiek atkārtoti drukāta. Ja izvēles rūtiņa **Atjaunināt kopuma etiķetes informāciju** tiek atzīmēta, tiek ģenerēta jauna virkne. Esošās kopuma etiķetes tiek pārrēķinātas, un visas liekās etiķetes (piemēram, ja saistītās darba rindas ir atceltas vai modificētas) ir atzīmētas kā **Anulēts** un nav atkārtoti drukājamas.

1. Atlasiet **Labi**, lai apstiprinātu atlasi.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>2. scenārijs: atkārtota etiķešu drukāšana no noliktavas programmas

Šis scenārijs parasti tiek lietots, ja etiķešu rullis ir pazaudēts vai bojāts. Tas sniedz piemēru, parādot, kā iestatīt mobilās ierīces izvēlnes vienumus, kas ļauj darbiniekiem atkārtoti drukāt vienu un vairākas etiķetes. Pēc tam tiek parādīts, kā izmantot šos jaunos izvēlnes vienumus, strādājot ar mobilo ierīci.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Mobilajai ierīcei nepieciešamo izvēlnes vienumu un izvēlnes iestatīšana

Pirms darbinieki var atkārtoti drukāt etiķetes no mobilās ierīces, ir jāiestata izvēlnes vienumi, lai nodrošinātu šo funkcionalitāti, un pēc tam tie ir jāpievieno noliktavas programmas izvēlnei.

#### <a name="create-new-mobile-device-menu-items"></a>Jaunas mobilās ierīces izvēlnes vienumu izveide

Veiciet tālāk norādītās darbības, lai izveidotu jaunu izvēlnes vienumu kolekciju, atkārtotai etiķešu drukāšanai no noliktavas programmas.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Izveidojiet izvēlnes vienumu un iestatiet tam šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Atkārtoti drukāt vienu kopuma etiķeti*
    - **Nosaukums:** *Atkārtoti drukāt vienu kopuma etiķeti*
    - **Režīms:** *Netiešs*
    - **Aktivitātes kods:** *Atkārtoti drukāt vienu kopuma etiķeti*

1. Izveidojiet otru izvēlnes vienumu un iestatiet tam šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Atkārtota etiķešu drukāšana (Krājums)*
    - **Nosaukums:** *Kopuma etiķešu atkārtota drukāšana (Krājums)*
    - **Režīms:** *Netiešs*
    - **Aktivitātes kods:** *Atkārtoti drukāt vairākas kopuma etiķetes*
    - **Rādīt darbu saraksta grupēšanas filtru:** *Jā*
    - **Sistēmas grupēšanas lauks:** *ShipmentID*
    - **Sistēmas grupēšanas etiķete:** *Sūtījuma ID*
    - **Drukas režīms:** *Prece*

1. Darbību rūtī atlasiet **Lauku saraksts**, lai atvērtu lapu, kurā var atlasīt laukus, kas tiks parādīti, lai palīdzētu darbiniekiem identificēt pareizo etiķešu rulli.
1. Var norādīt līdz septiņiem laukiem. Izmantojiet nolaižamos sarakstus, lai atlasītu lauku, kas ir redzams katrā pieejamā pozīcijā. Atstājiet tukšus visus laukus, kuri nav nepieciešami. 

    Tas ir piemērs:

    - **Parādāmais lauks:** *LabelItemId*
    - **2. parādāmais lauks:** *LabelItemName*
    - **3. parādāmais lauks:** *InventQty*
    - **4. parādāmais lauks:** *LabelUnitId*

1. Aizvērt lapu.
1. Izveidojiet trešo izvēlnes vienumu un iestatiet tam šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Atkārtota etiķešu drukāšana (Uzskaitījums)*
    - **Nosaukums:** *Kopuma etiķešu atkārtota drukāšana (Uzskaitījums)*
    - **Režīms:** *Netiešs**
    - **Aktivitātes kods:** *Atkārtoti drukāt vairākas kopuma etiķetes*
    - **Rādīt darbu saraksta grupēšanas filtru:** *Jā*
    - **Sistēmas grupēšanas lauks:** *ShipmentID*
    - **Sistēmas grupēšanas etiķete:** *Sūtījuma ID*
    - **Drukāšanas režīms:** *Uzskaitījums*

1. Darbību rūtī atlasiet **Lauku saraksts** un pēc tam, izmantojot nolaižamos sarakstus, atlasiet laukus, kas tiks parādīti, lai palīdzētu darbiniekiem identificēt pareizo etiķešu rulli (piemēram, *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId* un *NumberOfLabels*).
1. Aizvērt lapu.
1. Izveidojiet ceturto izvēlnes vienumu un iestatiet tam šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Atkārtota etiķešu drukāšana (pēc pēdējā)*
    - **Nosaukums:** *Kopuma etiķešu atkārtota drukāšana (pēc pēdējā)*
    - **Režīms:** *Netiešs*
    - **Aktivitātes kods:** *Atkārtoti drukāt vairākas kopuma etiķetes*
    - **Rādīt darbu saraksta grupēšanas filtru:** *Jā*
    - **Sistēmas grupēšanas lauks:** *ShipmentID*
    - **Sistēmas grupēšanas etiķete:** *Sūtījuma ID*
    - **Drukas režīms:** *Pēdējās derīgās kopuma etiķetes ID*

1. Darbību rūtī atlasiet **Lauku saraksts** un pēc tam, izmantojot nolaižamos sarakstus, atlasiet laukus, kas tiks parādīti, lai palīdzētu darbiniekiem identificēt pareizo etiķešu rulli (piemēram, *LabelItemId*, *LabelItemName*, *InventQty*, *LabelUnitId* un *NumberOfLabels*).
1. Aizvērt lapu.

#### <a name="set-up-the-mobile-device-menu"></a>Mobilās ierīces izvēlnes iestatīšana

Veiciet tālāk norādītās darbības, lai pievienotu jaunos izvēlnes vienumus noliktavas programmas izvēlnei.

1. Dodieties uz **Noliktavas vadība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlne**.
1. Atlasiet esošu **Izejošs** izvēlni.
1. Kreisajā pusē esošajā sarakstā atrodiet tikko izveidotos atkārtotās drukas izvēlnes vienumus un pēc tam, izmantojot labās bultiņas pogu, pievienojiet tos labajā pusē esošajam sarakstam.
1. Aizvērt lapu.

### <a name="use-cases"></a>Lietošanas gadījumi

Šeit sniegtie lietošanas gadījumi sniedz piemērus, kā izmantot dažādus iestatītos mobilās ierīces izvēlnes vienumus, lai darbinieki varētu atkārtoti drukāt kopuma etiķetes.

Pirms sākat strādāt ar šiem lietošanas gadījumiem, ir jābūt ieviestiem šādiem priekšnoteikumiem:

- Ir jābūt instalētiem demonstrācijas datiem un ir jāatlasa **USMF** juridiskā persona.
- Kopuma etiķešu drukāšana ir jākonfigurē un dažām etiķetēm jābūt ģenerētām, kā aprakstīts sadaļā [Konfigurēt kopuma etiķešu drukāšanu](../warehousing/configure-wave-label-printing.md).

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Lietošanas gadījums 2.1: ir saskrāpēta viena kopuma etiķete, un tā ir jādrukā atkārtoti.

1. Piesakieties noliktavas programmā kā lietotājs, ar piekļuvi *62* noliktavai. (Standarta demonstrācijas datos var pieteikties, izmantojot lietotāja ID *62* un paroli *1*.)
1. Dodieties uz **Izejošs \> Atkārtoti drukāt vienu kopuma etiķeti**.
1. Ievadiet vai noskenējiet kopuma etiķetes ID.
1. Atlasiet printeri, uz kura drukāt atkārtoti.
1. Lai apstiprinātu darbību, atlasiet **Labi**.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Lietošanas gadījums 2.2: viena krājuma kastu vairākas etiķetes tika bojātas, un tās ir jādrukā atkārtoti. Katrai etiķetei ir preces svītrkods, bet nav uzskaitījuma vai SSCC numura.

1. Piesakieties noliktavas programmā kā lietotājs, ar piekļuvi *62* noliktavai. (Standarta demonstrācijas datos var pieteikties, izmantojot lietotāja ID *62* un paroli *1*.)
1. Dodieties uz **Izejošs \> Atkārtota etiķešu drukāšana (Krājums)**.
1. Ievadiet vai noskenējiet sūtījuma ID.
1. Atlasiet elementu, kam ir pareizais etiķešu rullis atkārtotai drukāšanai.
1. Skenējiet preces svītrkodu no esošas etiķetes, lai apstiprinātu, ka ir atlasīta pareizā rinda.
1. Ievadiet atkārtoti drukājamo etiķešu skaitu.
1. Atlasiet printeri, uz kura drukāt atkārtoti.
1. Lai apstiprinātu darbību, atlasiet **Labi**.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Lietošanas gadījums 2.3: printerī iesprūduša papīra dēļ, vairākas kastu etiķetes netika izdrukātas. Tā kā etiķetēm ir uzskaitījums, varat definēt atkārtoti drukājamo kastu diapazonu.

1. Piesakieties noliktavas programmā kā lietotājs, ar piekļuvi *62* noliktavai. (Standarta demonstrācijas datos var pieteikties, izmantojot lietotāja ID *62* un paroli *1*.)
1. Dodieties uz **Izejošs \> Atkārtota etiķešu drukāšana (Uzskaitījums)**.
1. Ievadiet vai noskenējiet sūtījuma ID.
1. Atlasiet elementu, kam ir pareizais etiķešu rullis atkārtotai drukāšanai.
1. Ievadiet pirmo kasti, kam atkārtoti drukāt etiķeti.
1. Ievadiet pēdējo kasti, kam atkārtoti drukāt etiķeti. Vai arī atstājiet šo lauku tukšu, lai atkārtoti drukātu etiķetes visām kastēm pēc norādītās pirmās kastes.
1. Atlasiet printeri, uz kura drukāt atkārtoti.
1. Lai apstiprinātu darbību, atlasiet **Labi**.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Lietošanas gadījums 2.4: printerī iesprūduša papīra dēļ, vairākas kastu etiķetes netika izdrukātas. Pēdējai derīgajai etiķetei ir kopuma etiķetes ID, kas tiek drukāts kā svītrkods.

1. Piesakieties noliktavas programmā kā lietotājs, ar piekļuvi *62* noliktavai. (Standarta demonstrācijas datos var pieteikties, izmantojot lietotāja ID *62* un paroli *1*.)
1. Dodieties uz **Izejošs \> Atkārtota etiķešu drukāšana (pēc pēdējā)**.
1. Ievadiet vai noskenējiet sūtījuma ID.
1. Atlasiet elementu, kam ir pareizais etiķešu rullis atkārtotai drukāšanai.
1. Ievadiet vai noskenējiet kopuma etiķetes ID no pēdējās derīgās kopuma etiķetes. Programma nākamo etiķeti secībā identificē kā pirmo kasti, kurai atkārtoti tiks drukāta etiķete.
1. Ievadiet pēdējo kasti, kam atkārtoti drukāt etiķeti. Vai arī atstājiet šo lauku tukšu, lai atkārtoti drukātu etiķetes visām kastēm pēc norādītās pirmās kastes.
1. Atlasiet printeri, uz kura drukāt atkārtoti.
1. Lai apstiprinātu darbību, atlasiet **Labi**.

## <a name="scenario-3-short-pick-and-reprint"></a>3. scenārijs: saīsināta izdošana un atkārtota drukāšana

Pirms sākat strādāt ar šo scenāriju, ir jābūt ieviestiem šādiem priekšnoteikumiem:

- Ir jābūt instalētiem demonstrācijas datiem un ir jāatlasa **USMF** juridiskā persona.
- Kopuma etiķešu drukāšana ir jākonfigurē un dažām etiķetēm jābūt ģenerētām, kā aprakstīts sadaļā [Konfigurēt kopuma etiķešu drukāšanu](../warehousing/configure-wave-label-printing.md).

### <a name="set-up-work-exceptions"></a>Iestatīt darba izņēmumus

Darba izņēmumi kontrolē saīsinātās izdošanas darbību. Veiciet tālāk norādītās darbības, lai iestatītu darba izņēmumu.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Darbs \> Darba izņēmumi**.
1. Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:

    - **Darba izņēmuma kods:** *Saīsināta izdošana un drukāšana*
    - **Izņēmuma veids:** *Saīsināta izdošana*
    - **Ieteikt kopuma etiķešu atkārtotu drukāšanu:** *Jā*

### <a name="void-and-reprint-after-a-short-pick"></a>Anulēt un atkārtoti drukāt pēc saīsinātās izdošanas

1. Piesakieties noliktavas programmā kā lietotājs, ar piekļuvi *62* noliktavai. (Standarta demonstrācijas datos var pieteikties, izmantojot lietotāja ID *62* un paroli *1*.)
1. Atveriet darba apstrādes plūsmu pārdošanas pasūtījuma darbam, kas tika izveidots, sākotnēji drukājot kopuma etiķetes.
1. Atlasiet **Saīsināta izdošana**.
1. Atlasiet darba izņēmuma kodu, ko izveidojāt šim scenārijam.
1. Atlasot pareizo izņēmumu, ir jābūt pieejamai izvēles rūtiņai **Anulēt un atkārtoti drukāt**. Atzīmējiet šo lodziņu un apstipriniet. Pēc apstiprināšanas tiek pārrēķināta etiķetes ruļļa secība, kas tiek identificēta ar lauka **Etiķešu kompilācijas ID**, pamatojoties uz mainīto darba rindas daudzumu. Pēc tam tas tiek atkārtoti drukāts norādītajā printerī.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]