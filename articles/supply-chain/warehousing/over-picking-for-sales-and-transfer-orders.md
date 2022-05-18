---
title: Pārdošanas pasūtījumu un pārsūtīšanas pasūtījumu pārmērīga izdošana
description: Šajā tēmā skaidrots, kā iespējot pārdošanas pasūtījumu un pārsūtīšanas pasūtījumu pārmērīgu izdošanu.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 52a4225efa88a7b9303dd611d5652f59da1612a4
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678413"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Pārdošanas pasūtījumu un pārsūtīšanas pasūtījumu pārmērīga izdošana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir parādīts scenārijs, kurā parādīts, kā iespējot noteiktu darbinieku vai visus darbiniekus pārmērīgai izdošanai. Pārmērīgas izdošanas process ļauj kontrolēt pārmērīgu izdošanu izdošanas laikā.

Noliktavas pārmērīga izdošana ir vienkāršs jēdziens. Sistēma ļauj darbiniekiem izdot vairāk krājumu, nekā norādīts pasūtījumam. Tomēr tas joprojām ņem vērā pasūtījuma pārsniegšanas ierobežojumu, kas ir noteikts rindas līmenī pārsūtīšanas pasūtījumam vai pārdošanas pasūtījumam. Ja šis ierobežojums ir pārsniegts, programma Warehouse Management ziņo darbiniekiem, ka viņi pārsniedz pasūtījuma pārsniegšanas limitu.

Pārmērīgas izdošanas līdzeklis palīdz minimizēt uzturēšanu, kā arī un palīdz iestatījumiem palikt elastīgiem. Varat definēt vienu vai vairākus mobilās ierīces izvēlnes vienumus un iespējot pārmērīgu izdošanu tikai dažiem no tiem. Var arī neļaut atlasītajiem darbiniekiem mainīt izvēlnes krājumus no pārdošanas pasūtījumu un/vai pārsūtīšanas pasūtījumu pārmērīgas izdošanas. Tā vietā varat izslēgt vienu vai abas šīs iespējas atbilstīgos darbinieka iestatījumos.

Pārmērīgās izdošanas līdzeklis var palīdzēt darbiniekiem ietaupīt laiku un darbu, kad viņi saņem un nosūta krājumus. Piemēram, šis līdzeklis ļauj darbiniekiem veikt šos uzdevumus:

- Kompensēt sarukumu izdošanas vai nosūtīšanas laikā.
- Izdošanas laikā neatpakot atsevišķu iepakojuma materiālu.
- Kompensēt krājuma bojājumu transportēšanas laikā.
- Nosūtīt daudzuma vai mērvienības novirzi.
- Samazināt daudzumu pārkāpumus uz numura zīmēm.
- Izvairīties no materiālu atkritumiem un dārgu materiālu trūkuma.
- Mērīt izdoto daudzumu pēc izdošanas (piemēram, izmantojot kravas automašīnas svērumu).

> [!IMPORTANT]
> Pārmērīgas izdošanas līdzeklis attiecas tikai uz pārdošanas pasūtījuma un pārsūtīšanas pasūtījuma izdošanu un apstrādi. Papildināšana neatbalsta pārmērīgu izdošanu. Kad ir palaists papildināšanas darbs, sistēma neļaus lietotājiem veikt pārmērīgu izdošanu.

Šajā tēmā ir parādīts, kā iestatīt un izmantot pārmērīgās izdošanas līdzekli.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Scenārija priekšnosacījums: padarīt pieejamus demonstrācijas datus

Šīs tēmas scenārijā ir atsauces uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Microsoft Dynamics 365 Supply Chain Management. Ja jūs vēlaties izmantot vērtības, kas tiek sniegtas šeit, kad veicat vingrinājumus, pārliecinieties, ka strādājat vidē, kur ir instalēti demonstrācijas dati, un iestatiet juridisko personu *USMF*, pirms sākat darbu.

## <a name="scenario-setup"></a>Scenāriju iestatīšana

Pirms strādājat ar piemēra scenāriju, jums ir jāiespējo pārmērīga izdošana gan attiecīgajam darbiniekam, gan attiecīgajam izvēlnes vienumam.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Iestatīt darbinieku, kam atļaut pārmērīgu izdošanu

Šeit ir vispārīga procedūra darbinieka konfigurēšanai, lai iespējotu pārdošanas pasūtījumu un pārsūtīšanas pasūtījumu pārmērīgu izdošanu atsevišķi. Šī konfigurācija kontrolē, kurš izdošanas darbinieks var veikt pārmērīgu izdošanu, un to, vai darbinieks var veikt pārmērīgu izdošanu gan pārsūtīšanas pasūtījumiem, gan pārdošanas pasūtījumiem.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Nodarbinātais**.
1. Saraksta rūtī atlasiet **Jūlija Funderburka**.
1. Kopsavilkuma cilnē **Lietotāji** atlasiet rindu, kurā ir šādas vērtības. Ja nevienai esošai rindai nav šo vērtību, izveidojiet to.

    - **Lietotāja ID:** *24*
    - **Lietotājvārds:** *WH 24*
    - **Noklusējuma noliktava:** *24*
    - **Izvēlnes nosaukums:** *Galvenā*

1. Kopsavilkuma cilnē **Darbs** iestatiet tālāk norādītās vērtības lietotājam *24*, ja tās vēl nav iestatītas.

    - **Atļaut pārdošanas pārmērīgu izdošanu:** *Jā*
    - **Atļaut pārsūtīšanas pasūtījuma pārmērīgu izdošanu:** *Jā*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Mobilās ierīces izvēlnes vienuma iestatīšana, lai atļautu pārmērīgu izdošanu

Šeit ir vispārīga procedūra mobilās ierīces izvēlnes vienumu konfigurēšanai, lai iespējotu pārmērīgu izdošanu. Atkarībā no jūsu biznesa prasībām tā darbinieka atļauju līmenim, kurš izmantos mobilās ierīces izvēlni, daži parametri var būt ieslēgti vai izslēgti.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Saraksta rūtī atlasiet ierakstu ar nosaukumu *Pārdošnas izdošana*. Ja nevienam esošam ierakstam nav šī nosaukuma, izveidojiet to. Apstipriniet vai iestatiet ierakstam šādas vērtības:

    - **Izvēlnes vienuma nosaukums:** *Pārdošanas izdošana*
    - **Nosaukums:** *Pārdošanas izdošana*
    - **Režīms:** *Darbs*
    - **Izmantot esošo darbu:** *Jā*
    - **Noteikts:** *Lietotāja noteikts*
    - **Ignorēt mērķa noliktavas vienību:** *Jā*
    - **Ignorēt numura zīmi izvietošanas laikā:** *Jā*
    - **Lietotājs, kurš bloķējis darbu:** *Jā*
    - **Atļaut pārmērīgu izdošanu:** *Jā*

> [!IMPORTANT]
> Kad darbiniekam un mobilās ierīces izvēlnes vienumam ir iespējoti atbilstošie parametri, pārmērīgu izdošanu var apstrādāt tikai izmantojot mobilo ierīci.

## <a name="example-scenario"></a>Piemērs

Kad priekšnosacījumi, darbinieka iestatījumi un izvēlnes elementu iestatījumi ir iestatīti, varat strādāt ar šo līdzekli.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Izveidot pārdošanas pasūtījumu, kas ļauj veikt pasūtījuma pārsniegšanu

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**, lai izveidotu jaunu pārdošanas pasūtījumu.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *24*

1. Atlasiet **Labi**.
1. Jaunais pārdošanas pasūtījums ir atvērts. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet rindu, kurai ir šādi iestatījumi:

    - **Krājuma numurs:** *A0001*
    - **Daudzums:** *10*

1. Kopsavilkuma cilnē **Rindas informācija** cilnē **Piegāde** iestatiet **Pārsniegtās piegādes** lauku uz *10*.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Krājumi \> Rezervācija**.
1. Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, lai rezervētu krājumus.
1. Aizveriet lapu **Rezervācija**.
1. Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.

Kad izlaišana ir pabeigta, saņemsiet informatīvus ziņojumus, kas parāda izveidotos kopuma un noslodzes ID.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Iegūt jaunā pasūtījuma darba ID un numura zīmes numuru

Izlaižot pārdošanas pasūtījumu nosūtīšanai uz noliktavu, sistēmai jābūt izveidotam jaunam darba ID, kam ir viena izdošanas rinda. Sekojiet šiem soļiem, lai atrastu darba ID un unikālās noliktavas vienības piešķires.

1. Dodieties uz **Noliktavas pārvaldība \> Darbs \> Darba informācija**.
1. Režģī **Pārskats** meklējiet tikko izveidoto pārdošanas pasūtījuma kolonnu **Pasūtījuma numurs** . Tam pārdošanas pasūtījumam atzīmējiet atbilstošo darba ID.
1. Atlasiet rindu jaunajam pārdošanas pasūtījumam, lai parādītu saistīto informāciju režģī **Rindas** . Atzīmējiet vietu, no kuras tiks izdota vienība.
1. Dodieties uz **Krājumu vadība \> Uzziņas un atskaites \> Rīcībā esošie krājumu saraksts**.
1. Darbību rūtī atlasiet **Dimensijas**.
1. Dialoglodziņā **Dimensiju attēlojums** pārliecinieties, vai ir atzīmētas izvēles rūtiņas **Numura zīme**, **Noliktava** un **Vienuma numurs** un pēc tam atlasiet **Labi**.
1. Rūtī **Filtrs** iestatiet šādus filtrus:

    - **Vienuma numurs** – **ir viens no** – *A0001*
    - **Noliktava** – **sākas ar** – *24*

1. Atlasiet **Lietot**.
1. Atzīmējiet paradītās **Vienuma numurs** vērtības.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Pasūtījuma pārmērīga izdošana, izmantojot mobilo programmu Warehouse Management

1. Pierakstieties Warehouse Management mobile programmā kā lietotājs noliktavā *24*.
1. Doties uz **Izejošs \> Pārdošanas saņemšana**.
1. Laukā **Skenēt darba ID vai numura zīmi** ievadiet pārdošanas pasūtījumam izveidoto darba ID.
1. Atlasiet **Labi** (atzīmes simbols).
1. Atlasiet **Pārmērīga izdošana**.
1. Iestatiet lauku **Izdošanas daudzums** uz *14*.
1. Atlasiet **Labi** (atzīmes simbols).

    Lapā **Pārmērīga izdošana** saņemat šādu ziņojumu: "Rindas pasūtījuma pārsniegšana ir 40,00 procenti, bet atļautā pasūtījuma pārsniegšana ir tikai 10,00 procenti." Šis ziņojums norāda, ka jūsu ievadītais izdošanas daudzums pārsniedz pasūtījuma pārsniegšanas ierobežojumu. Pārdošanas pasūtījumu rindas pasūtījuma pārsniegšanas limits ir 10 procenti. Tāpēc, ja ir noteikts daudzums 10, jūs varat pārmērīgi izdod tikai par 1, ar kopējo izdošanas daudzumu 11.

1. Iestatiet lauku **Izdošanas daudzums** uz *11*.
1. Atlasiet **Labi** (atzīmes simbols).
1. Laukā **Noliktavas vienības identifikators** ievadiet noliktavas vienības identifikatoru, kuru atzīmējāt iepriekšējā sadaļā.
1. Laukā **Mērķa noliktavas vienības identifikators** ievadiet mērķa noliktavas vienības identifikatoru. Ievērojiet, ka tiek rādīta izdošanas vieta (*FLOOR-001*), krājums (*A0001*) un daudzums (*11 gab.*).
1. Atlasiet **Labi** (atzīmes simbols).
1. Pārskatiet informāciju lapā **Pārdošanas pasūtījumi - izvietošana**. Laukam **Vieta** ir jānorāda, ka izdotie krājumi ir jānosūta uz atrašanās vietu *BAYDOOR*.
1. Atlasiet **Labi** (atzīmes simbols).

Lapā **Skenēt darba ID / noliktavas vienības ID** tiek saņemts ziņojums “Darbs pabeigts”. Šis ziņojums norāda, ka pārdošanas pasūtījuma darba ID ir pabeigts un pārmērigi izdotais daudzums nepārsniedz pasūtījuma apjoma pārsniegšanas ierobežojumu 10 procenti.
