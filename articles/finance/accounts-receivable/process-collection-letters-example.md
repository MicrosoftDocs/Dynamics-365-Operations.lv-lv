---
title: Atgādinājuma vēstuļu apstrādes piemērs
description: Šajā tēmā aplūkots piemērs, kas parāda atgādinājuma vēstuļu izveides, drukāšanas un grāmatošanas procesu.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1bb1889e9450685f7b6a5000e2ef81d1a65f1b51
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721820"
---
# <a name="process-collection-letters-example"></a>Atgādinājuma vēstuļu apstrādes piemērs

[!include [banner](../../includes/banner.md)]

Šajā tēmā aplūkots piemērs, kas parāda atgādinājuma vēstuļu izveides, drukāšanas un grāmatošanas procesu. Piemērs ir pamatots uz opciju **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** sadaļā Kredīts un iekasēšana. Tas izmanto datus USMF demonstrācijas uzņēmumā un jaunu debitoru — US-045.

Lai sāktu, pārejiet uz sadaļu **Debitoru parādi \> Debitori \> Visi debitori**, atlasiet **Jauns** un pēc tam ievadiet nepieciešamo informāciju, lai izveidotu debitoru US-045.

Kad esat pabeidzis, izpildiet tālāk minētās darbības.

1. Pārejiet uz sadaļu **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Iestatīt atgādinājuma vēstuļu secību** un iestatiet atgādinājuma vēstuļu secību, kā parādīts tabulā zemāk, kas ir piešķirta debitora grāmatošanas profilam.

|     Atgādinājuma vēstules kods      |     Apraksts                           |     Valūta      |     Galvenais konts        |     Papildmaksa valūtā     |     Minimālais nokavētais        |     Dienu bloķēšana      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     Atgādinājuma vēstule Nr. 1         |     Otrais paziņojums ar papildu maksu        |     USD           |                           |     0.00                  |     0.00                  |     2                 |
|     Atgādinājuma vēstule Nr. 2         |     Otrais paziņojums ar papildu maksu        |     USC           |     403150                |     20.00                 |     10,00                 |     3                 |
|     Iekasēšana                    |     Galīgais paziņojums ar papildu maksu         |     USD           |     403150                |     50.00                 |     100.00                |     15                |

Ilustrācijā zemāk ir parādīta tabulā esošā informācija tā, kā tā būtu redzama lapā **Atgādinājuma vēstules**. 

[![Atgādinājuma vēstuļu secības iestatīšana.](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Tagad jāiestata divi parametri, kas nepieciešami šim piemēram.

2. Pārejiet uz sadaļu **Kredīts un iekasēšana \> Iestatījumi \> Debitoru parādu parametri** un izpildiet tālāk minētās darbības.

    1. Cilnē **Iekasēšana** iestatiet opciju **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** uz **Jā**.
    2. Pārliecinieties, vai lauks **Izveidot atgādinājuma vēstuli katram** ir iestatīts uz **Debitors**.

    [![Debitoru parādu parametru iestatīšana kredīta iekasēšanai.](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Pārejiet uz sadaļu **Debitoru parādi \> Rēķini \> Visi brīva teksta rēķini**, atlasiet **Jauns** un pēc tam izpildiet tālāk minētās darbības.

    1. Laukā **Debitora konts** atlasiet **US-045**.
    2. Laukā **Rēķina datums** ievadiet **1/15/2021**.
    3. Laukā **Apmaksas datums** ievadiet **1/16/2021**.
    4. Kopsavilkuma cilnes **Rēķina rindas** laukā **Galvenais konts** ievadiet **401100**.
    5. Laukā **Vienības cena** ievadiet **500.00**.
    6. Atlasiet **Grāmatot**.

    Tagad jāievada divas debitora kredīta notas.

4. Atlasiet **Jauns**, tad veiciet šādas darbības:

    1. Laukā **Debitora konts** atlasiet **US-045**.
    2. Laukā **Rēķina datums** ievadiet **1/15/2021**.
    3. Laukā **Apmaksas datums** ievadiet **1/16/2021**.
    4. Kopsavilkuma cilnes **Rēķina rindas** laukā **Galvenais konts** ievadiet **401100**.
    5. Laukā **Vienības cena** ievadiet **-100,00**.
    6. Atlasiet **Grāmatot**.

5. Atkārtojiet 4. darbību, bet ievadiet **-200,00** laukā **Vienības cena**.
6. Pārejiet uz **Debitoru parādi \> Debitori \> Visi debitori** un atlasiet debitoru **US-045**. Pēc tam Darbību rūtī atlasiet **Darījumi \> Darījumi**, lai pārskatītu debitora darbības, ko iepriekš iegrāmatojāt.

    [![Grāmatoto debitoru darījumu pārskatīšana.](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Tagad jāizveido atgādinājuma vēstules debitoram US-045.

7. Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Izveidot atgādinājuma vēstules** un izpildiet tālāk minētās darbības.

    1. Iestatiet opcijas **Rēķins** un **Kredīta nota** uz **Jā**.

        Pēc noklusējuma laukam **Atgādinājuma vēstules** jābūt iestatītam uz **Atgādinājums katram debitoram**.

    2. Laukā **Atgādinājuma vēstules datums** ievadiet **1/19/2021**.
    3. Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrēt** un pēc tam laukā **Debitora konts** pievienojiet debitoru **US-045**.
    4. Atlasiet **Labi**.
    5. Atlasiet **Labi**, lai izveidotu atgādinājuma vēstules.

8. Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Pārskatīt un apstrādāt atgādinājuma vēstules** un izpildiet tālāk minētās darbības.

    1. Ņemiet vērā, ka atgādinājuma vēstules kods gan virsrakstā, gan darbības rindās ir **1. atgādinājuma vēstule**, jo šī atgādinājuma vēstule secībā ir pirmā atgādinājuma vēstule. (Lai skatītu darbību rindas, iespējams, būs jāatlasa kopsavilkuma cilne **Darījumi**.)

   [![Pārbaude, vai galvenē un rindās ir viens un tas pats atgādinājuma vēstules kods.](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Darbību rūtī atlasiet **Grāmatot**.
    3. Laukā **Grāmatošanas datums** ievadiet **1/19/2021**.

    Tagad vēlreiz jāizveido atgādinājuma vēstules debitoram US-045.

9. Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Izveidot atgādinājuma vēstules** un izpildiet tālāk minētās darbības.

    1. Iestatiet opcijas **Rēķins** un **Kredīta nota** uz **Jā**.

        Pēc noklusējuma laukam **Atgādinājuma vēstules** jābūt iestatītam uz **Atgādinājums katram debitoram**.

    2. Laukā **Atgādinājuma vēstules datums** ievadiet **1/23/2021**.
    3. Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrēt** un pēc tam laukā **Debitora konts** pievienojiet debitoru **US-045**.
    4. Atlasiet **Labi**.
    5. Atlasiet **Labi**, lai izveidotu atgādinājuma vēstules.

10. Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Pārskatīt un apstrādāt atgādinājuma vēstules** un izpildiet tālāk minētās darbības.

    1. Ņemiet vērā, ka atgādinājuma vēstules kods galvenē ir **1. atgādinājuma vēstule**. Tomēr kods darījuma rindās ir **2. atgādinājuma vēstule**.

   [![Pārbaude, vai galvenē un rindās ir dažādi atgādinājuma vēstules kodi.](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  Kodi atšķiras, jo opcija **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** ir iestatīta uz **Jā**.

  2. Negrāmatojiet šo atgādinājuma vēstuli.

11. Pārejiet uz sadaļu **Kredīts un iekasēšana \> Iestatīšana \> Debitoru parādu parametri** un pēc tam cilnē **Atgādinājumi** iestatiet opciju **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** uz **Nē**.

    [![Opcijas Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu, iestatīšana uz Nē.](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Tagad vēlreiz jāizveido atgādinājuma vēstules debitoram US-045.

12. Pārejiet uz **Kredīts un iekasēšana \> Atgādinājuma vēstule \> Izveidot atgādinājuma vēstules** un izpildiet tālāk minētās darbības.

    1. Iestatiet opcijas **Rēķins** un **Kredīta nota** uz **Jā**.

        Pēc noklusējuma laukam **Atgādinājuma vēstules** jābūt iestatītam uz **Atgādinājums katram debitoram**.

    2. Laukā **Atgādinājuma vēstules datums** ievadiet **1/23/2021**.
    3. Kopsavilkuma cilnē **Iekļaujamie ieraksti** atlasiet **Filtrēt** un pēc tam laukā **Debitora konts** pievienojiet debitoru **US-045**.
    4. Atlasiet **Labi**.
    5. Atlasiet **Labi**, lai izveidotu atgādinājuma vēstules.

13. Pārejiet uz sadaļu **Kredīts un ieksēšana \> Atgādinājuma vēstule \> Pārskatīt un apstrādāt atgādinājuma vēstules** un ņemiet vērā, ka atgādinājuma vēstules kods gan virsrakstā, gan darbības rindās ir **2. atgādinājuma vēstule**.

    [![Parādīšana vēlreiz, ka galvenē un rindās ir viens un tas pats atgādinājuma vēstules kods.](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Viens un tas pats kods parādās abās vietās, jo opcija **Maksājumu un kredītrēķinu ignorēšana, aprēķinot atgādinājuma vēstules kodu** tagad ir iestatīta uz **Nē**.
