---
title: Kvalitātes pārvaldības testa grupas
description: Šajā tēmā ir aprakstīts, kā izveidot testa grupas, lai ar kvalitātes pasūtījumiem varētu tikt izmantoti vairāki testi Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 020a610e6a7e4d4b35ceb176d542bae32503a615
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021760"
---
# <a name="quality-management-test-groups"></a>Kvalitātes pārvaldības testa grupas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot testa grupas, lai ar kvalitātes pasūtījumiem varētu tikt izmantoti vairāki testi Microsoft Dynamics 365 Supply Chain Management.

Izmantojiet lapu **Testa grupas**, lai iestatītu, rediģētu un apskatītu testu grupas un atsevišķus testus, kas ir piešķirti tiem. Augšējā lapas daļā ir parādītas testu grupas, bet apakšējā daļā ir parādīti testi, kas piešķirti atlasītajai testu grupai.

Jūs piešķirat vairākus ierobežojumus testu grupai, tādus kā iztveršanas plānu, pieņemamu kvalitātes līmeni (AQL) un destruktīvās testēšanas pieprasījumu. Tad, kad atsevišķu testu piešķirat testu grupai, jūs definējat papildu informāciju, piemēram, secību, dokumentus un derīguma datumus. Kvantitatīvam testam jūsu definēta informācija ietver arī pieņemamās mērījumu vērtības. Kvalitatīvam testam šī informācija ietver testa mainīgo un noklusējuma iznākumu.

Testa grupa, kas ir piešķirta kādam kvalitātes pārbaudes pasūtījumam, nosaka noklusējuma kopu ar testiem, kas ir jāizpilda norādītajam krājumam. Taču kvalitātes pārbaudes pasūtījumā testus varat pievienot, dzēst vai mainīt. Katra testa rezultāti tiek uzrādīti kvalitātes pasūtījumā.

Definējot testa grupu, varat pēc izvēles norādīt krājumu iztveršanu. Krājumu iztveršana tiek izmantota, lai noteiktu testējamā produkta daudzumu. Papildinformāciju skatiet [Kvalitātes pārvaldības krājumu iztveršana](quality-item-sampling.md). Jūs varat arī norādīt, vai testi testu grupā ir destruktīvi. Destruktīvā testā krājumu iztveršana tiek iznīcināta un daudzums tiek izņemts no rīcībā esošiem krājumiem.

## <a name="example-of-a-test-group"></a>Testa grupas piemērs

Ražošanas uzņēmums definē testu grupu katrai tās kvalitātes vadlīniju variācijai. Dažādās testu grupas parāda atšķirības iztveršanas plānos, kopā izpildāmo testu kopās, pieņemamajos kvalitātes līmeņos AQL un citos faktoros. Kvantitatīvajiem testiem pastāv arī pieņemamo mērījumu vērtību atšķirības. Lai ieviestu savas kvalitātes vadlīnijas, uzņēmums piešķir testa grupu katram noteikumam, kas tiek izmantots, lai automātiski izveidotu kvalitātes pasūtījumus lapā **Kvalitātes saistības**. Tas arī piešķir testu grupu kvalitātes pārbaudes pasūtījumiem, kas ir izveidoti manuāli.

## <a name="create-a-test-group"></a>Testa grupas izveide

Lai izveidotu testa grupu, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Testa grupas**.
1. Darbību rūtī atlasiet **Jauns**, lai režģim pievienotu rindu augšējā lapas daļā. Jaunajā rindā iestatiet šādus laukus:

    - **Testa grupa** – ievadiet unikālu ID vai nosaukumu testa grupai.
    - **Apraksts** — ievadiet testa grupas detālizēto aprakstu.
    - **Pieņemamais kvalitātes līmenis** – ievadiet testa rezultātu kopējo procentuālo daudzumu, kas jāiztur, lai testu grupu uzskatītu par izturētu.
    - **Krājumu iztveršana** – atlasiet krājumu iztveršanu. Papildinformāciju skatiet [Kvalitātes pārvaldības krājumu iztveršana](quality-item-sampling.md).
    - **Destruktīvs** – atzīmējiet šo izvēles rūtiņu, lai norādītu, ka testa grupa novērtēs krājumus, kas tiek testēti.

1. Kamēr jaunā rinda joprojām ir atlasīta, atlasiet cilni **Vispārīgi** lapas augšējā daļā. Daži cilnē **Pārskats** atlasītās testu grupas iestatījumi tiek atkārtoti šeit. Turklāt grupai var iestatīt šādus laukus:

    - **Atjauniniet krājumu partijas atribūtu** - Kad iestatāt šo opciju kā *Jā*, tas automātiski tiks iestatīts uz *Jā* katram jaunam testam, kas tiek pievienots testu grupai lapas apakšējā daļā.
    - **Atjaunināt partijas izvietojumu** - Kad iestatāt šo opciju uz *Jā*, ja krājums, kas tiek testēts, ir partijas kontrolēts, partijas izvietojums tiks automātiski atjaunināts ar vērtību, kas atlasīts lauks **Kvalitātes pasūtījuma partijas izvietojums neizdevās** vai **Kvalitātes pasūtījuma partijas izvietojums izdevās**.
    - **Kvalitātes pasūtījuma partijas izvietojums neizdevās** — atlasiet partijas atgriešanas kodu, kas ir jāpiešķir, kad kvalitātes pasūtījums, kas ietver šo testa grupu, neizdodas, jo tas neatbilst AQL.
    - **Kvalitātes pasūtījuma partijas izvietojums izdevās** — atlasiet partijas atgriešanas kodu, kas ir jāpiešķir, kad kvalitātes pasūtījums, kas ietver šo testa grupu, izdodas, jo tas atbilst AQL.
    - **Atjaunināt krājumu statusus** - iestatot šo opciju uz *Jā*, ja testējamā krājuma noliktavas dimensiju grupā krājumam ir iespējots **Krājumu statuss**, statuss automātiski tiks atjaunināts ar statusu, kas ir atlasīts laukā **Nesekmīga kvalitātes pārbaudes pasūtījuma statuss** vai **Veiksmīga kvalitātes pārbaudes pasūtījuma statuss**.
    - **Nesekmīga kvalitātes pārbaudes pasūtījuma statuss** — atlasiet krājumu statusu, kas ir jāpiešķir krājumam, kad kvalitātes pasūtījums, kas ietver šo testa grupu, neizdodas, jo tas neatbilst AQL.
    - **Vekmīga kvalitātes pārbaudes pasūtījuma statuss** — atlasiet krājumu statusu, kas ir jāpiešķir krājumam, kad kvalitātes pasūtījums, kas ietver šo testa grupu, izdodas, jo tas atbilst AQL.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Pievienot kvalitatīvo testu testa grupai

Lai pievienotu kvalitatīvo testu testa grupai, rīkojieties šādi.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Testa grupas**.
1. Lapas augšējā daļā cilnē **Pārskats** atlasiet testa grupu, kurai vēlaties pievienot testu.
1. Lapas apakšējā daļā cilnē **Pārskats** rīkjoslā atlasiet **Pievienot**, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādus laukus:

    - **Kārtas numurs** – ievadiet veselu skaitli, lai norādītu kārtību, kādā jāveic testi. Testi, kuriem ir mazāki sērijas numuri, tiks veikti pirms testiem, kuriem ir lielāki sērijas numuri.

        > [!NOTE]
        > Ieteicams atstāt atstarpi starp sērijas numuriem. Piemēram, pirmajam testam iestatiet lauku **Kārtas numurs** uz *10* un tad palieliniet vērtību par 10 katram papildu testam. Šādā veidā jaunus testus varat pievienot vēlāk bez dzēšanas un no jauna izveidot rindas, lai ievietotu tos vēlamajā secībā.

    - **Tests** - Atlasiet veicamo testu. Kvalitātes testam atlasiet testu, kur lauks **Veids** ir iestatīts uz *Opcija*.
    - **Efektīvs** - Atlasiet pirmo datumu, kad tests ir derīgs. Ja atstājiet šo lauku tukšu, tad nav limita.
    - **Derīguma termiņš** - Atlasiet pēdējo datumu, kad tests ir derīgs. Ja atstājat šo lauku tukšu vai iestatāt to uz *Nekad*, tad limita nav.
    - **Testa vērtības noteikšana** – atlasiet, kā jānosaka AQL, ja vienam testam tiek ierakstīti vairāki rezultāti. Kvalitatīvam testam var atlasīt tikai opciju *Manuāls*. Atlasot vienu no citām vērtībām (*Vidējais*, *Minimāls* vai *Maksimāls*), saglabājot testu grupu, saņemsit kļūdas ziņojumu.
    - **Atribūts** – ja partijas atribūtam vēlaties ierakstīt testa rezultātus, šeit atlasiet atribūtu un atzīmējiet izvēles rūtiņu **Atjaunināt krājuma partijas atribūtu**.
    - **Atjaunināt krājuma partijas atribūtu** – atzīmējiet šo izvēles rūtiņu, lai ierakstītu testa rezultātus partijas atribūtam, kas atlasīts laukā **Atribūts**.

1. Lapas apakšējā daļā izvēlieties cilni **Vispārīgi**. Daži cilnē **Pārskats** atlasītie testa iestatījumi tiek atkārtoti. Turklāt testam var iestatīt šādus laukus:

    - **Analīzes sertifikāta pārskats** – iestatiet šo opciju kā *Jā*, lai norādītu, ka testa rezultāti jādrukā analīzes sertifikātā (CoA). Šo pārskatu var veidot no kvalitātes pārbaudes pasūtījuma.
    - **Rīcība kļūmes gadījumā** - atlasiet *Akceptēt* vai *Neizdodas*, lai norādītu, vai tests izdevās vai neizdevās, ja tam nav izpildīts AQL.
    - **Pieņemamais kvalitātes līmenis** – ievadiet testa rezultātu kopējo procentuālo daudzumu, kas jāiztur, lai testu uzskatītu par izturētu.

1. Lapas apakšējā daļā cilnē **Tests** iestatiet šādus laukus:

    - **Mainīgais** - atlasiet testa mainīgo, lai reģistrētu kvalitatīvā testa rezultātus.
    - **Noklusējuma rezultāts** – atlasiet noklusējuma rezultātu, kas jāieraksta testa rezultātiem.
    - **Testa instruments** – atlasiet ierīci, kas jāizmanto testam. Ja ir definēts testa instruments, tas tiek automātiski ievadīts testam testu grupā.

1. Aizvērt lapu.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Pievienot kvantitatīvo testu testa grupai

Lai pievienotu kvantitatīvo testu testa grupai, rīkojieties šādi.

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes kontrole \> Testa grupas**.
1. Lapas augšējā daļā cilnē **Pārskats** atlasiet testa grupu, kurai vēlaties pievienot testu.
1. Lapas apakšējā daļā cilnē **Pārskats** rīkjoslā atlasiet **Pievienot**, lai režģim pievienotu rindu. Jaunajā rindā iestatiet šādus laukus:

    - **Kārtas numurs** – ievadiet veselu skaitli, lai norādītu kārtību, kādā jāveic testi. Testi, kuriem ir mazāki sērijas numuri, tiks veikti pirms testiem, kuriem ir lielāki sērijas numuri.

        > [!NOTE]
        > Ieteicams atstāt atstarpi starp sērijas numuriem. Piemēram, pirmajam testam iestatiet lauku **Kārtas numurs** uz *10* un tad palieliniet vērtību par 10 katram papildu testam. Šādā veidā jaunus testus varat pievienot vēlāk bez dzēšanas un no jauna izveidot rindas, lai ievietotu tos vēlamajā secībā.

    - **Tests** - Atlasiet veicamo testu. Kvantitatīvām testam atlasiet testu, kur lauks **Veids** ir iestatīts uz *Daļskaitlis* vai *Vesels skaitlis*.
    - **Efektīvs** - Atlasiet pirmo datumu, kad tests ir derīgs. Ja atstājiet šo lauku tukšu, tad nav limita.
    - **Derīguma termiņš** - Atlasiet pēdējo datumu, kad tests ir derīgs. Ja atstājat šo lauku tukšu vai iestatāt to uz *Nekad*, tad limita nav.
    - **Testa vērtības noteikšana** – atlasiet, kā jānosaka AQL, ja vienam testam tiek ierakstīti vairāki rezultāti. Pieejamās opcijas ir *Vidējais*, *Minimāls*, *Maksimāls* un *Manuāls*.
    - **Atribūts** – ja partijas atribūtam vēlaties ierakstīt testa rezultātus, šeit atlasiet atribūtu un atzīmējiet izvēles rūtiņu **Atjaunināt krājuma partijas atribūtu**.
    - **Atjaunināt krājuma partijas atribūtu** – atzīmējiet šo izvēles rūtiņu, lai ierakstītu testa rezultātus partijas atribūtam, kas atlasīts laukā **Atribūts**.

1. Lapas apakšējā daļā izvēlieties cilni **Vispārīgi**. Daži cilnē **Pārskats** atlasītie testa iestatījumi tiek atkārtoti. Turklāt testam var iestatīt šādus laukus:

    - **Analīzes sertifikāta pārskats** – iestatiet šo opciju kā *Jā*, lai norādītu, ka testa rezultāti jādrukā CoA. Šo pārskatu var veidot no kvalitātes pārbaudes pasūtījuma.
    - **Rīcība kļūmes gadījumā** - atlasiet *Akceptēt* vai *Neizdodas*, lai norādītu, vai tests izdevās vai neizdevās, ja tam nav izpildīts AQL.
    - **Pieņemamais kvalitātes līmenis** – ievadiet testa rezultātu kopējo procentuālo daudzumu, kas jāiztur, lai testu uzskatītu par izturētu.

1. Lapas apakšējā daļā cilnē **Tests** iestatiet šādus laukus:

    - **Standarta** – ievadiet summu (veselu skaitli vai daļskaitli), kas paredzama testa rezultātiem. Ievadītā vērtība tiks ievadīta testa rezultātos pēc noklusējuma. Turklāt tā automātiski tiks ievadīta kā noklusētā vērtība laukos **Min** un **Maks**.
    - **Min** – ievadiet minimālo atļauto vērtību testa rezultātiem. Ievadītai vērtībai jābūt mazākai par laukā **Standarta** iestatīto summu. Atjauninot lauku **Min**, lauks **Min. tolerance (%)** tiek atjaunināts automātiski. Tāpat, atjauninot lauku **Min. tolerance (%)**, lauks **Min** tiek atjaunināts automātiski.
    - **Maks** – ievadiet maksimālo atļauto vērtību testa rezultātiem. Ievadītai vērtībai jābūt lielākai par laukā **Standarta** iestatīto summu. Atjauninot lauku **Maks**, lauks **Maks. tolerance (%)** tiek atjaunināts automātiski. Tāpat, atjauninot lauku **Maks. tolerance (%)**, lauks **Maks** tiek atjaunināts automātiski.
    - **Testa instruments** – atlasiet ierīci, kas jāizmanto testam. Ja ir definēts testa instruments, tas tiek automātiski ievadīts testam testu grupā.

1. Aizvērt lapu.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības testa instrumenti](quality-management-processes.md)
- [Kvalitātes pārvaldības testi](quality-management-processes.md)
- [Kvalitātes pārvaldības testa mainīgie](quality-management-processes.md)
- [Kvalitātes piesaistes](quality-management-processes.md)
- [Partijas atribūti](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
