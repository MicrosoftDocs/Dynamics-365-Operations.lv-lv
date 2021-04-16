---
title: Konteinerizēšana
description: Šajā tēmā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā . Automatizētā konteinerizēšana kopuma apstrādāšanas laikā sūtījumiem izveido konteinerus un izdošanas darbu.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3546547bd064835d195a2c6ac7e4eb1d5afc9b00
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838110"
---
# <a name="containerization"></a>Konteinerizēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā automatizēt kravu konteinerizēšanu sadaļā . Automatizētā konteinerizēšana kopuma apstrādāšanas laikā sūtījumiem izveido konteinerus un izdošanas darbu.

Lai iestatītu konteinerizēšanu, ir jāizveido tālāk aprakstītie vienumi:

- **Konteinera veids** ─ norādiet konteineru fiziskās īpašības. Izmantojiet konteineru tipus, lai krājumu vienības iepakotu noteikta tipa un lieluma iepakojumos, piemēram, tvertnēs vai paletēs.
- **Konteinera grupas** ─ izveidojiet grupas no līdzīgiem konteineru tipiem. Konteineru grupas var iekļaut, piemēram, konteineru tipus ar līdzīgiem izmēriem. Konteineru grupa norāda secību, kādā konteineri tiek iepakoti, kā arī katra konteinera aizpildes vērtību procentos.
- **Konteinera būvējuma veidne** ─ Izveidojiet veidnes, kas nosaka konteineriizēšanas noteikumus. Piemēram, krājumu kombinēšanas un citu iepakošanas stratēģiju kārtulas.
- **Kopuma veidnes** — iestatiet vienu vai vairākas kopumu veidnes, lai konteinerizēšanai izveidotu izdošanas darbu.

## <a name="create-wave-templates-for-containerization"></a>Kopuma veidnes izveide konteinerizēšanai

Konteinerizēšanai jums ir jāiestata viena vai vairākas sūtījumu kopumu veidnes. Kopuma veidnes ietver kritērijus, kas nosaka tālāk aprakstītās īpašības:

- Kā kopumi tiek apstrādāti. Tas var notikt manuāli vai automātiski.
- Kā tiek izveidots izdošanas darbs. To nosaka kopuma metodes. Kopuma veidnei ir jāietver **konteinerizēšanas** metode.
- Kā krājumi vai sadalījuma rindas tiek saskaņotas ar kopumu.

Papildu informāciju skatiet [Kopuma veidnes](wave-templates.md).

## <a name="create-container-types"></a>Izveidot koneineru tipus

Izmantojiet konteineru tipus, lai izveidotu konteineru aprakstus, tostarp maksimālās vērtības fiziskajiem izmēriem un celtspējai. Kad tiek apstrādāts konteinerizēts kopums, tiek izveidoti konteineri, pamatojoties uz konteinera tipa informāciju.

Lai iestatītu konteinera tipu, izpildiet tālāk aprakstītās darbības:

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Konteineri** \> **Konteineru veidi**.
1. Atlasiet **Jauns**, lai izveidotu jaunu konteinera veidu.
1. Ievadiet unikālu konteinera tipa identifikatoru (ID) un aprakstu.
1. Laukā **Taras svars** ierakstiet faktisko vai prognozēto konteinera svaru.
1. Laukā **Maksimālais svars** ierakstiet maksimālo svaru, ko šādā konteinerā var ievietot.
1. Laukos **Konteinerizēšanas maksimālais apjoms**, **Konteinerizēšanas maksimālais garums**, **Konteinerizēšanas maksimālais platums** un **Konteinerizēšanas maksimālais augstums** norādiet konteinera fiziskās dimensijas.

    > [!NOTE]
    > Garuma un platuma vērtības var savstarpēji mainīt. Tas nozīmē, ka krājumu varat grozīt gareniski jeb pa x asi, ja nepieciešams. Piemēram, ja ilgums ir 2 pēdas un platums ir 1 pēda, garumu varat mainīt uz 1 pēdu un platumu — uz 2 pēdām. Ņemiet vērā, ka tas neattiecas uz augstuma izmēriem. Augstuma vērtību nevarat mainīt, lai krājumu grozītu vertikāli.

1. Neobligāti: atribūtu laukos atlasiet konteineram pielāgotas atribūtu vērtības. Atribūti ir pielāgotas vērtības, kas tiek izmantotas krājumu filtrēšanai vai kārtošanai, ņemot vērā vērtību, kas citādi nav pieejama. Piemēram, ja vēlaties iepakot krājumu noteiktam debitoram, varat izveidot atribūtu šī debitora nosaukumam. Izveidojiet atribūtu tipus lapā **Konteineru atribūti**.

## <a name="create-container-groups"></a>Konteineru grupu izveide

Varat iestatīt konteineru tipu loģiskās grupas. Katrai grupai jūs varat norādīt secību, kādā konteineri tiek iepakoti, kā arī katra konteinera aizpildes vērtību procentos. Krājuma izmēru dimensijas tiek izmantotas, lai noteiktu, vai krājumu varēs ievietot konteinerā. Tiek izmantots konteiners, kas ir vistuvāk krājuma izmēru dimensijām. Ja vienā grupā ir vairāki konteineru tipi, ieteicams izveidot secību pēc lieluma, lai lielākais konteiners būtu pirmais, šīs secības 1. numurs, un vismazākais konteiners būtu pēdējais.

Lai iestatītu konteineru grupu, izpildiet tālāk aprakstītās darbības:

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Konteineri** \> **Konteineru grupas**.
1. Atlasiet **Jauns**, lai izveidotu konteinera grupu.
1. Ievadiet unikālu konteineru grupas ID un aprakstu.
1. Kopsavilkuma cilnē **Informācija** noklikšķiniet uz **Jauns**, lai grupai pievienotu konteineru tipu.
1. Laukā **Konteinera veids** atlasiet konteinera veidu.
1. Atlasiet **Pārvietot uz augšu** vai **Pārvietot uz leju**, lai norādītu secību, kādā tiek iepakoti konteineru tipi.

## <a name="create-container-build-templates"></a>Izveidojiet konteinera būvējuma veidni

Varat iestatīt konteinerizēšanas procesa kārtulas, piemēram, krājumu kombinēšanas un citu iepakošanas stratēģiju kārtulas. Varat iestatīt, piemēram, kārtulu, lai darbinieki vienā konteinerā nevarētu iepakot sadalījuma rindas, kas apzīmē pārdošanas pasūtījumus no dažādiem klientiem.

Lai iestatītu konteinera būvējuma veidni, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Konteineri** \> **Konteinera būvējuma veidnes**.
1. Izveidojiet jaunu konteinera būvējuma veidni.
1. Laukos **Konteinerizēšanas nosaukums** un **Secības numurs** ievadiet konteinerizēšanas veidnes nosaukumu un secību, kas atbilst sadalījuma rindām.

    > [!NOTE]
    > Sistēma lieto pirmo veidni, kuras vaicājuma kritērijiem šī sadalījuma rinda atbilst. Tāpēc šī saraksta sākumā ir jānovieto veidne ar visspecifiskākajiem kritērijiem. Jo plašāki ir kritēriji, jo lielāka iespēja, ka sadalījuma rinda šiem kritērijiem atbildīs. Tas var izraisīt rindu piešķiršanu nepareizajam konteineram. Ja nepieciešams, var atlasīt **Pārvietot uz augšu** vai **Pārvietot uz leju**, lai mainītu veidņu secību.

1. Laukā **Konteinera grupas ID** atlasiet konteineru grupu, no kuras izveidot konteinerus.
1. Laukā **Pamata uzziņu veidi** atlasiet vaicājumu tipu, kas noteiks, ko iepakot un uz ko balstīt filtra vaicājumu. Pieejamas šādas opcijas:

      - **Pārdošanas sadalījuma rinda** ─ iepakot sadalījuma rindas, kas ir izveidotas pārdošanas pasūtījumiem.
      - **Pārsūtījuma sadalījuma rinda** ─ iepakot sadalījuma rindas, kas ir izveidotas pārsūtīšanas pasūtījumiem.
      - **Konteiners** ─ iepakot konteineru, kas jau bija izveidots, izmantojot konteinerizēšanas procesu. Šī opcija tiek izmantota, piemēram, ligzdotajiem konteineriem.

        > [!NOTE]
        > Lai izmantotu ligzdošanas konteinerus, konteinerizēšanas metode ir jānorāda kā atkārtojama. Papildu informāciju skatiet [Kopuma veidnes](wave-templates.md).

1. Kopsavilkuma cilnē **Vispārīgi**, laukā **Kopuma darbības kods** ierakstiet kopuma apstrādes metodes unikālo identifikatoru, kas konteinera būvējuma veidni saista ar kopuma veidnes darbībām.
1. Atzīmējiet izvēles rūtiņu **Atļaut dalīto izdošanu**, lai darbiniekiem no darba pasūtījuma krājumus ļautu iepakot atsevišķos konteineros. Šīs opcijas priekšnosacījums — viss daudzums ietilpst šajā konteinerā. Vienmēr tiek izmantota sadalījuma rindas vislielākā mērvienība.
1. Laukā **Iepakot pēc vienības** atlasiet mērvienību, kas apzīmē šo konteineru. Varat norādīt, piemēram, ka kaste ir konteiners. Ja iepakošanu veicat pēc mērvienības, nevarat norādīt arī konteineru grupu, jo mērvienība ir konteiners.
1. Laukā **Konteinera iepakošanas stratēģija** atlasiet izmantojamo iepakošanas stratēģiju. Pieejamas šādas opcijas:

    > [!NOTE]
    > Šī stratēģija attiecas tikai uz pārdošanas sadalījuma rindām un pārsūtīšanas sadalījuma rindām.

      - **Iepakot visos atvērtajos konteineros** — sistēma novērtē, vai sadalījuma rinda ietilpst kādā no konteineriem, kuri tika izveidoti konteinerizēšanas cikla laikā.
      - **Iepakot tikai esošajā konteinerā** — sistēma novērtē tikai vai to, vai sadalījuma rinda ietilpst konteinerā, kurš tika izveidots pēdējais.

1. Atlasiet **Kombinēšanas loģikas pārtraukumpunkti**, lai iestatītu noteikumus iepakošanas sadalījuma rindām konteineros. Varat izveidot, piemēram, kārtulu, kas darbiniekiem ļauj divu dažādu krājumu sadalījuma rindas iepakot vienā konteinerā. Lai definētu kombinēšanas kārtulu, izpildiet tālāk aprakstītās darbības:

    1. Lapā **Kombinēšanas loģikas pārtraukumi** atlasiet **Jauns**.
    1. Laukā **Tabula** atlasiet tabulu, kas ietver lauku, kurš attiecīgajam kombinēšanas loģikas pārtraukumpunktam ir jāizmanto kā kritērijs.
    1. Laukā **Lauka atlase** atlasiet lauku, kurš attiecīgajam kombinēšanas loģikas pārtraukumpunktam ir jāizmanto kā kritērijs.
    1. Atkārtojiet šīs darbības, līdz ir pievienoti visi kombinēšanas loģikas pārtraukumpunktu kritēriji.

    > [!NOTE]
    > Ja izmantojat kombinēšanas loģiku, filtra kritēriju vaicājumā ieteicams kārtot pēc tiem pašiem laukiem. Šādi tiek samazināts izveidoto konteineru skaits.
