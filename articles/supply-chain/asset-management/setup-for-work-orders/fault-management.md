---
title: Kļūmju pārvaldība
description: Šajā tēmā ir izskaidrota kļūmju pārvaldība modulī Līdzekļu pārvaldība.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6665e80342af1baa7176aee92693b77e83b368f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205924"
---
# <a name="fault-management"></a>Kļūmju pārvaldība

[!include [banner](../../includes/banner.md)]

 

Modulī Līdzekļu pārvaldība varat izmantot kļūmju noformētāju, lai līdzekļu tipiem iestatītu kļūmju simptomus, kļūmju apgabalus un kļūmju tipus. Šādi varat pārvaldīt līdzekļos konstatētās kļūdas. Turklāt kļūmju iemeslus un ieteikumus to labošanai var reģistrēt darba pasūtījumā.

Kļūmju reģistrācijas un pārvaldības process ietver trīs darbības.

1. Izveidojiet kļūmju simptomu, kļūmju apgabalu un kļūmju tipu sarakstu, kuri var parādīties jūsu līdzekļu tipos.
2. Kļūmju noformētājā iestatiet simptomus, kļūmju apgabalus un kļūmju tipus.

Tālāk ir sniegti daži piemēri, lai palīdzētu jums izprast atšķirību starp kļūmju simptomiem, kļūmju apgabaliem un kļūmju tipiem.

**Kļūmju simptomi:**

- Nesabalansēti spriegumi
- Īsa shēma
- Troksnis
- Noplūde
- Vibrācijas

**Kļūmju apgabali:**

- Elektrības
- Mehānisks
- Hidraulisks
- Pneimātisks

**Kļūmju tipi**

- Bojāts galvenā statora tinums
- Bojāta diode
- Netīri tinumi
- Defektīvs ģenerators
- Defektīvs sensors

## <a name="create-fault-symptoms"></a>Kļūmju simptomu izveide

Izpildiet tālāk norādītās darbības kļūmju simptomu izveidei, kurus var izmantot kļūmju noformētājā.

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju simptomi**.
2. Atlasiet **Jauns**, lai izveidotu ierakstu.
3. Laukā **Kļūmes simptoms** ievadiet kļūmes simptoma nosaukumu.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Atlasiet **Saglabāt**.

## <a name="create-fault-areas"></a>Kļūmju apgabalu izveide

Izpildiet tālāk norādītās darbības apgabalu vai atrašanās vietu saraksta izveidei, kurus var izmantot kļūmju noformētājā.

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju apgabali**.
2. Atlasiet **Jauns**, lai izveidotu ierakstu.
3. Laukā **Kļūmes apgabals** ievadiet kļūmes apgabala nosaukumu.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Atlasiet **Saglabāt**.

## <a name="create-fault-types"></a>Kļūmju tipu izveide

Izpildiet tālāk norādītās darbības kļūmju tipu saraksta izveidei, kurus var izmantot kļūmju noformētājā.

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju tipi**.
2. Atlasiet **Jauns**, lai izveidotu ierakstu.
3. Laukā **Kļūmes tips** ievadiet kļūmes tipa nosaukumu.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Atlasiet **Saglabāt**.

## <a name="set-up-the-fault-designer"></a>Kļūmju noformētāja iestatīšana

Kļūmju noformētājā līdzekļu tipiem iestatiet kļūmju datus.

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju noformētājs**.
2. Kreisajā rūtī atlasiet līdzekļa tipu, kuram iestatīt kļūmes ierakstu.
3. Cilnē FastTab **Kļūmes simptoms** atlasiet **Pievienot rindu** un pēc tam laukā **Kļūmes simptoms** atlasiet kļūmes simptomu.
4. Cilnē FastTab **Kļūmes apgabals** atlasiet **Pievienot rindu** un pēc tam laukā **Kļūmes apgabals** atlasiet kļūmes apgabalu.
5. Cilnē FastTab **Kļūmes tips** atlasiet **Pievienot rindu** un pēc tam laukā **Kļūmes tips** atlasiet kļūmes tipu.
6. Lai ātri izveidotu kombināciju no visiem esošajiem kļūmju simptomiem, apgabaliem un tipiem atlasītajam līdzekļa tipam, atlasiet **Izveidot kļūmju kombinācijas**. Šī funkcija ir noderīga, ja esat pievienojis daudz kļūmju simptomu, apgabalu un tipu. Ir vieglāk dzēst rindas jebkādām kombinācijām, kas neatbilst līdzekļa tipam, nekā manuāli izveidot jaunas rindas.

    > [!NOTE]
    > Lai kopētu kļūmju simptomu, apgabalu un tipu iestatīšanu no viena līdzekļa tipa uz atlasīto līdzekļa tipu, atlasiet **Kopēt no līdzekļa tipa**.

7. Atlasiet **Saglabāt**, lai saglabātu izmaiņas.

![Kļūmes veidotāja lapa](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Kļūmju iemeslu izveide

Izpildiet tālāk norādītās darbības zināmo kļūmju iemeslu saraksta izveidei, kurus var pievienot darba pasūtījumam vai uzturēšanas pieprasījumam.

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju iemesli**.
2. Atlasiet **Jauns**, lai izveidotu ierakstu.
3. Laukā **Kļūmes iemesls** ievadiet kļūmes iemesla nosaukumu.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Atlasiet **Saglabāt**.

## <a name="create-fault-remedies"></a>Kļūmju novēršanas izveide

Izpildiet tālāk norādītās darbības, lai izveidotu ieteikumus kļūmju novēršanai un labošanai, kurus var pievienot darba pasūtījumam vai uzturēšanas pieprasījumam.

1. Atlasiet **Līdzekļu pārvaldība** \> **Uzstādīšana** \> **Kļūme** \> **Kļūmju novēršana**.
2. Atlasiet **Jauns**, lai izveidotu ierakstu.
3. Laukā **Kļūmes novēršana** ievadiet kļūmes novēršanas nosaukumu.
4. Ievadiet aprakstu laukā **Apraksts**.
5. Atlasiet **Saglabāt**.

> [!NOTE]
> Varat mainīt savu kļūmju simptomu, apgabalu, tipu, iemeslu un novēršanas nosaukumus pēc saviem ieskatiem. Nosaukuma izmaiņas automātiski tiek atspoguļoti atbilstošajās kļūmju reģistrācijās.
