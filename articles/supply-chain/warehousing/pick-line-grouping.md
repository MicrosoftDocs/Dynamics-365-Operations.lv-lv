---
title: Izdošanas rindu grupēšana
description: Šajā tēmā ir sniegts pārskats par izdošanas rindu grupēšanu.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433112"
---
# <a name="pick-line-grouping"></a>Izdošanas rindu grupēšana

[!include [banner](../includes/banner.md)]

Izdošanas rindu grupēšanā vairākas darba rindas, kurām ir viens un tas pats vienums un novietojums, var apvienot vienā savākšanas programmā, kas lietotājam tiek uzrādīta mobilajā ierīcē. Tādējādi noliktavas darbinieki var saņemt visefektīvākos iespējamos norādījumus, bet tiek uzturēta arī nepieciešamā darba līniju nodalīšana sistēmā (piemēram, dažādiem konteineriem un pasūtījumiem).

## <a name="set-up-pick-line-grouping"></a>Izdošanas rindu grupēšanas iestatīšana

### <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide

1. Dodieties uz **Noliktavas pārvaldība \>Iestatījumi \>Mobilās ierīces \>Mobilās ierīces izvēlnes vienumi** un izveidojiet jaunu izvēlnes vienumu ar nosaukumu **Pārdošanas grupas rindas izdošana — lietotāja norādīts**.
2. Sadaļā **Mobilās ierīces izvēlnes vienumi** iestatiet šādas vērtības:

    - Laukā **izvēlnes elementa nosaukums** ievadiet **Pārdošanas izdošana - grupas rinda**.
    - Laukā **Nosaukums** ievadiet **Pārdošanas izdošana - grupas rinda**.
    - Laukā **Režīms** atlasiet **Darba**.
    - Iestatiet opciju **Izmantot esošo darbu** uz **Jā**.

3. Kopsavilkuma cilnē **Vispārīgi** jūs varat iestatīt šādas vērtības:

    - Laukā **Noteica** atlasiet **Noteica lietotājs**.
    - Iestatiet opciju **Ģenerēt pozīcijas unikālo noliktavas vienības identifikatoru** uz **Jā**.
    - Atlasiet opcijas **Grupas izdošana** iestatījumu **Jā**.

4. Kopsavilkuma cilnē **Darba klases** veiciet šīs darbības, lai konfigurētu mobilās ierīces izvēlnes vienumam derīgās darba klases:

    1. Atlasiet **Jauns**.
    2. Laukā **Darba klases ID** atlasiet **Pārdošana** vai **SO izdošana** atkarībā no noliktavas, kuru izmantosiet.
    3. Laukā **Darba pasūtījuma veids** atlasiet **Pārdošanas pasūtījumi**.

### <a name="set-up-a-mobile-device-menu"></a>Mobilās ierīces izvēlnes iestatīšana

1. Dodieties uz **Noliktavas vadība \> Iestatīšana \> Mobilā ierīce \> Mobilās ierīces izvēlne**. 
1. Pievienojiet tikko izveidoto izvēlnes vienumu vēlamajai izvēlnei.

### <a name="set-up-a-work-template"></a>Darba veidnes iestatīšana

1. Doties uz **Noliktavas vadība \> Iestatīšana \> Darbs \> Darba veidnes**.
1. Atrodiet darba veidni, kas jāizmanto ar šo funkciju. Šajā piemērā atlasiet standarta **51 izdot posmam** Contoso darba veidni.
1. Izvēlnē atlasiet **Rediģēt vaicājumu**.
1. Cilnē **Kārtošana** atlasiet **Pievienot** un pēc tam iestatiet šādas vērtības:

    - Laukā **Tabula** atlasiet **Pagaidu darba transakcijas**.
    - Laukā **Atveidotā tabula** atlasiet **Pagaidu darba transakcijas**.
    - Laukā **Lauks** atlasiet **Vienuma numurs**.
    - Laukā **Meklēšanas virziens** atlasiet **Augošā secībā**.

> [!NOTE]
> Lai izdošanas rindu grupēšanas funkcionalitāte darbotos, darba rindas ir jākārto pēc vienuma ID. Ja rindas, kurām ir vienādi vienumi, netiek kārtotas viena pēc otras, tās netiks grupētas.

## <a name="example"></a>Paraugs

### <a name="create-picking-work"></a>Izveidot izdošanas darbu

Pirms varēsiet iestatīt izdošanas rindas grupēšanu, ir jāizveido daži piemēroti izejošie darbi.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
2. Atlasiet **Jauns**, lai izveidotu pārdošanas pasūtījumu. 
3. Laukā **Debitora konts** atlasiet jebkuru debitoru. 
4. Kopsavilkuma cilnes **Vispārīgi** laukā **Noliktava** atlasiet **51**. Tad atl. **Labi**.
5. Sadaļā **Pārdošanas pasūtījuma rindas** pievienojiet šādas sešas rindas:

    - **1. rinda:** laukā **Krājuma numurs**, atlasiet **M9200**. Laukā **Daudzums** ievadiet **3**.
    - **2. rinda:** laukā **Krājuma numurs**, atlasiet **M9201**. Laukā **Daudzums** ievadiet **3**. 
    - **3. rinda:** laukā **Krājuma numurs**, atlasiet **M9202**. Laukā **Daudzums** ievadiet **2**. 
    - **4. rinda:** laukā **Krājuma numurs**, atlasiet **M9200**. Laukā **Daudzums** ievadiet **1**. 
    - **5. rinda:** laukā **Krājuma numurs**, atlasiet **M9200**. Laukā **Daudzums** ievadiet **3**.
    - **6. rinda:** laukā **Krājuma numurs**, atlasiet **M9202**. Laukā **Daudzums** ievadiet **7**. 

    Šeit ir kopsavilkums par kopējiem daudzumiem katram krājumam:

    - **Krājums M9200:** 7 katram
    - **Krājums M9201:** 3 katram
    - **Krājums M9202:** 9 katram

6. Pirms pasūtījumu izdošanas noliktavā jāpārliecinās, vai savākšanas vietās ir pietiekami daudz krājumu visām precēm visos pasūtījumos. Pārskatiet **Atrašanās vietas direktīvas** iestatījumu, lai noteiktu, kuras izdošanas vietas tiek izmantotas pārdošanas pasūtījuma izdošanai.
7. Rezervējiet krājumu un izdodiet to noliktavai. Tiek izveidots darba ID, kuram ir sešas rindas. Rindas tiek kārtotas pēc krājuma koda.

### <a name="run-the-mobile-device-flow"></a>Mobilās ierīces plūsmas palaišana

1. Mobilajā ierīcē atlasiet izvēlni, kurā ir iekļauts jaunais mobilās ierīces izvēlnes vienums.
1. Atlasiet izvēlnes vienumu **Pārdošanas izdošana - Grupas rinda** un iniciējiet izdošanu.

    Kad ir atlasīta izvēlne un ievadīts darba ID, tiek parādīta izdošanas darbība, kurā ir grupētas visas preču M9200 savākšanas rindas. Jūs saņemat instrukciju, lai izvēlētos 7 katram no krājumiem M9200.

1. Apstipriniet izdošanas darbību. 
1. Pārejiet uz darba procesa klienta ekrānu un ievērojiet, ka visas trīs savākšanas rindas krājumam M9200 tika slēgtas vienlaicīgi.

    Uzrāda 4. darba līniju.

1. Apstipriniet izdošanas darbību.

    Pēdējā izdošanas darbība mobilajā ierīcē apkopo pēdējās divas izdošanas rindas no darba pasūtījuma.

1. Pabeidziet izdošanas darbību pa 9 no katra krājuma M9202.
1. Apstipriniet nolikšanas darbību un visus papildu izdošanas/nolikšanas pārus, lai pabeigtu darbu.

> [!NOTE]
> - Darba rindas var grupēt tikai tad, ja tās ir secīgas.
> - Šī funkcionalitāte netiek atbalstīta:
>
>    - Pieļaujamā svara krājumi. Ja darbā ir kādi pieļaujamā svara krājumi, jūs pirms izdošanas uzsākšanas saņemsit kļūdas ziņojumu.
>    - Vienību izdošana.
>    - Darba rindas, kurām ir nepabeigt papildināšanas darbi.
>    - Pārizidošana.
>    - Saīsināta izdošana ar krājuma atkārtotu sadali


[!INCLUDE[footer-include](../../includes/footer-banner.md)]